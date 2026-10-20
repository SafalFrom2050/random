# App Idea of the Day: Resume Point
Date: 2026-10-21 (Japan)

## Concept
A tiny app that helps you restart interrupted projects. Before stopping, save a quick “resume card” containing what you just did, the exact next action, and the links or files you will need.

## Target users
Hobby developers, students, writers, and makers who switch between several projects and return after days or weeks away.

## Problem
Task lists say what needs doing but rarely preserve enough context to begin immediately. Returning to a project turns into rereading notes, reopening tabs, and remembering why you stopped.

## Core workflow
1. Create a project such as “Weekend game.”
2. Tap “Pause” and answer three prompts: “Where did you stop?”, “What is the next physical action?”, and “What might trip you up?”
3. Attach a link, screenshot, or short code snippet.
4. When returning, open a single resume card rather than the full project history.
5. Tap “Started” and optionally record whether the card helped. Replace the card at the next pause.

Example card:
- Stopped: The player moves, but collisions fail on the left wall.
- Next action: Open player.dart and reproduce the issue in level 2.
- Watch out: The test map uses a different tile size.
- Context: Repository link and a screenshot of the collision bounds.

## MVP features
- Project list with one current resume card per project.
- Three short text fields plus links and one optional image.
- Automatic save and a last-updated timestamp.
- Share-sheet capture for adding a URL to a project.
- Search, project archiving, and Markdown export/import.
- Optional user-scheduled reminder to reopen a project.

Keep collaboration, AI summaries, time tracking, and full task management outside the initial scope.

## Build approach
Build a Flutter mobile app with SQLite for projects and cards, app-private image storage, and native share-sheet integration. Store everything locally and require no account. Use a simple Markdown export with bundled image files for backups. Treat shared URLs as references; the app does not need to fetch or summarize their contents.

The central data model is Project → CurrentResumeCard, with a small attachment list. Editing a card replaces its content; undo can protect against accidental edits without introducing a complex history interface.

## Validation plan
Recruit six people with at least two unfinished projects. For one week, ask them to save a card before pausing and return to the project at least twice.
- Record self-reported minutes from opening the project to taking the first useful action.
- Compare with each participant's usual restart process.
- Check how often cards are saved without a reminder.
- Ask whether a three-field card feels useful or burdensome.

Continue only if at least four participants voluntarily use it again and describe a concrete restart it made easier. Treat the small study as directional evidence, not proof of demand.

## Biggest risk
People may forget to write the card when stopping, leaving nothing useful to resume from. Make saving possible in under 30 seconds, preserve unfinished drafts, and let users save just the next action when rushed.

## Possible business model
A free version for a few active projects and a one-time upgrade for unlimited projects, custom prompts, and richer exports. Validate repeat use before building paid features.
