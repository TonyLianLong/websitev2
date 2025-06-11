---
title: "Describe Anything: Detailed Localized Image and Video Captioning"
collection: publications
excerpt: 'Describe Anything Model (DAM) generates detailed descriptions for user-specified regions in images and videos, marked by points, boxes, scribbles, or masks. We introduce DLC-Bench to evaluate such region-based descriptions.'
date: 2025-04-22
paper_url: 'https://arxiv.org/abs/2504.16072'
project_page_url: 'https://describe-anything.github.io/'
demo_url: 'https://huggingface.co/spaces/nvidia/describe-anything-model-demo'
code_url: 'https://github.com/NVlabs/describe-anything'
bibtex_url: 'https://describe-anything.github.io/#citation'
authors: '**Long Lian**, Yifan Ding, Yunhao Ge, Sifei Liu, Hanzi Mao, Boyi Li, Marco Pavone, Ming-Yu Liu, Trevor Darrell, Adam Yala, Yin Cui'
citation:
cover_image: 2025-04-22-DescribeAnything.jpg
---
Generating detailed and accurate descriptions for specific regions in images and videos remains a fundamental challenge for vision-language models. We introduce the Describe Anything Model (DAM), a model designed for detailed localized captioning (DLC). DAM preserves both local details and global context through two key innovations: a focal prompt, which ensures high-resolution encoding of targeted regions, and a localized vision backbone, which integrates precise localization with its broader context. To tackle the scarcity of high-quality DLC data, we propose a Semi-supervised learning (SSL)-based Data Pipeline (DLC-SDP). DLC-SDP starts with existing segmentation datasets and expands to unlabeled web images using SSL. We introduce DLC-Bench, a benchmark designed to evaluate DLC without relying on reference captions. DAM sets new state-of-the-art on 7 benchmarks spanning keyword-level, phrase-level, and detailed multi-sentence localized image and video captioning.
