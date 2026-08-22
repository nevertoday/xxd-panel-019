<div align="center">

# XXD Panel 019

### Reconstruct a specific photographed subject and relationship as a modernist illustration that remains recognisable

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-000000?style=flat-square)](./SKILL.md)
[![Four Modes](https://img.shields.io/badge/Modes-4-d18437?style=flat-square)](#four-outputs-one-recognition-system)
[![Raster Output](https://img.shields.io/badge/Output-PNG-355c7d?style=flat-square)](#boundaries-and-trust)

<a href="README.md">简体中文</a> · <strong>English</strong> · <a href="README.ja.md">日本語</a>

</div>

> RECOGNISE FIRST · REDUCE WITH INTENT · COMPOSE WITH TYPE

XXD Panel 019 is an image-generation skill for Codex and compatible agents. It translates subject, posture, direction, proportion, and inseparable relationships into recognisable retro-modernist flat illustration. It is neither vector tracing nor an excuse to erase the source under generic geometry.

Reduction should remove noise, not identity.

## Why it exists

Many photo-to-flat-illustration workflows collapse into a universal visual kit: people become faceless silhouettes, a real place becomes a sun and road, colours come from a template, and type becomes decorative filler. The image looks designed but no longer belongs to the photograph.

019 requires at least three source-specific identity cues in every transformed frame—outer contour, posture, direction, proportion, overlap, negative shape, or distance between subjects. The geometry may be bold, but the viewer should still recognise which scene is being retold.

```text
source photo → identify subject and relation → lock identity cues → extract 3–5 colours → reconstruct → typeset → inspect
```

## The 019 visual contract

- **Recognition first:** preserve subject and relationship before pursuing graphic tension.
- **At least three identity cues:** contour, posture, proportion, direction, overlap, and negative shape work together.
- **Three to five source colours:** the palette comes from the photograph, not an example or template.
- **Positive/negative shape and scale:** large planes, hard facets, concise curves, and void create the eye path.
- **Restrained print character:** light halftone, paper, and registration texture support flat hierarchy rather than glossy 3D.
- **Editorial typography:** title and microcopy participate in geometry, visual weight, and spatial rhythm.

## Four outputs, one recognition system

If no mode is specified, the skill asks first. Dimensions may be supplied at the same time; exact pixels take priority.

| Mode | Default canvas | Deliverable |
| --- | ---: | --- |
| `top-bottom` | 3:4 | original photo above, 019 illustration below, exact 50/50 split |
| `left-right` | 3:2 | original photo left, 019 illustration right, exact 50/50 split |
| `design-only` | 3:4 | one complete transformed illustration with no visible source photo |
| `wallpaper-pack` | four device sizes | separate phone, iPad, desktop, and watch PNGs |

Photography in paired modes remains truthful, with only restrained grading and necessary environmental extension. In design-only and wallpaper modes, the photograph supplies subject, relation, colour, and copy evidence but does not appear in the result.

### Wallpaper packs: one family, not one image

Defaults are phone `1440×3200`, iPad `2048×2732`, desktop `3840×2160`, and watch `1024×1024`; each can be overridden.

- **Linked pack (recommended):** generate and approve the iPad anchor first; the other three receive the original photo plus that same anchor and are recomposed for their own devices.
- **Independent set:** every device receives only the source photograph and may explore more freely.

A linked pack carries palette, graphic grammar, print character, and typographic rhythm across devices, while solving subject position, hierarchy, type, and safe areas anew. It never crops one master or chains references sequentially.

## Copy must belong to the image

Copy is on by default. Automatic copy does not reach for generic words such as “Memory”, “Dream”, or “Journey”. It reads visible fact, relational tension, and grounded subtext, then finds a title that makes the viewer see the photograph again.

The title must pass the unrelated-image swap test. If it works just as well on another photograph, it does not belong here. Microcopy must extend the same semantic core rather than fill the layout with random serial numbers or pseudo-archive labels.

Finished user wording remains verbatim. A direction or editable draft is transcreated only after preserving audience, purpose, mandatory wording, tone, and implication.

Language priority:

```text
target market or audience > requested output language > direction language > request language
```

A Japanese edition uses natural Japanese and Japanese line-breaking rules; a Korean edition uses natural Korean and correct spacing; a UK edition uses British English. The skill never infers nationality from appearance and never uses pseudo-foreign text.

## Scripts guarantee geometry; image generation creates the illustration

`scripts/compose_panel.py` handles planning, exact 50/50 raster composition, final dimensions, and auditing. It never substitutes SVG or programmatic colour blocks for real bitmap generation.

```bash
python3 scripts/compose_panel.py --plan --layout top-bottom
python3 scripts/compose_panel.py --plan --layout left-right --size 2560x1440
python3 scripts/compose_panel.py --audit result.png --layout design-only --size 2048x2048
```

Exact top-bottom canvases require an even total height; left-right canvases require an even total width. Odd dimensions are never silently changed.

## Get started

```bash
git clone https://github.com/nevertoday/xxd-panel-019.git
mkdir -p ~/.codex/skills
ln -s "$(pwd)/xxd-panel-019" ~/.codex/skills/xxd-panel-019
```

Claude Code users can link the same folder to `~/.claude/skills/xxd-panel-019`. Restart the agent session after installation.

```text
$xxd-panel-019
Turn this photo into a linked four-device wallpaper pack. Use British English for the main title.
```

You may also invoke the skill with only a photograph. It asks for the output mode in a numbered multiline menu, then asks whether a wallpaper pack should be linked or independent when necessary.

Full specifications:

- [Skill workflow](SKILL.md)
- [Chinese full prompt](references/xxd-panel-019-prompt.zh-CN.md)
- [English full prompt](references/xxd-panel-019-prompt.en.md)

## Boundaries and trust

- The current photograph is the current task's only content source; no other input, old result, or bundled example is borrowed.
- Every invocation opens a fresh task directory, even with identical source and parameters.
- Final deliverables are PNG bitmaps, never SVG, HTML, Canvas, or programmatic drawing substitutes.
- The configured bitmap bridge emits sanitised status only and does not print providers, endpoints, headers, credentials, prompts, or server response bodies.
- Ordinary modes return one result per source; wallpaper mode returns exactly four separate files, never a contact sheet.

Local composition needs Python 3 and Pillow. The safe bitmap bridge uses Python 3.11+ `tomllib`. Generation still requires a host agent with built-in raster generation or an already configured compatible raster route.

## Repository

```text
xxd-panel-019/
├── SKILL.md
├── README.md / README.en.md / README.ja.md
├── agents/openai.yaml
├── scripts/
│   ├── compose_panel.py
│   └── configured_imagegen.py
└── references/
    ├── xxd-panel-019-prompt.zh-CN.md
    └── xxd-panel-019-prompt.en.md
```

## About XXD

XXD is the abbreviated brand name of Xiaoxiaodong. This project is created and maintained by [@xiaoxiaodong01](https://x.com/xiaoxiaodong01).

## Community and Member Prompt Library

### Skills Q&A · CNY 99

The fee covers Q&A support for using the Skills. [Join through Knowledge Planet](https://wx.zsxq.com/group/15554814142882), or scan the WeChat QR code below with questions about access or payment.

<p align="center">
  <a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="XXD paid community WeChat QR code" width="320"></a>
</p>

### Member Prompt Library · CNY 699/year

The [XXD Member Prompt Library](https://vip.xiaoxiaodong.ai/) is available as a self-service annual membership for CNY 699.

<div align="center">

**Reduce the image, not its identity.**

</div>
