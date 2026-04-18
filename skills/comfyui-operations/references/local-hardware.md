# Local Hardware Profile

Use this profile when planning ComfyUI workflows on this machine.

## Current machine summary

- CPU: Intel i5-7400
- RAM: 24 GB
- GPU 0: NVIDIA RTX 3070, 8 GB VRAM
- GPU 1: NVIDIA RTX 3070, 8 GB VRAM
- Disk free: roughly 100+ GB available when profiled
- OS: Fedora Linux
- NVIDIA drivers and CUDA are present and working

## Practical meaning

This machine is strong enough for serious local image generation.

But it is still an **8 GB VRAM reality per card** for many workflows.
Do not plan as if this is one giant pooled-VRAM workstation.

## Implications

Prefer:
- efficient models
- sensible resolutions
- staged workflows
- separate ideation and upscale passes
- careful custom-node selection

Avoid starting with:
- giant all-in-one graphs
- extreme VRAM-heavy checkpoints without testing
- unnecessary node sprawl

## Recommended posture

Use one GPU per active workflow unless there is a proven multi-GPU setup.
Treat the second 3070 as capacity for parallel tasks or later refinement workflows, not as assumed shared memory for one job.

## Good first-use targets

- concept art
- moodboards
- brand exploration
- product scene mockups
- ad creative ideation
- visual testing for website direction
