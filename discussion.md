
https://www.kaggle.com/competitions/rsna-2024-lumbar-spine-degenerative-classification/discussion/503433  
過去のコンペ内容

https://www.kaggle.com/competitions/rsna-2024-lumbar-spine-degenerative-classification/discussion/519628　　
けろけろっぴさんの分析まとめ(詳細はあとで見る)
派生:   


https://www.kaggle.com/competitions/rsna-2024-lumbar-spine-degenerative-classification/discussion/507101  
ドメイン知識  

### https://www.kaggle.com/competitions/rsna-2024-lumbar-spine-degenerative-classification/discussion/511055
メトリック
この分析では、コンペティションの評価メトリックがどのように誤予測をペナルティするかについて解説しています。特に、さまざまなタイプのエラーの影響を理解し、スコアを最適化する方法に焦点を当てています。

### 評価メトリックの挙動と誤予測に関する分析

#### 1. メトリックのペナルティ

評価メトリックの挙動を理解するために、以下のサンプルを用いて、正しいラベルを誤ったラベルに置き換えた場合のペナルティを分析しました：

- **正常サンプル (Normal/Mild)**
- **重度サンプル (Severe)**
- **中等度サンプル (Moderate)**

これにより、誤って予測した場合のペナルティがどのように変化するかを把握しました。特に、重度のターゲットラベルを誤った場合のペナルティが最も高いことが確認されました。また、脊髄管狭窄症に関しては、重度の予測ミスが特に厳しく評価されることが分かりました。ペナルティは線形であり、競技の重み付けとは完全に比例しているわけではありません。

#### 2. トレインヒルクライミング（座標下降法）

トレインセットを基にしてヒルクライミングを行い、スコアの変化を確認しました。以下は、いくつかの重み設定とそれに対するスコアの例です：

- 重み設定 [0.55, 0.20, 0.25] の場合、スコア: 0.910161
- 重み設定 [0.60, 0.20, 0.20] の場合、スコア: 0.915495

また、リーダーボードの結果と比較した際のスコアの変化も示されています：

- **頻度**: 1.24 → 1.21
- **重み設定 [0.33, 0.33, 0.33]**: 0.89 → 1.02
- **重み設定 [0.424223, 0.303108, 0.272669]**: 0.84 → 0.98
- **重み設定 [0.5, 0.15, 0.35] (ヒルクライミング)**: 0.97 → 1.25





### https://www.kaggle.com/competitions/rsna-2024-lumbar-spine-degenerative-classification/discussion/512048
間違っているラベルがある

