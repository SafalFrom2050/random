# App Idea of the Day: Taste Compass
Date: 2026-11-03 (Japan)

## Concept
A personal tasting notebook that helps you discover what you enjoy in coffee or tea through simple side-by-side comparisons. Record two drinks, pick which you prefer, and keep a short explanation in your own words.

## Target users
Curious home brewers and café visitors who want to understand their preferences without learning specialist tasting vocabulary.

## Problem
Star ratings flatten different experiences into one number. People remember liking a drink but forget whether it was the roast, brewing method, sweetness, or setting that mattered.

## Core workflow
1. Create a coffee or tea entry with a name, optional photo, and a few preparation details.
2. Compare it with another entry, either tasted together or from memory.
3. Choose a preference, a tie, or “too different to compare.”
4. Add a plain-language reason such as “less bitter” or “better without milk.”
5. Browse preferences within comparable groups and revisit notes before brewing or buying again.

Example: Two preparations of the same tea reveal that the user preferred the shorter steep. The app records that observation without claiming steeping time caused the preference.

## MVP features
- Separate coffee and tea collections.
- Optional preparation fields and custom flavor tags.
- Pairwise preference, tie, and incomparable outcomes.
- A clear distinction between simultaneous tasting and memory-based comparison.
- Search, photos, and a simple comparison history.
- Local storage and CSV/JSON export.

Keep automated flavor identification, universal rankings, shopping recommendations, and public reviews outside the MVP.

## Build approach
Build a Flutter app with SQLite for drinks, preparation records, and comparison events. Store photos locally and require no account.

Show direct comparison results and counts rather than manufacturing a precise global score from a small sample. Allow contradictory preferences and distinguish preparation attempts from the underlying product. Preserve units for brew quantities and temperatures, and let users omit any field.

Export a versioned JSON backup with optional image attachments; offer a flat CSV for notes and comparisons.

## Validation plan
Recruit eight casual coffee or tea drinkers for a two-week pilot.
- Ask each person to record three drinks and one comparison.
- Measure entry time and which fields they skip.
- Check whether they can retrieve a useful preference before preparing another drink.
- Track voluntary comparisons after the initial task.
- Ask whether the notebook teaches them something specific about their own taste.

Continue if five people return voluntarily and can describe a choice their notes helped them make. Treat recorded preferences as personal observations, not controlled experimental findings.

## Biggest risk
Logging could feel like work, and memory-based comparisons may be unreliable. Make name and preference sufficient, show comparison context clearly, and encourage short notes rather than exhaustive scoring. Validate usefulness before building charts or ranking algorithms.

## Possible business model
Free for a modest collection, with a one-time upgrade for unlimited entries and custom preparation templates. Keep basic backup and export available to everyone.
