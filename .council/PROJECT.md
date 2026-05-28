# Hoffman Soft Water
B2B commercial water treatment landing page for Greater Cincinnati — generates leads from property managers, hospitality operators, and industrial facilities.

**Stack:** HTML · CSS · Vanilla JS (single file — no build tools, no framework)
**Hosting:** Vercel — pushes to `main` auto-deploy
**Fonts:** Google Fonts CDN — Lexend (headings) + Source Sans 3 (body)
**DB:** None — static site
**Integrations:** None live yet — contact form unconnected; analytics TBD
**Future:** Planned migration to WordPress (timing TBD)

**Structure:**
- `index.html` — entire site: HTML structure + all CSS + all JS inline
- `assets/` — logo and images
- `BRAND_STRATEGY.md` — brand positioning, color palette, copy, section map

**Shared modules / reuse hotspots:**
- `:root` CSS variables in `index.html` — all colors/fonts; always use these, never hardcode values
- `BRAND_STRATEGY.md` — source of truth for copy, colors, and section purpose before changing anything

**Conventions:**
- All styles and scripts stay inline in `index.html` — no separate `.css` or `.js` files
- CSS custom properties (`:root`) for all color and typography tokens
- Vanilla JS only — no libraries or frameworks
- Semantic HTML5 + ARIA attributes for accessibility (`aria-expanded`, `aria-label`, etc.)
- Placeholder content is marked with HTML comments — search `<!-- REPLACE` before launch
- Mobile-first responsive — CSS Grid + Flexbox, single breakpoint at 768px

**Context files:** `BRAND_STRATEGY.md` for copy/brand decisions; `README.md` for deploy notes
