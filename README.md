# MIDNIGHT CLUB — design-fitness-gym-salon

> **架空ブランド注記**: MIDNIGHT CLUB はデザイン研究のために作成した架空の会員制ジムです。実在の施設・店舗ではありません。

## Overview

**fitness-gym design research series** の「夜の社交場」ペルソナ作品。

都市部の高所得層に向けて、トレーニング・ホテルラウンジ・会員制バーを一つの灯のもとに置く、紹介制クラブの空気を Web 上で立ち上げる試み。婚活サイト化を構造的に拒否し、装飾ではなくタイポグラフィと余白で「下品にならない出会いの場」を成立させる。

## Brand

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

## Design Approach

- 暗背景 × アンティーク・ゴールド一色 × serif で、ホテルラウンジの夜の質感を作る
- 顔写真はゼロ。メンバー像は SVG シルエット + 抽象タグだけで提示し、婚活サイト化を構造的に拒否
- "By introduction only." を footer に小さく添え、品位のある敷居を可視化（小さく日本語「※紹介制」を併記）
- Hover 演出はゴールド hairline が左から伸びるパターンで統一（クラブのスポットライト由来）
- 時刻・番号は `JetBrains Mono` + `tabular-nums`、ブランド名・価格表記には `white-space: nowrap`

## Sections

- `hero` — 暗いラウンジ写真 + "Where the city slows down."
- `evenings` — 週ごとの夜のイベント（Jazz / Champagne / Mixer / Slow Sunday）
- `floor` — メンバー像、顔なし SVG シルエット + 職種・時間帯・嗜好タグ
- `lounge` — THE LOUNGE / THE BAR 紹介（トレーニングと同格）
- `rules` — HOUSE RULES（ドレスコード・撮影禁止・紹介制等）
- `membership` — 面談制であることを示唆、具体額は非公開

## Tech

- Vanilla HTML / CSS / 最小限の JS — single file (`index.html`)
- Google Fonts: Cormorant Garamond, Inter, Noto Serif JP, JetBrains Mono
- ビルドツール不要

## Local Development

```bash
open index.html
# または
python3 -m http.server 8080
```

## Deployment

GitHub Pages + Cloudflare DNS で `design.fitness-gym-salon.riumu.net` に公開。
