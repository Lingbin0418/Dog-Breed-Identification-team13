# Dog-Breed-Identification-team13

## 📘 專案簡介

本專案旨在參與 Kaggle 的「Dog Breed Identification」競賽，目標是建立一個機器學習模型，能夠判斷一張狗狗圖片所屬的品種。透過深度學習模型訓練與優化，提升圖像辨識的準確度與穩定性。

## 📁 專案結構

```
├── data/ # 資料集
├── 不同訓練結果/ # 各版本訓練結果
├── 最高分程式碼完整版/ # 最佳模型完整程式碼
└── README.md # 專案說明文件
```


## 📂 Kaggle 提供的資料集（data/）

- `train`：訓練資料集  
- `test`：測試資料集
- `label.csv`：標籤檔樣式
- `sample_submission.csv`：提交格式範例

## 🧪 不同訓練結果（不同訓練結果/）

此資料夾包含多個訓練版本的結果，每個版本皆包含：

- `.ipynb`：Jupyter Notebook 格式的訓練程式碼  
- 模型輸出結果與可視化圖表  

使用者可參考不同版本的訓練策略與結果，進行比較與分析。

## 📊 訓練配置與效能分析表

| 模型           | Kaggle 分數 | validation Accuracy | validation Loss |
|---------------|----------------|----------------|------------|
|CNN            | 5.51885        | 0.08     | 4.0            |
|Xception       | 0.86652        | 0.75     | 0.9            | 
|EfficientNet-B0| 0.99080        | 0.74     | 1.0            | 
|Resnet50       | 0.75419        | 0.77     | 0.8            | 
|Resnext50      | 0.64626        | 0.83     | 0.7            | 
|Resnext101     | 0.44344        | 0.88     | 0.4            | 
|DenseNet       | 0.84058        | 0.746    | 0.9            | 

### 📂 不同模型訓練結果/ 資料夾內容

- `1.dog-breed-cnn.ipynb' 
- `2.dog-breed-xception.ipynb'
- `3.dog-breed-efficient.ipynb'
- `4.dog-breed-Resnet50.ipynb'
- `5.dog-breed-Resnext50.ipynb'
- `5.dog-breed-Resnext101.ipynb'
- `6.dog-breed-dense.ipynb'

## 🚀 使用方式

### 安裝所需套件

```bash
pip install -r requirements.txt
```
### 下載資料集連結
```bash
(https://www.kaggle.com/competitions/dog-breed-identification/data)
```
以上為本次 Kaggle 專案之完整內容說明！

## 模型架構
使用預訓練的 EfficientNet-B0 模型作為 backbone，並自訂最後的全連接層如下：

- 替換 EfficientNet 的分類頭為新的 Linear 層，輸出類別數為 120
- 輸出經過 Softmax 層計算每個類別的機率

## 執行環境
- Python 3.x  
- PyTorch  
- torchvision  
- pandas, sklearn  
- PIL  
- CUDA（Kaggle 提供 GPU）

## 備註
- 測試集預測前請移除 `.jpg` 副檔名以符合提交格式


