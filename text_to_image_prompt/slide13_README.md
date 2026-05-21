# Slide 13：生成画像の品質評価 — 図生成用プロンプト

Slide 13 では **3つの評価**を横並びで示す。GPT Image 等では **1枚ずつ別プロンプトで生成**し、pptx で横に配置する。

| 順（左→右） | ファイル | 内容 |
|-------------|----------|------|
| 左 | [slide13_vqascore.md](slide13_vqascore.md) | VQAScore 横棒（0.822 / 0.776 / 0.670） |
| 中 | [slide13_turing_test.md](slide13_turing_test.md) | Turing test（62% / 66%） |
| 右 | [slide13_visual_quality_score.md](slide13_visual_quality_score.md) | Visual quality score（5段階＋平均点） |

## 論文照合（2026-03 手元 PDF）

照合元：`Boosting foundation models for rare eye disease diagnosis via a multimodal text-to-image generative framework.pdf`（npj Digital Medicine, 2026）

### VQAScore — **正しい**（Results p.、Table 2 *Average）

| タスク | 値 |
|--------|-----|
| OCT-based disease detection | **0.822** |
| CFP-based multi-category eye disease diagnosis | **0.776** |
| Multimodal imaging-based rare disease diagnosis | **0.670** |

### Turing test — **62% / 66% は正しいが意味に注意**（Table 3 Total）

- 実験：**100枚**（実50＋生成50）、専門医2名、盲検
- **62.00% / 66.00%** ＝ 生成50枚のうち「実画像と誤認」した割合（Grader 1: 31/50、Grader 2: 33/50）
- 本文にも「62.00% to 66.67% of **generated** images were mistaken for real」と記載
- **混同しやすい別数値**（図には載せない）：全体正答率 50.00% / 54.50%；実画像の識別率 62% / 76%；生成画像の識別率 38% / 33.33%

### Visual quality score — **正しい**（Results、Methods）

| 項目 | 値 |
|------|-----|
| 対象 | 生成画像 **50枚**（ランダム抽出） |
| Grader 1 | **1.940 ± 1.085** |
| Grader 2 | **2.080 ± 1.055** |
| Kappa | **0.870** |
| 5段階 | 1＝プロンプトの要素を十分再現、5＝要素をほとんど含まない（Results の定義） |

## 旧ファイル

[slide13.md](slide13.md) は VQAScore＋Turing を1枚にまとめた旧版。3分割生成では上記3ファイルを使用する。

## 図中ラベル

3つのプロンプトは **日本語メイン**（聴衆向け）。英語は略語・サブ行のみ。数値は論文どおり変更しない。

## 口頭スクリプト

[../script/slide13.md](../script/slide13.md)
