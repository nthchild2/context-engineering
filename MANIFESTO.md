# Manifesto for Agentic Orchestration (v0.2)

This manifesto is the durable output of a cyclic research process in this repository.

- Inputs: `research/sources.md`, `research/questions.md`, and cycle validation artifacts.
- Output: postulates that are evidence-traceable and status-labeled.
- Rule: separate descriptive observations from normative postulates.
- Learning model: this manifesto is the repository's current best knowledge state, updated each cycle as evidence improves or contradicts prior assumptions.

## Descriptive Observations

These claims describe how models and agent systems actually behave.

1. **Non-determinism is persistent**: LLM outputs vary run-to-run, and confidence language is not a reliable accuracy signal.
2. **Tool mediation increases reliability**: Models are stronger when they can execute and verify through tools instead of free-form text only.
3. **Operational limits dominate design**: context windows, latency, cost, and tool interfaces constrain agent performance.
4. **Multi-agent systems are conditional gains**: specialization can improve outcomes, but unclear roles add coordination noise.
5. **High-stakes tasks require external feedback**: objective checks and independent evidence are stronger signals than self-reported certainty.

## Normative Postulates

Status legend: `accepted` means sufficient evidence for use now; `provisional` means useful but still under active validation.

### P1 - Tool-grounded execution (`accepted`)
- Statement: Prefer agent actions that call tools and produce verifiable artifacts over raw narrative outputs.
- Evidence: Anthropic tool-use docs; OpenAI reliability guidance.
- Validation: Use objective pass/fail checks before accepting output.

### P2 - Artifact-centered orchestration (`accepted`)
- Statement: Coordinate work through shared artifacts (plans, records, outputs, docs, logs), not chat continuity.
- Evidence: AutoGen Studio workflow/debug emphasis.
- Validation: Require handoffs to update durable files each cycle.

### P3 - Verification before trust (`accepted`)
- Statement: Treat model confidence as untrusted until outputs pass executable or auditable checks.
- Evidence: Hallucination guidance.
- Validation: Add a verification field to cycle outputs for each promoted postulate.

### P4 - Explicit role boundaries (`accepted`)
- Statement: Use multi-agent design only when role boundaries and handoff contracts are explicit.
- Evidence: AutoGen/CrewAI role-separation results and coordination overhead notes.
- Validation: Reject multi-agent expansions without role and interface definitions.

### P5 - Externalize memory and audit trails (`accepted`)
- Statement: Persist state, rationale, and decisions in files/logs; never rely on transient model context alone.
- Evidence: Context-window limitations and memory constraints across vendor docs.
- Validation: Cycle records must include decisions, evidence links, and unresolved gaps.

### P6 - Classify failures by layer (`provisional`)
- Statement: Every failed run should be labeled as model, orchestration, or specification failure.
- Evidence: Cross-source pattern from benchmark interpretation and orchestration debugging guidance.
- Validation: Trial in Cycle 02 on at least one concrete domain task.
- Cycle 02 status: `hold` (taxonomy and counting protocol defined, but not yet stress-tested on multiple executed runs).

### P7 - Optimize for trustworthy attention (`provisional`)
- Statement: Design flows that minimize irrelevant context and maximize surfaced, checkable signals.
- Evidence: Validated hypothesis on attention scarcity and context management constraints.
- Validation: Compare a focused-context run vs broad-context run in a future cycle.
- Cycle 02 status: `hold` (supporting evidence expanded; controlled comparison still pending).

### P8 - Evidence-weighted promotion (`provisional`)
- Statement: Promote postulates only when evidence quality, reproducibility, and scope fit are explicit and auditable.
- Evidence: NIST AI RMF, OECD principles, HELM-style evaluation framing.
- Validation: Apply rubric to at least two postulate promotion decisions in Cycle 03.
- Cycle 02 status: `added`.

## Postulate Template

Use this template when drafting or revising postulates.

```markdown
### PX - <short name> (`candidate|provisional|accepted|rejected`)
- Statement: <normative claim>
- Claim type: <descriptive|normative>
- Evidence: <source links, benchmark references, experiment artifacts>
- Scope and assumptions: <where this applies and where it may fail>
- Validation method: <smallest executable or auditable check>
- Last updated in cycle: <cycle-id>
```

## Provenance

- `v0.1` derived in Cycle 01 from `research/sources.md` and `research/questions.md`.
- `v0.2` updated in Cycle 02 with protocol-oriented evidence and status checks.
- Operationalized with run records in `research/cycles/cycle-01.md` and `research/cycles/cycle-02.md`.
