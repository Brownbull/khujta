# Evolved Agents Unified Specification Schema

This schema standardizes all operational agent definition files under `khujta/010_evolved_agents/agents/`.  
Each agent file MUST follow this structure to enable predictable orchestration, automation, auditing, and cross-agent interoperability.

---

## 1. Frontmatter (YAML)

```yaml
---
name: short-machine-name (kebab-case)
archetype: Vision & Value | System Architect | Maker-Builder | Quality & Reality | Living User
description: One-line actionable description
merged_roles: Comma-separated merged legacy roles
primary_purpose: Single focused purpose statement
color: semantic accent color keyword
tools: Comma-separated canonical tool identifiers (must reflect actual available tools)
cycles_limit: Integer | null (if cyclical review/iteration logic applies)
placeholders:
  - {placeholder_name}: Human-readable description of runtime substitution
  - {another_placeholder}: Description
output_primary_artifact: relative/path/with/placeholders.ext
---
```

### Required Conventions
- `name` must be unique across repository.
- `tools` list only capabilities actually invocable in runtime environment.
- `placeholders` must enumerate EVERY `{variable}` referenced later in the document.
- `output_primary_artifact` must match the artifact described in Output Requirements.

---

## 2. Sections (Ordered, Mandatory Unless Marked Optional)

### 2.1 Mission
Concise, outcome-driven mission (NOT a restatement of description).

### 2.2 Functional Domains
Bullet list of domain scopes this agent is authoritative over (no overlap ambiguity).

### 2.3 Inputs Required
Structured subsections:
- Source Files / Data
- Dynamic Runtime Signals
- Cross-Agent Dependencies (explicit directional inputs)
- Preconditions (gating criteria before execution)

### 2.4 Operating Protocol
Two parts:
1. **Initialization Sequence** (ordered numbered steps)
2. **Execution Loop** (repeat cycle with conditional branches)
Include guard conditions and failure abort points.

### 2.5 Interface Contracts
Table-like bullet sets (no actual table required if avoided) for:
- Receives From (agent → artifact types)
- Provides To (artifact → agent consumers)
- Event Triggers (what starts a run)

### 2.6 Quality Gates
Hierarchical list of validation domains with PASS criteria (objective wording only).

### 2.7 Metrics & Telemetry
List:
- Realtime Counters
- Derived KPIs
- Logged Artifacts (filenames / formats)
- Failure Classifications

### 2.8 Constraints & Guardrails
Hard prohibitions + soft guidance. MUST include:
- Scope exclusions
- Security / compliance constraints
- Performance or latency bounds (if applicable)

### 2.9 Escalation & Collaboration
Define:
- Escalation triggers
- Escalation targets
- Synchronization cadence
- Conflict resolution protocol

### 2.10 Output Requirements
Precise artifact contract:
```
Primary Artifact: {output_primary_artifact}
Format: markdown|json|mixed
Sections / JSON Schema: Explicit required structure
Determinism: YES/NO (state why)
Versioning: How new cycles increment / replace
```

### 2.11 Response Format (Runtime Return)
MANDATORY final response block pattern (mirrors example agents).  
Specify EXACT minimal return template (fenced code) that downstream tools rely on.

### 2.12 Failure Modes & Recovery
Enumerate:
- Failure Code → Detection Heuristic → Recovery Action → Escalation (if any)

### 2.13 Security & Integrity (Optional if trivial)
Data handling, provenance tagging, tamper-evidence approaches.

### 2.14 Evolution Hooks (Optional)
What can be extended later without breaking contract.

---

## 3. Style & Content Rules

- All imperative instructions use present tense second person (e.g., "Validate", "Generate").
- No future tense speculation.
- No marketing language.
- No redundant restatement of earlier sections.
- Output artifact instructions MUST be single source of truth (do not contradict elsewhere).
- Placeholders appear ONLY in:
  - Frontmatter `placeholders`
  - Output Requirements
  - Response Format template

---

## 4. Placeholder Design Guidelines

Good placeholder examples:
- `{cycle_number}` → Sequential integer iteration index (starts at 1)
- `{feedback_signals_path}` → Absolute or relative path to structured ingestion file
- `{architecture_registry_path}` → Path to canonical architecture baseline document

Each placeholder MUST:
- Be lower_snake_case inside braces
- Have exactly one definition line under `placeholders` in frontmatter
- Be replaceable without semantic ambiguity

---

## 5. Validation Checklist (Applied to Every Agent File)

- [ ] Frontmatter present & valid YAML
- [ ] All placeholders defined & used consistently
- [ ] Exactly one Primary Artifact
- [ ] Output Response Format present & minimal
- [ ] No broken cross-agent references
- [ ] No orphan domain responsibilities
- [ ] Quality Gates measurable (no subjective adjectives)
- [ ] Failure Modes include recovery

---

## 6. Example Minimal Response Format Pattern

Agents MUST end runtime output (not file content) with ONLY:

```
## Artifact Location:
Primary artifact generated at: `{resolved_output_path}`
Status: [SUCCESS|FAILED]
```

(Adapt per agent spec if stricter wording required.)

---

## 7. Change Management

- Schema modifications require documenting delta in `CHANGELOG` (future file).
- Backward-incompatible changes must bump `schema_version` (add field when first needed).
- Existing agent files must be revalidated post-change.

---

## 8. Implementation Roadmap (Already Executed)

Phase 1 (Current): Establish schema (this file)  
Phase 2: Create 5 agent definitions (VIVA, SYRA, MAKA, QRA, LUA) conforming strictly  
Phase 3: Add `INDEX.md` summarizing cross-agent graph + responsibility matrix  
Phase 4: Consistency pass vs `evolved_agents.md`, `agents-workflow.md`, `daily-flow.md`

---

## 9. Pending Artifacts (Will Be Produced Next)

- Agent definitions:
  - `viva-agent.md`
  - `syra-agent.md`
  - `maka-agent.md`
  - `qra-agent.md`
  - `lua-agent.md`
- `INDEX.md` (cross-agent matrix)

---

## 10. Acceptance Criteria for This Schema

- Single canonical source for structural expectations
- Supports deterministic automation of parsing
- Clear output contract for each agent
- Extensible without churn

If all above satisfied, proceed to agent file creation.
