# slay docs

Source for the slay documentation site, built with [Mintlify](https://mintlify.com).

Live at **https://www.slaycamera.com/docs**. The website proxies `/docs` to Mintlify
(see `next.config.ts` in the website repo), so don't add Mintlify's DNS records:
its CNAME would take over the whole domain.

- `docs.json`: site config (theme, colours, navigation, links)
- `index.mdx`: the LUTs overview
- `luts/`: download and apply-in-code pages
- `logo/`: navbar logo (light and dark), copied from the website's app icon and wordmark
- `favicon.png`: the website's `public/icon-512.png`

## Preview locally

```bash
npm i -g mint
mint dev
```

The site runs at `http://localhost:3000`.

## Publishing

Pushes to `main` deploy through the Mintlify GitHub app. Check links before pushing:

```bash
mint broken-links
```

## Code samples

Every sample in `luts/apply-in-code.mdx` was run against the LUTs in
[slaycamera/luts](https://github.com/slaycamera/luts) and agreed with ffmpeg's
`lut3d` filter to within 1 level out of 255. If you change a sample, run it again
before you publish.
