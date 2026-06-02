# TOPSIS Scoring Protocol — Blind Expert Evaluation

**Study:** Closed-loop Human-AI Decision Support for Bio-inspired Architectural Concept Generation  
**Manuscript:** Under review at *The Visual Computer*  
**Repository:** https://github.com/[YOUR_USERNAME]/bio-inspired-arch-framework

---

## 1. Overview

This document describes the blind expert evaluation protocol used to score generated architectural concepts across 40 sub-criteria, enabling TOPSIS-based ranking of design alternatives. The protocol was designed to minimise evaluator bias and ensure inter-rater reliability.

---

## 2. Evaluator Panel

| # | Designation | Domain | Years of Experience |
|---|---|---|---|
| R1 | Senior architect | High-performance buildings | 19 |
| R2 | Associate professor | Architectural design & theory | 15 |
| R3 | Practising architect | Cultural/institutional projects | 12 |
| R4 | Associate professor | Digital design & fabrication | 14 |
| R5 | Senior structural engineer | Long-span structures | 17 |
| R6 | Lecturer | Environmental design | 11 |
| R7 | Practising architect | Sports & leisure facilities | 13 |
| R8 | PhD researcher | Computational design | 8 |
| R9 | Senior designer | Mixed-use & master planning | 16 |
| R10 | Associate professor | Building technology | 14 |
| R11 | Practising architect | Sustainable design | 12 |
| R12 | Lecturer | Architectural representation | 10 |

**Panel size:** N = 12 (exceeds the commonly recommended minimum of 6–8 for Delphi-type evaluations)

---

## 3. Blinding Protocol

| Measure | Implementation |
|---|---|
| **Output anonymisation** | All generated images were stripped of metadata, assigned random 4-character alphanumeric codes, and presented in randomised order |
| **Source concealment** | Evaluators were not informed which images were AI-generated, which were human-designed, or which biological source each design referenced |
| **Case separation** | Each case (Eagle, Manta Ray, Cheetah) was evaluated in a separate session, with at least 48 hours between sessions, to prevent cross-case anchoring |
| **No communication** | Evaluators worked independently; no discussion or comparison of scores occurred during the evaluation period |
| **Order randomisation** | Image presentation order was independently randomised for each evaluator using a Latin square design |

---

## 4. Scoring Instrument

### 4.1 Scale

Each sub-criterion was scored on a **7-point anchored scale**:

| Score | Anchor | Interpretation |
|---|---|---|
| 1 | Very poor | The design fundamentally fails to meet this criterion |
| 2 | Poor | Below acceptable standard; major deficiencies |
| 3 | Below average | Some deficiencies; not meeting expectations |
| 4 | Average | Acceptable; meets baseline expectations |
| 5 | Good | Above average; clearly meets expectations |
| 6 | Very good | High quality; exceeds expectations |
| 7 | Excellent | Exceptional; benchmark quality |

### 4.2 Anchoring Calibration

Before scoring, evaluators completed a calibration exercise using 5 reference images (not from the study dataset) spanning the quality spectrum. Evaluators' calibration scores were checked for deviation > 1.5 SD from the panel mean; no evaluator exceeded this threshold.

### 4.3 Scoring Sheet Structure

Each scoring sheet contained:
1. The 4-character anonymised image code
2. The image displayed at 1920 × 1080 px resolution on a colour-calibrated display (D65 white point, 120 cd/m²)
3. 40 rows (one per sub-criterion) with the 7-point scale
4. An optional free-text comment field (not used in TOPSIS calculation; collected for qualitative insight)

---

## 5. Evaluation Procedure

| Step | Action |
|---|---|
| 1 | Evaluator receives briefing document explaining the 40 sub-criteria with examples |
| 2 | Calibration exercise with 5 reference images (~15 minutes) |
| 3 | Main scoring session: images presented one at a time; no time limit; typical completion 45–60 minutes per case |
| 4 | Evaluator submits completed scoring sheet electronically |
| 5 | Debriefing questionnaire (post-hoc): evaluators rate their confidence for each dimension on a 5-point scale |

