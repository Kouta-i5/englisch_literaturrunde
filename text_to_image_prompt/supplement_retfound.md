Create only ONE supplementary figure for a Japanese medical AI presentation (backup slide: RETFound).
This explains the baseline foundation model used in the EyeDiff paper (Table 4 main text).
Do not create a full presentation slide with a large slide title bar.
Leave generous white margin on all sides.
Use 16:9 landscape aspect ratio.

Style:
Clean scientific schematic, pure white background, black/dark gray lines.
Dark navy for headings only. Red only for model name "RETFound" (max 2 uses).
No blue filled backgrounds. No cartoon icons. Flat academic diagram.

Typography:
Japanese descriptive text: MS PGothic style, large and readable.
English paper title, model names, abbreviations: Arial style.
Technical module names in English: ViT, MAE, SSL, CFP, OCT.

Accuracy:
Use ONLY the facts listed below. Do not invent performance numbers or dataset counts.

---

Figure theme:
RETFound — modality-specific retinal foundation model (Zhou et al., Nature 2023).

Layout (top to bottom, three zones):

【Zone 1 — Header card】
Main title (dark navy, Japanese):
RETFound
Subline (gray, English):
A foundation model for generalizable disease detection from retinal images

Citation line (small gray):
Zhou Y. et al., Nature 622:156–163 (2023)
doi:10.1038/s41586-023-06555-x

【Zone 2 — Concept diagram (center, largest area)】
Left: stack of unlabeled retinal images (small thumbnails)
- Mix of color fundus (orange-red) and OCT (grayscale) thumbnails
- Japanese label: ラベルなし網膜画像

Center: pretraining block (white box, black outline)
English inside box: Masked Autoencoder (MAE)
Japanese sublabel: 自己教師あり学習（SSL）
Below: ViT encoder icon (simple patch grid + transformer blocks)

Arrow labeled (Japanese): 事前学習

Right: two separate weight checkpoints (important visual)
Box A label: CFP weight（眼底写真用）
Box B label: OCT weight（OCT用）
Japanese callout (small): モダリティごとに別ウェイト
This must visually differ from a single unified model.

Arrow down to downstream:
Japanese: 下流タスクへファインチューニング
Small boxes: 疾患分類 / 予後予測

【Zone 3 — Key facts (bottom, two columns)】

Left column — 学習規模 (Japanese heading):
・約160万枚のラベルなし網膜画像
・MAE（マスク付きオートエンコーダ）で表現学習
・ViT アーキテクチャ

Right column — EyeDiff論文での位置づけ (Japanese heading):
・下流評価の基盤モデル（3つのうちの1つ）
・本文 Table 4・5・6 は **RETFound** ベース
・EyeFound / EyeCLIP は Supplementary Tables 1–2

Optional small footer (gray Japanese):
出典：Zhou et al. Nature 2023；EyeDiff論文 Methods 参照

Do NOT include EyeFound or EyeCLIP architecture.
Do NOT include AUROC numbers.
Do NOT include EyeDiff pipeline.
Generate only this RETFound supplementary figure.
