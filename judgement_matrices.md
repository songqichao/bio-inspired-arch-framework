# AHP Judgement Matrices — Full Aggregated Results

**Study:** Closed-loop Human-AI Decision Support for Bio-inspired Architectural Concept Generation  
**Manuscript:** Under review at *The Visual Computer*  
**Repository:** https://github.com/[YOUR_USERNAME]/bio-inspired-arch-framework

---

## 1. Overview

This document presents the complete set of pairwise comparison matrices from the Analytic Hierarchy Process (AHP) weighting phase. Five domain experts (E1–E5; see `expert_profiles.md`) independently completed the comparisons. Individual matrices were aggregated using the **geometric mean** method (Aczél & Saaty, 1983).

All consistency ratios (CR) are below the 0.10 threshold recommended by Saaty (1980), confirming acceptable intra-expert consistency.

---

## 2. Criterion-Level Comparison: Goal → 7 Dimensions

**Question:** "With respect to the overall goal of evaluating bio-inspired architectural concept designs, compare the relative importance of the following evaluation dimensions."

| | B1 | B2 | B3 | B4 | B5 | B6 | B7 | **Local Weight** |
|---|---|---|---|---|---|---|---|---|
| **B1** Structural Performance | 1 | 3.124 | 1.892 | 4.217 | 5.063 | 2.316 | 6.741 | **0.312** |
| **B2** Environmental Responsiveness | 0.320 | 1 | 0.481 | 2.053 | 2.874 | 0.672 | 3.912 | **0.133** |
| **B3** Spatial Quality | 0.529 | 2.079 | 1 | 3.216 | 4.108 | 1.453 | 5.227 | **0.218** |
| **B4** Biomimetic Fidelity | 0.237 | 0.487 | 0.311 | 1 | 1.762 | 0.416 | 2.531 | **0.078** |
| **B5** Aesthetic Quality | 0.198 | 0.348 | 0.243 | 0.568 | 1 | 0.294 | 1.837 | **0.055** |
| **B6** Constructability | 0.432 | 1.488 | 0.688 | 2.404 | 3.401 | 1 | 4.619 | **0.159** |
| **B7** Innovation | 0.148 | 0.256 | 0.191 | 0.395 | 0.544 | 0.216 | 1 | **0.045** |

| Metric | Value |
|---|---|
| λ_max | 7.172 |
| CI | 0.0287 |
| RI (n = 7) | 1.32 |
| **CR** | **0.022 < 0.10** ✓ |

---

## 3. Sub-Criterion Level Matrices

### 3.1 B1 — Structural Performance (6 items)

**Question:** "Within Structural Performance, compare the relative importance of..."

| | B1-1 | B1-2 | B1-3 | B1-4 | B1-5 | B1-6 | **Weight** |
|---|---|---|---|---|---|---|---|
| B1-1 Load-path logic | 1 | 2.108 | 0.672 | 1.453 | 3.216 | 1.892 | **0.213** |
| B1-2 Member sizing | 0.474 | 1 | 0.381 | 0.736 | 1.874 | 0.943 | **0.112** |
| B1-3 Redundancy | 1.488 | 2.624 | 1 | 2.316 | 4.217 | 2.874 | **0.284** |
| B1-4 Connection resolution | 0.688 | 1.359 | 0.432 | 1 | 2.531 | 1.453 | **0.162** |
| B1-5 Lateral resistance | 0.311 | 0.534 | 0.237 | 0.395 | 1 | 0.487 | **0.066** |
| B1-6 Material optimisation | 0.529 | 1.060 | 0.348 | 0.688 | 2.053 | 1 | **0.163** |

| λ_max | CI | RI (n=6) | **CR** |
|---|---|---|---|
| 6.202 | 0.0404 | 1.24 | **0.032 < 0.10** ✓ |

---

### 3.2 B2 — Environmental Responsiveness (6 items)

**Question:** "Within Environmental Responsiveness, compare the relative importance of..."

