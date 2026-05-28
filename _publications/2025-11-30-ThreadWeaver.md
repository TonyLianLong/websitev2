---
title: "ThreadWeaver: Adaptive Threading for Efficient Parallel Reasoning in Language Models"
collection: publications
excerpt: 'ThreadWeaver is a framework for adaptive parallel reasoning that achieves accuracy on par with cutting-edge sequential reasoning models while significantly reducing inference latency. ThreadWeaver utilizes a two-stage parallel trajectory generator, trie-based training-inference co-design, and parallelization-aware reinforcement learning (P-GRPO).'
date: 2025-11-30
selected: true
venue: '*International Conference on Machine Learning* (ICML), 2026 (**Oral**)'
paper_url: 'https://threadweaver-parallel.github.io/assets/paper.pdf'
project_page_url: 'https://threadweaver-parallel.github.io/'
code_url: 'https://github.com/facebookresearch/threadweaver'
bibtex_url: 'https://threadweaver-parallel.github.io/#citation'
authors: '**Long Lian**, Sida Wang, Felix Juefei-Xu, Tsu-Jui Fu, Xiuyu Li, Adam Yala, Trevor Darrell, Alane Suhr, Yuandong Tian, Xi Victoria Lin'
citation:
cover_image: 2025-11-30-ThreadWeaver.gif
---
Scaling inference-time computation boosts LLM reasoning, but sequential decoding results in high latency. ThreadWeaver enables adaptive parallel reasoning that matches sequential accuracy of cutting-edge reasoning models while reducing token latency by up to 1.53×. It uses a two-stage parallel trajectory generator, a trie-based training–inference design compatible with standard inference engines, and parallelization-aware RL (P-GRPO). Across six math benchmarks, it achieves state-of-the-art sequential performance (e.g., 79.9% on AIME24). By spawning and joining concurrent reasoning threads, ThreadWeaver shortens the critical path whenever more compute is available.
