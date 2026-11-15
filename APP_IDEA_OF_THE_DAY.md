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

## Quantity and handover rules
Allow an expected quantity to be unknown until the renter checks the inventory. For a set of three keys where only two are found, show “2 of 3 ready” and keep the missing key visible. Let renters record “handed back” separately after the inspection so a packed item never looks like it has already been returned. Default the printable summary to item names and counts; exclude photos, key markings, and storage locations.

## Pilot decision
Recruit ten renters who have not used the app before and ask each to make a list using their usual method. Then give them ten minutes to try the checklist and compare the two lists against their own move-in inventory or handover instructions. Continue if at least six renters find a confirmed omission or quantity mismatch and at least eight can locate their unresolved items in under 30 seconds. Record omissions suggested by the template separately from those found during the room walk-through to see which part earns its place.
