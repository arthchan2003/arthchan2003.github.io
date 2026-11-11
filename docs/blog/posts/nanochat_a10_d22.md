---
date: 2026-07-28
title: Notes on nanochat training with an A10 (Depth <= 22)
description: Personal notes on training nanochat up to depth 22 on a single A10 GPU — results, observations, and what the numbers actually mean.
categories:
  - LLM
  - Training
---

## 1. Context

## 2. Review of GPT-2, nanochat, and nanochat's Innovations

## 3. Why Dataset Matters

## 4. My A10 Runs (From depth=2 to depth=22)

### 4.1 Results

## 5. Scaling Law

## 6. Chatting with nanochat

## 7. Conclusion and Future Work

## 8. References

Similar posts / related reading:

- [Reproducing Karpathy's NanoChat on a Single GPU](https://limcheekin.medium.com/reproducing-karpathys-nanochat-on-a-single-gpu-step-by-step-with-ai-tools-e9420aaee912) — Lim Chee Kin, Medium
- [Reproducing nanochat in a homelab](https://github.com/karpathy/nanochat/discussions/710) — GitHub discussion #710 (DGX Spark / 2×GB10)
- [nanochat on RTX 3060, depth=10](https://github.com/karpathy/nanochat/discussions/176) — GitHub discussion #176
- [Running nanochat on low resource infrastructure (RTX 3080+)](https://github.com/karpathy/nanochat/discussions/231) — GitHub discussion #231
- [nanochat on RTX 4070 Ti Super, depth=20, CORE=0.2087](https://github.com/karpathy/nanochat/discussions/250) — GitHub discussion #250
- [Jan 7 2026 nanochat miniseries v1](https://github.com/karpathy/nanochat/discussions/420) — Karpathy's own writeup
- [nanochat Tutorial: Train Your Own LLM for $100](https://byteiota.com/nanochat-karpathy-llm-100-dollars/) — byteiota.com
- [Karpathy's Autoresearch: AI That Improves Its Own Training](https://www.analyticsvidhya.com/blog/2026/03/nanochat-gpt-2-training/) — Analytics Vidhya
- [Which H100 instance to train Nanochat](https://bluenotebook.io/blog/h100-nanochat-training/) — bluenotebook.io
- [Training nanochat on DGX Spark](https://objectgraph.com/blog/nanochat-dgx-spark/) — objectgraph.com (Matt Langston)
- [nanochat](https://simonwillison.net/2025/Oct/13/nanochat/) — Simon Willison

## Appendix: 2080 Runs
