# Kiwi Made — Kyuhee Jo's Personal Portfolio

## Owner

Kyuhee Jo (조규희) — Coder, Creator, Consultant.
Head of GTM @ Trillion Labs | ex-McKinsey, Google, Palantir, Lunit
JHU CS '23 (GPA 3.95), Minor in Entrepreneurship & Applied Math

- Email: kyuhee0622@gmail.com
- LinkedIn: https://www.linkedin.com/in/kyuheejo/
- GitHub: https://github.com/kyuheejo
- YouTube: https://www.youtube.com/channel/UCactbUmyH9dO1BYBBALk6Gw

## Brand Identity

**"Coder & Creator & Consultant"** — lives at the intersection of tech and business, solves problems with products. The portfolio should reflect someone who codes, ships products, advises enterprises, and creates content (AI videos).

Tone: confident but playful. Technical depth with approachable personality. The "Kiwi Made" brand uses a juice pouch / grocery store metaphor — nutrition labels for skills, aisles for project categories, receipts for blog posts.

## Tech Stack

- **Framework**: Astro (static site generator)
- **Styling**: Vanilla CSS with CSS custom properties (no Tailwind — the design system is too custom)
- **Fonts**: Google Fonts — `Titan One` (logo/headings), `Fredoka` (display text), `Inter` (body/data), `JetBrains Mono` (code/blog)
- **Blog**: Astro Content Collections with Markdown/MDX
- **Animations**: CSS animations (keyframes for float, squeeze, pulse effects). GSAP only if needed for scroll-triggered animations.
- **Deployment**: Vercel or Netlify (static)
- **No JS framework required** — pages are mostly static. Use Astro islands (React or Svelte) only for interactive components (e.g., project filters, search)

## Design System

### Color Palette (CSS Custom Properties)

```css
:root {
  --bg-color: #E87A35;      /* Orange background */
  --pouch-bg: #F4EBE1;      /* Cream / paper */
  --kiwi-main: #6CA632;     /* Primary green */
  --kiwi-light: #9BD94E;    /* Light green accent */
  --kiwi-dark: #4A7320;     /* Dark green */
  --seed-black: #2A1F1A;    /* Near-black for text/borders */
  --accent-yellow: #F2C12E; /* Yellow accent */
  --ink-red: #d32f2f;       /* Red for highlights/prices */
  --shelf-wood: #D29B62;    /* Wood tone for shelf UI */
  --shelf-shadow: #8B5E34;  /* Dark wood shadow */
}
```

### Font Variables

```css
:root {
  --font-logo: 'Titan One', cursive;
  --font-display: 'Fredoka', sans-serif;
  --font-data: 'Inter', sans-serif;
  --font-mono: 'JetBrains Mono', monospace;
}
```

### Core UI Patterns

1. **Pouch Card** — Rounded rectangle (`border-radius: 18-32px`) with cream background, subtle box-shadow, optional squeeze animation. Used as the primary container everywhere.
2. **Nutrition Label** — White box with thick black border (`3px solid`), bold header with thick underline, rows with `justify-content: space-between` and thin border-bottom. Used for skills, experience details, project tech stacks.
3. **Shelf Layout** — Horizontal display with "wood shelf" bottom bar. Used for project grid.
4. **Receipt / Deli Menu** — Monospace font, dotted borders, barcode decoration. Used for blog post listing.
5. **Floating SVG Decorations** — Organic blob shapes (kiwi cross-sections, leaves, abstract forms) floating in the background with CSS `float` animation at low opacity.
6. **Badges** — Small circles (`50px`) with bold text, slight rotation. Used for tech indicators.
7. **CTA Buttons** — Full-width, bold font, 3px border + offset box-shadow that reduces on hover for a "press" effect.

### Animation Patterns

- `squeeze`: scaleX oscillation on containers (loading state)
- `float`: translateY + slight rotate for background elements
- `pulse`: opacity oscillation for loading text
- `fillJuice`: width 0% → 100% for progress bars
- `moveBubbles`: background-position shift for bubble texture

## Site Structure

```
/                       → Loading splash → Hero section
/experience             → Horizontal-scroll timeline (career history)
/projects               → Grocery shelf grid of shipped products
/blog                   → Receipt/deli-menu style blog listing
/blog/[slug]            → Individual blog post (receipt detail view)
/videos                 → Video gallery (AI videos from YouTube)
```

