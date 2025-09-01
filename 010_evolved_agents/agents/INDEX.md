# Evolved Agents Index & Responsibility Matrix

Canonical cross-agent overview for `khujta/010_evolved_agents`.  
Sources synchronized with: `evolved_agents.md`, `agents-workflow.md`, `daily-flow.md`, individual agent specs under `agents/`.

---

## 1. Agent Archetypes

| Agent | Archetype | Primary Purpose | Primary Artifact (per spec) |
|-------|-----------|-----------------|------------------------------|
| VIVA | Vision & Value | Continuous value-driven prioritization & acceptance criteria definition | `{value_map_path}` |
| SYRA | System Architect | Secure-by-default adaptive architecture & infra alignment | `{architecture_alignment_report_path}` |
| MAKA | Maker-Builder | Full-stack feature vertical slice implementation | `{implementation_report_path}` |
| QRA | Quality & Reality | Reality + quality validation (UX, accessibility, performance) | `{quality_review_report_path}` |
| LUA | Living User | High-fidelity workflow simulation & adoption/friction signaling | `{adoption_signals_path}` |

---

## 2. Responsibility Domains (No Overlap)

| Domain | Owner (Primary) | Secondary (If Any) | Exclusions Clarified |
|--------|-----------------|--------------------|----------------------|
| Backlog Value Scoring | VIVA | LUA (signals) | Implementation details |
| Architecture Patterns & Drift Control | SYRA | MAKA (feedback) | UX design, backlog scoring |
| Full-Stack Feature Construction | MAKA | SYRA (constraints) | Prioritization, final QA sign-off |
| Quality & UX Validation | QRA | LUA (reality), SYRA (perf baselines) | Architecture decisions, backlog reprioritization |
| Workflow Simulation & Friction Detection | LUA | QRA (validation correlation) | Feature implementation, architecture changes |
| Security Embedding | SYRA | MAKA (execution) | End-user UX heuristics |
| Localization Canonical Source (Spanish-first) | MAKA | QRA (usability), VIVA (value phrasing) | Architecture, simulation |
| Performance Baseline Ownership | SYRA | QRA (UX impact), LUA (interaction latency) | Business prioritization |
| Adoption & Usage Signal Synthesis | LUA | VIVA (value integration) | Test coverage judgment |
| Accessibility Compliance Gate | QRA | MAKA (remediation) | Architecture risk scoring |
| Cognitive Load Index | LUA (raw heuristics) | QRA (interpretation) | Implementation strategy |
| Risk & Drift Escalation | SYRA | VIVA (business trade-offs) | UX micro-adjustments |

---

## 3. Inter-Agent Data Flow (Core Loop)

```
LUA (friction/adoption signals)
  → VIVA (value map & acceptance criteria)
    → MAKA (implementation report & features)
      → SYRA (architecture alignment & performance baselines)
        → QRA (quality & reality validation)
          → LUA (updated scenarios & friction confirmation)
(cycle repeats)
```

Escalation Side-Channels:
- SYRA ↔ VIVA (cost & compliance trade-offs)
- QRA ↔ MAKA (defect remediation cycle)
- LUA ↔ QRA (scenario refinement)
- SYRA ↔ MAKA (secure scaffolding + deviations)
- LUA ↔ VIVA (priority focus adjustments)

---

## 4. Artifact Dependency Graph

| Producing Agent | Artifact | Consumed By | Consumption Purpose |
|-----------------|----------|------------|---------------------|
| LUA | `{adoption_signals_path}` | VIVA | Priority weighting (friction, adoption) |
| VIVA | `{value_map_path}` | MAKA | Feature intake selection |
| MAKA | `{implementation_report_path}` | SYRA | Alignment drift & performance impact |
| SYRA | `{architecture_alignment_report_path}` | QRA | Baselines & constraints for validation |
| QRA | `{quality_review_report_path}` | LUA | Scenario recalibration & friction resolution tracking |

