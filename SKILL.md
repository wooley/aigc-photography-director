---
name: aigc-photography-director
description: Use for AI photography direction, camera planning, and image prompts.
---

# AIGC Photography Director Skill

## Purpose

Transform AIGC image/video requests from simple visual descriptions into photography-director level instructions.

The skill focuses on camera spatial reasoning, series consistency, cinematic composition and professional photography language.

## Core Principle

Do not only describe the subject and environment.
Define the relationship between:

- camera position
- camera height
- camera distance
- shooting direction
- lens and shot size
- foreground relationship
- subject placement

Formula:

`Camera Position × Height × Distance × Direction × Shot Size × Foreground × Subject Placement`

## Workflow

1. Understand the creative theme.
2. Define visual style and emotional direction.
3. Create a photography plan.
4. Generate camera positions for each shot.
5. Expand each shot into production-ready prompts.
6. Lock character identity and visual consistency.

## Required Shot Description

Every generated shot should contain:

```yaml
camera_position:
camera_height:
distance_to_subject:
direction:
lens:
shot_size:
foreground:
subject_position:
lighting:
color_profile:
```

## Series Generation Rules

For multi-image requests:

- Keep character identity stable.
- Keep color system stable.
- Vary camera language instead of only changing backgrounds.
- Create different visual narratives through composition.

## Face Stability and Long-Shot Composition

In a 16:9 full-body or long shot, the face occupies fewer pixels, so the model may prioritize the body, clothing, environment, and overall composition. Wide-angle lenses, profiles, backlighting, action, and motion blur can make facial drift worse.

Use this correction workflow when identity fidelity matters:

1. Generate a frontal or three-quarter half-body portrait first. Select a sharp, well-lit image as the face-lock identity reference.
2. Generate the full-body image with a 50–85mm lens, an eye-level camera, and a medium-to-long camera distance. Keep the subject large enough that the face is readable; when facial identity is important, the subject should occupy roughly 60–75% of the frame height.
3. Require: face clearly visible and in focus, natural facial proportions, no motion blur, no extreme wide-angle distortion, and identity preserved from the face-lock reference.
4. If the face is only slightly off, locally repair the face while preserving the hair, clothing, pose, lighting, and background. If it is severely deformed, regenerate from the face-lock reference instead of relying on smoothing or upscaling.

For a nine-image series, prefer a 3/3/3 balance by default: three full-body images, three medium shots, and three close or half-body portraits. This preserves narrative variety while ensuring that several images provide enough facial detail for stable identity.

## Identity Lock

Fixed:

- face structure
- hairstyle
- age
- body proportion
- clothing identity
- character personality

Variable:

- camera angle
- pose
- environment interaction
- composition
- movement

## Output Style

Prefer professional photography terminology:

- editorial photography
- documentary photography
- cinematic portrait
- environmental portrait
- street photography
- film photography

Avoid meaningless style stacking such as:

"high-end, cinematic, masterpiece, amazing"

unless supported by concrete photographic decisions.
