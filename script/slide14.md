# Slide 14：結果 — 下流分類（Table 4・データセット全体）（約1分10秒）

## スライド文案（最新 pptx 準拠）

**タイトル**  
結果：下流分類タスク　全データセットの総合比較

**メイン図**  
`assets/table4_extract.png`（論文 Table 4 抜粋・4データセット × 3条件）

**スライド下段（✓）— xxx の置き換え案**

**推奨（1行・スライドにそのまま貼れる）**  
✓ データセット全体の性能で、EyeDiff はベースラインを上回り、抜粋4例ではいずれも有意（\*P<0.05）

**短縮版（余白が狭いとき）**  
✓ EyeDiff はベースラインより有意に改善（一般・希少コホートを含む4データセット抜粋）

**やや詳しめ**  
✓ 11データセット横断で EyeDiff がベースラインを有意に上回る傾向（本表は Table 4 の4例抜粋）

**口頭のみ（表・スライドには載せない）**  
- 同条件の実験を **EyeFound**・**EyeCLIP** でも実施。数値は本文 PDF にはなく **Supplementary Tables 1–2**（別サプリ PDF）  
- JSIEC、Retina、OCTID、OCTDL など残り7データセットでも同傾向が多い  
- 例外：**PAPILA** は AUROC で Oversampling が EyeDiff より高い  
- 個別の少数クラス・希少疾患サブタイプ → **Slide 15**（Table 5・6）

---

## メタ情報

| 項目 | 値 |
|------|-----|
| 文字数 | 約380字 |
| 想定時間（300字/分） | 1.27分（76秒） |
| 想定時間（320字/分） | 1.19分（71秒） |

## スクリプト

次は下流分類タスクです。そのスライドは全データセットの総合比較抜粋で、RETFound をベースラインに、実画像のみ、Oversampling、EyeDiff の3条件を、11データセットのうち代表的な4つで示しています。
同じ設計で EyeFound と EyeCLIP でも実験していますが、本文の表には載っておらず、別 PDF の Supplementary Tablesにあるため、本スライドでは RETFound だけに絞ります。
4例は一般疾患の IDRiD と Glaucoma Fundus に加え、希少疾患コホートの ImageBank、外部検証の OphthalWeChat (オフサルウィーチャット)です。
いずれも EyeDiff の行で AUROC と AUPR がベースラインより有意に上がっており、Oversampling より EyeDiff が高い例も多くなっています。
載せきれてない その他のデータセット でも、EyeDiff がベースラインを上回る傾向が多いと論文内に言及がありました。
以上より、データセット全体の性能で、EyeDiff はベースラインを上回り、いずれも有意（*P<0.05）であった言えます。

**話し方のメモ**：具体的な数値は口頭では言わず、指し示し＋「上がった」「有意」で進める。聞き手が表を見れば足りる。

## メモ

### Table 4 抜粋（`assets/table4_extract.png`・PDF照合済み）

P値はすべて **vs ベースライン RETFound**。*P<0.05。↑＝EyeDiff による改善。

| Dataset | EyeDiff（抜粋） | P value |
|---------|-------------------|---------|
| IDRiD | 0.837 / 0.518 | 0.008* |
| Glaucoma Fundus | 0.959 / 0.893 | 0.008* |
| ImageBank | 0.919 / 0.530 | <0.001* |
| OphthalWeChat | 0.663 / 0.439 | <0.001* |

### 基盤モデル3種（論文 Methods）

| モデル | 本文 Table 4 | サプリ |
|--------|-------------|--------|
| RETFound | ✅ 本スライド | — |
| EyeFound | ❌ | Supplementary Table 1 |
| EyeCLIP | ❌ | Supplementary Table 2 |

- 図：`assets/table4_extract.png`
- プロンプト：`text_to_image_prompt/slide14.md`
