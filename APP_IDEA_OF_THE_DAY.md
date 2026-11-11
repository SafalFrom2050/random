# App Idea of the Day: Swap Shelf
Date: 2026-11-12 (Japan)

## Concept
A QR-based catalog for a physical free shelf. Visitors can see what is available or mark an item taken without installing an app.

## Target users
Community centers, coworking spaces, and apartment buildings that run a staffed or volunteer-managed giveaway shelf.

## Problem
A shelf can look empty online while being full in person, or advertise items that disappeared days ago. Volunteers have little time to reconcile a spreadsheet.

## Core workflow
1. A steward prints a shelf QR code and adds a few items with short IDs and optional photos.
2. A visitor checks the catalog, finds an item on the shelf, and taps “I took this” using its label.
3. The steward resolves mismatches and clears stale entries during the next shelf check.

## MVP features
- Phone-friendly catalog with item IDs, photos, and last-checked dates.
- Account-free visitor view and a quick take form.
- Steward-only listing and reconciliation controls.
- Printable shelf sign and item labels.

## Build approach
Use a mobile web app with a relational database for shelves, item states, and events. Store compressed images separately. Require sign-in for stewards and scope each catalog to a single shelf.

## Validation plan
Pilot with two existing shelves for three weeks. Compare catalog accuracy and the time stewards spend maintaining it against their previous process.

## Biggest risk
People may take items without updating the catalog. Show when an item was last seen and give stewards a fast way to reconcile multiple entries in one visit.

## Reconciliation rules
Keep “listed,” “reported taken,” and “confirmed removed” separate. Hide reported items from the available view while showing them in the steward queue. A steward can restore an item after seeing it in person. After seven days without a check, move the item to an “availability uncertain” view; do not silently declare it gone.

## At-shelf interaction
Print short, shelf-specific IDs in large text and include the shelf QR on the sign, so visitors need only scan once. The take form shows the matching title and photo before confirmation. Offer a plain URL on the sign and keep the physical shelf usable by people without phones; steward checks cover those pickups.

## Data and permissions
Record the visitor action and item state change in one database transaction. Make repeat submissions for the same item idempotent until a steward restores it, at which point old forms must refresh before submitting. Keep take reports anonymous and rate-limit them per shelf. Only stewards can restore items or edit listings; don't collect pickup names, addresses, or contact details.

## Pilot decision
During the pilot, audit ten randomly selected item statuses per shelf each week against physical inventory. Record false availability and false removal separately, alongside minutes spent on each steward check. Continue only if both shelves reach at least 85% status agreement and the median check takes under five minutes. If accuracy falls short, test a clearer pickup sign before adding reservations or notifications.
