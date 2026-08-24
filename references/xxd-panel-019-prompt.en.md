# XXD Panel 019 · Full Generation Prompt (English)

## Runtime complete-canvas contract — highest priority

- `TOP_BOTTOM` and `LEFT_RIGHT` default to one complete finished generation using the current source as a high-fidelity edit/reference input. Do not pre-split the job into photographic and design halves.
- Top-bottom keeps the faithful source in approximately the upper 50% and performs this style transformation below; left-right uses the faithful source in approximately the left 50% and the transformation on the right. Unify both regions through colour, light, rhythm, typography, and meaning.
- `DESIGN_ONLY` and `WALLPAPER_PACK` use the complete canvas while the source remains an invisible identity/content reference. Recompose every wallpaper separately for its device.
- `FINAL CANVAS` means the ratio/pixels of the whole finished artwork and must be explicitly resolved before generation; never apply source dimensions silently. `DESIGN FRAME` is used only if a failed complete-canvas retry triggers deterministic composition fallback.
- Retry a failed complete canvas once against the failed constraint only. Scripted composition is allowed only after that retry still fails, when pixel-identical source preservation is explicitly required, when the active route cannot realise the canvas, or for lossless pixel calibration.

Treat the selected uploaded photograph as the sole content source. Each selected ordinary mode creates one finished premium editorial artwork for this photograph; selected wallpaper-pack creates four separate device wallpaper files under a caller-locked `INDEPENDENT` or `LINKED` relationship. Never combine them with another photo or turn any outputs into one overview, grid, collage, or series sheet.

Use one or more modes locked in section 7: photograph above and illustration below, photograph left and illustration right, one transformed illustration filling the canvas, and/or four separately recomposed device wallpapers. Each paired mode stays exact 50/50; source-hidden modes have no photographic region or seam. Before any generation call, explicitly resolve automatic copy, custom copy, or text-free output; automatic and custom copy also require a target language or locale.

The **transformed design frame** means the lower panel in top-bottom, the right panel in left-right, and the full canvas in design-only or each wallpaper output.

## 0. Aesthetic motive and generation-medium lock

Mode and device dimensions may change placement and aspect ratio, never the 019 aesthetic motive. Every transformed frame must visibly express: **this exact photographed subject or inseparable relationship → at least three source-specific identity cues → recognizable retro-modernist reconstruction → source-derived 3–5 color hierarchy → deliberate positive/negative shape and scale tension → editorial typography integrated into the geometry**.

If an unrelated photo could replace the source without materially changing the subject construction, spatial relationship, palette, or copy, the result is generic and must fail. When the photo contains specific vehicles, people, architecture, objects, poses, or relationships, do not reduce it to a generic sunset, sun-and-wave symbol, road icon, mountain silhouette, stock vector landscape, or decorative wallpaper. Device safe areas may move elements but must not erase source identity, illustration hierarchy, main title, or editorial typography.

Generate and edit all visual assets with an available raster image-generation capability and deliver PNG bitmaps. “Flat illustration,” “geometric plane,” or “vector-like edge” describes appearance only, never the file format. Do not substitute SVG, HTML, CSS, Canvas, diagrams, hand-coded vector markup, or programmatic drawing. Judge availability by actual capability, not a provider name or one environment variable; a missing variable does not prove that authentication or image generation is absent. Capability checks may expose only sanitized status and must never read out, display, log, or leak secret values. Explicitly invoking this skill and supplying the source image and mode confirms use of any already configured raster route for this PNG task; do not ask again merely because the built-in tool is unavailable and execution moves to a compatible configured route. Report a limitation only after safe checks confirm that no usable raster route exists.

Treat every invocation as a new generation job by default. Even when source, mode, and dimensions match an earlier job, generate a fresh result in a new task directory. Historical outputs are never current sources or completion evidence. Accept only current user attachments, explicit paths, or earlier user-supplied sources explicitly identified by the current request. Never scan the Desktop, workspace, or this skill's output root to improvise a source; if the intended source is inaccessible, request it instead of auditing and returning an old result.

## 1. Two roles of the source photo

The same photograph serves two roles:

