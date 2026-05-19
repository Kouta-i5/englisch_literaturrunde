Create only the central figure or diagram for a Japanese medical AI PowerPoint presentation.

Style:
Create a clean scientific schematic figure similar to a research paper figure, adapted for PowerPoint.
Use a pure white background.
Use mostly black, dark gray, and thin gray lines.
Most boxes should have white fill with black or dark gray outlines.
Use gray or black arrows.
Use dotted boxes when showing conceptual spaces, embeddings, or evaluation groups.
Use dark navy only for section labels, model names, or key headings.
Use red only for a few important keywords, model names, or loss terms.
Do not use blue or pale blue filled backgrounds.
Do not use colored header bands.
Avoid cartoon style, colorful icons, decorative elements, and excessive colors.
Use flat line-art, clean rectangles, arrow flows, encoder/decoder blocks, dataset stacks, simple charts, and simple medical AI diagrams.
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
Slit lamp or external eye thumbnails should look like small realistic anterior or ocular images when needed.
Do not make all medical thumbnails black-and-white.
Do not create patient-identifiable images.

Accuracy:
Do not invent unsupported numerical values.
Use only the exact values explicitly provided in the prompt.
If a figure is based on the attached paper, use it conceptually and redesign it as a clean slide-friendly diagram rather than copying the original figure exactly.Create only the central workflow figure for Slide 6.

Refer to the attached paper conceptually, especially Figure 1, but redesign it as a clean slide-friendly schematic.

Figure theme:
Overall study workflow of EyeDiff.

Layout:
Horizontal five-step pipeline.

Step 1:
Image-text pairs
8 datasets
42,048 images

Visual:
Stacked multimodal ophthalmic thumbnails plus document sheets.

Step 2:
Structured prompts
modality
disease
lesion
severity

Visual:
Prompt cards with short labels.

Step 3:
EyeDiff training
Stable Diffusion v1.5
Latent Diffusion Model

Visual:
Diffusion model block with noise → denoising → image.

Step 4:
Synthetic augmentation
minority classes
rare diseases

Visual:
Generated CFP/OCT/FFA thumbnails.

Step 5:
Downstream evaluation
RETFound / EyeFound / EyeCLIP
AUROC / AUPR

Visual:
Classifier block plus small bar chart.

Arrows:
Connect all steps left to right with thick gray arrows.

Style:
Pure white background.
White boxes with black outlines.
Dark navy labels.
Gray arrows.
Use red only for “EyeDiff”.
Use exact numbers only:
8 datasets, 42,048 images.
