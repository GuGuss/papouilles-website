# papouilles-website

The landing page of Papouilles, a macOS app that prepares the French crypto tax declaration on the
user's computer. "Papouilles" is a working name.

## Files

Only `public/` is published.

| File | Content |
| --- | --- |
| `public/index.html` | The page. Self-contained: styles and scripts inline. |
| `public/feed.xml` | The Atom feed for release news. |
| `public/logo.svg` | The working logo. |
| `public/_headers` | HTTP headers: security policy, no referrer, and `noindex` until the launch. |

`drafts/` holds local design explorations. Git ignores it.

## Rules

The page practises what the product promises:

- No cookie, no tracker, no third-party font, script or request. The Content-Security-Policy in
  `index.html` enforces it.
- No personal data collected: no sign-up form, no email.
- Every claim about competitors or incidents is dated and has a source, and names no company.

The brand and the market analysis live in the app repository: `docs/brand.md` and
`docs/market/competitors.md`.

## Before the public launch

- A lawyer reviews the comparative claims and the legal notice.
- Set `SIMPLEX_LINK` and check `RELEASE_DATE` in the script of `index.html`.
- Remove the `noindex` from `public/_headers` and from the `robots` meta tag in `public/index.html`.
- Choose the domain.

## Preview

```bash
python3 -m http.server 4321 --bind 127.0.0.1 --directory public
```

## Deployment

Cloudflare Pages, free plan, connected to this repository:

- Each push to `main` deploys the production site.
- Each pull request gets its own preview URL, posted on the pull request.

Settings: no framework, no build command, output directory `public`.
