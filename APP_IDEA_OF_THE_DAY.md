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
