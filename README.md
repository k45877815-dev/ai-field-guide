# AI Field Guide

A static, no-backend AI tools site, now expanded to 10 pages, deployed free on GitHub Pages at:
`https://k45877815-dev.github.io/ai-field-guide/`

## What's new in this version

- **`compare.html`** — ChatGPT vs Claude vs Gemini, compared honestly with a comparison table and FAQ
- **`free-tools.html`** — which tools have a genuinely usable free tier vs a limited trial
- **`glossary.html`** — plain-English definitions of terms like token, hallucination, RAG, context window
- **`blog/best-ai-tools-for-freelancers.html`** — new original post
- **`blog/common-ai-tool-mistakes.html`** — new original post
- Every existing page got its navigation updated to link to all of the above, plus your real domain replacing the old `YOUR-USERNAME` placeholder — no more find-and-replace needed on this batch.

## How to re-upload

Since your repo already has files with these names (`index.html`, `tools.html`, `about.html`, `sitemap.xml`, `robots.txt`, and the `blog/` folder), GitHub will ask if you want to replace them when you upload — say yes. The new files (`compare.html`, `free-tools.html`, `glossary.html`, and the two new blog posts) will just be added.

1. Go to your repo → **Add file → Upload files**
2. Drag in every file from this folder again, including the `assets` and `blog` folders
3. When prompted about existing files, confirm you want to overwrite them
4. Commit the changes
5. Give GitHub Pages 1–2 minutes to rebuild, then check `https://k45877815-dev.github.io/ai-field-guide/`

**Important:** your `index.html` has a `google-site-verification` meta tag you added for Search Console — it's already preserved in this version, so you won't lose your verification.

## Submit the new pages to Google

Since `sitemap.xml` now lists all 10 pages, go back into **Google Search Console → Sitemaps** and resubmit `sitemap.xml` (or it'll pick up the new URLs automatically on its next crawl). You can also use **URL Inspection → Request Indexing** on `compare.html`, `free-tools.html`, and `glossary.html` individually to speed up their discovery, since these are new URLs Google hasn't seen before.

## Full file structure (10 content pages)

```
/
├── index.html                                  1. homepage
├── tools.html                                  2. full directory (18 tools, 6 families)
├── compare.html                                3. ChatGPT vs Claude vs Gemini
├── free-tools.html                             4. free tools guide
├── glossary.html                               5. AI terms glossary
├── about.html                                  6. about / methodology
├── blog/
│   ├── index.html                              7. blog listing
│   ├── how-to-choose-an-ai-writing-tool.html    8. post
│   ├── common-ai-tool-mistakes.html            9. post
│   └── best-ai-tools-for-freelancers.html      10. post
├── sitemap.xml
├── robots.txt
└── assets/
    ├── style.css
    └── script.js
```

## Keeping content accurate over time

A few things in this version are written to age well rather than go stale:
- The comparison page avoids hard numbers (pricing, specific limits) that change often, and says so explicitly — update it if any assistant's core positioning changes significantly.
- The free-tools page includes a callout warning that free tiers shift without notice — re-check each tool's actual pricing page every few months and adjust if something's no longer accurate.
- The glossary covers stable, foundational terms unlikely to need frequent updates.

If you keep adding original blog posts every couple of weeks, that's the single biggest lever for actual ranking growth from here — the technical/structural side of the site is now fully built out.
