# App Idea of the Day: Prop Table
Date: 2026-11-02 (Japan)

## Concept
A continuity notebook for small video productions that records where props belong in each scene. Take a reference photo, label important objects, and compare the setup before the next take.

## Target users
Student filmmakers, solo video creators, and small theater or stop-motion teams working without a dedicated continuity assistant.

## Problem
A cup changes sides, a jacket disappears, or a notebook opens to a different page between takes. Ordinary camera rolls make the correct reference hard to find when a team is ready to shoot.

## Core workflow
1. Create a production, scene, and setup.
2. Photograph the approved arrangement before filming.
3. Add numbered markers with notes such as “handle faces left” or “half full.”
4. Mark the photo as the reference for that setup.
5. Before another take, open the reference beside a fresh check photo.
6. Record intentional changes as a new reference version.

Example: A kitchen scene preserves the mug position, chair angle, and towel placement when filming resumes the following day.

## MVP features
- Production → scene → setup organization.
- Reference photos with editable markers and notes.
- Side-by-side and adjustable-opacity image comparison.
- Explicit reference approval and version labels.
- A short pre-take checklist.
- Offline storage and per-scene ZIP export/import.

Keep automatic object detection, cloud collaboration, script parsing, and full production scheduling outside the first release.

## Build approach
Build a Flutter tablet-and-phone app with SQLite metadata and app-private image files. Store marker coordinates relative to the normalized image dimensions so annotations survive resizing.

Keep reference versions immutable after approval; edits create a new version, and the user explicitly chooses which is current. Comparison supports manual zoom and alignment, since camera position may change. Do not imply that an overlay can automatically prove continuity. Export a versioned JSON manifest with reference photos and annotations.

## Validation plan
Pilot with four small filmmaking teams during a short scene shoot.
- Measure time to locate the correct setup reference.
- Observe whether markers capture details the team otherwise forgets.
- Record continuity mismatches noticed before shooting another take.
- Test resuming a scene after a day away.
- Ask whether maintaining references slows the shoot excessively.
- Verify export and restore on a second device.

Continue if three teams voluntarily use it on another scene and identify a concrete mistake it helped them catch. Review capture overhead before adding more production features.

## Biggest risk
A busy crew may forget to capture an approved setup, or select the wrong reference. Make the current scene and reference label prominent, keep capture to a few taps, and distinguish unapproved photos clearly. Validate that the habit fits an actual shoot.

## Possible business model
Free for one active production, with a one-time upgrade for multiple productions and printable continuity sheets. Keep basic scene export available to everyone.
