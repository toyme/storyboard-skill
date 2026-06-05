# Example: Fix Prompt

## User Request

```text
Use $storyboard-skill to write a fix prompt. The image is good, but the hand looks wrong. Only fix the hand. Do not change the face, coat, lighting, or composition.
```

## Expected Output Shape

```text
Preserve:
The approved adult protagonist identity, face, damp dark coat, rainy alley environment, cool streetlamp backlight, wet pavement reflections, camera angle, composition, and dramatic mood.

Change only:
Correct the right hand so it naturally holds the paper letter with believable finger anatomy and a relaxed but tense grip.

Do not change:
Do not alter the face, hair, coat, body pose, letter design, alley background, lighting direction, color palette, framing, or aspect ratio.

Output:
Use the provided image as the base. Keep the same character, coat, rainy alley, cool night lighting, and composition. Correct only the right hand so it holds the paper letter naturally with anatomically believable fingers and a subtle tense grip. Do not change the face, wardrobe, pose, camera angle, background, lighting, color palette, or overall scene.
```

## Notes

For localized repairs, keep the prompt narrow. Start with preservation, then specify one change, then list continuity-critical details that must not move.
