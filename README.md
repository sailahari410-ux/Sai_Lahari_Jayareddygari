# NO VANILLA.

**No bland ideas. No forgettable brands.**

Portfolio of **Sai Lahari Jayareddygari**: Brand Strategy · Creative Direction · Growth.

This is a single-page site with a case study for each of the four brands I've worked with:

| Brand | What it is | Highlights |
|---|---|---|
| **Coffee Kathà** | South Indian filter coffee café chain in Hyderabad | 5 → 12 outlets, a 100k+ view pre-launch reel, the Sunday Kathà series |
| **Mind 360** | Online therapy app for millennials and Gen Z | Brand and product direction ahead of a pan-India launch |
| **TéSoul Blends** | Ayurvedic-inspired premium wellness teas | Revenue before launch, ~12,000 cups served, the Adika partnership |
| **Open Minds Child Vista** | Child development and therapy centre | +40% clients, strategy delivered in 1 week instead of 4 |

---

## Project structure

```
.
├── index.html        # the whole site: markup, styles and script in one file
├── img/              # screenshots used in the case studies
│   ├── ck-grid.jpg       # Coffee Kathà Instagram grid
│   ├── m360-site.jpg     # Mind 360 website hero
│   ├── m360-grid.jpg     # Mind 360 Instagram grid
│   ├── ts-hero.jpg       # TéSoul website hero
│   ├── ts-products.jpg   # TéSoul product section
│   ├── ts-grid.jpg       # TéSoul Instagram grid
│   └── om-grid.jpg       # Open Minds Instagram grid
└── README.md
```

There are no frameworks, no build step and no dependencies. The only external request is the Google Fonts stylesheet for Fraunces and Inter.

## Run it locally

Open `index.html` in a browser. If you'd rather use a local server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy on GitHub Pages

1. Push this folder to a GitHub repository.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, then select `main` and `/ (root)`.
4. Save. The site goes live at `https://<username>.github.io/<repo-name>/` within a minute or two.

> To use a custom domain, add it under **Settings → Pages → Custom domain** and point your domain's DNS to GitHub.

The site also works on Netlify, Vercel or Cloudflare Pages. Drag the folder in, or connect the repo, and no build settings are needed.

## Editing the content

Everything lives in `index.html`. Search for these to find each part:

| To change… | Look for |
|---|---|
| Name, title, tagline, intro | `<header class="hero"` |
| The four brand cards under the intro | `class="flavours"` |
| Headline stats (5 → 12, 100k+, etc.) | `class="stats"` |
| "How I keep it un-vanilla" pillars | `class="approach"` |
| A brand's case study | `id="coffee-katha"`, `id="mind-360"`, `id="tesoul"`, `id="open-minds"` |
| Vanilla vs No Vanilla comparison | `class="vs"` |
| Featured reels / "Extra shots" dropdown | `class="reels"` / `details class="more"` |
| Closing section | `class="closing"` |

**Adding a reel:** copy any `<a class="reel" …>` block, change the Instagram link in `href` and update the text. Put it inside the `reel-grid` you want, either the featured one or the one in the dropdown.

**Swapping an image:** drop the new file into `img/` and update the `src` and `data-full` attributes on its `<div class="shot">`. Images around 1600px wide, saved as JPG, keep the page fast.

**Brand colours** are CSS variables at the top of the `<style>` block:

```css
--ck: #1f5a4a;   /* Coffee Kathà green */
--m3: #6a55a6;   /* Mind 360 purple   */
--ts: #3f948f;   /* TéSoul teal       */
--om: #e2583e;   /* Open Minds coral (also the dot in NO VANILLA.) */
```

## Credits

Brand names, logos and screenshots belong to their respective brands and appear here only as proof of work.

© 2026 Sai Lahari Jayareddygari
