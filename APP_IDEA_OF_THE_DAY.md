# App Idea of the Day: Counter Cue
Date: 2026-11-14 (Japan)

## Concept
A shared prep timer for small bakeries. A wall tablet shows what needs attention next and which baker has picked it up.

## Target users
Two- to five-person bakery teams that juggle several doughs and trays during the morning shift.

## Problem
A phone timer can ring in a baker's pocket while someone else stands next to the oven. Even when the alarm is heard, a label like “timer 2” doesn't tell the team which tray to check.

## Core workflow
1. A baker starts a labeled timer from a preset and adds the tray or bench location.
2. The wall display moves the due timer to the top with its label and next action.
3. A teammate claims the task, checks the batch, and marks it done or sets a short recheck.

## MVP features
- Reusable duration and action presets.
- Shared board with due, claimed, and completed states.
- One-tap recheck and a visible record of who handled each batch.

## Build approach
Build a mobile web interface and a large-text tablet board backed by a database. Save absolute due times so the countdown can recover after a refresh.

## Validation plan
Shadow two morning shifts, then test with one bakery for a week. Compare unattended alarms and time spent asking which batch a timer belongs to.

## Biggest risk
A busy team may fall back to personal timers if creating a shared timer is slower. Put the common presets on the first screen and test the flow on the actual prep bench.

## Batch handoff
Show a location and verb on each card: “Rack B, tray 2 — check proof.” Claiming a card adds initials but leaves it visible until someone completes it. A baker can release a claim if pulled away; after two minutes, flag the claim as needing a check rather than assuming the action happened.

## Pilot scope
Start with dough rest and proof checks only. Use the bakery's existing oven timers independently during the pilot. Put the wall board where both benches can see it, order due cards by oldest deadline, and pair every color cue with a written status. Make the board readable without sound in a noisy kitchen.

## Synchronization and outages
The server calculates the due time from the preset when a timer starts. Use an atomic update to claim an unclaimed card so simultaneous taps cannot create two owners. If the board loses its connection, keep showing the last known timers with an offline banner, disable edits, and tell the crew to use local timers until the board reconnects and refreshes.
