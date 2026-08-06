---
title: "Construction-Site Safety-Hazard VLM"
excerpt: "Industry collaboration (Guangdong Heavy Industry). A pilot VLM that flags construction-site safety hazards, cites the violated regulation, and drafts rectification advice — ~35% relative accuracy gain over baseline.<br/>Qwen3-VL · LoRA · Knowledge Distillation · GEMS · Agentic RAG · vLLM"
collection: portfolio
---

*2025 – Present · Guangdong Heavy Industry, Industry Collaboration · Role: Lead*

A pilot VLM system that flags construction-site safety hazards, cites the violated regulation, and drafts rectification advice. I led the data pipeline, model adaptation, and evaluation end to end.

- Raised hazard-recognition accuracy by **~35% (relative) over baseline** on the internal validation set across v2–v5 iterations — driven mainly by data-quality refinement (semantic extraction over expert annotations into a sharper hazard taxonomy) and system-prompt engineering (per-category definitions + a fixed output schema).
- Distilled a same-family **Qwen3-VL-235B-A22B teacher into a Qwen3-VL-32B student via LoRA** — the largest student our compute budget supports — using a contrastive teacher process to auto-generate structured "description → hazard → regulation → fix" labels and sharply cut manual labeling cost.
- Curated an expert-reviewed 30K-instance SFT dataset from 100K+ raw inspection records, using **GEMS (graph-enhanced data selection)** to counter severe class long-tail and focus senior-engineer review on high-value data instead of the full corpus; expanded the hazard taxonomy from 62 to 90 classes along the way.
- Designing a decoupled **Agentic RAG** pipeline (in progress) to replace direct VLM generation of regulation citations, targeting traceability and maintainability.

**Stack:** Qwen3-VL · LoRA / PEFT · Knowledge Distillation · Contrastive Labeling · GEMS · LLaMA-Factory · Agentic RAG · vLLM · 8×A6000
