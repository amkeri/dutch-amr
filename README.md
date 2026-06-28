# Dutch AMR

This repository contains the corpus, parses, and evaluation scripts created and used for the thesis *"Establishing Dutch Abstract Meaning Representation: Annotated Corpus and Fine-tuned Parser"* for the BSc Artificial Intelligence at the Vrije Universiteit Amsterdam.

---

## Repository Structure

```
dutch-amr/
├── corpus/                          
├── evaluation/          
├── guidelines.md        
└── README.md
```

---

## Corpus

Included are the silver Dutch corpus used for parser training and evaluation, the gold Dutch corpus for future Dutch AMR work, and the silver English corpus used for the cross-lingual evaluation. The Dutch corpora consist of **100 manually annotated Dutch sentences**:

- 50 sentences from *De Kleine Prins*
- 50 sentences from the [Four Translations dataset](https://catalog.ldc.upenn.edu/LDC2020T07)

Annotation follows the [AMR guidelines](https://github.com/amrisi/amr-guidelines) with Dutch-specific conventions added. 

---

## Parser

The `parse_xfm_bart_large` from the [amrlib repo](https://github.com/bjascob/amrlib) (v0.8.1) is used as base model, with an **mT5-base** backbone.


⚠️ Due to the size, it is not included in this repository but is available from [HuggingFace](https://huggingface.co/AKerissi/dutch-amr-parser). 

---

## Evaluation

The translate-then-parse approach is evaluated using **XS2match** (developed by [Wein et al.](https://github.com/shirawein/Crossling-AMR-Eval), adjusted to use Dutch and English wiki aligned word vectors files (from [fastText](https://fasttext.cc/docs/en/aligned-vectors.html)). 
