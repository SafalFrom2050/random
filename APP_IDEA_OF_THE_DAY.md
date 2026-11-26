# App Idea of the Day: Market Load
Date: 2026-11-27 (Japan)

## Concept
A packing and return checklist for craft-market sellers that separates sale stock from the display gear needed to run a stall.

## Target users
Solo makers selling at occasional weekend markets with a few crates of products and reusable stall equipment.

## Problem
A stock spreadsheet rarely reminds a seller to bring clips, price signs, or the table covering. After the event, leftover counts and missing display items get mixed together, making the next packing session harder.

## Core workflow
1. Copy a previous market's packing template into a new event.
2. Enter planned stock quantities and check off display equipment as it is loaded.
3. At pack-down, count stock returning and flag missing reusable gear.
4. Review discrepancies before preparing the next event.

## MVP features
- Separate stock and equipment lists.
- Planned, loaded, and returned stock quantities.
- Reusable event templates with one-off additions.
- Offline checklist and printable packing sheet.

## Build approach
Build a Flutter app with SQLite. Snapshot a template into each event so edits do not change past checklists. Use manual quantities and local CSV export, starting with one seller on one device.

## Validation plan
Recruit six makers attending at least two markets. Observe their usual packing process, then test Market Load at their next comparable event. Record forgotten essentials and time spent reconciling returned items.

## Biggest risk
A checklist may add work without improving on a seller's paper routine. Keep equipment checks to one tap and make stock counting optional for sellers who only need packing help.

## Counting rules
Show loaded minus returned as “units not brought back,” not automatically as sales: gifts, samples, damage, and transfers also change the count. Allow sellers to allocate that difference to those reasons or leave it unresolved. Preserve an explicit unknown state for uncounted stock. Keep equipment flags independent from stock arithmetic, and carry unresolved missing gear into the next event as a visible reminder rather than marking it packed by default.

## Pilot decision
Before each event, have the seller identify their essential equipment so forgotten-item counts use a consistent list. Compare baseline and pilot packing time, forgotten essentials discovered at setup, and pack-down reconciliation time. Continue if at least four of six makers reduce forgotten essentials without adding more than five minutes to total preparation and reconciliation. If a seller has no baseline omissions, assess whether they choose to reuse the app at a second event instead of claiming an improvement. Log skipped stock counts separately to decide whether the stock module deserves further work.
