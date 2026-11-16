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
