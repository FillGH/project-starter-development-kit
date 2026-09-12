# Project Starter Development Kit

> **v0.1 — Ready for Pilot**

A lightweight, risk-based starter for engineering and software projects. It is designed to be reusable across web apps, dashboards, automations, AlgoTrade systems, industrial tools, scripts, and other technical projects without forcing heavyweight process onto small work.

## Core principle

**Use engineering judgment to add only the process, code, documentation, and controls that earn their cost.**

The kit standardizes the way a project is thought through, not the technology used to build it.

## Development lifecycle

```text
DEFINE → DESIGN → BUILD → VERIFY → OPERATE → LEARN
```

### DEFINE
Understand the problem, desired outcome, users, constraints, assumptions, and consequences of failure. A valid outcome may be **DO NOT BUILD** when a simpler solution is better.

### DESIGN
Choose scope, trade-offs, solution approach, risks, and acceptance criteria. Use a prototype, mock-up, pseudo-code, or simulation only when it helps resolve uncertainty.

### BUILD
Implement the agreed baseline using the simplest sufficient solution. Avoid speculative features, unnecessary abstractions, and infrastructure without a demonstrated need.

### VERIFY
Use evidence to show that the solution satisfies the acceptance criteria. Evidence may include manual tests, automated tests, backtests, field tests, smoke tests, or user acceptance depending on the project.

### OPERATE
Consider real-world use: ownership, failure detection, fallback, recovery, backup, maintenance, and support only to the level justified by risk.

### LEARN
Check whether the solution actually improved the original problem. Capture lessons that are likely to be useful again.

## Core files

Every project created from this template starts with only three required files:

- `README.md` — what the project is and how to use/run it.
- `PROJECT.md` — the engineering source of truth: problem, scope, design, requirements, risks, acceptance criteria, baseline, and changes.
- `AGENTS.md` — working rules for AI coding agents and developers.

Add source-code, test, documentation, or operational folders only when the project actually needs them.

## Two decision gates

### Ready to Build
Before implementation, there should be enough clarity on:

- Problem and desired outcome
- Scope and out of scope
- Important constraints and assumptions
- Chosen design direction
- Acceptance criteria
- Material risks

The goal is not perfect documentation. The goal is to avoid coding from guesses.

### Ready to Release
Before real use, confirm that:

- Acceptance criteria pass
- No known critical defect remains
- Material risks are handled appropriately
- The target environment works
- Recovery/fallback exists when the risk justifies it
- The owner/user accepts the result

## Risk-based controls

GitHub Issues, branches, pull requests, Codex review, automated tests, CI/CD, monitoring, backup, runbooks, and security review are **optional controls**, not mandatory ceremony.

Add them when risk or complexity makes them worthwhile. Examples:

- Use an **Issue** when work must be tracked beyond the current session, a bug needs follow-up, or a dependency/backlog item must not be lost.
- Use a **Pull Request** when independent review is valuable, multiple people contribute, or regression risk is meaningful.
- Use **Codex review** when correctness, regression, data integrity, or relevant security risk justifies an independent review.
- Use **automated tests** when logic is complex, regression risk is high, or repeated verification makes automation worthwhile.
- Use **monitoring, backup, or a runbook** when failure, data loss, or handover would have meaningful consequences.

## Review finding policy

A review finding is a recommendation, not an automatic requirement. Every actionable finding should end in one of three states:

- **FIX** — relevant to the current baseline and worth correcting now.
- **DEFER** — valid, but not required for the current baseline.
- **REJECT** — outside scope, too hypothetical, or adds more complexity than value.

**Zero review findings is not a project KPI.**

## Starting a new project

1. Create a repository from this template.
2. Replace this README with project-specific usage information when appropriate.
3. Complete `PROJECT.md` enough to pass **Ready to Build**.
4. Keep `AGENTS.md` unless the project has a concrete reason to amend it.
5. Build and verify against the acceptance criteria.
6. Add controls only when risk or complexity justifies them.
7. After real use, capture useful lessons and refine the next project rather than adding process automatically.

## Pilot rule

This kit is intentionally **v0.1**. Pilot it on several real projects before promoting it to a stable v1.0. Add a rule to the core only when repeated experience shows that the rule consistently prevents real problems or creates clear value.
