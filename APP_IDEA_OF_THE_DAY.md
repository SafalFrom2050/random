# App Idea of the Day: Mix Memo
Date: 2026-11-26 (Japan)

## Concept
A pocket recipe book for miniature painters who want to recreate a custom paint mix after the original batch runs out.

## Target users
Hobbyists painting tabletop figures in batches over several weeks.

## Problem
A photo captures the finished model but rarely records which paints, proportions, and thinning choices produced its color. A vague note like “mostly blue” is difficult to repeat when the next squad needs matching uniforms.

## Core workflow
1. Create a recipe with named paints and relative amounts.
2. Attach a photo of the dried test swatch and note the primer.
3. Link the recipe to a model or project.
4. When mixing again, scale the amounts and save any adjustment as a new version.

## MVP features
- Manual paint catalog and searchable recipe cards.
- Ratio calculator with clearly labeled measuring units.
- Swatch photos, primer notes, and recipe versions.
- Offline access and a shareable recipe summary.

## Build approach
Build a Flutter app with SQLite and app-private photo storage. Store each ingredient amount with its unit and calculate scaled quantities locally. Use manual paint names in the first release so no external catalog is required.

## Validation plan
Recruit eight miniature painters to record one useful mix and recreate it after at least a week. Observe whether their recipe contains enough information and compare their result with the original dried swatch.

## Biggest risk
Drop sizes, pigment behavior, and lighting can make apparently precise recipes difficult to reproduce. Treat amounts as a starting point, preserve the measuring method, and encourage a dried test swatch before applying a recreated mix.

## Recipe and comparison rules
Scale only amounts entered in the same unit, such as drops; do not silently convert drops to milliliters. If a scaled recipe needs fractions smaller than the user's measuring method supports, offer a larger batch size rather than rounding each ingredient independently. Keep thinner separate from the color ratio and label it with its own method. Photos are visual notes, not calibrated color measurements. Record paint brand, finish, primer, and any dilution alongside each recipe version.

## Pilot decision
Have each participant recreate the recorded mix using the same paints and measuring method. Compare dried swatches side by side under the same light, asking the painter whether the result is acceptable for their actual project. Advance if at least six of eight reach an acceptable match within two adjustments and median recipe entry takes under two minutes. Log missing details and incorrect unit assumptions separately; revise the form if either prevents a recreation. Avoid automated color matching until the manual workflow proves useful.
