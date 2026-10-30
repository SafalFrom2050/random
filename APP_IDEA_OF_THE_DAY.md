# App Idea of the Day: Foldback
Date: 2026-10-31 (Japan)

## Concept
A paper-folding practice app that lets people record the tricky steps of their own origami models as short photo sequences, then replay them with a large, hands-free-friendly step view.

## Target users
Origami hobbyists, craft teachers, and people who learn a model once but forget the difficult fold when trying again.

## Problem
Long videos are awkward to scrub through while holding paper. Static diagrams can leave out the exact intermediate shape a learner needs, while personal photos become scattered in a gallery.

## Core workflow
1. Create a model and note the paper size and starting orientation.
2. Photograph each important intermediate shape.
3. Add a short instruction and optional arrow annotation.
4. Mark difficult steps for extra practice.
5. Open practice mode, advance through the sequence, and jump directly to a marked fold.
6. Save a separate attempt photo and note what went wrong.

Example: A crane sequence includes close-up photos immediately before and after the reverse fold, plus “open the pocket before flattening.”

## MVP features
- Ordered photo steps with captions and simple drawn arrows.
- Insert, duplicate, reorder, and delete steps.
- Large practice controls and adjustable screen-awake behavior.
- Bookmarks for difficult folds.
- Paper size, model attribution, and source-link fields.
- Offline collections and ZIP export/import.

Start with user-created sequences. Public pattern sharing, automatic fold recognition, 3D simulation, and a licensed tutorial catalog are outside the first release.

## Build approach
Build a Flutter app with SQLite for models, ordered steps, and attempt notes, plus app-private image storage. Keep the original photo and annotation coordinates separately so arrows remain editable.

Normalize photo orientation before annotation and store coordinates relative to image dimensions. Save edits immediately and provide undo for step deletion. Export a versioned JSON manifest alongside image assets; validate referenced files during import.

The central interaction should remain simple enough to use with paper in hand. Test large tap targets and an optional delayed advance button before considering voice controls.

## Validation plan
Recruit six origami learners and two instructors for a small usability pilot.
- Have each learner document one difficult section of a model they already know.
- A week later, ask them to repeat it using their sequence.
- Observe navigation mistakes and missing intermediate views.
- Compare the effort of making a sequence with finding the same point in their usual tutorial.
- Ask instructors whether annotations clarify the fold without obscuring the paper.

Continue if four learners voluntarily reuse a sequence and can identify a specific fold it helped them remember. If capture is too burdensome, narrow the app to bookmarking a few difficult steps.

## Biggest risk
Creating instructions may take more effort than replaying an existing video. Focus on personal memory aids for difficult folds, allow a useful sequence to contain only two or three photos, and validate capture effort before expanding into full tutorials.

## Possible business model
Free for a few models, with a one-time upgrade for unlimited collections and custom practice layouts. Keep basic export available to everyone.
