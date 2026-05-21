Create only a compact educational figure explaining AUROC and AUPR for a Japanese medical AI PowerPoint presentation.
This figure is the main visual for Slide 11 (supplement: AUROC and AUPR metrics), following Slide 10 evaluation design.
Do not create a full presentation slide.
Do not add a slide title.
Leave generous white margin on all sides.
Use 16:9 aspect ratio.

Style:
Create a clean scientific schematic figure similar to a textbook or research paper figure, adapted for PowerPoint.
Use a pure white background.
Use mostly black, dark gray, and thin gray lines.
Curve lines: black or dark gray for model curves; light gray dashed diagonal for random baseline (ROC only).
Shaded areas under curves: very light gray fill only (no blue).
Use dark navy for panel headings "ROC" and "PR".
Use red only for the labels "AUROC" and "AUPR" and their short Japanese glosses.
Do not use blue or pale blue filled backgrounds.
Do not use colored header bands.
Avoid cartoon style, 3D effects, decorative icons, and excessive colors.
Use flat 2D line charts with clear axis arrows and tick marks.
Do not invent specific numeric scores (no 0.85, no percentages on curves).

Typography:
Japanese labels: MS PGothic style.
English abbreviations and axis names: Arial style.
Keep all text short and large enough to read when embedded in a slide.

---

Figure theme:
Side-by-side comparison of ROC curve (AUROC) and Precision-Recall curve (AUPR) for binary / multi-class classification evaluation, in the context of imbalanced ophthalmic disease diagnosis.

Overall layout:
Two equal panels, left and right, separated by a thin vertical gray line.
A small bottom caption bar spanning both panels (one line, Japanese).

---

LEFT PANEL — ROC / AUROC

Panel heading (dark navy):
ROC curve

Axes:
- X-axis label: False Positive Rate (FPR)
  Japanese sublabel: 偽陽性率
- Y-axis label: True Positive Rate (TPR)
  Japanese sublabel: 感度

Draw:
- Light gray dashed diagonal line from (0,0) to (1,1) labeled "Random" / ランダム
- Solid black curve starting near origin, bending strongly toward top-left, then flattening toward (1,1) — a good classifier shape
- Light gray shaded region between the solid curve and the x-axis

Annotation on shaded region (red):
AUROC
Japanese one-line gloss below (smaller black text):
曲線下面積＝全閾値での判別性能

Small callout box (white fill, black outline) near top-left of panel:
Threshold を変えても
陽性・陰性の順位付けが
どれだけうまいか

---

RIGHT PANEL — PR / AUPR

Panel heading (dark navy):
PR curve

Axes:
- X-axis label: Recall
  Japanese sublabel: 再現率
- Y-axis label: Precision
  Japanese sublabel: 適合率

Draw:
- Light gray horizontal dashed line at low precision level, labeled "Baseline (prevalence)" / ベースライン（陽性率）
- Solid black curve starting high on the left (high precision at low recall), gradually descending toward bottom-right — good classifier on imbalanced data
- Light gray shaded region between the solid curve and the x-axis (or between curve and baseline — choose the standard PR-AUC shading)

Annotation on shaded region (red):
AUPR
Japanese one-line gloss below (smaller black text):
曲線下面積＝少数クラスに敏感

Small callout box (white fill, black outline) near top-right of panel:
陽性が少ない希少疾患で
見逃し・誤判定の
バランスを評価

---

BOTTOM CAPTION (centered, black text, one line):
下流分類では AUROC と AUPR の両方で性能を比較（少数クラス・希少疾患を重視）

Optional tiny context line above bottom caption (very small, gray, optional — omit if crowded):
Input: classifier scores from RETFound / EyeFound / EyeCLIP

---

Visual constraints:
- No confusion matrix, no fundus images, no EyeDiff logo in this figure.
- No patient photos.
- Curves must look mathematically plausible (smooth, monotonic where appropriate).
- Do not show multiple colored curves for different models; one exemplary "good model" curve per panel is enough.
- Do not add numerical AUROC/AUPR values on the figure.

Purpose for the audience:
A viewer should understand at a glance:
1) AUROC = area under ROC (TPR vs FPR), overall discrimination across thresholds.
2) AUPR = area under PR (Precision vs Recall), especially informative when positives are rare.
3) The EyeDiff paper reports both metrics for downstream classification.
