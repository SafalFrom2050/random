# App Idea of the Day: Fixfolio
Date: 2026-10-25 (Japan)

## Concept
A simple home-repair log that helps people remember how an appliance, bike, or piece of furniture was fixed—and what parts or tools worked.

## Target users
Renters, homeowners, and hands-on people who handle small repairs themselves or coordinate with a repair shop.

## Problem
Repair details disappear into chat threads, paper receipts, and memory. When the same issue returns, people often repeat troubleshooting or buy the wrong replacement part.

## Core workflow
1. Add an item with a name, photo, model number, and optional serial number.
2. Record a symptom, date, and what was tried.
3. Mark the outcome: fixed, temporary workaround, or still unresolved.
4. Attach the part number, receipt, and a short note about what worked.
5. Set a reminder to recheck a temporary fix or schedule routine maintenance.
6. Search past repairs by item, symptom, or part number.

Example: “Washing machine — drain error. Cleaned the filter; issue resolved. Filter cover opened with a coin. Recheck in one month.”

## MVP features
- Item cards with photos and model details.
- A dated repair timeline for each item.
- Searchable notes, parts, costs, and receipts.
- Optional reminders for follow-up and maintenance.
- Local-first storage with backup and export.

Keep repair diagnosis, automatic parts matching, technician booking, and shared household accounts outside the first release.

## Build approach
Build a Flutter app with SQLite and local attachment storage. Store each repair as a separate event linked to an item, so the timeline remains easy to scan and edit. Make fields optional and support quick voice-to-text notes. Export a versioned JSON file with attachments in a ZIP archive.

## Validation plan
Ask eight people to log one recent repair, then use Fixfolio for a month.
- Check whether they can find a past repair or part number in under 30 seconds.
- Track how often they add a note immediately after a repair.
- Ask whether recording a repair feels easier than their current method.
- Verify that export and restore preserve item history and attachments.

Proceed if most participants record at least two repairs and can retrieve a useful detail without help.

## Biggest risk
People may not want to document routine fixes. Keep logging to a few taps, provide a “quick note” path, and test whether the reminders and searchable history are useful enough to bring them back.

## Possible business model
Free for a small number of items, with a one-time upgrade for unlimited items and expanded backup history. Keep export available to everyone.
