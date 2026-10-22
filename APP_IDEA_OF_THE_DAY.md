# App Idea of the Day: Fridge Friday
Date: 2026-10-22 (Japan)

## Concept
A lightweight food-planning app that turns the groceries you already have into a few realistic meal suggestions before they expire.

## Target users
People who live alone, buy groceries without a plan, and want to waste less food without following a strict meal-prep routine.

## Problem
Recipes usually start with a shopping list. In real kitchens, the problem is often the opposite: a half-used cabbage, tofu nearing its date, and no clear idea what can be made quickly.

## Core workflow
1. Add groceries by typing, scanning a receipt, or snapping a shelf photo.
2. Set an optional “use by” date and note how much is left.
3. Get three simple meal ideas ranked by soonest-to-expire ingredients, prep time, and dietary preferences.
4. Mark ingredients as used, partially used, or still available.
5. Build a short shopping list from gaps in a selected meal.

Example: With tofu, cabbage, eggs, and rice on hand, the app suggests quick tofu-and-cabbage stir-fry, an egg rice bowl, and a simple miso soup.

## MVP features
- Fast manual ingredient entry with common Japanese supermarket items.
- Expiry reminders that users can snooze or dismiss.
- A small recipe set with adjustable portions and clear substitutions.
- Meal suggestions filtered by prep time and dietary preferences.
- “Used it” updates that reduce or remove ingredient quantities.
- Local-first pantry data with backup and export.

Start with manual entry and a curated recipe collection. Receipt OCR, barcode lookup, shared households, and AI-generated recipes can wait.

## Build approach
Build a Flutter app with a local SQLite pantry and recipe database. Store ingredient names, quantities, purchase dates, and optional expiry dates. Use deterministic matching to rank recipes by expiring ingredients and missing items; this makes suggestions predictable and works offline.

Keep reminders opt-in and schedule them only for ingredients with a date the user entered or confirmed. Never assume a product's expiry date from a receipt.

## Validation plan
Run a two-week pilot with ten people who cook at home at least twice a week.
- Have participants enter five to ten groceries during setup.
- Track whether they open a suggestion, cook it, and mark ingredients as used.
- Ask what made entry feel annoying and whether reminders arrived at useful times.
- Compare food participants report throwing away during the pilot with a typical prior two-week period.

A promising signal would be six participants cooking at least two suggested meals and reporting that pantry entry took under two minutes per shopping trip. Treat the results as directional, not proof of reduced food waste.

## Biggest risk
Maintaining an accurate pantry can feel like extra work, so users may stop updating it. Make partial updates easy, let suggestions tolerate missing or uncertain quantities, and test whether quick capture is enough before adding more automation.

## Possible business model
Offer the pantry, expiry reminders, and core recipe suggestions for free. A modest subscription could add household sharing, custom recipe collections, and cross-device backup after users show they return to the app.
