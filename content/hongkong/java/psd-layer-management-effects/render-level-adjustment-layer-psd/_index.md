---
title: PSD 檔案中的渲染等級調整圖層 - Java
linktitle: PSD 檔案中的渲染等級調整圖層 - Java
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 輕鬆增強影像對比度和活力。透過此逐步指南掌握等級調整圖層。
type: docs
weight: 17
url: /zh-hant/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---
## 介紹

您是否曾經打開過 PSD 檔案卻發現影像缺乏對比或活力？不要害怕，圖像編輯勇士們！ Aspose.PSD for Java 以其強大的等級調整圖層操作功能來解決這個問題。本指南將為您提供使用色階輕鬆微調影像的知識。 

## 先決條件

- Java 開發工具包 (JDK)：確保您的系統上安裝了最新版本的 JDK。您可以從 Oracle 網站下載它（[https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)）。
- Aspose.PSD for Java 函式庫：從下載頁面下載 Aspose.PSD for Java 函式庫（[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)）。您需要有效的許可證才能使用全部功能，但可以免費試用以幫助您入門（[https://releases.aspose.com/](https://releases.aspose.com/)）。

## 導入包

在深入研究程式碼之前，我們需要匯入必要的 Aspose.PSD 類別以與 PSD 檔案互動。這是您需要的：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

這`com.aspose.psd`包提供對 PSD 操作功能的訪問，同時`com.aspose.psd.imaging.PngOptions`允許我們在將圖像儲存為 PNG 時定義選項。

現在，讓我們開始我們的等級調整冒險：

## 第 1 步：設定檔案路徑：

- 為您的文檔目錄定義變數（`dataDir`), 來源 PSD 檔案名稱 (`sourceFileName`),修改後的目標PSD檔名(`psdPathAfterChange`），以及最終的PNG導出路徑（`pngExportPath`）。考慮使用描述性名稱來提高程式碼的可讀性。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## 第 2 步：載入 PSD 映像：

- 使用`Image.load`方法開啟來源 PSD 檔案並將其儲存在`PsdImage`目的 （`im`）。 Aspose.PSD 自動偵測檔案格式。

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## 第 3 步：迭代各層：

- 我們需要在 PSD 中找到等級調整圖層。 Aspose 提供了一種使用循環迭代所有層的便利方法。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ...（將在此處新增檢查 Levels Layer 的程式碼）
}
```

## 第 4 步：識別層級層：

- 在循環內，檢查目前層（`im.getLayers()[i]` ）是一個實例`LevelsLayer`類別使用`instanceof`操作員。 
- 如果是，則將圖層投射到`LevelsLayer`進一步操作的對象。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ...（此處將新增調整等級的程式碼）
   }
}
```
## 步驟 5：微調等級（續）：

- 使用調整輸出電平`setOutputShadowLevel`和`setOutputHighlightLevel`控制生成影像的暗度和亮度。這些值決定將映射到輸出範圍的輸入等級的範圍。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   //調整輸入電平（0-255）：
	   channel.setInputShadowLevel((short) 10); //稍微加深陰影
	   channel.setInputMidtoneLevel(2.0f);     //增加中間色調
	   channel.setInputHighlightLevel((short) 230); //減少亮點

	   //調整輸出電平（0-255）：
	   channel.setOutputShadowLevel((short) 20); //進一步加深陰影
	   channel.setOutputHighlightLevel((short) 200); //提亮亮點
   }
}
```

## 第6步：儲存修改後的PSD：

- 使用`save`的方法`PsdImage`物件將修改後的影像儲存到指定路徑（`psdPathAfterChange`）。

```java
im.save(psdPathAfterChange);
```

## 第 7 步：匯出為 PNG（可選）：

- 如果您需要調整映像的 PNG 版本，請建立一個`PngOptions`物件並將顏色類型設為`TruecolorWithAlpha`。然後，使用`save`再次使用 PNG 匯出路徑和選項。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

現在你就擁有了！您已使用 Aspose.PSD for Java 成功調整了 PSD 檔案中的色階調整圖層。透過了解這些步驟並嘗試不同的值，您可以增強影像的對比度和整體外觀。

## 結論

Aspose.PSD for Java 可讓您控制影像編輯過程。透過掌握等級調整圖層，您可以為您的照片和設計注入新的活力。請記住，熟能生巧，因此請毫不猶豫地嘗試並探索這個強大工具的全部潛力。
 
## 常見問題解答

### 我可以單獨調整各個色彩通道 (RGB) 嗎？ 
是的，您可以使用以下命令存取每個顏色通道`getChannel`的方法`LevelsLayer`獨立反對並修改其等級。

### 如何處理 PSD 中的多個層級調整圖層？
程式碼會迭代所有圖層，因此它將自動處理影像中找到的任何其他層級圖層。

### 除了色階之外，還有其他方法可以調整影像對比嗎？
絕對地！ Aspose.PSD 提供各種影像調整工具，如曲線、亮度/對比度等。

### 我可以對多個圖像自動執行此過程嗎？ 
是的，您可以將此程式碼合併到循環或批次腳本中，以有效地處理多個 PSD 檔案。

### 我可以在哪裡找到更多資訊和支援？
Aspose 提供了廣泛的文件（[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)）和支援論壇（[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) 對於您可能遇到的任何疑問或問題。