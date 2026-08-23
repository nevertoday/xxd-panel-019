<p align="center">
  <img src="./assets/banner.svg" alt="XXD Panel 019 project banner" width="1200">
</p>

<div align="center">

# 🦁 XXD Panel 019

### Reconstruct a specific photographed subject and relationship as a modernist illustration that remains recognisable

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-000000?style=flat-square)](./SKILL.md)
[![Four Modes](https://img.shields.io/badge/Modes-4-d18437?style=flat-square)](#four-outputs-one-recognition-system)
[![Raster Output](https://img.shields.io/badge/Output-PNG-355c7d?style=flat-square)](#boundaries-and-trust)

<a href="README.md">简体中文</a> · <strong>English</strong> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.ar.md">العربية</a>

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

## Samples · from X

> [Xiaoxiaodong (@xiaoxiaodong01)](https://x.com/xiaoxiaodong01/status/2090144142366233008) · 19 August 2026<br>
> GPT2 × retro × flat × aesthetic prompt × VOL.019<br>
> The post also demonstrates language preference: naming a target such as Spanish lets the copy transcreate naturally for that audience.

<table>
  <tr>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="https://pbs.twimg.com/media/HQGvA3TasAAH3cc.jpg?format=jpg&amp;name=large" alt="XXD Panel 019 sample 1"></a></td>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="https://pbs.twimg.com/media/HQGvA3RbgAA_3_D.jpg?format=jpg&amp;name=large" alt="XXD Panel 019 sample 2"></a></td>
  </tr>
  <tr>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="https://pbs.twimg.com/media/HQGvA3RbAAAP0Wj.jpg?format=jpg&amp;name=large" alt="XXD Panel 019 sample 3"></a></td>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="https://pbs.twimg.com/media/HQGvA3aboAAuH6f.jpg?format=jpg&amp;name=large" alt="XXD Panel 019 sample 4"></a></td>
  </tr>
</table>

<p align="center"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008">View the original post and full prompt →</a></p>

These samples demonstrate the 019 aesthetic motive; they do not turn the post's earlier canvas into a current default. The four modes still follow the source-adaptive and custom sizing logic below.

## Four outputs, one recognition system

The four modes support single or multiple selection. Reply with `1`, `1+3`, `1,2,4`, or `all`; the Skill deduplicates and runs them in menu order 1→4. Every mode is delivered independently in its own task directory—never as an overview—and `all` yields seven PNGs per source (one for each ordinary mode plus four wallpapers). Sizes may be labelled by mode in the same reply; unlabeled ordinary modes remain source-adaptive. Copy is shared across selected modes by default and may be overridden per mode.

| Mode | Sizing logic | Deliverable |
| --- | ---: | --- |
| `top-bottom` | source-adaptive | original photo above, 019 illustration below, each panel retains the complete source size; exact 50/50 split |
| `left-right` | source-adaptive | original photo left, 019 illustration right, each panel retains the complete source size; exact 50/50 split |
| `design-only` | source-adaptive | one complete transformed illustration with no visible source photo; retains the source ratio and dimensions |
| `wallpaper-pack` | four device sizes | separate phone, iPad, desktop, and watch PNGs |

Photography in paired modes remains truthful, with only restrained grading and necessary environmental extension. In design-only and wallpaper modes, the photograph supplies subject, relation, colour, and copy evidence but does not appear in the result.

### Wallpaper packs: one family, not one image

Wallpaper-pack has no silent size default. Choose the common device preset—phone `1440×3200`, iPad `2048×2732`, desktop `3840×2160`, watch `1024×1024`—or provide labeled custom sizes.

- **Linked pack (recommended):** generate and approve the iPad anchor first; the other three receive the original photo plus that same anchor and are recomposed for their own devices.
- **Independent set:** every device receives only the source photograph and may explore more freely.

A linked pack carries palette, graphic grammar, print character, and typographic rhythm across devices, while solving subject position, hierarchy, type, and safe areas anew. It never crops one master or chains references sequentially.

## Copy must belong to the image

Before generation, choose automatic copy, custom copy, or text-free output, and name the target language or locale for the first two. Automatic copy does not reach for generic words such as “Memory”, “Dream”, or “Journey”. It reads visible fact, relational tension, and grounded subtext, then finds a title that makes the viewer see the photograph again.

The title must pass the unrelated-image swap test. If it works just as well on another photograph, it does not belong here. Microcopy must extend the same semantic core rather than fill the layout with random serial numbers or pseudo-archive labels.

Finished user wording remains verbatim. A direction or editable draft is transcreated only after preserving audience, purpose, mandatory wording, tone, and implication.

Language priority:

```text
target market or audience > requested output language > direction language; if none is explicit, ask before generation
```

A Japanese edition uses natural Japanese and Japanese line-breaking rules; a Korean edition uses natural Korean and correct spacing; a UK edition uses British English; and an Arabic edition uses natural Modern Standard Arabic, correct shaping, and right-to-left composition. The skill never infers nationality from appearance and never uses pseudo-foreign text.

## Scripts guarantee geometry; image generation creates the illustration

`scripts/compose_panel.py` handles planning, exact 50/50 raster composition, final dimensions, and auditing. It never substitutes SVG or programmatic colour blocks for real bitmap generation.

```bash
python3 scripts/compose_panel.py --plan --layout top-bottom --source photo.png
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

You may also invoke the skill with only a photograph. It asks for one or more output modes in a numbered multiline menu, then asks whether a wallpaper pack should be linked or independent when necessary.

Full specifications:

- [Skill workflow](SKILL.md)
- [Chinese full prompt](references/xxd-panel-019-prompt.zh-CN.md)
- [English full prompt](references/xxd-panel-019-prompt.en.md)

## Boundaries and trust

- The current photograph is the current task's only content source; no other input, old result, or bundled example is borrowed.
- Every invocation opens a fresh task directory, even with identical source and parameters.
- Final deliverables are PNG bitmaps, never SVG, HTML, Canvas, or programmatic drawing substitutes.
- The configured bitmap bridge emits sanitised status only and does not print providers, endpoints, headers, credentials, prompts, or server response bodies.
- Each selected ordinary mode returns one file; selected `wallpaper-pack` adds four separate wallpapers. `all` returns seven PNGs per source across four sibling mode directories, never a contact sheet or overview.

Local composition needs Python 3 and Pillow. The safe bitmap bridge uses Python 3.11+ `tomllib`. Generation still requires a host agent with built-in raster generation or an already configured compatible raster route.

## Repository

```text
xxd-panel-019/
├── SKILL.md
├── README.md / README.en.md / README.ja.md / README.ko.md / README.ar.md
├── agents/openai.yaml
├── assets/banner.svg
├── scripts/
│   ├── compose_panel.py
│   └── configured_imagegen.py
└── references/
    ├── xxd-panel-019-prompt.zh-CN.md
    └── xxd-panel-019-prompt.en.md
```

## About XXD

XXD is the abbreviated brand name of Xiaoxiaodong. This project is created and maintained by [@xiaoxiaodong01](https://x.com/xiaoxiaodong01).

## Support and Membership

### In-depth Consultation · CNY 299/hour

One-to-one in-depth consultation for using the Skills is billed at CNY 299 per hour. To book a session, contact Xiaoxiaodong through the WeChat QR code below.

### Xiaoxiaodong Skills User Community · CNY 99 to join

A one-time CNY 99 fee joins the user community for sharing workflows, discussing work, and peer support. It does not include hourly one-to-one in-depth consultation. Scan the WeChat QR code below and include “Skills User Community” in your message.

### Knowledge Planet + Member Prompt Library · CNY 699/year

The Knowledge Planet community and the [XXD Member Prompt Library](https://vip.xiaoxiaodong.ai/) are one membership: **one annual payment unlocks both, with no second purchase required.**

Choose either activation route:

1. Subscribe through [Knowledge Planet](https://wx.zsxq.com/group/15554814142882), then contact Xiaoxiaodong on WeChat for a Member Prompt Library redemption code.
2. Subscribe directly through the [Member Prompt Library](https://vip.xiaoxiaodong.ai/), then contact Xiaoxiaodong on WeChat for an invitation to Knowledge Planet.

<p align="center">
  <a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="XXD paid community WeChat QR code" width="320"></a>
</p>

<div align="center">

**Reduce the image, not its identity.**

</div>

---

<div align="center">
  <h2>☕ Support this open-source project</h2>
  <p>If this project saved you time, a Star, a share, or a coffee helps keep it moving.</p>
  <table>
    <tr>
      <td align="center" width="240">
        <a href="https://github.com/nevertoday/zhongguo-traditional-colors/blob/main/docs/images/buy-me-a-coffee-qr.png?raw=true"><img src="https://github.com/nevertoday/zhongguo-traditional-colors/blob/main/docs/images/buy-me-a-coffee-qr.png?raw=true" alt="Support Xiaoxiaodong through Buy Me a Coffee" width="180"></a><br>
        <strong>Buy me a coffee</strong><br>
        <sub>Scan or open the QR code to support Xiaoxiaodong</sub>
      </td>
    </tr>
  </table>
  <p><sub>Support is entirely optional and never changes access to this open-source project.</sub></p>
</div>
