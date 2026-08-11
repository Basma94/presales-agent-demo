# Design Export — for Figma import

Static, self-contained snapshots of the app's key screens, generated from the live app so they match pixel-for-pixel. Use these to import the design into Figma (e.g. with the **html.to.design** plugin, or similar).

## Files

- `01-dashboard.html` — Dashboard
- `02-opportunities.html` — Opportunities list
- `03-opportunity-profile.html` — Opportunity detail, Profile tab
- `04-opportunity-documents.html` — Opportunity detail, Documents tab
- `05-tender.html` — Tender page
- `06-customers.html` — Customers list
- `shared.css` — the full design system stylesheet (colors, type, components) used by every page above

## How to import into Figma

**Option A — from these files (recommended for the pages listed above):**
1. Install a Figma plugin such as [html.to.design](https://www.figma.com/community/plugin/1159123024924461424/html-to-design).
2. In Figma, run the plugin and choose "Import from local file," then select one of the `.html` files above (they're self-contained — CSS and fonts load automatically).
3. Each import lands as its own Figma frame; repeat per page.

**Option B — from the live app (needed for the Summary tab):**
The Opportunity **Summary** tab (Assessment Pack + CHAMP/MEDDPICC/Requirements/Solution accordion) wasn't exported as a static file — it's too large and deeply nested to hand-transcribe reliably. For that page, use the plugin's "capture current tab" / browser-extension mode directly against the live app:
`https://basma94.github.io/presales-agent-demo/` → open an opportunity → Summary tab.

## Design tokens

All colors, fonts (Space Grotesk for headings, Inter for body) and spacing are CSS custom properties at the top of `shared.css` under `:root`. Import that file into Figma variables/styles if you want the design tokens rather than the pixel layouts.

Note: the Opportunity Overview / Assessment Pack section (inside the Summary tab) intentionally uses a *different* palette (Poppins/DM Sans, its own reds/teals) — it's pinned to a separate reference design and isn't part of `shared.css`.
