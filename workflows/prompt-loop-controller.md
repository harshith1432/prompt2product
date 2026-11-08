# Workflow: Prompt Loop Engineering (Never Stop on Partial Output)

This workflow defines the execution engine that guarantees agents **never stop with a partial, untested, or incomplete implementation**.

---

## 1. The Core Law of Prompt Loop Engineering

> **"A task is NOT complete until all acceptance criteria are written, automated test suites execute, and exit code 0 is proven with zero placeholders."**

### Forbidden Behaviors (Immediate Rejection)
If a subagent output contains any of the following, the orchestrator immediately rejects the turn and prompts for completion:
* `// TODO: Implement later`
* `/* Add your code here */`
* Stubs or mock functions that throw `"Not implemented"`
* Halting with text like *"I created the frontend, now you can wire up the backend."*
* Proposing a change without running verification tests.

---

## 2. The 4-Step Verification Cycle

```mermaid
flowchart TD
    Assign["1. Task Dispatched with Acceptance Matrix"] --> Code["2. Subagent Implements Full Code"]
    Code --> ScanPlaceholders{"Check for // TODO or Stubs"}
    
    ScanPlaceholders -->|Found Placeholders| RejectStub["Reject: Re-prompt with Missing Implementation"]
    RejectStub --> Code
    
    ScanPlaceholders -->|Clean| RunHarness["3. Run Automated Verification Harness<br/>(tsc, test runner, linter, security scan)"]
    
    RunHarness --> TestResult{"All Tests Pass?<br/>(Exit Code 0)"}
    
    TestResult -->|Failure / Exit Code != 0| Diagnostic["4. Diagnostic Feedback Loop<br/>Format stack trace into repair prompt"]
    Diagnostic --> Code
    
    TestResult -->|All Clean (Exit Code 0)| Approved["Task Verified & Completed"]
```

---

## 3. The Diagnostic Feedback Protocol

When a build or test fails, the orchestrator constructs a structured **Diagnostic Repair Prompt**:

```markdown
════════════════════════════════════════════════════════════════
[PROMPT LOOP FAILURE DETECTED — REPAIR REQUIRED]
════════════════════════════════════════════════════════════════
Step: Automated Verification
Target: [File / Module / Component]
Command: `pnpm test src/components/CartDrawer.test.tsx`
Exit Code: 1

Captured Output:
FAIL src/components/CartDrawer.test.tsx
  ● CartDrawer Component › should calculate subtotal with taxes correctly
    expect(received).toBe(expected) // Object.is equality
    Expected: 149.99
    Received: 129.99
      at src/components/CartDrawer.tsx:78:22

REQUIRED ACTIONS:
1. Inspect the exact line referenced in the stack trace.
2. Fix the underlying calculation or logic in `src/components/CartDrawer.tsx`.
3. DO NOT weaken or delete the test assertion.
4. Re-run `pnpm test src/components/CartDrawer.test.tsx` and confirm passing.
5. Provide the complete modified file without placeholders.
════════════════════════════════════════════════════════════════
```

---

## 4. Convergence Safeguards

To prevent infinite thrashing loops while guaranteeing completion:
1. **Identical Error Trap:** If a subagent returns the exact same compilation or test failure across 2 consecutive loops, the orchestrator:
   * Upgrades the subagent model to `pro` (or a higher reasoning tier).
   * Prompts the agent to emit an explicit diagnostic hypothesis before editing code.
2. **Hard Loop Ceiling:** Each ticket has a maximum iteration ceiling (default: 8 repair loops). If reached without resolution, the orchestrator triggers an escalation artifact to "The Board" (the user) detailing the exact environmental blocker.
3. **Atomic Scope:** Subagents are given small, atomic tickets (e.g. "Implement Cart Drawer Component & Hook" instead of "Implement the entire frontend") to maximize loop speed and minimize token overhead.
