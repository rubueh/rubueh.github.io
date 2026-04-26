# rubueh.github.io

The marketing site for **SaniBrau Labs**, an engineering team building
automated Clean-in-Place (CIP) systems for small craft breweries.

Live at **[sanibrau.com](https://sanibrau.com)**.

## Stage

Pre-pilot. The first SaniBrau Station prototype is in active build as a
senior mechanical-engineering capstone at New Mexico State University,
completing late spring 2026. Pilot validation runs with New Mexico
breweries through summer 2026. The site reflects that — every claim is
tagged Built, Targeted, or Vision, and the public site states only the
first two.

## Stack

Plain static HTML and CSS. No build step, no framework, no dependencies.
Hosted on GitHub Pages directly from `main`. The choice was deliberate:
the team is small, the timeline is short, and the site is mostly content
with a sticky-anchor nav and two contact forms — none of which needs a
framework. If interactivity grows past what plain JS can handle, the
upgrade path is Vite + GitHub Actions.

```
.
├── index.html          # the entire homepage
├── css/styles.css      # design tokens + component styles (one file)
├── images/
│   ├── branding/       # puffin logo variants
│   ├── photography/    # brewery photos used in section frames
│   └── team/           # founder and advisor headshots
└── CNAME               # custom domain pointer
```

## Local preview

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000`. No install step, no rebuild on save —
just refresh.

When you change CSS, bump the cache-bust query on the stylesheet link in
`index.html` (`css/styles.css?v=N`) so returning visitors pull a fresh
copy instead of fighting their browser cache.

## Design tokens and brand

All visual styling derives from the **SaniBrau Design System v1** —
forest / amber / cream palette, Inter and JetBrains Mono, alternating
forest → bone → cream section rhythm. Tokens live at the top of
`css/styles.css` as `--sb-*` CSS custom properties. Reference tokens,
not raw hex.

The brand guide lives outside this repo. The component styles in
`css/styles.css` are the deployed expression of §8 (application notes)
and §10 (audience filtering) of the v1 brand document.

## Forms

Two forms — the partner brewery inquiry and the "stay in the loop"
updates signup — submit via `fetch` to
[formsubmit.co](https://formsubmit.co) using a hashed endpoint that
keeps the destination email out of page source. Both forms share one
endpoint, both feed the founders' inbox, and both include a honeypot
field plus formsubmit's spam filtering. No backend, no database, no
monthly cost.

If a form ever stops delivering, the likeliest cause is formsubmit
needing reactivation after long inactivity. A single test submission
re-triggers the activation email.

## License

No license declared. The puffin mark, brand name, photography, and copy
are SaniBrau Labs property and not for reuse without permission. The
HTML and CSS scaffolding is small and unremarkable — borrow patterns if
useful, but please don't lift the brand.
