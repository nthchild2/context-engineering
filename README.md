# Agent Engineering

`agent-engineering` is a research and development repository for domain-agnostic agentic AI methodology.

## Main Goal

Develop a formal methodology for orchestrating agentic AI at maximum practical capability, then turn that methodology into concrete tools, workflows, and evaluation methods across domains.

## Why This Exists

It is no longer enough to ask whether AI can assist real work. It already does. The harder question is how to organize models, tools, memory, evaluation, and human judgment so the overall system produces better outcomes than either a lone human or an unstructured chat loop.

This repository exists to answer that question seriously.

## Current Direction

The work now runs as a recurring cycle:

1. Intake sources, questions, and validation artifacts.
2. Distill evidence into descriptive observations and normative postulates.
3. Nourish `MANIFESTO.md` with status-labeled postulates.
4. Validate and feed unresolved gaps into the next cycle.

Cycle planning is tracked in `plans/build-methodology-plan.md` and run records live in `research/cycles/`.

`plans/build-methodology-plan.md` is the canonical operating procedure for building and refining the manifesto.

## Working Principles

- Start from first principles and operational constraints.
- Separate what is true from what is aspirational.
- Prefer source-backed claims, experiments, and executable feedback over intuition alone.
- Treat orchestration as a systems design problem, not a prompt-writing trick.
- Build around artifacts, checkpoints, and verification.
- Keep methodology domain-agnostic unless a cycle explicitly declares a domain-specific application pass.
- Iterate on repository instructions as the methodology hardens.

## Repository Structure

- `README.md`: repository purpose, direction, and durable framing.
- `AGENTS.md`: repository rules for coding agents.
- `.github/copilot-instructions.md`: aligned instructions for AI-assisted development tools.
- `research/`: temporary research notes, source collection, and exploratory thinking.
- `plans/`: documented plans for repository development and process steps.
- `research/cycles/`: per-cycle input/output records and next-cycle queues.

## Where To Resume

Use `README.md` as the durable entry point and `research/` as the working area.

- `README.md`: the main goal, current direction, and the durable framing of the repository.
- `research/`: provisional work such as open questions, sources, early theses, and draft postulates.
- `research/questions.md`: the active question backlog.
- `research/sources.md`: the auditable source list.
- `research/cycles/cycle-02.md`: latest cycle run record and open gaps for Cycle 03.

## Near-Term Questions

- What are generative models good at in agentic work?
- What are they bad at or unreliable at?
- Which operating parameters matter most in practice?
- When does multi-agent orchestration outperform a single strong agent?
- Which orchestration patterns actually hold up in real work?
- What should be measured to judge whether an agentic workflow is any good?

## Contribution Standard

Contributions should tighten the methodology, improve the clarity of the repository’s purpose, or advance a concrete tool or workflow that follows from the emerging manifesto.
