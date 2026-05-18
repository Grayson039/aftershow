# Aftershow — Session Handoff
**Date:** May 18, 2026 | **Phase:** 3 — UI Design & Asset Creation | **Screens:** 13 of 14 done

---

## Immediately pick up here

Next screen to build: **Artist Page** (`aftershow-phase3-artist-page.html`)

This is screen 14 of 14 — the final MVP screen. Use **Dance Gavin Dance** as the artist (Sako's band). Will wants to review this one together. Build it, then the prototype shell is the next major milestone.

---

## Artist Page — Design Notes

- **Hero:** Artist name (Playfair Display Italic, big) + genre tags + Aftershow stats (logs, fans, avg rating)
- **Community Photos:** 3 top-voted fan photos in a row (P1 feature — design the component even though it's P1, load-bearing for card fallback in feed). Use placeholder gradients.
- **Setlist History:** Recent shows — list of show cards (venue, date, fan log count, avg rating). Taps to Show Page.
- **Fan Stats:** "X Aftershow fans have seen them" — breakdown by times seen (1x, 2x, 3x+)
- **Follow Artist button** — toggles to Following state
- **Top Songs:** ranked by frequency across all fan logs on Aftershow

---

## Screens Status

| File | Screen | Status |
|---|---|---|
| `aftershow-phase3-log-a-show.html` | Log a Show | ✅ Done |
| `aftershow-phase3-my-shows.html` | My Shows / Archive | ✅ Done |
| `aftershow-phase3-show-detail.html` | Show Detail | ✅ Done |
| `aftershow-phase3-friends-feed.html` | Friends Feed (interactive tabs) | ✅ Done |
| `aftershow-phase3-profile.html` | User Profile | ✅ Done |
| `aftershow-phase3-global-feed.html` | Global Feed | ✅ Done |
| `aftershow-phase3-tonight-feed.html` | Tonight Feed | ✅ Done |
| `aftershow-phase3-search.html` | Search / Discover | ✅ Done |
| `aftershow-phase3-show-page.html` | Show Page | ✅ Done |
| `aftershow-phase3-followers.html` | Followers / Following | ✅ Done |
| `aftershow-phase3-stats.html` | Stats Dashboard | ✅ Done |
| `aftershow-phase3-settings.html` | Settings | ✅ Done |
| `aftershow-phase3-onboarding.html` | Onboarding | ✅ Done |
| `aftershow-phase3-artist-page.html` | **Artist Page** | 🔲 NEXT |

---

## After Artist Page: Interactive Prototype Shell

Chain all 14 screens into a single end-to-end prototype:
- Single `aftershow-prototype.html` file
- One phone frame (not side-by-side)
- Dark/light toggle button
- JS router showing/hiding screens with CSS transitions
- Nav items clickable between screens
- Feed cards tap to Show Detail
- Log button opens Log a Show
- Onboarding first, then archive/profile

The Friends Feed tab switching (JS + data-tab pattern) is the exact foundation.

---

## Design System Quick Reference

**Shared fonts:** Playfair Display Italic 700 / Crimson Pro Italic 400 / DM Mono 400-500 / Syne 800

**Dark (Marshall):** bg `#0C0C0C` · cards `#111111` · gold `#D4A853` · tolex grain texture on `.phone.dark`

**Light (Orange):** bg `#EDE6D3` · cards `#F7F2E6` · ink `#1A1209` · gold `#D4A853` · rust `#C4401C` · diamond weave on `.phone.light`

Theme names: **Marshall Dark** / **Orange Vintage**

---

## Real Users in the Mockups

| Username | Real Person | Avatar | Bands |
|---|---|---|---|
| Grayson039 | Will (the user) | G initial | NIN, TBQ, Gojira, Tool, Deftones |
| Mimsie | Michelle (wife) | surprised-pikachu.gif | Paramore, BTS, K-Pop |
| xSasquatchx | Bryant (brother-in-law) | foxhound.jpg | Mastodon, Gojira, Baroness, DEP |
| Sako H. | Sako (iOS dev, critical reviewer) | sako.jpg | Dance Gavin Dance |

---

## Key Decisions Already Made (don't re-litigate)

- Archive-first — My Shows is Tab 1, not Feed
- From Memory = feature, not warning
- No internal tab bar on Profile (one scroll)
- Photo fallback: user photo → community top-voted → empty
- Contacts import P0 + CSV/spreadsheet import P1
- Phase 4 target: SwiftUI (Sako is iOS dev — React Native deprioritized)
- Marshall/Orange amp texture baked into both themes
- Theme names: "Marshall Dark" / "Orange Vintage"
- Concert Archives teardown done
- Onboarding: theme picker → contacts import → first show log (confirmed)
- 1-show minimum to unlock Feed

---

## Pending / Open Questions

- Sako's profile photo in profile screen (currently "G" placeholder for Grayson)
- After prototype shell: test with Sako and Mimsie before Phase 4?

---

*AFTERSHOW · Handoff · May 18, 2026*
