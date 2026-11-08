---
name: enterprise-orchestrator
description: >
  Autonomous enterprise software orchestrator based on Paperclip AI principles. 
  Takes a simple user prompt (e.g. "Build an e-commerce website for a shoe shop"), 
  autonomously conducts live web research on trending designs and legal/security compliance 
  (OWASP Top 10, DPDP Act 2023, GDPR), synthesizes an entrepreneur-grade master specification, 
  deploys specialized domain subagents (UI/UX, Frontend, Backend, Security, QA), executes 
  via Prompt Loop Engineering, and runs a 6-round Red Team / Blue Team security audit & patch loop.
---

# Enterprise Autonomous Orchestrator

The Enterprise Autonomous Orchestrator converts a **simple, brief user prompt** into an **entrepreneur-grade, secure, compliant, fully-implemented production application**.

It is modeled after [Paperclip AI](https://github.com/paperclipai/paperclip)'s control plane and org chart dynamics, fortified with **Prompt Loop Engineering** and an **Iterative Red Team / Blue Team Security Hardening Loop** so that no vulnerability or partial output remains.

---

## The 6-Stage Orchestration Lifecycle

```
[ Simple User Prompt ]
          │
          ▼
┌──────────────────────────────────────────────────────────┐
│ STAGE 1: Autonomous Web Research & Intelligence         │
│  • Market & Design Trends (Color palettes, UX patterns)  │
│  • Security & Privacy Laws (OWASP Top 10, DPDP, GDPR)    │
└──────────────────────────────────────────────────────────┘
          │
          ▼
┌──────────────────────────────────────────────────────────┐
│ STAGE 2: Master Prompt & Enterprise Spec Synthesis       │
│  • Brand identity & Design Tokens                        │
│  • Full Feature & API Contracts                          │
│  • Strict Definition-of-Done (DoD) & Acceptance Matrix   │
└──────────────────────────────────────────────────────────┘
          │
          ▼
┌──────────────────────────────────────────────────────────┐
│ STAGE 3: Specialized Domain Subagent Fleet               │
│  1. 🎨 UI/UX Designer Subagent                           │
│  2. 💻 Frontend Engineer Subagent                        │
│  3. ⚙️ Backend & DB Subagent                             │
│  4. 🛡️ Security & Compliance Subagent                    │
│  5. 🧪 QA & Pentest Subagent                             │
└──────────────────────────────────────────────────────────┘
          │
          ▼
┌──────────────────────────────────────────────────────────┐
│ STAGE 4: Prompt Loop Engineering (Zero Partial Output)   │
│  • Implement -> Automated Test -> Diagnose -> Fix Loop   │
│  • Anti-placeholder rejection (No // TODO or stubs)     │
│  • Continuous iteration until 100% tests pass cleanly    │
└──────────────────────────────────────────────────────────┘
          │
          ▼
┌──────────────────────────────────────────────────────────┐
│ STAGE 5: Red Team / Blue Team Security Hardening Loop    │
│  • Red Team audits codebase & generates vuln report      │
│  • Blue Team patches weaknesses & verifies regressions   │
│  • Iterates up to 6 rounds until 0 vulnerabilities exist │
└──────────────────────────────────────────────────────────┘
          │
          ▼
┌──────────────────────────────────────────────────────────┐
│ STAGE 6: Board Presentation & Deliverables               │
│  • Verified diffs, live previews, and audit reports      │
└──────────────────────────────────────────────────────────┘
```

---

## Stage 1: Autonomous Web Research & Intelligence

When the user enters a simple prompt:
1. **Never ask the user to elaborate upfront.** Instead, execute automated web research using available search tools (`search_web`).
2. **Track A — Market & UX Trends:**
   * Query trending leaders in the domain (e.g. for shoes: Nike, Allbirds, Goat, StockX, On-Running).
   * Identify current modern aesthetics: minimalist luxury, bold streetwear, micro-interactions, responsive grids, magnetic cursors, fluid sticky carts.
   * Extract trending color schemes (monochrome foundations with bold fluorescent or earthy accent palettes) and typography pairings.
   * Catalog high-converting features: multi-angle galleries, dynamic faceted filters, quick-view drawers, size recommendation guides.
   * Follow `workflows/prompt-expander.md`.
3. **Track B — Security & Legal Regulations:**
   * **OWASP Top 10 Checklist:** Input sanitization, parameterized queries, CSRF tokens, strict CSP/CORS headers, rate limiting, and password hashing (bcrypt/argon2).
   * **Data Privacy Laws:**
     * **DPDP Act (India - Digital Personal Data Protection Act 2023):** Explicit consent notice, purpose specification, right to grievance redressal, right to erasure/correction, child data restrictions.
     * **GDPR & CCPA:** Granular cookie consent banners, Do-Not-Sell toggles, privacy policy, and data portability endpoints.
   * Follow `workflows/compliance-checker.md`.

---

## Stage 2: Master Prompt Synthesis

Synthesize the findings into an **Entrepreneur-Grade Master Specification** following `templates/master-prompt.template.md`. 

The master specification must define:
1. **Mission & Value Proposition:** Market positioning, target audience, conversion goals.
2. **Design Tokens & UI System:** Exact hex palettes, typography hierarchy, border radiuses, dark/light mode tokens.
3. **Architecture & Tech Stack:** Framework (e.g., Next.js / Vite + React + Express), database schema, caching, state management.
4. **Security & Legal Compliance Matrices:** Explicit OWASP controls and DPDP/GDPR consent flows.
5. **Acceptance Matrix (Definition-of-Done):** Exact files to create, commands to verify, and non-negotiable test criteria.

---

## Stage 3: Specialized Domain Subagent Fleet

Partition work across 5 specialized subagents. Each subagent operates on a 3-step internal protocol:
1. **Refine Domain Prompt:** Takes its section of the master specification and enriches it into an actionable technical brief.
2. **Formulate Implementation Plan:** Drafts file-by-file changes, dependencies, and test commands.
3. **Execute & Self-Verify:** Implements code using the Prompt Loop Engineering engine.

| Subagent Role | Template | Model | Scope |
| :--- | :--- | :--- | :--- |
| **🎨 UI/UX Designer** | `templates/subagent-ui.md` | `inherit` / `pro` | Color tokens, typography, component styling, animations. |
| **💻 Frontend Engineer** | `templates/subagent-frontend.md` | `flash` / `inherit` | React/Next components, responsive layouts, cart/filter state. |
| **⚙️ Backend & DB Engineer** | `templates/subagent-backend.md` | `flash` / `inherit` | REST/GraphQL APIs, DB models, authentication, checkout logic. |
| **🛡️ Security & Compliance** | `templates/subagent-security.md` | `inherit` / `pro` | OWASP Top 10 hardening, DPDP/GDPR consent flows, audit logs. |
| **🧪 QA & Pentester** | `templates/subagent-qa.md` | `inherit` / `flash` | Test suites, vulnerability audits, accessibility checks. |

---

## Stage 4: Prompt Loop Engineering (Zero Partial Output)

Follow `workflows/prompt-loop-controller.md`.

### Core Rules of the Prompt Loop:
1. **No Partial Output Allowed:**
   * Outputs containing `// TODO`, `/* Add implementation here */`, or placeholder comments are strictly rejected.
   * Every component, handler, and route must be fully coded.
2. **Automated Verification Harness:**
   * Every change must immediately trigger verification:
     * Compile/Typecheck: `tsc --noEmit` or equivalent.
     * Unit & Component Tests: `pnpm test`.
     * Linting & Formatting: `pnpm lint`.
3. **The Verify-Diagnose-Fix Loop:**
   * If any command fails (exit code != 0), the failure log and stack trace are formatted into a diagnostic prompt.
   * The subagent receives the diagnostic prompt and must fix the source code (never weaken test assertions).
   * The loop repeats until all checks return `exit code 0`.

---

## Stage 5: Red Team / Blue Team Security Hardening Loop

Follow `workflows/security-audit-remediation-loop.md`.

After initial implementation passes all functional tests, the codebase enters a dedicated **Red/Blue Team Security Loop**:
1. **Red Team (Security Auditor Subagent):**
   * Employs `templates/subagent-red-team.md`.
   * Probes for IDOR, injection vectors, CSRF weaknesses, missing rate limits, leaky logs, and DPDP/GDPR non-compliance.
   * Emits a comprehensive **Vulnerability Audit Report** with CWEs, severity, and exact file/line numbers.
2. **Blue Team (Remediation Engineer Subagent):**
   * Employs `templates/subagent-blue-team.md`.
   * Patches identified vulnerabilities in source files with defensive middleware, sanitizers, and authorization checks.
   * Re-verifies application tests to ensure zero functional regression.
3. **6-Round Convergence Loop:**
   * This audit-remediation cycle runs up to **6 consecutive rounds**.
   * It terminates early as soon as the Red Team certifies **zero vulnerabilities (0 Critical, 0 High, 0 Medium, 0 Low)**.

---

## Stage 6: Board Presentation & Deliverables

1. Produce an inspectable artifact summarizing:
   * Research findings and trending design choices.
   * Architecture overview and security compliance checklist.
   * 6-Round Security Audit & Remediation Log with certified clean sign-off.
   * Completed file map and verified test logs.
2. Present the working application and diffs to the user ("The Board") for review and sign-off.
