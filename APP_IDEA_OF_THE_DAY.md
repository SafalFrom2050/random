# App Idea of the Day: Borrow Back
Date: 2026-11-24 (Japan)

## Concept
A simple lending ledger for small clubs that tracks borrowed equipment and the accessories that should come back with it.

## Target users
Photography clubs, school activity groups, and neighborhood hobby groups lending a modest collection of equipment to known members.

## Problem
A camera may return without its charger, or a board game without its reference cards. A spreadsheet showing only “returned” hides incomplete kits and leaves the next borrower disappointed.

## Core workflow
1. A steward defines a kit and its expected components.
2. At checkout, the steward records the borrower, due date, and components actually issued.
3. At return, the steward checks components individually and records missing parts.
4. The kit becomes available after the steward confirms it is ready for the next loan.

## MVP features
- Kit templates with component counts.
- Checkout and return checklists.
- Due-date view and incomplete-return queue.
- Printable loan summary and CSV export.

## Build approach
Build a mobile web app with a relational database for kits, loan snapshots, and component returns. Start with one club and steward-only editing. Apply checkout and availability changes in one transaction so a kit cannot have two active loans.

## Validation plan
Pilot with two clubs for four weeks. Compare kit completeness at the next checkout with their existing ledger and measure the time required to record each handover.

## Biggest risk
Detailed checklists may slow down casual lending enough that stewards skip them. Let each club start with only the components that are frequently forgotten and expand based on real misses.

## Return rules
Snapshot the issued component list at checkout so later template edits do not change what a borrower owes. Record counts returned against that snapshot; a partial return keeps the loan open and the kit unavailable. Allow the steward to resolve a missing component with a dated note, such as “replacement received” or “removed from kit,” before closing the loan. A returned kit remains in a review state until its next-use checklist is confirmed.
