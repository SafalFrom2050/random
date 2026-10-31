# App Idea of the Day: Round Robin
Date: 2026-11-01 (Japan)

## Concept
A casual sports-session organizer that rotates players through short matches while balancing playing time and avoiding repeated teammates. One person runs the session from a phone.

## Target users
Small badminton, table-tennis, or doubles-tennis groups that meet informally and have more players than available courts.

## Problem
Organizers repeatedly stop playing to decide who goes next. Some people sit out too long, and the same pairs keep forming even when everyone wants variety.

## Core workflow
1. Add player nicknames, choose singles or doubles, and enter the number of courts.
2. Mark who is ready, resting, or leaving.
3. Generate the next round, with an explanation such as “These players have waited longest.”
4. Make any manual swaps and confirm the assignments.
5. Finish the round and record who actually played.
6. Repeat, then review a simple participation summary.

Example: Seven players on one doubles court get rotating groups of four, with the organizer able to keep an injured player resting without removing their history.

## MVP features
- Session roster and player availability.
- Singles or doubles assignments for one or two courts.
- Participation counts and rounds spent waiting.
- Teammate and opponent repetition tracking.
- Manual swaps, undo, and session recovery.
- A large court-assignment screen and text summary export.

Treat each round as a shared block; asynchronous court scheduling, skill ratings, rankings, payments, and online invitations are outside the MVP.

## Build approach
Build a Flutter app with SQLite for sessions, players, and confirmed rounds. Generate candidate assignments locally.

Use an explicit priority order: first reduce differences in rounds played among available players, then favor those waiting longest, then reduce repeated teammates and opponents. Show the tradeoff when perfect balance is impossible. Do not count a proposed round until the organizer confirms it, and preserve the actual lineup after manual swaps.

For small rosters, enumerate feasible assignments with a cap on candidates; use a deterministic tie-breaker so regenerating without changes is predictable. Test odd player counts, availability changes, undo, and session restoration.

## Validation plan
Pilot with four existing groups over three sessions each.
- Compare organizing time with their normal method.
- Check participation differences and maximum consecutive rounds waiting.
- Record manual overrides and the reasons for them.
- Ask whether people understand why they were assigned or rested.
- Test mid-session arrivals and departures.

Continue if three groups choose to use it again and organizers report less coordination effort without players feeling that the rotation is unfair. Analyze overrides before tuning the selection rules.

## Biggest risk
Numerical balance may conflict with social preferences, fatigue, or people wanting a specific partner. Keep the selection rules understandable, make manual changes easy, and use availability controls rather than silently assuming everyone wants equal play.

## Possible business model
Free for basic sessions, with a one-time upgrade for saved group presets, more courts, and custom rotation priorities. Keep participation summaries and session recovery available to everyone.
