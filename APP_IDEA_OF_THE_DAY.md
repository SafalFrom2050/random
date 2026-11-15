# App Idea of the Day: Exit Pocket
Date: 2026-11-16 (Japan)

## Concept
A mobile checklist that helps renters remember which fixtures, keys, and accessories to return when moving out.

## Target users
Renters preparing for their first move-out inspection, especially those who have stored original fixtures or swapped them for their own.

## Problem
Original remote controls, shelf pegs, and spare keys can get packed into the wrong box. A generic moving checklist can't tell renters what came with their particular apartment or where they put it.

## Core workflow
1. At move-in or while packing, make a room-by-room list of items to hand back.
2. Add a photo, expected quantity, and current storage spot for each item.
3. Before inspection, open the handover view, reconcile quantities, and review anything still missing.

## MVP features
- Room templates and editable item cards.
- Optional photo and storage note per card.
- Handover view grouped by missing, ready, and handed back.
- Printable summary that works without the app.

## Build approach
Use Flutter and SQLite. Keep records on the device, store compressed photos in app-private storage, and generate the printable summary locally.

## Validation plan
Recruit renters with inspections in the next month. Observe a packing session and a handover rehearsal, then ask which items they would have missed using their usual notes.

## Biggest risk
The app may feel useful only if someone starts using it months before moving out. Test a packing-week workflow that builds the list from an existing inventory and a quick walk-through.