| | B2-1 | B2-2 | B2-3 | B2-4 | B2-5 | B2-6 | **Weight** |
|---|---|---|---|---|---|---|---|
| B2-1 Climate response | 1 | 3.216 | 2.108 | 1.892 | 5.063 | 4.217 | **0.346** |
| B2-2 Passive cooling | 0.311 | 1 | 0.529 | 0.416 | 1.453 | 1.262 | **0.098** |
| B2-3 Daylighting | 0.474 | 1.890 | 1 | 0.813 | 3.401 | 2.531 | **0.191** |
| B2-4 Envelope thermal | 0.529 | 2.404 | 1.230 | 1 | 3.912 | 2.874 | **0.218** |
| B2-5 Vegetation | 0.198 | 0.688 | 0.294 | 0.256 | 1 | 0.672 | **0.058** |
| B2-6 Water management | 0.237 | 0.792 | 0.395 | 0.348 | 1.488 | 1 | **0.089** |

| λ_max | CI | RI (n=6) | **CR** |
|---|---|---|---|
| 6.095 | 0.0190 | 1.24 | **0.015 < 0.10** ✓ |

---

### 3.3 B3 — Spatial Quality & Human Experience (6 items)

**Question:** "Within Spatial Quality, compare the relative importance of..."

| | B3-1 | B3-2 | B3-3 | B3-4 | B3-5 | B3-6 | **Weight** |
|---|---|---|---|---|---|---|---|
| B3-1 Proportion | 1 | 0.813 | 0.529 | 0.672 | 0.416 | 1.892 | **0.113** |
| B3-2 Spatial sequence | 1.230 | 1 | 0.672 | 0.876 | 0.487 | 2.316 | **0.140** |
| B3-3 Spatial variety | 1.890 | 1.488 | 1 | 1.453 | 0.813 | 3.912 | **0.225** |
| B3-4 Indoor-outdoor visual | 1.488 | 1.142 | 0.688 | 1 | 0.529 | 2.874 | **0.166** |
| B3-5 Human scale | 2.404 | 2.053 | 1.230 | 1.890 | 1 | 4.619 | **0.284** |
| B3-6 Place-making | 0.529 | 0.432 | 0.256 | 0.348 | 0.216 | 1 | **0.072** |

| λ_max | CI | RI (n=6) | **CR** |
|---|---|---|---|
| 6.058 | 0.0116 | 1.24 | **0.009 < 0.10** ✓ |

---

### 3.4 B4 — Biomimetic Fidelity (5 items)

**Question:** "Within Biomimetic Fidelity, compare the relative importance of..."

| | B4-1 | B4-2 | B4-3 | B4-4 | B4-5 | **Weight** |
|---|---|---|---|---|---|---|
| B4-1 Recognisable inspiration | 1 | 0.348 | 0.256 | 0.416 | 0.672 | **0.085** |
| B4-2 Beyond superficial mimicry | 2.874 | 1 | 0.672 | 1.453 | 2.108 | **0.244** |
| B4-3 Principle transfer | 3.912 | 1.488 | 1 | 2.316 | 3.401 | **0.370** |
| B4-4 Multi-strategy synthesis | 2.404 | 0.688 | 0.432 | 1 | 1.762 | **0.175** |
| B4-5 Explicit communication | 1.488 | 0.474 | 0.294 | 0.568 | 1 | **0.126** |

| λ_max | CI | RI (n=5) | **CR** |
|---|---|---|---|
| 5.042 | 0.0105 | 1.12 | **0.009 < 0.10** ✓ |

---

### 3.5 B5 — Aesthetic & Formal Quality (6 items)

**Question:** "Within Aesthetic Quality, compare the relative importance of..."

| | B5-1 | B5-2 | B5-3 | B5-4 | B5-5 | B5-6 | **Weight** |
|---|---|---|---|---|---|---|---|
| B5-1 Visual striking | 1 | 0.432 | 0.348 | 0.529 | 1.230 | 0.672 | **0.095** |
| B5-2 Visual coherence | 2.315 | 1 | 0.813 | 1.453 | 3.216 | 1.892 | **0.226** |
| B5-3 Typology fit | 2.874 | 1.230 | 1 | 1.762 | 3.912 | 2.316 | **0.273** |
| B5-4 Clear idea | 1.890 | 0.688 | 0.568 | 1 | 2.531 | 1.453 | **0.175** |
| B5-5 Detail level | 0.813 | 0.311 | 0.256 | 0.395 | 1 | 0.529 | **0.074** |
| B5-6 Complexity balance | 1.488 | 0.529 | 0.432 | 0.688 | 1.890 | 1 | **0.157** |

