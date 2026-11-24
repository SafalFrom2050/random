# App Idea of the Day: Queue Draft
Date: 2026-11-25 (Japan)

## Concept
A small question board for hands-on workshops that lets participants ask for help without leaving their work or repeatedly raising a hand.

## Target users
Facilitators running adult craft, software, or electronics workshops with ten to thirty participants and a few roaming helpers.

## Problem
Helpers cannot easily see who has waited longest or which questions affect several tables. Quiet participants can remain stuck while more visible requests get answered first.

## Core workflow
1. The facilitator opens a session and displays its short URL and QR code.
2. A participant submits a table label and a short question.
3. A helper claims the question and visits that table.
4. The helper resolves it or flags it for a short group explanation.

## MVP features
- Account-free participant form with a private request status link.
- Helper queue ordered by waiting time.
- Claim, resolve, and group-explanation actions.
- Session close control and anonymous timing summary.

## Build approach
Build a mobile web app with a relational database and live queue updates. Require helper sign-in, scope access to the session, and update claims atomically to prevent duplicate visits. Start with one organizer and in-person workshops.

## Validation plan
Observe one baseline workshop and two comparable pilot workshops. Track how long participants stay blocked and whether helpers spend less time scanning the room for raised hands.

## Biggest risk
Typing a question may be harder than asking aloud, especially during practical work. Require only a table label, offer a “please visit” shortcut, and keep verbal requests available.
