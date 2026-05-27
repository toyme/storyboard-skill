# Storyboard Project Structure

Use this file when creating a reusable storyboard workspace.

## Files

`bible/character_bible.md`

```markdown
# Character Bible

## char_a_v1
- Name:
- Role:
- Age range:
- Face:
- Hair:
- Body / silhouette:
- Wardrobe:
- Signature props:
- Never change:
- Current approved reference:
```

`bible/visual_style_bible.md`

```markdown
# Visual Style Bible

## style_main_v1
- Medium:
- Genre:
- Color logic:
- Lighting rules:
- Camera language:
- Texture / grain:
- Aspect ratio:
- Avoid:
- Approved references:
```

`bible/continuity_rules.md`

```markdown
# Continuity Rules

## Global
- 

## Characters
- 

## Locations
- 

## Style
- 

## Known failure patterns
- 
```

`scenes/scene_##.yaml`

```yaml
scene: 1
title:
location:
time_of_day:
story_beat:
characters:
  - char_a_v1
visual_style: style_main_v1
continuity_notes:
  - 
```

`shots/scene_##_shots.yaml`

```yaml
scene: 1
shots:
  - id: scene_01_shot_001
    shot_type: close-up
    lens: 85mm
    camera_angle: eye-level
    emotion:
    action:
    composition:
    continuity:
      - 
    status: draft
```

`prompts/scene_##_shot_###.md`

```markdown
# scene_##_shot_###

## Production Notes

## Image Prompt

## Fix Notes
```

## Operating Rules

- Keep bibles short and canonical. Move experiments to prompt files or reviews.
- Give every character, location, style, scene, shot, and prompt a stable ID.
- Store approved decisions in bibles; store temporary attempts in prompt or review files.
- Split scenes into separate files once a file becomes long enough to distract from the current task.
