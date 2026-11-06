# Image Director

<img src="skills/image-director/assets/chef-light-1024.png" alt="Image Director chef mascot" width="128">

A skill by Prabal for directing image generation through careful reference analysis, intentional styling, believable photography, and staged visual problem solving.

The workflow moves from brief and reference analysis to input preparation, prompting, generation, and diagnosis. Imperfections and photographic restraint are flexible creative choices, not mandatory filters. Reference boards use manually assembled original images rather than AI-generated collages.

The skill is in [`skills/image-director/SKILL.md`](skills/image-director/SKILL.md). It needs a host with image-generation or editing capabilities to produce images; it does not bundle an image engine.

## Use in Codex

Ask Codex:

```text
Use $skill-installer to install the image-director skill from
https://github.com/Prabal2004/image-director/tree/main/skills/image-director
```

Once installed, attach your references and write:

```text
Use $image-director to create a realistic product photograph of my packaging.
Use the attached artwork exactly. Borrow the lighting from reference 1 and
the composition from reference 2. Output a square image for social media.
```

You can also ask for an illustration, a new composition, a mockup, or a revision such as: "This still looks too artificial; diagnose the lighting and material response before regenerating."

For manual local installation, copy the complete `skills/image-director` folder into your project's `.agents/skills/` directory or your user-level `~/.agents/skills/` directory. Codex detects skills automatically; restart if it does not appear.

In this source checkout, before installation, ask Codex to read `skills/image-director/SKILL.md` and follow it for your image brief.

## ChatGPT

The root `plugin.json` packages the skill for ChatGPT and Codex. Public directory review and publication are separate from GitHub availability. For a manual trial, attach `SKILL.md` and your reference images to a chat with image generation available and ask ChatGPT to follow the workflow.

## Claude Code

The `.claude-plugin/plugin.json` manifest exposes the same `skills/` directory. To try a local checkout, launch `claude --plugin-dir /absolute/path/to/image-director` and use `/image-director:image-director` with your brief. Image generation still requires a suitable tool in the host.

Claude's manifest includes the chef icon for its directory listing. Claude Code's documented runtime ignores that listing icon, so an icon beside a skill invocation is not guaranteed.

## Icon and policies

Chef icon SVGs and PNGs are in `skills/image-director/assets/`. The OpenAI plugin includes light and dark variants. Skill-level Codex metadata includes small and large icons.

[Support](SUPPORT.md) · [Privacy](PRIVACY.md) · [Terms](TERMS.md)

## Status

Initial workflow version. No reference assets are bundled yet. Image generation requires the host's own tools and access; this repository does not include an API key or image-generation service.

Usage and local discovery follow the [official skills documentation](https://learn.chatgpt.com/docs/build-skills).
