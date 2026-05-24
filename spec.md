# MIDNIGHT CLUB — fitness-gym/salon Spec

**Status:** Approved
**Author:** torifo
**Created:** 2026-05-24
**Updated:** 2026-05-24

---

## 1. Overview

### Problem Statement
都市部の高所得層は「自己投資」と「社交」を一体で求めているが、既存のフィットネスサイトはトレーニング機能や肉体の成果に偏り、ジムを「夜の社交場」として扱う設計言語が極めて少ない。一方で、出会いを前面に出すと婚活サイトの空気になり、ターゲットの審美眼に合わない。「上質な大人の社交場としてのジム」を表現する語彙が、Web 上に確立されていない。

### Goal
架空ブランド **MIDNIGHT CLUB** を、ジム × ホテルラウンジ × 会員制バーの三位一体として実装する。b-monster のクラブ的暗背景演出を骨格にしつつ、Aman のような serif の品格と余白で「下品にならない出会いの場」を成立させる。ユーザーが「夜、ここに行けば誰かと自然に話せる」と感じる温度を、装飾ではなくタイポグラフィと光の表現だけで作る。

### Non-Goals
- 婚活サイト化（プロフィール検索・マッチング機能は持たない）
- 男女の出会いを露骨に煽るコピー／写真表現
- 価格・割引キャンペーンの前面化（高級会員制の品位を損なう）
- ビフォーアフター訴求や筋肉強調の写真
- カート／決済／オンライン入会フォーム（来店予約のみ）

---

## 2. User Stories

| ID | Persona | Want to | So that |
|----|---------|---------|---------|
| US-01 | 32歳・外資金融・独身男性 | 仕事帰りに通えて、同レベルの人がいる場所を知りたい | 自然な縁を期待しつつ運動も続けられる |
| US-02 | 29歳・スタートアップPR・独身女性 | 婚活臭がなく、安全に夜の社交ができる場所を見たい | 警戒せず通えるか判断できる |
| US-03 | 36歳・経営者・DINKs | パートナーとイベントに行ける大人の場が欲しい | 既婚層でも疎外感なく社交できる |
| US-04 | 30歳・コンサル・新規検討者 | メンバー層・ドレスコード・夜の雰囲気を事前に把握したい | 場違いにならないか確認してから問い合わせできる |

---

## 3. Functional Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| FR-01 | 暗背景（near-black）+ ゴールド差し色 + serif 見出しで構成 | P0 |
| FR-02 | ヒーローに夜のラウンジ／カウンターバーの暗い写真 1 枚と短い serif コピー | P0 |
| FR-03 | EVENINGS（夜のイベントカレンダー）セクション：DJ Night / Champagne Friday / Members' Mixer 等 3〜4 件 | P0 |
| FR-04 | THE FLOOR（メンバー像紹介）：年代・職種・通う時間帯を匿名で抽象的に提示（顔写真は使わず、シルエットまたはタイポのみ） | P0 |
| FR-05 | THE LOUNGE / THE BAR（併設ラウンジ・カウンターバーの紹介）。トレーニングと同格に配置 | P0 |
| FR-06 | HOUSE RULES（ドレスコード・撮影禁止・紹介制等の作法）を明記し、品位の担保を可視化 | P0 |
| FR-07 | MEMBERSHIP（料金は税抜年額・面談制であることを示唆。具体額より「by introduction」のニュアンス） | P0 |
| FR-08 | ナビは固定上部、リンクホバー時のみゴールドの細い下線が左から伸びる | P1 |
| FR-09 | 840px 以下で 1 カラム化、EVENINGS は時刻軸の縦リストに変形 | P0 |
| FR-10 | フッターに小さく "By introduction only." の一文 | P1 |

---

## 4. Key Design Decisions

