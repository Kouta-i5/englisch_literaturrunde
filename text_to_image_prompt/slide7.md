Create only the central figure or diagram for a Japanese medical AI PowerPoint presentation.

Style:
Create a clean scientific schematic figure similar to a research paper figure, adapted for PowerPoint.
Use a pure white background.
Use mostly black, dark gray, and thin gray lines.
Most boxes should have white fill with black or dark gray outlines.
Use gray or black arrows.
Use dotted boxes when showing conceptual spaces, embeddings, synthetic image groups, or evaluation groups.
Use dark navy only for section labels, model names, or key headings.
Use red only for a few important keywords, model names, or loss terms.
Do not use blue or pale blue filled backgrounds.
Do not use colored header bands.
Avoid cartoon style, colorful icons, decorative elements, and excessive colors.
Use flat line-art, clean rectangles, arrow flows, dataset stacks, and simple medical AI diagrams.
Do not create a full presentation slide.
Do not add a slide title.
Leave enough empty margin around the figure so it can be placed inside a PowerPoint slide.
Use 16:9 aspect ratio.

Typography:
All labels should be minimal and readable.
Japanese labels should use MS PGothic style.
English letters, numbers, model names, dataset names, and abbreviations should use Arial style.
If text rendering may be unstable, keep labels short and simple.

Medical image thumbnail style:
The overall diagram should be monochrome, but medical image thumbnails must preserve modality-appropriate appearance.
CFP / fundus thumbnails should be realistic orange-red color fundus-like images.
OCT thumbnails should be grayscale cross-sectional retinal images.
FFA thumbnails should be grayscale angiography-like images.
Do not make all medical thumbnails black-and-white.
Do not create patient-identifiable images.

Accuracy:
Do not invent unsupported numerical values.
Use only the exact values explicitly provided in the prompt.
Redesign conceptually from the attached paper Figure 1 / Table 1, but do not copy the original figure exactly.

---

Create only the central dataset-flow figure for Slide 7.

Figure theme:
Clear separation between EyeDiff training data (left) and downstream evaluation data (right), with correct arrow directions so viewers do NOT think evaluation data is fed into EyeDiff training.

Overall layout:
Three-column layout: Left panel | Center EyeDiff block | Right panel.
Add a small bottom row for downstream classifier evaluation.

---

## LEFT PANEL — Generative model development data

Panel header (dark navy):
生成モデル開発用データ

Content inside panel:
- Dataset stack icon
- Exact values (must appear exactly):
  8 datasets
  42,048 images
  14 modalities
  80+ disease categories
- Short subtitle:
  大規模・多モーダル・多疾患の画像–テキストペア
- Small modality thumbnails in a row with labels:
  CFP, OCT, FFA, ICGA, FAF, Slit Lamp

Optional tiny dataset name tags (very small, do not overcrowd):
Retinal Image Bank, EyePACS, OCTDL, REFUGE, ORIGA, RIM-ONE, DRISHTI, GAMMA

---

## CENTER — EyeDiff

Center box header (red text):
EyeDiff

Subtitle:
テキスト条件付き画像生成モデル

Below the center box, a dashed rectangle:
汎化能力の高い合成画像の生成

Small icon: text prompt card → generated CFP / OCT / FFA thumbnails

---

## RIGHT PANEL — Downstream task evaluation data

Panel header (dark navy):
下流タスク評価用データ

Important small note inside panel (gray text):
※ EyeDiffの学習には使用しない

Content inside panel:
- Validation dataset stack icon
- Exact values (must appear exactly):
  11 datasets
  2 internal
  9 external
- Short subtitle:
  既存基盤モデルを用いた下流診断タスクでの性能評価
- Four task blocks (simple white mini-boxes):
  DR診断
  緑内障診断
  マルチ疾患分類
  希少疾患診断

Optional tiny dataset name tags (very small):
IDRiD, APTOS-2019, MESSIDOR-2, PAPILA, Glaucoma Fundus, JSIEC, Retina, OCTID, OCTDL, Rare Diseases

---

## ARROWS — CRITICAL (must follow exactly)

Allowed arrows ONLY:

1) LEFT panel → CENTER EyeDiff
   - Thick gray arrow
   - Label on arrow: 学習用データ

2) CENTER EyeDiff → dashed synthetic-image box below EyeDiff
   - Downward gray arrow

3) Dashed synthetic-image box → small merge node OR directly toward RIGHT panel lower area
   - Label near arrow: 生成画像

4) RIGHT panel → bottom evaluation row
   - Thick gray arrow
   - Label on arrow: 実画像

5) Merge node (if used) combining:
   - 実画像 (from right panel)
   - 生成画像 (from EyeDiff output)
   - Label: 実画像 + 生成画像（少数クラス・希少疾患を補強）

6) Bottom evaluation row → classifier block → metrics
   - Blocks:
     RETFound / EyeFound / EyeCLIP
     AUROC / AUPR

Forbidden arrows (DO NOT draw):
- Any arrow from RIGHT panel into EyeDiff center box
- Any arrow labeled 評価用データ pointing into EyeDiff
- Any arrow suggesting downstream datasets train EyeDiff

---

## BOTTOM ROW — Downstream evaluation (spanning under center-right)

A horizontal white box at the bottom:

Header:
下流分類性能の評価

Inside:
- Three small conditions as mini-blocks:
  実画像のみ
  Oversampling
  実画像 + EyeDiff生成画像
- Arrow to foundation model icons:
  RETFound / EyeFound / EyeCLIP
- Small bar chart icon labeled:
  AUROC / AUPR

---

Visual style summary:
- Pure white background
- White panels with black outlines
- Dark navy panel headers
- Gray arrows with short Japanese labels
- Red only for “EyeDiff”
- Dotted box for synthetic images
- Clean, readable, no clutter

Use exact numbers only:
8, 42,048, 14, 80+, 11, 2, 9.
Do not add other statistics.
