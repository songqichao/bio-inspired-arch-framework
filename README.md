# Closed-loop Human-AI Decision Support for Bio-inspired Architectural Concept Generation

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![DOI](https://img.shields.io/badge/DOI-待Zenodo注册-blue.svg)](#citation)

**Repository for the manuscript under review at *The Visual Computer***  
Submission ID: 43b03e05

---

## Overview

This repository contains the supplementary materials, data, and reproducibility resources for the paper:

> Song Q., Zhang Y., et al. "Closed-loop Human-AI Decision Support for Bio-inspired Architectural Concept Generation: Integrating KANO, AHP, TOPSIS, and Diffusion Models." Under review at *The Visual Computer*, 2026.

The study proposes a closed-loop framework that integrates:
- **KANO model** — user requirement elicitation and classification
- **Analytic Hierarchy Process (AHP)** — multi-criteria weight derivation
- **Technique for Order Preference by Similarity to Ideal Solution (TOPSIS)** — quantitative evaluation of generated alternatives
- **Diffusion-based image generation** — AI-driven biomimetic architectural concept visualisation

Three biomimetic case studies are presented: Eagle (aviation museum), Manta Ray (aquatic centre), and Cheetah (sports complex).

---

## Repository Structure

```
.
├── README.md                           ← This file
├── CITATION.cff                         ← Citation metadata
├── LICENSE                              ← CC BY 4.0
├── questionnaire/
│   ├── KANO_questionnaire.md            ← Full 40-item KANO questionnaire
│   ├── sampling_protocol.md             ← Distribution & screening (318→282)
│   └── response_coding_guide.md         ← KANO classification matrix & reliability
├── ahp/
│   ├── expert_profiles.md               ← 5 anonymised expert backgrounds
│   ├── judgement_matrices.md            ← 7 pairwise matrices with CR values
│   └── sensitivity_analysis.md          ← ±20% weight perturbation analysis
├── prompts/
│   ├── prompt_templates.md              ← Weight-to-prompt conversion & examples
│   ├── generation_parameters.md         ← CFG, steps, seed records
│   └── failure_cases.md                 ← 4 failure categories with examples
└── topsis/
    ├── scoring_protocol.md              ← Blind evaluation protocol & ICC
    ├── scoring_sheets_anonymised.md     ← Raw evaluator scores (Eagle case)
    ├── topsis_calculation.md            ← Full 6-step TOPSIS matrix calculation
    └── ablation_results.md              ← 4-condition ablation data
```

---

## Data Availability

- **KANO raw responses:** Aggregated frequency tables and classification results are provided in `questionnaire/`. Anonymised individual-level data available upon reasonable request to the corresponding author (participant consent restricts public posting of raw responses).
- **AHP matrices:** Complete expert-aggregated pairwise comparison matrices in `ahp/`.
- **TOPSIS scores:** Full scoring sheets for the Eagle case in `topsis/`; Manta Ray and Cheetah data available upon request.
- **Generated images:** Available upon request (file size constraints prevent direct repository inclusion).

---

## Reproducibility

All methodological parameters are fully documented:
- KANO classification: Berger et al. (1993) matrix; dominant category by frequency with M>O>A>I tie-breaking
- AHP: Geometric mean aggregation (Aczél & Saaty, 1983); CR < 0.10 for all matrices
- TOPSIS: Vector normalisation; AHP-weighted; 12 blinded evaluators; ICC(2,1) ≥ 0.74
- Image generation: Stable Diffusion XL; CFG = 7.5; 50 steps; 5 seeds per prompt

---

## Citation

If you use this repository in your research, please cite:

```bibtex
@article{song2026closed,
  title={Closed-loop Human-AI Decision Support for Bio-inspired Architectural Concept Generation:
         Integrating KANO, AHP, TOPSIS, and Diffusion Models},
  author={Song, Qichao and Zhang, Yanqiu and others},
  journal={The Visual Computer},
  year={2026},
  note={Under review},
  doi={待Zenodo注册后更新}
}
```

A DOI will be assigned via **Zenodo** upon acceptance/publication. For now, please cite using the repository URL.

---

## License

This repository is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0). You are free to share and adapt the material for any purpose, provided you give appropriate credit.

---

## Contact

For questions about the data or methodology, please contact the corresponding author via the journal's submission system (Submission ID: 43b03e05).

---

*Last updated: June 2026*
