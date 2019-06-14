---
category: Multiple-steps
path: ''
title: 'Step-by-Step: Separating Planning from Realization in Neural Data-to-Text Generation'
pdf: https://www.aclweb.org/anthology/N19-1236
bibtex: https://www.aclweb.org/anthology/papers/N/N19/N19-1236.bib
appendix: https://www.aclweb.org/anthology/attachments/N19-1236.Supplementary.pdf
code: https://github.com/amitmy/chimera
type: 'NAACL 2019'
layout: nil
---

### Goal
improve reliability and adequacy while maintaining fluent output 

### Idea
Data-to-text -> two steps (text planning + plan realization)

### Method 
- *text planner*: non-nueral, determines the information structure and expresses it into a sequence of ordered trees
- each plan captures 1) the ordering of facts within the sentence, 2) the ordering of entities within a fact 3) the structure between facts that whare an entity
- plan data building: input triplets -> exhaustive generation of plans -> find *matching* plans using ref text
- plan realizer: neural NMT system. 
- eval on WebNLG corpus
<img src="/imgs/step-by-step.png"/>

### Contributions
- proposed adding an explicit symbolic planning component to a neural data-to-text NLG system
- The system performs on par with a strong end-to-end neural system regarding automatic eval metrics, while substantially outperforms regarding faithfulness to the input

### Limitations
- no referring strucutre between sentences (limited fluency)
- no way to decide order between trees (some sentences might be better come before other sentences)

### Comments
- Was interesting to see how coreference resolution can complicate the task and the method.
- has many good references to text planning 