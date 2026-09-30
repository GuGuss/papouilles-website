# papouilles-website

The landing page of Papouilles, a macOS app that prepares the French crypto tax declaration on the
user's computer. "Papouilles" is a working name.

## Files

| File | Content |
| --- | --- |
| `index.html` | The page. Self-contained: styles and scripts inline. |
| `feed.xml` | The Atom feed for release news. |
| `logo.svg` | The working logo. |

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
- Choose the host and the domain.

## Preview

```bash
python3 -m http.server 4321 --bind 127.0.0.1
```
