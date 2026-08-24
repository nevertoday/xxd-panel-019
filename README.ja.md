<p align="center">
  <img src="./assets/banner.svg" alt="XXD Panel 019 プロジェクトバナー" width="1200">
</p>

<div align="center">

# 🦁 XXD Panel 019

### 写真固有の被写体と関係を、見分けられるままモダニズム・イラストへ再構成する

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-000000?style=flat-square)](./SKILL.md)
[![Four Modes](https://img.shields.io/badge/Modes-4-d18437?style=flat-square)](#4つの出力を支えるひとつの認識ロジック)
[![Raster Output](https://img.shields.io/badge/Output-PNG-355c7d?style=flat-square)](#境界と信頼性)

<a href="README.md">简体中文</a> · <a href="README.en.md">English</a> · <strong>日本語</strong> · <a href="README.ko.md">한국어</a> · <a href="README.ar.md">العربية</a>

</div>

> RECOGNISE FIRST · REDUCE WITH INTENT · COMPOSE WITH TYPE

XXD Panel 019 は、Codex と互換 Agent のための画像生成 Skill です。写真の被写体、姿勢、方向、比率、切り離せない関係を、判別可能なレトロモダニズムの平面イラストへ翻訳します。写真の自動トレースでも、一般的な幾何学で内容を消す仕組みでもありません。

減らすべきなのはノイズであり、固有性ではありません。

## なぜ、この Skill が必要なのか

写真を平面イラストへ変換する多くの手法は、やがて共通の道具箱へ収束します。人物は顔のないシルエットになり、実在する場所は太陽と道路へ変わり、色はテンプレートから選ばれ、文字は余白を埋める装飾になります。デザインには見えても、その写真の作品ではなくなります。

019 は、すべての変換画面に少なくとも三つの元写真固有の手がかりを求めます。外形、姿勢、方向、比率、重なり、負形、被写体間の距離などです。幾何学的な再構成は大胆でも、どの場面を語り直しているのかが一目で分からなければなりません。

```text
元写真 → 被写体と関係を特定 → 識別手がかりを固定 → 3–5 色を抽出 → 再構成 → 組版 → 検証
```

## 019 のビジュアル原則

- **まず識別**：グラフィックな緊張感より先に、被写体と関係を守ります。
- **少なくとも三つの手がかり**：輪郭、姿勢、比率、方向、重なり、負形を組み合わせます。
- **元写真由来の 3–5 色**：作例やテンプレートの色を持ち込みません。
- **正負形とスケール差**：大きな色面、硬質な切面、簡潔な曲線、余白で視線を導きます。
- **抑制された印刷感**：軽い網点、紙、版ずれを平面階層へ使い、滑らかな 3D 表現にはしません。
- **編集的タイポグラフィ**：見出しとマイクロコピーを幾何学、重心、空間リズムへ参加させます。

## 作例 · X より

> [Xiaoxiaodong（@xiaoxiaodong01）](https://x.com/xiaoxiaodong01/status/2090144142366233008) · 2026年8月19日<br>
> GPT2 × レトロ × フラット × 美学プロンプト × VOL.019<br>
> 投稿では「言語設定：スペイン語」のように対象言語を指定すると、その受け手に自然なコピーへトランスクリエーションされることも示しています。

<table>
  <tr>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="./assets/examples/sample-01.jpg" alt="XXD Panel 019 作例 1"></a></td>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="./assets/examples/sample-02.jpg" alt="XXD Panel 019 作例 2"></a></td>
  </tr>
  <tr>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="./assets/examples/sample-03.jpg" alt="XXD Panel 019 作例 3"></a></td>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008"><img src="./assets/examples/sample-04.jpg" alt="XXD Panel 019 作例 4"></a></td>
  </tr>
</table>

<p align="center"><a href="https://x.com/xiaoxiaodong01/status/2090144142366233008">元の投稿と完全なプロンプトを見る →</a></p>

これらは 019 の美学的動機を示す作例です。投稿当時の画面比率を現在の既定値にはしません。4つのモードは、以下の生成前に画角を明示するカスタムサイズ方針に従います。

## 組み合わせ可能な4つの出力

`1`、`1+3`、`1,2,4`、`全部` で一つまたは複数を選べます。`全部` は元画像ごとに7点の独立PNGを出力します。モード選択後、生成前に完成画像全体の画角を必ず確認します：元プロンプトの `3:4`、明示的な元画像比率、一般的な比率、またはカスタム比率／正確なピクセルです。元画像寸法を暗黙には適用しません。

| モード | 画角ルール | 成果物 |
| --- | --- | --- |
| `top-bottom` | ユーザー確認済みの完成画角 | 完成キャンバスを一度に生成：上に高忠実度の元画像、下に 019 デザイン、約50/50 |
| `left-right` | ユーザー確認済みの完成画角 | 完成キャンバスを一度に生成：左に高忠実度の元画像、右に 019 デザイン、約50/50 |
| `design-only` | ユーザー確認済みの完成画角 | 019 デザインが全画面を満たし、元画像は表示しない |
| `wallpaper-pack` | 端末ごとに確認 | スマートフォン、iPad、デスクトップ、子ども用ウォッチの個別PNG |

二連モードは元画像を高忠実度の編集／参照入力として使い、完全なスタイルプロンプト一式で完成画面を直接生成します。写真、デザイン、色、光、文字、意味を一体化するためです。決定論的な合成は、完成画面の再試行後も失敗した場合、原画像のピクセル完全保持を明示された場合、生成経路が指定画角に対応しない場合、または無劣化の最終ピクセル調整が必要な場合だけ使います。

壁紙は連動または独立を選べます。連動はiPad基準作を一つ承認し、他の端末を元画像＋同じ基準作から個別に再構成します。独立は各端末が元画像だけを参照します。どちらも他端末の成果を切り抜かず、派生を連鎖しません。

## コピーは画面固有でなければならない

生成前に、自動コピー、カスタムコピー、文字なしのいずれかを確認します。自動／カスタムでは対象言語または地域も指定し、カスタムでは見出しと任意のマイクロコピーを直接入力できます。

タイトルは無関係な写真との入れ替えテストを通過する必要があります。別の写真でも同じように成立するなら、この作品の言葉ではありません。マイクロコピーも同じ意味の核を延長し、無関係なシリアル番号や擬似アーカイブ語で余白を埋めません。

完成原稿は一字一句保持します。方向性や編集可能な草稿は、読者、目的、必須語句、語調、含意を守っている範囲でだけ転創します。

言語の優先順位：

```text
対象市場・読者 > 指定された出力言語 > コピー方針の言語；いずれも明示されていない場合は生成前に確認
```

日本版は自然な日本語と日本語の禁則処理、韓国版は自然な韓国語と正しい空白、英国版はイギリス英語、アラビア語版は自然な現代標準アラビア語、正しい字形連結、右から左の組版を使います。外見から国籍を推測せず、擬似外国語も使いません。

## 完成キャンバス優先とラスター境界

画像モデルが完成画面全体の美的再構成を担当し、二連レイアウトも完成キャンバス一枚の直接生成を既定とします。`scripts/compose_panel.py` は条件付きの復旧、無劣化ピクセル調整、読み取り専用監査にだけ残し、毎回の事前計画や美的評価には使いません。

納品物はすべてPNGラスターで、呼び出しごとに `~/Desktop/xxd/` に新規タスクを作ります。設定済み画像経路は匿名化された状態だけを返し、提供元、接続先、認証情報、ヘッダー、プロンプト、応答、アカウント情報を公開しません。SVG、HTML、Canvas、図解、プログラム描画は最終作品の代替になりません。

## 選択式 UI とインラインパラメータ

実行環境に本物の対話コントロールがある場合、カード式の選択を優先します。出力モードと通常画像サイズは複数選択、文案方式と壁紙の関係は単一選択です。サイズは自動調整、元画像比率、1:1、3:4、4:3、4:5、5:4、2:3、3:2、9:16、16:9、21:9、5:7、7:5、カスタム比率／ピクセルから選べます。対話コントロールがない環境では、クリックできない疑似チェックボックスではなく、読みやすい複数行の番号メニューに切り替えます。

すべての設定は呼び出し後の変数として直接指定できます。

```text
/xxd-panel-019 photo.jpg --mode top-bottom,design-only --size auto,3:4,9:16 --text auto --locale ja-JP
```

`--mode`、複数指定可能な `--size`、`--text auto|custom|none`、`--locale`、`--copy`、`--wallpaper linked|independent`、`--wallpaper-size`、`--out` に対応します。必要な値が揃っていれば質問を省略して生成を開始し、不足分だけを追加で尋ねます。異なる縦横比はそれぞれ再構成し、四端末壁紙は通常サイズと機械的に掛け合わせない独立分岐です。

## 画像モデルの優先順位

GPT Image 2 を既定の第一候補とします。高忠実度の参照画像、生成前の完成キャンバス確認、二連モードの完成画面一括生成、条件を満たした場合だけのスクリプト合成という既存の流れは変わりません。

現在のツールまたは設定済み経路から実際に利用でき、元画像の忠実度、完成画角、対象言語の文字、連動壁紙の複数参照を満たせる場合は、Seedance 5.0 Pro、Nano Banana Pro（Gemini Image Pro）、Nano Banana 2（Gemini Image Flash）、その他の互換ビットマップモデルも利用できます。代替モデルが変更できるのは生成経路だけで、モード、画角、文案、言語、壁紙関係、完成キャンバス優先の方針は変更できません。

適切な経路がない場合は、画像生成ツールを有効にするか API Key を提供するようユーザーに案内します。ユーザーが提供した認証情報は現在のタスクで利用できますが、返信やログに再表示・記録・開示しません。明示的な依頼がない限り、長期保存やプロバイダー、アカウント、課金、グローバル経路の設定変更も行いません。

## はじめる

```bash
git clone https://github.com/nevertoday/xxd-panel-019.git
mkdir -p ~/.codex/skills
ln -s "$(pwd)/xxd-panel-019" ~/.codex/skills/xxd-panel-019
```

Claude Code では同じフォルダーを `~/.claude/skills/xxd-panel-019` へリンクできます。インストール後は Agent セッションを再起動してください。

```text
$xxd-panel-019
この写真から4端末向けの連続壁紙セットを作ってください。見出しはイギリス英語で。
```

写真だけを添えて Skill を呼び出すこともできます。その場合は、改行された番号付きメニューで一つまたは複数のモードを確認し、壁紙セットなら必要に応じて「連続セット」か「4枚を独立制作」かを続けて確認します。

完全な仕様：

- [Skill ワークフロー](SKILL.md)
- [中国語版フルプロンプト](references/xxd-panel-019-prompt.zh-CN.md)
- [英語版フルプロンプト](references/xxd-panel-019-prompt.en.md)
- [019 オリジナルスタイル原稿](references/019-source.md)

## 境界と信頼性

- 現在の写真だけが現在のタスクの内容ソースです。別入力、過去成果、同梱例から内容を借りません。
- 同じ写真と同じパラメータでも、呼び出しごとに新しいタスクフォルダーを作ります。
- 最終成果は PNG ビットマップです。SVG、HTML、Canvas、プログラム描画で代用しません。
- 設定済みビットマップブリッジは匿名化した状態だけを返し、provider、endpoint、header、credential、Prompt、サーバー応答本文を表示しません。
- 選択した通常モードごとに1点を返し、`wallpaper-pack` を選ぶと独立壁紙4点を追加します。`全部` は元写真1枚につき7点を4つの同階層モードフォルダへ出力し、一覧コラージュにはまとめません。

ローカル合成には Python 3 と Pillow が必要です。安全なビットマップブリッジは Python 3.11+ の `tomllib` を使用します。実際の生成には、ホスト Agent の内蔵ビットマップ生成機能、または設定済みの互換ルートが必要です。

## リポジトリ構成

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

## XXD について

XXD は Xiaoxiaodong のブランド名を略したものです。このプロジェクトは [@xiaoxiaodong01](https://x.com/xiaoxiaodong01) が制作・管理しています。

## サポートと会員特典

### 個別の深度相談｜CNY 299／時間

Skills の利用に関する 1 対 1 の深度相談は、1 時間あたり CNY 299 です。予約は、以下の WeChat QR コードから Xiaoxiaodong へご連絡ください。

### Xiaoxiaodong Skills ユーザー交流グループ｜参加費 CNY 99

一度の支払いで、使い方や制作事例の共有、メンバー同士の情報交換を行うユーザーグループに参加できます。時間制の 1 対 1 深度相談は含まれません。以下の WeChat QR コードから「Skills ユーザーグループ」と添えてご連絡ください。

### 知识星球＋会員向けプロンプトライブラリ｜年額 CNY 699

知识星球と [XXD 会員向けプロンプトライブラリ](https://vip.xiaoxiaodong.ai/)は、ひとつの会員特典です。**年額料金を一度支払えば両方を利用でき、二重に購入する必要はありません。**

登録方法は、次のどちらかを選べます。

1. [知识星球](https://wx.zsxq.com/group/15554814142882)で登録後、WeChat で Xiaoxiaodong に連絡し、会員向けプロンプトライブラリの引換コードを受け取る。
2. [会員向けプロンプトライブラリ](https://vip.xiaoxiaodong.ai/)で直接登録後、WeChat で Xiaoxiaodong に連絡し、知识星球への招待を受ける。

<p align="center">
  <a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="XXD 有料コミュニティの WeChat QR コード" width="320"></a>
</p>

<div align="center">

**画面を簡潔にしても、その固有性までは削らない。**

</div>

---

<div align="center">
  <h2>☕ このオープンソースプロジェクトを応援する</h2>
  <p>このプロジェクトが役立ったら、Star、シェア、またはコーヒー一杯で応援していただけるとうれしいです。</p>
  <table>
    <tr>
      <td align="center" width="240">
        <a href="https://github.com/nevertoday/zhongguo-traditional-colors/blob/main/docs/images/buy-me-a-coffee-qr.png?raw=true"><img src="https://github.com/nevertoday/zhongguo-traditional-colors/blob/main/docs/images/buy-me-a-coffee-qr.png?raw=true" alt="Buy Me a Coffee で Xiaoxiaodong を応援する" width="180"></a><br>
        <strong>Buy me a coffee</strong><br>
        <sub>QR コードを読み取るか開いて、Xiaoxiaodong を応援できます</sub>
      </td>
    </tr>
  </table>
  <p><sub>支援は任意であり、このオープンソースプロジェクトの利用条件には影響しません。</sub></p>
</div>