1. **Photographic original in paired modes.** Show it above in top-bottom or left in left-right, preserving structure, material reality, natural light, perspective, and color atmosphere. Design-only and wallpaper-pack do not show it.
2. **Design evidence for the transformed frame.** Extract the most recognizable subject, outer contour, pose, orientation, proportions, center of gravity, depth relationships, and narrative action, then translate them into a retro-modernist flat illustration.

Do not borrow people, objects, scenes, colors, compositions, or decorations from other uploads, examples, or stock material. Every important form in the transformed frame must be traceable to a visible fact in this photograph. The sole exception is a `LINKED` wallpaper pack: an approved anchor wallpaper from this same source may serve as the second visual reference for the other three devices, but only to lock family resemblance. The original photo remains the sole authority for subject, pose, relationship, color provenance, and narrative content.

## 2. Internal design method

Complete this process internally without printing the analysis:

**OBSERVE → IDENTIFY → REDUCE → RECONSTRUCT → TYPESET → CHECK**

1. Identify the single principal narrative subject, or the smallest inseparable relationship in a multi-subject scene.
2. Lock onto the decisive identity cues: contour, pose, action, direction, proportion, overlap, or negative shape.
3. Remove surface texture, realistic detail, background noise, and low-information decoration.
4. Rebuild the subject with silhouettes, geometric color planes, hard facets, and concise curves. Make it correspond immediately to the original before pursuing graphic drama.
5. Extract three to five defining source colors and create a clear editorial hierarchy for the title and microcopy.
6. Check the fixed proportions, cross-panel identity, color provenance, language, and every exclusion.

This is not tracing, automatic vectorization, a filter, a complete realistic illustration, or unrelated abstraction. Preserve the minimum clear identity cues and compress real relationships into an ordered graphic language.

## 3. Faithful photography — paired modes only

The photographic panel must remain photographic rather than redrawn or illustrated. Skip this section in design-only and wallpaper-pack, where the source remains reference evidence only.

- Preserve the subject's structure, proportions, identity, pose, real material quality, natural light, lens perspective, and original color atmosphere.
- Permit only restrained editorial grading of exposure, contrast, highlights, shadows, white balance, and color purity, giving the image the finish of an art magazine, independent publication, or exhibition photograph.
- To fit the photographic frame (whose shape follows the mode and canvas chosen in section 7), naturally extend sky, ground, water, wall, or environmental background. Any extension must match the source lighting, grain, perspective, and color without visible seams.
- Never stretch, squash, warp, change the pose, replace clothing, reshape facial features, or alter identity.
- Do not crop away a decisive contour or action merely to force the layout.
- Place no title, caption, number, sticker, or typography in the photographic frame of either paired mode.
- Avoid heavy filters, HDR, excessive sharpening, skin smoothing, cyberpunk grading, aggressive split toning, and visible generative outpainting artifacts.

## 4. Transformed design: retro-modernist flat illustration

Reconstruct the same subject and relationship as a concise, vivid, restrained, and recognizable flat illustration.

### 4.1 Recognition first

- The subject must correspond immediately to the source original. Preserve its decisive proportions, contour, pose, direction, and structural relationship.
- Do not mechanically trace interior details, copy photographic texture, or rebuild a complete realistic scene.
- Use one primary visual anchor. Secondary forms may support space, action, or scale but must not become an unrelated second focal point.
- The subject may be enlarged, cropped, offset, layered, or allowed to leave the transformed-frame edge, but it must retain its identity.

Adapt to content:

- **People:** preserve head-to-body proportion, posture, direction, the broad clothing silhouette, and the key action; retain facial or hand detail only when indispensable.
- **Animals:** preserve the defining outer contour, limb movement, and head direction; omit fur detail.
- **Plants:** preserve growth direction, branch rhythm, crown width, or foliage-mass relationships; omit veins.
- **Architecture:** retain one to three cues such as skyline contour, taper, arch, spire, eave line, or layered rhythm.
- **Objects and vehicles:** preserve overall form, functional negative shapes, proportions, and direction; remove mechanical and material detail.
- **Natural landscapes:** compress them into terrain blocks, horizontal axes, curves, and scale relationships rather than realistic scenery.

### 4.2 Graphic construction

