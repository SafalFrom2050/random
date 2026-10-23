# App Idea of the Day: Fit Through
Date: 2026-10-24 (Japan)

## Concept
A furniture-shopping companion that keeps the measurements of your home’s narrow spots and checks a product against them before you buy. It highlights which doorway, lift, or stair landing needs a closer look.

## Target users
Apartment renters, people moving home, and anyone shopping for bulky furniture without a professional delivery survey.

## Problem
A sofa can fit in a room but be difficult to get there. Measurements are scattered across notes and photos, while product listings may distinguish poorly between assembled and packaged dimensions.

## Core workflow
1. Create a delivery route: building entrance, lift, hallway, apartment door, and final room.
2. Enter clear opening measurements manually and attach photos with notes about handles, steps, and turns.
3. Add a product’s packaged dimensions, assembled dimensions, and whether legs or panels can be removed.
4. See a checkpoint-by-checkpoint comparison showing clearances and missing measurements.
5. Export a concise measurement sheet to discuss with the seller or delivery team.

Example: A boxed desk has adequate clearance at the apartment door, but the lift depth is unknown. The app marks the lift as “needs measurement” and makes no overall delivery claim.

## MVP features
- Saved home profiles with an ordered list of delivery checkpoints.
- Manual dimensions with units, measurement dates, and photos.
- Separate product records for packaging and assembled size.
- A conservative rectangular-opening comparison with user-selected orientation.
- A user-set clearance margin and explicit “unknown” results for incomplete inputs.
- PDF measurement-sheet export and local backup.

Start with straight openings and static measurements. Camera measurement, augmented reality, automatic stair-turn simulation, retailer scraping, and delivery booking stay outside the MVP.

## Build approach
Build a Flutter app with SQLite for home profiles, checkpoints, and products, plus local storage for photos. Normalize calculations to millimeters while preserving the user’s display units.

For a straight opening, compare the two cross-section dimensions of the selected product orientation against the clear opening and chosen margin. Show the calculation and each clearance instead of a single green “fits” badge.

Treat corners, stairs, route length, weight, and lifting access as separate unresolved constraints. A successful opening comparison must never become an overall delivery guarantee. Generate the export from the same stored measurements so screen and document agree.

## Validation plan
Recruit eight people who recently moved or are shopping for furniture.
- Ask them to record a route and evaluate two products using supplied dimensions.
- Observe unit mistakes, confusion about packaging, and time required for setup.
- Have a delivery professional review anonymized sample sheets for missing practical details.
- Test known straight-opening examples and confirm that incomplete or turning routes remain unresolved.
- Ask whether participants would send the sheet to a seller before purchasing.

Proceed if six participants complete a comparison without help and the professional finds the sheet useful for follow-up questions. Evaluate usefulness first; do not claim the app predicts successful deliveries.

## Biggest risk
A reassuring result could create false confidence because real delivery depends on rotation space, protrusions, packaging, weight, and handling constraints. Limit the MVP to transparent dimension checks, distinguish measured facts from assumptions, and flag every unmodeled checkpoint prominently.

## Possible business model
A free home profile with a few saved products, followed by a one-time upgrade for multiple homes and unlimited product comparisons. Keep measurement export available in the free version so users can verify details with a delivery team.
