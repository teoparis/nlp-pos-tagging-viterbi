# Natural Language Processing: Mazzei

University project for the *Tecnologie del Linguaggio Naturale* course, taught by **Prof. Mazzei** at the University of Turin.

## Project: PoS Tagging with Viterbi on Latin and Ancient Greek

Implementation of the **Viterbi algorithm** (based on Hidden Markov Models) for Part-of-Speech tagging on ancient languages.

> Given a sentence, PoS tagging assigns a grammatical tag (noun, verb, adjective, etc.) to each word. The Viterbi algorithm finds the optimal tag sequence using HMM parameters learned from annotated corpora.

## Approach

The project covers the full HMM pipeline:

1. **Modelling**: formal definition of the HMM for PoS tagging
2. **Learning**: estimating the **transition matrix** (tag → tag) and **emission matrix** (tag → word) from the training corpus
3. **Decoding**: Viterbi algorithm to find the most likely tag sequence for new sentences
4. **Smoothing**: handling unseen words/transitions (sparse matrix problem, especially in morphologically rich languages)
5. **Baseline**: most-frequent-tag baseline for comparison

Evaluated separately on **Ancient Greek** (`grc_perseus-ud`) and **Latin** (`la_llct-ud`).

## Dataset

CoNLL-U format corpora from [Universal Dependencies](https://universaldependencies.org/):

| Language | Corpus | Split |
|---|---|---|
| Ancient Greek | Perseus UD | train / dev / test |
| Latin | LLCT UD | train / dev / test |

## Tech Stack

- **Python 3** + **Jupyter Notebook**
- **NumPy** for matrix operations
- CoNLL-U parsing (custom implementation)

## Run

```bash
pip install numpy jupyter
jupyter notebook "pos_tagging_viterbi.ipynb"
```

## Report

A written report is included: `Relazione Parisi Matteo - PoS Tagging per Latino e Greco.pdf`

## Related repos

- [NLP: Radicioni](https://github.com/teoparis/Tecnologie-del-linguaggio-naturale---Radicioni)
- [NLP: Di Caro](https://github.com/teoparis/Tecnologie-del-linguaggio-naturale---Di-Caro)

---

*University project, Tecnologie del Linguaggio Naturale, University of Turin, 2022–2023*
