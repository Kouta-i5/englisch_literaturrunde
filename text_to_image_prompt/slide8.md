Create only the central architecture diagram for Slide 8.

Refer to the attached paper conceptually, especially Figure 1b, and make sure the architecture is correct before drawing.
Redesign it as a clear PowerPoint figure for explaining EyeDiff.

Figure theme:
EyeDiff architecture built on Stable Diffusion v1.5.
Show EyeDiff as a Stable Diffusion v1.5-based Latent Diffusion Model with VAE Encoder, CLIP Text Encoder, U-Net, Cross-attention, and VAE Decoder.

Emphasize four mechanisms:
1. EyeDiff is based on Stable Diffusion v1.5
2. VAE image encoding into latent space
3. Forward noising and reverse denoising in latent space
4. Text conditioning through CLIP Text Encoder and Cross-attention inside U-Net

Style:
Create a clean scientific schematic figure similar to a research paper figure.
Use a pure white background.
Use mostly black, dark gray, and thin gray lines.
Most boxes should have white fill with black or dark gray outlines.
Use gray or black arrows.
Use dotted boxes only for latent space, diffusion process, or token embedding groups.
Use dark navy only for section labels, model names, or key headings.
Use red only for “EyeDiff” and “Cross-attention”.
Do not use blue or pale blue filled backgrounds.
Do not use colored header bands.
Do not create a full slide.
Do not add a slide title.
Use 16:9 aspect ratio.
Leave enough empty margin.

Typography:
Use short and readable labels.
Use English labels mainly inside the figure.
Japanese explanatory text will be added later in PowerPoint.
English letters, numbers, model names, dataset names, and abbreviations should use Arial style.
Avoid tiny text.

Medical image thumbnail style:
CFP / fundus thumbnails should be realistic orange-red color fundus-like images.
Do not create patient-identifiable images.

Architecture correctness:
The image stream and text stream must be separate.
Do not draw any arrow or dashed connection from VAE Encoder to CLIP Text Encoder.
The text prompt must go only to CLIP Text Encoder.
CLIP Text Encoder must output token embeddings.
The token embeddings must condition the U-Net through Cross-attention layers.
The text embedding should not directly become an image latent.
The VAE Encoder should output image latent.
The VAE Decoder should decode the final denoised latent into the generated ophthalmic image.
Use only one VAE Decoder on the right.

Layout:
Two separate input streams on the left.

Upper left stream:
Input ophthalmic image
→ VAE Encoder
→ Clean image latent

Use one color fundus thumbnail for the input image.

Lower left stream:
Text prompt
“fundus image, glaucoma”
→ CLIP Text Encoder
→ Token embeddings

Represent token embeddings as a row of small vertical token boxes:
[token 1] [token 2] [token 3] [...]

Add a small label:
Text token embeddings

Center:
A large white outlined block labeled:
EyeDiff
Stable Diffusion v1.5-based
Latent Diffusion Model

Use red only for “EyeDiff”.
Use dark navy for “Stable Diffusion v1.5-based” and “Latent Diffusion Model”.

Inside the EyeDiff block, clearly split into two horizontal lanes.

Top lane:
Forward noising process
Label:
training

Flow:
Clean image latent
→ add noise
→ noisy latent
→ more noise
→ pure noise

Use small latent grid thumbnails that gradually become noisier from left to right.
Use arrows pointing left to right.

Bottom lane:
Reverse denoising process
Label:
generation

Flow:
random noise
→ U-Net denoising step t
→ U-Net denoising step t-1
→ U-Net denoising step 0
→ denoised latent

Use small latent grid thumbnails that gradually become clearer from left to right.
Use arrows pointing left to right.

U-Net and Cross-attention:
Place a large U-Net block in the reverse denoising lane.
Inside the U-Net block, draw several small red Cross-attention modules at multiple depths.
Show token embeddings entering these red Cross-attention modules with red arrows.
Label the red pathway:
Text conditioning

Important:
Make it visually clear that text token embeddings condition the denoising U-Net through Cross-attention.
Do not show text embedding as just a detached vector.
Do not show text embedding going directly to the VAE Decoder.
Do not show text embedding going directly to the final image.
Do not show the image latent going into the CLIP Text Encoder.

Right:
Denoised latent
→ VAE Decoder
→ Generated ophthalmic image

Use one realistic orange-red fundus-like thumbnail as the generated image.

Bottom small legend:
solid arrow = data flow
dashed arrow = skip connection
red arrow = text conditioning
red box = Cross-attention

Keep labels short and readable.
Avoid dense mathematical notation.
Make the forward noising process and reverse denoising process visually obvious.
Make the CLIP Text Encoder, token embeddings, and Cross-attention mechanism visually explicit and architecturally correct.
