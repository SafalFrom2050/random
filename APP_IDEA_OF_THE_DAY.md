# App Idea of the Day: Puzzle Pause
Date: 2026-11-23 (Japan)

## Concept
A visual pause card for unfinished jigsaw puzzles that records which sections and sorting trays someone was working on.

## Target users
Casual puzzlers who pack projects away between sessions or share a puzzle with family members on different schedules.

## Problem
After a week away, it is easy to forget which loose pieces belong to a promising section or what a handwritten tray label meant. An overview photo captures progress but loses the intended next move.

## Core workflow
1. Take an overhead photo before packing away the puzzle.
2. Mark a few regions and attach short notes such as “finish blue window.”
3. Add tray labels and a next-session goal.
4. Reopen the pause card when resuming and update it when stopping again.

## MVP features
- Project cards with a dated overview photo.
- Numbered photo markers with text notes.
- Tray names and a single next-session goal.
- Offline viewing and a shareable image summary.

## Build approach
Build a Flutter app with SQLite and local compressed images. Store marker positions as normalized coordinates tied to a particular photo. Render the shareable summary on the device, with numbered notes beside the image.

## Validation plan
Recruit eight puzzlers who regularly pause projects for at least three days. Compare time spent reconstructing their plan using normal notes or photos with time using a pause card.

## Biggest risk
Documenting the puzzle may feel like a chore that saves little time. Default to one photo and one next-session goal, making tray notes and markers optional.

## Resume details
A marker belongs to the exact photo on which it was placed. Replacing the photo creates a new pause card without transferring markers automatically, since the puzzle or camera angle may have changed. Show only the latest card by default, with the previous two available for reference. Give trays short visible codes such as T1; a note can say “T1: blue window candidates” without suggesting the app knows which pieces are correct.

## Pilot decision
For each participant, observe a baseline return and two returns using the app after comparable gaps. Time from opening the stored puzzle until they select a section and begin placing or testing pieces; record documentation time separately. Continue if at least six of eight reduce median restart time by 25% and median pause-card creation takes under 45 seconds. Ask whether the card helped or constrained their choice of next section. If people skip documentation in either pilot session, count that as an adoption failure rather than excluding the session.