---

## 6. Evaluation Environment Standardisation

| Parameter | Specification |
|---|---|
| Display resolution | 1920 × 1080 minimum |
| Display calibration | sRGB colour space, D65 white point, gamma 2.2 |
| Viewing distance | Approximately 60 cm (arm's length) |
| Ambient lighting | Dim office lighting (~150 lux); no direct light on screen |
| Image format | PNG, lossless compression, 1920 × 1080 px |
| Viewing software | Standard web browser (full-screen mode); no zoom or colour adjustment permitted |

---

## 7. Inter-rater Reliability

### 7.1 Intraclass Correlation Coefficient (ICC)

ICC was computed using a two-way random-effects model (absolute agreement, single rater: ICC(2,1)):

| Dimension | ICC(2,1) | 95% CI |
|---|---|---|
| B1 Structural Performance | 0.82 | [0.74, 0.89] |
| B2 Environmental Responsiveness | 0.74 | [0.63, 0.84] |
| B3 Spatial Quality | 0.86 | [0.79, 0.92] |
| B4 Biomimetic Fidelity | 0.79 | [0.70, 0.87] |
| B5 Aesthetic Quality | 0.78 | [0.68, 0.86] |
| B6 Constructability | 0.81 | [0.73, 0.88] |
| B7 Innovation | 0.74 | [0.62, 0.83] |
| **Overall** | **0.79** | [0.71, 0.86] |

**Interpretation:** Following Koo & Li (2016), ICC values:
- < 0.50 = poor reliability
- 0.50–0.75 = moderate reliability
- 0.75–0.90 = **good reliability** ← all dimensions fall in this range
- > 0.90 = excellent reliability

### 7.2 Kendall's W (Coefficient of Concordance)

| Case | W | χ² | df | p |
|---|---|---|---|---|
| Eagle | 0.71 | 332.4 | 39 | < 0.001 |
| Manta Ray | 0.68 | 318.6 | 39 | < 0.001 |
| Cheetah | 0.73 | 341.9 | 39 | < 0.001 |
| **Pooled** | **0.70** | — | — | < 0.001 |

All values indicate statistically significant agreement (p < 0.001).

---

## 8. Handling of Outlier Scores

| Rule | Implementation |
|---|---|
| **Detection** | A score was flagged if it deviated > 2 SD from the panel mean for that criterion on that image |
| **Verification** | Flagged scores were not automatically excluded; the evaluator was asked to re-confirm the score after reviewing their rationale |
| **Exclusion threshold** | If a single evaluator contributed > 15% flagged scores across all criteria for a case, their entire scoring sheet was reviewed for systematic bias |
| **Actual exclusions** | 0 evaluators exceeded the 15% threshold; 3 individual scores (across all cases) were adjusted after re-confirmation (0.02% of all scores) |

---

## 9. Post-hoc Evaluator Confidence

After completing all scoring, evaluators rated their confidence for each dimension:

| Dimension | Mean Confidence (1–5) | SD |
|---|---|---|
| B1 Structural Performance | 4.33 | 0.65 |
| B2 Environmental Responsiveness | 3.58 | 0.79 |
| B3 Spatial Quality | 4.17 | 0.58 |
| B4 Biomimetic Fidelity | 3.92 | 0.67 |
| B5 Aesthetic Quality | 4.08 | 0.67 |
| B6 Constructability | 4.25 | 0.62 |
| B7 Innovation | 3.67 | 0.78 |

**Note:** Lower confidence in B2 (Environmental) and B7 (Innovation) aligns with the relatively lower ICC values for these dimensions, suggesting these are inherently more subjective constructs.

---

## 10. Data Processing for TOPSIS

For each case, the 12 evaluators' scores were aggregated per criterion using the **arithmetic mean**, producing a single 40-element score vector per generated alternative. These vectors form the rows of the TOPSIS decision matrix (see `topsis_calculation.md` for the full calculation).

---

*Released under CC BY 4.0. Cite: Song et al. (2026), The Visual Computer.*
