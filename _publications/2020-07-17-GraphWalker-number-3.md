---
title: "GraphWalker: An I/O-Efficient and Resource-Friendly Graph Analytic System for Fast and Scalable Random Walks."
collection: publications
permalink: /publication/2020-07-17-GraphWalker-number-3
excerpt: 'This paper is about the number 3. The number 4 is left for future work.'
date: 2020-7-17
venue: 'ATC 2020'
paperurl: 'https://www.usenix.org/conference/atc20/presentation/wang-rui'
citation: 'Rui Wang, Yongkun Li, Hong Xie, Yinlong Xu, and John CS Lui. "GraphWalker: An I/O-Efficient and Resource-Friendly Graph Analytic System for Fast and Scalable Random Walks." In 2020 USENIX Annual Technical Conference (USENIX ATC 20), pp. 559-571. 2020.'
---

Traditional graph systems mainly use the iteration-based model which iteratively loads graph blocks into memory for analysis so as to reduce random I/Os. However, this iterationbased model limits the efficiency and scalability of running random walk, which is a fundamental technique to analyze large graphs. In this paper, we propose GraphWalker, an I/O-efficient graph system for random walks by deploying a novel state-aware I/O model with asynchronous walk updating. GraphWalker is efficient to handle very large diskresident graphs consisting of hundreds of billions of edges with only a single commodity machine, and it is also scalable to run tens of billions of random walks with thousands of steps long. Experiments on our prototype system show that GraphWalker can achieve more than an order of magnitude speedup when running a large amount of long random walks when compared with DrunkardMob, which is tailored for random walk based on the classical system GraphChi, as well as two state-of-the-art single-machine graph systems, Graphene and GraFSoft. Furthermore, comparing with the most recent distributed system KnightKing, which optimizes for random walks and runs on cluster machines, GraphWalker achieves comparable performance with only a single machine, thereby making it a more cost-effective alternative.
