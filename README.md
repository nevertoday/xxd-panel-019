<p align="center">
  <img src="./assets/banner.svg" alt="XXD Panel 019 项目介绍" width="1200">
</p>

<div align="center">

# 🦁 XXD Panel 019

### 把照片中的特定主体与关系，重构成一张仍然认得出来的现代主义插画

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-000000?style=flat-square)](./SKILL.md)
[![Four Modes](https://img.shields.io/badge/Modes-4-d18437?style=flat-square)](#四种输出共享同一种识别逻辑)
[![Raster Output](https://img.shields.io/badge/Output-PNG-355c7d?style=flat-square)](#边界与信任)

<strong>简体中文</strong> · <a href="README.en.md">English</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.ar.md">العربية</a>

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

## 样张 · 来自 X

> [小小东（@xiaoxiaodong01）](https://x.com/xiaoxiaodong01/status/2090144142366233008) · 2026 年 8 月 19 日<br>
> GPT2 × 复古 × 扁平 × 美学提示词 × VOL.019<br>
> 推文同时演示：在提示词中注明“语言偏好：西班牙语”等目标语言，文字会跟随受众语言自然转创。

<table>
  <tr>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="./assets/examples/sample-01.jpg" alt="XXD Panel 019 样张 1"></a></td>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="./assets/examples/sample-02.jpg" alt="XXD Panel 019 样张 2"></a></td>
  </tr>
  <tr>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="./assets/examples/sample-03.jpg" alt="XXD Panel 019 样张 3"></a></td>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="./assets/examples/sample-04.jpg" alt="XXD Panel 019 样张 4"></a></td>
  </tr>
</table>

<p align="center"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008">查看原推文与完整提示词 →</a></p>

这些样张用于展示 019 的美学动机，不会把推文中的旧画幅写成当前 Skill 的默认尺寸；当前四种模式仍遵循下方的生成前明确画幅与自定义尺寸逻辑。

## 四种可组合输出模式

可用 `1`、`1+3`、`1、2、4` 或 `全部` 选择一个或多个模式；`全部` 每张源图输出 7 个独立 PNG。模式确定后，Skill 会在生图前继续询问整张最终成品的画幅：`3:4` 原提示词画幅、明确跟随原图、常用比例，或自定义比例／准确像素。不会再静默套用源图尺寸。

| 模式 | 画幅逻辑 | 成品 |
| --- | --- | --- |
| `top-bottom` | 用户确认的整张成品画幅 | 一次生成完整画布：高保真原图在上，019 设计在下，约 50/50 |
| `left-right` | 用户确认的整张成品画幅 | 一次生成完整画布：高保真原图在左，019 设计在右，约 50/50 |
| `design-only` | 用户确认的整张成品画幅 | 019 设计铺满画布，不显示原照片 |
| `wallpaper-pack` | 逐设备确认 | 手机、iPad、电脑、儿童手表四张独立 PNG |

双联默认把原图作为高保真垫图／编辑参考，用一套完整提示词直接生成一张整体成品，让摄影、设计、色彩、光线、文字与含义自然呼应。只有完整画布针对性重试仍失败、用户要求原片逐像素不变、当前通道无法实现目标画幅，或需要无创像素校准时，才启用确定性拼合兜底。

壁纸可选连贯或独立。连贯套装先批准一张 iPad 定调图，另外三张分别参考原图＋同一定调图重新构图；独立套装的四张都只参考原图。两者都不会裁切其他设备成品或串联衍生图。

## 文案必须与画面高度绑定

文字不再静默开启。正式生图前先选择自动文案、自定义文案或无文字，并为前两者注明目标语言或地区。自动文案不会从“Memory / Dream / Journey”一类通用词中抽取，而是先读取画面的事实、关系张力和有依据的潜台词，再寻找一个让观众重新看懂照片的标题。

标题要通过“换图测试”：换到无关照片仍然成立，就说明它不属于当前作品。微型文字必须延续同一个语义核心，不能为了排版随意堆序列号或伪档案标签。

用户给出最终成稿时逐字保留；给出方向或可编辑草稿时，Skill 会理解受众、目的、必留词、语气和暗示，再在授权范围内专业转创。

文案语言优先级：

```text
目标市场／受众地区 > 指定成品语言 > 文案方向语言；以上均未明确时，生图前询问
```

日本版使用自然日语与日文断行规则，韩国版使用自然韩语与正确空格，英国版使用英式英语，阿拉伯语版使用自然的现代标准阿拉伯语、正确连写和从右到左排版。Skill 不从人物外貌推断国籍，也不使用伪外文。

## 完整画布优先与位图边界

图像模型负责整张成品的审美重构，双联也默认一次直出完整画布。`scripts/compose_panel.py` 只保留为条件明确的兜底、无创尺寸校准和只读审计工具，不再预先规划每次任务，也不评价审美是否成功。

全部交付为 PNG 位图。每次调用都在 `~/Desktop/xxd/` 下创建新任务；已配置图像通道只返回脱敏状态，不公开供应商、端点、凭据、请求头、提示词、响应或账户信息。SVG、HTML、Canvas、图表和程序绘图不能替代最终作品。

## 生图模型优先级

GPT Image 2 是默认首选，并继续执行本项目现有的高保真垫图、生成前确认整张画幅、双联一次生成完整画布、脚本仅作条件式兜底等逻辑。

当当前工具或已配置兼容通道确实可用，并能满足原图保真、整张成品比例、目标语言文字和连贯壁纸多图参考等要求时，也支持 Seedance 5.0 Pro、Nano Banana Pro（Gemini Image Pro）、Nano Banana 2（Gemini Image Flash）或其他兼容位图模型。备用模型只替换生成通道，不得改变模式、画幅、文案、语言、壁纸关系和完整画布优先策略。

如果没有合适的生图通道，Skill 会请用户启用生图工具或提供 API Key。用户主动提供的凭据可以用于当前任务，但不得在回复或日志中回显、展示或泄露；未经用户明确要求，不会长期保存凭据或修改供应商、账户、计费及全局路由配置。

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

只上传照片并调用也可以；Skill 会先用分行编号菜单询问一个或多个模式。壁纸模式未说明关系时，再询问“连贯套装”或“四张独立”。

完整生成规范：

- [Skill 工作流](SKILL.md)
- [中文完整提示词](references/xxd-panel-019-prompt.zh-CN.md)
- [English full prompt](references/xxd-panel-019-prompt.en.md)
- [019 原始风格提示词](references/019-source.md)

## 边界与信任

- 当前照片是当前任务唯一的内容来源，不借用其他输入、旧成品或示例素材。
- 每次调用新建任务目录；相同照片与相同参数也必须重新生成。
- 最终交付为 PNG 位图，不用 SVG、HTML、Canvas 或程序化绘图冒充。
- 位图桥接器只返回脱敏状态，不打印 provider、端点、请求头、凭据、Prompt 或服务端正文。
- 每个所选普通模式各返回一张；若选择 `wallpaper-pack`，再返回四张独立壁纸。选择 `全部` 时每张原图共返回 7 个 PNG，分处四个同级模式文件夹，绝不生成拼贴总览。

本地合成需要 Python 3 与 Pillow；安全位图桥接器使用 Python 3.11+ 的 `tomllib`。实际生成需要宿主 Agent 的内置位图能力，或已配置好的兼容位图路径。

## 仓库结构

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

## 关于 XXD

XXD 是小小东的品牌名缩写。本项目由 [@xiaoxiaodong01](https://x.com/xiaoxiaodong01) 创作与维护。

## 支持与会员权益

### 深度咨询｜299 元/小时

按小时提供一对一 Skills 深度咨询，每小时 299 元。如需预约，请扫描下方微信二维码联系小小东。

### 小小东 Skills 用户交流群｜入群 99 元

一次付费加入用户交流群，用于 Skills 使用经验分享、作品交流与成员互助；不包含按小时的一对一深度咨询。入群请扫描下方微信二维码，备注「Skills 用户群」。

### 知识星球＋成员提示词库｜699 元/年

知识星球与 [XXD 成员提示词库](https://vip.xiaoxiaodong.ai/)属于同一项会员权益：**支付一次年费，两项同时开通，不需要重复付费。**

任选一种开通方式：

1. 在[知识星球](https://wx.zsxq.com/group/15554814142882)开通后，微信联系小小东，领取成员提示词库兑换码。
2. 在[成员提示词库](https://vip.xiaoxiaodong.ai/)自助开通后，微信联系小小东，由小小东邀请进入知识星球。

<p align="center">
  <a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="XXD 付费社群微信二维码" width="320"></a>
</p>

<div align="center">

**简化画面，但不简化它的身份。**

</div>

---

<div align="center">
  <h2>⚡ 算力赞助</h2>
  <p>如果这个项目为你节省了时间，欢迎点亮 Star、分享给朋友，或自愿赞助项目算力。</p>
  <table>
    <tr>
      <td align="center" width="240">
        <a href="https://colors.xiaoxiaodong.ai/docs/images/wechat-reward-qr.png"><img src="https://colors.xiaoxiaodong.ai/docs/images/wechat-reward-qr.png" alt="XXD 算力赞助微信收款码" height="220"></a><br>
        <strong>微信</strong><br>
        <sub>扫描二维码赞助算力</sub>
      </td>
      <td align="center" width="240">
        <a href="https://colors.xiaoxiaodong.ai/docs/images/alipay-reward-qr.png"><img src="https://colors.xiaoxiaodong.ai/docs/images/alipay-reward-qr.png" alt="XXD 算力赞助支付宝收款码" height="220"></a><br>
        <strong>支付宝</strong><br>
        <sub>扫描二维码赞助算力</sub>
      </td>
    </tr>
  </table>
  <p><sub>算力赞助完全自愿，用于支持生成测试与项目持续维护，不影响项目的免费使用。</sub></p>
</div>
