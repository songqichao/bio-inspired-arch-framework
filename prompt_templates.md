# Prompt Templates — Weight-to-Text Conversion

**Study:** Closed-loop Human-AI Decision Support for Bio-inspired Architectural Concept Generation  
**Manuscript:** Under review at *The Visual Computer*  
**Repository:** https://github.com/[YOUR_USERNAME]/bio-inspired-arch-framework

---

## 1. Overview

This document describes how AHP-derived requirement weights are translated into structured natural-language prompts fed into the diffusion-based image generation system. The prompt engineering strategy follows a three-tier hierarchy: **system prompt → structural prompt → stylistic prompt**, with weights modulating the emphasis and placement of each requirement descriptor.

---

## 2. Prompt Architecture

### 2.1 System Prompt (Fixed — applied to all generations)

```
You are an architectural concept design assistant specialising in biomimetic form generation.
Generate exterior perspective views of a building concept. Output architectural visualisation
quality. Maintain structural plausibility. Integrate biological principles, not merely biological
shapes. Prioritise spatial quality and human-scale experience.
```

### 2.2 Structural Prompt (Weight-driven — varies by case)

Template:
```
[BIOMIMETIC SOURCE]: {species/biological system}
[BUILDING TYPOLOGY]: {programme type}
[SCALE]: {approximate dimensions in metres}
[KEY STRUCTURAL PRINCIPLE]: {derived from top-weighted B1 sub-criterion}
[CLIMATE CONTEXT]: {derived from top-weighted B2 sub-criterion}
[SPATIAL PRIORITY]: {derived from top-weighted B3 sub-criterion}
```

### 2.3 Stylistic Prompt (Weight-driven — varies by case)

Template:
```
[BIOMIMETIC DEPTH]: {derived from top-weighted B4 sub-criterion}
[AESTHETIC EMPHASIS]: {derived from top-weighted B5 sub-criterion}
[FEASIBILITY CONSTRAINT]: {derived from top-weighted B6 sub-criterion}
[INNOVATION ANGLE]: {derived from top-weighted B7 sub-criterion}
```

---

## 3. Weight-to-Emphasis Mapping

Weights are mapped to prompt emphasis levels using the following discretisation:

| Global Weight Range | Emphasis Level | Prompt Modifier |
|---|---|---|
| ≥ 0.06 | **Critical** | Placed first in the prompt; prefixed with "crucially," or "above all," |
| 0.03 – 0.059 | **Major** | Placed in the main body; no special modifier |
| 0.015 – 0.029 | **Moderate** | Placed after major items; prefixed with "also consider," |
| < 0.015 | **Minor** | Omitted from the primary prompt; addressed in negative-prompt exclusions |

---

## 4. Case-Specific Prompt Examples

### 4.1 Eagle Case (Aquila chrysaetos → Aviation Museum)

**AHP-derived priorities (top 5 global weights):**
1. B1-3 Structural redundancy (0.0886) → CRITICAL
2. B1-1 Load-path logic (0.0665) → CRITICAL
3. B6-1 Buildability (0.0642) → CRITICAL
4. B3-5 Human scale (0.0619) → CRITICAL
5. B1-6 Material optimisation (0.0509) → MAJOR

**Assembled Prompt:**

> [SYSTEM PROMPT — as defined in §2.1]
>
> **Biomimetic source:** Golden Eagle (Aquila chrysaetos) wing morphology — primary feather separation at wingtip during soaring, alula deployment for stall control.
>
> **Building typology:** Aviation museum and research centre.
>
> **Scale:** Approx. 120 m × 80 m footprint, max. height 35 m.
>
> **Crucially, the design must demonstrate visible structural redundancy** through a diagrid system inspired by the eagle's skeletal wing structure, where load paths are distributed across multiple intersecting members rather than a single spine. **Above all, the load-path logic must be legible** — the transition from roof loads through the primary structure to the ground should be visually traceable.
>
> The design **must appear buildable with contemporary steel and glass construction technology**. Primary members should follow standardised section profiles; complex doubly-curved elements should be limited to the canopy edge.
>
> Despite the large span, the building **must respect human scale** at ground level — entrance, lobby, and gallery spaces should read as welcoming rather than overwhelming.
>
> **Also prioritise** material optimisation: structural elements should appear efficiently sized for their spans, without visible over-engineering.
>
> **Negative prompt:** pure sculptural form with no structural logic, impossible cantilevers, unbuildable organic blobs, inhuman monumental scale, structurally ambiguous floating volumes.

### 4.2 Manta Ray Case (Mobula birostris → Aquatic Centre)

**AHP-derived priorities:**
1. B2-1 Climate response (0.0460) → MAJOR
2. B2-4 Envelope thermal (0.0290) → MAJOR
3. B3-3 Spatial variety (0.0491) → MAJOR
4. B4-3 Principle transfer (0.0289) → MODERATE
5. B1-4 Connection resolution (0.0505) → MAJOR

