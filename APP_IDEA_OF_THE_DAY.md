# App Idea of the Day: Box Echo
Date: 2026-11-20 (Japan)

## Concept
A phone-first catalog that answers “Which box did I put that in?” for seasonal household items, using short box codes and a printable index.

## Target users
People with a few storage bins in closets or rented storage, especially households rotating decorations, camping gear, or winter clothing.

## Problem
A label like “winter stuff” becomes useless when contents change. Full inventory apps can demand too much detail, so people stop maintaining them after the first afternoon.

## Core workflow
1. Create a box with a short code such as B04 and a storage location.
2. Take one overview photo and add a few searchable item names or nicknames.
3. Search for an item to see its box code and location.
4. When removing something, mark it out; when returning it, confirm the box or move it to another box.

## MVP features
- Box cards with photos, codes, locations, and free-text item lists.
- Search across item names, synonyms entered by the owner, and locations.
- Quick item moves with undo and an explicit “currently out” state.
- Printable box labels and a plain-text household index.

## Build approach
Build an offline Flutter app with SQLite and compressed photos in app-private storage. Use stable IDs internally so renaming a box does not break item links. Apply item moves in a single transaction and keep a small undo history. Export a ZIP with structured records, photos, and a readable index for backup; importing creates a separate catalog to avoid silently replacing newer data.

## MVP scope
Start with one device per household and manual item entry. QR labels can open the matching box inside the app, but the large printed code must also work without scanning. Leave automatic photo recognition, purchase prices, and multi-user synchronization for later validation.

## Validation plan
Recruit eight households with at least six storage boxes. Time three item-finding tasks using their existing labels, then repeat comparable tasks after a week with Box Echo. Track wrong-box openings and ask participants to record time spent updating changed contents. Continue if at least six households cut median lookup time by 30% and typical updates take under 20 seconds. Treat a household that stops updating as a failed adoption case, even if its initial lookup results were good.

## Biggest risk
The catalog can become confidently wrong when items move without an update. Display each box's last-confirmed date, keep “currently out” visible in search, and offer a quick box audit that confirms or edits several entries together. Test whether this is less work than relabeling boxes before expanding the feature set.
