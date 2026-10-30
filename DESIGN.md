---
name: Date Itinerary & Auto-Rundown Planner
description: Single-Stream Dynamic 2-Column Date Planner for couples with smart auto-sorting and real-time sync.
colors:
  primary: "#e11d48"
  primary-hover: "#be123c"
  primary-light: "#fff1f2"
  neutral-bg: "#faf8f5"
  neutral-card: "#ffffff"
  neutral-border: "#f2ece4"
  neutral-text: "#27272a"
  neutral-muted: "#71717a"
  huda-accent: "#0284c7"
  huda-bg: "#f0f9ff"
  huda-border: "#bae6fd"
  kenia-accent: "#f43f5e"
  kenia-bg: "#fdf2f8"
  kenia-border: "#fbcfe8"
  bareng-gradient-start: "#fff1f2"
  bareng-gradient-end: "#fef3c7"
  amber-accent: "#d97706"
typography:
  headline:
    fontFamily: "Plus Jakarta Sans, sans-serif"
    fontWeight: 700
    letterSpacing: "-0.02em"
  body:
    fontFamily: "Plus Jakarta Sans, sans-serif"
    fontWeight: 500
    fontSize: "0.875rem"
    lineHeight: 1.5
rounded:
  sm: "8px"
  md: "12px"
  lg: "16px"
  full: "9999px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "#ffffff"
    rounded: "{rounded.md}"
    padding: "10px 18px"
  card-activity:
    backgroundColor: "{colors.neutral-card}"
    rounded: "{rounded.lg}"
    padding: "16px 20px"
---

# Design System

## Overview

A grounded, warm, intimate interface designed for couples to plan shared itineraries effortlessly. Built around a **Single-Stream Dynamic 2-Column Grid** where individual routines occupy separate columns (Huda on the left, Kenia on the right) and converge into wide romantic cards (Bareng) in the middle.

## Colors

- **Neutral Canvas**: `#faf8f5` provides warm, tactile paper softness, avoiding sterile clinical white.
- **Card Surface**: Pure `#ffffff` framed with subtle warm borders (`#f2ece4`).
- **Brand & Shared Accent**: Rose red (`#e11d48`) representing romance, passion, and togetherness.
- **Huda's Stream**: Calm sky blue (`#0284c7`) with soft ice blue tint (`#f0f9ff`).
- **Kenia's Stream**: Tender blossom rose (`#f43f5e`) with delicate blush tint (`#fdf2f8`).
- **Shared Moments (Bareng)**: Romantic dual-tone gradient from rose mist to warm sunrise amber (`#fff1f2` to `#fef3c7`).

## Typography

- **Font Family**: Google Fonts *Plus Jakarta Sans*, modern geometric neo-grotesque with humanistic warmth.
- **Hierarchy**:
  - `h1`: 16px to 18px Bold tracking-tight.
  - Section Titles: 14px to 16px Bold.
  - Card Titles: 14px Bold.
  - Time & Badges: 11px to 12px Semi-Bold / Font-Mono for numerical clarity.
  - Notes & Subtext: 11px to 12px Medium.

## Layout

- **Split Desktop Structure**: Sticky input control panel (4 columns / 33%) on the left, wide timeline stream (8 columns / 67%) on the right.
- **Time-Grid Calendar Canvas (Google Calendar Day-View)**:
  - Vertical Time Axis: Sumbu kiri dengan label jam (06:00 sampai 24:00) dan garis horizontal tipis per jam + garis putus-putus per 30 menit.
  - Huda Lane: Jalur kiri (`left: 4px; width: calc(50% - 8px)`).
  - Kenia Lane: Jalur kanan (`left: calc(50% + 4px); width: calc(50% - 8px)`).
  - Bareng Card: Melebar menembus kedua kolom (`left: 4px; width: calc(100% - 8px); z-index: 12`).
  - Proportional Height & Top: Dihitung otomatis per rasio jam (60px atau 80px per jam, 1 menit = 1px atau 1.33px).
- **Mobile Reflow**: Scroll horizontal lembut (`overflow-x-auto`) menjaga keterbacaan kolom dan proporsi jam pada layar ponsel.

## Elevation & Depth

- **Ground Plane**: Cards sit flat with crisp borders (`1px solid #f2ece4`).
- **Hover Elevation**: Micro lift with subtle warm shadow (`box-shadow: 0 4px 14px -2px rgba(225, 29, 72, 0.06)`).
- **Single Glass Surface**: Header navigation uses soft backdrop blur (`bg-white/95 backdrop-blur-md`). All other containers remain solid.

## Shapes

- Small interactive elements (chips, badges, icons): `rounded-lg` (8px).
- Action buttons and input fields: `rounded-xl` (12px).
- Content cards, panels, and modals: `rounded-2xl` (16px).
- Pips and status indicators: `rounded-full`.

## Components

- **Owner Toggle**: Radio-like trio buttons (`Huda`, `Kenia`, `Bareng`) with real-time hint updates.
- **Quick Duration Chips**: Instant time-math chips (`15m`, `30m`, `45m`, `1 Jam`, `1.5 Jam`, `2 Jam`, `3 Jam`, `4 Jam`) that automatically format start-end ranges.
- **Done Toggle**: Inline checklist button with green state transition and strike-through title.
- **Connection Badge**: Solid semantic state indicator (Green = Connected, Amber = Connecting, Red = Disconnected).

## Do's and Don'ts

### Do
- Maintain strict start-time chronological order.
- Use semantic SVG icons for UI actions and buttons.
- Keep touch targets at minimum 40px to 44px on mobile devices.
- Preserve all user data in local storage with full undo/redo stack (`Ctrl+Z`, `Ctrl+Y`).

### Don't
- Don't use decorative emoji spam in UI text, labels, or buttons.
- Don't use endless animation loops (`pulse`, `ping`) on status indicators.
- Don't force rigid time blocks—allow couples to enter single times (`08:20`) or flexible ranges (`15:00 - 19:00`).
- Don't separate Huda and Kenia into disconnected tabs; keep them in a unified alternating timeline.
