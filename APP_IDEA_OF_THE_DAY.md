# App Idea of the Day: Table Relay
Date: 2026-11-19 (Japan)

## Concept
A lightweight handover board for board-game café staff to track which tables need a rules explanation.

## Target users
Small board-game cafés where two or three staff members share hosting duties.

## Problem
One host promises to explain a game and gets interrupted at the counter. Another host cannot tell whether that table is still waiting, already being helped, or ready to play.

## Core workflow
1. A host adds a table number, game title, and request for help.
2. The next available host claims the request from a shared board.
3. After the explanation, the host marks it resolved or leaves a short follow-up note.

## MVP features
- Waiting, claimed, and resolved request states.
- Table and game labels with elapsed waiting time.
- Staff initials and one-line handover notes.
- Large-text board for a counter tablet.

## Build approach
Build a mobile web app with a small relational database and live board updates. Use a venue account with individual staff identities, starting with one café.

## Validation plan
Observe two baseline shifts and two pilot shifts. Measure requests that need a repeated reminder and the time visitors wait for an explanation.

## Biggest risk
Staff may forget to log requests during busy periods. Put table buttons on the first screen and let a request start with just a table number.

## Handover rules
Allow one active explanation request per table. A host claims it atomically so simultaneous taps cannot assign two hosts. Releasing a claim returns the request to waiting while preserving its original arrival time. A follow-up after resolution starts a new request, keeping the previous note available only to staff for the current shift.

## Busy-shift behavior
Sort waiting requests by original arrival time and show the oldest first. A claim remains visible with the host's initials; after five minutes, ask staff to check its status rather than silently resolving it. Pair all colors with text labels. The board shows a clear disconnected banner and disables edits until it has refreshed after reconnecting.
