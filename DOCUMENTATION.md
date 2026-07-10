# CP Intelligence — Product Documentation

> **Xanadu × XOS · CP Intelligence** — a channel-partner (CP) discovery, scoring and
> shortlisting platform for real-estate launches. Powered by **Sudha Solutions (SS)**.
> This build is an **interactive front-end prototype** (no backend); all data is
> illustrative.

- **Live app:** https://anjalijha2.github.io/cp-intelligence/
- **Hosted docs:** https://anjalijha2.github.io/cp-intelligence/documentation.html
- **Login:** click **Sign in →** (no credentials — auth is stubbed for the demo).

---

## Table of contents
1. [What it does](#1-what-it-does)
2. [User guide — screen by screen](#2-user-guide--screen-by-screen)
3. [Feature changelog](#3-feature-changelog)
4. [Technical reference](#4-technical-reference)
5. [Run locally & share](#5-run-locally--share)
6. [Deployment](#6-deployment)
7. [Known limitations](#7-known-limitations)

---

## 1. What it does

CP Intelligence turns the 15–20 day manual hunt for channel partners into a **ranked,
scored shortlist on day one**. For each **launch** (a project a developer is selling),
a Sales Manager can:

- **Match** verified CPs against the launch criteria (location, configuration, price
  band, developer type) and see them **scored 0–100** with an explainable breakdown.
- **Triage** them on a Proven × Fit **quadrant**.
- **Study the micro-market** — nearby competing projects, real transacted prices, and
  where matched CPs already sell — on a live map.
- **Shortlist** partners into custom categories and **track each** from *New →
  Contacted → Meeting → Proposal → Tie-up Done*, ending with a **Final Launch Partners**
  list.

Everything is organised **per launch**, and there is a **CP Directory** for browsing the
full partner database.

---

## 2. User guide — screen by screen

Sidebar navigation (left): **Dashboard · Launches · CP Directory · Launch Match ·
Micro-Market · Shortlist**. The sidebar footer shows the **current launch** and a quick
"N in shortlist" link.

### Login
Product intro + **Sign in →**. No real authentication — clicking sign-in enters the app.

### Dashboard
Landing view with data-health KPIs (verified %, RERA/PAN/GST coverage, recent
refreshes) — a snapshot of how current and trustworthy the CP database is.

### Launches
Launch management for the whole portfolio.
- **List** with status pills: **Active / Draft / Completed / Inactive**, a summary strip
  (counts), and **filter chips** (All/Active/Draft/Completed/Inactive).
- Each row shows a **shortlist badge** — `📌 N shortlisted · 🤝 M finalized`. **Click the
  badge to open that launch's Shortlist board.**
- Per-row actions by status: **Micro-Market**, **Activate** (draft), **Complete /
  Archive** (active), **Reopen** (completed/inactive).
- **+ New Launch** opens a slide-in drawer:
  - **Search address** — a free, keyless **autocomplete** (OpenStreetMap/Photon). Start
    typing; pick a suggestion and it **auto-fills Street, Country, State, District and
    PIN** (all remain editable).
  - Plus BHK configuration, price band, developer tier, status, total units, notes.
  - **Create launch** adds it and jumps to Launch Match for that launch.

### Launch Match
The core scoring workspace. Left = **Match criteria**, right = results.
- **Criteria:** all-India **State → District → City** cascade (36 states/UTs), **PIN**
  chips, **BHK** chips, **price band** sliders, **Verified-only** toggle, and **Advanced
  filters** = **6 weight sliders** (Geography, Configuration, Price-band, Developer-type,
  Recency, Compliance). Moving a slider **re-scores and re-ranks every CP live**.
- **Summary widget:** Matches · Shortlisted · Contacted · Meetings · Finalised for the
  current launch (click it to open the Shortlist board).
- **Tab · Matching Channel Partners:** CPs **grouped into the 4 quadrant categories**
  (Proven + Fit, Proven · low fit, Test & Validate, Unproven · low fit) with counts,
  each row showing the score, a **WHY?** explainer, a **Verified** badge, and actions
  **Call / Email / Tie up / Shortlist**. Long groups collapse behind **"+N more"**,
  which opens a multi-select **bulk** popup.
- **Tab · Quadrant View:** the same filtered CPs plotted on a 2×2 **Proven × Fit** grid,
  with an **Approach-first** side list. The two tabs always show the **same set** of CPs.

### CP Directory
Browse the entire partner database.
- **Search** (firm name / XR code), **quadrant filter**, **pagination**.
- Per-row quick actions: **Call / Email / View Profile**.
- **Corrections** tracking — data changes logged with a **Source** (System vs User);
  editing a field in a profile adds a User-sourced correction here.

### Profile 360
Full CP dossier (opens from any list/row): **score ring + breakdown**, **compliance &
documentation** (RERA/PAN/GST), **performance** (avg VDNB, units sold), **market
coverage**, **project/track record**, **developers worked with**, **tied launches**, and
**quick actions** (call/email/add-to-shortlist/assign).

### Micro-Market
The competitive terrain around the current launch, on a live **Leaflet + OpenStreetMap**
map.
- **Tower markers** coloured by project category (Premium/Mid/Affordable/Luxury/
  Completed); the launch is a larger purple tower.
- The launch's **label sits to the right of its marker and auto-flips** to the left near
  the map edge so it's never clipped.
- **Nearby competitor projects** side panel — name, developer, distance, category,
  configuration, price range, status. **Two-way linked**: click a card to centre + open
  its map marker; click a marker to highlight its card.
- KPI bar, **asking-vs-transacted** price chart, and a **competitor-CP map** (which of
  your matched CPs already sell nearby, incl. leak risk).

### Shortlist board  ★
An Amazon-wishlist-style workspace, **per launch**.
- **Custom categories** — create, rename, delete, reorder (⚙ **Manage categories**);
  each shows its CP count. Defaults: High / Medium / Low Priority.
- **Add to Shortlist popup** — appears on every "+ Shortlist" (list, profile, bulk). It
  has a **multi-select launch dropdown** (add **one CP to several launches at once** —
  current launch pre-selected) and a category picker; **+ Create new category** adds and
  files the CP in one step. The chosen category name is applied to **every** selected
  launch (created where missing).
- **Progress tracking** — each CP card has a **status dropdown** (New · Contacted ·
  Meeting Scheduled · Meeting Done · Proposal Shared · Negotiation · Tie-up Done ·
  Rejected) and **one-tap quick actions** (Contacted / Meeting / Proposal / **Tie-up
  Done** / **Move to…** / Remove) — no need to open the profile.
- **Filters** — status chips (with counts) + Verified-only, Category, City, Assigned
  user, and Sort (Last updated / Fit score).
- **Final Launch Partners** — CPs marked **Tie-up Done** collect automatically into a
  highlighted section with a total ("the officially selected partners").
- **Timeline** — every CP keeps a dated **activity log** (Added → Contacted → Meeting →
  Tie-up), expandable on the card.
- **Summary widget** — Total Matches · Shortlisted · Contacted · Meetings · Tie-up Done ·
  Final Selected.

---

## 3. Feature changelog

Shipped incrementally (most recent last); commit short-SHAs on `main`:

| Area | What | Commit |
|---|---|---|
| Micro-Market | Nearby competitor projects side panel (two-way map ↔ card) | `ec85300` |
| Location | All-India `geoTree` — 36 states/UTs, 662 districts, ~15.5k cities | `29ebce6`, `fd6bf92` |
| Micro-Market | Tower/building markers (category-coloured) instead of dots | `e94ae06` |
| Micro-Market | Launch label anchored right of marker, auto-flips near edges | `47082d5` |
| QA | Stale title, KPI mismatch, empty-location auto-seed (`ensureCitySeed`) | `bda92a5` |
| Launch Match | Quadrant View reads the **same filtered set** as the list | `342811f` |
| New Launch | Free keyless **address autocomplete** + Country/State/District | `f334435` |
| Shortlist | Full **Shortlisting board** (categories, statuses, quick actions, timeline, final partners, filters, listing badges, summary) | `1ee37bd` |
| Shortlist | Add popup **multi-launch selector** (one CP → many launches) | `08fa5b2` |

Earlier work (pre-panel) also delivered: cascading geo search, launch-management drawer
+ statuses, CP Directory (search/filter/pagination/corrections), tabbed Launch Match with
grouped categories + dynamic score sliders, bulk shortlist, verified-partner badges, and
the professional login redesign.

---

## 4. Technical reference

### Architecture
- The entire app is one file — **`CP Intelligence.dc.html`** — authored in the **Claude
  Design** runtime.
- **`support.js`** is the client runtime: it self-loads **React 18 + Babel** and fonts
  from CDN (unpkg / Google Fonts) and calls **`fetch(location.href)`** to read its own
  markup — so the file **must be served over HTTP** (opening via `file://` won't
  hydrate) and needs internet on first paint.
- Templating: `<sc-if value="{{x}}">`, `<sc-for list="{{arr}}" as="item">`,
  `{{bindings}}`; a `class extends DCLogic` holds `state`, methods, and a **`renderVals()`**
  that returns every binding. **`ScoreRing.dc.html`** is an imported sub-component.

### Data model (in-memory, seeded)
- **`cpData`** — the CP records. Extended by **`buildCitySeeds()`** (3 CPs for each of 13
  seeded cities) and **`ensureCitySeed()`** (generates 3 generic CPs on demand for any
  selected location that has none, so Launch Match is never empty).
- **`geoTree`** — `{ state: { district: { city: [pins…] } } }`, **36 states/UTs · 662
  districts · ~15,500 cities** with real PIN codes (derived from the GeoNames India
  postal dataset). Drives both the Launch Match filter and the New Launch drawer.
- **`launches`** — ~12 launches `{ id, name, city, config, price, dev, status, created,
  matches, address, pins, lat/lng }`.
- **Shortlist store** — `sl[launchId] = { cats:[{id,name}], items:{ [xr]: { cat, status,
  assigned, added, log:[{d,t}] } } }`. `SL_STATUS` defines the 8 statuses; helpers
  `slFor/slAddToCat/slSetStatus/slMoveItem/slCounts/ensureCatByName`.
- **Scoring** — base `weights[6]`, user-tunable `scoreWeights[6]`; **`dynScore(cp)`**
  recomputes a CP's score from its `got[]` sub-scores and the current weights;
  `makeBreakdown()` powers the profile bars. **`verifiedSet`** is the predefined list of
  verified XR codes (green badge).

### External services (all keyless / free)
| Use | Service |
|---|---|
| Map tiles | OpenStreetMap raster tiles (Leaflet) |
| Geocoding (launch → lat/lng) | Nominatim |
| Address autocomplete (New Launch) | Photon (komoot) |

No API keys, no billing — chosen deliberately because the site is public. These are
best-effort public endpoints (light rate limits); if unreachable, fields stay manual.

### Repository / file map
- **`project/`** — working copy: `CP Intelligence.dc.html` (the app), `support.js`,
  `ScoreRing.dc.html`.
- **`site/`** — the **deployed** GitHub repo: the app at the repo root **and** a byte-
  identical **`docs/`** mirror, plus `.nojekyll`. Six HTML copies are kept in **md5
  parity** on every change (`project/index.html`, `site/index.html`, `site/docs/…`, etc.).
- **`server.js`**, **`package.json`**, **`share.js`** — local runner + sharing.

---

## 5. Run locally & share

```bash
npm start          # serves ./project on http://localhost:5173 (binds 0.0.0.0)
```
Open the printed **Local** URL. Change port: `PORT=8080 npm start`
(PowerShell: `$env:PORT=8080; npm start`).

**Share on the same wifi:** `npm start` also prints a **LAN** URL (`http://<ip>:5173`).

**Public link (remote demo):**
```bash
npm run share      # starts the server + a Cloudflare quick-tunnel, prints an https URL
# or, separately:
npm run tunnel     # localtunnel on :5173
```

> Needs internet — React/Babel/fonts, map tiles and geocoders all load from the network.

---

## 6. Deployment

- Hosted on **GitHub Pages**, repo **`Anjalijha2/cp-intelligence`**, branch `main`.
- Pages serves the **repo root**; a **`docs/`** mirror is kept identical so either Pages
  source setting works. **`.nojekyll`** disables Jekyll (the file is `{{…}}`-heavy).
- Publishing uses the **"pages build and deployment"** GitHub Action.

**Ops notes / gotchas**
- After editing the app, **sync all 6 HTML copies** and confirm **md5 parity = 1** before
  committing.
- A Pages build can occasionally be **cancelled** (runner/concurrency) — it then serves
  the previous build. Fix: **push again** (an empty commit works) to re-trigger.
- Pages throttles to **~10 builds/hour**; batching changes avoids queueing.
- Verify a deploy landed via the Actions API (status `completed` / conclusion `success`)
  before assuming the live site updated; then hard-refresh (**Ctrl+Shift+R**).

---

## 7. Known limitations

This is a **front-end prototype** for demos, not a production system:
- **No backend / persistence** — all state is in memory and **resets on reload**
  (shortlists, statuses, created launches, categories).
- **No real authentication** — Sign-in is a stub.
- **Illustrative data** — CP records, prices, RERA/PAN/GST and scores are fabricated.
- Detail screens (Micro-Market visuals, some KPIs) are tuned around the **Borivali West**
  demo launch; other launches reuse the demo terrain.
- CPs are seeded for known cities; other locations get **generic auto-seeded** CPs so no
  view is empty.
- Geocoding/autocomplete use **free public endpoints** with no uptime guarantee.

---

*Generated as living documentation for the CP Intelligence prototype. Update alongside
new change requests.*
