# RSNA_2024

# Codeまとめ(Vote 50over)
### (https://www.kaggle.com/code/satyaprakashshukl/rsna-lumbar-spine-analysis)
モデルアーキテクチャ: ResNet、EfficientNet、DenseNetなどの事前学習済みCNNを使用し、カスタム層を追加。多出力モデルを作成し、各椎間板レベル（L1/L2～L5/S1）の重症度を予測。  
最終的に、ランダムフォレストで予測している???  

### https://www.kaggle.com/code/allegich/lumbar-rsna-2024-visualizing-eda-sub  
 Axial and Sagittal やT1,T2の意味が分かりやすい。  基本的なRDAをしているため、わかりやすい. 
 最終的にCXGBoostで予測.入力データに画像を使用してはいない...?  

 ### https://www.kaggle.com/code/shubhamcodez/rsna-efficientnet-starter-notebook　　
EfficientNetV2の事前学習済みモデルをベースにしたカスタムモデルを作成、'Sagittal T1'、'Axial T2'、'Sagittal T2/STIR':のそれぞれに対して、モデルを作成。  

