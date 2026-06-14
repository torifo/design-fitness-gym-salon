---
name: design-fitness-gym-salon
description: "fitness gym / studio landing-page design study — 'salon' theme/persona (pure HTML/CSS/JS, no build). Use when designing a 'salon'-style fitness gym / studio site aesthetic. Where the city slows down. fitness gym / studioの「salon」テーマLPのデザイン参照スキル。"
---

# design-fitness-gym-salon

A landing-page **design study** for a fictional **salon**-theme fitness gym / studio (pure HTML + CSS + vanilla JS, no build, GitHub-Pages ready). Use this as a **style / design-system reference** when building a similar aesthetic.

架空の「salon」テーマのfitness gym / studio LP デザイン研究。同種の世界観を作るときの**スタイル／デザインシステム参照**として使う。

## When to use / 使いどころ
- **EN:** designing a 'salon'-style fitness gym / studio site — match its palette, typography and layout discipline.
- **JP:** 「salon」系のfitness gym / studioサイトを設計するとき。配色・タイポ・レイアウト規律を流用。

## Bundled assets / 同梱アセット
This skill folder is the reference implementation — start from these files:
- `index.html` — full page markup
- `style.css` — design tokens (CSS custom properties) + layout
- `script.js` — vanilla JS (if present)
- `README.md` — full bilingual doc, brand context and series links

## Design reference / デザイン参照
_Lifted from the repo README — see README.md for the complete, bilingual version._

### Overview
**fitness-gym design research series** の「夜の社交場」ペルソナ作品。

都市部の高所得層に向けて、トレーニング・ホテルラウンジ・会員制バーを一つの灯のもとに置く、紹介制クラブの空気を Web 上で立ち上げる試み。婚活サイト化を構造的に拒否し、装飾ではなくタイポグラフィと余白で「下品にならない出会いの場」を成立させる。

### Brand
| | |
|--|--|
| **Brand** | MIDNIGHT CLUB |
| **Tagline** | Where the city slows down. |
| **Aesthetic** | Near-black × Antique gold × Ivory |
| **Concept** | Gym × Hotel lounge × Members' bar |
| **Target Persona** | 30s 前後の外資金融・経営者・クリエイティブ |
| **Color** | `#0b0b0d` near-black + `#c8a96a` antique gold + `#ece7dd` ivory |
| **Display Font** | Cormorant Garamond |
| **JP Display** | Noto Serif JP (500+) |
| **Body Font** | Inter |
| **Mono Font** | JetBrains Mono (時刻・番号) |

### Design Approach
- 暗背景 × アンティーク・ゴールド一色 × serif で、ホテルラウンジの夜の質感を作る
- 顔写真はゼロ。メンバー像は SVG シルエット + 抽象タグだけで提示し、婚活サイト化を構造的に拒否
- "By introduction only." を footer に小さく添え、品位のある敷居を可視化（小さく日本語「※紹介制」を併記）
- Hover 演出はゴールド hairline が左から伸びるパターンで統一（クラブのスポットライト由来）
- 時刻・番号は `JetBrains Mono` + `tabular-nums`、ブランド名・価格表記には `white-space: nowrap`

## Tech / 技術
- Vanilla HTML / CSS / 最小限の JS — single file (`index.html`)
- Google Fonts: Cormorant Garamond, Inter, Noto Serif JP, JetBrains Mono
- ビルドツール不要

## How to apply / 適用方法
1. Reuse `style.css` custom properties (color / type / spacing tokens) as the design-system base.
2. Copy `index.html` layout as the starting structure, then swap brand name and content.
3. Keep the palette, font pairing and layout discipline described above.

---
> The brand is fictional (design study) — replace all brand/content. Full context: see **`README.md`**.
