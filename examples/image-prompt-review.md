# Example: Image Prompt Review

## User Request

```text
Use $storyboard-skill to review these prompts for character consistency, wardrobe drift, prop continuity, and safety risks.
```

## Expected Output Shape

```markdown
## Continuity Review

| Shot | Status | Issue | Fix |
|---|---|---|---|
| scene_01_shot_001 | pass | Stable wardrobe, letter prop, rainy alley, and cool lighting. | None. |
| scene_01_shot_002 | revise | Prompt changes the coat from dark wool to tan leather. | Restore the approved dark coat from char_a_v1. |
| scene_01_shot_003 | revise | The letter moves from the right hand to the left hand without story reason. | Keep the letter in the right hand until the tearing action begins. |

## Safety Review

| Item | Status | Issue | Fix |
|---|---|---|---|
| NSFW / sexual content | pass | No sexual framing. | None. |
| Minors | pass | Character is described as an adult. | None. |
| Violence / gore | pass | No graphic injury. | None. |
| Real-person likeness | pass | No real person is referenced. | None. |
| Copyrighted characters / brands | pass | No protected character or brand is central. | None. |

## Priority Fixes

1. Restore wardrobe continuity in scene_01_shot_002.
2. Keep the letter prop in the right hand until the action beat changes.
3. Reuse the same cool rainy-night lighting language across all shots.
```

## Notes

Keep reviews practical. Point to the exact shot, explain the drift, and give a replacement instruction that can be pasted back into the prompt.
