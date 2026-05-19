# EyeDiff 英文抄読会スライド作成

## 概要

本リポジトリは、医療AI研究室の英文抄読会で使用する日本語スライドを作成するための作業用リポジトリである。

発表対象論文は以下である。

**Boosting foundation models for rare eye disease diagnosis via a multimodal text-to-image generative framework**  
Ruoyu Chen, Weiyi Zhang, Bowen Liu, et al.  
npj Digital Medicine, 2026

本論文では、眼科領域における希少疾患・少数クラスのデータ不足を解決するために、テキストプロンプトから病変を保持した多モーダル眼科画像を生成する **EyeDiff** を提案している。EyeDiffは、Stable Diffusion v1.5を基盤としたLatent Diffusion Modelであり、VAE、CLIP Text Encoder、U-Net、Cross-attentionを用いて、テキスト条件付きで眼科画像を生成する。

EyeDiffは、8データセット・42,048画像を用いて開発され、14種類の眼科画像モダリティと80以上の疾患カテゴリを扱っている。また、2つのinternal datasetと9つのexternal dataset、合計11データセットを用いて下流分類性能が評価されている。評価では、生成画像そのものの品質評価としてVQAScore、Turing test、Visual quality scoreが用いられ、さらに生成画像を少数クラス・希少疾患のデータ拡張に用いた際の診断性能がAUROC/AUPRで評価されている。 [oai_citation:0‡Boosting foundation models for rare eye disease diagnosis via a multimodal text-to-image generative framework.pdf](sediment://file_00000000a6987209a4cd11c11765e67d)

## スライド構成

本発表は、10〜15分の英文抄読会を想定し、全15枚で構成する。  

構成は「背景 → 目的 → 方法 → 結果 → 結論」の流れとし、EyeDiffの研究背景、モデル構造、評価設計、生成画像の品質評価、下流分類性能の改善までを順に説明する。

### Slide 1：タイトル

**タイトル**  

希少眼疾患診断における基盤モデル性能向上のための  

マルチモーダルText-to-Image生成フレームワーク

**内容**

- 論文名

- 著者名

- 掲載誌

- 発表者名

**役割**  

発表対象論文とテーマを提示する。

---

### Slide 2：背景：眼科AIにおける基盤モデルの進展

**主張**  

眼科画像AIでは、RETFound、EyeFound、EyeCLIPのような基盤モデルにより、少量データでも高性能な診断モデルを構築できる可能性が広がっている。

**使用する図**

- RETFound / EyeFound / EyeCLIPの比較図

- Large-scale ophthalmic data → Foundation model → Few-shot fine-tuning → Disease diagnosis の流れ

**説明ポイント**

- RETFound：網膜画像に特化した基盤モデル

- EyeFound：マルチモーダル眼科画像から汎用表現を学習

- EyeCLIP：眼科画像と言語を対応づけるVision-Language model

- 本研究では、これらの基盤モデルを下流診断タスクのベースラインとして使用する

---

### Slide 3：背景：少数クラス・希少疾患の課題

**主張**  

基盤モデルを用いても、少数クラスや希少疾患では十分な性能を得ることが難しい。

**使用する図**

- Few samples → Weak feature learning → Unstable diagnosis

- Majority classes / Minority classes / Rare diseases のクラス不均衡概念図

**説明ポイント**

- 少数クラス・希少疾患では学習画像が少ない

- 疾患特異的な病変特徴を十分に学習しにくい

- 医療画像共有にはプライバシーや施設間制約がある

- 少数クラスを安全かつ多様に補うデータ拡張が必要である

---

### Slide 4：背景：従来のデータ拡張の限界

**主張**  

従来のデータ拡張では、少数クラス・希少疾患に対する汎用的な解決には限界がある。

**使用する図**

- Traditional augmentation

- Oversampling

- GAN-based generation

- Text-controllable multimodal generation の必要性

**説明ポイント**

- Traditional augmentation：既存画像を変形するだけで、新しい臨床情報は増えにくい

- Oversampling：少数クラス画像を複製するため、過学習リスクがある

- GAN-based generation：多くは単一モダリティ・単一タスクに限定されやすい

- テキストで制御可能なマルチモーダル生成モデルが必要である

---

### Slide 5：目的

**主張**  

EyeDiffが、テキストプロンプトから病変を保持した多モーダル眼科画像を生成できるか、さらに生成画像を用いることで下流分類性能が改善するかを検証する。

**内容**

- 生成画像は臨床的に妥当か？

- 生成画像は下流診断性能を改善するか？

**役割**  

背景で提示したデータ不足・クラス不均衡の課題に対して、本論文が何を検証するのかを明確にする。

---

### Slide 6：方法：研究全体の流れ

**主張**  

EyeDiffを学習し、少数クラス・希少疾患の合成画像を生成して、下流診断性能を評価した。

**使用する図**

5ステップの横方向ワークフロー。

1. Image-text pairs  

   - 8 datasets

   - 42,048 images

2. Structured prompts  

   - modality

   - disease

   - lesion

   - severity

3. EyeDiff training  

   - Stable Diffusion v1.5

   - Latent Diffusion Model

4. Synthetic augmentation  

   - minority classes

   - rare diseases

5. Downstream evaluation  

   - RETFound / EyeFound / EyeCLIP

   - AUROC / AUPR

**説明ポイント**

- Figure 1の研究デザインを発表用に簡略化して説明する

- 生成モデル開発から下流分類評価までの全体像を示す

---

### Slide 7：方法：データセット

**主張**  

生成モデル開発データと下流評価データを明確に分けて設計している。

**使用する図**

左右2パネルのデータセット概要図。

**左：生成モデル開発データ**

- 8 datasets

- 42,048 images

- 14 modalities

- 80+ disease categories

**右：下流評価データ**

- 11 datasets

- 2 internal

- 9 external

- DR diagnosis

- Glaucoma diagnosis

- Multi-disease classification

- Rare disease diagnosis

**説明ポイント**

- EyeDiffは広範な眼科画像・テキストペアで開発されている

- 下流評価では複数の疾患・モダリティ・施設由来データセットで汎化性を検証している

---

### Slide 8：方法：EyeDiffのモデル構造

**主張**  

EyeDiffはStable Diffusion v1.5を基盤としたLatent Diffusion Modelであり、VAE、CLIP Text Encoder、U-Net、Cross-attentionを用いてテキスト条件付き画像生成を行う。

**使用する図**

EyeDiffのアーキテクチャ図。

**図に含める要素**

- Input ophthalmic image → VAE Encoder → Clean image latent

- Text prompt → CLIP Text Encoder → Text token embeddings

- EyeDiff / Stable Diffusion v1.5-based / Latent Diffusion Model

- Forward noising process

- Reverse denoising process

- U-Net内のCross-attention

- Denoised latent → VAE Decoder → Generated image

**説明ポイント**

- 画像はVAE Encoderで潜在表現に圧縮される

- 学習時はlatentに段階的にノイズを加える

- 生成時はランダムノイズからU-Netで段階的にdenoiseする

- テキストプロンプトはCLIP Text Encoderでtoken embeddingsに変換される

- token embeddingsがU-Net内のCross-attentionを通じてdenoising過程を条件付ける

- 最後にVAE Decoderで生成眼科画像に復元する

---

### Slide 9：方法：テキストプロンプト設計

**主張**  

EyeDiffでは、モダリティ・疾患・病変・重症度などを含む構造化プロンプトにより、生成画像を制御する。

**使用する図**

上段にStructured Text Prompt、下段にFigure 2風の代表例を配置する。

**上段：Structured Text Prompt**

- Modality

- Disease

- Lesion

- Severity

**中段**

- Structured text prompt → EyeDiff → Generated ophthalmic images

**下段：Figure 2風の代表例**

| Text Prompt | Generated Image | Real Reference |

|---|---|---|

| color fundus, glaucoma | 生成画像 | 実画像参照 |

| color fundus, severe diabetic retinopathy | 生成画像 | 実画像参照 |

| ffa, macular dystrophy, degeneration | 生成画像 | 実画像参照 |

| oct, macular edema, retinal vein occlusion | 生成画像 | 実画像参照 |

**説明ポイント**

- プロンプトは画像モダリティ、疾患または病変タイプ、重症度などから構成される

- テキストを変えることで、生成するモダリティ・疾患・病変を制御できる

- 黄色矢印は、指定された病変・臨床所見の位置を示す

---

### Slide 10：方法：評価設計

**主張**  

EyeDiffが生成した合成眼科画像を、生成画像そのものの品質と、下流診断タスクへの有用性の2段階で評価する。

**使用する図**

中央にEyeDiffとGenerated ophthalmic imagesを配置し、そこからStage 1とStage 2に分岐する評価設計図。

**中央**

- Text prompt

- EyeDiff

- Generated ophthalmic images

**Stage 1：Image quality evaluation**

- VQAScore

- Turing test

- Visual quality score

**Stage 2：Downstream classification evaluation**

- Real images only

- Oversampling

- Real + EyeDiff images

- RETFound / EyeFound / EyeCLIP

- AUROC / AUPR

**説明ポイント**

- Stage 1では、生成画像がテキストと合っているか、本物らしいか、病変・構造を再現しているかを評価する

- Stage 2では、生成画像を少数クラス・希少疾患のデータ拡張に用いた際、分類性能が改善するかを評価する

---

### Slide 11：結果：生成画像の品質評価

**主張**  

EyeDiff生成画像は、一定のテキスト整合性と医学的リアリティを示した。

**使用する図**

左にVQAScore横棒グラフ、右にTuring testの結果を配置する。

**VQAScore**

- OCT-based disease detection：0.822

- CFP-based multi-category diagnosis：0.776

- Multimodal rare disease diagnosis：0.670

**Turing test**

- Grader 1：62.00%

- Grader 2：66.00%

**Artifacts**

- color tone

- lesion boundary

- noise

**説明ポイント**

- VQAScoreによりテキストと生成画像の整合性を評価している

- Turing testでは、生成画像が実画像と誤認された割合を示している

- 一方で、色調、病変境界、ノイズなどの違和感も残っている

---

### Slide 12：結果：生成画像の具体例

**主張**  

テキストプロンプトで指定された病変所見が、生成画像上に反映されている。

**使用する図**

Figure 2風の3列構成。

| Text Prompt | Generated Image | Real Reference |

|---|---|---|

| color fundus, glaucoma | 生成画像 | 実画像参照 |

| color fundus, severe diabetic retinopathy | 生成画像 | 実画像参照 |

| OCT, vitreomacular traction, macular hole | 生成画像 | 実画像参照 |

| OCT, macular edema, retinal vein occlusion | 生成画像 | 実画像参照 |

**説明ポイント**

- 黄色矢印は病変・臨床所見の位置を示す

- 生成画像と実画像参照を比較することで、病変保持性を視覚的に確認できる

- Figure 2では、視神経乳頭陥凹拡大、糖尿病網膜症の出血や白斑、黄斑円孔、黄斑浮腫などが例示されている

---

### Slide 13：結果：下流分類性能の改善

**主張**  

EyeDiff生成画像の追加により、希少疾患を含むデータセットでAUROC/AUPRが改善した。

**使用する図**

2つの棒グラフ。

**Rare Diseases dataset**

- Baseline AUROC：0.871

- EyeDiff AUROC：0.919

- Baseline AUPR：0.439

- EyeDiff AUPR：0.530

**OphthalWeChat dataset**

- Baseline AUROC：0.613

- EyeDiff AUROC：0.663

- Baseline AUPR：0.397

- EyeDiff AUPR：0.439

**説明ポイント**

- Rare Diseases datasetでは、AUROCが0.871から0.919、AUPRが0.439から0.530に改善した

- OphthalWeChat datasetでも、AUROCが0.613から0.663、AUPRが0.397から0.439に改善した

- EyeDiffによる合成画像追加が、希少疾患分類性能の改善に寄与した

---

### Slide 14：結果：少数クラス・希少疾患での改善

**主張**  

少数クラスや希少疾患では、特にAUPRの改善が重要であり、EyeDiff追加により代表例でAUROC/AUPRが改善した。

**使用する図**

表形式の結果図。

| Target | Baseline | EyeDiff | Interpretation |

|---|---|---|---|

| Early glaucoma | AUROC 0.860 / AUPR 0.570 | AUROC 0.927 / AUPR 0.809 | Minority class improved |

| Stargardt disease | AUROC 0.695 / AUPR 0.513 | AUROC 0.816 / AUPR 0.723 | Rare disease improved |

| Retinoblastoma | AUROC 0.740 / AUPR 0.316 | AUROC 0.787 / AUPR 0.742 | Large AUPR improvement |

**説明ポイント**

- Early glaucomaは少数クラスとして評価されている

- Stargardt diseaseとRetinoblastomaは希少疾患として評価されている

- 陽性例が少ないタスクではAUPRが重要である

- EyeDiff追加により、少数クラス・希少疾患で性能改善が確認された

---

### Slide 15：結論

**主張**  

EyeDiffは、医療画像におけるデータ不足・クラス不均衡を補う有用な合成画像生成フレームワークである。

**結論**

- EyeDiffは、テキストプロンプトから病変を保持した多モーダル眼科画像を生成できた

- 生成画像を追加することで、基盤モデルの診断性能が改善した

- 少数クラス・希少疾患のデータ拡張として有望である

- 一方で、生成画像には色調・ノイズ・病変位置の違和感が残るため、臨床応用にはさらなる品質検証とバイアス評価が必要である

**役割**  

目的で提示した2つの問いに対する答えとして、生成画像の妥当性と下流分類性能改善の両方をまとめる。
