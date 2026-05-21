Create only ONE supplementary figure for a Japanese medical AI presentation (backup slide: EyeCLIP).
This explains the third baseline foundation model in the EyeDiff paper (Supplementary Table 2).
Do not create a full presentation slide with a large slide title bar.
Leave generous white margin on all sides.
Use 16:9 landscape aspect ratio.

Style:
Clean scientific schematic, pure white background, black/dark gray lines.
Dark navy for headings only. Red only for model name "EyeCLIP" (max 2 uses).
No blue filled backgrounds. No cartoon icons. Flat academic diagram.

Typography:
Japanese descriptive text: MS PGothic style, large and readable.
English model names and framework names: Arial style (CLIP, MAE, VQA).

Accuracy:
Use ONLY the facts listed below. Do not invent benchmark AUROC values.

---

Figure theme:
EyeCLIP — multimodal visual-language foundation model for computational ophthalmology (Shi et al., npj Digital Medicine 2025).

Layout (top to bottom, three zones):

【Zone 1 — Header card】
Main title (dark navy, Japanese):
EyeCLIP
Subline (gray, English):
A multimodal visual-language foundation model for computational ophthalmology

Citation line (small gray):
Shi D. et al., npj Digital Medicine 8:381 (2025)
doi:10.1038/s41746-025-01772-2

【Zone 2 — Concept diagram (center)】
Three-input pretraining schematic:

Left input: ophthalmic image thumbnails (multiple modalities, small)
Japanese label: 多モダリティ画像

Center input: clinical text / report snippet (document icon, not real patient text)
Japanese label: 臨床テキスト（部分）

Right: unified vision encoder box
English: Shared vision encoder (all modalities)
Japanese sublabel: モダリティ不変な表現

Three training objective boxes connected to encoder (horizontal row):
Box 1 (Japanese main / English sub):
画像―テキスト対比学習
Image-text contrastive (CLIP)

Box 2:
画像―画像対比学習
Cross-modality alignment

Box 3:
マスク画像再構成
MAE-style reconstruction

Framework label (small): CLIP + MAE-inspired decoder

Downstream task arrows (Japanese):
ゼロショット分類 / 少数ショット / VQA / クロスモーダル検索 / 希少疾患

【Zone 3 — Key facts (bottom, two columns)】

Left column — 学習規模 (Japanese heading):
・約277万枚の眼科画像 ＋ 臨床テキスト
・11モダリティ、12万人以上の患者規模（原著）
・224×224、CLIP系の対比学習

Right column — EyeDiff論文での位置づけ (Japanese heading):
・下流評価の基盤モデル（3つのうちの1つ）
・数値は **Supplementary Table 2**（本文 PDF には未掲載）
・長尾・希少疾患のゼロ/少数ショットに強み（原著）

Key difference callout (thin border, Japanese):
画像＋言語の共有埋め込み空間（RETFound / EyeFound は主に画像表現）

Optional footer (gray):
出典：Shi et al. npj Digital Medicine 2025；EyeDiff論文 Supplementary Table 2

Do NOT include RETFound separate-weight diagram.
Do NOT include specific AUROC from 14 datasets.
Generate only this EyeCLIP supplementary figure.
