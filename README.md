# Videoprompt

A skill for writing **production-grade AI video-generation prompts** in the *Seedance 2.5 shot-memo style* — fixed sections in a fixed order, beat-level timing, locked character identity, motivated lighting, and a hard must-hit checklist.

Everything here is reverse-engineered from three working Seedance 2.5 production templates (kept verbatim in [`references/seedance-examples.md`](references/seedance-examples.md)).

## What it does

Turns a shot idea into a prompt any shot-based video model can consume (Seedance, Veo, Kling, Sora, Hailuo…), for:

- character beats and dialogue scenes with verbatim screenplay dialogue
- aerial / VFX shots and scene extensions ("direct continuation of @Video 1")
- converting a scene, beat, or storyboard frame into a full shot memo

**Core ideas behind the format:**

1. **Write a shot memo, not a pitch** — each section answers exactly one department-head question.
2. **Positive constraints** — state what WILL be true; name "no X" only against known AI failure modes.
3. **Redundancy on load-bearing facts** — dialogue, hero staging, and end-states appear 2–3× across sections.
4. **Lock identity twice** — every recurring element gets an `@tag` *and* a full physical description.
5. **Screen-space directions + metric anchoring** — "to the LEFT of frame", "about 5 meters wide, clearly smaller than the observatory".
6. **Name the failure mode, not the fear** — write the antidote to the default cheesy version of the shot.

The full method — a 17-section skeleton, beat math, extension rules, failure-mode antidote table, and a pre-flight checklist — lives in [`SKILL.md`](SKILL.md).

## Install

Copy the `videoprompt/` folder into your agent's skills directory, e.g. for ZCode:

```
~/.zcode/skills/videoprompt/
├── SKILL.md                      # the method: principles, skeleton, checklist
└── references/
    └── seedance-examples.md      # 3 verbatim production templates
```

Restart your agent session and ask it to "write a video prompt for …" — the skill triggers on any prompt-writing or shot-description task.

## Usage example

Ask your agent:

> Write a 4-second Seedance prompt: night exterior, a woman spray-paints the word "GALAXY" next to "FOOD" on her delivery van while a small alien watches from the roof.

You get a copy-paste-ready shot memo with `PACING / ENERGY / EMOTION / LOCATION MAP / FORMAT MODE / OPTICS / CAMERA / ACTION TIMING / LIGHTING / AUDIO / CHARACTER ACTING / STYLE / POSITIVE CONSTRAINTS` sections and the fixed quality footer.

## License

[MIT](LICENSE) © 2026 MichaelCao1
