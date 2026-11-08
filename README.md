# Prompt2Product 🚀

> **From a 1-Line Prompt to a Full Production App.**

An autonomous AI agent orchestration skill modeled after [Paperclip AI](https://github.com/paperclipai/paperclip)'s control plane principles, fortified with **Prompt Loop Engineering** and an automated **6-Round Red Team / Blue Team Security Hardening Loop**.

---

## 📖 About

### The Problem
Most AI coding assistants suffer from three critical flaws when given an idea:
1. **Premature Stopping & Stub Code:** They generate boilerplate, write `// TODO: Implement later`, and expect the human user to finish the difficult work.
2. **Disconnected from Market & Compliance Realities:** They guess visual styles and ignore modern data privacy regulations (e.g., India's **DPDP Act 2023**, Europe's **GDPR**) and security standards (**OWASP Top 10**).
3. **Overloaded Single-Agent Bottlenecks:** A single agent prompt attempts to design UI, write APIs, optimize queries, configure security headers, and test logic simultaneously—inevitably producing fragile, vulnerable software.

### The Solution: Prompt2Product
Inspired by **Paperclip AI's** corporate orchestration philosophy—where agents act like organized departments rather than scattered terminal tabs—**Prompt2Product** elevates software development from simple prompt-response to an autonomous digital enterprise:

* **From 1 Line to Enterprise-Grade:** You don't need a 5-page specification. Input a simple goal (e.g., *"Build an e-commerce website for a shoe shop"*), and the orchestrator autonomously executes live web research on top market players (Nike, StockX, Goat), identifies current design aesthetics, extracts trending color palettes, and models data structures.
* **Specialized Subagent Fleet:** Work is cleanly partitioned across 5 dedicated roles: UI/UX Designer, Frontend Engineer, Backend Engineer, Security & Compliance Officer, and QA Pentester.
* **Prompt Loop Engineering:** Built-in verification loops run compilers, unit tests, and security linters on every change. Code is automatically repaired until all tests pass with zero placeholders.
* **6-Round Red Team / Blue Team Security Hardening:** After initial build, a dedicated Red Team probes the application for vulnerabilities (IDOR, XSS, rate-limiting gaps, leaky logs). A Blue Team patches the source files, repeating for up to 6 rounds until a **Clean Security Certificate (0 Vulnerabilities)** is verified.

---

## ⚡ Key Capabilities

1. **Autonomous Web Research & Intelligence:**
   - Automatically searches the live web for industry benchmarks, trending UI/UX designs, modern color palettes, and high-converting features.
   - Extracts modern compliance and security standards: **OWASP Top 10**, India's **DPDP Act (Digital Personal Data Protection Act 2023)**, **GDPR**, and **CCPA**.

2. **Master Prompt & Architectural Synthesis:**
   - Expands the one-liner into an Entrepreneur-Grade Master Blueprint with complete design tokens, API contracts, data models, and non-negotiable Definition-of-Done (DoD) criteria.

3. **Specialized Domain Subagent Fleet:**
   - **UI/UX Designer**: Visual identity, palette tokens, responsive components, accessibility.
   - **Frontend Engineer**: React/Next.js UI, dynamic filters, cart drawer, checkout flow.
   - **Backend & Database Engineer**: REST APIs, database schema, cart & orders, simulated payment gateway.
   - **Security & Legal Compliance Officer**: OWASP Top 10 headers (Helmet, CSP, CORS), rate limiters, DPDP/GDPR consent manager, data erasure endpoints.
   - **QA & Pentest Inspector**: Automated test suites, vulnerability scans, accessibility checks.

4. **Prompt Loop Engineering (Zero Partial Output):**
   - Anti-placeholder enforcement: strictly rejects `// TODO`, skeleton code, or incomplete stubs.
   - Continuous automated verification: `pnpm test`, `tsc --noEmit`, linters.
   - Diagnostic repair loop: compiler/test errors are fed back into the agent to diagnose and fix root causes until 100% of checks pass with exit code 0.

5. **6-Round Red Team / Blue Team Security Hardening Loop:**
   - **Red Team (Security Auditor)**: Audits the codebase for IDOR, injection vectors, CSRF weaknesses, leaky logs, and compliance gaps. Emits a structured Vulnerability Audit Report.
   - **Blue Team (Remediation Engineer)**: Patches identified vulnerabilities in source files without functional regressions.
   - Repeats up to **6 consecutive rounds** until a **Clean Security Certificate (0 Vulnerabilities)** is achieved.

---

## 📂 Repository Structure

```
prompt2product/
├── SKILL.md                          # Main Skill Manifest & 6-stage lifecycle
├── workflows/
│   ├── prompt-expander.md            # Market & design trend research logic
│   ├── compliance-checker.md         # OWASP Top 10 & DPDP/GDPR compliance
│   ├── prompt-loop-controller.md     # Prompt Loop Engineering & anti-placeholder rules
│   └── security-audit-remediation-loop.md # 6-Round Red/Blue Team hardening loop
└── templates/
    ├── master-prompt.template.md     # Entrepreneur-grade master blueprint template
    ├── subagent-ui.md                # UI/UX Subagent protocol
    ├── subagent-frontend.md          # Frontend Subagent protocol
    ├── subagent-backend.md           # Backend Subagent protocol
    ├── subagent-security.md          # Security & Compliance Subagent protocol
    ├── subagent-qa.md                # QA Pentest Subagent protocol
    ├── subagent-red-team.md          # Red Team Auditor protocol
    └── subagent-blue-team.md         # Blue Team Remediation protocol
```

---

## 🚀 Installation & Usage

### Global Antigravity Install
Copy this skill directory into your Antigravity skills path:
```bash
cp -r prompt2product ~/.gemini/antigravity/skills/
```

### Usage
In your chat or agent prompt, simply supply any goal:
> *"Build an e-commerce website for a shoe shop"*

Prompt2Product will automatically execute the research, synthesis, subagent delegation, prompt loop, and 6-round security audit.

---

## 📜 License

MIT License.
