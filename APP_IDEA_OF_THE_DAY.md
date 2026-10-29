# App Idea of the Day: Borrow Loop
Date: 2026-10-30 (Japan)

## Concept
A simple lending notebook for keeping track of physical things shared with friends: books, tools, chargers, board games, and kitchen equipment. Each loan gets a photo, an agreed return date if needed, and a clear returned/not-returned state.

## Target users
People who regularly lend or borrow everyday items within an existing circle of friends, neighbors, or club members.

## Problem
Small loans disappear into chat history. Months later, neither person remembers who has the drill or which copy of a book belongs to whom, and asking can feel awkward.

## Core workflow
1. Photograph an item and choose “I lent this” or “I borrowed this.”
2. Enter the other person's nickname manually and optionally set an agreed return date.
3. Save a note about accessories or condition.
4. View open loans grouped by person or item.
5. When needed, copy a neutral reminder draft into your preferred messaging app.
6. Mark the item returned and retain a searchable closed record.

Example: “Cordless drill + charger, lent to Alex. Needed back before Saturday.” The app reminds its owner privately; it never contacts Alex automatically.

## MVP features
- Fast item photo and title entry.
- Lending and borrowing records with optional due dates.
- Local reminders with snooze and an overdue filter.
- Accessory checklist and short handoff notes.
- Editable reminder text with copy-to-clipboard.
- Return confirmation, undo, and local backup export/import.

Start with a private notebook. Accounts, contact-book access, shared confirmations, public listings, payments, and a lending marketplace are outside the MVP.

## Build approach
Build a Flutter app with SQLite for items, people aliases, and loan records, plus local attachment storage. Require no account and collect no recipient contact details.

Represent loans as open or returned, storing handoff and return timestamps separately. Schedule local notifications only when the user chooses a reminder; reschedule them after due-date edits and cancel them on return. Export a versioned JSON manifest with photos in a ZIP archive. Keep reminder drafts editable and require a separate user action to copy or share them.

## Validation plan
Recruit eight people who have at least two items currently borrowed or lent, and run a three-week pilot.
- Measure time to record an existing loan.
- Ask participants to locate an item or person in their records.
- Observe whether accessory notes prevent confusion.
- Track voluntary new entries and completed returns.
- Ask whether reminders feel useful or socially uncomfortable.
- Verify that restoring a backup preserves open and closed records.

Proceed if five participants voluntarily record another loan and can retrieve a useful detail faster than with their usual notes or chat search. Do not treat returned items alone as proof the app caused better repayment behavior.

## Biggest risk
People may forget to create the record during a casual handoff, leaving the notebook incomplete. Make a photo and title sufficient to start, allow missing details to be added later, and validate capture speed before building shared workflows.

## Possible business model
Free for a small number of open loans, with a one-time upgrade for unlimited open records and custom reminder presets. Keep closed history and basic backup export available to everyone.