**Assembled Prompt:**

> [SYSTEM PROMPT — as defined in §2.1]
>
> **Biomimetic source:** Manta ray (Mobula birostris) — cephalic fin funneling for hydrodynamic efficiency, cartilaginous tessellated skeleton for flexible yet robust structural support.
>
> **Building typology:** Public aquatic centre with competition and leisure pools.
>
> **Scale:** Approx. 90 m × 60 m footprint, max. height 18 m.
>
> The design must respond visibly to the **local hot-humid climate** — the roof form should suggest self-shading, natural ventilation chimneys, and protection from direct solar gain, inspired by the ray's wing-like pectoral fins creating shaded micro-zones.
>
> **Prioritise spatial variety**: distinct zones for competition (enclosed), leisure (semi-enclosed), and external pool deck should read as a sequenced spatial journey.
>
> **Connection resolution** between the sweeping roof form and vertical supports must be visually articulated — avoid ambiguous blob-to-column transitions. The tessellated cartilage principle should inform a modular connection logic.
>
> The **envelope** should communicate thermal performance — deep overhangs, louvred openings, and layered façade elements.
>
> **Also consider** that the principle transfer should go beyond shape: the manta ray's cephalic fin funneling should translate into a ventilation strategy, not merely a curved roof.
>
> **Negative prompt:** generic swooping roof with no climate logic, unarticulated junctions, monotonous internal volume, purely decorative biomorphism.

### 4.3 Cheetah Case (Acinonyx jubatus → Sports Complex)

**AHP-derived priorities:**
1. B3-5 Human scale (0.0619) → CRITICAL
2. B5-3 Typology fit (0.0150) → MODERATE
3. B4-3 Principle transfer (0.0289) → MODERATE
4. B1-3 Structural redundancy (0.0886) → CRITICAL
5. B6-1 Buildability (0.0642) → CRITICAL

**Assembled Prompt:**

> [SYSTEM PROMPT — as defined in §2.1]
>
> **Biomimetic source:** Cheetah (Acinonyx jubatus) — spinal flexion-extension during high-speed gallop, semi-retractable claws for traction, lightweight skeletal structure.
>
> **Building typology:** Multi-sport training complex with indoor track.
>
> **Scale:** Approx. 150 m × 60 m footprint, max. height 22 m.
>
> **Above all, the building must demonstrate structural redundancy** through a spine-like primary structural rhythm with secondary cross-bracing inspired by the cheetah's ribcage — no single member failure should cause disproportionate collapse.
>
> The design **must appear buildable** using long-span steel truss systems with fabric membrane roofing. The cheetah's lightweight skeleton should translate to an expressed tensile structure.
>
> Despite the athletic programme, **human scale must be maintained** — the building should feel dynamic and aspirational, not intimidating. Entry sequences should compress and release, echoing the cheetah's crouch-to-sprint transition.
>
> **Also consider** that the design must fit a sports typology — the form should communicate motion and athleticism without resorting to literal animal shapes.
>
> **Negative prompt:** literal cheetah-shaped building, structurally implausible dynamic forms, inhuman megastructure, cartoonish animal mimicry.

---

## 5. Prompt Consistency Protocol

To ensure reproducibility across generation runs:

| Parameter | Rule |
|---|---|
| Prompt structure | Fixed three-tier (system → structural → stylistic); order within each tier follows global weight ranking |
| Terminology | Use architectural, not colloquial, descriptors (e.g., "expressed tensile structure" not "cool roof") |
| Negative prompt | Standardised set of exclusions per case, derived from the five lowest-weighted sub-criteria |
| Prompt length | 250–400 words (including system prompt); tested empirically — shorter prompts produced generic outputs, longer prompts introduced conflicting directives |
| Reproducibility seed | Each prompt was used with 5 different random seeds; the best output per seed was evaluated in TOPSIS scoring |

---

## 6. Prompt Evolution Log

During the iterative refinement phase, the following adjustments were made:

| Iteration | Change | Rationale |
|---|---|---|
| v0 (initial) | No weight-based emphasis | Baseline; outputs scored C_i = 0.312 |
| v1 | Added critical/major/moderate emphasis tiers | +0.106 improvement in TOPSIS C_i |
| v2 | Negative prompt derived from lowest-weight sub-criteria | Reduced off-target generations by 34% |
| v3 | Added "structural plausibility" constraint in system prompt | Eliminated physically impossible outputs |
| v4 (final) | Climate context integrated from B2 top weights | Improved environmental responsiveness scores |

---

*Released under CC BY 4.0. Cite: Song et al. (2026), The Visual Computer.*
