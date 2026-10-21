# App Idea of the Day: Sound Postcard
Date: 2026-10-22 (Japan)

## Concept
An audio diary for collecting the sounds of ordinary places: rain on a balcony, a festival street, a train arriving, or a quiet kitchen. Each postcard pairs a short recording with one photo and a sentence about the moment.

## Target users
Travelers, people living away from home, and anyone who enjoys keeping small personal memories without writing a journal.

## Problem
Photos preserve how a moment looked but often lose its atmosphere. Voice memo apps capture sound, yet recordings become a list of anonymous files that people rarely revisit.

## Core workflow
1. Tap “Capture” and record up to 30 seconds of ambient sound.
2. Add an optional photo, title, and one-line memory.
3. Choose a broad place label such as “Kathmandu rooftop”; exact coordinates are unnecessary.
4. Browse postcards by month or a personal collection.
5. Open a postcard to hear the moment while viewing its photo.
6. Export selected postcards as a portable collection.

Example: A photo of a paper kite, the sound of wind and distant celebrations, and the caption “The afternoon we finally got it flying.”

## MVP features
- Short audio recording with visible duration and playback preview.
- One optional photo and caption per postcard.
- Collections, text search, and a chronological gallery.
- A “revisit a random memory” button.
- Local storage, deletion, and ZIP export/import containing audio, images, and a JSON manifest.
- Clear handling of interrupted recordings and low storage.

Start with personal collections. Public feeds, automatic transcription, cloud sync, and social messaging can wait.

## Build approach
Build a Flutter app using native audio recording APIs and SQLite for metadata. Store compressed audio and photos in app-private files. Use generated identifiers for filenames and export relative paths in a versioned manifest.

Request microphone access when the user starts recording and photo access only when attaching an image. Keep recording in the foreground for the MVP. Save each completed recording before opening the caption editor so an interrupted edit does not lose the sound.

## Validation plan
Recruit eight people for a two-week pilot, including travelers and people living abroad.
- Ask each person to capture at least three moments, then leave subsequent use voluntary.
- Measure capture completion, voluntary additional postcards, and playback of older postcards.
- Ask participants to compare one sound postcard with a photo of the same moment.
- Test export and restore on a second device.

A useful early signal would be at least five participants creating another postcard voluntarily and describing a memory that audio helped them revisit. This is a small exploratory study, not proof of a market.

## Biggest risk
The novelty may wear off, leaving recordings nobody replays. Make playback immediate, keep capture short, and test whether the random-memory feature brings people back. If people enjoy recording but never revisiting, reconsider the diary premise before adding features.

Recordings may also capture private conversations. Keep collections private by default, offer easy trimming and deletion, and let users review every recording before exporting it.

## Possible business model
A free personal diary with a one-time upgrade for custom collection covers and richer export presentation. Keep basic backup export available to everyone. Consider paid cloud backup only after repeat use and storage costs are understood.
