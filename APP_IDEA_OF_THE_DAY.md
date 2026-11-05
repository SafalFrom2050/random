# App Idea of the Day: Setlist Pocket
Date: 2026-11-06 (Japan)

## Concept
A rehearsal planner for amateur bands that turns a setlist into a practical practice session. Give each song a rough duration and mark troublesome sections, then build a rehearsal around the time available.

## Target users
Small bands, school music clubs, and casual ensembles with limited shared rehearsal time.

## Problem
Groups spend valuable rehearsal time deciding what to play. Running whole songs repeatedly can leave difficult transitions untouched, and notes about what needs work get lost between sessions.

## Core workflow
1. Add songs with estimated durations and optional key or tuning notes.
2. Mark sections needing attention, such as “bridge entry” or “ending.”
3. Enter the rehearsal length and reserve time for setup and breaks.
4. Select full-song runs or focused section blocks until the plan fits.
5. During rehearsal, advance through blocks and record short outcomes.
6. Carry unresolved sections into the next session.

Example: A 60-minute booking becomes ten minutes of setup, two focused sections, a short break, and a closing set run.

## MVP features
- Song library and ordered setlists.
- Named problem sections with brief notes.
- Manual rehearsal blocks with estimated durations.
- A running total and clear indication when the plan exceeds the available time.
- Session playback view with optional timer and outcome notes.
- Offline storage and text export.

Keep audio recording, automatic music analysis, cloud collaboration, and venue booking outside the first release.

## Build approach
Build a Flutter app with SQLite for songs, sections, rehearsal plans, and outcomes. Store durations as integer seconds and perform all planning locally.

Let users arrange their own blocks; offer a simple suggestion that prioritizes selected unresolved sections rather than pretending to optimize musical progress. Distinguish planned time from actual elapsed time. Save after each block so interruptions do not erase rehearsal notes.

## Rehearsal behavior and data design
Each block has a type: setup, break, full song, or focused section. A focused section gets its own time budget; its duration is not inferred from the full song.

Starting a session freezes a copy of the plan so later song-library edits cannot alter what the group rehearsed. Each block can be completed, skipped, or left unfinished. An outcome can resolve a problem section or leave it open with a next-step note.

Use a monotonic timer while active, pause on backgrounding, and ask whether to resume or manually add time when returning. Show remaining planned time separately from actual time spent. If a block runs long, offer to shorten or remove later blocks without changing them automatically.

Give songs and sections stable identifiers. Archive a song referenced by past sessions rather than deleting its history. Export a versioned JSON backup in addition to the readable text plan; validate imports before replacing data.

## Validation plan
Pilot with four bands over three rehearsals each. Observe planning time, how often the group follows the plan, and whether unresolved sections remain easy to find. Ask whether the app reduces discussion overhead without making rehearsal feel rigid.

Continue if three bands choose to plan another rehearsal voluntarily and identify a concrete problem section they addressed using the app.

## Biggest risk
A detailed plan may be too rigid for a creative group. Allow instant reorder, skip, and extension of blocks, and make the timer optional. Test whether the plan supports discussion rather than becoming another obligation.

## Possible business model
A free core planner with a one-time upgrade for multiple band libraries and reusable rehearsal templates. Keep text export available to everyone.
