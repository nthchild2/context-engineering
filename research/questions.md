# Research Questions

## Cycle Tracking (Cycle 02)

| Q# | Status | Evidence strength | Cycle 02 output | Next action |
| --- | --- | --- | --- | --- |
| 3 | partial | medium | Parameter set is stable (context, cost, latency, tool boundaries), but thresholds remain uncalibrated. | Add threshold bands from one executable protocol run. |
| 8 | partial | medium | Governance sources support risk-based autonomy gating. | Draft concrete gating policy and test on one scenario. |
| 9 | partial | medium | Focused reasoning-action loops reduce context drift in principle. | Run focused vs broad context comparison. |
| 11 | partial | medium | Tool boundary is clearer with explicit act/observe loops. | Define boundary checklist for ambiguous tasks. |
| 12 | answered | high | Evaluation protocol now requires baseline + metrics + failure breakdown. | Apply protocol in one executable cycle. |
| 13 | partial | medium | Failure taxonomy is reinforced; counting protocol defined but not yet stress-tested. | Pilot taxonomy counts on two tasks. |
| 16 | partial | medium | Audit trail now includes comparison scope, metrics, and promotion decisions. | Add example artifact bundle template. |
| 19 | partial | medium | Promotion criteria drafted: evidence quality, reproducibility, scope fit, and contradiction check. | Convert criteria into rubric with pass/fail bar. |
| 20 | partial | medium | Core metric schema drafted (success, rework, latency, cost, verification pass rate). | Calibrate acceptable ranges. |
| 21 | partial | medium | Baseline protocol drafted for attribution of orchestration gains. | Execute controlled baseline in Cycle 03. |

## Cycle Tracking (Cycle 01)

| Q# | Status | Evidence strength | Cycle 01 output | Next action |
| --- | --- | --- | --- | --- |
| 1 | answered | medium | Pattern tasks and tool use are repeat strengths. | Keep monitoring with benchmark updates. |
| 2 | answered | medium | Hallucinations and overconfidence remain persistent risks. | Track mitigation patterns by provider. |
| 3 | partial | medium | Context, cost, latency, and tooling are key parameters. | Add concrete thresholds from experiments. |
| 4 | answered | medium | Role separation + explicit handoffs are key gains. | Test against single-agent baseline in Cycle 02. |
| 5 | partial | low | Specialization transfers; implicit coordination does not. | Collect direct domain-level evidence. |
| 6 | answered | medium | Domain application needs external feedback loops. | Convert into stricter validation protocol. |
| 7 | partial | low | Accountable deliverables appear stronger than prompt-only tasks. | Define a deliverable contract template. |
| 8 | partial | low | Autonomy should depend on risk and uncertainty. | Add concrete gating policy examples. |
| 9 | partial | low | Partitioned context with shared artifacts reduces noise. | Run focused-context experiment. |
| 10 | answered | medium | Persistent state and audit trails must be externalized. | Define minimum artifact set per run. |
| 11 | partial | medium | Agent proposes intent; tool executes verifiable actions. | Add boundary tests on ambiguous tasks. |
| 12 | answered | medium | Benchmarks + real tasks outperform demo-only claims. | Add repo-native evaluation rubric. |
| 13 | partial | low | Failure taxonomy is useful but under-tested operationally. | Pilot taxonomy on one concrete task. |
| 14 | partial | low | More agents increase cost/latency; gains depend on design quality. | Collect cycle-level cost/latency metrics. |
| 15 | partial | low | Artifact-based coordination appears robust. | Define artifact handoff checklist. |
| 16 | partial | low | Minimal audit trail likely includes actions, checks, and overrides. | Formalize minimum audit schema. |
| 17 | partial | low | Multi-agent wins when decomposition and specialization are real. | Validate with controlled A/B task comparison. |
| 18 | partial | low | Maximum capability should prioritize reliability + leverage over raw speed. | Define measurable objective function. |

## New Questions Spawned in Cycle 01

19. What is the minimum acceptance bar for promoting a postulate from `provisional` to `accepted`?
    - Note: Need explicit promotion criteria to avoid subjective upgrades.
20. What cycle metrics are mandatory so iterations are comparable over time?
    - Note: Candidate metrics include success rate, rework rate, latency, and cost.
21. What is the smallest repeatable experiment that distinguishes orchestration gains from model gains?
    - Note: Need a controlled baseline protocol for single-agent vs multi-agent runs.

## New Questions Spawned in Cycle 02

22. How should postulate confidence decay when evidence is old, narrow, or contradicted by newer runs?
    - Note: Need explicit downgrade triggers for `accepted` and `provisional` postulates.
23. What is the minimum cross-domain sample size before claiming a postulate is generally applicable?
    - Note: Need a transferability bar beyond one-domain validation.

## Question Backlog