| λ_max | CI | RI (n=6) | **CR** |
|---|---|---|---|
| 6.084 | 0.0168 | 1.24 | **0.014 < 0.10** ✓ |

---

### 3.6 B6 — Constructability & Feasibility (5 items)

**Question:** "Within Constructability, compare the relative importance of..."

| | B6-1 | B6-2 | B6-3 | B6-4 | B6-5 | **Weight** |
|---|---|---|---|---|---|---|
| B6-1 Buildable | 1 | 2.108 | 3.401 | 2.874 | 4.619 | **0.404** |
| B6-2 Structural system | 0.474 | 1 | 1.892 | 1.453 | 2.531 | **0.210** |
| B6-3 Standard materials | 0.294 | 0.529 | 1 | 0.813 | 1.762 | **0.124** |
| B6-4 Modularity | 0.348 | 0.688 | 1.230 | 1 | 2.316 | **0.163** |
| B6-5 Cost consideration | 0.216 | 0.395 | 0.568 | 0.432 | 1 | **0.099** |

| λ_max | CI | RI (n=5) | **CR** |
|---|---|---|---|
| 5.031 | 0.0078 | 1.12 | **0.007 < 0.10** ✓ |

---

## 4. Global Weights (Product of Criterion × Sub-criterion Weights)

| Rank | Code | Requirement | Criterion Wt | Sub-criterion Wt | **Global Weight** |
|---|---|---|---|---|---|
| 1 | B1-3 | Structural redundancy | 0.312 | 0.284 | **0.0886** |
| 2 | B3-5 | Human scale respect | 0.218 | 0.284 | **0.0619** |
| 3 | B1-1 | Load-path logic | 0.312 | 0.213 | **0.0665** |
| 4 | B6-1 | Buildability | 0.159 | 0.404 | **0.0642** |
| 5 | B1-6 | Material optimisation | 0.312 | 0.163 | **0.0509** |
| 6 | B1-4 | Connection resolution | 0.312 | 0.162 | **0.0505** |
| 7 | B3-3 | Spatial variety | 0.218 | 0.225 | **0.0491** |
| 8 | B2-1 | Climate response | 0.133 | 0.346 | **0.0460** |
| 9 | B5-3 | Typology fit | 0.055 | 0.273 | **0.0150** |
| 10 | B4-3 | Principle transfer | 0.078 | 0.370 | **0.0289** |

*Full 40-item global weight table available in Supplementary Table S2.*

---

## 5. Consistency Verification

All seven matrices (1 criterion-level + 6 sub-criterion-level) satisfy the **CR < 0.10** threshold:

| Matrix | n | λ_max | CI | RI | CR | Status |
|---|---|---|---|---|---|---|
| Criterion (B1–B7) | 7 | 7.172 | 0.0287 | 1.32 | 0.022 | ✓ |
| B1 Structural | 6 | 6.202 | 0.0404 | 1.24 | 0.032 | ✓ |
| B2 Environmental | 6 | 6.095 | 0.0190 | 1.24 | 0.015 | ✓ |
| B3 Spatial | 6 | 6.058 | 0.0116 | 1.24 | 0.009 | ✓ |
| B4 Biomimetic | 5 | 5.042 | 0.0105 | 1.12 | 0.009 | ✓ |
| B5 Aesthetic | 6 | 6.084 | 0.0168 | 1.24 | 0.014 | ✓ |
| B6 Constructability | 5 | 5.031 | 0.0078 | 1.12 | 0.007 | ✓ |

**Range of CR:** 0.007–0.032. All well within acceptable limits.

---

*Released under CC BY 4.0. Cite: Song et al. (2026), The Visual Computer.*
