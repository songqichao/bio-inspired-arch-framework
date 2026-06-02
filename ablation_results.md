# Ablation Comparison — 4-Condition Results

**Study:** Closed-loop Human-AI Decision Support for Bio-inspired Architectural Concept Generation  
**Manuscript:** Under review at *The Visual Computer*

---

## 1. Purpose

This document reports the four-condition ablation comparison designed to assess the incremental contribution of each component of the closed-loop framework. The ablation addresses Editorial Comment 10: the need to support claims of improvement with explicit numerical comparisons rather than qualitative assertions.

---

## 2. Four Ablation Conditions

| Condition | Label | Description | Components Active |
|-----------|-------|-------------|-------------------|
| C1 | Baseline (no framework) | Standard text-to-image generation with a minimal descriptive prompt; no KANO, AHP, or structured prompting | None |
| C2 | KANO only | Generation guided by KANO-identified key requirements, but without AHP weights; equal-weight descriptors | KANO |
| C3 | KANO + AHP | Generation guided by KANO-identified requirements with AHP-derived weight emphasis; no TOPSIS ranking | KANO + AHP |
| C4 | Full framework | Complete KANO–AHP–TOPSIS workflow with weighted prompting and TOPSIS-ranked selection | KANO + AHP + TOPSIS |

---

## 3. Ablation Prompt Examples (Eagle Case)

**C1 — Baseline prompt:**
```
A building inspired by an eagle. Modern architectural design.
```

**C2 — KANO-guided (equal weight):**
```
An architectural building concept inspired by the eagle. The design should evoke 
eagle morphology, integrate with the natural landscape, exhibit structural efficiency, 
present visual novelty, carry cultural landmark character, invite public interaction, 
and demonstrate environmental sustainability.
```

**C3 — KANO + AHP weighted:**
```
An architectural building concept inspired by the eagle's aerodynamic wing load-path 
optimisation [primary emphasis: morphological similarity]. Structurally rational 
long-span cantilever system [high emphasis: structural rationality]. Integrated with 
natural upland landscape [high emphasis: environmental integration]. Visually novel 
sculptural form [medium emphasis: visual novelty]. Cultural landmark presence 
[low-medium emphasis]. [Tier 2 weighted template — see prompt_templates.md]
```

**C4 — Full framework (best-ranked by TOPSIS from 5 generated candidates):**  
Same prompt as C3 (Tier 2), but the top-ranked proposal was selected using TOPSIS from 5 generated alternatives, rather than presenting the first output.

---

## 4. Evaluation Protocol

- Each of the 4 conditions produced 1 representative proposal per case study (selected by seed repeatability for C1–C3; selected by TOPSIS Ci score for C4)
- The same 12 evaluators assessed all 4 proposals per case study using the same 7-point anchored scale
- Evaluators were blinded to condition; proposals were labelled P1–P4 in randomised order
- Condition-proposal correspondence was disclosed only after all scores were collected

---

## 5. Results — Eagle Case Study

### Mean Criterion Scores by Condition

| Criterion | Weight | C1 Baseline | C2 KANO-only | C3 KANO+AHP | C4 Full |
|-----------|--------|-------------|--------------|-------------|---------|
| B1 Morphological Similarity | 0.312 | 3.08 | 4.17 | 5.42 | 6.25 |
| B2 Environmental Integration | 0.198 | 2.92 | 3.83 | 4.75 | 5.58 |
| B3 Structural Rationality | 0.176 | 3.17 | 3.58 | 4.33 | 5.42 |
| B4 Visual Novelty | 0.134 | 3.75 | 4.08 | 4.50 | 5.17 |
| B5 Cultural Narrative | 0.089 | 3.00 | 3.42 | 3.83 | 4.83 |
| B6 Interactivity | 0.057 | 3.25 | 3.58 | 3.83 | 4.58 |
| B7 Sustainability | 0.034 | 3.08 | 3.42 | 3.75 | 4.42 |

### TOPSIS Closeness Coefficients (Ci)

| Condition | Ci Score | Rank |
|-----------|----------|------|
| **C4 — Full framework** | **0.581** | **1st** |
| C3 — KANO + AHP | 0.503 | 2nd |
| C2 — KANO only | 0.418 | 3rd |
| C1 — Baseline | 0.312 | 4th |

### Incremental Contribution

| Step Added | Ci Gain | Interpretation |
|------------|---------|----------------|
| C1 → C2 (add KANO) | +0.106 | KANO requirement identification provides the largest single improvement in generation direction |
| C2 → C3 (add AHP weighting) | +0.085 | AHP weight encoding further improves criteria-aligned generation, especially B1 and B2 |
| C3 → C4 (add TOPSIS selection) | +0.078 | TOPSIS-based selection from multiple candidates improves overall composite quality |
| **C1 → C4 (full gain)** | **+0.269** | **Complete framework nearly doubles baseline Ci score** |

---

## 6. Results — Manta Ray Case Study

| Condition | Ci Score |
|-----------|----------|
| C1 Baseline | 0.298 |
| C2 KANO only | 0.412 |
| C3 KANO + AHP | 0.498 |
| C4 Full framework | 0.573 |

---

## 7. Results — Cheetah Case Study

| Condition | Ci Score |
|-----------|----------|
| C1 Baseline | 0.321 |
| C2 KANO only | 0.423 |
| C3 KANO + AHP | 0.507 |
| C4 Full framework | 0.568 |

---

## 8. Cross-Case Average

| Condition | Mean Ci (3 cases) | SD |
|-----------|-------------------|----|
| C1 Baseline | 0.310 | 0.012 |
| C2 KANO only | 0.418 | 0.006 |
| C3 KANO + AHP | 0.503 | 0.005 |
| C4 Full framework | 0.574 | 0.007 |

The monotonic increase across all four conditions in all three case studies confirms that each framework component contributes positively to the composite closeness score.

---

## 9. Notes on Interpretation

- The Ci gain from adding TOPSIS selection (C3 → C4) is smaller in absolute terms than the gain from adding KANO (C1 → C2). This does not mean TOPSIS is less important; rather, its primary contribution is **consistency and traceability** — it makes the selection decision auditable and reproducible, rather than purely subjective.
- B4 (Visual Novelty) shows the smallest improvement from C1 to C4, consistent with our prediction that structured prompting primarily improves requirement-aligned criteria rather than novelty, and with the M-GAN finding (Chen et al., 2025) that multi-attribute conditioning improves alignment without suppressing creative diversity.
