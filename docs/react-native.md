# React Native (Stash Tracker)

## Repo

- **Name:** stash-tracker
- **Owner:** c3p0talksalot-ai
- **URL:** https://github.com/c3p0talksalot-ai/stash-tracker

## Stack

- React Native (Ignite boilerplate)
- WatermelonDB (SQLite ORM)
- Zustand (state management)
- MMKV (persistence)
- Expo (camera, image picker)

## Architecture

### Database Schema (WatermelonDB)

Tables:
-  — Core inventory items (name required)
-  — Key/value/unit for items
-  — Files attached to items
-  — Key-value metadata for attachments
-  — User-defined tags with dedup support
-  — Many-to-many join table
-  — User preferences

### Tag Dedup Strategy

- Normalize: trim whitespace, lowercase, slugify
- On create: query for existing , reuse if found
- Similarity detection: Dice coefficient (>80% match = warning)

### AI Detection Flow

1. User captures image
2. Call LLM API (local or cloud)
3. Parse response for tags + properties
4. Show approve/reject list
5. Apply accepted to item

### Smart Suggestions

Collect property keys from items with matching tags, sort by frequency.

## Git Workflow

### Branch Strategy

-  — production-ready
- Feature branches:  (e.g., )

### Before PR



### Commit Messages



### Pre-Push Hook

Warns if main has new commits, offers to cancel or proceed.

### Aliases

