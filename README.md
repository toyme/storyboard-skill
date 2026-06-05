# Storyboard Skill

Codex skill for AI image storyboard planning, structured image prompts, continuity checks, fix prompts, and prompt safety review.

這是一個給 Codex 使用的分鏡輔助技能。它把故事、場景描述、分鏡想法整理成清楚的 shot list、production notes、AI 圖像生成 prompt，以及角色/服裝/道具/場景連續性檢查。

## What It Helps With

- Turn a scene or story beat into a storyboard shot list.
- Write one structured image prompt per shot.
- Maintain character, wardrobe, prop, location, and visual-style continuity.
- Create targeted fix prompts for image-to-image revisions.
- Review prompts for common safety and rights risks, including NSFW, minors, gore, real-person likeness, copyrighted characters, brands, and sensitive personal data.
- Keep longer projects organized with compact project files instead of long chat threads.

## Best Fit

Use this skill when you are working on:

- AI image storyboards
- short drama or short-form narrative concepts
- visual pitch decks
- character-consistent image sequences
- image prompt packs for tools such as ChatGPT Image, Midjourney, Stable Diffusion, Nano Banana, or similar image tools
- prompt repair after an image is close but needs a specific local change

This skill does not directly generate images or videos, connect to Seedance, Higgsfield, Runway, Kling, or upload assets to any platform. It prepares the structured prompts and review notes that you can use in those tools.

## Install

Clone this repo into your Codex skills folder.

Windows PowerShell:

```powershell
git clone https://github.com/toyme/storyboard-skill.git "$env:USERPROFILE\.codex\skills\storyboard-skill"
```

macOS / Linux:

```bash
git clone https://github.com/toyme/storyboard-skill.git ~/.codex/skills/storyboard-skill
```

After installation, confirm this file exists:

```text
~/.codex/skills/storyboard-skill/SKILL.md
```

If Codex does not pick up the skill immediately, start a new conversation or restart Codex.

## Quick Start

English:

```text
Use $storyboard-skill to turn this scene into 6 storyboard image prompts with continuity notes:

The protagonist stands in a rainy alley holding a letter. They hesitate, tear it in half, and walk away.
```

Chinese:

```text
使用 $storyboard-skill 幫我把這段劇情拆成 6 格分鏡，並替每格寫 AI 圖像 prompt、角色一致性檢查和修圖備註：

主角站在雨中的巷口，手裡拿著一封信。他猶豫很久，最後把信撕掉，轉身離開。
```

Fix prompt:

```text
使用 $storyboard-skill 幫我寫修正 prompt，只改手的姿勢，不要改角色長相、服裝、構圖和光線。
```

Continuity review:

```text
Use $storyboard-skill to review these 8 image prompts for character consistency, wardrobe drift, prop continuity, and safety risks.
```

## Output Shape

For each shot, the skill favors this compact production format:

```text
[SHOT ID]
[PURPOSE]
[CHARACTER]
[CAMERA]
[LIGHTING]
[EMOTION]
[COMPOSITION]
[ENVIRONMENT]
[CONTINUITY]
[NEGATIVE CONSTRAINTS]
[IMAGE PROMPT]
[FIX NOTES] optional
```

The `[IMAGE PROMPT]` block is meant to be ready to paste into an image tool. The other sections are production notes for continuity and review.

## Project Structure

For larger storyboard projects, the skill can help create and maintain this structure:

```text
storyboard-project/
  bible/
    character_bible.md
    visual_style_bible.md
    continuity_rules.md
  scenes/
    scene_01.yaml
  shots/
    scene_01_shots.yaml
  prompts/
    scene_01_shot_001.md
  reviews/
    continuity_review.md
```

You do not need all files for a quick test. Start with one scene or one shot list, then add bibles and reviews when continuity becomes important.

## Examples

See:

- [`examples/short-drama-scene.md`](examples/short-drama-scene.md) - turn one dramatic beat into a multi-shot image prompt plan
- [`examples/image-prompt-review.md`](examples/image-prompt-review.md) - review prompt consistency and safety risks
- [`examples/fix-prompt.md`](examples/fix-prompt.md) - write a targeted regeneration prompt without changing approved details

## Included References

- [`references/project-structure.md`](references/project-structure.md) - reusable storyboard project layout
- [`references/prompt-patterns.md`](references/prompt-patterns.md) - image prompt, fix prompt, and review output patterns
- [`references/prompt-safety-checklist.md`](references/prompt-safety-checklist.md) - prompt safety and rights-risk review checklist

## Version

Current public baseline: `v0.1.0`

This first public version focuses on:

- storyboard breakdown
- structured image prompts
- continuity review
- targeted fix prompts
- compact project-file workflow
- basic safety and rights-risk prompt review

## License

MIT
