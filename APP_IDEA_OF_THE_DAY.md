# App Idea of the Day: Cue Cards
Date: 2026-10-27 (Japan)

## Concept
A rehearsal app for people who need to deliver a short talk without reading a full script. Turn a draft into a handful of cue cards, practice aloud, and gradually hide the prompts as confidence grows.

## Target users
People preparing workplace introductions, morning speeches, class presentations, wedding toasts, or interview opening statements.

## Problem
Memorizing an entire script takes time, while reading it word for word can sound stiff. Ordinary notes do not help a speaker move from full sentences to a few useful reminders.

## Core workflow
1. Paste a short draft or create cards manually.
2. Split the talk into three to six sections and write a short cue for each.
3. Rehearse with full text visible, then switch to cues only.
4. Advance cards by tapping anywhere on a large control.
5. Review elapsed time per card and mark where you lost your place.
6. Repeat with selected cues hidden, revealing them whenever needed.

Example: A one-minute introduction becomes four cards: background, current work, one achievement, and why this role.

## MVP features
- Manual script entry and section splitting.
- Separate full-text and cue fields for each card.
- Full-text, cue-only, and hidden-cue practice modes.
- Session timing with per-card durations.
- A “got stuck here” marker and focused retry.
- Local storage and plain-text export/import.
- Adjustable text size and presentation contrast.

The first release needs no microphone, speech recognition, AI scoring, or account. Timing describes a rehearsal; it does not grade speaking ability.

## Build approach
Build a Flutter app using SQLite for talks, ordered cards, and rehearsal summaries. Maintain an explicit session state with current card, mode, elapsed duration, and pause status.

Use a monotonic clock for timing and pause when the app leaves the foreground. Save progress after each card transition. Keep editing separate from rehearsal so accidental touches cannot change the script. Export talks as versioned JSON and a readable text file.

## Validation plan
Recruit eight people preparing a real talk under three minutes.
- Observe their usual rehearsal method before introducing the app.
- Compare setup effort and ability to finish using cues only.
- Ask whether revealing a hidden cue helps them recover naturally.
- Track voluntary repeat sessions over a week.
- Test large text, interruptions, and accidental taps.

Continue if at least five participants rehearse again voluntarily and report a specific benefit over ordinary notes. Do not infer better public-speaking performance from faster rehearsals alone.

## Biggest risk
Creating cue cards could become extra homework that users abandon. Let people start directly from pasted text, split sections with a simple gesture, and edit cues during review. Validate that setup takes less than two minutes for a one-minute talk before adding automation.

## Possible business model
Free for a few active talks, with a one-time upgrade for unlimited talks and custom practice presets. Keep basic rehearsal and export available to everyone.
