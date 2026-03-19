# Sources and Evidence Ledger

This file is the intake and evidence layer for the cycle:

`source references -> extracted evidence -> linked questions -> linked postulates`

## Cycle Update Protocol

1. Add/update a source entry (`S##`) with URL and why it matters.
2. Add extracted evidence rows (`E##`) tied to one or more `S##`.
3. Link each `E##` to `Q#` in `research/questions.md`.
4. Link each `E##` to `P#` in `MANIFESTO.md` (or mark `candidate`).

## Source Entries

### Model and provider docs
- `S01` OpenAI GPT-5.1 model page
  - URL: https://platform.openai.com/docs/models/gpt-5.1
  - Why it matters: coding/agentic positioning, context window, output limits, reasoning controls.
- `S02` OpenAI GPT-4.1 model page
  - URL: https://platform.openai.com/docs/models/gpt-4.1
  - Why it matters: contrast case for large-context behavior.
- `S03` OpenAI prompting reliability guide
  - URL: https://platform.openai.com/docs/guides/prompt-engineering/strategies-to-improve-reliability
  - Why it matters: non-determinism and eval guidance.
- `S04` Anthropic context windows
  - URL: https://docs.anthropic.com/en/docs/build-with-claude/context-windows
  - Why it matters: context-as-working-memory and overflow behavior.
- `S05` Anthropic tool use overview
  - URL: https://docs.anthropic.com/en/docs/agents-and-tools/tool-use/overview
  - Why it matters: model intent vs external tool execution boundary.
- `S06` Anthropic reduce hallucinations
  - URL: https://docs.anthropic.com/en/docs/test-and-evaluate/strengthen-guardrails/reduce-hallucinations
  - Why it matters: uncertainty and verification guidance.
- `S07` Anthropic Claude model comparison
  - URL: https://docs.anthropic.com/en/docs/about-claude/models#model-comparison
  - Why it matters: capability/cost context for coding and tool use.
- `S08` xAI Grok models documentation
  - URL: https://docs.x.ai/docs/models
  - Why it matters: alternative model/tooling positioning including search.
- `S09` OpenAI Assistants API overview
  - URL: https://platform.openai.com/docs/assistants/overview
  - Why it matters: agent app pattern with tools and conversation state.

### Orchestration frameworks and papers
- `S10` AutoGen multi-agent framework paper
  - URL: https://www.microsoft.com/en-us/research/publication/autogen-enabling-next-gen-llm-applications-via-multi-agent-conversation-framework/
  - Why it matters: baseline multi-agent composition model.
- `S11` AutoGen v0.4 actor model redesign
  - URL: https://www.microsoft.com/en-us/research/articles/autogen-v0-4-reimagining-the-foundation-of-agentic-ai-for-scale-extensibility-and-robustness/
  - Why it matters: robustness/scalability architecture insights.
- `S12` AutoGen Studio paper
  - URL: https://www.microsoft.com/en-us/research/publication/autogen-studio-a-no-code-developer-tool-for-building-and-debugging-multi-agent-systems/
  - Why it matters: workflow debug/eval as first-class design concerns.
- `S13` LangChain Agents documentation
  - URL: https://python.langchain.com/docs/modules/agents/
  - Why it matters: common tooling patterns for execution loops.
- `S14` CrewAI documentation
  - URL: https://docs.crewai.com/
  - Why it matters: role/handoff oriented multi-agent orchestration.
- `S15` LLM autonomous agents survey
  - URL: https://arxiv.org/abs/2308.11421
  - Why it matters: broad synthesis of architectures and limits.
- `S16` Challenges in Human-Agent Communication
  - URL: https://doi.org/10.48550/arXiv.2412.10380
  - Why it matters: communication and coordination failure modes.

### Evaluation and governance references (Cycle 02)
- `S17` NIST AI Risk Management Framework (AI RMF 1.0)
  - URL: https://www.nist.gov/itl/ai-risk-management-framework
  - Why it matters: domain-neutral guidance for measurable, governed AI risk management.
- `S18` OECD AI Principles
  - URL: https://oecd.ai/en/ai-principles
  - Why it matters: cross-domain requirements for accountability, transparency, and robustness.
