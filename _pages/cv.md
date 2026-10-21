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
  * Co-advisor: Prof. Chengwei Qin
  * Passed the Ph.D. Qualifying Examination (PQE), Aug. 2026
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
  <ul>{% for post in site.publications reversed %}{% if post.category == 'conferences' %}
    {% include archive-single-cv.html %}
  {% endif %}{% endfor %}</ul>

Manuscripts under Review
======
  <ul>{% for post in site.publications reversed %}{% if post.category == 'manuscripts' %}
    {% include archive-single-cv.html %}
  {% endif %}{% endfor %}</ul>

Ongoing Research
======
* **Multimodal process reward models** (targeting ACL 2027): a paired-image diagnostic benchmark that tests whether PRM step scores follow the image facts that decide each step.
* **Game world models:** what it takes for pretrained video models to obey game mechanics when a program harness supplies the rules.
* **Survey:** expanding my PQE survey, *From Visual Chain-of-Thought to Verifiable Visual-Thinking Agents*, into an ACM Computing Surveys submission.

Projects
======
* **Construction-Site Safety-Hazard VLM** (Guangdong Heavy Industry, Industry Collaboration), 2025 – Present — *Lead*
  * Fine-tuned Qwen3.6-27B, deployed for the partner on a single-GPU FP8 server and on the partner's Ascend NPU service. On 1,156 independent test scenes, strict top-1 accuracy rose from 24.9% (base model) to 45.9%, while a Qwen3-VL-235B teacher reached 27.4%; the evaluation was rebuilt for deployment validity. [Details](/portfolio/1-construction-safety-vlm/)
* **RedDust — Long-Horizon LLM-Agent Benchmark** (open source), 2026
  * A 30-day survival-shelter benchmark scored as a non-compensatory profile. In a preliminary cross-model panel, agents with matched short-horizon social skill still split on long-horizon consistency. [Details](/portfolio/2-reddust/) · [Code](https://github.com/peter-cui-yi/RedDust)

Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Skills
======
* **Research areas:** VLM/MLLM · Multimodal Evaluation &amp; Benchmarking · Process Reward Models / Verifiable Reasoning · LLM-Agent Evaluation · Data-Centric AI
* **Training &amp; deployment:** Full-parameter SFT · LoRA / PEFT · Knowledge Distillation · Contrastive Learning · Distributed Training (multi-GPU) · FP8 Inference Serving
* **Programming:** Python · C++ · Java · TypeScript
* **Frameworks/Tools:** PyTorch · ms-swift · LLaMA-Factory · vLLM · React/Phaser · MATLAB

Languages
======
* English (Fluent — 6 years of study in the U.S.)
* Chinese (Mandarin, Native)
