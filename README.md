# aftershow.

*"Letterboxd for concerts — your full lifetime show history, no proof needed."* Conceived at a Black Queen show. Built as a portfolio-grade project.

---

## Project Status

| | |
|:---:|:---:|
| **Current Phase** | Phase 3 — UI Design & Asset Creation |
| **Last Updated** | May 17, 2026 |
| **Version** | 0.3.0 |

---

## What Is Aftershow?

A concert logging and social discovery app for die-hard live music fans. Users build a lifelong record of every show they've attended, log setlists, rate performances, and follow friends to see what they've been to.

**The key differentiator:** The "from memory" log. Users can add any show they've ever been to — no ticket, no proof, no location check required. Just artist, venue, date, setlist as best you remember, and a rating. This unlocks the lifetime diary use case that no other app has.

**Direct competitor:** Concert Archives

---

## Project Phases

| Phase | Name | Status |
|:---:|:---:|:---:|
| 1 | Ideation, Competitive Analysis & Feature Differentiation | ✅ Complete |
| 2 | UX Architecture | ✅ Complete |
| 3 | UI Design & Asset Creation | 🔄 In Progress |
| 4 | Technical Architecture & Prototype Development | 🔒 Locked |
| 5 | Case Study Compilation & Portfolio Readiness | 🔒 Locked |

---

## Decision Log

Every major call made, in order. This is the paper trail for the Phase 5 case study.

### Phase 1 — Ideation & Competitive Analysis

| Date | Decision | Rationale |
|:---:|:---:|:---:|
| May 17, 2026 | Project initiated | Conceived at a Black Queen show at Thalia Hall |
| May 17, 2026 | Primary competitor: Concert Archives | Most feature-equivalent product. Deep data, zero soul. |
| May 17, 2026 | 3 UX gaps identified | AI-assisted logging, archive as identity, private-first social |
| May 17, 2026 | AI logging assist → v1.1, not MVP | Setlist.fm API covers 80% of cases free. AI layer is an enhancement, not a foundation. |
| May 17, 2026 | North Star user: die-hard fan (100+ shows) | Populates data, writes reviews, becomes community backbone |

### Phase 2 — UX Architecture

| Date | Decision | Rationale |
|:---:|:---:|:---:|
| May 17, 2026 | Onboarding entry point: build concert history first | Differentiates from every competitor who pushes upcoming shows |
| May 17, 2026 | Primary return loop: archive browsing & reminiscing | Unique behavior no competitor owns. Upcoming shows = Bandsintown's territory. |
| May 17, 2026 | Social weight: equal pillar — not the lead | Letterboxd model. Diary first, shareable second. |
| May 17, 2026 | Upcoming shows: feature, not the hook | Keep it. Remove it from top-level nav priority. |
| May 17, 2026 | My Shows = Tab 1, not Feed | The archive is the product. The feed is the reward. Biggest architectural departure from competitors. |
| May 17, 2026 | Onboarding threshold: 1-show minimum | 3-show threshold alienates users early in their concert journey. Encourage more, never gate on it. |
| May 17, 2026 | Social unlocks after first show logged | Archive must be seeded before feed has value |
| May 17, 2026 | 14 MVP screens across 5 tabs | Confirmed scope for portfolio piece |

### Phase 3 — UI Design & Asset Creation

| Date | Decision | Rationale |
|:---:|:---:|:---:|
| May 17, 2026 | Design both themes simultaneously | Portfolio piece — dual-mode design from day one signals craft |
| May 17, 2026 | Log a Show as anchor screen | Contains every component: toggle, inputs, setlist, rating, badge, CTA. Design system derives from this. |
| May 17, 2026 | One type system, two color palettes | Cleaner, more maintainable. Bebas Neue is one-note. Playfair has range. |
| May 17, 2026 | Field label color: #6B6B6B (Option B) | #555 illegible, #4A4A4A worse. #6B6B6B — readable, subordinate, doesn't compete with values. |
| May 17, 2026 | Onboarding: theme picker with live preview | Dark/light toggle at top of onboarding — tapping it updates an example screen in real time. Signals that both modes are equal, not an afterthought in settings. |
| May 17, 2026 | Show card photo fallback hierarchy | User photo → community top-voted artist photo → empty state. Community photos (P1) are load-bearing for P0 card design — both must be designed together. Creates a virtuous loop: contributors improve the experience for the whole network. |
| May 17, 2026 | Friends Feed: interactive tabs (Friends / Global / Tonight) | First interactive prototype element. Tab switching via JS — both phones sync. Global shows geo-tagged logs from strangers worldwide. Tonight shows live-logging cards with pulsing LIVE indicator. Foundation for full prototype chain. |
| May 17, 2026 | User Profile screen completed | Archive-first (no upcoming show hero). Stats as identity flex (4-up gold numbers). No internal tab bar — one scroll. Ranked lists: Top Artists, Genres, Venues. Concerts Per Year bar chart with COVID dip. Direct response to Concert Archives teardown. |
| May 17, 2026 | Import from CSV/spreadsheet added as P1 feature | Critical for switching cost. Mimsie (primary real test user) has 229 shows in Concert Archives — can't require manual re-entry. Supports generic CSV so any tracker works, not just Concert Archives export. |
| May 17, 2026 | Marshall/Orange amp texture references | Dark mode: subtle gold dot grain on #0C0C0C (Marshall tolex), gold-tinted nav border (gold piping). Light mode: diamond crosshatch at 4.5% opacity on #EDE6D3 (Orange baffle board). Subconscious music culture signal — referential, not derivative. |
| May 17, 2026 | Real test users identified | Mimsie (wife, 229 shows in Concert Archives — primary switcher target), xSasquatchx/Bryant (Mastodon/Gojira/Baroness/DEP fan), Sako H. (iOS developer, SwiftUI — will evaluate technical buildability, not just UX). |

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