| Decision | Chosen | Rationale | Rejected |
|----------|--------|-----------|----------|
| 基調色 | near-black `#0b0b0d` + ゴールド `#c8a96a` | ホテルラウンジ／会員制バーの夜の質感。純黒は重すぎ、紫味の暗色は風俗的になる | 純黒 #000、ネイビー基調 |
| アクセント | くすんだゴールド 1 色のみ | 派手な金は成金的になる。アンティーク金で「静かな格」 | 蛍光イエロー、ローズゴールド |
| 見出し書体 | Cormorant Garamond（serif） | Aman 系の品格。ディスプレイサイズで線の細さが映える | Playfair（やや甘い）、Bodoni（硬すぎ） |
| 本文書体 | Inter（sans）+ Noto Serif JP（和文見出し） | 本文の可読性 × 和文見出しの格を両立 | Noto Sans JP 本文のみ（軽すぎ） |
| 写真 | 顔を映さない。グラス・カウンター・後ろ姿・光の粒のみ | 出会い系の匂いを避け、想像の余地で品位を保つ | メンバー集合写真、男女のツーショット |
| 装飾 | 細いゴールドの hairline（1px）と大きな余白 | "Less but precious"。Aman の余白思想 | グラデーション、ガラス効果 |
| コピートーン | 英語の短いフレーズ + 控えめな和文補足 | "Where the city slows down." のような寡黙な大人の声 | 「出会える」「マッチング」等の直接語 |
| メンバー紹介 | 顔写真なし、職種・時間帯・嗜好の抽象タグのみ | 婚活サイト化を構造的に拒否 | プロフィールカード形式 |
| Hover演出 | ゴールド hairline が左から伸びる + 文字色を ivory に | 「灯がつく」感覚。クラブのスポットライト由来 | スケール拡大、影 |

---

## 5. Design System

```css
/* Palette */
--bg:        #0b0b0d;   /* near-black, 深夜のラウンジ */
--bg-soft:   #15151a;   /* カード／セクション分割 */
--ink:       #ece7dd;   /* ivory, 本文 */
--ink-mute:  #8a8479;   /* 補足・キャプション */
--gold:      #c8a96a;   /* 唯一の差し色（アンティーク金） */
--gold-soft: #6a5a3a;   /* hairline / 区切り線 */
--line:      #2a2a30;   /* 暗背景上の薄い区切り */

/* Typography */
--font-display: 'Cormorant Garamond', 'Noto Serif JP', serif;
--font-body:    'Inter', 'Noto Sans JP', sans-serif;
--font-mono:    'JetBrains Mono', monospace;  /* 時刻・番号用 */

/* Scale */
--fs-hero:  clamp(48px, 8vw, 128px);  /* serif display */
--fs-h2:    clamp(28px, 3.6vw, 56px);
--fs-body:  16px;
--fs-cap:   12px;
--lh-body:  1.75;
--tracking-display: 0.02em;
--tracking-eyebrow: 0.24em;  /* "EVENINGS" 等の小見出し */

/* Layout */
--max:      1240px;
--pad-x:    clamp(20px, 4vw, 64px);
--gap:      clamp(48px, 8vh, 128px);

/* Motion */
--ease:     cubic-bezier(.2,.7,.2,1);
--dur:      .6s;
```

### セクション構成

```text
index.html
├── header.nav                 固定・透明→スクロール時に near-black
├── section.hero               暗いラウンジ写真 + "Where the city slows down."
├── section.evenings           夜のイベントカレンダー（3〜4件）
├── section.floor              THE FLOOR — メンバー像（匿名タグ）
├── section.lounge             THE LOUNGE / THE BAR 紹介
├── section.rules              HOUSE RULES — ドレスコード等
├── section.membership         by introduction の一文と問い合わせ
└── footer                     "By introduction only."
```

---

## 6. References

### 参照サイト
- [b-monster](https://b-monster.jp/) — 暗背景クラブ型フィットネスの骨格、PERFORMER という名づけ方
- [FEELCYCLE](https://www.feelcycle.com/) — 暗闇 × 音楽の演出パターン
- [Equinox](https://www.equinox.com/) — "It's Not Fitness. It's Life." 高級会員制のコピートーン
- [Barry's Bootcamp](https://www.barrysbootcamp.com/) — Red Room の劇場性、夜のスポットライト演出
- [Aman](https://www.aman.com/) — serif の品格、余白の思想、寡黙な大人の声

### Google Fonts
- [Cormorant Garamond](https://fonts.google.com/specimen/Cormorant+Garamond) — display serif
- [Inter](https://fonts.google.com/specimen/Inter) — body sans
- [Noto Serif JP](https://fonts.google.com/noto/specimen/Noto+Serif+JP) — 和文見出し
- [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) — 時刻・番号

### 内部参照
- [stationery/mono/spec.md](../../stationery/mono/spec.md) — spec フォーマットの基準
- [seasidebookshop/fuyunagi/spec.md](../../seasidebookshop/fuyunagi/spec.md) — 暗色系トーンの参考
