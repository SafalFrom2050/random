# App Idea of the Day: Palette Walk
Date: 2026-10-26 (Japan)

## Concept
A creative scavenger-hunt app that challenges you to find a small set of colors in your surroundings and turn your discoveries into a personal photo palette.

## Target users
Casual photographers, designers seeking inspiration, and people who want a playful reason to notice their neighborhood.

## Problem
Creative prompts can be too broad to start, while ordinary photo galleries bury small visual discoveries. A concrete color hunt gives a short outing a purpose and produces something easy to keep or share.

## Core workflow
1. Choose a three-color challenge or generate a random palette.
2. Photograph something matching each color using an in-app camera or import an existing photo.
3. Tap the part of the photo you want to sample.
4. See the sampled color beside the target; accept it yourself or try another shot.
5. Finish with a collage of three photos and their sampled color codes.
6. Save the collection or export a shareable image.

Example: A rust-red gate, a cream-colored wall, and a blue bicycle become one neighborhood palette.

## MVP features
- Bundled and randomly generated three-color prompts.
- Camera capture and system photo-picker import.
- Tap-to-sample color with a magnified preview.
- Target and sample comparison using swatches, labels, and color codes.
- A local gallery of completed and unfinished challenges.
- Collage image export with optional captions.

Allow users to skip colors or complete a challenge indoors. Keep maps, public feeds, competitive scoring, and AI object recognition outside the first release.

## Build approach
Build a Flutter app with local image storage and SQLite for challenges, target colors, and sample coordinates. Generate palettes from a curated set of combinations so early prompts remain varied and achievable.

Normalize image orientation before sampling. Average a small patch around the chosen point to reduce single-pixel noise, and store the resulting RGB value with the photo. Describe samples as image colors: lighting and camera processing mean they are not calibrated measurements of real objects.

Render exported collages from the same saved challenge data. Use the system share sheet only after the user explicitly chooses export; remove location metadata from generated images.

## Validation plan
Invite eight people to try one ten-minute challenge and then use the app freely for a week.
- Observe whether they understand sampling without a tutorial.
- Check whether target colors feel achievable in different surroundings.
- Ask whether they enjoyed noticing details they would usually overlook.
- Track voluntary second challenges and saved or exported collages.
- Test orientation and sampling on photos from several devices.

Continue if five participants voluntarily complete another challenge and can explain what they enjoyed. Investigate whether prompts or collage creation drives repeat use before adding more features.

## Biggest risk
Strict color matching could turn a relaxing activity into a frustrating accuracy test. Let users decide whether a photo fits, show comparisons without pass/fail judgments, and offer replacement colors. The main uncertainty is whether the activity stays interesting after the first few hunts.

## Possible business model
A free core experience with optional one-time purchases for themed prompt packs and collage styles. Keep sampling, saved collections, and basic image export free.
