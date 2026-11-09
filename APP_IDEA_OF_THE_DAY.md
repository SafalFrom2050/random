# App Idea of the Day: Same Frame
Date: 2026-11-10 (Japan)

## Concept
A camera app that overlays a previous photo as a guide so you can photograph the same scene from the same angle over time.

## Target users
Gardeners documenting a season, DIY builders tracking a project, and photographers making long-term visual studies.

## Problem
A before-and-after comparison can be hard to read when framing and distance change. Finding an old photo and switching back and forth with the camera slows down each repeat shot.

## Core workflow
1. Create a series and take its reference photo.
2. When returning, open that series and adjust the opacity of the reference over the camera preview.
3. Line up two stationary features, such as the corners of a planter, and take a new shot.
4. Compare any two dates with a swipe and export the pair as a labeled image.

## MVP features
- Local series with a reference photo, dates, and optional notes.
- Adjustable preview overlay and a grid.
- Date picker, swipe comparison, and labeled image export.

## Build approach
Build a phone app with Flutter, app-private photo storage, and SQLite for series metadata. Preserve capture orientation and normalize the preview and reference to the same visible crop. Start with manual alignment.

## Validation plan
Have six participants document two scenes over three visits. Compare how long they take and how consistently they frame the scene with the overlay versus the default camera.

## Biggest risk
Changes in light, lens, or viewpoint can make a close match impossible. Let users hide the overlay at any time, and show the original photos so people can judge the comparison for themselves.
