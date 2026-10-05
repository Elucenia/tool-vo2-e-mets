<!-- ELUCENIA technical documentation · vo2-e-mets · ja · no clinical/professional/rights approval -->

# 推定VO₂・METs・機能的運動能力

[条件・出典・許諾](https://elucenia.org/ja/tools/vo2-e-mets)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 運動時間（Bruce）

`tempo`

min · 範囲: 1–27

### 年齢

`idade`

年 · 範囲: 15–100

### 性別

`sexo`

- `F` — 女性
- `M` — 男性

### 身体活動をしていますか？

`ativo`

- `0` — いいえ
- `1` — はい

## 方法の版

Foster 1984 Bruce多項式、Bruce 1973年齢活動VO₂、MET=VO₂/3.5、FAI

## 記載された計算式

VO₂ (Foster, Bruce): 14.8 − 1.379 × t + 0.451 × t² − 0.012 × t³ (mL/kg/min; tは分)

METs = VO₂ ÷ 3.5

予測VO₂ (Bruce): 不活動男性 57.8 − 0.445 × 年齢; 活動男性 69.7 − 0.612 × 年齢; 不活動女性 42.3 − 0.356 × 年齢; 活動女性 42.9 − 0.312 × 年齢

機能障害 (FAI) = (予測VO₂ − 実測値) ÷ 予測VO₂ × 100

## 限界・対象集団

VO₂ 推定に使う時間は、対応する Bruce トレッドミルプロトコルの時間であり、任意の運動時間ではありません。式は予測値を示し、呼気ガス分析で測定した酸素摂取量ではありません。MET は 3.5 mL/kg/min という慣用値を用い、個人の安静時代謝を測定するものではありません。予測運動能力の基準と予後との関連は研究集団に固有です。Myers 2002 は臨床検査に紹介された男性を検討しました。小児、別のプロトコル、個人の死亡リスクへ自動的に外挿しないでください。

## 参考文献

- [Foster C et al. Generalized equations for predicting functional capacity from treadmill performance. Am Heart J, 1984.](https://doi.org/10.1016/0002-8703(84)90282-5)

- [Bruce RA, Kusumi F, Hosmer D. Maximal oxygen intake and nomographic assessment of functional aerobic impairment in cardiovascular disease. Am Heart J, 1973.](https://doi.org/10.1016/0002-8703(73)90502-4)

- [Myers J et al. Exercise capacity and mortality among men referred for exercise testing. N Engl J Med, 2002.](https://doi.org/10.1056/NEJMoa011858)

- [Foster1984](https://www.sciencedirect.com/science/article/pii/0002870384902825/pdf?md5=b82463125b785d7b4c7bb66e5b29bf38&pid=1-s2.0-0002870384902825-main.pdf)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026
