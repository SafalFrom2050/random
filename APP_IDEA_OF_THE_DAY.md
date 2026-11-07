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
