## ファイルと内容

### train.csv
- **説明**: 訓練セットのラベルを含むファイル
- **各レコードの内容**:
  - `study_id` (文字列): 研究ID
  - 各研究には複数の画像シリーズが含まれる場合があります
  - `[condition]_[level]` (文字列): 目標ラベル。例: `spinal_canal_stenosis_l1_l2` などで、重症度は「Normal/Mild」、「Moderate」、「Severe」があります
  - 一部のエントリーには不完全なラベルがあります

### train_label_coordinates.csv
- **説明**: ラベル付けされた領域の座標を提供するファイル
- **各レコードの内容**:
  - `study_id` (文字列): 研究ID
  - `series_id` (文字列): 画像シリーズID
  - `instance_number` (整数): 3Dスタック内での画像の順序番号
  - `condition` (文字列): 中核の状態。例: 
    - `spinal_canal_stenosis`
    - `neural_foraminal_narrowing` (脊椎の各側について考慮)
    - `subarticular_stenosis` (脊椎の各側について考慮)
  - `level` (文字列): 関連する椎体。例: `l3_l4`
  - `x` (浮動小数点数): ラベル付け領域の中心のx座標
  - `y` (浮動小数点数): ラベル付け領域の中心のy座標

### sample_submission.csv
- **説明**: 提出フォーマットのテンプレートを提供するファイル
- **各レコードの内容**:
  - `row_id` (文字列): 研究ID、状態、およびレベルのスラグ。例: `12345_spinal_canal_stenosis_l3_l4`
  - `normal_mild` (浮動小数点数): 「Normal/Mild」重症度レベルの予測確率
  - `moderate` (浮動小数点数): 「Moderate」重症度レベルの予測確率
  - `severe` (浮動小数点数): 「Severe」重症度レベルの予測確率

### [train/test]_images/[study_id]/[series_id]/[instance_number].dcm
- **説明**: 画像データのディレクトリ構造
- **内容**: 各画像ファイルはDICOM形式で保存され、`train` または `test` ディレクトリ内にあります。

### [train/test]_series_descriptions.csv
- **説明**: スキャンシリーズの説明を含むファイル
- **各レコードの内容**:
  - `study_id` (文字列): 研究ID
  - `series_id` (文字列): シリーズID
  - `series_description` (文字列): スキャンの方向
