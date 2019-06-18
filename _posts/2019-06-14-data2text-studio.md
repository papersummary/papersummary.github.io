---
category: Visualization
path: ''
title: "Data2Text Studio: Automated Text Generation from Structured Data"
pdf: https://www.aclweb.org/anthology/D18-2003
bibtex: https://aclweb.org/anthology/papers/D/D18/D18-2003.bib
demo: http://demo.kcgpu.com:8002/studio/index.html
type: 'EMNLP 2018'
layout: nil
---

### Goal
*Data2Text Studio*: a platform for data-to-text generation systems which improves the interactivity and interpretability of the generated text. 

### Method 
3 components
- Model training: upload data -> extract the templates and corresponding trigger conditions automatically
- Model revision: revise the extracted templates and conditions manually
- Text generation: prview the generated texts of the customized model, and APIs are provided


### Contributions
- Interactivity: can preview the generated texts, call the APIs to generate texts, can train their own models by uploading parallel data
- Interpretability: attributes in generated texts are aligned with inputs
- Proposed Semi-HMM model, which achives better F1, BLEU score compared to a generative model (Liang et al.,2009)

### Limitations
- the baseline they compared with seems to be too weak, but it should be fine as it is not the main contribution of this paper
- it's based on the template-based solution, so large part of interactivity and interpretability cannot be remain intact in neural setting