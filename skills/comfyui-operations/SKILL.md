---
name: comfyui-operations
description: Operate, configure, and optimize ComfyUI for local image generation workflows, especially for concept art, brand exploration, product mockups, and iterative visual ideation. Use when installing or managing ComfyUI, choosing models and workflows, working within GPU VRAM limits, designing prompt-to-image pipelines, or reviewing local image-generation options against cloud tools.
---

# ComfyUI Operations

Operate like a ComfyUI power user, not a casual prompt box user.

## Core role

Use ComfyUI as a controllable local image-generation system for:
- concept generation
- design exploration
- moodboards
- brand direction
- ad creative ideation
- product visualization
- workflow experimentation

Optimize for:
- repeatability
- clarity
- VRAM-aware workflow design
- fast iteration
- saved workflow reuse

## Default posture

Prefer ComfyUI when:
- local generation is good enough
- rapid concept iteration matters
- workflows need control
- prompt chains, LoRAs, or image-to-image need structure
- cloud cost or privacy matters

Do not overcomplicate the stack at the start.
Build a stable base workflow first.

## Workflow design process

1. Define the visual objective.
2. Decide whether the job is concepting, refinement, or final-quality generation.
3. Choose a model that fits the machine's VRAM reality.
4. Build the smallest workflow that can reliably achieve the goal.
5. Save reusable variants only after the workflow proves itself.
6. Track what settings actually produce good output.

## Practical rule

For most real work, separate workflows into:
- fast ideation
- refinement
- upscale or polish

Do not force one giant workflow to do everything.

## VRAM discipline

Always account for hardware limits before choosing models or resolution.

Use memory-conscious defaults first.
Increase complexity only after confirming stability.

See `references/local-hardware.md` for the current machine profile.

## What good ComfyUI usage looks like

A good setup has:
- a stable install
- a known model directory structure
- a few proven workflows
- clear naming for outputs
- resolution choices matched to hardware
- a documented path from rough concept to refined image

A bad setup is a pile of random custom nodes and broken graphs.

## Prompting standard

Prompt for:
- subject
- environment
- mood
- material qualities
- composition
- lighting
- style influence
- exclusions when needed

For brand work, translate abstract positioning into visual language instead of vague adjectives.

## Review standard

Before accepting an image direction, check:
- Does it match the business objective?
- Is it usable for concepting, or only visually interesting?
- Is the style coherent?
- Does it strengthen the brand, or just look pretty?
- Could it guide design, copy, or product presentation decisions?

## Local vs cloud rule

Use local ComfyUI for:
- brainstorming
- exploration
- variant generation
- internal concept work
- workflow experimentation

Use cloud or premium external models when:
- maximum polish matters
- the local workflow hits quality ceilings
- turnaround matters more than system control

## Review mode

When reviewing a ComfyUI plan, inspect:
- install approach
- model suitability
- VRAM fit
- workflow simplicity
- maintainability
- output usefulness

See `references/workflow-patterns.md` for recommended workflow shapes.
