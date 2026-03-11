# ADR-001: Adopt Spec-Driven Development with AI-Augmented Implementation

> **Status:** Proposed  
> **Date:** 2026-03-11  
> **Decision Makers:** Chief Architect, VP Engineering  
> **Tags:** process, ai, architecture

## Context

Qcells software engineering is evaluating how to restructure team design and workflows to take advantage of AI-powered code generation tools (specifically Claude Code). The current model — large teams of mixed-seniority developers writing code manually against loosely defined requirements — is not optimized for AI-augmented development.

Key observations:

- AI code generation tools produce significantly higher quality output when given precise, detailed specifications rather than vague requirements or verbal instructions.
- The bottleneck in AI-augmented development shifts from "writing code" to "defining what to build" and "validating what was built."
- Traditional team structures (many junior/mid devs, few architects) are inverted in value — architectural and specification work becomes the highest-leverage activity.
- Executive reporting based on story points and velocity is a poor proxy for delivered value. Spec-based tracking offers a more meaningful alternative.

## Decision

We will adopt a spec-driven development (SDD) model with the following core principles:

1. **The spec is the atomic unit.** All planning, execution, and reporting revolves around formally written specifications authored by architects.

2. **AI generates code, humans provide judgment.** Senior developers orchestrate Claude Code agent teams to implement specs. They review, validate, and integrate — they don't write most code by hand.

3. **Four core roles** with clearly defined responsibilities: Architect, Senior Developer, TPM, and Dev Manager.

4. **Seven-phase lifecycle:** Spec → Review → Prioritize → Implement → Validate → Ship → Report.

5. **Executive reporting** maps specs to features to milestones, providing traceability from investment to delivered value.

## Consequences

### Positive

- Higher leverage per engineer — smaller, senior-heavy teams producing more output
- Better traceability from business goals to implementation
- Specs serve as durable documentation (not just throwaway tickets)
- AI-generated code is more consistent when driven by precise specs
- Executive reporting becomes more meaningful (delivered specs, not story points)

### Negative / Risks

- Architects become a bottleneck if spec throughput is too low
- Requires significant investment in spec writing skills and templates
- Senior developers need to learn new skills (agent orchestration, prompt engineering)
- AI code quality depends heavily on spec quality — garbage in, garbage out
- Metrics and estimation models from traditional development don't transfer directly
- Cultural shift may face resistance from developers accustomed to writing code directly

### Mitigations

- Invest in spec templates, examples, and training for architects
- Start with a pilot team before full rollout
- Track spec rework rate as an early indicator of spec quality issues
- Dev Managers coach developers through the transition
- Iterate on the model based on retrospective feedback

## Alternatives Considered

1. **Keep current model, add AI tools informally.** Rejected because it doesn't address the fundamental shift in where value is created. Ad hoc AI adoption leads to inconsistent results.

2. **Fully automated AI pipeline (no human-in-the-loop).** Rejected because current AI tools require human judgment for architectural decisions, edge cases, and quality assurance. Premature for 2026.

3. **Test-driven development (TDD) as the primary driver.** Considered as complementary, not a replacement. TDD fits well within the SDD model — specs inform tests, tests validate AI output. But TDD alone doesn't address team structure, reporting, or the spec-writing bottleneck.

## References

- [Operating Model (GitHub Pages)](../index.html)
- [Spec Template](../../specs/SPEC_TEMPLATE.md)
