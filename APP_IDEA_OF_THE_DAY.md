# App Idea of the Day: Stitch Ledger
Date: 2026-10-25 (Japan)

## Concept
A knitting and crochet companion that remembers exactly where you stopped in a pattern, including row counts, repeats, yarn changes, and personal corrections.

## Target users
Hobby knitters and crocheters who juggle multiple projects or follow patterns with repeated sections.

## Problem
A basic row counter records a number but loses its meaning. After a break, makers must reconstruct which repeat they were on, whether a shaping step happened, and what they changed from the pattern.

## Core workflow
1. Create a project and enter a small sequence of pattern steps manually.
2. Define repeats, such as “Work these four rows six times.”
3. Tap a large counter after completing a row; show both the current row and repeat.
4. Attach a note or photo to the current step when making a modification.
5. Pause the project and return to a clear “next row” card.
6. Undo an accidental tap or move back when unpicking work.

Example: “Next: row 3 of 4, repeat 5 of 6. Your note: use the larger hook for this section.”

## MVP features
- Multiple projects with independent progress.
- Manually entered sections and a single level of repeats.
- Large accessible counter controls, undo, and explicit backtracking.
- Notes and photos attached to sections.
- A progress timeline distinguishing completed work from corrections.
- Local storage and project export/import.

Keep pattern marketplaces, PDF interpretation, nested repeat logic, and automatic stitch recognition outside the first release.

## Build approach
Build a Flutter app with SQLite and local image storage. Represent a pattern as ordered sections, each containing a row count and repeat count. Store progress changes as events so undo restores the previous position reliably.

Define the displayed position as the next row to work. Advancing from the final row should show a completion screen and allow undo. Save each action immediately and restore the same state after an app restart. Export a versioned JSON manifest with optional image attachments.

## Validation plan
Observe six knitters or crocheters using the app on a small repeated pattern, then let them try it on their own projects for a week.
- Test whether they correctly identify the next row after an interruption.
- Record accidental advances and successful corrections.
- Ask whether setup takes less effort than their current notes.
- Check that backtracking across section boundaries matches real work.
- Measure voluntary use on a second project.

Proceed if at least four participants choose to keep using it and can resume their work without reconstructing progress. Treat this as an initial usability signal.

## Biggest risk
Recording every row may interrupt the craft more than it helps. Make the main control usable with one hand, offer adjustable screen-awake behavior during a session, and let users count whole repeats instead of individual rows. Validate the interaction before adding more pattern logic.

## Possible business model
A free version with two active projects and a one-time upgrade for unlimited projects and custom section templates. Keep basic backup export available to everyone.
