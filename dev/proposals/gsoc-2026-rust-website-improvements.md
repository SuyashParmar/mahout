# GSoC 2026 Draft Proposal: Rust Code Quality and Website Improvements (QDP + Site)

## Problem Statement
Mahout QDP has a strong Rust core (`qdp-core`, `qdp-kernels`, PyO3 bindings), but maintainability and contributor UX can be improved in two connected areas:

1. Rust quality hardening (unsafe boundaries, docs, lint hygiene, targeted tests)
2. Website/docs consistency (link integrity, navigation coherence, API discoverability)

The goal is to improve long-term maintainability while reducing friction for new contributors.

## Scope

### A) Rust quality improvements (QDP)
- Narrow broad/complex `unsafe` regions where possible
- Add/normalize `// SAFETY:` justification comments at unsafe boundaries
- Resolve clippy/rustfmt debt in touched modules
- Improve rustdoc coverage for key public APIs
- Add deterministic tests for under-covered behavior/regression-prone paths

### B) Website/docs improvements
- Fix broken/outdated links and navigation mismatches
- Replace TODO placeholders with concrete content/links where feasible
- Improve QDP API discoverability and cross-linking in docs
- Add/strengthen documentation checks in CI where appropriate

## Deliverables
- A sequence of reviewable PRs (small batches) across `qdp/`, `docs/`, and `website/`
- Measurable reduction in clippy/doc issues for touched modules
- Improved rustdoc/API discoverability from docs navigation
- Contributor-facing guidance updates for Rust/doc changes

## Milestone Plan (Draft)

### Phase 1: Baseline and prioritization (Week 1-2)
- Identify top Rust quality hotspots and docs pain points
- Publish issue checklist with module/file targets

### Phase 2: Rust quality hardening (Week 3-7)
- Unsafe-scope refactors + safety comments
- Lint/style cleanup in targeted modules
- Focused tests for regressions and edge cases

### Phase 3: Website/docs improvements (Week 8-10)
- Link/nav consistency fixes
- QDP docs cross-linking and placeholder cleanup
- API discoverability improvements

### Phase 4: Consolidation (Week 11-12)
- Final documentation polish
- Follow-up issue list for post-GSoC continuity

## Success Metrics
- All introduced/updated checks pass in CI
- No functional regressions in existing test suites
- Reduced doc/link errors and clearer navigation to QDP API resources
- Maintainer-accepted PRs with clear audit trail and rationale

## Risks and Mitigation
- Risk: scope spread across Rust and website areas
  - Mitigation: small, milestone-scoped PRs with strict issue checklist
- Risk: refactor regressions
  - Mitigation: behavior-preserving changes + targeted tests before/after

## Current Status
This file is an initial prototype draft to gather maintainer feedback on scope and sequencing before submitting a final GSoC proposal.
