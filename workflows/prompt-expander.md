# Workflow: Autonomous Market & Design Trend Intelligence

This workflow transforms a simple user prompt (e.g. *"Build an e-commerce website for a shoe shop"*) into an industry-leading, high-converting design and feature blueprint through autonomous web research.

---

## 1. Automated Research Execution

When the user prompt arrives, execute search queries using `search_web` along three distinct axes:

### Axis 1: Industry Benchmarking & Top Players
Query examples:
* `"top trending sneaker ecommerce websites 2026 UI UX"`
* `"award winning shoe shop web design Awwwards"`
* `"best luxury and streetwear ecommerce design patterns"`

Extract:
* **Layout Patterns:** Asymmetrical hero banners, sticky split-screen product detail pages (PDP), interactive drawer carts, floating bottom navigation on mobile.
* **Micro-Interactions:** Image hover zoom, magnetic CTA buttons, 3D/360-degree shoe viewer, smooth page transitions, dynamic badge tags (e.g., "Trending", "Limited Release").

### Axis 2: Color Theory & Visual Aesthetics
Query examples:
* `"trending color palettes ecommerce fashion shoes"`
* `"modern typography pairings ecommerce streetwear"`

Synthesize:
* **Primary Palette:** High-contrast neutral bases (e.g. Off-white `#F9F9FB`, Deep Obsidian `#111113`, Slate Gray `#64748B`).
* **Accent & Energy Tones:** Electric Amber (`#F59E0B`), Cyber Lime (`#84CC16`), or Crimson Red (`#EF4444`) for CTAs and inventory urgency.
* **Typography:** Bold geometric sans-serif for headings (e.g. Inter / Space Grotesk / Syne) paired with crisp readable body fonts.
* **Spatial Rhythm:** Generous whitespace, rounded-2xl cards, subtle border borders (`border-neutral-200/60`), glassmorphic overlays (`backdrop-blur-md`).

### Axis 3: High-Converting Feature Set
Identify and incorporate must-have e-commerce features:
* **Dynamic Catalog & Faceted Filters:** Filtering by size (US/UK/EU), category (Running, Casual, High-top), gender, price range, and color swatches.
* **Interactive Size Guide & Recommender:** Accordion modal with measurements and fit advisory.
* **Cart & Mini-Cart Drawer:** Real-time quantity updates, subtotal calculation, coupon code input, shipping progress bar.
* **Simulated Checkout Flow:** Multi-step wizard (Shipping -> Payment -> Order Review -> Confirmation with simulated order tracking).
* **Wishlist & Quick View:** Instant product preview modal without navigating away from the catalog.

---

## 2. Output Schema: Design Intelligence Brief

Compile findings into the Master Specification under the `## Design & Market Intelligence` section:

```markdown
### Visual Design Tokens
- Background: #0B0F17 (Dark) / #FAFAFA (Light)
- Surface: #161D2B (Dark) / #FFFFFF (Light)
- Accent / CTA: #FF5E36 (Electric Coral)
- Text Primary: #F1F5F9 / #0F172A
- Radius Scale: sm (4px), md (8px), lg (12px), xl (20px)

### Micro-Interactions & Styling Guidelines
- Cards: Hover translate-y-1 with subtle ambient drop-shadow.
- Image Gallering: Thumbnail carousel with cross-fade transition.
- Cart Drawer: Slide-over right drawer with backdrop blur.
- Responsive Behavior: 1-col mobile, 2-col tablet, 3-4 col desktop grid.
```
