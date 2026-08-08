---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<a href="/files/Yi_Cui_CV.pdf" class="btn btn--info">Download CV (PDF)</a> &nbsp; <a href="/files/Yi_Cui_CV_CN.pdf">中文版</a>

Education
======
* Ph.D. in Artificial Intelligence, **The Hong Kong University of Science and Technology (Guangzhou)**, 2024 – Present
  * Advisor: Prof. Hui Xiong (Founding Head of AI Thrust; Fellow of ACM, IEEE, AAAS, AAAI, CAAI)
* M.S. in Computer Engineering, **New York University**, 2024
* B.S. in Computer Science (Minor in Economics), **Pennsylvania State University**, 2021

Research Interests
======
* Vision-Language Models (VLM / MLLM)
* Multimodal Evaluation &amp; Benchmarking
* Process Reward Models / Verifiable Reasoning
* Trustworthy &amp; Agentic AI; Data-Centric AI

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Projects
======
* **Construction-Site Safety-Hazard VLM** (Guangdong Heavy Industry, Industry Collaboration), 2025 – Present — *Lead*
  * Pilot VLM that flags safety hazards, cites the violated regulation, and drafts rectification advice; ~35% relative accuracy gain over baseline (internal validation). Qwen3-VL student (LoRA) distilled from a Qwen3-VL-235B-A22B teacher; GEMS data selection; decoupled Agentic RAG (in design).

*RedDust now appears under Publications above (paper in preparation); see the [project page](/portfolio/2-reddust/) for the engine and evaluation design.*

Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Skills
======
* **Research areas:** VLM/MLLM · Multimodal Evaluation &amp; Benchmarking · Process Reward Models / Verifiable Reasoning · Data-Centric AI
* **Training &amp; methods:** LoRA / PEFT · Knowledge Distillation · Contrastive Learning · Distributed Training (multi-GPU) · Agentic RAG
* **Programming:** Python · C++ · Java
* **Frameworks/Tools:** PyTorch · MATLAB · React/Phaser · TypeScript · vLLM · LLaMA-Factory

Languages
======
* English (Fluent — 6 years of study in the U.S.)
* Chinese (Mandarin, Native)