### Color Tokens

#### Dark Mode — Dark Vintage

| Token | Hex | Usage |
|:---:|:---:|:---:|
| bg-base | #0C0C0C | App background |
| bg-card | #111111 | Feed cards, list items |
| border | #1E1E1E | Card outlines |
| divider | #181818 | Section separators |
| text-primary | #F0F0F0 | Artist names, show titles |
| text-secondary | #888888 | Usernames, metadata |
| text-tertiary | #555555 | Supporting info |
| accent-gold | #D4A853 | Active tabs, stars, rare badge, logo dot |
| gold-tint | #3A2E10 | Rare badge border, filled field border |

#### Light Mode — Vintage Bold

| Token | Hex | Usage |
|:---:|:---:|:---:|
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

---

## Information Architecture

### Navigation (5 Tabs)

| Tab | Name | MVP Screens |
|:---:|:---:|:---:|
| 1 | My Shows ← *archive leads* | Archive View, Show Detail, Stats Dashboard |
| 2 | Feed | Friends Feed, Global Feed, Tonight Feed |
| 3 | Log *(center CTA)* | Log a Show, Live Now Mode, From Memory Mode |
| 4 | Discover | Search, Artist Page, Show Page |
| 5 | Me | Profile, Followers/Following, Settings |

### MVP Screen Count: 14

---

## User Personas

| Persona | Archetype | Priority | Key Need |
|:---:|:---:|:---:|:---:|
| Marcus, 34 | The Archivist | ★ North Star | Fast bulk logging, stats that validate his 200+ show history |
| Jordan, 27 | The Casual Logger | Secondary | Low friction logging, social discovery via friends |
| Dana, 41 | The Skeptic | Edge Case | Data integrity, private mode, import from existing tools |

---

## Feature Priority

| Feature | Priority | Notes |
|:---:|:---:|:---:|
| Setlist Logging | P0 — MVP | Core action. From memory + live now modes. |
| From Memory Tag | P0 — MVP | Design principle, not a warning. "We trust you." |
| Friends Feed | P0 — MVP | Social payoff. Unlocks after first show logged. |
| Star Ratings & Notes | P0 — MVP | 5-star + free text. Displayed on feed card. |
| Personal Archive | P0 — MVP | Tab 1. Full history sortable by artist/year/venue/rating. |
| Rare Song Badge | P1 | Auto-flag. Threshold TBD — not appeared in last 20 setlists. |
| Show Photo Upload | P0 — MVP | Optional user photo per show log. Thumbnail in show card bottom-right. Fallback hierarchy: 1) user's own photo → 2) community top-voted photo for that artist → 3) empty state. |
| Contacts Import | P0 — MVP | Import phone contacts (+ optional Spotify followers) to find friends already on Aftershow. Available in onboarding and Settings. Permission prompt copy must be framed carefully — "find friends" not "access your contacts". Apple/Google privacy review sensitive. |
| Artist Page — Community Photo Voting | P1 | Top 3 concert photos per artist, community-upvoted. Surfaced on Artist Page. Top photo also serves as card thumbnail fallback for users without their own. Creates a virtuous loop — contributors improve the experience for everyone. |
| Artist Pages | P1 | Setlist history, fan stats, upcoming tours. |
| Tour Dates | P1 | Bandsintown/Songkick API. |
| Stats & Milestones | P2 | "You've seen this artist 8 times." Profile flex layer. |
| AI Logging Assist | v1.1 | Fuzzy input → Setlist.fm API match. Post-MVP. |
| Import History | v1.1 | For Dana. Concert Archives migration path. |

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

## Workflow Rules

1. Maintain this README as a living document — update at every major milestone.
2. Do not proceed to a new phase without announcing the transition, updating this log, and confirming readiness.
3. Phase gates are hard stops. No skipping.

---

## Integrations

- **Figma** — UI design & component specs
- **GitHub** — repo, prototype code, version history

---

*AFTERSHOW · Concept Stage · May 2026 · The show never really ends.*