- Primary vocabulary: clear silhouettes, flat geometric color planes, hard-edged facets, and concise curves.
- Emphasize visual center, scale contrast, foreground/background hierarchy, positive and negative shape, cropping, and geometric rhythm.
- A few circles, rectangles, arcs, oblique planes, or structural lines may establish space, but each must answer a real source relationship.
- Keep edges crisp and forceful, with at most slight old-print imperfection. Do not turn the panel into dirty texture or painterly realism.
- Exclude 3D volume, realistic reflections, lens glow, glassmorphism, card shadows, cel animation, and generic vector-template graphics.

## 5. Color system

Extract the photograph's most recognizable and energetic colors and reorganize them into a strict **three-to-five-color vintage limited palette**.

The roles normally include:

- one dominant field color;
- one dark structural color;
- one light ground or breathing color;
- zero to two small contrast accents.

Colors may be purified, simplified, or artistically translated, but each must have a source in the photograph. Build hierarchy through area, overlap, negative space, and value contrast rather than complex gradients.

Avoid muddy mixtures, too many competing colors, unsupported complements, neon or fluorescent hues, candy-cartoon palettes, rainbow gradients, cheap retro filters, and equal use of every color.

## 6. Modernist editorial typography

Typography appears only in the transformed design frame and functions as part of the illustration.

### 6.1 Copy mode and user priority

Copy has no silent default. Before generation, explicitly resolve source-derived automatic copy, user-supplied custom copy, or text-free output; automatic and custom copy also require a target language or locale. Lock a separate copy package for every photo using this priority:

1. **The user explicitly requests no copy, no text, or a purely visual result:** render no letters, characters, numbers, title, caption, or decorative pseudo-text anywhere.
2. **The user supplies finished wording:** preserve it verbatim without rewriting, translating, adding, or removing words; adapt only size, position, and typographic relationships.
3. **The user supplies a copy direction, theme, tone, or keywords:** write one definitive version to that direction without presenting alternatives.
4. **The user has not resolved copy mode or target language/locale:** stop before image generation and ask one concise preflight question offering automatic copy, custom copy, or text-free output; automatic/custom also require a language or locale. Never guess and continue.

For multiple photos, build an independent copy package for each one. A shared creative direction may govern the batch, but each photo still receives distinct source-aware wording unless the user explicitly requests identical copy.

Resolve copy locale separately from the language used to issue the command. For automatic or direction-led copy, use: **explicit target market/audience locale > explicit output language > language of the supplied direction or draft; if none is explicit, ask before generation**. Thus a Chinese instruction asking for a Japanese edition produces natural Japanese; a Korean-audience request produces natural Korean; a UK edition uses British English; and an Arabic edition uses natural Modern Standard Arabic unless the user names a regional variety. Never infer nationality, ethnicity, or audience language from a face, name, clothing, scenery, filename, metadata, or visible signage.

Localize by transcreation, not word-for-word translation: preserve the semantic core and moment of recognition, then rebuild it through native syntax, register, idiom, punctuation, and line breaking. Arabic uses natural Modern Standard Arabic unless a regional variety is requested, correct connected shaping, right-to-left reading order, Arabic punctuation, semantic line breaks, and deliberate bidirectional handling of embedded Latin text or numerals; reverse typographic flow and alignment without blindly mirroring the source-derived composition. Japanese uses natural contemporary wording, an appropriate kanji/kana balance, Japanese punctuation, and kinsoku-aware breaks. Korean uses natural contemporary wording, correct spacing, and intact Hangul syllable blocks without decorative pseudo-Hanja. UK English uses British spelling, vocabulary, punctuation, date conventions, and culturally natural understatement rather than American wording. Apply the same native-register principle to every other locale. Finished user copy remains verbatim; when it conflicts with a named target locale and translation/localization permission is unclear, ask one concise clarification.

Distinguish immutable finished copy from an editable direction or draft. Finished copy is the semantic authority: preserve it verbatim, understand its emphasis, turn, double meaning, addressee, and tone, then present it professionally through scale, position, void, line breaks, and geometric relationships. Break lines by semantic phrase; never split a fixed expression, create a false ambiguity, or demote a crucial word into unreadable microtype. For a direction or draft, first lock audience, communication goal, mandatory wording, tone, and subtext, then refine only within the permission given. Ask one concise question only when ambiguity would materially change the message; otherwise take the most conservative faithful reading.

### 6.2 Semantic distillation, language, and content

