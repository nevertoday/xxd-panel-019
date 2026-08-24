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
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="./assets/examples/sample-01.jpg" alt="XXD Panel 019 sample 1"></a></td>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="./assets/examples/sample-02.jpg" alt="XXD Panel 019 sample 2"></a></td>
  </tr>
  <tr>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="./assets/examples/sample-03.jpg" alt="XXD Panel 019 sample 3"></a></td>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="./assets/examples/sample-04.jpg" alt="XXD Panel 019 sample 4"></a></td>
  </tr>
</table>

<p align="center"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008">View the original post and full prompt →</a></p>

These samples demonstrate the 019 aesthetic motive; they do not turn the post's earlier canvas into a current default. The four modes still follow the explicit pre-generation canvas and custom sizing logic below.

## Four combinable output modes

Choose one or several modes with `1`, `1+3`, `1,2,4`, or `all`; `all` produces seven separate PNGs per source. After mode selection and before generation, the Skill explicitly asks for the whole finished canvas: the original-prompt `3:4`, an explicit source-aspect choice, a common ratio, or custom ratio/exact pixels. Source dimensions are never applied silently.

| Mode | Canvas rule | Result |
| --- | --- | --- |
| `top-bottom` | user-confirmed whole canvas | one complete generation: high-fidelity source above, 019 design below, approximately 50/50 |
| `left-right` | user-confirmed whole canvas | one complete generation: high-fidelity source left, 019 design right, approximately 50/50 |
| `design-only` | user-confirmed whole canvas | 019 design fills the canvas; source remains invisible |
| `wallpaper-pack` | confirmed per device | separate phone, iPad, desktop, and children's-watch PNGs |

Paired modes use the source as a high-fidelity edit/reference input and one complete style prompt to generate the finished composition directly, so photography, design, colour, light, typography, and meaning can cohere. Deterministic composition is fallback-only: after one targeted complete-canvas retry fails, when pixel-identical source preservation is explicitly required, when the active route cannot realise the canvas, or for lossless final pixel calibration.

Wallpapers may be linked or independent. A linked pack approves one iPad anchor, then recomposes every other device from the original plus that same anchor. An independent pack gives each device only the original. Neither crops another device output nor chains derivatives.

## Copy must belong to the image

Before generation, choose automatic copy, custom copy, or text-free output, and name the target language or locale for the first two. Automatic copy does not reach for generic words such as “Memory”, “Dream”, or “Journey”. It reads visible fact, relational tension, and grounded subtext, then finds a title that makes the viewer see the photograph again.

The title must pass the unrelated-image swap test. If it works just as well on another photograph, it does not belong here. Microcopy must extend the same semantic core rather than fill the layout with random serial numbers or pseudo-archive labels.

Finished user wording remains verbatim. A direction or editable draft is transcreated only after preserving audience, purpose, mandatory wording, tone, and implication.

Language priority:

```text
target market or audience > requested output language > direction language; if none is explicit, ask before generation
```

A Japanese edition uses natural Japanese and Japanese line-breaking rules; a Korean edition uses natural Korean and correct spacing; a UK edition uses British English; and an Arabic edition uses natural Modern Standard Arabic, correct shaping, and right-to-left composition. The skill never infers nationality from appearance and never uses pseudo-foreign text.

## Complete-canvas first, raster-only delivery

The image model owns the aesthetics of the entire finished composition; paired layouts also default to one complete-canvas generation. `scripts/compose_panel.py` remains only for condition-based recovery, lossless pixel calibration, and read-only audit. It is not run pre-emptively and does not judge aesthetic success.

Every deliverable is a raster PNG and every invocation creates a fresh task under `~/Desktop/xxd/`. The configured image route exposes sanitised status only—never providers, endpoints, credentials, headers, prompts, responses, or account details. SVG, HTML, Canvas, diagrams, and programmatic drawing are not substitutes for the final artwork.

## Selectable controls and inline parameters

When the host provides genuine interactive controls, the Skill prefers card-style selection: output modes and ordinary output sizes are multi-select, while copy mode and wallpaper relationship are single-select. Size choices include auto-fit, source aspect, 1:1, 3:4, 4:3, 4:5, 5:4, 2:3, 3:2, 9:16, 16:9, 21:9, 5:7, 7:5, and custom ratios or pixels. Without an interactive control, it falls back to a clear multiline numbered menu rather than showing fake checkboxes.

Every setting can also be supplied as an inline variable:

```text
/xxd-panel-019 photo.jpg --mode top-bottom,design-only --size auto,3:4,9:16 --text auto --locale ja-JP
```

Supported parameters include `--mode`, repeatable or comma-separated `--size`, `--text auto|custom|none`, `--locale`, `--copy`, `--wallpaper linked|independent`, `--wallpaper-size`, and `--out`. Complete parameters skip all preflight questions; partial parameters trigger only the missing questions. Different aspect ratios are independently recomposed, and the four-device wallpaper pack remains a separate branch rather than being multiplied by ordinary sizes.

## Image-model priority

GPT Image 2 is the default first choice. It keeps this project's established workflow: high-fidelity source reference, explicit whole-canvas selection before generation, one complete-canvas generation for paired modes, and scripted composition only as a conditional fallback.

Seedance 5.0 Pro, Nano Banana Pro (Gemini Image Pro), Nano Banana 2 (Gemini Image Flash), or another compatible bitmap model may also be used when it is actually available through the current tools or configured routes and can satisfy source fidelity, whole-canvas ratio, target-language text, and linked-wallpaper multi-reference requirements. An alternative changes only the generation route; it must not change modes, canvas, copy, locale, wallpaper relationship, or the complete-canvas-first strategy.

If no suitable route is available, the Skill asks the user to enable an image-generation tool or provide an API key. User-provided credentials may be used for the current task without being echoed, displayed, logged, or exposed. They are not persisted, and provider, account, billing, or global route configuration is not modified, unless the user explicitly requests that configuration change.

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
- [Original 019 style brief](references/019-source.md)

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
    ├── xxd-panel-019-prompt.en.md
    └── 019-source.md
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
