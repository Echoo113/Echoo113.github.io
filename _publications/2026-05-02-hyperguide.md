---
title: "HyperGuide: Hyperbolic Guidance for Efficient Multi-Step Reasoning in Large Language Models"
collection: publications
category: preprints
permalink: /publication/2026-hyperguide
date: 2026-05-22
venue: "arXiv:2605.24140"
paperurl: "https://arxiv.org/abs/2605.24140"
codeurl: "https://github.com/yuyuliu11037/HyperGuide"
excerpt: "HyperGuide distills reasoning progress into a hyperbolic geometric signal that guides step-by-step LLM generation, yielding consistent gains especially on deeper reasoning chains."
authors: "Yuyu Liu, Haotian Xu, Yanan He, Sarang Rajendra Patil, Mengjia Xu, Tengfei Ma"
---

\[[Paper](https://arxiv.org/abs/2605.24140)\] \[[Code](https://github.com/yuyuliu11037/HyperGuide)\]

### Abstract (Brief Summary)

Multi-step reasoning remains a central challenge for large language models: single-pass generation is efficient but lacks accuracy; tree-search methods explore multiple paths but are computation-heavy. HyperGuide addresses this gap by distilling reasoning progress into a hyperbolic geometric signal that guides step-by-step generation. The key insight is structural: in combinatorial reasoning trees, solution-bearing states are few while dead ends are exponentially numerous — hyperbolic space matches this asymmetry naturally, with distance-to-origin encoding solution proximity and angular separation distinguishing branches. A lightweight head projects LLM hidden states into this space, and a low-rank adapter is fine-tuned to act on the injected signal. Across multiple benchmarks, HyperGuide yields consistent gains, with larger improvements on deeper reasoning chains.

### Main Contributions

- **Hyperbolic Geometry as Reasoning Signal:** Exploits the exponential capacity of hyperbolic space to encode solution proximity and branch structure in reasoning trees.
- **Lightweight Architecture:** A small projection head + LoRA adapter — no expensive tree search or verifier models required.
- **Scalable Gains:** Improvements grow with reasoning chain depth, making HyperGuide especially effective on hard, multi-step problems.
