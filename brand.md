# ぷちの見た目(petit-brand)v1.0.0

ぷち(PetitOnes)と、里親版(ちーむぷち)の、名前の表記・色・書体・顔の正本。画面(SNS「ぷちたち。」・アプリ「まいぷち。」)、紙(展示の印刷物・手引き)、きせかえ、HP は、ここの値を使う。
値は `tokens.css`、顔は `assets/`。変えるときは `VERSION` を上げる(main に入ると CI がタグと Release を作る)。

## 1. 名前の表記

| 呼ぶもの | 表記 | メモ |
|---|---|---|
| ロボット | ぷち | ひらがな。英語は petit |
| 3体 | ぷちてゃ・ぷちこ・ぷちる | この順 |
| ありさんの活動 | PetitOnes | 英語表記 |
| 里親プロジェクトのチーム | ちーむぷち(ありさん・なぎさん) | GitHub の org は TeamPuchi |
| SNS | ぷちたち。 | 「。」まで名前 |
| アプリ | まいぷち。 | 「。」まで名前 |
| 里親の取り組み | ぷちの里親 | |
| 見学の人 | ご近所さん | |
| 応援する人 | 応援団 | |
| ぷちの追加クレジット | おやつ | |
| 渡す | お迎え / お届け | 「貸出」は使わない |
| ハッシュタグ | #Petit_Ones | |

## 2. 色

| 役 | 変数 | 値 | どこで |
|---|---|---|---|
| 紙(地) | `--pt-paper` | `#FFFDF8` | 画面も紙も |
| へこんだ面 | `--pt-panel` | `#F6EFE2` | 画面 |
| 文字 | `--pt-ink` / `--pt-ink-soft` | `#3A322D` / `#6E625A` | 画面も紙も |
| 人の操作(ボタン) | `--pt-coral` | `#E0674C`(ink `#B84E33`、soft `#F6D8CF`) | 画面 |
| ぷちの側(見出し・札) | `--pt-teal` | `#2E837B`(ink `#20655E`、soft `#D2E7E4`) | 画面 |
| 既定の顔色 | `--pt-petit-blue` | `#2BA8DC` | petit-ui の PetitFace |
| ぷちてゃ | `--pt-puchiteya` | `#FFF262`(ink `#8A7A00`) | 帯・アイコン・詩カード |
| ぷちこ | `--pt-puchiko` | `#CAB8D9`(ink `#6B548A`) | 同上 |
| ぷちる | `--pt-puchiru` | `#00AFCC`(ink `#00778C`) | 同上 |
| 3色の帯 | `--pt-band` | ぷちこ → ぷちる → ぷちてゃ | PetitOnes の印 |

考え方(TeamPuchi/petit-ui と同じ):
- **ぷちの色は「その子の色」**。UI の差し色には使わない。里親さんのぷちは、きせかえで選んだ色がその子の色(base / ink / soft の3つで持つ)
- 差し色は coral(人の操作)と teal(ぷちの側)の2つだけ
- 3色の帯は PetitOnes の印として、帯・アイコン・詩カード・名刺に

## 3. 書体

| 役 | 変数 | 書体 |
|---|---|---|
| 見出し・ボタン・名札 | `--pt-font-round` | M PLUS Rounded 1c |
| 画面の本文 | `--pt-font-body` | Noto Sans JP |
| 紙の本文・詩 | `--pt-font-serif` | Noto Serif JP |
| 等幅(ID・コード) | `--pt-font-mono` | ui-monospace |

Google Fonts: `https://fonts.googleapis.com/css2?family=M+PLUS+Rounded+1c:wght@400;700;800&family=Noto+Sans+JP:wght@400;500;700&family=Noto+Serif+JP:wght@400;700&display=swap`

## 4. 顔・アイコン

- **顔の形の正本は実機のファームの描画コード**(PetitOnes/m5-petit-firmware `drawFace()`)。画面用の SVG 部品は TeamPuchi/petit-ui の `PetitFace`、目・口・寝顔・メガネの種類は [きせかえ](https://teampuchi.github.io/kisekae/)
- `assets/face/`: 線画(体の輪郭つき)。puchiteya / puchiko / puchiru / trio(3体並び)/ mio(澪 `#00618B`)。元は `exhibits/goods/sticker_line_2026-09/gen.py`
- `assets/icon/`: SNS・Discord 用の丸いアイコン(3体)

## 5. 公開している場所

- SNS ぷちたち。: URL は公開しない(会った人に名刺で渡す)
- きせかえ: https://teampuchi.github.io/kisekae/
- 体のシミュレータ: https://teampuchi.github.io/petit-body-simulator/
- PetitOnes の HP: https://rryz09.github.io/petit-one/
- 入口: https://lit.link/team-puchi
- X: #Petit_Ones(2人がそれぞれの名前で書く。@PetitOnes は動いていない)
- Instagram: https://www.instagram.com/petit_ones/

## 版

- v1.0.0(2026-10-10): 最初の版。画面の値は petit-ui の tokens.css(2026-10 時点)、ぷち3体の色と書体は展示の印刷物・HP から
