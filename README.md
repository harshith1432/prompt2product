# Enterprise Autonomous Orchestrator

An autonomous AI agent orchestration skill modeled after [Paperclip AI](https://github.com/paperclipai/paperclip)'s control plane principles, fortified with **Prompt Loop Engineering** and an automated **6-Round Red Team / Blue Team Security Hardening Loop**.

---

## Overview

The Enterprise Autonomous Orchestrator enables an AI agent to convert a **simple, one-line user prompt** (e.g. *"Build an e-commerce website for a shoe shop"*) into an **entrepreneur-grade, secure, compliant, fully-implemented production application**.

It eliminates the common failure mode of AI assistants stopping at partial, half-baked code or asking users to write extensive engineering specifications.

---

## Key Capabilities

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

## Repository Structure

```
enterprise-orchestrator/
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

## Installation & Usage

### Global Antigravity Install
Copy this skill directory into your Antigravity skills path:
```bash
cp -r enterprise-orchestrator ~/.gemini/antigravity/skills/
```

### Usage
In your chat or agent prompt, simply supply any goal:
> *"Build an e-commerce website for a shoe shop"*

The orchestrator will automatically execute the research, synthesis, subagent delegation, prompt loop, and 6-round security audit.

---

## License

MIT License.
