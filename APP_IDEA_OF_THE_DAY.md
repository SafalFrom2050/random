# App Idea of the Day: Margin Map
Date: 2026-11-05 (Japan)

## Concept
A personal index for handwritten notebooks. Photograph a page, add a few searchable keywords and its page number, then find the physical note later without digitizing the entire notebook.

## Target users
Students, engineers, researchers, and journal users who prefer writing on paper but struggle to retrieve old notes.

## Problem
Useful sketches and explanations are buried across multiple notebooks. Full scanning requires too much effort, while a table of contents becomes outdated as topics reappear on later pages.

## Core workflow
1. Give a notebook a name and an optional cover photo.
2. When a page seems worth finding again, photograph it and enter its page number.
3. Add a title and two or three keywords.
4. Search across notebooks by topic.
5. Open a result to see the image and physical location, such as “Blue notebook, page 47.”
6. Link related pages without moving or rewriting the original notes.

Example: Searching “CAN termination” finds three relevant pages across two engineering notebooks.

## MVP features
- Notebook records with cover images and optional shelf-location notes.
- Page entries with manual page numbers, titles, keywords, and photos.
- Search across all notebooks with notebook and tag filters.
- Links between related entries.
- A quick capture queue for adding metadata later.
- Offline storage and ZIP backup export/import.

Keep handwriting recognition, cloud sync, automatic summaries, and full PDF notebook scanning outside the first release.

## Build approach
Build a Flutter app with SQLite for notebooks, page entries, keywords, and links. Store photos in app-private files and use local text search over user-entered metadata.

Allow page ranges and unnumbered pages with a custom location label. Warn about duplicate page entries but allow multiple topics on one page. Save a captured photo before opening the metadata form so interruptions do not lose it. Normalize image orientation and generate thumbnails for search results.

Export a versioned JSON manifest with original images. Validate imports and restore links by stable identifiers rather than titles. Start with manual indexing to test whether the retrieval benefit justifies capture effort before investing in OCR.

## Validation plan
Recruit eight frequent paper-note users for a two-week pilot.
- Ask each person to index five existing pages.
- After several days, give them a topic-retrieval task using their own notes.
- Compare retrieval time and success with their usual method.
- Measure capture effort and metadata fields commonly skipped.
- Track voluntary indexing of new pages after the initial task.
- Verify that backup restoration preserves images and cross-links.

Continue if five participants voluntarily add new entries and can retrieve a useful note faster than before. Treat the small study as a usability signal rather than proof of productivity gains.

## Biggest risk
Users may index pages inconsistently or choose keywords they do not remember later. Make titles searchable, show recently used tags, and allow quick capture followed by optional cleanup. If logging becomes burdensome, focus on a small set of high-value pages rather than complete notebook coverage.

## Possible business model
Free for a few notebooks, with a one-time upgrade for unlimited notebooks and printable topic indexes. Keep basic search and backup export available to everyone.
