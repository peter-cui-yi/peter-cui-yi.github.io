---
permalink: /
title: "Yi Cui (崔屹)"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a Ph.D. student in Artificial Intelligence at the **Hong Kong University of Science and Technology (Guangzhou)**, advised by [Prof. Hui Xiong](https://scholar.google.com/citations?user=HHWV_OUAAAAJ) (Founding Head of the AI Thrust; Fellow of ACM, IEEE, AAAS, AAAI, CAAI). Before HKUST-GZ, I received an M.S. in Computer Engineering from **New York University** and a B.S. in Computer Science (minor in Economics) from **Pennsylvania State University**.

My research builds toward **trustworthy, process-level verification of multimodal and agentic systems**. Starting from benchmark construction that exposes how i.i.d. evaluation overstates real-deployment reliability ([SafeBuild-Bench](/publications/), KDD&nbsp;2026), I moved to the verification layer itself — diagnosing a hidden *position-prior* confounder that inflates multimodal process-reward scores — and then to **GLANCE**, which separates answers that genuinely use visual evidence from ones that are correct by prior, without training, labels, or edited images. I am now extending accountability evaluation from perception to long-horizon agent behavior (**RedDust**), and mapping 100+ papers from visual chain-of-thought to verifiable reasoning agents into a process-level verification agenda (survey in preparation).

## Research Interests

- Vision-Language Models (VLM / MLLM)
- Multimodal Evaluation &amp; Benchmarking
- Process Reward Models / Verifiable Reasoning
- Trustworthy &amp; Agentic AI
- Data-Centric AI

## News

- **2026** — *SafeBuild-Bench* accepted to **ACM SIGKDD 2026** (Datasets &amp; Benchmarks Track).
- **2026** — *Beyond Boundaries* (Source-Free Object Detection) accepted to **AAAI 2026**.
- **2026** — *Beyond Step AUC* under review at **ACL 2027**; *GLANCE* and *RedDust* in preparation, targeting **ICLR 2027**.
- **2024** — Started my Ph.D. in AI at HKUST (Guangzhou) with Prof. Hui Xiong.

## Selected Publications

- **SafeBuild-Bench: A Temporal-Robust Construction Safety Benchmark with Graph-Enhanced Data Mining.** <br> <u>Yi Cui</u>†, Zilin Wang†, et al. **ACM SIGKDD 2026** (Datasets &amp; Benchmarks).
- **Beyond Step AUC: Hidden Position Priors and Capability Trade-offs in Multimodal Process Reward Models.** <br> <u>Yi Cui</u>, Huizai Yao, Zilin Wang, Zihan Wang, Hui Xiong. Under review, **ACL 2027**. <br> <small>A step-index-only baseline reaches 0.73 AUC on VisualProcessBench while the best trained PRM reaches 0.36 — published rankings are driven by a hidden position prior, not step-verification ability.</small>
- **Grounding or Guessing? A Privileged-Crop Detector of Visual Evidence Use in Multimodal LLMs (GLANCE).** <br> <u>Yi Cui</u>, Hui Xiong. In preparation, targeting **ICLR 2027**. <br> <small>Estimates from an untouched image whether a model used the visual evidence or was merely right by prior — 0.81 AUROC, +0.26 over the strongest region-blind baseline, with no training and no labels.</small>
- **RedDust: Short-Horizon Social Skill Does Not Predict Long-Horizon Consistency in LLM Agents.** <br> <u>Yi Cui</u>, Hui Xiong. In preparation, targeting **ICLR 2027**. <br> <small>A 30-day agent-accountability benchmark: at matched early comprehension, model families split between keeping and breaking their own commitments.</small>

See the full list on the [Publications](/publications/) page, or download my [CV (PDF)](/files/Yi_Cui_CV.pdf).
