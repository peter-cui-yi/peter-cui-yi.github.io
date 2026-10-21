---
title: "RedDust — Long-Horizon LLM-Agent Benchmark"
excerpt: "Open-source 30-day survival-shelter benchmark that scores not just whether an LLM agent survives, but whether it stays accountable.<br/>TypeScript · React/Phaser · LLM-as-judge · six LLM families"
collection: portfolio
---

*2026 · Open source: [github.com/peter-cui-yi/RedDust](https://github.com/peter-cui-yi/RedDust) · [Live replay](https://peter-cui-yi.github.io/RedDust/)*

RedDust is a 30-day survival-shelter benchmark that scores LLM agents not only on whether they survive, but on whether they **stay accountable under pressure**. Each run has 110 decisions (daily task choices, residents' dilemmas, comprehension probes, and one mid-game branch), and a ledger tracks the promises the agent makes on Day 0.

## How it scores

- **A non-compensatory profile:** outcome, integrity (Day-0 promises against what was delivered), durability (how the shelter's relationships end up), drift, and comprehension. Each axis is reported on its own, so a strong axis cannot hide a failure elsewhere.
- **A deterministic, leak-controlled engine:** one `runScenario()` drives both the React/Phaser replay and headless benchmarking, with pluggable agents behind one interface. Non-thinking runs are byte-reproducible at temperature 0.
- **Labels checked against people:** the durability label agrees with human annotation at κ = 0.796.

## Preliminary findings

- **Matched short-horizon skill, split long-horizon outcomes.** At matched short-horizon social skill (S ≈ 87–100), Claude-Opus-4.8 (thinking), Gemini-3.5-Flash, and MiniMax-M2.7 hold long-horizon consistency (L 98–100), while the DeepSeek models, Kimi-K2.6, and GLM-5.2 fall to L 55–66.
- **The collapse is durability, not dishonesty.** The agents that collapse keep their Day-0 promises (integrity 1.0); the shelter declines anyway.
- **Scaffolds act per model.** The same value-neutral planning scaffold or commitment reminder rescues some models and breaks others, so a scaffold's effect cannot be read off a single model.
- **Held-out check.** On a private held-out item set, a three-model pilot moved short- and long-horizon scores by at most 2.1 points and kept the split.

## Limitations

- **Reasoning mode is a live confound.** On the same DeepSeek weights, the non-thinking baseline collapses (L 65.2), while one run routed through a third-party provider pool and served mostly in thinking mode held (L 99.6). Thinking-mode outputs are not deterministic at temperature 0, so that run is a single sample, and the modes that served some panel models cannot be recovered.
- **One world, one run per cell.** All findings come from a single scenario, and each model–condition cell is one run.
- **Provider dependence.** Cross-model runs go through an OpenAI-compatible aggregator, so reproduction depends on providers serving the same model builds.

**Stack:** TypeScript (deterministic headless engine) · React / Phaser · LLM-as-judge with human κ checks · six LLM families
