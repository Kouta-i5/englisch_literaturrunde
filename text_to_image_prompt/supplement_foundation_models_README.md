# 補足資料：基盤モデル3種（RETFound / EyeFound / EyeCLIP）

EyeDiff 論文の下流評価で使った3つの基盤モデルを、**別スライド3枚**で説明するための text-to-image プロンプト。

## ファイル一覧

| スライド案 | プロンプト | 保存先（推奨） | 原著 |
|-----------|------------|----------------|------|
| 補足 A | `supplement_retfound.md` | `assets/supplement_retfound.png` | Zhou et al., **Nature** 622:156–163 (2023) |
| 補足 B | `supplement_eyefound.md` | `assets/supplement_eyefound.png` | Shi et al., **arXiv:2405.11338** (2024) |
| 補足 C | `supplement_eyeclip.md` | `assets/supplement_eyeclip.png` | Shi et al., **npj Digit. Med.** 8:381 (2025) |

## EyeDiff 論文との対応

| モデル | アーキテクチャ（EyeDiff Methods） | 結果の掲載 |
|--------|-----------------------------------|------------|
| **RETFound** | ViT、モダリティ別ウェイト（CFP / OCT 等） | 本文 **Table 4–6** |
| **EyeFound** | ViT（統合マルチモーダル MAE） | **Supplementary Table 1** |
| **EyeCLIP** | CLIP ＋ MAE 型デコーダ、画像―言語対比 | **Supplementary Table 2** |

## 調査メモ（プロンプト記載の根拠）

### RETFound
- 約 **160万枚**のラベルなし網膜画像で SSL（**MAE**）
- **モダリティごとに別ウェイト**（EyeDiff 論文 Introduction / Methods）
- 下流：ViT 特徴 → 1024次元 → attention → FC（EyeDiff Methods）

### EyeFound
- 約 **278万枚**、**227病院**、**11モダリティ**（CFP, FFA, ICGA, FAF, RetCam, Ultrasound, OCT, Slit-lamp, External eye, Specular, Cornea topo）
- **単一の統合モデル**（RETFound との対比が重要）
- MAE、ViT-large、RETFound で初期化（原著）

### EyeCLIP
- 約 **277万枚**の画像 ＋ 臨床テキスト（原著：2,777,593 images, 11,180 reports）
- **CLIP** ＋ 画像再構成（MAE 着想）、画像―テキスト・画像―画像の対比学習
- ゼロショット / 少数ショット / VQA / 希少疾患に強み（原著）
- EyeDiff Methods：224×224、統一 vision encoder

## 口頭用（各補足スライド・各20–30秒）

**RETFound**  
「下流の主結果は RETFound ベースです。160万枚のラベルなし網膜画像で MAE 事前学習し、眼底と OCT などモダリティ別のウェイトを使います。」

**EyeFound**  
「同じ条件で EyeFound も評価しています。278万枚・11モダリティを1つの ViT で学習する統合モデルで、数値はサプリ Table 1 です。」

**EyeCLIP**  
「EyeCLIP は画像と臨床テキストの対比学習が特徴です。希少疾患のゼロショット等に強く、EyeDiff との組み合わせ結果はサプリ Table 2 です。」

## 生成手順

1. 各 `.md` プロンプトで図を1枚ずつ生成  
2. `assets/` に保存  
3. 補足 PDF（Supplementary Tables 1–2）とセットで配布・質疑用に使用  

## 注意

- プロンプト内に **AUROC 等の数値は入れない**（誤生成防止）  
- 性能比較の詳細は必ず **サプリメント表** を正とする  
