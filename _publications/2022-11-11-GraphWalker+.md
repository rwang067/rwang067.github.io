---
title: "Toward Fast and Scalable Random Walks over Disk-Resident Graphs via Efficient I/O Management."
collection: publications
permalink: /publication/2022-11-11-GraphWalker+
excerpt: 'This paper is about an I/O-efficient out-of-core graph system for random walks.'
date: 2022-11-11
venue: 'ACM TOS'
paperurl: 'https://dl.acm.org/doi/abs/10.1145/3533579'
citation: 'Rui Wang, Yongkun Li, Yinlong Xu, Hong Xie, John C. S. Lui, and Shuibing He. Toward Fast and Scalable Random Walks over Disk-Resident Graphs via Efficient I/O Management. ACM Trans. Storage (ACM TOS) 18, 4, Article 36, 2022, 33 pages.'
---

Traditional graph systems mainly use the iteration-based model, which iteratively loads graph blocks into memory for analysis so as to reduce random I/Os. However, this iteration-based model limits the efficiency and scalability of running random walk, which is a fundamental technique to analyze large graphs. In this article, we first propose a state-aware I/O model to improve the I/O efficiency of running random walk, then we develop a block-centric indexing and buffering scheme for managing walk data, and leverage an asynchronous walk updating strategy to improve random walk efficiency. We implement an I/O-efficient graph system, GraphWalker, which is efficient to handle very large disk-resident graphs and also scalable to run tens of billions of random walks with only a single commodity machine. Experiments show that GraphWalker can achieve more than an order of magnitude speedup when compared with DrunkardMob, which is tailored for random walks based on the classical graph system GraphChi, as well as two state-of-the-art single-machine graph systems, Graphene and GraFSoft. Furthermore, when compared with the most recent distributed system KnightKing, GraphWalker still achieves comparable performance with only a single machine, thereby making it a more cost-effective alternative.
