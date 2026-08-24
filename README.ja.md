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

## 原文プロンプトを唯一の美的基準にする

`references/019-source.md` が、このプロジェクト唯一の創作・美的基準です。Skill は原文を要約・拡張せず、共通の配色計画、美的動機、タイトル、マイクロコピーを追加しません。色、素材、構図、余白、言葉、タイポグラフィは、GPT Image 2 が原文プロンプトの規則どおりに実行します。

モードとサイズは、原文の変換美学を変えずに、旧来の 3:4 上下出力コンテナを完全に置き換えます。各成果物では選択された一つのモード契約だけを GPT Image 2 に送り、四つの候補を一つの汎用テンプレート内で解釈させません。

## 組み合わせ可能な4つの出力

`top-bottom`、`left-right`、`design-only`、`wallpaper-pack` は単独でも複数でも選べます。複数選択時も、各モードを独立したプロンプトで別々に生成します。

- `top-bottom`：現実画像を上、デザイン変換を下に置く一枚の完成キャンバス。
- `left-right`：上端から下端まで左右構造を保ち、元画像を左、デザインを右に配置します。文字もその構造内に統合し、幅は非対称でも構いません。
- `design-only`：元画像は不可視の参照に限定し、見える要素はすべて当該 Panel のデザイン変換言語に従います。
- `wallpaper-pack`：各端末用にデザイン変換のみの壁紙を独立再構成します。

境界線、中央比率、ピクセル座標は測定しません。決定論的な合成は、ユーザーが正確な分割または元写真のピクセル保持を明示した場合だけ使います。

通常サイズも複数選択できます：自動適応、元画像比率、1:1、3:4、4:3、4:5、5:4、2:3、3:2、9:16、16:9、21:9、5:7、7:5、カスタム比率／正確なピクセル。暗黙の既定サイズはありません。異なる比率は、同じ原文プロンプトから個別に再構成します。

壁紙セットは連動型または独立型。連動型は最初の一枚を基準画像とし、残りを元写真＋基準画像から各端末向けに再構成します。一枚を四サイズへ機械的に切り抜くことはありません。

各呼び出しではタスクディレクトリを一つだけ作り、最終 PNG をすべてその直下へ保存します。元画像、モード、サイズ、端末ごとのサブフォルダーは作らず、`source-01-left-right-3x2-2160x1440.png` や `source-01-wallpaper-linked-phone-1440x3200.png` のようにファイル名で識別します。

## 文字モード

生成前に次の一つを選びます。

1. **原文プロンプトに従ってモデルが文字を生成**：ユーザーは言語・地域だけを指定し、内容、量、調子、組版は GPT Image 2 が原文どおりに生成します。表示される言葉は現在の画像の内容、空気感、または暗示から生まれ、事実・資料として見える情報には、ユーザー提供・画像内で確認可能・検証済みの根拠が必要です。
2. **自分の正確な文言を使う**：一字一句そのまま渡し、書き換え・翻訳・タイトル追加をしません。組版は原文に従います。
3. **文字なし**：文字と疑似文字を厳格に禁止します。

外側の Skill はタイトルやマイクロコピーを先に書きません。出力言語は操作言語と別に確認し、人物、風景、ファイル名から推測しません。

## 完成キャンバス優先とラスター境界

画像モデルが完成画面全体の美的再構成を担当し、二連レイアウトも完成キャンバス一枚の直接生成を既定とします。`scripts/compose_panel.py` は条件付きの復旧、無劣化ピクセル調整、読み取り専用監査にだけ残し、毎回の事前計画や美的評価には使いません。

納品物はすべてPNGラスターで、呼び出しごとに `~/Desktop/xxd/` に新規タスクを作ります。設定済み画像経路は匿名化された状態だけを返し、提供元、接続先、認証情報、ヘッダー、プロンプト、応答、アカウント情報を公開しません。SVG、HTML、Canvas、図解、プログラム描画は最終作品の代替になりません。

## 宿主能力に適応する質問とインライン引数

同じ Skill が、宿主に実在する対話機能へ適応します。装飾記号をクリック可能な UI のようには見せません。

- **Claude Code に `AskUserQuestion + multiSelect: true` がある場合**：モードとサイズは本物のチェックボックス、文字方式と壁紙関係は単一選択。一般サイズは正方形・縦・横のグループに分け、選択を累積し、カスタム値は自由入力します。
- **Codex に `request_user_input` しかない場合**：文字方式や壁紙関係など、相互排他的な項目だけに使います。モードやサイズを単一選択に見せかけず、組み合わせ入力で受け取ります。
- **対話ツールがない場合**：1回目にモード、2回目にサイズ＋文字方式を入力します。偽の `- [ ]` は表示せず、フォームのためだけに Plan mode への切り替えも求めません。

2回目は最初に「自動推薦／元画像比率／一般比率／カスタム」だけを表示します。一般比率を選んだときだけ、正方形 `1:1`、縦 `3:4、4:5、2:3、9:16、5:7`、横 `4:3、5:4、3:2、16:9、21:9、7:5` を展開します。複数比率と正確なピクセルを指定できます。

すべての設定はインラインでも指定できます。

```text
/xxd-panel-019 photo.jpg --mode top-bottom,design-only --size auto,3:4,9:16 --text prompt --locale ja-JP
```

`--mode`、複数指定可能な `--size`、`--text prompt|exact|none`、`--locale`、`--copy`、`--wallpaper linked|independent`、`--wallpaper-size`、`--out` に対応します。必要な値が揃っていれば質問を省略し、不足分だけを尋ねます。

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
- [中国語ランタイムアダプター](references/xxd-panel-019-prompt.zh-CN.md)
- [英語ランタイムアダプター](references/xxd-panel-019-prompt.en.md)
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
