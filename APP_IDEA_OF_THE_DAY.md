# App Idea of the Day: Shelf Shuffle
Date: 2026-10-29 (Japan)

## Concept
A personal reading app that helps you choose your next book from the unread books you already own. Pick your available time and current mood, then draw three candidates from your own shelf.

## Target users
Readers with a growing pile of unread books who spend more time choosing than starting.

## Problem
A book collection can become an overwhelming backlog. Ratings and recommendation feeds encourage more purchases while giving little help choosing among books already at home.

## Core workflow
1. Add five unread books with titles and optional cover photos.
2. Give each book simple personal tags, such as light, demanding, funny, or practical.
3. Choose a mood and a reading window.
4. Draw up to three matching books, with a short explanation based on your tags.
5. Start a ten-minute reading trial and decide whether to continue, return it to the shelf, or set it aside.
6. Save a brief note about why it did or did not suit you today.

Example: “Low energy, twenty minutes” surfaces a funny essay collection you tagged as easy to dip into.

## MVP features
- Fast manual book entry and optional cover photos.
- Editable mood, effort, and short-session suitability tags.
- Transparent filtering and random selection among eligible books.
- A reading-trial timer and continue/later/set-aside outcomes.
- A cooldown so recently declined books do not appear immediately.
- Local storage and CSV export/import.

Avoid external recommendations, public ratings, purchase links, and automatic reading-level inference in the first version.

## Build approach
Build a Flutter app with SQLite for books, tags, trial sessions, and cooldown dates. Store cover images locally and require no account.

Use user-entered tags as the source of matching. Treat the reading window as suitability for a session, not a promise to finish a book. When no books match, explain which filters excluded them and let the reader relax one constraint. Persist a trial start time so returning from the background restores the remaining time without relying on a continuously running timer.

## Validation plan
Recruit eight readers with at least ten unread books for a two-week pilot.
- Measure the effort needed to enter the first five books.
- Observe whether the selection explanation makes sense.
- Record voluntary draws, started trials, and books readers choose to continue.
- Ask whether the app helped them start reading sooner than their usual method.
- Check whether cooldowns hide books too aggressively.

Continue if five participants voluntarily return and can name a book they started because of the app. Use the small pilot to assess behavior, not to claim increased reading volume.

## Biggest risk
Cataloging and tagging may take more effort than simply picking a book. Make every field except title optional, let people begin with five books, and ask for tags gradually after trials. Validate setup friction before adding barcode lookup or a large catalog.

## Possible business model
A free small shelf and a one-time upgrade for unlimited books and custom selection presets. Keep basic export available to all readers.
