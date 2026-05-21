# Slide 15 図生成ガイド

## 構成

| 位置 | プロンプト | 保存先（推奨） | 内容 |
|------|------------|----------------|------|
| 左 | `slide15_table5.md` | `assets/table5_extract.png` | Table 5 抜粋（2少数クラス × 3条件） |
| 右 | `slide15_table6.md` | `assets/table6_extract.png` | Table 6 抜粋（2希少疾患 × 3条件） |

pptx では横並び。各図は **3:4 縦長**（スライド幅の約45%）。

## 生成手順

1. `slide15_table5.md` のプロンプトで左表を生成 → `assets/table5_extract.png` に保存  
2. `slide15_table6.md` のプロンプトで右表を生成 → `assets/table6_extract.png` に保存  
3. 生成後、論文 PDF の Table 5・6 と数値照合（`script/slide15.md` のメモ欄）

## 数値の正は論文 PDF

`Boosting foundation models for rare eye disease diagnosis via a multimodal text-to-image generative framework.pdf`  
Table 5（p. 付近）、Table 6

## 旧プロンプト

`slide15.md`（単一の簡易4列表）は廃止。Table 5・6 形式に合わせて `slide15_table5.md` / `slide15_table6.md` を使用すること。
