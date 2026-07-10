# AI Field Guide

A static, no-backend AI tools directory built to deploy free on GitHub Pages. This README is your complete deployment + SEO checklist — follow it in order.

## 1. Publish it on GitHub Pages (free)

1. Create a free GitHub account at github.com if you don't have one.
2. Create a new repository named exactly `ai-field-guide` (or rename it — just update step 4 if you do). Keep it **Public** (Pages needs public on the free tier).
3. Upload every file in this folder to that repository, keeping the folder structure exactly as-is (`index.html` and `tools.html` at the root, `assets/` and `blog/` as subfolders). Easiest way: on the repo page, click **Add file → Upload files**, then drag the whole folder contents in.
4. In the repo, go to **Settings → Pages**. Under "Build and deployment," set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
5. Wait 1–2 minutes, then your site is live at:
   `https://k45877815-dev.github.io/ai-field-guide/`

## 2. Replace the placeholder URL everywhere

Every file has `https://k45877815-dev.github.io/ai-field-guide/` in a few meta tags (canonical links, Open Graph tags) and in `sitemap.xml` / `robots.txt`. Find-and-replace `k45877815-dev` with your actual GitHub username in every `.html` file plus `sitemap.xml` and `robots.txt`. This matters — search engines use these tags, and wrong ones can quietly hurt indexing.

Also update the "Suggest a tool" link in `about.html` to point at your actual repo URL.

## 3. Tell Google the site exists

Free hosting doesn't hurt your ranking, but Google still has to find the site first:

1. Go to **Google Search Console** (search.google.com/search-console) and sign in with any Google account.
2. Add your site as a URL-prefix property: `https://k45877815-dev.github.io/ai-field-guide/`
3. Verify ownership (Search Console will offer an HTML file or meta-tag method — either works for a static site like this).
4. Once verified, go to **Sitemaps** in the left menu and submit: `sitemap.xml`
5. Give it a few days to a few weeks. New sites are not indexed instantly.

## 4. About your domain

You mentioned you have a domain in mind but can't buy it yet — that's fine, the site works perfectly on the free `github.io` subdomain in the meantime. One real trade-off to know: a free subdomain won't build the same domain authority a custom domain would over time, so treat this as a strong starting point, not the permanent home.

When you're ready to add the domain later:
1. Buy it from any registrar (Namecheap, Porkbun, Cloudflare Registrar are all reasonably cheap, ~$10–15/year).
2. Add a file named `CNAME` (no extension) at the repo root containing just your domain, e.g. `www.yourdomain.com`
3. At your registrar, point the domain's DNS at GitHub Pages (GitHub's Pages docs list the exact records — search "GitHub Pages custom domain DNS" when you're at that step).
4. Update every `k45877815-dev.github.io/ai-field-guide/` reference in the HTML/sitemap/robots files to your new domain instead.
5. Re-verify the new domain as a fresh property in Search Console and resubmit the sitemap.

## 5. Add more content (this is what actually moves rankings)

The technical setup gets you found; content is what gets you ranked. Two easy ways to extend this site:

**Add a tool to the directory** — copy one `<div class="specimen">…</div>` block in `tools.html` under the right family, fill in the name/description/link, and bump the `No. 0XX` numbers after it if you want the count to stay sequential (purely cosmetic — not required).

**Add a blog post** — copy `blog/how-to-choose-an-ai-writing-tool.html`, rename the file, write a new original article (comparisons, "how to" guides, and specific-use-case posts tend to perform best), and add a new `<a class="note-row">` entry at the top of `blog/index.html` and `index.html` pointing to it. Also add its URL to `sitemap.xml`.

Aim for genuinely original writing — Google's ranking systems have gotten better at deprioritizing thin, copied, or AI-generated-and-unedited content, and this niche has a lot of competition, so specific, first-hand detail is what will actually separate this site from the hundreds of other AI tool lists.

## File structure

```
/
├── index.html                 homepage
├── tools.html                 the directory (18 tools, 6 categories)
├── about.html
├── sitemap.xml
├── robots.txt
├── assets/
│   ├── style.css
│   └── script.js
└── blog/
    ├── index.html              blog listing
    └── how-to-choose-an-ai-writing-tool.html   sample post
```

No build step, no dependencies, no server — just static files. Anything that edits an `.html` file is editing the live page.
