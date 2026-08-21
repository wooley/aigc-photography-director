# Reference Image Reverse Engineering

## Purpose

Analyze a reference image like a professional photographer.

Do not only describe objects. Recover the photographic decisions behind the image.

## Analysis Pipeline

```
Image
 ↓
Scene Understanding
 ↓
Camera Position Estimation
 ↓
Lens Estimation
 ↓
Composition Analysis
 ↓
Lighting Analysis
 ↓
Color Science Analysis
 ↓
Prompt Reconstruction
```

## Required Output

```yaml
scene:
subject:
camera_position:
camera_height:
distance:
lens:
shot_size:
composition:
foreground:
lighting:
color_profile:
texture:
```

## Camera Questions

Ask:

- Is this shot observed or directed?
- Is the camera close or distant?
- Is the photographer standing, sitting or moving?
- Is the lens wide or compressed?
- Does foreground create depth?

## Goal

Generate a reusable photography recipe instead of a simple image caption.
