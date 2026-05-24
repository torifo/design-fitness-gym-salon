# MIDNIGHT CLUB Design Learnings

## 目的

「夜のジム × ホテルラウンジ × 会員制バー」という三位一体を、婚活サイトの空気にせずに Web で表現する。Aman の serif の品格と b-monster の暗背景の劇場性を、装飾を増やさずに重ねる。

## 設計したこと

- 配色はくすんだゴールド一色にして、派手な金（成金）と紫味の暗色（風俗）を回避した。near-black `#0b0b0d` + アンティーク・ゴールド `#c8a96a` + ivory `#ece7dd` のみ。
- メンバー紹介は顔写真ゼロ。SVG の単線シルエット + 職種・時間帯・嗜好タグだけで、プロフィールカード形式を構造的に拒否した。
- Hover 演出は「ゴールド hairline が左から伸びる」一パターンに統一。クラブのスポットライトの「灯がつく」感覚を、scale や shadow を使わず CSS の `transform: scaleX(0→1) transform-origin: left` だけで表現した。
- 価格は具体額を出さず "Annual · disclosed on interview" とした。EVENINGS の時刻は `JetBrains Mono` + `tabular-nums` で並びを揃えた。
- "By introduction only." の英文に小さく `※紹介制` を併記。英語が主、和文は補足という温度を footer で固定した。

## CSS の効いた指針

```css
/* 暗背景での Noto Serif JP は 500 以上必須。Light だと線が痩せる */
--font-jp: 'Noto Serif JP', serif; /* wght 500;600;700 のみ読み込み */

/* hairline が左から伸びる hover、装飾はこれだけ */
.evening::before {
  transform: scaleX(0);
  transform-origin: left;
  transition: transform .6s var(--ease);
}
.evening:hover::before { transform: scaleX(1); }

/* 時刻・番号は等幅、価格・ブランド名は nowrap */
.mono { font-family: var(--font-mono); font-variant-numeric: tabular-nums; }
.brand, .intro { white-space: nowrap; }
```

## 学び

「会員制」を Web で表現するとき、最も効くのは情報を増やすことではなく、削ることだった。顔写真を消し、価格を消し、CTA を消すと、残るのは serif の見出しと余白だけ。それが「敷居」として機能する。装飾を足すと、必ず婚活サイトか高級風俗のどちらかに寄ってしまう。タイポグラフィと余白だけで品位を成立させるのが、このペルソナの唯一の正解だった。
