# App Idea of the Day: Puzzle Parking
Date: 2026-11-04 (Japan)

## Concept
A companion for physical jigsaw puzzles that helps people pause a puzzle, pack away loose pieces, and resume without losing their sorting system.

## Target users
Puzzle hobbyists working on shared tables, people with limited space, and households that cannot leave a puzzle spread out for days.

## Problem
Packing away a half-finished puzzle destroys the useful work of sorting pieces into groups. A photo alone does not explain which bag contains the sky pieces or what section someone planned to tackle next.

## Core workflow
1. Create a puzzle project with its title, piece count, and reference photo.
2. Photograph the current board before clearing the table.
3. Create labeled groups such as “dark blue edges” or “window lettering.”
4. Assign each group a bag or tray label and optional photo.
5. Save a short next-step note.
6. On return, open a resume screen showing the board, group locations, and next step.

Example: “Bag C: pale sky pieces; Tray 2: roof sections. Next: connect the two red rooftops.”

## MVP features
- Multiple puzzle projects and progress snapshots.
- Piece-group cards with editable labels and container identifiers.
- A printable sheet of simple lettered container labels.
- A pause checklist and next-step note.
- Search by group description or container.
- Offline storage and project backup export/import.

Keep automatic piece matching, camera-based completion estimates, public collections, and marketplace features outside the first release.

## Build approach
Build a Flutter app with SQLite for projects, snapshots, and groups, plus local image storage. Each pause creates a dated snapshot linked to the active group list.

Use stable group identifiers so renaming a bag does not break its history. Allow groups to be merged or marked used when their pieces join the board. Generate label sheets as PDFs using the same container identifiers shown in the app. Export a versioned JSON manifest with image attachments in a ZIP archive.

## Validation plan
Recruit eight puzzlers who regularly clear their workspace for a two-week pilot.
- Observe one pack-away and restart using their usual method.
- Measure app setup and logging effort during another session.
- Check whether users can locate a requested piece group after several days.
- Track voluntary reuse on later pauses.
- Ask which notes and photos actually helped them resume.

Continue if five participants reuse it voluntarily and report that finding groups is easier without excessive logging. If full inventories are burdensome, narrow the app to a board photo and a few bag labels.

## Biggest risk
Documenting groups may take longer than simply reopening the bags. Make a container letter and photo sufficient, allow bulk capture, and validate time spent during real pack-away sessions before adding detailed tracking.

## Possible business model
Free for a few active puzzles, with a one-time upgrade for unlimited projects and custom label layouts. Keep basic backup export available to everyone.
