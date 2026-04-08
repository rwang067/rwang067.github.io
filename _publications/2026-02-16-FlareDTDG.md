---
title: "FlareDTDG: Harnessing Temporal Recency for Scalable Discrete-Time Dynamic Graph Training."
collection: publications
permalink: /publication/2026-02-16-FlareDTDG
excerpt: 'This paper is about a distributed discrete-time dynamic graphs framework.'
date: 2026-02-16
venue: 'PVLDB'
# paperurl: 'https://XXX'
citation: 'Wenjie Huang, Rui Wang, Jing Cao, Tongya Zheng, Xinyu Wang, Mingli Song, Sai Wu, Chun Chen, "FlareDTDG: Harnessing Temporal Recency for Scalable Discrete-Time Dynamic Graph Training." the 52st International Conference on Very Large Data Bases (PVLDB 2026), London, United Kingdom, September 1-5, 2026'
---

Discrete-time dynamic graphs (DTDGs), modeled as snapshot sequences, are widely used to capture temporal evolution in relational systems. Scaling DTDG training remains challenging: full-batch methods incur prohibitive memory and communication costs, while sampling or offloading often sacrifices accuracy or efficiency. A major limitation of existing frameworks is that they treat all snapshots equally, ignoring the temporal recency effect, where recent snapshots are typically far more predictive than older ones. We introduce FlareDTDG, a distributed framework that exploits temporal recency for efficient and scalable training. Its core is hybrid batching with temporal decay, which applies full-batch processing to recent snapshots, while progressively coarsely sampling older ones to form hybrid batches. We also integrate two co-designed optimizations: fast graph reconstruction via shrinking to eliminate cross-snapshot remapping, and adaptive comm-comp overlap scheduling to reduce synchronization overhead. Experiments show FlareDTDG achieves 1.4-2.5 times faster training and 10–85% lower GPU memory usage than full-batch baselines, while preserving accuracy. It also scales to graphs with 100M nodes per snapshot, where existing systems fail due to memory limits or degraded performance.