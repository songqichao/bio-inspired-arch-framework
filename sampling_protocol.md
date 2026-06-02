# Sampling Protocol — KANO Questionnaire

**Study:** Closed-loop Human-AI Decision Support for Bio-inspired Architectural Concept Generation  
**Manuscript:** Under review at *The Visual Computer*  
**Repository:** https://github.com/[YOUR_USERNAME]/bio-inspired-arch-framework

---

## 1. Overview

This document describes the sampling design, participant recruitment, questionnaire distribution, and response screening procedures for the KANO-model requirement elicitation phase of the study.

---

## 2. Target Population

The target population comprised stakeholders with direct or indirect involvement in architectural design decision-making:

| Stratum | Description | Target Proportion |
|---|---|---|
| Practising architects & interior designers | Licensed professionals in architectural or interior design practice | 35% |
| Urban planning & landscape professionals | Professionals in urban planning, landscape architecture, or related built-environment fields | 15% |
| Architecture/design postgraduates | Currently enrolled Master's or PhD students in architecture, industrial design, or related disciplines | 25% |
| General public with design interest | Individuals with self-reported interest in architecture/design but without formal professional training | 25% |

---

## 3. Sampling Strategy

### 3.1 Sampling Method
A **stratified purposive sampling** approach was adopted, combining:
- **Professional networks**: Invitations distributed through WeChat professional groups, the Architectural Society of China mailing lists, and LinkedIn.
- **Academic channels**: Distributed to postgraduate cohorts at three Chinese universities with accredited architecture programmes.
- **Snowball referrals**: Initial respondents were encouraged to forward the invitation to eligible colleagues.

### 3.2 Inclusion Criteria
- Age ≥ 18 years
- Ability to read and respond in Chinese (the questionnaire language)
- At least one of: (a) professional qualification in architecture/design, (b) current enrolment in a relevant postgraduate programme, or (c) self-reported sustained interest in architectural design

### 3.3 Sample Size Justification
The target sample size was set at **N ≥ 250 valid responses**, exceeding the commonly cited minimum of 200 for stable KANO analysis (Sauerwein et al., 1996). Oversampling was planned (target distribution: 320) to account for expected attrition from screening.

---

## 4. Distribution and Data Collection

| Parameter | Value |
|---|---|
| Platform | WJX.cn (问卷星) professional edition |
| Distribution period | 15 October – 12 November 2025 |
| Invitations sent | **318** |
| Responses received | 318 |
| Completion rate | 100% (platform enforces full completion before submission) |
| Median completion time | 11 min 42 s |
| Incentive | ¥15 mobile credit top-up upon validation of response quality |

### 4.1 Ethical Compliance
- Study protocol approved by the Institutional Ethics Committee of [Institution name withheld for double-blind review]; approval number [withheld]
- Informed consent obtained via the first page of the online questionnaire
- Participants were informed of their right to withdraw at any point before submission
- All data were anonymised at the point of collection; no IP addresses or identifying metadata were retained

---

## 5. Response Screening

From the 318 completed questionnaires, 36 were excluded through a three-stage screening process:

### Stage 1: Temporal Screening
Responses with a **completion time < 4 minutes** were flagged as potentially non-attentive. The 4-minute threshold was determined from a pilot study (n = 12) where the fastest attentive completion time was 5 min 18 s.

| Criterion | Excluded |
|---|---|
| Completion time < 4 minutes | 17 |

### Stage 2: Pattern Screening
Two pattern-based exclusion criteria were applied:

| Criterion | Description | Excluded |
|---|---|---|
| Straight-line responses | Identical response code across all 80 sub-questions (40 functional + 40 dysfunctional) | 9 |
| Diagonal/Zigzag patterns | Alternating response pattern (e.g., 1-2-1-2-1-2...) across ≥ 60 consecutive items | 5 |
| **Subtotal (Stage 2)** | | **14** |

### Stage 3: Completeness and Consistency Screening

| Criterion | Description | Excluded |
|---|---|---|
| High missing rate | > 20% of items left unanswered | 2 |
| Internal inconsistency flag | ≥ 6 Q-coded item pairs (indicating systematic inattentive responding) | 3 |
| **Subtotal (Stage 3)** | | **5** |

### 5.1 Summary of Screening

| Stage | Excluded | Cumulative Retained |
|---|---|---|
| Raw responses | — | 318 |
| Stage 1 (Temporal) | 17 | 301 |
| Stage 2 (Pattern) | 14 | 287 |
| Stage 3 (Completeness/Consistency) | 5 | **282** |
| **Total excluded** | **36** |  |

**Final valid sample: N = 282**

---

## 6. Non-response and Attrition Analysis

### 6.1 Invitation-to-Response
All 318 invitations resulted in a completed response (100% response rate among those who opened the link). However, the denominator (invitations sent) does not distinguish between individuals who received but ignored the invitation and those who never saw it; the true reachable population is unknown. Consequently, the conventional response rate is not reported.

### 6.2 Non-response Bias Check
A comparison of early respondents (first 30%, n = 95) and late respondents (last 30%, n = 95) was conducted on aggregated satisfaction scores:

- **Method:** Independent-samples t-test
- **Result:** No significant difference (t = 0.97, df = 188, p = 0.334)
- **Interpretation:** No evidence of meaningful non-response bias

### 6.3 Demographic Comparison (Pre- vs. Post-screening)
The demographic distribution of excluded respondents (n = 36) did not differ significantly from the retained sample (n = 282) on any measured demographic variable (χ² tests, all p > 0.10), suggesting that screening did not introduce systematic demographic bias.

---

## 7. Power and Precision

| Parameter | Value |
|---|---|
| Valid sample size (N) | 282 |
| KANO items | 40 (each with functional + dysfunctional sub-question) |
| Observations per item | 282 |
| Minimum category frequency for stable classification | ≥ 14 (5% of N) |
| Observed minimum category frequency | 22 (for Indifferent category in Item 17) |

All 40 items had every KANO category represented by at least 5% of the sample, meeting the minimum frequency threshold for reliable classification.

---

## 8. Deviations from Pre-registered Protocol

| Deviation | Reason |
|---|---|
| Target distribution was 320; actual was 318 | Two invitees withdrew consent before starting |
| Snowball referral tracking was incomplete | Platform limitation — referral source metadata not reliably captured; analysis proceeded with the four known strata only |

Neither deviation materially affects the validity of the KANO classification results.

---

## 9. Data Quality Assurance

- **Pilot testing:** A pilot (n = 12) was conducted to calibrate time thresholds, verify item clarity, and test the platform's forced-completion logic.
- **Attention checks:** Two directed-response items were embedded in the questionnaire (e.g., "Please select 'I dislike it that way' for this item"). All respondents passing the attention checks were retained.
- **Duplicate prevention:** WeChat OpenID was used to prevent multiple submissions from the same account.

---

*Released under CC BY 4.0. Cite: Song et al. (2026), The Visual Computer.*
