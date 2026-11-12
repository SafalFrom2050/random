# App Idea of the Day: Mend Match
Date: 2026-11-13 (Japan)

## Concept
A browser tool that lets repair cafés tell visitors what to bring before they show up with a broken item.

## Target users
Volunteer organizers at monthly repair cafés and first-time visitors bringing clothing, bags, or simple household objects.

## Problem
A volunteer may be able to fix a backpack zipper but need the original slider, or repair a loose chair only if the visitor brings the missing hardware. Generic event pages leave those details to last-minute messages or wasted trips.

## Core workflow
1. The organizer publishes the next session and selects the repair categories it can handle.
2. A visitor chooses a category, describes the problem, and optionally adds a photo.
3. The organizer replies with a short bring list or explains why the item is outside the session’s scope. The visitor can open the reply from a private link.

## MVP features
- Session page with supported categories and a request cutoff.
- Mobile intake form and private reply page.
- Volunteer queue with reusable bring-list templates and editable replies.
- Confirmation that the visitor has read the instructions.

## Build approach
Use a mobile web app with a relational database for sessions, requests, and replies. Store photos privately and email a reply link when a volunteer responds. Keep the first pilot to one venue and three repair categories.

## Validation plan
Compare one baseline session with two pilot sessions at the same venue. Track arrivals missing essential items and how many minutes volunteers spend answering questions before the event.

## Biggest risk
Intake could add more work than it saves. Start with a capped queue and templates for common requests; reduce the intake fields if volunteers still have to ask the same follow-up questions.

## Triage and arrival
Each reply has one of three outcomes: “bring it,” “need one detail,” or “outside this session’s scope.” A bring-it reply names the item, any detached parts, and any supplies the visitor already has; it does not promise a repair or reserve a time slot. For example, for a backpack zipper, ask for the backpack and any loose slider or pull, and tell the visitor to wait before buying replacements. Close requests 48 hours before the event and show the cutoff before anyone starts the form.