Supporting / Shared:
| Artifact | Source | Downstream |
|----------|--------|------------|
| Performance Baseline `{performance_baseline_path}` | SYRA | QRA, LUA |
| Friction Catalog `{friction_catalog_path}` | LUA | VIVA, QRA, MAKA |
| Risk Register `{risk_register_path}` | SYRA | VIVA, MAKA |

---

## 5. Escalation Matrix

| Trigger | Origin | Escalates To | Mandatory Action |
|---------|--------|--------------|------------------|
| EXCESSIVE_CHURN (VIVA) | VIVA | Human Oversight + SYRA | Validate weights / business shifts |
| SECURITY_CRITICAL | SYRA | VIVA + MAKA + Security Oversight | Block affected features, prioritize remediation |
| PERFORMANCE_REGRESSION (sustained) | SYRA/QRA | MAKA + VIVA | Optimize or re-scope features |
| ACCESSIBILITY_CRITICAL | QRA | MAKA + VIVA | Block release; remediate |
| COVERAGE_DEFICIT (core flows) | LUA | QRA + MAKA | Add scenario/tests |
| ADOPTION_COLLAPSE (new feature) | LUA | VIVA + MAKA | Re-evaluate user value / UX redesign |

---

## 6. Quality Gate Alignment Summary

| Gate Category | Primary Enforcer | Feeds Back To | Pass Criteria Summary |
|---------------|------------------|---------------|-----------------------|
| Value Determinism | VIVA | MAKA, VIVA self | Stable ranking hash |
| Architecture Security | SYRA | MAKA, QRA | No critical unmitigated vulns |
| Implementation Integrity | MAKA | QRA, SYRA | Zero type errors & coverage threshold |
| Reality & UX | QRA | VIVA, MAKA | Acceptance & accessibility compliance |
| Workflow Fidelity | LUA | VIVA, QRA | Scenario coverage & friction detection integrity |

---

## 7. Daily Flow Mapping (Condensed)

| Phase | Lead Agent | Parallel Agents | Key Outputs |
|-------|------------|-----------------|-------------|
| Morning Re-Scoring | VIVA | SYRA (infra health), LUA (baseline simulations) | Updated value map |
| Midday Build & Validation | MAKA | SYRA (alignment), QRA (continuous tests) | Implementation report, perf assessments |
| Afternoon Simulation & Feedback | LUA | VIVA (adjust priorities), QRA (extended validation) | Adoption & friction deltas |
| Evening Deployment Decision | SYRA (deploy readiness) | VIVA/QRA/LUA (green status) | Aligned release decision |

---

## 8. Consistency Verification Checklist

| Item | Status |
|------|--------|
| Archetype roles match `evolved_agents.md` | OK |
| Workflow loop matches `agents-workflow.md` | OK |
| Daily phases align with `daily-flow.md` | OK |
| Dependencies reflect each agent spec frontmatter placeholders | OK |
| No domain overlap conflicts detected | OK |

---

## 9. Open Extension Hooks

| Future Hook | Candidate Owner | Rationale |
|-------------|-----------------|-----------|
| Weight Config Externalization | VIVA | Dynamic prioritization tuning |
| IaC Drift Auto-Diff | SYRA | Faster mitigation cycles |
| Automated Cognitive Model | LUA & QRA | Predictive friction detection |
| Complexity Scoring Engine | MAKA | Resource forecasting |
| Cross-Agent Telemetry Bus | All (SYRA steward) | Unified observability |

---

## 10. Validation Criteria for This Index

- Reflects current agent spec filenames and primary artifacts
- No contradictory responsibility claims
- Each artifact has at least one consumer
- All escalation triggers map to an action & target
- Workflow loop closed (no dangling outputs)

If any criterion fails during future changes, this index must be regenerated.

---

## 11. Change Management

Any modification to an agent's primary artifact contract or quality gate requires:
1. Update agent file
2. Update relevant matrix rows here
3. Re-run consistency checklist
4. Record delta in future `CHANGELOG` (planned)
