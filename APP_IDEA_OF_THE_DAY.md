# App Idea of the Day: Doorstep Directions
Date: 2026-11-09 (Japan)

## Concept
Create a short visual guide for the last 100 meters of a trip, from a map pin to the actual entrance.

## Target users
Workshop hosts, pop-up organizers, and small venues whose doors are easy to miss.

## Problem
A map can get visitors to the right building while leaving them at a locked gate or the wrong side of a complex. Hosts then repeat the same directions by phone.

## Core workflow
1. Pick a recognizable starting point near the venue.
2. Add up to five photos with brief instructions, such as “walk past the bicycle racks and take the second door.”
3. Preview the guide as a visitor and share its link.
4. Visitors follow the steps in a mobile browser and can reopen a previously cached guide if their connection drops.

## MVP features
- Phone-friendly editor for ordered photos and text.
- Account-free visitor view with large images and readable captions.
- Expiring links, a revoke button, and a printable text version.

## Build approach
Use a mobile web app with a small database for guide metadata and object storage for compressed images. Require sign-in only for authors. Serve guides through unguessable share links and cache previously opened steps for intermittent connectivity.

## Validation plan
Recruit three venues and observe first-time arrivals. Compare time from map pin to door and calls for help against each venue's usual directions.

## Biggest risk
A stale photo can send someone to the wrong entrance. Give every guide a visible last-reviewed date and let hosts revise or revoke it quickly.

## Route alternatives and offline behavior
Allow authors to add an optional alternate route, with the reason stated at the start (for example, “Avoid the stairs”). Have hosts walk each route before publishing, label any opening-hour restrictions, and provide text directions even when a photo fails to load. Downloading a guide requires a connection; once downloaded, show its version and date. Revocation blocks future online loads, but cannot erase copies already cached or printed. Strip location metadata from uploads and prompt authors to crop faces and access codes.

## Pilot decision
At each venue, alternate between standard instructions and the guide across at least ten first-time arrivals. Start timing at the same landmark, record wrong entrances and calls separately, and ask visitors who did not open the guide why. Continue if at least two venues see faster median arrival with no increase in wrong entrances. Test one cached route in airplane mode before inviting visitors.
