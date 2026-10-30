# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

HTML5, Tailwind CSS, Vanilla JavaScript (zero-build single-page web app architecture)

## Users

Couples planning dates, weekend itineraries, and multi-day travels together in real-time.

## Product Purpose

A dynamic Time-Grid date planner (Google Calendar Day-View style) that visualizes parallel routines (Huda in Column 1, Kenia in Column 2) converging into shared activities (Bareng spanning both columns), featuring proportional hourly heights, automatic vertical positioning, smart duration presets, multi-day support, and cross-device synchronization.

## Positioning

Unlike rigid calendar apps or disjointed notes, it models dating reality: couples prepare separately, meet up for joint moments, split for individual errands, and reunite in the evening, all rendered in an alternating dynamic stream with one-click WhatsApp export.

## Operating Context

- Mobile and laptop browsers during planning sessions or on-the-go during the date.
- Real-time shared session via simple URL query parameters (`?room=ID`).
- Offline-resilient local persistence backed by instant undo/redo history.

## Capabilities and Constraints

- **Time-Grid Calendar 2-Column Canvas**: Vertical time axis (06:00 to 24:00) with thin hourly grid lines. Column 1 for Huda (`left: 0; width: 50%`), Column 2 for Kenia (`left: 50%; width: 50%`), and Merged for Bareng (`left: 0; width: 100%`) spanning across both lanes.
- **Proportional Card Height & Positioning**: Top offset strictly proportional to start time minutes (`top: (startMinutes - 360) * scale`); card height strictly proportional to duration (`height = durationMinutes * scale`, with default 30-min pin height for single timepoints). Toggleable scale presets (`60px/jam` and `80px/jam`).
- **Auto-Sort Timeline Flow**: Activities are automatically ordered chronologically based on parsed start times.
- **Smart Time Auto-Fill & Quick Chips**: Automatically suggests the next chronological slot and formats time ranges (`15:00 - 19:00`) with quick duration chips (`15m` through `4 Jam`).
- **Multi-Day Tabs**: Independent schedules, anchor times, and metrics per day.
- **Cross-Device Cloud Sync**: Dual-channel synchronization (cloud WebSocket relay and Firebase Realtime Database) with clear connection state badges.
- **Zero Build Dependency**: Runs in any modern browser without build pipelines, deployable to static hosting like Vercel or GitHub Pages.

## Brand Commitments

- **Aesthetic**: Warm romantic, grounded, tactile, and clean.
- **Color Identity**: Soft warm background (`#faf8f5`), high-contrast stone typography (`#27272a`), rose accent (`#e11d48`) for brand & shared activities, sky blue (`#0284c7`) for Huda, and rose-pink (`#f43f5e`) for Kenia.
- **Tone**: Intimate, encouraging, and distraction-free.

## Evidence on Hand

- Runnable single-page application at `index.html`.
- Tested on desktop and mobile viewports with full keyboard shortcuts (`Ctrl+Z`, `Ctrl+Y`).

## Product Principles

1. **Natural Interleaving**: Separate routines and shared moments flow together chronologically without forced artificial silos.
2. **Never Lose Work**: State is immediately persisted to local storage, backed by full undo/redo history and safe confirmation gates.
3. **Restraint Over Noise**: Semantic iconography, solid status indicators, and clean typography over decorative AI cliches.
4. **Instant Action**: Direct WhatsApp formatting and room sharing without requiring accounts or logins.

## Accessibility & Inclusion

- WCAG AA color contrast ratios across all cards, badges, and controls.
- Minimum 40px to 44px tap targets for mobile usability.
- Visible focus rings (`outline: 2px solid #e11d48`) for keyboard navigation.
