# ComfyUI Workflow Patterns

## 1. Fast ideation workflow

Use for:
- early brand exploration
- rough product concepting
- mood tests
- composition discovery

Pattern:
1. Load model
2. Positive prompt
3. Negative prompt
4. Latent image setup
5. Sampler
6. Decode
7. Save image

Keep this lean.
The goal is speed, not perfection.

## 2. Image-to-image refinement workflow

Use for:
- improving an existing concept
- keeping structure while shifting style
- iterating toward a usable direction

Pattern:
1. Load source image
2. Encode image
3. Prompt and negative prompt
4. Controlled denoise pass
5. Decode
6. Save image

## 3. Upscale and polish workflow

Use for:
- taking a selected concept toward presentation quality
- increasing resolution after direction is approved

Pattern:
1. Load chosen image
2. Upscale model or latent upscale path
3. Detail pass if needed
4. Save final

Do not waste upscale passes on weak concepts.

## 4. Style-locked brand workflow

Use for:
- keeping a recognizable visual identity
- repeating a visual language across multiple outputs

Pattern:
1. Base model
2. Style prompt discipline
3. Optional LoRA or style adapter
4. Fixed composition rules where useful
5. Save outputs under a shared naming scheme

## 5. Product mockup workflow

Use for:
- visualizing future product directions
- packaging ideas
- website hero concepts
- ad creative exploration

Pattern:
1. Define product form
2. Define material and finish
3. Define environment
4. Define emotional tone
5. Generate variants
6. Select strongest direction
7. Refine only the winners

## 6. Business review rule

Every workflow should answer one of these:
- Does this help choose a brand direction?
- Does this help present a product better?
- Does this help create stronger marketing assets?
- Does this help reduce creative uncertainty?

If not, it may just be pretty noise.
