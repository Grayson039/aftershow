# AFTERSHOW — Claude Code Project Instructions

*"Letterboxd for concerts — your full lifetime show history, no proof needed."* Conceived at a Black Queen show. Built as a portfolio-grade project.

---

## Your Role

You are acting as **Senior Mobile Developer, Lead UI/UX Designer, and Expert AI Consultant** on this project.

**Tone:** Candid, professional, humorous, and critical. Push back sharply on bad ideas or scope creep. Do not sugarcoat.

---

## Project Goal

Build a portfolio-grade project from scratch, including:

- Case studies
- Figma assets
- GitHub prototype

---

## Direct Competitor

**Concert Archives** — primary competitor to benchmark and differentiate against.

---

## Non-Negotiable Workflow Rules

1. **Maintain a living Project Log** (README.md at repo root). Update it with every core decision, tech stack change, and UX architecture update at every major milestone.
2. **Do not proceed to a new phase** without:
   - Announcing the transition
   - Updating the Project Log
   - Confirming readiness with the user
3. **Phase gates are hard stops.** No skipping.

---

## Project Phases

| Phase | Name | Status |
|:---:|:---:|:---:|
| 1 | Ideation, Competitive Analysis & Feature Differentiation | ✅ Complete |
| 2 | UX Architecture (User Personas, Journeys, Information Architecture) | ✅ Complete |
| 3 | UI Design & Asset Creation (Figma Wireframes & Component Specs) | 🔄 In Progress |
| 4 | Technical Architecture & Prototype Development (GitHub Repo Setup & Code) | 🔒 Locked |
| 5 | Case Study Compilation & Portfolio Readiness | 🔒 Locked |

---

## Current Phase: Phase 3 — UI Design & Asset Creation

### Phase 3 Deliverables

- Figma wireframes for all 14 MVP screens (dark + light mode)
- Full component spec sheet
- Design system documented and finalized

---

## Product Overview

**Aftershow** is a concert logging and social discovery app for die-hard live music fans.

### Core Value Prop

The **"from memory" log** — users can add any show they've ever attended with no ticket, no proof, no location check required. Just artist, venue, date, setlist as best remembered, and a rating. This unlocks the lifetime diary use case no other app has.

### Target Users

- **Primary:** Die-hard fans — setlist nerds, collectors, 100+ show attendees. They populate data, write reviews, become community backbone.
- **Secondary:** Casual concertgoers who want a simple way to remember attended shows.

---

## MVP Feature Set (P0)

| Feature | Description |
|:---:|:---:|
| Setlist Logging | Log any show — live or from memory. Artist, venue, date, setlist, rating, notes. |
| From Memory Tag | Shows without ticket verification show a subtle "from memory" indicator. No gatekeeping. |
| Friends Feed | Chronological feed of shows logged by followed users. |
| Star Ratings & Notes | 5-star rating + short free-text note per show. |
| Personal Concert Archive | Full show history — sortable by artist, year, venue, rating. |

## P1 Features (Post-MVP)

- Rare Song Badge (auto-flag for songs not played recently)
- Artist Pages
- Tour Dates (via Bandsintown/Songkick API)

## P2 Features (Future)

- Stats & Milestones ("You've seen this artist 8 times")
- AI Logging Assist (fuzzy input → Setlist.fm API match via Claude API)
- Import History (Concert Archives migration path)

---

## Design System

### Type System (Shared — Both Modes)

| Role | Typeface | Size | Usage |
|:---:|:---:|:---:|:---:|
| Display | Playfair Display Italic 700 | 28–40px | Screen titles, artist names, show titles |
| Body / Setlist | Crimson Pro Italic 400 | 13–16px | Setlist songs, notes, quotes |
| UI Labels | DM Mono 400–500 | 9–12px | Field labels, tabs, metadata, timestamps |
| Bold UI | Syne 800 | 13–20px | Usernames, bold labels |

All typefaces available via Google Fonts at no cost.

### Color Palette

**Dark Mode — Dark Vintage**

| Token | Hex | Usage |
|-------|-----|-------|
| bg-base | #0C0C0C | App background |
| bg-card | #111111 | Feed cards, list items |
| border | #1E1E1E | Card outlines |
| divider | #181818 | Section separators |
| text-primary | #F0F0F0 | Artist names, show titles |
| text-secondary | #888888 | Usernames, metadata |
| text-tertiary | #555555 | Supporting info |
| field-label | #6B6B6B | Form field labels (DM Mono 9px uppercase) |
| accent-gold | #D4A853 | Active tabs, stars, rare badge, logo dot |
| gold-tint | #3A2E10 | Rare badge border, filled field border |

**Light Mode — Vintage Bold**

| Token | Hex | Usage |
|-------|-----|-------|
| bg-base | #EDE6D3 | App background — warm cream |
| bg-card | #F7F2E6 | Feed cards, elevated surfaces |
| border | #D8CCAA | Setlist separator, subtle borders |
| border-inner | #C8BCA0 | Inner dividers, muted outlines |
| text-primary | #1A1209 | All primary text, logo, nav bg |
| text-body | #4A3E2A | Setlist song text |
| text-secondary | #9A8C74 | Venues, timestamps, subtitles |
| text-tertiary | #B8A880 | Song numbers, muted labels |
| accent-gold | #D4A853 | Shared with dark — connective thread |
| accent-rust | #C4401C | Error states, edge case persona |

### Design Principles

1. **Utility over decoration** — setlist is the hero
2. **The show is the product** — all flows lead to the "+" log button
3. **No gatekeeping** — "from memory" is a feature, not a warning
4. **Dark and light are equal** — gold (#D4A853) is the connective thread
5. **Respect the culture** — designed for people who've stood in a pit at 11pm on a Tuesday

---

## MVP Screen Inventory

| Screen | Description | Nav |
|:---:|:---:|:---:|
| My Shows (Archive) | Full personal concert history | Tab 1 |
| Show Detail | Individual show log with setlist | Via archive/tap |
| Stats Dashboard | Personal milestones and stats | Tab 1 overflow |
| Friends Feed | Shows logged by followed users | Tab 2 |
| Global Feed | All recent logs | Tab 2 (tab) |
| Tonight Feed | Shows happening right now | Tab 2 (tab) |
| Log a Show | Artist, venue, date, setlist, rating, notes. Live vs. from memory toggle. | Tab 3 (center CTA) |
| Search / Discover | Search artists, users, venues | Tab 4 |
| Artist Page | Setlist history, upcoming tours, fan logs | Via search/tap |
| Show Page | All fan logs, aggregated setlist, ratings | Via feed/tap |
| User Profile | Full concert history, stats, followers/following | Tab 5 |
| Followers/Following | Social graph | Via profile |
| Settings | Dark/light toggle, notifications, account | Tab 5 overflow |
| Onboarding | Build concert history first | First launch |

**MVP Screen Count: 14**

---

## Tech Stack (Provisional — Confirmed in Phase 4)

| Layer | Decision | Notes |
|:---:|:---:|:---:|
| Framework | React Native | Cross-platform mobile |
| Setlist Data | Setlist.fm API | Free tier covers MVP |
| Tour Data | Bandsintown or Songkick | TBD in Phase 4 |
| AI Layer | Claude API (Anthropic) | ~200 tokens/call. Nearly free. v1.1 feature. |

### Data Model (Draft)

```
User → Shows → Songs
Artist → Shows
Venue → Shows
```

---

*AFTERSHOW · The show never really ends.*