- Use the resolved target-locale language above; an explicit audience locale overrides the command language. When none of those signals is explicit, ask before generation; do not silently follow the request language.
- Before writing automatic or direction-led copy, make a private three-level reading: literal fact (the visible subject, action, direction, distance, material, light, or spatial relationship); relational tension (what is approaching, missing, waiting, holding, leaving, hovering, resisting, or echoing); and latent implication (what the first two jointly suggest). The implication must remain grounded in visible evidence and may not invent biography, location, ownership, events, or feelings.
- Compress these levels into one private semantic core, then choose one restrained rhetorical hinge: precise naming, contrast, understatement, double meaning, or a slight reversal. Derive one short main title that makes the viewer suddenly see the photograph differently and produces a quiet, exact moment of recognition. Do not force a pun, slogan, inspirational line, or sentimental backstory.
- Prefer one to six words or one concise phrase: accurate, readable, resonant, and free of empty melodrama.
- Apply the unrelated-image swap test: if the title would retain nearly the same force on an unrelated photograph, it does not belong to this image and must be rewritten.
- Add **two to four** groups of very small supporting text, chosen from short fragments, place or object information, serial numbers, status words, direction words, classification labels, or micro-observations. They must extend the same semantic core rather than pad the design with random archival labels.
- A small amount of a second language may be used as a meaningful editorial accent only when the user permits it. Primary information remains in the target-locale language; never use pseudo-foreign text or gibberish to simulate an international look.
- **Do not invent a year.** Retain one only when the user explicitly supplies or requests it. Do not generate title options, design commentary, camera settings, or meaningless placeholder text.

### 6.3 Typographic behavior

- Create clear hierarchy through large/small contrast, weight, tracking, and a strict grid.
- Align, cut, weave, wrap, corner-lock, stack vertically, rotate 90 degrees, or span type across color planes when it strengthens the composition.
- Break user copy by semantic phrase. Visual rhythm may not override verbal rhythm; never split or weaken a crucial, negative, or turning word.
- Typography must participate in visual weight and spatial rhythm rather than sit inside a separate commercial title box.
- Keep the main title accurately readable; microcopy may be restrained but must not become gibberish.
- The main title must be immediately legible at normal viewing size and at least about three times the microtext scale; never reduce it to a nearly invisible hairline label.
- Avoid drop shadows, outlines, gradient type, 3D lettering, cartoon display faces, UI-label matrices, web components, and advertising templates.

### 6.4 Locked copy payload

Do not leave the actual wording for the image model to invent during rendering. Append the resolved per-photo copy package to the prompt in this exact form:

```text
COPY MODE: REQUIRED
COPY ORIGIN: USER_EXACT | USER_DIRECTION | SOURCE_DERIVED
COPY LOCALE: <resolved locale, such as ar | ja-JP | ko-KR | en-GB | zh-CN>
COPY INTENT — INSTRUCTION ONLY, NEVER RENDER: <one semantic core and intended emotional turn>
MAIN TITLE: <locked exact string>
MICROTEXT 1: <locked exact string>
MICROTEXT 2: <locked exact string>
MICROTEXT 3: <optional locked exact string>
MICROTEXT 4: <optional locked exact string>
COPY RULE: Render only MAIN TITLE and populated MICROTEXT strings, each exactly once. COPY ORIGIN, COPY LOCALE, and COPY INTENT are instructions, never visible text. Do not rewrite, translate, spell-correct, duplicate, or add text. Respect the resolved locale's script shaping, punctuation, spacing, and semantic line-breaking rules.
```

Remove unused optional lines rather than rendering placeholders. In text-free mode, replace the entire block with `COPY MODE: NONE — render no text or pseudo-text anywhere.`

## 7. Output mode, dimensions, and boundary

### 7.1 Four modes

Lock one or more modes before generation; when the caller provides none, ask before continuing. Accept one number, multiple numbers separated by `+`, Chinese/English commas or whitespace, mode names, and `全部` / `all`; deduplicate and execute in menu order 1→4. Each selected ordinary mode produces one file and selected wallpaper mode produces four, so `all` yields seven PNGs per source across four sibling mode directories, never an overview. By default, share the same locked source-specific copy verbatim across all selected modes; only explicit per-mode copy instructions create overrides. In multi-select, custom dimensions must be labeled by mode; ask rather than applying one ambiguous unlabeled size to several modes.

