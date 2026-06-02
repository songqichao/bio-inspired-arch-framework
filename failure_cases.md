# Failure Cases — Representative Generation Failures and Analysis

**Study:** Closed-loop Human-AI Decision Support for Bio-inspired Architectural Concept Generation  
**Manuscript:** Under review at *The Visual Computer*

---

## 1. Purpose

This document reports representative failure cases encountered during the image generation process. Documenting failures is essential for honest reporting of framework limitations and for helping future researchers anticipate and mitigate similar issues.

---

## 2. Failure Taxonomy

Failures were categorised into four types:

| Type | Description | Frequency (of 45 total generated candidates) |
|------|-------------|----------------------------------------------|
| **F1 — Literal animal depiction** | Output shows the biological organism itself rather than an architectural abstraction | 7 / 45 (15.6%) |
| **F2 — Structural incoherence** | Floating elements, physically impossible cantilevers, or disconnected geometry | 5 / 45 (11.1%) |
| **F3 — Prompt override** | Style modifiers overwhelm biological principle transfer (e.g., output is pure modern minimalism with no biomimetic reference) | 4 / 45 (8.9%) |
| **F4 — Visual confusion** | Multiple biological sources conflated; unclear dominant reference | 2 / 45 (4.4%) |

Total failure rate: **18/45 (40%)** of generated candidates were discarded before TOPSIS evaluation.  
Valid candidates retained: **27/45 (60%)**; 9 selected for evaluation (see `generation_parameters.md`).

---

## 3. Case-by-Case Analysis

### F1.1 — Eagle: Literal Animal Depiction
**Prompt excerpt:** "...inspired by the eagle's aerodynamic wing load-path optimisation..."  
**Failure:** Output depicted a photorealistic eagle perching on a building rather than an architectural form derived from eagle wing principles.  
**Diagnosis:** The term "eagle" was interpreted literally by the generation system without sufficient architectural programme anchoring.  
**Fix:** Added explicit architectural programme anchors ("contemporary cultural centre building", "architectural exterior render") and moved the biological reference to a secondary descriptive clause rather than the primary subject.

### F1.2 — Manta Ray: Literal Marine Scene
**Prompt excerpt:** "...inspired by the manta ray's hydrodynamic drag-reduction surface..."  
**Failure:** Output depicted an underwater scene with a manta ray, not an architectural concept.  
**Diagnosis:** Insufficient domain specification; generation defaulted to the most common visual context for "manta ray" (marine photography).  
**Fix:** Added "architectural building exterior" as the primary subject and included "above-ground structure", "urban context" to redirect the generation domain.

### F2.1 — Cheetah: Structural Incoherence
**Prompt excerpt:** "...dynamic ground-reaction-force distribution inspired by cheetah locomotion mechanics..."  
**Failure:** Generated roof canopy with no visible structural support; floating slab with no columns or load paths.  
**Diagnosis:** The "dynamic" descriptor combined with "ground-reaction-force distribution" was misinterpreted as implying levitation rather than transfer of forces to ground.  
**Fix:** Replaced "ground-reaction-force distribution" with "branching structural grid transferring loads to ground points" for clearer structural intent.

### F2.2 — Eagle: Disconnected Wing Elements
**Prompt excerpt:** "...long-span cantilever wing geometry..."  
**Failure:** Two separate wing-like canopies with no visible structural connection to the ground or each other.  
**Diagnosis:** "Long-span cantilever" generated two separate forms rather than a unified structural system.  
**Fix:** Added "unified continuous structural shell", "single building mass" to enforce structural unity.

### F3.1 — Manta Ray: Style Override
**Prompt:** Full weighted Tier 2 prompt with "minimalist architectural render" as style modifier.  
**Failure:** Output was a generic glass-and-steel tower with no biomimetic reference; the minimalist style modifier completely dominated the biological principle transfer descriptors.  
**Diagnosis:** Style modifiers placed at the end of the prompt with high intrinsic model weight overrode the weaker biological principle descriptors.  
**Fix:** Moved biological principle descriptors to the **start** of the prompt (highest attention weight position) and replaced generic style modifiers with more specific medium descriptors ("parametric architectural concept, high-resolution 3D render, physical model aesthetic").

### F4.1 — Cheetah: Visual Confusion
**Prompt:** Early version including multiple biological references for comparison purposes.  
**Failure:** Output showed a form combining leopard-print façade patterning (cheetah) with raptor-wing canopy (eagle) — a chimeric result.  
**Diagnosis:** Multi-biological-reference prompt without clear hierarchy caused conflation.  
**Fix:** Established strict one-organism-per-image rule; all multi-organism references removed from individual prompts.

---

## 4. Prompt Engineering Lessons Learned

| Lesson | Implication for Template Design |
|--------|--------------------------------|
| Always specify architectural programme as the **primary subject** | Subject slot: "A contemporary [building type] building concept" |
| Place biological principle transfer as **secondary descriptive clause** | "inspired by [organism]'s [specific mechanical principle]" |
| Avoid generic style modifiers that may override domain | Use domain-specific medium descriptors instead of "minimalist", "modern" |
| One biological organism per prompt | No comparative or multi-organism prompts |
| Structural logic requires explicit verbal specification | Include load-path language; do not assume generation system will infer structural rationality |
| Negative prompts are essential for domain control | Include "photorealistic animal", "underwater", "cartoon" in negative prompts for architectural generation |

These lessons are incorporated into the final prompt templates in `prompt_templates.md`.

---

## 5. Failure Rate Context

The 40% initial failure rate is consistent with reported generation efficiency in structured architectural prompt studies. The combination of prompt engineering refinements described above reduced the need for regeneration in later case studies (manta ray and cheetah) compared to the first (eagle), where most F1-type failures were encountered during template development.
