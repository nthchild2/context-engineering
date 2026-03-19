## Plan: Cyclic Agent-Engineering Methodology

Turn the repository into a repeatable input-output system:

- Inputs: `research/sources.md`, `research/questions.md`, and validation artifacts.
- Transformation: distill evidence into postulates, then test postulates.
- Outputs: updated manifesto postulates, updated question backlog, and cycle records.
- Feedback: unresolved gaps and failed assumptions become next-cycle inputs.

Learning lens for this process:
- Treat each cycle as a knowledge-refinement loop.
- `sources` capture observations, `questions` capture uncertainty, `manifesto` captures consolidated guidance.
- Validation updates confidence, scope, and status of what the repository believes.

This file is the canonical operating procedure for cycle execution.

## Cycle Definition

### Required Artifact Flow

When applicable in a cycle, update artifacts in this order:

1. `research/sources.md`
2. `research/questions.md`
3. `MANIFESTO.md`
4. `research/cycles/cycle-XX.md`

The sequence preserves traceability from evidence to questions to postulates to run record.

### Phase 1: Intake
1. Update `research/sources.md` with new primary sources and concise extraction notes.
2. Update `research/questions.md` with question status and priority.
3. Tag each question as `answered`, `partial`, `unresolved`, or `new`.

Required outputs:
- New or revised `S##` source entries.
- New or revised `E##` evidence rows linked to `Q#` and `P#/candidate`.

Exit criteria:
- Source additions are traceable.
- Question backlog is prioritized.

### Phase 2: Distillation
1. Separate descriptive claims from normative recommendations.
2. Draft or revise postulates with explicit evidence links and uncertainty labels.
3. Record which claims are candidate, provisional, accepted, or rejected.

Required outputs:
- Updated question statuses and next actions.
- Candidate postulates with clear status labels.

Exit criteria:
- Every postulate has evidence provenance and a validation path.

### Phase 3: Manifesto Nourishment
1. Promote accepted/provisional postulates into `MANIFESTO.md`.
2. Keep provisional postulates clearly marked as provisional.
3. Preserve stable naming and focused diffs.

Required outputs:
- Postulate updates using the manifesto template.
- Explicit mapping from `P#` to supporting `E##`.

Exit criteria:
- Manifesto updates map to concrete postulate records.

### Phase 4: Validation
1. Run the smallest relevant validation (benchmark slice, domain task, or manual protocol).
2. Record outcomes and classify failures as model, orchestration, or specification failures.
3. Update question and postulate status based on evidence quality.

Required outputs:
- Validation record with method, result, and limitation.
- Queue for next cycle with prioritized unresolved items.

Exit criteria:
- Validation outcome is logged.
- Next-cycle questions are explicitly queued.

## Canonical Artifacts Per Cycle

- `research/sources.md`: source intake and extraction notes.
- `research/questions.md`: question backlog and cycle status table.
- `research/cycles/cycle-XX.md`: cycle inputs, outputs, deltas, and open gaps.
- `MANIFESTO.md`: durable postulates promoted from cycle outputs.

## Promotion and Status Rules

- `candidate`: drafted from evidence, not yet validated.
- `provisional`: supported by evidence but still needs stronger or broader validation.
- `accepted`: sufficiently supported for active methodology guidance.
- `rejected`: contradicted, weakly supported, or superseded.

Do not promote from `candidate` to `accepted` in a single step unless validation quality is explicitly documented.

## Cycle Handoff Bootstrap

At the start of each new session, read these files in order:

1. `README.md`
2. `AGENTS.md`
3. `plans/build-methodology-plan.md`
4. Latest file in `research/cycles/`
5. `research/questions.md`
6. `research/sources.md`

This bootstrap is required to avoid dependence on long-lived chat context.

## Recurring Cycle Execution Checklist

Use this checklist for every new cycle (`cycle-XX`):

1. Choose cycle scope and write one-sentence objective in `research/cycles/cycle-XX.md`.
2. Intake update in `research/sources.md`:
   - Add new `S##` source entries.
   - Add new `E##` evidence rows linked to `Q#` and `P#/candidate`.
3. Question update in `research/questions.md`:
   - Update question statuses.
   - Add new questions discovered during intake.
   - Add cycle delta summary.
4. Manifesto update in `MANIFESTO.md`:
   - Promote/revise postulates with status labels.
   - Keep evidence references explicit.
5. Validation update in `research/cycles/cycle-XX.md`:
   - Record validation method and result.
   - Record failure classification (`model|orchestration|specification`).
   - Queue next-cycle priorities.

Minimum cycle-completion bar:
- At least 2 new/updated `E##` entries.
- At least 1 question status change.
- At least 1 manifesto postulate status check (promote, hold, or demote with reason).
- A completed `research/cycles/cycle-XX.md` run record.

## Cycle Comparison Protocol (for Q19-Q21)

When claiming methodology improvement across cycles, record these fields in `research/cycles/cycle-XX.md`:

- Comparison scope: what changed in orchestration design.
- Baseline: prior-cycle or control setup.
- Metrics: success rate, rework count, latency proxy, cost proxy, and verification pass rate.
- Failure breakdown: `model|orchestration|specification` counts.
- Promotion decision: which postulates were promoted, held, demoted, or added.

Use this protocol even for documentation-only cycles; mark missing runtime metrics explicitly.

## First Run (Cycle 01)

1. Snapshot existing sources and questions as cycle inputs.
2. Convert validated hypotheses into postulates using the manifesto template.
3. Mark answered and unresolved questions; add new questions discovered this cycle.
4. Write `research/cycles/cycle-01.md` with question and postulate deltas.
5. Queue Cycle 02 priorities from unresolved gaps.
