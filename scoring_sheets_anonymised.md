# TOPSIS Scoring Sheets — Anonymised Evaluator Data

**Study:** Closed-loop Human-AI Decision Support for Bio-inspired Architectural Concept Generation  
**Manuscript:** Under review at *The Visual Computer*

---

## 1. Evaluation Setup

- **Number of evaluators:** 12
- **Evaluator pool:** Architecture and design professionals (n = 7) and design-informed researchers (n = 5)
- **Blinding:** Evaluators received proposals labelled Proposal A / B / C (randomised); they were not informed which generation condition (weighted vs. unweighted vs. baseline) produced which proposal
- **Scale:** 7-point anchored scale (1 = very poor, 7 = excellent) per criterion
- **Instrument:** See `scoring_protocol.md` for full criterion definitions and scale anchors

---

## 2. Inter-rater Reliability

Intraclass Correlation Coefficients (ICC, two-way mixed, absolute agreement) were computed per criterion:

| Criterion | ICC | 95% CI | Interpretation |
|-----------|-----|--------|----------------|
| B1 — Morphological Similarity | 0.82 | [0.71, 0.90] | Good |
| B2 — Environmental Integration | 0.78 | [0.65, 0.87] | Good |
| B3 — Structural Rationality | 0.86 | [0.77, 0.92] | Good–Excellent |
| B4 — Visual Novelty | 0.74 | [0.60, 0.85] | Good |
| B5 — Cultural Narrative | 0.76 | [0.62, 0.86] | Good |
| B6 — Interactivity | 0.71 | [0.56, 0.83] | Good |
| B7 — Sustainability | 0.79 | [0.66, 0.88] | Good |

All ICC values exceed the 0.70 threshold for acceptable inter-rater reliability.

---

## 3. Eagle Case Study — Anonymised Score Matrix

Proposal codes: **A** = Scheme 1 (full KANO-AHP-TOPSIS guided), **B** = Scheme 2 (unweighted prompts), **C** = Scheme 3 (no-prompt baseline)  
*(Proposal-scheme correspondence was revealed only after all evaluations were complete)*

### B1 — Morphological Similarity (Eagle)

| Evaluator | Proposal A | Proposal B | Proposal C |
|-----------|-----------|-----------|-----------|
| E01 | 6 | 5 | 3 |
| E02 | 7 | 5 | 4 |
| E03 | 6 | 4 | 3 |
| E04 | 6 | 5 | 3 |
| E05 | 7 | 6 | 4 |
| E06 | 5 | 5 | 3 |
| E07 | 6 | 4 | 2 |
| E08 | 6 | 5 | 4 |
| E09 | 7 | 5 | 3 |
| E10 | 6 | 4 | 3 |
| E11 | 6 | 5 | 3 |
| E12 | 7 | 5 | 4 |
| **Mean** | **6.25** | **4.83** | **3.25** |
| **SD** | **0.62** | **0.58** | **0.62** |

### B2 — Environmental Integration (Eagle)

| Evaluator | Proposal A | Proposal B | Proposal C |
|-----------|-----------|-----------|-----------|
| E01 | 5 | 4 | 3 |
| E02 | 6 | 4 | 3 |
| E03 | 5 | 5 | 3 |
| E04 | 6 | 4 | 4 |
| E05 | 6 | 5 | 3 |
| E06 | 5 | 4 | 3 |
| E07 | 6 | 4 | 2 |
| E08 | 5 | 5 | 4 |
| E09 | 6 | 4 | 3 |
| E10 | 5 | 5 | 3 |
| E11 | 6 | 4 | 3 |
| E12 | 6 | 4 | 3 |
| **Mean** | **5.58** | **4.33** | **3.08** |
| **SD** | **0.51** | **0.49** | **0.51** |

### B3 — Structural Rationality (Eagle)

| Evaluator | Proposal A | Proposal B | Proposal C |
|-----------|-----------|-----------|-----------|
| E01–E12 mean | **5.42** | **4.08** | **3.33** |
| SD | **0.67** | **0.79** | **0.65** |

*(Full per-evaluator data for B3–B7 available upon request; summary statistics reported here for brevity)*

### Aggregate Mean Scores (Eagle)

| Criterion | Weight | Proposal A | Proposal B | Proposal C |
|-----------|--------|-----------|-----------|-----------|
| B1 Morphological Similarity | 0.312 | 6.25 | 4.83 | 3.25 |
| B2 Environmental Integration | 0.198 | 5.58 | 4.33 | 3.08 |
| B3 Structural Rationality | 0.176 | 5.42 | 4.08 | 3.33 |
| B4 Visual Novelty | 0.134 | 5.17 | 4.50 | 3.83 |
| B5 Cultural Narrative | 0.089 | 4.83 | 3.75 | 3.17 |
| B6 Interactivity | 0.057 | 4.58 | 3.92 | 3.42 |
| B7 Sustainability | 0.034 | 4.42 | 3.83 | 3.25 |

---

## 4. Manta Ray Case Study — Aggregate Mean Scores

| Criterion | Weight | Proposal A | Proposal B | Proposal C |
|-----------|--------|-----------|-----------|-----------|
| B1 Morphological Similarity | 0.312 | 6.08 | 4.67 | 3.42 |
| B2 Environmental Integration | 0.198 | 5.75 | 4.42 | 3.17 |
| B3 Structural Rationality | 0.176 | 5.17 | 4.25 | 3.58 |
| B4 Visual Novelty | 0.134 | 5.33 | 4.58 | 3.92 |
| B5 Cultural Narrative | 0.089 | 4.67 | 3.92 | 3.08 |
| B6 Interactivity | 0.057 | 4.75 | 4.08 | 3.58 |
| B7 Sustainability | 0.034 | 4.83 | 4.17 | 3.33 |

---

## 5. Cheetah Case Study — Aggregate Mean Scores

| Criterion | Weight | Proposal A | Proposal B | Proposal C |
|-----------|--------|-----------|-----------|-----------|
| B1 Morphological Similarity | 0.312 | 5.92 | 4.58 | 3.17 |
| B2 Environmental Integration | 0.198 | 5.42 | 4.17 | 3.42 |
| B3 Structural Rationality | 0.176 | 5.58 | 4.33 | 3.25 |
| B4 Visual Novelty | 0.134 | 5.67 | 4.75 | 3.75 |
| B5 Cultural Narrative | 0.089 | 4.42 | 3.67 | 3.33 |
| B6 Interactivity | 0.057 | 4.33 | 3.75 | 3.17 |
| B7 Sustainability | 0.034 | 4.17 | 3.58 | 3.08 |

---

## 6. Data Availability Note

Evaluators provided informed consent for anonymised aggregate reporting. Individual evaluator scores are identified only by codes E01–E12 with no personally identifying information. Complete per-evaluator, per-criterion raw data for all three case studies are available from the corresponding author upon reasonable request.
