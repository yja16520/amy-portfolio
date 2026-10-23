# Zimeng (Amy) Yan — Personal Portfolio & Academic Showcase

A modern, editorial website built with **Astro 5** and **Tailwind CSS**, designed specifically for **effortless long-term maintenance** and presentation quality.

---

## 🌟 Architecture & Design Upgrades

Unlike standard generic templates, this site was custom-designed around Amy's multifaceted journey:
1. **Editorial Narrative & Hero**: Replaced generic centered blocks with an asymmetrical, editorial layout highlighting her four pillars: **Clinical & AI Research**, **Visual Arts & Realism**, **Public Speaking (140+ Speeches)**, and **Competitive Dance & Baton Twirling**.
2. **Searchable & Filterable Speeches Archive (`/speeches`)**:
   - Organizes all **141 speeches** delivered between 2020 and 2025.
   - Includes an instant, real-time search bar (by topic, source, or forum) and year-by-year filtering.
   - Curated photographic strip from five years of speech presentations.
3. **Interactive Art Studio (`/art`)**:
   - Filterable gallery by medium (*Oil, Colored Pencils, Black & White Pencil*).
   - Accessible lightbox `<dialog>` modal showing full image, materials, year, and Amy's artist rationale.
   - Direct link support (e.g. `/art#distorted-sweetness`).
4. **Dance & Baton Twirling Showcase (`/dance`)**:
   - Highlights her National Championship, 7 State Championships, 25+ local titles, and 585-day practice streak.
   - Year-by-year performance chronicles (2017–2025) with full-resolution photo viewer.
5. **Clinical Research & Professional Track (`/experiences`)**:
   - Dual-track view separating **Leadership, Clinical & Research** (AI in Medicine, Pediatrician shadowing, First-Aid TikTok channel) from **Professional & Teaching** (Motorola Solutions engineering pitch 1st place, tutoring, barista).
6. **Blazing Fast Performance**:
   - Zero unnecessary JavaScript bloat; pure static HTML/CSS with lightweight vanilla interactivity.
   - Instant page loads and sub-2 second production build time.

---

## 🛠️ Effortless Maintenance Guide

All website data is completely separated from the UI into clean JSON files inside [`src/data/`](./src/data/):

| To update or add... | Edit this file | How to do it |
| :--- | :--- | :--- |
| **New Speech** (e.g. Speech #142) | [`src/data/speeches.json`](./src/data/speeches.json) | Add a 4-line object: `{"id": "speech142", "date": "2026-XX-XX", "topic": "...", "source": "...", "forum": "..."}` |
| **New Artwork** | [`src/data/artworks.json`](./src/data/artworks.json) | Drop the image into `public/Amy_drawings_pics/` and add the entry with `title`, `year`, `type`, and `description`. |
| **New Dance Event / Season** | [`src/data/dance_events.json`](./src/data/dance_events.json) | Add year, cover image, and event details. |
| **New Leadership / Research** | [`src/data/volunteering.json`](./src/data/volunteering.json) | Add organization, role, grade period, and bullet points. |
| **New Work / Internship** | [`src/data/work.json`](./src/data/work.json) | Add organization, role, period, and description points. |
| **Bio, Headline or Social Links** | [`src/data/profile.json`](./src/data/profile.json) | Update bio, stats, or external links. |

---

## 🚀 Development & Deployment

### Run locally:
```bash
npm install
npm run dev
```
Open [http://localhost:4321](http://localhost:4321) in your browser.

### Build for Production:
```bash
npm run build
```
The static site output is generated in `./dist/`, ready to deploy to **Vercel**, **Cloudflare Pages**, **GitHub Pages**, or **Netlify** with zero configuration required.
