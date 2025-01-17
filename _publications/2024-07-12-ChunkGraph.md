---
title: "Efficient Large Graph Processing with Chunk-Based Graph Representation Model."
collection: publications
permalink: /publication/2024-07-12-ChunkGraph
excerpt: 'This paper is about an I/O-efficient graph system designed for processing large-scale graphs on NVMe SSDs.'
date: 2024-07-12
venue: 'USENIX ATC'
paperurl: 'https://www.usenix.org/conference/atc24/presentation/wang-rui'
citation: 'Rui Wang, Weixu Zong, Shuibing He, Xinyu Chen, Zhenxin Li, and Zheng Dang "Efficient Large Graph Processing with Chunk-Based Graph Representation Model." USENIX Annual Technical Conference (ATC 2024), Santa Clara, CA, pp.1239-1255, 2024.'
---

Existing external graph processing systems face challenges in terms of low I/O efficiency, expensive computation overhead, and high graph algorithm development costs when running on emerging NVMe SSDs, due to their reliance on complex loading and computing models that aim to convert numerous random I/Os into a few sequential I/Os. While in-memory graph systems working with memory-storage cache systems like OS page cache or TriCache, offer a promising solution for large graph processing with fine-grained I/Os and easy algorithm programming, they often overlook the specific characteristics of graph applications, resulting in inefficient graph processing. To address these challenges, we introduce ChunkGraph, an I/O-efficient graph system designed for processing large-scale graphs on NVMe SSDs. ChunkGraph introduces a novel chunk-based graph representation model, featuring classified and hierarchical vertex storage, and efficient chunk layout optimization. Evaluations show that ChunkGraph can outperform existing external graph systems, as well as in-memory graph systems relying on general cache systems, running several times faster.
