# PoliInfo4-FormalRun-Answer-Verification
Dataset (Formal Run): Answer Verification

## 目的
Answer Verification は、会議録の質問の要約と答弁の要約が与えられたときに、会議録中の質問に対応する答弁を参照して、答弁の要約が事実なのかフェイクなのかを判断することを目的としています。

PoliInfo-4 Question Answering-2 と相補的な関係にあり、2001 年以降の東京都議会（定例会）を対象とします。

## 方法論
Answer Verification は、Fake Generation と Answer Verification の2つのStageで構成されています。

Fake Generation では分類器を騙すような答弁の要約を作成します。
ここでは，[「AI城から財宝を奪おう!」](https://sites.google.com/view/poliinfo4/game)を通して作成されたフェイクデータセットを公開しています。

Answer Verification ではフェイクデータに騙されない分類器を作成します。
ここでは，分類器の性能を評価するためのテストデータを公開しています。

## データ形式
JSONフォーマットです。
PoliInfo-4 Question Answering-2 タスクと同一に，PredictedClass を追加しています。
Answer Verificationのテストデータでは，この項目を埋めてください。
AnswerSummaryの内容が事実と判断した場合はTrue、フェイクと判断した場合はFalseとしてください。でたらめな文字列など内容が理解できない場合もFalseとします。

## 配布ファイル

- st2_formal_test.json
  フォーマルランのテストデータセットです。

- st2_formal_Gold.json
  上記のテストデータセットの正解データです。
  
- train_fakes.json
[「AI城から財宝を奪おう!」](https://sites.google.com/view/poliinfo4/game)を通して作成されたフェイクデータセット（2023/6/28版）です。  
（注意）人手によるチェックをしていませんので、フェイクではないデータが含まれている可能性があります。
