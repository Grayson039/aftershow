# Aftershow — Session Handoff
**Date:** May 17, 2026 | **Phase:** 3 — UI Design & Asset Creation | **Screens:** 5 of 14 done

---

## Immediately pick up here

Next screen to build: **Global Feed** (`aftershow-phase3-global-feed.html`)

The Friends Feed already has Global and Tonight tab content stubbed in as interactive panes. The next step is building those as full standalone screens that match the same fidelity as the Friends Feed — then wiring everything into a single prototype shell.

---

## Screens Remaining (9 of 14)

| Priority | Screen | Notes |
|---|---|---|
| 1 | Global Feed | Strangers' logs, geo tags. Content already stubbed in friends-feed tabs. |
| 2 | Tonight Feed | Live-logging cards, pulsing LIVE badge. Also stubbed in friends-feed tabs. |
| 3 | Search / Discover | Artist search, user search, venue search |
| 4 | Artist Page | Setlist history, fan stats, community photo voting (P1) |
| 5 | Show Page | Aggregated setlist from all fan logs, ratings, photos |
| 6 | Followers / Following | Social graph screen |
| 7 | Stats Dashboard | Tab 1 overflow — milestones, streaks, year charts |
| 8 | Settings | Dark/light toggle, notifications, contacts import, account |
| 9 | Onboarding | Theme picker with live preview, contacts import prompt, 1-show minimum |

---

## The Big Next Task: Interactive Prototype Shell

User wants to chain all 14 screens into a single end-to-end prototype. Architecture:
- Single `aftershow-prototype.html` file
- One phone frame (not side-by-side)
- Dark/light toggle button
- JS router that shows/hides screens with CSS transitions
- Nav items are clickable and navigate between screens
- Feed cards tap to Show Detail
- Log button opens Log a Show

The Friends Feed tab switching (JS + data-tab pattern) is the exact foundation for this. Same approach scales to full navigation.

---

## Files

| File | Screen |
|---|---|
| `aftershow-phase3-log-a-show.html` | Log a Show |
| `aftershow-phase3-my-shows.html` | My Shows / Archive |
| `aftershow-phase3-show-detail.html` | Show Detail |
| `aftershow-phase3-friends-feed.html` | Friends Feed (interactive tabs) |
| `aftershow-phase3-profile.html` | User Profile |

All committed to: https://github.com/Grayson039/aftershow

---

## Design System Quick Reference

**Shared fonts:** Playfair Display Italic 700 / Crimson Pro Italic 400 / DM Mono 400-500 / Syne 800

**Dark (Marshall):** bg `#0C0C0C` · cards `#111111` · gold `#D4A853` · field labels `#6B6B6B` · tolex grain texture on `.phone.dark`

**Light (Orange):** bg `#EDE6D3` · cards `#F7F2E6` · ink `#1A1209` · gold `#D4A853` · rust `#C4401C` · diamond weave texture on `.phone.light`

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
- Concert Archives teardown done — don't copy their "Next Concert as profile hero" mistake

---

## Pending / Open Questions

- Sako's profile photo needs to be embedded in the profile screen (currently just "G" initial for Grayson — does Will want his own photo there or keep the placeholder?)
- Bryant's username on things is often "Mastodon"-related — confirm xSasquatchx is the right handle for mockups
- Onboarding screen: confirm flow is theme picker → contacts import prompt → first show log

---

*AFTERSHOW · Handoff · May 17, 2026*
