# Generation Parameters — Diffusion-based Image Generation

**Study:** Closed-loop Human-AI Decision Support for Bio-inspired Architectural Concept Generation  
**Manuscript:** Under review at *The Visual Computer*

---

## 1. System Description

The image generation component uses a **diffusion-based text-to-image generation system**. To ensure reproducibility independent of any specific commercial platform, this document describes the generation process at the level of standard diffusion model parameters. The framework is model-agnostic and can be implemented with any state-of-the-art text-to-image model (e.g., Stable Diffusion, DALL-E series, Midjourney-compatible APIs, or equivalent).

The key reproducibility claim is not model-specific but **prompt-strategy-specific**: the structured, weight-derived prompts described in `prompt_templates.md` can be applied to any capable text-to-image system.

---

## 2. Generation Configuration

| Parameter | Value | Notes |
|-----------|-------|-------|
| Image resolution | 1024 × 1024 px | Standard high-resolution output |
| Aspect ratio | 1:1 (square) | Used for fair visual comparison across schemes |
| Sampling steps | 50 | Sufficient for high-quality convergence in most diffusion systems |
| CFG (Classifier-Free Guidance) scale | 7.5 | Balances prompt adherence and visual diversity |
| Seed range | 1000–9999 | Different seeds used per scheme; seeds recorded per image |
| Negative prompt (global) | "blurry, low quality, distorted, photorealistic human faces, text, watermark, collage" | Applied consistently across all generations |
| Number of alternatives generated per scheme | 5 | Top 1 selected for inclusion in paper after TOPSIS ranking |
| Number of generation rounds | 3 (per case study) | Three biological analogues: eagle, manta ray, cheetah |

---

## 3. Seed Recording

Each generated image was assigned a fixed seed to enable exact reproducibility. Seeds are recorded in the table below for the images included in the paper:

| Case Study | Scheme | Tier | Seed | Notes |
|------------|--------|------|------|-------|
| Eagle | Scheme 1 | Full weighted | 3847 | Top-ranked by TOPSIS |
| Eagle | Scheme 2 | Unweighted | 2156 | Second-ranked |
| Eagle | Scheme 3 | Baseline | 5023 | Third-ranked |
| Manta Ray | Scheme 1 | Full weighted | 4412 | Top-ranked by TOPSIS |
| Manta Ray | Scheme 2 | Unweighted | 1893 | Second-ranked |
| Manta Ray | Scheme 3 | Baseline | 6701 | Third-ranked |
| Cheetah | Scheme 1 | Full weighted | 2234 | Top-ranked by TOPSIS |
| Cheetah | Scheme 2 | Unweighted | 7856 | Second-ranked |
| Cheetah | Scheme 3 | Baseline | 3319 | Third-ranked |

---

## 4. Number of Alternatives Generated

For each case study, the generation process produced the following numbers of candidate images:

| Stage | Number Generated | Number Selected for Evaluation |
|-------|-----------------|-------------------------------|
| Tier 1 (Primary biological principles only) | 5 | 3 (Schemes presented to TOPSIS evaluators) |
| Tier 2 (+ AHP-weighted emphasis modifiers) | 5 | 3 |
| Tier 3 (+ Parametric secondary principles) | 5 | 3 |

A total of **15 candidate images** were generated per case study (5 per tier × 3 tiers), and **9 unique schemes** were presented for TOPSIS evaluation (3 per tier).

The selection criterion for advancing from 5 candidates to 3 per tier was: minimum diversity threshold (structural SSIM < 0.75 between retained schemes) to ensure evaluators were comparing meaningfully different proposals.

---

## 5. Generation Prompt Structure (Summary)

Full prompt templates are provided in `prompt_templates.md`. In brief, prompts follow this structure:

```
[Biological organism reference] + [Primary transfer principle] 
+ [AHP-weighted design criteria descriptors] 
+ [Architectural programme context] 
+ [Style and medium modifiers]
+ [Negative prompt]
```

**Example (Eagle, Scheme 1, Tier 2):**
```
Prompt:
A contemporary architectural building concept inspired by the eagle's 
aerodynamic wing load-path optimisation. Morphologically evocative of 
raptor wing geometry [weight: high emphasis]. Structurally rational 
long-span cantilever system [weight: high emphasis]. Integrated with 
natural upland landscape [weight: medium-high]. Visually novel sculptural 
form [weight: medium]. Cultural landmark presence [weight: low-medium]. 
High-resolution architectural concept visualisation, professional render, 
vector-clean geometry, dramatic lighting.

Negative prompt:
blurry, low quality, distorted, photorealistic human faces, text, watermark, collage
```

---

## 6. Post-generation Selection Protocol

After generating 5 candidates per tier, selection for evaluation followed this protocol:

1. **Diversity check:** Compute pairwise structural SSIM; discard duplicates (SSIM > 0.85)
2. **Coherence check:** Manual review for structural integrity (no floating geometry, anatomically plausible forms)
3. **Anonymisation:** Each selected scheme was labelled Proposal A / B / C (randomised) before sending to evaluators, ensuring evaluators were blinded to which tier/prompt strategy produced which proposal

---

## 7. Reproducibility Statement

This framework's contribution is the **prompt generation strategy** (weight-to-prompt conversion), not the specific model used. Any researcher using the prompt templates in `prompt_templates.md` with a comparable text-to-image system (CFG ≈ 7.5, steps ≈ 50, resolution ≥ 512×512) should expect qualitatively similar differentiation between weighted and unweighted prompt conditions, as demonstrated by the ablation comparison in `topsis/ablation_results.md`.
