---
category: Exemplar-based
path: ''
title: 'Text Generation with Exemplar-based Adaptive Decoding'
pdf: 'https://www.aclweb.org/anthology/N19-1263'
bibtex: https://www.aclweb.org/anthology/papers/N/N19/N19-1263.bib
appendix: https://www.aclweb.org/anthology/attachments/N19-1263.Supplementary.pdf
type: 'NAACL 2019'
layout: nil
---

### Goal
fluency (abstractive) + controlled, realiability (exemplar-based)

### Idea
*exemplar-based adaptive decoding*: use exemplars to inform the decoding procedure

### Method 
- reparameterize the decoder's parameters with weighted linear sums
- decoder parameter P = sum(w_i * P_i), where P_i is a predifined parameters matrices. 
- based on examples, you compute w_i
- Reduce Parameters: p_i = u_i * v_i (d^2 -> 2d)

### Contributions
- First to propose exemplar-based adaptive decoding
- evaluated on summarization, data-to-text tasks and showed strong performance

### Limitations
- No direct learning on how to pick right example (possibly using RL?)
- They only use only one example as a reference