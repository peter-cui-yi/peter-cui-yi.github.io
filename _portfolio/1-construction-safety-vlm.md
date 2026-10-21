---
title: "Construction-Site Safety-Hazard VLM"
excerpt: "Industry collaboration (Guangdong Heavy Industry). A fine-tuned Qwen3.6-27B that flags safety hazards in construction-site inspection photos, deployed for the partner, with an evaluation rebuilt for deployment validity.<br/>Qwen3.6-27B · Full-parameter SFT + LoRA · ms-swift · vLLM FP8 · Ascend NPU"
collection: portfolio
---

*2025 – Present · Guangdong Heavy Industry, Industry Collaboration · Role: Lead*

A VLM that flags safety hazards in construction-site inspection photos. I lead the modeling, data, and evaluation work. The model is deployed for the industry partner, on a single-GPU FP8 server and on the partner's Ascend NPU service.

- **Fine-tuning, and the decision to drop distillation.** I fine-tuned Qwen3.6-27B on 100K+ inspection images labeled under an expert-revised 231-class hazard taxonomy. Across all 1,156 independent test scenes, strict top-1 accuracy rose from 24.9% (base model) to **45.9%**, while a Qwen3-VL-235B teacher reached only 27.4%. The task hinges on the partner's own labeling conventions, so I dropped the planned teacher distillation.
- **A prompt fix instead of retraining.** A weak top-3 score traced back to the training data: only 0.15% of samples carried more than one label, so the model learned to report one hazard per image. Requiring exactly three candidates in the prompt raised top-3 accuracy from 38.3% to **58.1%** with no retraining.
- **Evaluation built for deployment validity.** I sample by inspection scene instead of by image (10,173 test images were only 1,156 scenes), removed test photos duplicated in training via content hashing (~10%), and ran two rounds of expert audits that put image–description mismatch at 10–19%. Every reported accuracy names the subset it was measured on.
- **Serving.** Online FP8 quantization in vLLM on one NVIDIA L20 showed no measurable accuracy loss (top-3 65.8% vs. 64.6% in BF16, within noise). The partner's Ascend deployment matched internal evaluation (top-3 60.0% vs. 60.1% on 750 validation images).

**Stack:** Qwen3.6-27B · Full-parameter SFT + LoRA (ms-swift) · vLLM (FP8) · Ascend NPU deployment · Expert-in-the-loop data audits
