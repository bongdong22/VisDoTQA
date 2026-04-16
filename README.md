# VisDoT : Enhancing Visual Reasoning through Human-Like Interpretation Grounding and Decomposition of Thought

This repository hosts the public **VisDoTQA** test set for chart-focused visual reasoning research.

## Overview

VisDoTQA is organized around four core tasks:

- `Position`
- `Length`
- `Pattern`
- `Extract`

The released test set contains **1,120** samples with the following task distribution:

- `Position`: 350
- `Length`: 240
- `Pattern`: 267
- `Extract`: 263

## Data Release

This release includes:

- `data/VisDoTQA.json`
- `data/images/`

Each record in `data/VisDoTQA.json` contains:

- `imgname`
- `query`
- `label`
- `source`

The `source` field follows the VisDoTQA task taxonomy:

- `Position`
- `Length`
- `Pattern`
- `Extract`

Explanation fields from the internal source data are intentionally excluded from this public release.

## Repository Layout

```text
VisDoTQA/
├── README.md
└── data/
    ├── VisDoTQA.json
    └── images/
```

## Paper

You can find our paper at the following links:

- [ACL Anthology](https://aclanthology.org/2026.findings-eacl.30/)
- [arXiv](https://arxiv.org/abs/2509.18395)

## Citation

If you use this dataset in your research, please cite our paper:

```bibtex
@inproceedings{lee2026visdot,
  title={VisDoT: Enhancing Visual Reasoning through Human-Like Interpretation Grounding and Decomposition of Thought},
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
