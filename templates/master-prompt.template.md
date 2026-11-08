# Entrepreneur-Grade Master Specification & Prompt Template

This template is filled by the Orchestrator after analyzing the user's simple prompt and completing live web research on design trends and security/legal compliance.

---

## 1. Project Identity & Value Proposition
* **Project Name:** `[Generated Brand Name, e.g. Velos Kicks / Apex Footwear]`
* **Original Prompt:** `"[Simple prompt from user]"`
* **Domain & Positioning:** `[e.g. Modern D2C athletic and lifestyle footwear]`
* **Target Audience:** `[e.g. Urban runners, sneaker enthusiasts, trend-focused buyers]`
* **Conversion & UX Goals:** `[e.g. Under 3 clicks to checkout, mobile-first performance, accessible]`

---

## 2. Market & Visual Design System
* **Design Philosophy:** `[e.g. High-performance minimalism with brutalist accents]`
* **Color System:**
  * Background: `[Hex code, Light & Dark]`
  * Surface & Card: `[Hex code]`
  * Primary Accent / CTA: `[Hex code]`
  * Border & Subtle lines: `[Hex code]`
  * Text (Primary, Muted): `[Hex codes]`
* **Typography Hierarchy:**
  * Display / Headings: `[e.g. Space Grotesk / Inter Bold]`
  * Body / UI text: `[e.g. Inter / System Sans]`
* **Component Styling & Animations:**
  * Card radius: `[e.g. rounded-2xl]`
  * Micro-interactions: `[e.g. smooth zoom on hover, slide-over cart drawer]`

---

## 3. Comprehensive Feature Scope
* **Public Pages:**
  * Home / Landing with dynamic hero banner, featured releases, category grid.
  * Product Catalog with multi-attribute filtering (size, category, color, price).
  * Product Detail Page (PDP) with high-res gallery, size selector, size guide modal, stock indicator.
* **Cart & Commerce:**
  * Flyout Mini-Cart drawer with instant quantity modification and tax/shipping estimator.
  * Checkout Flow with multi-step validation (Shipping -> Payment Mock -> Order Review).
  * Order Confirmation with live order tracking simulation.
* **Customer Account & Privacy:**
  * User profile & order history.
  * DPDP/GDPR Data Privacy Center: consent preferences, data download, account deletion request.

---

## 4. Security & Compliance Matrix
* **OWASP Top 10 Guardrails:**
  * Helmet security headers (strict CSP, X-Frame-Options, HSTS).
  * Rate limiter on `/api/auth` and `/api/checkout`.
  * Input schema validation (Zod) on all API payload boundaries.
  * Parameterized DB access.
* **Legal Compliance (DPDP Act 2023 & GDPR):**
  * Granular cookie consent banner with refusal/settings toggles.
  * Notice of data collection with explicit purpose declaration.
  * Functional `/api/privacy/export` and `/api/privacy/erasure` routes.
  * Grievance officer contact in footer.

---

## 5. Domain Delegation Map
* **🎨 UI/UX Subagent:** Creates `design-tokens.ts`, Tailwind theme configuration, and SVG icon sets.
* **💻 Frontend Subagent:** Builds React/Next components, state hooks (`useCart`, `useFilter`), and responsive views.
* **⚙️ Backend Subagent:** Implements database models, REST APIs, mock payment processing, and auth middleware.
* **🛡️ Security Subagent:** Hardens headers, configures rate limiting, implements consent manager and privacy endpoints.
* **🧪 QA Subagent:** Authors and runs unit tests, E2E user journeys, and accessibility audits.

---

## 6. Non-Negotiable Acceptance Matrix (Definition-of-Done)
* [ ] Zero placeholder comments (`// TODO`, stubs, unhandled exceptions).
* [ ] All TypeScript types pass `tsc --noEmit` without errors.
* [ ] Unit and component test suites achieve 100% pass rate.
* [ ] Clean security audit (`npm audit` zero critical/high vulnerabilities).
* [ ] Verified on mobile (375px), tablet (768px), and desktop (1440px) breakpoints.
