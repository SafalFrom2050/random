# App Idea of the Day: Sound Check Card
Date: 2026-11-21 (Japan)

## Concept
A photo notebook that helps bands recreate a rehearsal-room setup that sounded good last time.

## Target users
Amateur bands renting different rehearsal rooms and sharing amplifiers or mixers.

## Problem
A useful setup disappears when the room booking ends. Photos of knobs are scattered across chats, and nobody remembers whether a note belongs to the current room, instrument, or song.

## Core workflow
1. Create a room session and add a photo for each relevant piece of equipment.
2. Attach short notes about the instrument, control positions, and what worked.
3. At the next booking, open the room's reference card and mark any changes after listening.

## MVP features
- Room and session cards with dated photos.
- Equipment labels and searchable notes.
- A pinned reference session per room.
- A compact offline view for use during setup.

## Build approach
Build a Flutter app with SQLite and compressed photos in local storage. Use one band member's device in the pilot and export a PDF reference card for others. Keep photos linked to stable equipment records so similarly named amplifiers do not get mixed up.

## MVP scope
Capture settings manually. Leave automatic knob recognition, audio analysis, and equipment control outside the first release. The reference is a starting point to check by ear rather than a promise that the same positions will sound identical.

## Validation plan
Recruit four bands with recurring room bookings. Time setup using their usual photos or notes, then two later setups using the reference cards. Record time spent searching for settings and whether anyone used the wrong equipment's reference.

## Biggest risk
Bands may spend longer documenting than they save at the next rehearsal. Start with one photo and one useful note per device; ask users to save only setups they actually want to repeat.

## Comparing setups
Require a room and equipment label before pinning a reference. Display the date beside every photo and allow “equipment changed” to remove an outdated reference from the default setup view. Save edits as a new session so a band can compare what changed without losing its last useful reference. For example, “vocal mic moved away from drummer” belongs to the room session, while “bass amp EQ” belongs to the labeled amp.

## Pilot decision
Measure from the first attempt to retrieve a setup note until all participating members say their equipment is ready to play. Compare each band's baseline with the median of its two pilot setups in the same room. Continue if at least three of four bands cut setup time by 20%, no band uses a mismatched equipment reference, and median documentation time stays under two minutes per session. Record changes in equipment or room layout separately; repeat those comparisons rather than attributing their timing to the app.