1. What are generative AIs actually good at in agentic work?
   - Note: Excel at pattern recognition, code generation, and tool-mediated tasks (sources: OpenAI GPT-5.1, Anthropic Claude, survey paper).
2. What are they consistently bad at, even when they appear confident?
   - Note: Long-term memory, complex multi-step reasoning without external aids, reliable factual recall beyond training data, and non-deterministic outputs prone to hallucinations (Anthropic reduce hallucinations, OpenAI prompting guide).
3. Which operating parameters matter most in practice?
   - Note: Context window size, cost, latency, tool interfaces, and evaluation setup quality (Anthropic context, model docs, evaluation sources).
4. What kinds of orchestration patterns make multiple agents stronger than one?
   - Note: Role separation, explicit handoffs, checkpoints for review, and tool-mediated execution (AutoGen, CrewAI, LangChain Agents).
5. Which human organizational patterns transfer well to AI agents, and which do not?
   - Note: Specialization and delegation transfer well; implicit communication and trust in confidence do not (Challenges in Human-Agent Communication, AutoGen).
6. How should agent orchestration change when moving from general guidance to a specific application domain?
   - Note: Emphasize objective checks, artifact-centered workflows, and verification over self-confidence.
7. What is the unit of work for an agent: prompt, task, subtask, role, or accountable deliverable?
   - Note: Accountable deliverable or subtask with checkpoints, rather than loose prompts (AutoGen Studio, survey paper).
8. When should an agent be autonomous, and when should it be gated by a human?
   - Note: Autonomous for low-risk tasks with verification; gated for high-stakes or uncertain decisions (AutoGen, Challenges paper).
9. How should context be partitioned across agents so that more agents increase signal rather than noise?
   - Note: Assign specialized roles with partitioned context and external memory for shared state (Anthropic context, CrewAI).
10. What information should never live only in model context and must be externalized into tools, files, memory, or logs?
    - Note: Persistent state, shared artifacts, and audit trails must be externalized (Anthropic context, manifesto implications).
11. What is the right boundary between an agent and a tool?
    - Note: Agent proposes intent, tool executes; boundary at verifiable action vs. model reasoning (Anthropic tool use, OpenAI Assistants API).
12. How do we evaluate an orchestration design beyond anecdotal demos?
    - Note: Use benchmarks, real-world tasks, and executable validation.
13. Which failures are model failures, which are orchestration failures, and which are specification failures?
    - Note: Model: hallucinations, determinism; Orchestration: poor handoffs, noise; Specification: unclear roles or goals (sources across buckets).
14. How do latency, cost, and reliability trade off against one another as we add more agents?
    - Note: More agents increase latency and cost but can improve reliability through specialization if designed well (AutoGen v0.4, operational constraints).
15. How should agents coordinate around shared artifacts such as plans, records, issues, and decisions?
    - Note: Use external artifacts for coordination, with logging and checkpoints.
16. What is the minimum viable audit trail for trustworthy agentic systems?
    - Note: Logs of actions, verifications, and human overrides; traceable to sources and experiments (manifesto implications).
17. When does a multi-agent design outperform a single strong agent with good tools?
    - Note: When tasks require decomposition, specialization, and explicit roles; otherwise, single agent suffices (AutoGen, CrewAI).
18. What does "maximum capability" mean in practice: speed, quality, autonomy, throughput, or organizational leverage?
    - Note: Balance of quality, reliability, and leverage through orchestration, not just speed or autonomy (sources on trade-offs).

## Provisional Hypotheses

These are working theses to test during research. They are not yet validated conclusions.

- Most gains come from better decomposition, retrieval, tool use, and verification, not from adding more free-form conversation. (Validated: Supported by tool-mediated patterns and verification emphasis.)
- Multi-agent systems help most when roles, boundaries, and handoffs are explicit. (Validated: Matches orchestration patterns from AutoGen and CrewAI.)
- In domain-specific application, objective external checks are more valuable than agent self-confidence. (Validated: Reinforced by verification-first manifesto implications.)
- The scarcest resource is not tokens but trustworthy attention: what the system chooses to keep, surface, and verify. (Validated: Aligns with attention to verification and audit trails.)
- Agent orchestration should be designed around artifacts and checkpoints, not personalities. (Validated: Consistent with artifact-centered design in sources.)

## Cycle 01 Question Delta

- Answered this cycle: 1, 2, 4, 6, 10, 12.
- Remain partial: 3, 5, 7, 8, 9, 11, 13, 14, 15, 16, 17, 18.
- New questions added: 19, 20, 21.

## Cycle 02 Question Delta

- Newly tracked this cycle: 19, 20, 21 moved from open to `partial` with defined protocols.
- Strengthened but still partial: 3, 8, 9, 11, 13, 16.
- Held answered: 12 (now with explicit comparison protocol).
- New questions added: 22, 23.

