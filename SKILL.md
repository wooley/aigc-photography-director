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