1. **TOP_BOTTOM:** generate the confirmed whole canvas once, with the high-fidelity source in approximately the upper half and the transformed illustration below; unify both regions through colour, rhythm, and meaning.
2. **LEFT_RIGHT:** generate the confirmed whole canvas once, with the high-fidelity source in approximately the left half and the transformed illustration on the right as one finished design.
3. **DESIGN_ONLY:** use the source only as content and identity evidence; let the transformed illustration fill the confirmed whole canvas with no visible source or reserved panel.
4. **WALLPAPER_PACK:** one source produces four separate transformed wallpapers—phone, iPad, desktop, and watch—with no visible source photo. Copy follows the preflight choice of automatic, custom, or text-free output. Also lock an `INDEPENDENT` or `LINKED` wallpaper relationship.

User intent selects the mode; canvas orientation must not silently change it. Paired modes stay exact 50/50. Source-hidden modes must not reintroduce the source, a seam, or reserved placeholder space. Wallpaper-pack recomposes every device separately; never mechanically crop or resize one wallpaper into another.

Wallpaper relationship has two values:

1. **INDEPENDENT:** every device receives only the source photograph, the full 019 aesthetic prompt, and the same locked source facts, three-to-five-color palette, and copy package. No generated wallpaper becomes a reference, so the four compositions may explore more freely.
2. **LINKED:** generate the iPad wallpaper first by default (honor another anchor device when the user explicitly names one), then approve its source identity, aesthetic motive, copy, typography, and safe area before continuing. Every remaining device receives both the original photograph and that same approved anchor: the photo locks content and identity, while the anchor locks only palette, graphic language, geometric hierarchy, typographic rhythm, and print character. All three derivatives point directly to the same anchor; never chain iPad → phone → desktop → watch, because sequential references accumulate drift.

`LINKED` still makes four separate generation calls and returns four files. The anchor is one of the four deliverables, not an extra fifth master. Every derivative must solve subject position, geometry, safe area, and typography anew for its device rather than convert the anchor's dimensions. Repeat the full aesthetic prompt and locked copy on every call; do not rely on reference pixels to preserve correct wording.

### 7.2 Dimension priority

Resolve dimensions in this order:

1. exact user-supplied pixels, such as 2560×1440;
2. a user-supplied ratio or destination;
3. an explicitly chosen canvas: original-prompt 3:4, source aspect, a common ratio, or a custom ratio; wallpaper-pack requires the user to choose the common device preset or provide labelled custom sizes.

Honor exact pixels literally. Top-bottom needs an even total height; left-right needs an even total width for an exact split. Design-only accepts any positive whole-pixel dimensions. Never silently round a requested exact size.

Wallpaper-pack has no silent size default. When the user explicitly chooses the common device preset, use phone 1440×3200, iPad 2048×2732 portrait, desktop 3840×2160, and watch 1024×1024; otherwise use labeled per-device custom sizes. Never apply one unlabeled size arbitrarily.

### 7.3 Generate the complete canvas first

For a paired mode, send the source as a high-fidelity edit/reference input together with the complete 019 aesthetic prompt and locked copy, then generate the whole finished canvas in one job. Treat 50/50 as the composition target while prioritising unity of colour, light, rhythm, typography, and meaning. Design-only and all four wallpapers each generate a complete canvas. Prepare separate photographic and design assets only after a targeted complete-canvas retry still fails or another runtime-contract fallback condition applies.

### 7.4 Resolved mode block

Append the resolved values to the generation prompt:

```text
OUTPUT MODE: TOP_BOTTOM | LEFT_RIGHT | DESIGN_ONLY | WALLPAPER_PACK
DEVICE PROFILE: NONE | PHONE | IPAD | DESKTOP | WATCH
FINAL CANVAS: <whole finished ratio and/or exact WIDTHxHEIGHT>
GENERATION STRATEGY: SINGLE COMPLETE CANVAS
REFERENCE ROLE: SOURCE — HIGH-FIDELITY CONTENT AND IDENTITY ANCHOR
SOURCE VISIBILITY: UPPER 50% | LEFT 50% | REFERENCE ONLY — NOT VISIBLE
LAYOUT RULE: Generate one finished image. Paired modes keep approximately equal source and transformed regions while unifying colour, light, rhythm, typography, and meaning. Source-hidden modes use the complete canvas and show no photo or reserved panel.
WALLPAPER RELATIONSHIP: NONE | INDEPENDENT | LINKED
ANCHOR DEVICE: NONE | IPAD
```

