# App Idea of the Day: Tabletop Takeover
Date: 2026-10-23 (Japan)

## Concept
A phone-based party game that turns objects already on a table into a playful auction. Players bid imaginary coins on everyday items, then reveal secret scoring rules that make an ordinary spoon unexpectedly valuable.

## Target users
Small groups of friends, families, and board-game clubs looking for a quick game with almost no preparation. The first version supports three to six players sharing one phone.

## Problem
Spontaneous game nights often stall because nobody brought a game, learning rules takes too long, or a phone game leaves everyone staring at separate screens.

## Core workflow
1. Place six harmless everyday objects on a table and name them in the app.
2. Enter player nicknames. Each player starts with 20 imaginary coins.
3. Pass the phone privately so each player can read a secret objective, such as “Collect items whose names contain the letter A.”
4. Reveal one item and hold a short spoken auction. The host enters the winner and winning bid.
5. Continue until every item is awarded, then reveal objectives and calculate scores.
6. Start a rematch using the same objects and new objectives.

Example: A pencil might earn base points, a bonus for being longer than a hand, and another bonus for completing a writing-tool collection.

## MVP features
- A guided setup for three to six players and six to ten objects.
- Manual item entry with simple host-confirmed tags such as “metal,” “soft,” and “used for writing.”
- Private objective screens with a handoff cover to reduce accidental reveals.
- A visible coin ledger that prevents bids above a player's remaining balance.
- Winner entry, undo, round progress, and a final score breakdown.
- A curated set of compatible objectives and a short practice round.

Use imaginary currency only. Keep online multiplayer, image recognition, user-created rule packs, and real purchases outside the first version.

## Build approach
Build a Flutter app with a local game-state model and bundled objective definitions. Save after every auction so an interrupted session can resume.

Represent objects with host-confirmed tags. Each objective is a deterministic scoring function over those tags and a player's won items. During setup, select only objectives that are achievable with the entered objects; show a warning if there are too few eligible objectives.

Use a fixed auction rule: bids increase by at least one coin, the last unchallenged bidder wins, and a no-bid item is discarded. Keep objective scoring and remaining-coin bonuses visible in the rules before play. Pilot the numbers for balance rather than assuming the initial values are fair.

## Validation plan
Observe five groups playing two rounds each with objects they choose.
- Measure time from opening the app to the first bid.
- Record rule questions, scoring disputes, and host entry mistakes.
- Ask whether players voluntarily want a rematch.
- Check whether losing players still felt they had meaningful choices.
- Try a deliberately awkward object set to test objective eligibility.

Proceed if at least four groups finish without facilitator intervention and three choose a rematch. Revise confusing objectives before adding more content.

## Biggest risk
Secret objectives may be uneven or impossible for a particular set of objects, making the result feel arbitrary. Validate eligibility before dealing objectives, start with simple tag-based rules, and test scoring balance across many object sets. Let the host correct tags before the first auction.

## Possible business model
Offer the core game free, then sell optional themed objective packs as one-time purchases. Keep all players in a shared session covered by the host's copy. Test repeat play before producing paid packs.
