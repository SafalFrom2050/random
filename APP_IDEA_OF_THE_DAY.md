# App Idea of the Day: Where Was It?
Date: 2026-10-20 (Japan)

## The pitch
A visual memory app for the things you store and then forget: spare cables, winter clothes, documents, tools, and rarely used kitchen items.

## Who it helps
People living in small apartments, sharing storage, or moving frequently.

## The problem
You know you own an item, but finding it means opening every drawer and box. Elaborate inventory apps take too much effort to maintain.

## The core experience
1. Photograph an open drawer, shelf, or box.
2. Give it a location such as “Bedroom → Closet → Blue box.”
3. Add a few searchable item labels.
4. Search “HDMI adapter” weeks later and see its location and original photo.
5. Tap “Moved” to update an item's location quickly.

## Smallest useful MVP
- Locations with optional parent locations.
- Photos with manually entered item labels.
- Search across item names, notes, and locations.
- A “recently moved” list for correcting mistakes.
- Local storage and a JSON export/import backup.

## A delightful detail
Print a QR label for a box. Scanning it opens the contents photo, so you can check inside without unpacking it.

## What makes it interesting
Capture a whole storage space in one photo rather than entering every object separately. Keep the ordinary workflow fast enough to use while tidying.

## Build approach
Flutter with SQLite and local image files. Start offline with manual labels; explore on-device image labeling only after the basic workflow proves useful.

## First validation
Ask five people to record three storage locations. A week later, ask them to find two stored items. Measure lookup time, successful finds, and whether they updated moved items.

## Biggest risk
An outdated location is worse than no location. Make moving an item a two-tap action, and show when each location was last checked.

## Possible business model
Free basic inventory, with a one-time upgrade for QR label sheets, multiple homes, and richer export options.
