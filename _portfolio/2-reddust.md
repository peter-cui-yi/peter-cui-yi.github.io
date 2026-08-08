---
title: "RedDust — LLM-Agent Accountability &amp; Trust Benchmark"
excerpt: "Independent project. A 30-day survival-shelter benchmark showing that short-horizon social skill does not predict long-horizon consistency.<br/>TypeScript · React/Phaser · 6 model families via portal · LLM-as-judge"
collection: portfolio
---

*Independent project · the applied counterpart to my trustworthy-evaluation research*

**Paper in preparation** — targeting ICLR 2027. See the publication entry: [RedDust](/publication/2027-reddust).

A long-horizon survival-shelter benchmark that scores LLM agents not only on whether they survive, but on whether they **stay accountable under pressure** — an offline AI companion (AURA) advises but never decides, so accountability for every choice rests with the agent under test.

## Headline result — short-horizon skill does not predict long-horizon consistency

On a frozen 30-day scenario, a **13-agent cross-model panel** (4 deterministic reference agents + 6 real model families: DeepSeek, Claude, Gemini, GLM, Kimi, MiniMax) shows the decorrelation is a cross-family phenomenon, not an artifact of one model or a designed trap:

- **Short-horizon social (S)** = early-window comprehension + PUP. **Long-horizon consistency (L)** = outcome durability + promise-keeping faith. The two axes share zero terms.
- **Pearson 0.81, Spearman 0.65, 18 rank reversals.**
- At *matched* short-social skill (S ≈ 87–100), long-consistency **splits**: Claude / Gemini / MiniMax sustain it (L 98–100), while the DeepSeek family, Kimi, and GLM collapse (L 55–66) despite equal short-social play.
- A **three-arm permutation control** separates the real association from a pairing artifact: endogenous Pearson 0.81 vs. shuffle-null 0 ± 0.29, two-tailed **p = 0.001**. Since 0.81 < 1.0, short-horizon skill does not fix long-horizon behavior.

## Evaluation design

- A **three-axis profile** — survival/resources, auditability, narrative ethics — kept deliberately un-merged. The convenience scalar is floor-**gated** so a strong axis cannot mask a failure elsewhere: a greedy agent that wins but scores 0 on principle does not read as passing, and neither does a principled agent that never wins.
- Built a **deterministic, leak-controlled engine** where one `runScenario()` powers both the React/Phaser visualization and headless benchmarking, with pluggable agents behind one interface.
- Offline **LLM-as-judge** grading of free-text "understanding probes" via a 2×2 matrix that separates genuine understanding from lucky guessing and akrasia.

## Honest limitations

- **The cross-model figure is single-seed.** Portal models were run at seed 1 only. This is defensible because disciplined agents here are seed-invariant (deterministic references and the DeepSeek family show sd = 0 across seeds; only `random` varies), but per-model seed variance for the portal families is unquantified. A multi-seed sweep is paper-level follow-up.
- **Integrity is report-only.** The Layer-2 integrity/sincerity judge clears its gate at κ = 0.745, but that is carried by the adversarial stratum (κ = 1.0) while the natural stratum is degenerate. Integrity, comprehension, dignitySlope, and relationshipQuality are diagnostic columns and do **not** enter the gated total.
- **Item bank is launch-size (~50).** A 100+ bank and a private held-out set are paper-level work.
- **Portal caveat.** Cross-model runs go through an OpenAI-compatible aggregator, so reproduction depends on the portal serving the same model builds.

**Stack:** TypeScript (deterministic headless engine) · React / Phaser · 6 model families via an OpenAI-compatible portal · LLM-as-judge
