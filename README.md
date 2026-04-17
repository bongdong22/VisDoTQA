# VisDoTQA

Official public benchmark release for  
**VisDoT : Enhancing Visual Reasoning through Human-Like Interpretation Grounding and Decomposition of Thought**

VisDoTQA is a chart visual reasoning benchmark introduced in *VisDoT : Enhancing Visual Reasoning through Human-Like Interpretation Grounding and Decomposition of Thought*.

Large vision-language models often struggle to reliably ground visual primitives in charts and align them with semantic references. VisDoT addresses this challenge through perception-grounded task design and decomposition-of-thought (DoT) reasoning, and VisDoTQA is introduced as a benchmark for evaluating these capabilities.

## Links

- [Paper (ACL Anthology)](https://aclanthology.org/2026.findings-eacl.30/)
- [Paper (arXiv)](https://arxiv.org/abs/2509.18395)
- [GitHub Repository](https://github.com/bongdong22/VisDoTQA)
- [Hugging Face Dataset](https://huggingface.co/datasets/bongdong/VisDoTQA)

## Overview

VisDoTQA is designed to evaluate **visual grounding** and **compositional reasoning** on chart images through four core task types:

- **Position**
- **Length**
- **Pattern**
- **Extract**

These task families follow the perception-grounded taxonomy introduced in the paper.

## Public Release

This repository releases the **public VisDoTQA test set only**.

The public test set consists of **visually grounded and complex chart questions**, enabling evaluation of both **visual grounding ability** and **compositional reasoning ability**. The questions require models to identify relevant chart elements, interpret perceptual cues, and reason over multiple pieces of visual information.

### Public release statistics

- **1,120** test samples
- **609** held-out charts used to construct the test set

### Task distribution in this release

- **Position**: 350  
  Compare object positions along a common scale.
- **Length**: 240  
  Reason over length-based visual encodings.
- **Pattern**: 267  
  Map visual patterns or category cues to chart elements.
- **Extract**: 263  
  Read explicitly shown values from charts.

## Relation to the Paper Dataset

The full VisDoTQA dataset described in the paper contains **331,969 QA pairs** across the same four perceptual task types. This repository does **not** release the full research dataset; it releases the public benchmark test set only.

## Task Taxonomy

VisDoTQA is organized around four core perceptual task families:

- `Position`  
  Compares object positions along a common scale to determine relative order.
- `Length`  
  Uses length as a perceptual cue for comparing chart elements.
- `Pattern`  
  Links pattern cues to legends and data categories for visual label mapping.
- `Extract`  
  Reads explicitly shown values from charts and evaluates direct numerical recognition.

## Data Release

This release includes:

- `data/VisDoTQA.json`
- `data/test.jsonl`
- `data/images/`

Each record in `data/VisDoTQA.json` contains the following fields:

- `imgname`
- `query`
- `label`
- `source`

The Hugging Face dataset viewer uses `data/test.jsonl`, which contains the same QA rows plus an `image` column for rendering chart images in the table view.

### Field Description

- `imgname`: image filename for the chart instance
- `query`: benchmark question
- `label`: ground-truth answer
- `source`: VisDoTQA task category
- `image`: relative image path used by the Hugging Face dataset viewer

In this public release, the `source` field denotes the **VisDoTQA task category**:

- `Position`
- `Length`
- `Pattern`
- `Extract`

It does **not** denote the original chart source website.

### Public Release Notes

- Explanation fields from the internal research artifact are intentionally excluded from this public release.
- Only evaluation-facing fields required for benchmark use are included.
- Each JSON record is expected to resolve to a matching image file in `data/images/`.

## Repository Layout

```text
VisDoTQA/
├── README.md
├── CITATION.cff
└── data/
    ├── VisDoTQA.json
    ├── test.jsonl
    └── images/
```

## Evaluation

VisDoTQA is evaluated using Relaxed Accuracy (RA), following the evaluation protocol described in the paper.

## Benchmark Context

In the paper, VisDoT is evaluated on ChartQA, ChartQAPro, and VisDoTQA. The reported results show strong gains from combining perception-following supervision with DoT-based reasoning, including a +33.2% improvement on VisDoTQA for the reported InternVL-4B setting.

## Paper

You can find our paper at the following links:

- [ACL Anthology](https://aclanthology.org/2026.findings-eacl.30/)
- [arXiv](https://arxiv.org/abs/2509.18395)

## Citation

If you use this dataset in your research, please cite our paper:

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

## License

License information for this release is pending.
