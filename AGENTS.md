# Agent and Developer Working Rules

This repository follows a lightweight, risk-based engineering process.

`PROJECT.md` is the authoritative statement of intended project behavior, scope, acceptance criteria, risks, and current baseline.

## 1. Work from the project definition

- Read `PROJECT.md` before making material changes.
- Do not expand scope without explicit human approval.
- Do not silently reinterpret requirements to make implementation easier.
- If the code, an issue, a review comment, or an AI suggestion conflicts with `PROJECT.md`, stop and surface the conflict rather than choosing silently.
- Human product and engineering decisions override AI recommendations.

## 2. Prefer the simplest sufficient solution

- Solve the current, demonstrated problem.
- Do not add speculative features.
- Do not introduce abstractions, frameworks, services, dependencies, infrastructure, or configuration for hypothetical future needs.
- Design for known change, not imagined change.
- Preserve working behavior unless the baseline or requirement intentionally changes.
- Complexity must justify its implementation and maintenance cost.

## 3. Use engineering judgment, not ceremony

GitHub Issues, branches, pull requests, Codex review, automated tests, CI/CD, monitoring, backup, runbooks, and additional documentation are controls, not mandatory steps.

Add a control when the project's risk, complexity, collaboration needs, or repeated verification cost makes it valuable.

Do not create process solely because a tool or template makes it available.

## 4. Build only when Ready to Build

Before substantial implementation, confirm that `PROJECT.md` provides enough clarity on:

- the problem and desired outcome;
- scope and out of scope;
- material constraints and assumptions;
- the chosen design direction;
- acceptance criteria; and
- material risks.

Perfect documentation is not required. Avoid implementing from unresolved guesses that could materially change the solution.

## 5. Verify against evidence

- Verification must map back to acceptance criteria and material risks.
- Use the lightest verification method that provides credible evidence.
- Manual testing is acceptable when it is reliable and proportionate.
- Automate tests when logic, regression risk, repeated execution, money, important data, production impact, or similar consequences justify it.
- Passing compilation or a successful deployment is not by itself evidence that the project outcome is correct.

## 6. Review policy

Review is decision support, not an authority.

Focus review on risks relevant to the current baseline, especially:

- correctness;
- regression against intended working behavior;
- data integrity;
- security relevant to the actual project context; and
- failure modes with meaningful consequences.

Do not optimize for zero review findings.

Every actionable finding must be classified as one of:

- **FIX** — relevant to the current baseline and worth correcting now.
- **DEFER** — valid, but intentionally postponed because it is not required for the current baseline.
- **REJECT** — outside scope, too hypothetical, incorrect, or adds more complexity than value.

For DEFER or REJECT, record a short rationale where it will remain visible if the finding matters later.

Avoid repeated review cycles unless a new change or unresolved material risk justifies another review.

## 7. Change control without bureaucracy

A baseline may change when new evidence or requirements justify it.

When a material requirement changes:

1. update `PROJECT.md`;
2. state the reason in the change history or important decisions section when useful;
3. update affected acceptance criteria; and
4. then modify the implementation.

Do not allow the implementation to become the only record of a changed requirement.

## 8. Release responsibly

A release should satisfy the Ready to Release gate in `PROJECT.md` at a rigor level proportionate to risk.

Consider, where relevant:

- target-environment verification;
- smoke testing;
- user/owner acceptance;
- rollback or fallback;
- data backup/recovery;
- operational ownership; and
- failure detection.

Do not add these controls when their cost exceeds the credible consequence they mitigate.

## 9. After release

Treat operation as part of engineering.

When useful, observe whether the solution:

- remains correct in real use;
- can be maintained by the intended owner;
- fails in ways not anticipated during design; and
- actually improves the original problem and success criteria.

Capture reusable lessons, but do not turn a one-off event into a permanent core rule unless repeated experience or high severity justifies it.

## 10. Default decision rule

When multiple approaches satisfy the current project:

> Choose the option that meets the requirements and manages the material risks with the least unnecessary complexity and operational burden.
