# Usability Report — egypt-vacation-plan.netlify.app

**Tested:** 2026-06-24  
**Coverage:** Full single-page application (desktop, 958 px wide)  
**Tester:** Claude Code browser automation

---

## What Works Well

| Area | Finding |
|---|---|
| **Hero section** | Strong visual impact — full-bleed pyramids photo, clear headline, descriptive tagline, and stat badges (3 Guides / 20 Day Trips / 5,000 Years of History) give instant orientation |
| **Sticky navbar** | Stays visible while scrolling; active link highlights gold when in that section (e.g. "DAY TRIPS" glows when scrolled there) |
| **Anchor navigation** | "LEAVING BAHRAIN" → `#bahrain`, "DAY TRIPS" → `#trips` both scroll accurately to the correct sections |
| **Dark / Light mode toggle** | Sun/moon icon toggles correctly; full theme swap with no flash or layout shift |
| **Filter tabs** | Historical / Nature / City / Score ≥ 8.5 filters all work — cards update instantly and correctly to the matching category |
| **Trip card design** | Numbered rankings, colour-coded gradients per category, score badges, drive time, and keyword tags (HIKING, WILDLIFE, etc.) make scanning easy |
| **Score Leaderboard** | Compact 3-column table at the bottom gives a quick-reference overview of all 20 trips |
| **Practical Tips block** | 6 well-organised tips with clear bold labels (Best season, Traffic, Tickets…) — highly useful at-a-glance info |
| **External links** | Guide cards link to relevant resources (LMRA Portal, Ministry of Labour, OpenSooq, Dubizzle, Wikipedia) — well sourced |
| **No console errors** | Zero JavaScript errors or warnings on page load |

---

## Issues & Recommendations

| Severity | Issue | Recommendation |
|---|---|---|
| **Medium** | **Filter state persists across nav clicks** — clicking "DAY TRIPS" while "Nature" is active keeps the Nature filter; a visitor would see only 6 of 20 trips instead of all 20 | Reset filter to "All (20)" whenever the `#trips` anchor is triggered via the nav |
| **Medium** | **Card thumbnails are emoji / icon placeholders** — all 20 trip cards use flat emoji icons instead of real photos | Add thumbnail photos (400 × 200 px, Wikimedia Commons) for better visual appeal and trust |
| **Low** | **No "Back to Top" button** — the page is long (hero → 2 guides → 20 trips → leaderboard → footer) with no shortcut to return to the top | Add a sticky "↑ Top" button that appears after scrolling past the hero |
| **Low** | **"Score ≥ 8.5" filter label** — the `≥` symbol may not be immediately clear to all users, especially on mobile | Label it "Top Rated" or "Score 8.5+" for broader clarity |
| **Low** | **Footer has no copyright year** | Add "© 2026" to the footer tagline |
| **Info** | **Mobile viewport not tested** — audit was at 958 px; recommend testing at 375 px (iPhone) and 768 px (iPad) to verify the two-column card grid collapses cleanly | Test with browser DevTools device emulation |

---

## Screenshots Captured

| # | Section | Key Observation |
|---|---|---|
| 1 | Hero section (dark mode) | Strong first impression |
| 2 | Guide cards — Leaving Bahrain | Clear step-by-step structure with numbered items |
| 3 | Day Trips section — All view | Numbered cards with colour-coded scores |
| 4 | Filter: Historical selected | Filter activates and highlights correctly |
| 5 | Filter: Nature selected | Cards update instantly to nature-only trips |
| 6 | Light mode — hero | Clean cream background, good contrast maintained |
| 7 | Light mode — guide cards | Legible text in both themes |
| 8 | Nav: LEAVING BAHRAIN clicked | Jumped to `#bahrain` correctly |
| 9 | Nav: DAY TRIPS clicked | Jumped to `#trips`; "DAY TRIPS" highlighted gold |
| 10 | Nature trip cards detail | Tags, Wikipedia links, and drive times visible |
| 11 | Score Leaderboard + Practical Tips | Excellent summary section at page bottom |
| 12 | Footer (zoomed) | Sources properly attributed |

**GIF walkthrough:** `egypt-vacation-usability-walkthrough.gif` — 23 frames, ~4.8 MB (downloaded to browser Downloads folder).

---

## Overall Verdict

The site is well-designed, content-rich, and functionally solid with zero runtime errors. The two medium-priority items worth fixing before wider sharing are:

1. **Reset the filter on nav click** — prevents users from seeing a truncated trip list unexpectedly.
2. **Add real trip photos** — emoji placeholders reduce visual trust for a travel guide.

Everything else is production-quality.
