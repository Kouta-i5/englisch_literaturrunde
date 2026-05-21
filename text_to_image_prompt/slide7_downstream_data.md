Create only the central figure or diagram for a Japanese medical AI PowerPoint presentation.

Match the EXACT same layout, composition, and visual hierarchy as the companion figure “生成モデル開発用データ” (generative model development data panel).
Use the same proportions: one large white rounded rectangle panel, blue top title, four-column statistics row with vertical separators, gray subtitle, middle split (left examples + right labeled thumbnails), bottom row of rounded dataset pills, and optional right-side flow arrow.

Style:
Pure white background inside the panel.
Thin gray or black outer border with slightly rounded corners.
Title in bold blue Japanese text (same style as development-data figure).
Statistics in large black numbers with smaller English labels below each number.
Vertical gray lines separating the four statistics.
Gray subtitle text centered under the statistics row.
Clean flat design, no cartoon style, no colored header bands.
Do not create a full PowerPoint slide with slide title bar.
Leave margin around the panel.
Use 16:9 aspect ratio.

Typography:
Japanese: MS PGothic style.
English / numbers / dataset names: Arial style.
Keep all text short and readable.

Medical thumbnails:
CFP in realistic orange-red.
OCT and FFA in grayscale.
Do not create patient-identifiable images.

Accuracy:
Use only the exact values and names provided below.
Do not invent extra datasets or numbers.

---

Create only the DOWNSTREAM TASK EVALUATION DATA panel (下流タスク評価用データ).
This panel must look like a paired “sibling” figure to the development-data panel, with identical structure but different content.

---

## TOP — Title (bold blue, centered)

下流タスク評価用データ

Small gray note directly under title (smaller font):
※ EyeDiffの学習には使用しない

---

## STATISTICS ROW — Four columns with vertical separators (same layout as development panel)

Column 1:
11
datasets

Column 2:
2
internal

Column 3:
9
external

Column 4:
4
evaluation tasks

Use exact values only: 11, 2, 9, 4.

---

## SUBTITLE (gray, centered under statistics)

既存基盤モデルを用いた下流診断タスクでの性能評価

---

## MIDDLE SECTION — Two columns (same proportions as development panel)

### Left column — Task examples (mirror the “image + text” rows on the development panel)

Show three horizontal rows. Each row contains:
- a small document or label-card icon on the left
- a small medical image thumbnail in the middle
- a short Japanese task description on the right

Row 1:
CFP fundus thumbnail (orange-red)
Text: DR診断（5段階重症度）

Row 2:
CFP fundus thumbnail (orange-red)
Text: 緑内障診断（非緑内障 / 早期 / 進行）

Row 3:
OCT thumbnail (grayscale)
Text: 希少疾患診断（少数クラス）

Do NOT show text-to-image training pairs.
Do NOT show prompt engineering cards.

---

### Right column — Four evaluation-task columns (mirror the six-modality grid, but use 4 tasks)

Create four vertical mini-columns (equal width), each with:
- task label on top
- representative medical thumbnail in the middle
- simple line-art icon below

Column 1:
Label: DR診断
Thumbnail: CFP fundus image
Icon: simple 5-step severity bar or grade icon

Column 2:
Label: 緑内障診断
Thumbnail: CFP fundus image
Icon: optic disc / cup outline icon

Column 3:
Label: マルチ疾患分類
Thumbnail: mix of small CFP and OCT thumbnails
Icon: multi-label tag icon

Column 4:
Label: 希少疾患診断
Thumbnail: rare-case fundus or multimodal thumbnail
Icon: rare / long-tail icon (small tail distribution)

---

## BOTTOM ROW — Rounded rectangular dataset pills (same style as development panel)

Arrange dataset names in rounded pill boxes.
Prefer one horizontal row if readable; if crowded, use two compact rows.

Must include these exact dataset names:
IDRiD
APTOS-2019
MESSIDOR-2
PAPILA
Glaucoma Fundus
JSIEC
Retina
OCTID
OCTDL
Rare Diseases

Optional 11th pill (only if space allows, same visual style):
OphthalWeChat

Do not include training-only datasets:
EyePACS, REFUGE, ORIGA, RIM-ONE, DRISHTI, GAMMA as training sources unless listed above.

---

## RIGHT EDGE — Flow arrow (same position as development panel, but different meaning)

Thick gray arrow leaving the panel toward the right.

Arrow label above or beside arrow (Japanese):
評価用データ → 下流分類評価

Small destination box at arrow tip (rounded square, same style as EyeDiff box in development figure):
Inside box, stacked text:
RETFound
EyeFound
EyeCLIP
Small sub-label below:
AUROC / AUPR

Use dark navy or black for model names.
Do NOT use red text unless labeling a tiny “+生成画像” note.

Optional small dotted box near the arrow origin (between panel and classifier box):
+ EyeDiff生成画像
with a thin arrow merging into the classifier box
(This shows synthetic augmentation, NOT training input into EyeDiff.)

---

## FORBIDDEN (critical)

- Do NOT draw “評価用データ → EyeDiff”
- Do NOT draw any arrow from this panel into an EyeDiff training block
- Do NOT duplicate the development-panel title or numbers (8, 42,048, 14, 80+)
- Do NOT imply downstream datasets train EyeDiff

---

## Visual consistency checklist

Same as development-data figure:
✓ Blue centered main title
✓ 4 statistics with vertical dividers
✓ Gray subtitle
✓ Left example rows + right thumbnail grid
✓ Bottom dataset pills
✓ Right-side gray arrow to next step
✓ White panel, minimal colors, professional medical AI schematic
