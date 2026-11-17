# App Idea of the Day: Thread Trail
Date: 2026-11-18 (Japan)

## Concept
A tiny project journal that helps knitters resume an unfinished piece without guessing where they stopped.

## Target users
Casual knitters who rotate between several projects or leave long gaps between sessions.

## Problem
A row counter gives a number but loses context: which pattern section it belongs to, whether an increase was completed, and what to do next. Reconstructing that state can take longer than the available knitting time.

## Core workflow
1. Create a project with a name and a reference to the pattern.
2. At the end of a session, save the section, last completed row, and next action.
3. On return, read a large resume card and optionally inspect a photo before continuing.

## MVP features
- Project list with a resume card for each piece.
- Row counter scoped to a named section.
- One-tap session checkpoint with a next-action note.
- Optional close-up photo and local export.

## Build approach
Build a Flutter app with SQLite and app-private photo storage. Keep the first release offline and store pattern references as text; users can enter their own short notes without uploading entire patterns.

## Validation plan
Ask eight knitters to use the journal for two weeks across projects they actually pause. Compare time to resume with their normal notes and ask which checkpoint details proved useful.

## Biggest risk
Writing a checkpoint may interrupt the relaxing part of the hobby. Keep it to the last completed row and one next action by default, with other details optional.

## Checkpoint rules
Label the row explicitly as “last completed,” and store the next action separately: “Section B, row 12 completed; next: row 13 increase.” When a repeat restarts, create a new repeat number within that section rather than resetting an unlabeled counter. A photo supports the written checkpoint but never automatically determines the stitch or row count.

## Recovery and storage
Save each checkpoint atomically with its section and repeat number. Keep the previous five checkpoints per project so a mistaken tap can be undone without reconstructing the session. Export a ZIP containing a readable Markdown summary, structured project data, and optional photos; importing it creates a new project to avoid overwriting newer work. Show the timestamp on the resume card so an old checkpoint is easier to notice.

## Pilot decision
For each participant, time one return after a gap of at least two days using their normal notes and two comparable returns using Thread Trail. Record whether they resume correctly without inspecting earlier rows, alongside checkpoint entry time. Continue if at least six of eight participants resume at least 30% faster and median checkpoint entry stays under 15 seconds. Log incorrect resumes separately and review the field labels before expanding the pilot if any occur.
