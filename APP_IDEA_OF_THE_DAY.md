# App Idea of the Day: Page Pair
Date: 2026-11-17 (Japan)

## Concept
A phone tool that helps zine makers arrange their pages in the right order for printing and folding into a booklet.

## Target users
First-time zine makers, school art clubs, and workshop facilitators printing small batches on ordinary office printers.

## Problem
Reading order and print order differ: the back cover sits beside the front cover on the same sheet. A wrong flip setting can put every back side upside down, wasting paper and time.

## Core workflow
1. Import a PDF in reading order and choose the paper size.
2. Preview each sheet front and back, including any blank pages needed to fill the last sheet.
3. Print a calibration sheet, follow the illustrated folding guide, and export the rearranged booklet PDF.

## MVP features
- PDF import and page thumbnails.
- Folded booklet preview with editable blank page placement.
- Printer calibration sheet and imposed PDF export.

## Build approach
Build a browser app that assembles the output PDF on the device. Start with A4 sheets folded to A5 and one centered staple fold.

## Validation plan
Watch eight new zine makers print and fold a sample booklet. Compare first-attempt page order and misprints against the workshop's existing instructions.

## Biggest risk
Printer drivers can rotate, scale, or reorder sheets in ways the app cannot see. Ask users to verify one test sheet before printing a whole run.

## Sheet layout
For an eight-page booklet, the outside sheet pairs 8 with 1 on the front and 2 with 7 on the back; the inside sheet pairs 6 with 3 and 4 with 5. Default padding goes immediately before the back cover. Limit the pilot to 24 pages and portrait source PDFs. Show a crop warning when the chosen margins would cut content and offer fit-to-page as the default.

## Printer calibration
Put a large directional arrow and distinct front and back labels on the calibration pages. After folding the test sheet, ask whether both arrows point up and the front label is on the outside. If the back is upside down, prompt the user to switch the duplex flip edge and reprint only the test. Leave manual paper reinsertion out of the first release and explain this before import.

## Pilot decision
Give four participants the workshop's usual instructions and four Page Pair for their first attempt, using equally sized source PDFs. Count a booklet as correct only if all pages are upright and in reading order, and track calibration sheets separately from misprints. Advance to a larger trial if at least three of four Page Pair users finish correctly without facilitator intervention and the group uses fewer wasted sheets than the comparison group. Record printer model and driver settings for each failure.
