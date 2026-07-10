# CP Intelligence

Xanadu × XOS **CP Intelligence** — a channel-partner discovery, scoring and
**shortlisting** platform for real-estate launches. Powered by **Sudha Solutions (SS)**.
Interactive front-end **prototype** (no backend; illustrative data).

- **Live app:** https://anjalijha2.github.io/cp-intelligence/
- **Documentation (hosted):** https://anjalijha2.github.io/cp-intelligence/documentation.html
- **Documentation (Markdown):** [DOCUMENTATION.md](DOCUMENTATION.md)
- **Login:** click **Sign in →** (no credentials — auth is stubbed for the demo).

## What's inside

Launch management · all-India location search (36 states/UTs) · scored CP matching with
live weight sliders · Proven × Fit quadrant · CP Directory · Micro-Market map (nearby
projects, real prices) · and a full **Shortlisting board** (custom categories, per-CP
status tracking, quick actions, timeline, Final Launch Partners). See
[DOCUMENTATION.md](DOCUMENTATION.md) for the screen-by-screen guide and technical details.

## Run locally

```bash
npm start          # serves the app on http://localhost:5173
```

Open the printed **Local** URL. Needs internet (React/Babel/fonts + map/geocoder CDNs).
Change port: `PORT=8080 npm start`.

## Share

```bash
npm run share      # local server + Cloudflare quick-tunnel → public https URL
```

`npm start` also prints a **LAN** URL for same-wifi sharing.

## Deploy

GitHub Pages serves this repo (`main`, root + identical `docs/` mirror, `.nojekyll`) via
the "pages build and deployment" Action. Keep the 6 HTML copies in md5 parity and confirm
the Action succeeds before assuming the live site updated. Details in
[DOCUMENTATION.md](DOCUMENTATION.md#6--deployment).
