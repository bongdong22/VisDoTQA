---
pretty_name: VisDoTQA
language:
  - en
license: unknown
task_categories:
  - visual-question-answering
  - question-answering
size_categories:
  - 1K<n<10K
source_datasets:
  - original
annotations_creators:
  - machine-generated
language_creators:
  - machine-generated
multilinguality:
  - monolingual
tags:
  - chart
  - chart-understanding
  - multimodal
  - vision-language
  - reasoning
  - synthetic
  - benchmark
---

# VisDoTQA: Enhancing Visual Reasoning through Human-Like Interpretation Grounding and Decomposition of Thought

This repository releases **VisDoTQA**, the public benchmark introduced in our paper [*VisDoT : Enhancing Visual Reasoning through Human-Like Interpretation Grounding and Decomposition of Thought*](https://aclanthology.org/2026.findings-eacl.30/).

The canonical publication record is the **ACL Anthology** page for **Findings of the Association for Computational Linguistics: EACL 2026**, and an additional mirror is available on **arXiv:2603.11631**.  
See our [GitHub repository](https://github.com/bongdong22/VisDoTQA) for the synchronized source release and updates.  
See the paper on [ACL Anthology](https://aclanthology.org/2026.findings-eacl.30/), on [arXiv:2603.11631](https://arxiv.org/abs/2603.11631), or via [DOI](https://doi.org/10.18653/v1/2026.findings-eacl.30).

## Highlights

- We release **VisDoTQA**, a public benchmark for evaluating **visual grounding** and **compositional reasoning** on chart images.
- The benchmark contains **1,120 QA pairs** built from **609 held-out charts**.
- VisDoTQA covers four perceptual task families: **Position**, **Length**, **Pattern**, and **Extract**.
- This Hugging Face repository releases the **public benchmark test split only**. The full research dataset described in the paper contains **331,969 QA pairs** and is not included here.

## Dataset Structure

- **Split**: `test`
- **Images**: `test/images/`
- **Metadata**: `test/metadata.jsonl`

Each example contains:

- `file_name`: relative path to the chart image
- `imgname`: image filename
- `query`: benchmark question
- `label`: ground-truth answer
- `source`: VisDoTQA task category (`Position`, `Length`, `Pattern`, `Extract`)

## Links

- [Paper (ACL Anthology, canonical)](https://aclanthology.org/2026.findings-eacl.30/)
- [Paper (arXiv:2603.11631 mirror)](https://arxiv.org/abs/2603.11631)
- [DOI](https://doi.org/10.18653/v1/2026.findings-eacl.30)
- [GitHub Repository](https://github.com/bongdong22/VisDoTQA)

## Contact

If you have questions about this dataset release, please use the [GitHub repository](https://github.com/bongdong22/VisDoTQA).

## Citation

```bibtex
@inproceedings{lee2026visdot,
  title={VisDoT : Enhancing Visual Reasoning through Human-Like Interpretation Grounding and Decomposition of Thought},
  author={Lee, Eunsoo and Lee, Jeongwoo and Hong, Minki and Choi, Jangho and Kim, Jihie},
  booktitle={Findings of the Association for Computational Linguistics: EACL 2026},
  pages={610--640},
  year={2026},
  doi={10.18653/v1/2026.findings-eacl.30},
  url={https://aclanthology.org/2026.findings-eacl.30/}
}
```
