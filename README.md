# Mintlify Clone

A practice project that replicates the [Mintlify](https://www.mintlify.com) landing page. Built with plain HTML and CSS.

### Check it on https://mintlify-landing-clone.vercel.app/

---

## Fonts

| Font | Usage | Source |
|------|--------|--------|
| **Inter** | Primary UI font (body, buttons, nav, paragraphs) | `assets/fonts/InterVariable-s.p.494bb210.ttf` (variable, TrueType). Fallback: Arial with size-adjust. |
| **Geist Mono** | Labels, tags, and accent text (e.g. “LLMS.TXT & MCP”, “AGENT”, section labels) | Multiple `.woff2` files in `media/` and `assets/fonts/` (variable weight 100–900). Fallback: Arial with metrics override. |

Fonts are declared in `styles/root.css` via `@font-face` and referenced with CSS variables: `--font-inter` and `--font-geist-mono`.

---

## Colors

All colors are defined as CSS custom properties in `styles/root.css` using the **LAB** color space.

| Variable | Purpose |
|----------|---------|
| `--color-background-main` | Page background (dark) |
| `--color-text-main` | Primary text (white) |
| `--color-text-soft` | Secondary/muted text (white at 70% opacity) |
| `--color-muted` | Muted text (e.g. footer copyright, nav headings) |
| `--color-brand` | Brand accent (mint/green) — CTAs, links, labels |
| `--color-brand-light` | Lighter brand tint (e.g. “New” badge) |
| `--color-background-soft` | Soft surfaces (cards, footer, inputs) |
| `--color-border-sub` | Subtle borders |
| `--color-border-surface` | Section dividers, card borders |
| `--color-border-soft` | Stronger borders (inputs, pills) |

---

## Page Sections (from `index.html`)

The landing page is structured as a single-page application with the following sections:

| Section | ID/Class | Contents |
|---------|----------|----------|
| **Header** | `<header class="header">` | Fixed navigation bar with brand logo, nav items (Resources, Documentation, Customers, Blog, Pricing), and action buttons ("Contact sales", "Start for free") |
| **Hero Section** | `#hero-section` | Blog CTA badge ("New: Self-updating docs with agent suggestions"), main heading ("The Intelligent Knowledge Platform"), description, email signup form, and hero image |
| **Trusted Companies** | `#trusted-companies` | Grid of 8 company logos: Anthropic, Coinbase, Microsoft, Perplexity, HubSpot, X, PayPal, Lovable |
| **Feature Highlights** | `#feature-highlight` | Section heading ("Built for the intelligence age"), description, and 3 feature cards: "LLMS.TXT & MCP" (Built for both people and AI), "AGENT" (Self-updating knowledge management), and "ASSISTANT" (Intelligent assistance for your users) |
| **Enterprise Features** | `#enterprise-features` | Enterprise label, heading ("Bring intelligence to enterprise knowledge"), description, "Explore for enterprise" button, two feature items (Build with partnership, Compliance and access control), enterprise image, and company logos |
| **Customer Stories** | `#customer-stories` | Section label ("customers"), heading ("Unlock knowledge for any industry"), description, horizontal scrollable cards (7 customer stories: Perplexity, X, Kalshi/Lovable, Cognition/Microsoft, Together AI/Coinbase, Laravel/Anthropic, Glean/PayPal), and navigation arrows |
| **Documentation Preview** | `#documentation-preview` | Heading ("Make documentation your winning advantage"), description, CTA buttons ("Get started for free", "Get a demo"), and two quick links ("Pricing on your terms", "Start building") |
| **Footer** | `<footer>` | Brand logo, social links (LinkedIn, X/Twitter, GitHub), 5-column navigation (Explore, Resources, Documentation, Company, Legal), security badge, system status indicator, copyright, and theme selector (System, Light, Dark) |

---

## File structure & what each file includes

### HTML

| File | Contents |
|------|----------|
| **`index.html`** | Single-page structure: header, hero, trusted companies, feature highlight, enterprise, customer stories, documentation preview, footer. Links all CSS and references assets. |

### CSS

| File | Contents |
|------|----------|
| **`styles/root.css`** | `:root` color and font variables; `@font-face` for Inter and Geist Mono (and fallbacks); global reset (`*`, `body`, `ul`, `ol`, `a`, form controls). |
| **`styles/common.css`** | Layout (`.container`, `.flex`, `.grid`); typography classes (`.text`, `.text-lg`, `.text-sm`, `.text-x-sm`, `.text-geist-mono`, `.heading`, `.heading-md`, `.heading-sm`, `.section-desc`, `.text-brand`); buttons (`.button-primary`, `.button-secondary`, `.outline-button`). |
| **`styles/header.css`** | Fixed header layout, nav items, header buttons, responsive gaps. |
| **`styles/main-sections.css`** | Hero (background, form, CTA); trusted companies grid; feature highlight cards; enterprise section; customer story cards and carousel; documentation preview and “Get started”/“Get a demo” blocks. |
| **`styles/footer.css`** | Footer layout, link columns, nav link headings, copyright bar, theme selector, security badge. |


### Assests

| File | Contents |
|------|----------|
| **`assets/fonts/`** | Geist Mono `.woff2`; Inter variable `.ttf`. |
| **`assets/images/`** | PNGs: featured cards, enterprise image, security badge. |
| **`assets/svg/`** | Logos (brand, companies), icons (arrows, book, enterprise, theme, social). |

---

## Quick start

Clone the repository, open `index.html` in a browser (no build step).

## Screenshot

![Screenshot](/assets/screen-capture.jpg)