### 7.5 Wallpaper safe regions

- **Phone:** keep the top clock/notch region and bottom control region quiet; place no subject core or fine type there.
- **iPad:** keep essential content inside a centered safe square; extend background planes and crop-safe space outside it so portrait and landscape crops remain viable.
- **Desktop:** keep the top menu area, bottom dock/taskbar, and both icon edges low-information; keep decisive contours away from the edges.
- **Watch:** keep the subject and a simplified but visible type hierarchy recognizable at thumbnail size while reserving the major clock/complication area. Type may be enlarged, shortened, or rearranged but not deleted by default. Preserve 019 identity with larger, simpler geometric planes rather than generic symbols or extra detail.

### 7.6 Boundary

- Top-bottom uses one clean, horizontal, shadowless central boundary. Left-right uses one clean, vertical, shadowless central boundary.
- Use no torn paper, frames, inset margins, dimensional cards, tape, scanner borders, collage shadows, or mockup effects.
- Design-only has no boundary and must not imitate a diptych.
- Wallpaper outputs also have no boundary, device frame, system UI, or multi-image layout.
- Any restrained cross-panel echo in paired modes must not cover, redraw, or contaminate the photographic subject.
- The transformed region always retains retro-flat illustration and premium editorial design; photography is visible only in paired modes.

## 8. Output limits

- Each selected ordinary mode produces one independent finished image per source; selected wallpaper-pack adds exactly four separate wallpaper files. `all` therefore produces seven PNGs across four sibling task directories per source. Process multiple source photos separately and never create a collage, grid, contact sheet, or series overview.
- Copy follows the resolved preflight: automatic or custom copy uses one clearly dominant title and up to two to four microtext groups; when custom copy omits microtext, derive supporting microtext professionally or keep title-only if requested. Text-free mode renders no letters, characters, numbers, or decorative pseudo-text. Include no logo, watermark, signature, palette, legend, frame note, or interface element.
- Do not output analysis, process notes, title candidates, or parameter tables.

Strictly avoid multi-photo composition, grids, overview sheets, photo redrawing, subject deformation, drifting panel proportions, realistic illustration, complex texture, 3D rendering, UI styling, stock-material aesthetics, template vector art, unsupported colors, complex gradients, cheap cartoon styling, or loss of identity between the two halves.

## 9. Pre-generation check

Before submitting the generation request, confirm internally:

1. This call processes one clearly selected photo only.
2. Mode and dimensions are locked per section 7, with exact pixels taking priority; paired modes split 50/50 on the correct axis, while source-hidden modes have no seam.
3. The photographic panel stays faithful in paired modes; design-only and wallpapers contain no source photo, seam, or reserved area.
4. The transformed illustration preserves the same subject's key contour, pose, and relationship.
5. The palette contains only three to five source-derived colors.
6. Copy mode follows section 6: automatic, custom, or text-free output is locked before generation; locale follows audience/market > output language > direction language; if none is explicit, ask before generation and is never guessed from identity. Automatic or direction-led copy uses native target-locale language, moves from visible fact to grounded subtext, passes the unrelated-image swap test, and avoids forced cleverness, while finished user copy stays verbatim and is typeset by that language's semantic phrases. Only an explicit text-free request removes all text and pseudo-text.
7. The finished bitmap was actually opened and inspected at normal and thumbnail size; it preserves at least three source-specific identity cues and the principal relationship rather than a generic sunset, road, or sun/wave symbol.
8. All four wallpapers were separately recomposed, match their exact sizes, keep essential content in device-safe regions, and contain no baked-in system UI. `INDEPENDENT` uses only the original photo for all four; `LINKED` approves the anchor first and makes every derivative reference the original photo plus that same anchor, with no sequential drift or mechanical resizing.
9. The deliverable is a Codex-generated PNG bitmap, not SVG, HTML, Canvas, or programmatic drawing.
10. There is no collage, logo, watermark, UI, mockup, or other excluded element.
