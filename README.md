# 🦪 Oystictor - Oyster Meat Weight Predictor

Oystictor 架構是本研究「基於卷積神經網路預測牡蠣肉重的研究」所提出的牡蠣肉重預測方法，整體架構分為三個階段：

1. **牡蠣特徵收集**
2. **牡蠣特徵處理**
3. **牡蠣肉重預測**
<img src="https://i.imgur.com/wJSSDa3.png" alt="Oystictor架構" width="500"/>

在「牡蠣肉重預測」階段中，本系統採用了線性迴歸（Linear Regression, LR）與卷積神經網路（Convolutional Neural Network, CNN）兩種方法進行模型訓練與預測。

---

## 📁 資料夾結構

- `01_牡蠣資料集`：含有170筆臺灣「葡萄牙牡蠣」的影像與數據。
-- `本資料集特色` : 先前並未有與臺灣的「葡萄牙牡蠣」相關之資料庫，且為了實現藉由深度學習的牡蠣肉重預測方法，與臺灣在地蚵農合作，前後共花了近一個月的時間，建立含有170筆產地為臺灣的「葡萄牙牡蠣」品種牡蠣的牡蠣資料庫，本資料庫中每一筆數據皆含有牡蠣圖像、尺寸與重量的特徵資料。
- `02_Oystictor程式系統`：模型訓練與預測程式。
-- `註`：本研究的所有內容皆透過Python 語法，於[Google Colaboratory](https://colab.research.google.com/?hl=zh-tw) 平台進行程式開發。

---

## 🧪 牡蠣特徵

本架構使用以下五項特徵進行預測：

- 牡蠣影像（處理後之400×400像素影像）
- 左殼殼長
- 殼寬
- 殼高
- 總重量（含殼）

---

## 🧠 主要技術說明

### 1. 牡蠣範圍辨識
使用 K-means 與二值化技術進行圖像分析，依據白點比例自動偵測牡蠣範圍。
<img src="https://i.imgur.com/TvftKh2.png" alt="牡蠣範圍辨識" width="800"/>

### 2. 興趣區域合成與縮小
將偵測到的牡蠣放入 1200×1200 像素白底畫布左上角，再縮小成 400×400 像素，供模型輸入使用。
<img src="https://i.imgur.com/Eo3zUCd.png" alt="興趣區域合成與縮小" width="800"/>

### 3. 異質特徵融合（Heterogeneous Feature Fusion）
將影像特徵與數值特徵（尺寸與重量）融合進入模型中，提升預測效果。
<img src="https://i.imgur.com/ZZtFYAN.png" alt="異質特徵融合" width="600"/>

---

## 🔍 模型訓練與預測

使用兩種模型進行訓練與比較：

- 線性迴歸（LR）: 本研究所用LR模型請參考「[LR模型](https://drive.google.com/drive/folders/1TOi9jT_47k6tEY0AgLZ8wwlvGu2tnCSI?usp=sharing)」。
- 卷積神經網路（CNN）: 本研究所用CNN模型請參考「[CNN模型](https://drive.google.com/drive/folders/11EdKJJ3N2LcicLlTZerIX0mFPCrQ1BBR?usp=drive_link)」。

資料分為：

- 訓練集：130 筆
- 測試集：40 筆

---

## 📎 延伸閱讀

如需完整說明與論文內容，歡迎參考：
> 📂 [Google Drive - 基於卷積神經網路預測牡蠣肉重的研究](https://drive.google.com/drive/folders/1A3849ZqeSTWrdHTVLs9eat6GbR-8BnAr?usp=sharing)

---

## 🙋 聯絡作者

THS8901  
研究：基於卷積神經網路預測牡蠣肉重的研究

---

