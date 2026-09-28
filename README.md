# Photo to Art-book Print

A portable Codex Skill for transforming an uploaded photograph into a quiet, handmade, print-like illustration on warm paper.

The Skill preserves recognizable people, poses, clothing, objects, and spatial relationships while reducing the scene to restrained color shapes, uneven pen work, broken pigment, and a sparse background. It produces one 3:4 portrait illustration and explicitly prevents photo panels, comparison layouts, invented captions, watercolor, colored pencil, cartoon styling, and other common style drift.

## Use

Attach a photograph and invoke the Skill:

```text
Use $photo-to-artbook-print to transform this photograph into a quiet handmade art-book print illustration.
```

You can add scene-specific instructions, such as asking to omit a background object or supplying exact title text. Without supplied text, the Skill adds no title, location, name, or date.

## Install from GitHub

Clone or download this repository, then place the `photo-to-artbook-print` folder in your Codex skills directory:

```text
~/.codex/skills/photo-to-artbook-print/
```

Restart or reload Codex if needed so it can discover the new Skill.

## Requirements

- Codex with the built-in image-generation tool available
- A photograph attached in the conversation, or a local image that Codex can inspect first

No scripts, API key, or third-party dependencies are required for the default built-in workflow.

## Repository contents

- `SKILL.md` — trigger, workflow, generation specification, and validation rules
- `agents/openai.yaml` — Codex UI metadata
- `README.md` — usage and distribution notes
- `LICENSE` — MIT license

## License

MIT
