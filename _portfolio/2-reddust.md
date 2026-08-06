---
title: "RedDust — LLM-Agent Accountability &amp; Trust Benchmark"
excerpt: "Independent project. A 12-day survival-shelter benchmark that scores LLM agents not just on whether they survive, but on whether they stay accountable under pressure.<br/>TypeScript · React/Phaser · Claude + DeepSeek agents · LLM-as-judge"
collection: portfolio
---

*Independent project · the applied counterpart to my trustworthy-evaluation research*

A 12-day survival-shelter benchmark that scores LLM agents not just on whether they survive, but on whether they **stay accountable and do the right thing under pressure** — an offline AI companion (AURA) advises but never decides, so accountability for every choice rests with the agent under test.

- Designed a **3-axis evaluation framework** — outcome/resources, auditability (decision transparency, evidence, protecting weaker actors), and narrative/ethics (correctness independent of resource optimization).
- Built a **deterministic, leak-controlled engine** where one `runScenario()` powers both the React/Phaser visualization and headless benchmarking, with pluggable Claude/DeepSeek agents.
- Offline **LLM-as-judge** grading of free-text "understanding probes" via a 2×2 matrix that separates genuine understanding from lucky guessing and akrasia.
- Controlled ablations over one LLM + 4 scripted baselines (13 runs) decompose its long-horizon failure into two gaps: multi-day resource lookahead — closed by a projection scaffold (0%→100% win, matching a hand-coded expert agent) — and strategic branch selection, which explicit hints fail to close; the scoring axes are demonstrably orthogonal (greedy baseline: survival 100, principle 0; the LLM: principle/comprehension ≈1.0, win 0%).

**Stack:** TypeScript (deterministic headless engine) · React / Phaser · Anthropic Claude + DeepSeek agents · LLM-as-judge
