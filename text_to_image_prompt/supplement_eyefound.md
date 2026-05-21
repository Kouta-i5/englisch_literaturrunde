Create only ONE supplementary figure for a Japanese medical AI presentation (backup slide: EyeFound).
This explains the second baseline foundation model in the EyeDiff paper (Supplementary Table 1).
Do not create a full presentation slide with a large slide title bar.
Leave generous white margin on all sides.
Use 16:9 landscape aspect ratio.

Style:
Clean scientific schematic, pure white background, black/dark gray lines.
Dark navy for headings only. Red only for model name "EyeFound" (max 2 uses).
No blue filled backgrounds. No cartoon icons. Flat academic diagram.

Typography:
Japanese descriptive text: MS PGothic style, large and readable.
English paper title, model names: Arial style.
Modality abbreviations in English: CFP, FFA, OCT, etc.

Accuracy:
Use ONLY the facts listed below. Do not invent performance numbers.

---

Figure theme:
EyeFound — multimodal generalist ophthalmic foundation model (Shi et al., arXiv 2024).

Layout (top to bottom, three zones):

【Zone 1 — Header card】
Main title (dark navy, Japanese):
EyeFound
Subline (gray, English):
A Multimodal Generalist Foundation Model for Ophthalmic Imaging

Citation line (small gray):
Shi D. et al., arXiv:2405.11338 (2024)

【Zone 2 — Concept diagram (center)】
Central large box (dotted outline optional):
Japanese label: 単一の統合モデル（11モダリティ共通）
English inside: Unified ViT-large encoder (MAE pretraining)

Surrounding ring or row of 11 small modality icons/thumbnails with English abbreviations:
CFP, FFA, ICGA, FAF, RetCam, Ultrasound, OCT, Slit-lamp, External eye, Specular, Cornea topo
Use realistic colors only for fundus/OCT thumbnails; others simple gray icons OK.

Arrow from all modalities into ONE central encoder (contrast with RETFound’s separate weights).

Pretraining flow:
Japanese: マスク付き画像再構成（MAE）
Small note: RETFound ウェイトで初期化（論文記載）

Downstream arrows to small task boxes (Japanese):
疾患分類 / 全身疾患予測 / VQA / レポート生成

【Zone 3 — Key facts (bottom, two columns)】

Left column — 学習規模 (Japanese heading):
・約278万枚（227病院）
・11の眼科画像モダリティ
・ラベルなしマルチモーダル事前学習

Right column — EyeDiff論文での位置づけ (Japanese heading):
・下流評価の基盤モデル（3つのうちの1つ）
・数値は **Supplementary Table 1**（本文 PDF には未掲載）
・RETFound と同様 ViT → 下流は MLP 分類（EyeDiff Methods）

Key difference callout box (thin red border, small text, Japanese):
RETFound：モダリティ別ウェイト ／ EyeFound：**1モデルで多モダリティ**

Optional footer (gray):
出典：Shi et al. arXiv 2024；EyeDiff論文 Supplementary Table 1

Do NOT include EyeCLIP text-image contrastive diagram.
Do NOT include AUROC numbers from benchmarks.
Generate only this EyeFound supplementary figure.
