<div align="center">

# 🦁 XXD Panel 019

### 把照片中的特定主体与关系，重构成一张仍然认得出来的现代主义插画

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-000000?style=flat-square)](./SKILL.md)
[![Four Modes](https://img.shields.io/badge/Modes-4-d18437?style=flat-square)](#四种输出共享同一种识别逻辑)
[![Raster Output](https://img.shields.io/badge/Output-PNG-355c7d?style=flat-square)](#边界与信任)

<strong>简体中文</strong> · <a href="README.en.md">English</a> · <a href="README.ja.md">日本語</a>

</div>

> RECOGNISE FIRST · REDUCE WITH INTENT · COMPOSE WITH TYPE

XXD Panel 019 是一个面向 Codex 与兼容 Agent 的图像生成 Skill。它把照片里的主体、姿态、方向、比例和不可拆分关系，转译成可辨认的复古现代主义平面插画；它不是把照片描摹成矢量，也不是用几何色块把内容抹掉。

简化不是删除身份，而是找到最少但足够准确的证据。

## 为什么需要它

很多“照片转平面插画”最后只剩一套通用语法：人物变成无脸剪影，场景变成太阳和道路，配色来自模板，文字只是装饰。结果看起来像设计，却不再属于原照片。

019 要求每张变化画面保留至少三个源图专属身份线索，例如外轮廓、姿态、朝向、比例、遮挡、负形或主体之间的距离。几何化可以大胆，但观众仍应一眼认出它在重新讲述哪一个画面。

```text
源照片 → 找到主体与关系 → 锁定身份线索 → 提取 3–5 色 → 几何重构 → 编辑排版 → 精确复核
```

## 019 的视觉承诺

- **辨识优先**：先保证主体和关系仍能对应原照片，再追求形式张力。
- **至少三个身份线索**：轮廓、姿态、比例、方向、遮挡与负形共同建立识别。
- **3–5 个源图颜色**：颜色来自照片，不借用示例作品或模板色盘。
- **正负形与尺度反差**：用大色面、切面、简洁曲线和留白建立观看路径。
- **克制的印刷气质**：轻微网点、纸感和套印特征服务于平面层级，不模拟光滑 3D。
- **编辑式文字**：标题与微型文字参与几何关系、视觉重心和空间节奏。

## 四种输出，共享同一种识别逻辑

若没有指定模式，Skill 会先询问。尺寸可以同时给出，精确像素优先。

| 模式 | 默认画布 | 成品 |
| --- | ---: | --- |
| `top-bottom` | 3:4 | 原照片在上，019 插画在下，严格等高 |
| `left-right` | 3:2 | 原照片在左，019 插画在右，严格等宽 |
| `design-only` | 3:4 | 只保留变化后的完整插画，不显示原照片 |
| `wallpaper-pack` | 四种设备尺寸 | 手机、iPad、电脑、儿童手表各一张独立 PNG |

双联中的摄影保持真实，只允许克制调色和必要的环境延展。单画面与壁纸中，照片仅作为主体、关系、配色与文案的依据，不进入最终画面。

### 四端壁纸：同一家族，不是同一张图

默认尺寸：手机 `1440×3200`、iPad `2048×2732`、电脑 `3840×2160`、儿童手表 `1024×1024`。可逐设备覆盖。

- **连贯套装（推荐）**：先生成并验收 iPad 定调图；另外三张都使用“原照片＋同一张定调图”重新构图。
- **四张独立**：每张只参考原照片，让不同设备拥有更自由的解法。

连贯套装锁定色盘、图形语法、印刷气质和排版节奏，但每个设备仍要重新求解主体位置、几何层级、文字和安全区。不会机械裁切，也不会串联垫图造成逐张漂移。

## 文案必须与画面高度绑定

文字默认开启。自动文案不是从“Memory / Dream / Journey”一类通用词中抽取，而是先读取画面的事实、关系张力和有依据的潜台词，再寻找一个让观众重新看懂照片的标题。

标题要通过“换图测试”：换到无关照片仍然成立，就说明它不属于当前作品。微型文字必须延续同一个语义核心，不能为了排版随意堆序列号或伪档案标签。

用户给出最终成稿时逐字保留；给出方向或可编辑草稿时，Skill 会理解受众、目的、必留词、语气和暗示，再在授权范围内专业转创。

文案语言优先级：

```text
目标市场／受众地区 > 指定成品语言 > 文案方向语言 > 当前请求语言
```

日本版使用自然日语与日文断行规则，韩国版使用自然韩语与正确空格，英国版使用英式英语。Skill 不从人物外貌推断国籍，也不使用伪外文。

## 准确分区由脚本完成，插画仍由生图完成

`scripts/compose_panel.py` 负责规划、严格 50/50 合成、最终尺寸和审计。它不会用 SVG 或程序化色块替代真正的位图生图。

```bash
python3 scripts/compose_panel.py --plan --layout top-bottom
python3 scripts/compose_panel.py --plan --layout left-right --size 2560x1440
python3 scripts/compose_panel.py --audit result.png --layout design-only --size 2048x2048
```

精确上下双联要求总高度为偶数，左右双联要求总宽度为偶数；奇数尺寸不会被静默改写。

## 开始使用

### 安装

```bash
git clone https://github.com/nevertoday/xxd-panel-019.git
mkdir -p ~/.codex/skills
ln -s "$(pwd)/xxd-panel-019" ~/.codex/skills/xxd-panel-019
```

Claude Code 用户可链接到 `~/.claude/skills/xxd-panel-019`。安装后重新开启 Agent 会话。

### 调用

```text
$xxd-panel-019
把这张照片做成四端连贯壁纸套装，主标题使用英式英语。
```

只上传照片并调用也可以；Skill 会先用分行编号菜单询问模式。壁纸模式未说明关系时，再询问“连贯套装”或“四张独立”。

完整生成规范：

- [Skill 工作流](SKILL.md)
- [中文完整提示词](references/xxd-panel-019-prompt.zh-CN.md)
- [English full prompt](references/xxd-panel-019-prompt.en.md)

## 边界与信任

- 当前照片是当前任务唯一的内容来源，不借用其他输入、旧成品或示例素材。
- 每次调用新建任务目录；相同照片与相同参数也必须重新生成。
- 最终交付为 PNG 位图，不用 SVG、HTML、Canvas 或程序化绘图冒充。
- 位图桥接器只返回脱敏状态，不打印 provider、端点、请求头、凭据、Prompt 或服务端正文。
- 普通模式一张源图输出一张；壁纸模式严格输出四张独立文件，不做拼贴总览。

本地合成需要 Python 3 与 Pillow；安全位图桥接器使用 Python 3.11+ 的 `tomllib`。实际生成需要宿主 Agent 的内置位图能力，或已配置好的兼容位图路径。

## 仓库结构

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

## 关于 XXD

XXD 是小小东的品牌名缩写。本项目由 [@xiaoxiaodong01](https://x.com/xiaoxiaodong01) 创作与维护。

## 社群与成员提示词库

### Skills 答疑｜99 元

费用用于 Skills 使用答疑。可直接[加入知识星球](https://wx.zsxq.com/group/15554814142882)；如需咨询加入或付款问题，请扫描下方微信二维码联系。

<p align="center">
  <a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="XXD 付费社群微信二维码" width="320"></a>
</p>

### 成员提示词库｜699 元/年

[XXD 成员提示词库](https://vip.xiaoxiaodong.ai/)支持自助开通，年费 699 元。

<div align="center">

**简化画面，但不简化它的身份。**

</div>
