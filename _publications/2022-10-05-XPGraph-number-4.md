---
title: "XPGraph: XPline-Friendly Persistent Memory Graph Stores for Large-Scale Evolving Graphs."
collection: publications
permalink: /publication/2022-02-17-XPGraph-number-4
excerpt: 'This paper is about dynamic graph stores on persistent memory.'
date: 2022-10-05
venue: 'MICRO 2022'
paperurl: 'https://ieeexplore.ieee.org/abstract/document/9923828'
citation: 'Rui Wang, Shuibing He, Weixu Zong, Yongkun Li, and Yinlong Xu. "XPGraph: XPline-friendly persistent memory graph stores for large-scale evolving graphs." In 2022 55th IEEE/ACM International Symposium on Microarchitecture (MICRO), pp. 1308-1325. IEEE, 2022.'
---

Traditional in-memory graph storage systems have limited scalability due to the limited capacity and volatility of DRAM. Emerging persistent memory (PMEM), with large capacity and non-volatility, provides us an opportunity to realize the scalable and high-performance graph stores. However, directly moving existing DRAM-based graph storage systems to PMEM would cause serious PMEM access inefficiency issues, including high read and write amplification in PMEM and costly remote PMEM accesses across NUMA nodes, thus leading to the performance bottleneck. In this paper, we propose XPGraph, a PMEM-based graph storage system for managing large-scale evolving graphs, by developing an XPLine-friendly graph access model with vertex-centric graph buffering, hierarchical vertex buffer managing, and NUMA-friendly graph accessing. Experimental results show that XPGraph achieves 3.01× to 3.95× higher update performance and up to 4.46× higher query performance, compared with the state-of-the-art in-memory graph storage system implemented on a PMEM-based system.