- `S19` HELM (Holistic Evaluation of Language Models)
  - URL: https://crfm.stanford.edu/helm/latest/
  - Why it matters: structured evaluation framing beyond single-metric performance claims.
- `S20` ReAct: Synergizing Reasoning and Acting in Language Models
  - URL: https://arxiv.org/abs/2210.03629
  - Why it matters: explicit reasoning + action loop and interaction protocol design.
- `S21` Reflexion: Language Agents with Verbal Reinforcement Learning
  - URL: https://arxiv.org/abs/2303.11366
  - Why it matters: iterative self-critique loop relevant to cycle-level refinement.
- `S22` CRITIC: Large Language Models Can Self-Correct with Tool-Interactive Critiquing
  - URL: https://arxiv.org/abs/2305.11738
  - Why it matters: demonstrates external-tool critique pathways for reliability gains.

## Extracted Evidence (Cycle 01 + Cycle 02)

Use four evidence buckets: `descriptive`, `constraints`, `patterns`, `implications`.

| Evidence ID | Bucket | Evidence statement | Sources | Linked questions | Linked postulates |
| --- | --- | --- | --- | --- | --- |
| E01 | descriptive | LLM outputs are non-deterministic; confidence is not a reliable truth signal. | S03, S06 | Q2, Q13 | P3 |
| E02 | descriptive | Models are stronger at pattern-heavy and tool-mediated tasks than long-horizon reasoning without scaffolds. | S01, S07, S15 | Q1, Q6 | P1, P3 |
| E03 | descriptive | Multi-agent specialization can help, but unclear roles add coordination overhead. | S10, S11, S14 | Q4, Q17 | P4 |
| E04 | constraints | Context acts as working memory and is capacity-limited; overflow degrades behavior. | S04, S01, S02 | Q3, Q9, Q10 | P5, P7 |
| E05 | constraints | Cost and latency rise with larger models, reasoning effort, and extra tool/agent turns. | S01, S04, S07 | Q3, Q14 | candidate |
| E06 | constraints | Persistent memory and audit trails must be externalized into artifacts. | S04, S05, S09 | Q10, Q16 | P5 |
| E07 | patterns | Tool-mediated loop (intent -> tool execution -> feedback) is more auditable than text-only flow. | S05, S09, S13 | Q11, Q12 | P1, P2 |
| E08 | patterns | Explicit role separation and handoff checkpoints improve orchestration reliability. | S10, S12, S14 | Q4, Q15 | P2, P4 |
| E09 | patterns | Human gating is needed for high-risk or high-uncertainty decisions. | S16, S10 | Q8 | candidate |
| E10 | implications | Evaluate with real tasks + benchmarks, not anecdotes alone. | S03, S12, S15 | Q12 | P3 |
| E11 | implications | Failure analysis should separate model, orchestration, and specification causes. | S12, S03, S16 | Q13 | P6 |
| E12 | implications | Design for trustworthy attention: prioritize surfaced, checkable signals over broad context. | S04, S06, S15 | Q9, Q18 | P7 |
| E13 | implications | Promotion criteria should require explicit evidence quality, reproducibility, and scoped applicability. | S17, S18, S19 | Q19 | candidate |
| E14 | implications | Cross-cycle comparability requires a stable metric schema, not ad hoc reporting. | S17, S19 | Q20 | candidate |
| E15 | patterns | Controlled baselines are required to attribute gains to orchestration rather than model variance. | S19, S20 | Q21 | P6 |
| E16 | patterns | Iterative critique loops improve reliability when grounded in external checks. | S21, S22 | Q12, Q13 | P3, P6 |
| E17 | constraints | Governance and risk framing are reusable across domains when expressed as auditable artifacts. | S17, S18 | Q16, Q18 | P2, P5 |
| E18 | patterns | Short reasoning-action cycles with explicit state updates reduce hidden-context drift. | S20, S21 | Q9, Q11 | P1, P7 |

## Provisional Evidence Gaps (for Cycle 03)

- Promotion criteria from `provisional` to `accepted` are now drafted, but still need one executed cycle comparison.
- Cycle metrics schema is drafted, but thresholds are not yet calibrated.
- Controlled baseline protocol is defined, but has not yet been run on two domains.
