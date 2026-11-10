# App Idea of the Day: Plant Sitter Pass
Date: 2026-11-11 (Japan)

## Concept
A temporary handover guide for looking after someone else's houseplants. Owners create photo cards with their own instructions; sitters record visits and flag questions in one place.

## Target users
Houseplant owners going away and friends or neighbors helping them.

## Problem
A chat message saying “water the plants” leaves too much ambiguity. Similar pots are easy to confuse, and owners cannot tell which instructions need clarification until they are away.

## Core workflow
1. Photograph each plant in its usual position and give it a recognizable label.
2. Add owner-written care instructions and optional visit dates.
3. Preview the guide with the sitter before departure.
4. Share a temporary guide link.
5. The sitter opens each card, records what they actually did, and flags uncertainty rather than guessing.
6. The owner closes the handover when they return.

## MVP features
- Photo cards with location descriptions and manual instructions.
- Planned visits and action notes with timestamps.
- A question flag and owner response thread.
- Expiring access links and a printable guide.

Keep plant diagnosis, automated watering advice, device integrations, and a sitter marketplace outside the MVP.

## Build approach
Build a responsive web app with an authenticated owner editor, a small database, and object storage for compressed photos. A random access token grants access only to one handover; owners can revoke it. Require connectivity to submit visit records and clearly show whether a note has been saved.

## Validation plan
Pilot with six owner-sitter pairs during actual short trips. Observe setup effort, questions asked, plant identification mistakes, and voluntary reuse. Compare against each pair's usual chat instructions.

## Biggest risk
Instructions may be ambiguous or outdated. Require the owner to review every card before sharing, show the review date, and make uncertainty easy to flag. Treat care details as owner-provided instructions, not expert recommendations.
