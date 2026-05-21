Create only ONE central figure for a Japanese medical AI PowerPoint presentation (Slide 14).
This figure is a simplified excerpt of paper Table 4 (RETFound baseline vs oversampling vs EyeDiff).
Do not create a full presentation slide.
Do not add a slide title at the top of the image.
Leave generous white margin on all sides so the figure can be placed inside an existing slide.
Use 16:9 landscape aspect ratio.

Style:
Create a clean academic table figure similar to a research paper supplementary table, adapted for PowerPoint.
Use a pure white background.
Use black and dark gray text only for table body.
Use dark navy for column headers only.
Use thin gray grid lines between rows and columns.
Do not use blue or pale blue filled backgrounds.
Do not use colored header bands or cartoon style.
Flat scientific table style only.

Typography:
Japanese footnote text: MS PGothic style, readable size.
English dataset names, model names, numbers: Arial style.
Keep all text large enough to read when scaled to about 70% slide width.

Language:
Column headers may mix Japanese and English as specified below.
Dataset names and model names stay in English exactly as written.
Footnote must be in Japanese exactly as provided.

Accuracy:
Use ONLY the exact numerical values provided below.
Do not invent extra datasets, rows, or P values.
Do not abbreviate or round numbers differently.

---

Figure theme:
Table 4 excerpt — downstream classification performance (RETFound-based, 4 datasets, 3 conditions).

Layout:
One compact table with 13 data rows grouped into 4 dataset blocks (3 rows per dataset + subtle grouping).

Column headers (dark navy background, white text):
Column 1: データセット / 条件
Column 2: AUROC (95% CI)
Column 3: AUPR (95% CI)
Column 4: P値
(small gray subheader under column 4: vs RETFound)

Row groups — use exactly these values:

【IDRiD】
Row 1 label: IDRiD — RETFound
AUROC: 0.826 (0.821, 0.832)
AUPR: 0.502 (0.483, 0.520)
P: — (em dash)

Row 2 label: IDRiD — Oversample
AUROC: 0.833 (0.826, 0.841)
AUPR: 0.516 (0.499, 0.532)
P: 0.012*

Row 3 label: IDRiD — EyeDiff
AUROC: 0.837 ↑ (0.833, 0.840)
AUPR: 0.518 ↑ (0.509, 0.527)
P: 0.008*
(↑ in red if color is used; otherwise bold black)

【Glaucoma Fundus】
Row 4: Glaucoma Fundus — RETFound
0.950 (0.937, 0.964) | 0.876 (0.841, 0.911) | —

Row 5: Glaucoma Fundus — Oversample
0.954 (0.940, 0.968) | 0.879 (0.843, 0.915) | 0.009*

Row 6: Glaucoma Fundus — EyeDiff
0.959 ↑ (0.945, 0.973) | 0.893 ↑ (0.855, 0.931) | 0.008*

【ImageBank】
Row 7: ImageBank — RETFound
0.871 (0.863, 0.891) | 0.439 (0.401, 0.462) | —

Row 8: ImageBank — Oversample
0.893 (0.872, 0.923) | 0.471 (0.454, 0.501) | <0.001*

Row 9: ImageBank — EyeDiff
0.919 ↑ (0.882, 0.931) | 0.530 ↑ (0.497, 0.550) | <0.001*

【OphthalWeChat】
Row 10: OphthalWeChat — RETFound
0.613 (0.570, 0.634) | 0.397 (0.351, 0.431) | —

Row 11: OphthalWeChat — Oversample
0.650 (0.603, 0.692) | 0.411 (0.382, 0.437) | <0.001*

Row 12: OphthalWeChat — EyeDiff
0.663 ↑ (0.629, 0.701) | 0.439 ↑ (0.401, 0.468) | <0.001*

Visual grouping:
- Light gray horizontal band or slightly thicker separator between each dataset block (4 blocks).
- RETFound rows: normal weight.
- Oversample rows: normal weight.
- EyeDiff rows: very subtle light gray row background OR bold dataset name only on EyeDiff rows.

Table footnote (bottom, small gray Japanese text, two lines):
Line 1: P値はベースライン RETFound との比較。*P<0.05。↑は EyeDiff による改善。
Line 2: 出典：論文 Table 4 抜粋（11データセット中4例）

Optional tiny legend box (bottom right, minimal):
↑ = EyeDiff improvement
* = P<0.05 vs RETFound

Do NOT include bar charts.
Do NOT include ImageBank-only emphasis or rare-disease titles.
Do NOT include Table 5 or Table 6 content.
Do NOT include EyeFound or EyeCLIP results.
Generate only this single table figure.
