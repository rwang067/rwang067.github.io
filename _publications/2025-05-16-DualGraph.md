---
title: "DualGuard: A Parameter Space Transformation Approach for Bidirectional Defense in Split-Based LLM Fine-Tuning."
collection: publications
permalink: /publication/2025-05-16-DualGuard
excerpt: 'This paper is about a bidirectional defense mechanism tailored for split- based LLM-FT scenarios.'
date: 2025-05-16
venue: 'ACL'
# paperurl: 'https://XXX'
citation: 'Zihan Liu, Yizhen Wang, Rui Wang, Sai Wu, "DualGuard: A Parameter Space Transformation Approach for Bidirectional Defense in Split-Based LLM Fine-Tuning." the 63rd Annual Meeting of the Association for Computational Linguistics (ACL 2025), Vienna, Austria, July 27 to August 1st, 2025.'
---

Integrating split learning with large language model fine-tuning (LLM-FT) enables secure collaboration between a trusted local client and a well-equipped remote server, but it is vulnerable to data reconstruction attacks (DRAs) that exploit transmitted activations and gradients. Current defense methods, like adding noise to activations or gradients, often sacrifice task-specific model performance under strict privacy constraints. This paper introduces DualGuard, a bidirectional defense mechanism against DRAs for split-based LLM-FT. DualGuard proposes a local warm-up parameter space transformation to alter client-side model parameters before training, using multi-task learning to strike a balance between privacy protection and model performance. Additionally, a global fine-tuning parameter space retention strategy prevents the model from reverting to vulnerable states during formal fine-tuning. Experiments show that DualGuard outperforms current defense methods against various DRAs, while maintaining task performance. Our code will be made publicly available.

