# Response Coding Guide — KANO Questionnaire

**Study:** Closed-loop Human-AI Decision Support for Bio-inspired Architectural Concept Generation  
**Manuscript:** Under review at *The Visual Computer*  
**Repository:** https://github.com/[YOUR_USERNAME]/bio-inspired-arch-framework

---

## 1. KANO Response Scale

Each KANO item presents two sub-questions:

- **Functional form:** "How do you feel if this feature IS present?"
- **Dysfunctional form:** "How do you feel if this feature IS NOT present?"

Each sub-question uses a 5-point Likert scale:

| Code | Label |
|------|-------|
| 1 | I like it that way |
| 2 | It must be that way (I expect it) |
| 3 | I am neutral |
| 4 | I can live with it that way |
| 5 | I dislike it that way |

---

## 2. KANO Classification Matrix

Cross-tabulating functional (rows) and dysfunctional (columns) responses yields the KANO category:

|  | Like (1) | Must-be (2) | Neutral (3) | Live-with (4) | Dislike (5) |
|--|----------|-------------|-------------|----------------|-------------|
| **Like (1)** | Q (Questionable) | A (Attractive) | A (Attractive) | A (Attractive) | O (One-dimensional) |
| **Must-be (2)** | R (Reverse) | I (Indifferent) | I (Indifferent) | I (Indifferent) | M (Must-be) |
| **Neutral (3)** | R (Reverse) | I (Indifferent) | I (Indifferent) | I (Indifferent) | M (Must-be) |
| **Live-with (4)** | R (Reverse) | I (Indifferent) | I (Indifferent) | I (Indifferent) | M (Must-be) |
| **Dislike (5)** | R (Reverse) | R (Reverse) | R (Reverse) | R (Reverse) | Q (Questionable) |

**Category abbreviations:**
- **A** — Attractive (excitement need): Absence not noticed; presence delights
- **O** — One-dimensional (performance need): Satisfaction proportional to degree of fulfilment
- **M** — Must-be (basic need): Absence causes dissatisfaction; presence taken for granted
- **I** — Indifferent: Neither presence nor absence affects satisfaction
- **R** — Reverse: Opposite preference to expectation (item re-examination required)
- **Q** — Questionable: Internally inconsistent response; excluded from analysis

---

## 3. Category Aggregation Rule

When the same item yields multiple categories across respondents, the dominant category is determined by:

**Priority rule (for tied frequencies):** M > O > A > I

If no single category has a plurality, apply the priority rule above. This rule follows Berger et al. (1993) and is standard in KANO analysis.

---

## 4. Better-Worse (Satisfaction) Coefficients

For each requirement, compute:

```
Better  (SI)  = (A + O) / (A + O + M + I)
Worse   (DI)  = (O + M) / (A + O + M + I) × (−1)
```

- **Better (SI):** How strongly the presence of the feature increases satisfaction (range 0–1; closer to 1 = stronger positive impact)
- **Worse (DI):** How strongly the absence of the feature decreases satisfaction (range −1 to 0; closer to −1 = stronger negative impact)

Requirements in the **upper-right quadrant** of the Better-Worse chart (high SI, low DI magnitude) are Attractive requirements — prioritised for AHP weight derivation in this study.

---

## 5. Invalid Response Treatment

### 5.1 Screening Criteria
Responses were excluded through a three-stage screening process (see `sampling_protocol.md` for full details):

| Exclusion Criterion | Count Excluded |
|--------------------|----------------|
| Completion time < 4 minutes (indicating non-attentive reading) | 17 |
| Straight-line responses (identical code for all 80 sub-questions) | 9 |
| Diagonal/Zigzag pattern responses | 5 |
| High missing rate (> 20% items left unanswered) | 2 |
| Internal inconsistency (≥ 6 Q-coded item pairs) | 3 |
| **Total excluded** | **36** |
| **Valid responses retained** | **282** (from 318 distributed) |

### 5.2 Handling of Q (Questionable) Responses
Within valid questionnaires, individual Q-coded item-pairs (functional=1 dysfunctional=1, or functional=5 dysfunctional=5) were treated as missing data for that item pair and excluded from that item's frequency count. Q-coded pairs constituted < 2.1% of all item responses in the final dataset.

### 5.3 Missing Item Treatment
Single missing items (< 3 per questionnaire) were imputed using the mode of same-group respondents (grouped by professional background). Questionnaires with ≥ 3 missing items were excluded (none occurred in the valid sample after time-based screening).

---

## 6. Reliability and Validity

### Internal Consistency
Cronbach's α was computed for the 40-item paired functional-dysfunctional instrument:
- α = **0.87** (full instrument)
- α = **0.84** (functional sub-scale only)
- α = **0.85** (dysfunctional sub-scale only)

All values exceed the conventional threshold of 0.70.

### Non-response Bias Check
A two-independent-samples t-test was conducted comparing early respondents (first 30%) and late respondents (last 30%) on the aggregate satisfaction score. No significant difference was found (t = 1.14, df = 167, p = 0.256), indicating absence of meaningful non-response bias.

### Construct Validity
Confirmatory factor analysis (CFA) was conducted on the seven requirement dimensions:
- CFI = 0.94, RMSEA = 0.058, SRMR = 0.063
- All factor loadings > 0.52 (p < 0.001)

---

## 7. Demographic Distribution of Valid Respondents (n = 282)

| Category | Sub-group | n | % |
|---|---|---|---|
| **Professional role** | Architecture/Interior Design professional | 94 | 33.3 |
|  | Urban planning/Landscape professional | 47 | 16.7 |
|  | Architecture/Design student (postgraduate) | 68 | 24.1 |
|  | General public with design interest | 73 | 25.9 |
| **Gender** | Female | 151 | 53.5 |
|  | Male | 131 | 46.5 |
| **Age group** | 18–25 | 89 | 31.6 |
|  | 26–35 | 104 | 36.9 |
|  | 36–45 | 61 | 21.6 |
|  | 46+ | 28 | 9.9 |
| **Region** | East China | 162 | 57.4 |
|  | Other China | 97 | 34.4 |
|  | Outside China | 23 | 8.2 |

---

## 8. Data Availability

Anonymised raw response data (coded, no personal identifiers) are available upon reasonable request to the corresponding author. Full raw data cannot be posted publicly due to participant consent terms, but the aggregated frequency tables and KANO classification results are provided in the supplementary materials.
