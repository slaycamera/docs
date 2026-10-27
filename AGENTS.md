# Documentation project instructions

## About this project

- Docs for slay, the composition-guide camera for iPhone, built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter; configuration lives in `docs.json`
- The LUT files themselves live in [slaycamera/luts](https://github.com/slaycamera/luts); link to their raw URLs rather than copying them here

## Terminology

- The product is "slay", always lowercase, including at the start of a sentence
- "Slay Pro" is the paid tier, capitalised
- Call the files "LUTs" or ".cube LUTs", and the looks by name: slay Amber, slay Fade, slay Neon, slay Film, slay Portrait

## Style preferences

- Use active voice and second person ("you")
- Keep sentences short, one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

## Hosting

- The site is served at https://www.slaycamera.com/docs through a rewrite in the website's `next.config.ts`; never add Mintlify's DNS records
- `sitemap.xml` is hand-written because Mintlify's generated one uses the mintlify.dev host. When you add a page, add its URL there too

## Code samples

- Run every code sample before publishing it, and keep the published text identical to what you ran
- Samples must agree with ffmpeg's `lut3d` filter on the same decoded pixels
- Links to slaycamera.com carry `utm_source=docs`
