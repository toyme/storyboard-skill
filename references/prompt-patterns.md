# Storyboard Prompt Patterns

Use this file when generating image prompts or review notes.

## Scene-To-Prompt Template

```text
[SHOT ID]
scene_##_shot_###

[PURPOSE]
What this frame must communicate in the storyboard.

[CHARACTER]
Only the character traits required for this shot. Include stable IDs.

[CAMERA]
Shot size, lens, camera angle, movement if relevant.

[LIGHTING]
Light source, direction, mood, contrast, time of day.

[EMOTION]
Visible emotional state and body language.

[COMPOSITION]
Subject placement, foreground/background, depth, negative space.

[ENVIRONMENT]
Location details that must appear.

[CONTINUITY]
What must match prior approved frames.

[NEGATIVE CONSTRAINTS]
What the image model must not alter or invent.

[IMAGE PROMPT]
One polished prompt ready for the image model.
```

## Compact Image Prompt Formula

```text
Create [shot type] of [character/action] in [location], [camera/lens/framing].
Preserve [identity/wardrobe/props/style refs].
Lighting: [specific lighting].
Mood: [emotion].
Composition: [layout/depth].
Style: [medium/rendering/color/texture/aspect].
Do not [negative constraints].
```

## Fix Prompt Template

```text
Use the provided image as the base.
Preserve: [approved elements].
Change only: [specific target].
Do not change: [identity, wardrobe, pose, camera, lighting, composition, style].
Result should look like: [target].
```

## Review Output Template

```markdown
## Continuity Review

| Shot | Status | Issue | Fix |
|---|---|---|---|
| scene_01_shot_001 | pass / revise |  |  |

## Global Notes
- 

## Priority Fixes
1. 
```

## Prompt Hygiene

- Use stable IDs instead of re-explaining the whole project.
- Include only details visible or important in the current frame.
- Put forbidden changes in negative constraints.
- Prefer targeted fixes over full prompt rewrites after a frame is close.
- Keep one image prompt per shot unless the user asks for variations.
