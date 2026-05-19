Create only the central comparison figure for Slide 4.

Figure theme:
Limitations of conventional data augmentation methods and the need for text-controllable multimodal generation.

Style:
Create a clean scientific schematic figure similar to a research paper figure, adapted for PowerPoint.
Use a pure white background.
Use mostly black, dark gray, and thin gray lines.
Most boxes should have white fill with black or dark gray outlines.
Use gray or black arrows.
Use dotted boxes for limitations.
Use dark navy only for section labels or key headings.
Use red only for important limitation keywords.
Do not use blue or pale blue filled backgrounds.
Do not use colored header bands.
Avoid cartoon style and colorful icons.
Do not create a full slide.
Do not add a slide title.
Use 16:9 aspect ratio.

Medical image thumbnail style:
CFP / fundus thumbnails should be orange-red fundus-like images.
OCT thumbnails should be grayscale cross-sectional retinal images.
FFA thumbnails should be grayscale angiography-like images.

Layout:
Top row: three-column comparison diagram.

Column 1:
Traditional augmentation
Visual:
One color fundus thumbnail transformed into three variants:
rotation
flip
color jitter
Dotted limitation box:
No new clinical information

Column 2:
Oversampling
Visual:
One minority class fundus thumbnail duplicated multiple times.
Dotted limitation box:
Overfitting risk
Use red for “Overfitting”.

Column 3:
GAN-based generation
Visual:
Noise input → GAN generator → synthetic fundus images
Dotted limitation box:
Single modality / single task
Use red for “Single modality”.

Bottom row:
A wide white outlined solution box spanning the figure.

Heading:
Needed solution:
Text-controllable multimodal generation

Inside:
Text prompts:
“fundus image, glaucoma”
“OCT, macular edema”
“FFA, diabetic retinopathy”
“fundus image, rare retinal disease”

Flow:
Text prompt → Text-to-image generative model → CFP / OCT / FFA synthetic images

Right side small bullets:
Multimodal generation
Disease and lesion control
Minority-class augmentation

Important:
Do not use the model name EyeDiff in this figure.
This is a background slide explaining the need before introducing EyeDiff.
Do not add numerical values.
