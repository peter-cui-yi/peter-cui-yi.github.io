---
permalink: /
title: "Yi Cui (崔屹)"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a Ph.D. candidate in Artificial Intelligence at the **Hong Kong University of Science and Technology (Guangzhou)**, advised by [Prof. Hui Xiong](https://scholar.google.com/citations?user=HHWV_OUAAAAJ) (Founding Head of the AI Thrust; Fellow of ACM, IEEE, AAAS, AAAI, CAAI) and co-advised by Prof. Chengwei Qin. Before HKUST-GZ, I received an M.S. in Computer Engineering from **New York University** and a B.S. in Computer Science (minor in Economics) from **Pennsylvania State University**.

My research builds toward **trustworthy, process-level verification of multimodal and agentic systems**. Starting from benchmark construction that exposes how i.i.d. evaluation overstates real-deployment reliability ([SafeBuild-Bench](/publication/2026-safebuild-bench), KDD&nbsp;2026), I moved to the verification layer itself: **GLANCE** predicts, from the original image alone, whether a vision–language model will follow an edit to the answer-relevant region, and my current process-reward-model work asks whether step scores track the image facts that decide each step. I am also studying what it takes for pretrained video world models to obey game rules, and expanding my PQE survey, from visual chain-of-thought to verifiable visual-thinking agents, into an ACM Computing Surveys submission.

## Research Interests

- Vision-Language Models (VLM / MLLM)
- Multimodal Evaluation &amp; Benchmarking
- Process Reward Models / Verifiable Reasoning
- Trustworthy &amp; Agentic AI
- Data-Centric AI

## News

- **2026** — *Change the Image, Change the Answer?* (GLANCE) is under review at **ICLR 2027**.
- **2026** — Passed the Ph.D. Qualifying Examination (PQE).
- **2026** — *SafeBuild-Bench* accepted to **ACM SIGKDD 2026** (Datasets &amp; Benchmarks Track).
- **2025** — *Beyond Boundaries* (Source-Free Object Detection) accepted to **AAAI 2026**.
- **2024** — Started my Ph.D. in AI at HKUST (Guangzhou) with Prof. Hui Xiong.

## Selected Publications

- **SafeBuild-Bench: A Temporal-Robust Construction Safety Benchmark with Graph-Enhanced Data Mining.** <br> <u>Yi Cui</u>†, Zilin Wang†, et al. **ACM SIGKDD 2026** (Datasets &amp; Benchmarks). [[arXiv]](https://arxiv.org/abs/2608.00068)
- **Change the Image, Change the Answer? Predicting VLM Responses to Regional Edits.** <br> <u>Yi Cui</u>, Yili Wang, Zilin Wang, Huizai Yao, Chengwei Qin, Hui Xiong. Under review, **ICLR 2027**. <br> <small>GLANCE, a training-free three-view score computed on the original image only, ranks edit-following above preservation at AUROC 0.71–0.83 across six Visual7W model cohorts.</small>

## Ongoing Research

- **Multimodal process reward models** (targeting **ACL 2027**) — a paired-image diagnostic benchmark that tests whether PRM step scores follow the image facts that decide each step: the step's text stays fixed while an image edit flips its truth.
- **Game world models** — using a program harness so that pretrained video models generate game video that obeys game mechanics, and measuring how much input, training data, and verification an event needs when it runs against the model's visual prior.
- **Survey** — expanding my PQE survey, *From Visual Chain-of-Thought to Verifiable Visual-Thinking Agents*, into an ACM Computing Surveys submission.

## Projects

- [Construction-Site Safety-Hazard VLM](/portfolio/1-construction-safety-vlm/) — a fine-tuned VLM deployed with an industry partner (Guangdong Heavy Industry).
- [RedDust](/portfolio/2-reddust/) — an open-source 30-day benchmark of long-horizon LLM-agent accountability.

See the full list on the [Publications](/publications/) page, or download my [CV (PDF)](/files/Yi_Cui_CV.pdf).
