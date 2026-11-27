# App Idea of the Day: Caption Keeper
Date: 2026-11-28 (Japan)

## Concept
A private photo-caption collection tool that helps a family album organizer ask relatives who, where, and when a picture shows.

## Target users
People assembling a small family photo book from scanned prints with incomplete labels.

## Problem
A relative may recognize a person in a photograph but never send the answer back in a form the organizer can connect to the right image. Long message threads mix confident identifications with guesses.

## Core workflow
1. The organizer uploads a small set of scans and gives each photo a short code.
2. A relative opens a private invitation link, views one photo at a time, and adds what they remember.
3. The organizer reviews answers, asks about disagreements, and approves a caption.
4. Export the approved captions with photo codes for use in a photo-book editor.

## MVP features
- Small private collections and revocable invitation links.
- Mobile response form with “not sure” and “skip” choices.
- Review queue that preserves separate answers.
- CSV export of approved captions and unresolved photo codes.

## Build approach
Build a mobile web app with organizer sign-in, a relational database, and private image storage. Invitation tokens grant access only to their collection. Start with still images and text responses; keep book layout and printing outside the MVP.

## Validation plan
Recruit five album organizers and two relatives per organizer. Ask them to identify ten previously unlabeled photographs, comparing the effort with their normal messaging workflow.

## Biggest risk
Different relatives may confidently remember different things, and the tool could make a guess look definitive. Preserve answer provenance and uncertainty, and require organizer review before a caption becomes approved.
