# RSNA_2024
画像コンペ  
https://www.guruguru.science/competitions/17/
2022の1stコード
https://www.kaggle.com/code/haqishen/rsna-2022-1st-place-solution-train-stage1/notebook

# Codeまとめ(Vote 50over)
### (https://www.kaggle.com/code/satyaprakashshukl/rsna-lumbar-spine-analysis)
モデルアーキテクチャ: ResNet、EfficientNet、DenseNetなどの事前学習済みCNNを使用し、カスタム層を追加。多出力モデルを作成し、各椎間板レベル（L1/L2～L5/S1）の重症度を予測。  
最終的に、ランダムフォレストで予測している???  
https://www.kaggle.com/code/adityakishor1/radiological-society-of-north-america-rsna-lumba/notebookはこのコードのパクリ


### https://www.kaggle.com/code/allegich/lumbar-rsna-2024-visualizing-eda-sub  
 Axial and Sagittal やT1,T2の意味が分かりやすい。  基本的なRDAをしているため、わかりやすい. 
 最終的にCXGBoostで予測.入力データに画像を使用してはいない...?  

 ### https://www.kaggle.com/code/shubhamcodez/rsna-efficientnet-starter-notebook　　
EfficientNetV2の事前学習済みモデルをベースにしたカスタムモデルを作成、'Sagittal T1'、'Axial T2'、'Sagittal T2/STIR':のそれぞれに対して、モデルを作成。   
これを理解するのが今回このコンペに参加した意義になりそう  

### https://www.kaggle.com/code/itsuki9180/rsna2024-lsdc-making-dataset  (これがかなり引用数高く、パブリックスコアが高いものもこれ or この派生形を参考にしている)
https://www.kaggle.com/code/itsuki9180/rsna2024-lsdc-training-baseline  
https://www.kaggle.com/code/itsuki9180/rsna2024-lsdc-submission-baseline
の三部作。  
1. 前処理: Axial T2, Sagittal T2/STIR, Sagittal T1ごとに異なる処理を実施し、PNGファイルに変更:(T2はそのままPngファイル化、それ以外は中央部分のみ抽出している?)
2. 訓練編:
https://www.kaggle.com/code/haqishen/1st-place-soluiton-code-small-ver を引用している
3. ....
   結構難しそう,,,,,

 #### 派生形
 #### https://www.kaggle.com/code/hugowjd/rsna2024-lsdc-densenet-submission　　
https://www.kaggle.com/code/hugowjd/rsna2024-lsdc-training-densenet
EfficientNet_B4からDenseNet201に変更して実施。



### https://www.kaggle.com/code/vaillant/cross-reference-images-in-different-mri-planes
異なる種類の写真の関係をわかりやすく説明.  

### https://www.kaggle.com/code/dschettler8845/rsna-lsdc-let-s-learn-together-eda/notebook   
長い....

### https://www.kaggle.com/code/docxian/rsna-2024-lumbar-spine-explore-training-data  
ほかのと同様のEDA　　


### https://www.kaggle.com/code/junkoda/optimize-the-evaluation-metric  　
メトリックの方法



### https://www.kaggle.com/code/hengck23/2d-to-3d-projection-for-dicom/notebook
2dデータから3dデータに変える方法

### https://www.kaggle.com/code/brendanartley/lumbar-coordinate-dataset-code/notebook 
RESNET18を使用して、座標を推定  


### https://www.kaggle.com/competitions/rsna-2024-lumbar-spine-degenerative-classification/discussion/512080  
欠損しているデータの理由(この作者的には、がぞうから判断がつかなかった場合とのこと)


### https://www.kaggle.com/code/anoukstein/2d-segmentation-of-sagittal-lumbar-spine-mri  
Unetを使用した予測(attension maskの表示もあるため、現況になりそう)  
ただし、座標データは使用していない?

### https://www.kaggle.com/code/guilhermelevi/rsna-lsdc-disc-detection-baseline-faster-r-cnn
Faster CNnを使用した脊椎部分の特定(物体検出) 予測まではおこなっていない


### https://www.kaggle.com/code/sacuscreed/foraminal-unet-vit-train  （要確認）
これは物体検出から、予測まで行っていそう..!?


### https://www.kaggle.com/code/samu2505/rsna2024-training2-5dmodel#Model
2,5次元モデル(2022年の優勝コードも2,5次元モデルを使用)

### https://www.kaggle.com/code/claverru/automatic-spine-cord-segmentation-sam-2 
SAM2というのを使用して、脊椎のせぐめんてーしょんしている


# EDAまとめ
### https://www.kaggle.com/code/adityakishor1/analysis-of-lumbar-spine-data-insights-from-rsna　
初期に出されたEDA、もう既知の内容か

### https://www.kaggle.com/code/utm529fg/rsna-initial-eda  
日本語で書かれたEDA
 

