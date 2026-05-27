# Prompt Safety Checklist

Use this file when reviewing storyboard frames, image prompts, fix prompts, or handoff notes for platform-safety risks. Keep the review focused on image-generation and storyboard compliance, not video-platform behavior.

## Review Output

```markdown
## Prompt Safety Review

| Item | Status | Issue | Fix |
|---|---|---|---|
| NSFW / sexual content | pass / revise |  |  |
| Minors | pass / revise |  |  |
| Violence / gore | pass / revise |  |  |
| Real-person likeness | pass / revise |  |  |
| Copyrighted characters / brands | pass / revise |  |  |
| Hate / harassment | pass / revise |  |  |
| Sensitive personal data | pass / revise |  |  |

## Required Fixes
1. 
```

## NSFW And Sexual Content

Flag for revision when a prompt includes:

- Nudity, exposed genitals, exposed nipples, or explicit sexual anatomy.
- Sex acts, sexual contact, arousal-focused descriptions, or fetish framing.
- Pornographic framing, erotic intent, or camera language focused on sexual body parts.
- Ambiguous age combined with sexualized clothing, pose, lighting, or language.

Safer alternatives:

- Use non-explicit emotional intimacy, fashion styling, or romantic tension.
- Keep wardrobe non-nude and non-transparent.
- Describe mood and relationship dynamics without sexual acts or explicit anatomy.

## Minors

Flag for revision when a prompt includes:

- Sexualized depiction of a minor or age-ambiguous character.
- School-uniform, teen, childlike, or youthful cues combined with sensual framing.
- Harmful, exploitative, humiliating, or abusive treatment of minors.

Safer alternatives:

- Remove sexualized styling and framing.
- Clarify adult age only when the character is intended to be an adult.
- Keep minors in ordinary, non-sexual, non-exploitative contexts.

## Violence And Gore

Flag for revision when a prompt includes:

- Graphic injury, gore, dismemberment, exposed organs, or excessive blood.
- Torture, sadistic framing, or realistic self-harm.
- Violence involving minors or vulnerable people.

Safer alternatives:

- Use implied danger, aftermath, shadows, or non-graphic conflict.
- Keep injuries mild, non-graphic, and story-relevant.
- Focus on emotion, consequence, or suspense rather than bodily detail.

## Real-Person Likeness

Flag for revision when a prompt includes:

- A living public figure, celebrity, influencer, private person, or client likeness without consent.
- Face-swap, identity transfer, or "make this person look like" requests without clear rights.
- Biometric or identity-specific details taken from private photos.

Safer alternatives:

- Create a fictional character with broad, non-identifying traits.
- Use consented reference material only.
- Preserve approved fictional character IDs instead of real-person names.

## Copyrighted Characters And Brands

Flag for revision when a prompt includes:

- Named copyrighted characters, franchise-specific costumes, logos, or protected designs.
- "In the exact style of" a living artist or highly specific protected visual identity.
- Brand logos or trademarks used as central visual elements without rights.

Safer alternatives:

- Describe generic genre traits, mood, era, medium, and composition.
- Remove logos unless the user confirms rights or the use is clearly authorized.
- Use original character and costume IDs in the storyboard bible.

## Hate, Harassment, And Abuse

Flag for revision when a prompt includes:

- Dehumanizing, hateful, or degrading content targeting protected classes.
- Harassment, humiliation, or non-consensual sexualized framing of a person.
- Slurs or symbols used to promote hate.

Safer alternatives:

- Reframe conflict without protected-class targeting.
- Remove degrading or exploitative visual framing.
- Use neutral descriptors and story-relevant tension.

## Sensitive Personal Data

Flag for revision when a prompt includes:

- Personal addresses, phone numbers, IDs, medical records, financial data, or login information.
- Private documents, screenshots, or identifiable records not required for the storyboard.
- Confidential client, company, or production information intended to remain private.

Safer alternatives:

- Replace real data with fictional placeholders.
- Remove visible private documents from the frame.
- Keep only the production detail necessary for the shot.

## Rewrite Pattern

When revising a risky prompt:

```text
Preserve: [story purpose, character role, composition, emotional beat, approved style]
Remove or change: [specific unsafe or rights-risk element]
Replace with: [safe visual alternative]
Do not change: [continuity-critical details]
Output: [revised image prompt]
```

Prefer minimal rewrites that preserve the storyboard intent.