## Page Specs

### 1. Loading Splash (`hero-section-loading.html`)
- Kiwi Made logo with squeeze animation
- Juice-fill progress bar (4s fill animation)
- "Freshly Squeezing Your Experience..." tagline with pulse
- Links to LinkedIn and GitHub (add to design)
- Auto-redirects to hero after animation completes

### 2. Hero Section (`hero-section.html`)
- Two-panel pouch layout (left: brand visual, right: nutrition label)
- Left panel: Kiwi Made logo blob with curved SVG text ("SOURCE OF CLEAN CODE" / "WHOLEGRAIN DESIGN"), flavor text, net weight gag
- Right panel: "Tech Stack Facts" nutrition label with actual skills:
  - Python 80%, JavaScript 70%, Java 60%, Go 60%
  - Figma 80%, Adobe Premiere 80%
  - React (frontend), Node/SQL (backend)
- INGREDIENTS list: actual tech + personality traits
- CTA button → contact or resume
- Floating kiwi/leaf SVGs in background
- Badges: "100% DEV", "VEGAN" (or repurpose to fit Kyuhee's brand)

### 3. Experience Timeline (`experience-timeline.html`)
- Horizontal scroll layout with "serving panel" cards connected by dashed lines
- Each card = one role, styled as nutrition label:
  - **Trillion Labs** — Founding GTM Lead (Nov 2025–Present)
  - **Palantir** — Deployment Strategist (Jun 2025–Nov 2025)
  - **McKinsey** — Business Analyst (Apr 2023–Mar 2025)
  - **Google** — SWE Intern (May 2022–Aug 2022)
  - **Lunit** — ML Intern (Dec 2021–Jan 2022)
  - **JHU** — BS Computer Science (2019–2023)
- "% Daily Contribution" rows = key achievements per role
- Back navigation link to hero
- Footer: "SCROLL HORIZONTALLY TO DISCOVER THE FULL HARVEST"

### 4. Projects Section (`projects-section.html`)
- Two layout variants available (shelf view and deli menu/receipt view)
- Default: Shelf view with pouch cards on wooden shelves
- Each project pouch includes: blob icon, flavor badge, project title, mini nutrition label (stack facts), "VIEW RECIPE" button, tech badge circle
- Price tags on shelf rails: "OPEN SOURCE FREE", "PRICED TO HIRE: $0.00"

### 5. Blog Section (`blog-post.html`)
- Deli menu / receipt board layout
- Left sidebar: "AISLE DIRECTORY" with category links
- Main area: receipt-style listing with blog post entries
- Each entry: post title (item-name), subtitle/flavor, tech tags (stack), stats (read time, date)
- Blog post detail: full receipt with header, content area, barcode footer
- Content managed via Astro Content Collections (`.md` or `.mdx` files in `src/content/blog/`)
- Categories can map to "aisles" in the grocery metaphor

### 6. Videos Section (NEW — no reference yet)
- Design in the Kiwi Made style — suggest: "FROZEN AISLE" or "BEVERAGE COOLER" metaphor
- Grid of video cards with YouTube thumbnail embeds
- Each card: video title, date, description, YouTube link
- Consider a "juice box" card design to match the pouch aesthetic
- Pull from YouTube channel: https://www.youtube.com/channel/UCactbUmyH9dO1BYBBALk6Gw

## Astro Project Structure

```
kiwi-codes/
├── CLAUDE.md
├── astro.config.mjs
├── package.json
├── tsconfig.json
├── public/
│   ├── fonts/
│   └── images/
│       └── kyuhee-profile.png
├── src/
│   ├── layouts/
│   │   └── BaseLayout.astro        # Shared head, fonts, global CSS vars
│   ├── components/
│   │   ├── LoadingSplash.astro      # Squeeze animation loader
│   │   ├── NutritionLabel.astro     # Reusable nutrition label component
│   │   ├── PouchCard.astro          # Reusable pouch container
│   │   ├── ShelfRow.astro           # Project shelf with wood bar
│   │   ├── TimelinePanel.astro      # Experience card for timeline
│   │   ├── BlogMenuItem.astro       # Receipt-style blog entry
│   │   ├── VideoCard.astro          # YouTube video embed card
│   │   ├── FloatingDecor.astro      # Background SVG blobs
│   │   └── Navigation.astro         # Site-wide nav
│   ├── pages/
│   │   ├── index.astro              # Loading → Hero
│   │   ├── experience.astro         # Timeline
│   │   ├── projects.astro           # Shelf grid
│   │   ├── blog/
│   │   │   ├── index.astro          # Blog listing (receipt board)
│   │   │   └── [...slug].astro      # Blog post detail
│   │   └── videos.astro             # Video gallery
│   ├── content/
│   │   ├── config.ts                # Content collection schemas
│   │   └── blog/                    # Markdown blog posts
│   │       └── first-post.md
│   └── styles/
│       └── global.css               # CSS custom properties, reset, shared styles
├── design-reference/                # Original HTML mockups (keep for reference)
│   ├── hero-section-loading.html
│   ├── hero-section.html
│   ├── experience-timeline.html
│   ├── projects-section.html
│   └── blog-post.html
└── kyuhee-info/                     # Source content (keep for reference)
    ├── kyuhee-jo-portfolio.md
    └── kyuhee-linkedin.md
```

## Content Data

### Career Timeline (ordered newest → oldest for horizontal scroll)

| Company | Role | Period | Location |
|---------|------|--------|----------|
| Trillion Labs | Founding GTM Lead | Nov 2025–Present | Korea |
| Palantir | Deployment Strategist | Jun–Nov 2025 | — |
| McKinsey & Company | Business Analyst | Apr 2023–Mar 2025 | SF / Seoul |
| Google | SWE Intern | May–Aug 2022 | Sunnyvale |
| Lunit | ML Intern | Dec 2021–Jan 2022 | Seoul |

### Education

| School | Degree | Period | GPA |
|--------|--------|--------|-----|
| Johns Hopkins University | BS Computer Science, Minor Entrepreneurship & Applied Math | 2019–2023 | 3.95 |
| Hankuk Academy of Foreign Studies | High School | 2016–2019 | — |

### Key Achievements

- AI x Product Hackathon 1st Place / 80 teams ($5,000) — 2023
- HopHacks 1st Place Overall / 45 teams — 2021
- JHU Business Plan Competition 3rd / 90 teams — 2022
- MICCAI Conference Paper — 2022
- Pistritto Research Fellowship ($4,000) — 2022
- EU Contest for Young Scientists 3rd / 140 competitors from 39 countries — 2018

### Skills (from Notion data)

| Skill | Level | Category | Use |
|-------|-------|----------|-----|
| Python | 80% | Language | ML development |
| JavaScript | 70% | Language | React, frontend |
| Java | 60% | Language | Backend |
| Go | 60% | Language | Backend |
| Figma | 80% | Tool | UI design |
| Adobe Premiere | 80% | Tool | Video editing |
| Excel | 90% | Tool | Data analysis, market modeling |
| Word | 90% | Tool | Planning documents |

### Social Links

- LinkedIn: https://www.linkedin.com/in/kyuheejo/
- GitHub: https://github.com/kyuheejo
- YouTube: https://www.youtube.com/channel/UCactbUmyH9dO1BYBBALk6Gw
- Email: kyuhee0622@gmail.com
- Phone: +82-10-5059-9469

## Development Guidelines

- **No frameworks for styling** — use vanilla CSS with custom properties to match the handcrafted design references
- **Preserve the metaphor** — every UI element should feel like it belongs in a juice pouch / grocery store. New sections should extend the metaphor (e.g., videos = "frozen aisle", about = "ingredients list")
- **Mobile responsiveness** — the references are desktop-first (960-1440px). Must add responsive breakpoints. Pouch cards should stack vertically on mobile. Timeline should scroll vertically on small screens.
- **Performance** — ship zero or minimal JS. Use Astro's static output. Lazy-load YouTube embeds.
- **SEO** — proper meta tags, Open Graph images, structured data for the blog
- **Accessibility** — semantic HTML, proper heading hierarchy, alt text, sufficient color contrast (seed-black on cream passes WCAG AA)
- **Blog writing** — posts are written in Markdown in `src/content/blog/`. Each post has frontmatter: title, date, description, tags, coverImage (optional)
- **Keep design-reference/ and kyuhee-info/ folders** — these are source-of-truth for design patterns and personal content. Do not delete.
