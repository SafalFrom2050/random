# App Idea of the Day: Glaze Grid
Date: 2026-11-08 (Japan)

## Concept
A visual reference for ceramic glaze tests. Map small fired tiles on a grid, photograph the batch, and find the exact test behind a finish worth repeating.

## Target users
Community pottery studios and hobby ceramicists who test glazes on tiles before using them on finished pieces.

## Problem
After firing, tiles can get separated from their notes. A beautiful result is hard to repeat if the clay body, application, or firing batch is unknown.

## Core workflow
1. Create a test batch and assign each tile a short ID.
2. Record the clay body, glaze label, and application notes before firing.
3. Match fired tiles back to their records and photograph the results.
4. Tag promising tiles and pull up the original notes for the next test.

## MVP features
- Batch grid with printable tile IDs for the workbench.
- Search by clay body, glaze, and outcome.
- Before and after photos, plus a shortlist of promising results.
- Offline access and backup export.

## Build approach
Build a Flutter app backed by SQLite and local image files. Model tiles separately from batches so users can compare tests across firings.

## Validation plan
Pilot with two community studios for two firing cycles. Compare how quickly participants can recover a tile's test notes using the app versus their usual method.

## Biggest risk
A record is useless if it points to the wrong tile. Make missing and uncertain matches explicit and keep identity confirmation separate from appearance notes.

## Tile reconciliation
Use an ID marked on the tile with the studio's established method and mirror it on the paper worksheet. Treat grid position as a temporary staging aid because tiles may move. After firing, match by the physical ID. If an ID cannot be read, save a photo as unmatched and keep it out of repeat-test suggestions until a person confirms the match.

## Repeat tests
Create a new test from an existing record with a fresh ID and a field for the intended change, such as trying one additional coat. Show both tiles alongside their respective firing and clay details. Flag when more than one field changed, so the comparison does not imply that one change caused the result.

## Storage and recovery
Use stable internal IDs and enforce unique human-readable tile IDs within each batch. Store thumbnails separately from originals. Package exports as a versioned manifest and images; validate references and reject duplicate IDs before importing. Preserve both records when users explicitly import a conflicting batch as a copy, with a new batch identifier.
