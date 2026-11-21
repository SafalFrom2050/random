# App Idea of the Day: Fit Slip
Date: 2026-11-22 (Japan)

## Concept
A pocket reference of clothes that already fit, so shoppers can compare a new garment against a trusted favorite.

## Target users
People shopping secondhand online or in stores where sizes vary and trying things on is inconvenient.

## Problem
A size label says little about sleeve length or how a shirt sits. Measurements scattered across screenshots are hard to compare, and a body measurement does not directly describe the cut of a garment someone likes.

## Core workflow
1. Pick a favorite shirt or pair of trousers and create a reference card.
2. Follow a diagram to record a few flat garment measurements and fit notes.
3. Enter a candidate garment's comparable measurements to see the differences.
4. After wearing a purchase, note whether the comparison helped.

## MVP features
- Shirt and trouser templates with illustrated measuring points.
- Named reference garments with optional photos.
- Side-by-side measurement differences in centimeters or inches.
- Offline access and exportable reference cards.

## Build approach
Build a Flutter app with SQLite and local photo storage. Store canonical measurements in millimeters and convert only for display. Use manual entry and deterministic comparison; begin with ordinary shirts and trousers.

## Validation plan
Recruit eight secondhand shoppers. Ask each to measure a favorite garment and compare two candidates using seller measurements, then report their experience after any purchase they choose to make.

## Biggest risk
Seller measurements may use a different method, making a precise-looking difference misleading. Show the measuring diagram beside every comparison and let users mark a field as not comparable.
