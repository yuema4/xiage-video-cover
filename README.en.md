# Xiage Video Cover

[简体中文](README.md) · [Skill instructions](SKILL.md)

Turn a video script and portrait references into bold, topic-driven thumbnails in three aspect ratios.

This is a **Codex workflow skill** developed through real cover-design sessions at Xiage Studio. The assistant extracts the main hook, writes the headline, designs the composition, and calls an image-generation tool. The creator supplies the content, portrait references, and feedback. It is not a standalone application, an image model, or a video editor.

![Skill launch cover](examples/skill-launch-16x9.png)

## Features

- Extract one clear audience benefit or central outcome from a script.
- Create a short headline and supporting subtitle.
- Use portrait references to preserve the creator’s facial features, hairstyle, and natural appearance.
- Develop a visual theme for each topic instead of forcing every cover into one template.
- Produce a master cover, refine it through feedback, then recompose each landscape version.
- Review text, likeness, overlap, thumbnail readability, and actual image dimensions.

| Aspect ratio (width:height) | Layout | Suggested dimensions |
| --- | --- | --- |
| 3:4 | Portrait master | 1080×1440 |
| 16:9 | Widescreen landscape | 1600×900 |
| 4:3 | Compact landscape | 1440×1080 |

These dimensions are suggestions, not guaranteed generation sizes. Other exact-ratio dimensions are acceptable; verify the delivered files.

## Requirements and installation

Use a Codex environment that supports local skills and provides the `imagegen` skill plus the built-in image-generation tool. This repository contains workflow instructions and does not install those capabilities. Generation availability, usage limits, and latency depend on your environment. The default built-in route does not ask for a separate API key; an explicitly chosen API route requires its own configuration.

Download the repository and ask Codex:

```text
Install this repository's SKILL.md as my personal xiage-video-cover skill.
If a skill with that name already exists, compare it before updating
and preserve my customizations.
```

Alternatively, place `SKILL.md` inside a `xiage-video-cover/` folder in the personal skills directory used by your Codex environment. The author's environment uses `~/.codex/skills/xiage-video-cover/SKILL.md`; follow your own environment's configuration. Check that the skill is available after installation, opening a new task if needed.

## Quick start

Attach a script and portrait photos, then send:

```text
Use $xiage-video-cover to create the cover for this video.

Script: [paste script]
Portrait references: [attach photos]
Brand name: [your name]
Cover text language: English
Special requests: [optional]

Choose the headline and visual direction. Create a 3:4 master first.
Once I approve it, adapt it to 16:9 and 4:3 landscape versions.
```

The skill instructions are written in Chinese. The default signature is “夏哥研究室” (Xiage Studio); explicitly specify your own brand, language, colors, or layout to override it.

## Workflow

1. **Supply inputs:** a script or summary and portrait references. Existing covers and real product screenshots are optional.
2. **Find the hook:** focus on the main outcome or audience value; the opening anecdote does not have to become the cover theme.
3. **Design the master:** generate a 3:4 composition with clear text hierarchy and a topic-specific visual treatment.
4. **Refine:** give concrete feedback such as “make the portrait larger” or “simplify the background.”
5. **Adapt:** after the master is approved, recompose both landscape versions. Requesting the complete set directly allows continuous production.
6. **Deliver:** review the images and provide final files, actual dimensions, and saved generation prompts.

The skill stores a workflow, not persistent access to old photos. Attach references again in a new conversation or provide accessible file locations.

## Real examples

| Dunhuang astronomy game | AI motion-graphics workflow | Talking-head packaging skill |
| --- | --- | --- |
| ![Ancient scroll and stars](examples/dunhuang-3x4.png) | ![Blue and violet editing workspace](examples/ai-editing-3x4.png) | ![Orange and black launch design](examples/skill-launch-3x4.png) |
| Scrolls, stars, and gold constellation lines | Portrait, visual-effects panels, and timeline | Four style cards and a launch headline |

Compare the same topic in [16:9](examples/skill-launch-16x9.png) and [4:3](examples/skill-launch-4x3.png) to see how the layout changes.

These are actual generated examples shared with the creator's permission, not guarantees of identical future results. Interface panels and style cards are conceptual illustrations. Product names and claims appearing in example artwork belong to those video topics and are not this project's dependencies or performance guarantees.

## Limits and review

- Generated images may contain text errors, identity drift, or hand artifacts. Inspect and iterate; one-pass success is not guaranteed.
- Do not describe a multi-step process as “one click” or add unsupported speed, revenue, or zero-rework claims.
- Use real screenshots when accurate product representation matters.
- Recompose each ratio without stretching the person or clipping the headline.
- This repository includes final example artwork, not original portrait photos, private machine paths, or account credentials.

## Repository layout

```text
xiage-video-cover/
├── SKILL.md       # Executable workflow instructions, in Chinese
├── README.md      # Chinese project guide
├── README.en.md   # English project guide
└── examples/      # Cover examples approved for public display
```

An independent creator project, not an official OpenAI project. See the [official OpenAI skill documentation](https://developers.openai.com/plugins/build/skills) for the skill format.

## Usage and permissions

No open-source license is currently included. Public display does not grant unrestricted redistribution, commercial use, or rights to the creator's likeness. Contact the author for those permissions and use photos and assets you have permission to use for your own covers.
