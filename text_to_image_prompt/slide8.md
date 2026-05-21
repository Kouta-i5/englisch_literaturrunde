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
Use dark navy only for section labels or key headings.
Use red only for “EyeDiff” and “Cross-attention”.
Do not use blue or pale blue filled backgrounds.
Do not use colored header bands.
Do not create a full slide.
Do not add a slide title.
Use 16:9 aspect ratio.
Leave enough empty margin.

Typography — IMPORTANT:
All descriptive labels inside the figure must be written in **Japanese**.
Use MS PGothic style for Japanese text.
Keep standard technical module names in **English** (see list below).
Use Arial style for English technical terms, numbers, and abbreviations such as CFP, t=0, token 1.
Avoid tiny text.
Do not mix English descriptive phrases if a Japanese equivalent is provided below.

Labels to keep in English (do not translate):
- EyeDiff
- Stable Diffusion v1.5-based
- Latent Diffusion Model
- VAE Encoder
- VAE Decoder
- CLIP Text Encoder
- U-Net
- Cross-attention
- CFP
- token 1, token 2, token 3, ...
- t = 0, t = 1, t = k, t = T

Example text prompt inside figure (keep English, as in paper):
“fundus image, glaucoma”

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

Upper left stream (use these exact Japanese labels):
入力眼科画像（例：CFP）
→ VAE Encoder
→ クリーンな画像潜在表現

Use one color fundus thumbnail for the input image.

Lower left stream (use these exact Japanese labels):
テキストプロンプト
“fundus image, glaucoma”
→ CLIP Text Encoder
→ トークン埋め込み

Represent token embeddings as a row of small vertical token boxes:
[token 1] [token 2] [token 3] [...]

Add a small Japanese label above or beside the token row:
テキストトークン埋め込み

Center:
A large white outlined block labeled:
EyeDiff（red text only for EyeDiff）
Stable Diffusion v1.5-based（dark navy）
Latent Diffusion Model（dark navy）

Inside the EyeDiff block, clearly split into two horizontal lanes.

Top lane (training / forward noising):
Section title:
順方向ノイズ付加過程

Small lane label in corner:
学習

Flow labels in Japanese:
クリーン潜在表現（t = 0）
→ ノイズ付加（t = 1）
→ ノイズ増加（t = k）
→ 純粋ノイズ（t = T）

Use small latent grid thumbnails that gradually become noisier from left to right.
Use arrows pointing left to right.
Optional timeline under the lane:
t = 0 → t = 1 → … → t = k → t = T

Bottom lane (generation / reverse denoising):
Section title:
逆方向ノイズ除去過程

Small lane label in corner:
生成

Flow labels in Japanese:
ランダムノイズ（t = T）
→ ステップ t の潜在表現
→ ステップ t-1 の潜在表現
→ ノイズ除去後潜在表現（t = 0）

Use small latent grid thumbnails that gradually become clearer from left to right.
Use arrows pointing left to right.

U-Net and Cross-attention:
Place a large U-Net block in the reverse denoising lane.
Inside the U-Net block, draw several small red Cross-attention modules at multiple depths.
Show token embeddings entering these red Cross-attention modules with red arrows.
Label the red pathway in Japanese:
テキスト条件付け

Important:
Make it visually clear that text token embeddings condition the denoising U-Net through Cross-attention.
Do not show text embedding as just a detached vector.
Do not show text embedding going directly to the VAE Decoder.
Do not show text embedding going directly to the final image.
Do not show the image latent going into the CLIP Text Encoder.

Right output path (use these exact Japanese labels):
ノイズ除去後潜在表現
→ VAE Decoder
→ 生成眼科画像（例：CFP）

Use one realistic orange-red fundus-like thumbnail as the generated image.

Bottom small legend (all in Japanese):
実線矢印 ＝ データの流れ
破線矢印 ＝ スキップ接続（U-Net）
赤矢印 ＝ テキスト条件付け
赤枠 ＝ Cross-attention
点線枠 ＝ 潜在空間（拡散過程）

Keep labels short and readable.
Avoid dense mathematical notation beyond t = 0, t = 1, t = k, t = T.
Make the forward noising process and reverse denoising process visually obvious.
Make the CLIP Text Encoder, token embeddings, and Cross-attention mechanism visually explicit and architecturally correct.
All descriptive text in the final figure must be Japanese except for the English technical terms listed above.
