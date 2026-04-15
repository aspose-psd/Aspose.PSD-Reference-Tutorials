---
date: 2026-03-26
description: 學習如何使用 Aspose.PSD for Java 編輯 PSD 檔案中的文字圖層及變更文字顏色。為開發者與設計師提供的逐步指南。
linktitle: Edit Text Layers PSD Files using Java
second_title: Aspose.PSD Java API
title: 使用 Java 編輯 PSD 檔案文字圖層 – Aspose.PSD 教學
url: /zh-hant/java/psd-image-modification-conversion/format-text-portions-psd-files/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 編輯 PSD 文本圖層檔案

## 介紹

在這個日益視覺化的世界中，能夠以程式方式 **edit text layers PSD** 檔案可以為您節省大量手動操作的時間。無論您是需要批次更新圖形的設計師，或是打造動態影像產生服務的開發者，Aspose.PSD for Java 都能讓您像在 Photoshop 中一樣修改 PSD 文字，只是透過程式碼。本教學將完整說明編輯 PSD 文本圖層的流程，並示範如何 **change text color PSD** 單獨的文字段落。

## 快速解答
- **哪個函式庫可以編輯 text layers PSD？** Aspose.PSD for Java  
- **可以程式化變更 text color PSD 嗎？** 可以，使用 `ITextStyle.setFillColor`  
- **正式環境需要授權嗎？** 需要商業授權；提供免費試用版。  
- **支援哪個 Java 版本？** Java 8 及以上。  
- **是否需要記憶體管理？** 需要——在儲存後釋放 `PsdImage`。

## 什麼是編輯 PSD 文本圖層？

編輯 PSD 文本圖層是指存取 Photoshop PSD 檔案內的文字資料，修改字元、樣式或格式，然後將變更寫回檔案。此功能對於自動化品牌更新、製作在地化圖形，或產生個人化行銷素材而不需手動操作 Photoshop 極為重要。

## 為什麼使用 Aspose.PSD 編輯 PSD 文本圖層？

- **完整控制** – 變更字型、顏色、對齊，甚至新增或移除文字段落。  
- **跨平台** – 可在任何支援 Java 的作業系統上執行。  
- **不需 Photoshop** – 可在伺服器或 CI 流程中執行批次作業。  
- **高保真度** – 保留圖層效果、遮色片及其他 PSD 功能。

## 前置條件

在開始撰寫程式碼之前，請確保您已具備以下環境：

1. **Java Development Kit (JDK)** – 已安裝並設定 Java 8 以上。  
2. **Aspose.PSD for Java Library** – 從 [here](https://releases.aspose.com/psd/java/) 下載，或使用 [free trial](https://releases.aspose.com/)。  
3. **IDE for Java Development** – IntelliJ IDEA、Eclipse 或 NetBeans，並將 Aspose.PSD JAR 加入專案的 classpath。  
4. **Basic Knowledge of Java** – 了解物件、迴圈與例外處理。

## 匯入必要的套件

使用 Aspose.PSD for Java 時，需要匯入特定套件以存取所需的類別與方法。以下為範例：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.fileformats.psd.layers.text.ITextPortion;
import com.aspose.psd.fileformats.psd.layers.text.ITextStyle;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.internal.Exceptions.Exception;
```

上述匯入讓我們能使用本教學中所需的 Aspose.PSD 基本功能。

## 步驟 1：定義目錄

在處理 PSD 檔案前，需要先定義來源 PSD 檔案的位置以及修改後檔案的儲存路徑。

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "ThreeColorsParagraphs.psd";
String outPsdFilePath = outputDir + "ThreeColorsParagraph_out.psd";
```

請將佔位路徑替換為您機器上的實際路徑。

## 步驟 2：載入 PSD 檔案

接下來載入要處理的 PSD 檔案。Aspose 讓這個動作非常簡單。

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

`Image.load` 會開啟檔案，讓我們可以開始檢查其圖層。

## 步驟 3：遍歷圖層

檔案載入後，我們需要深入圖層。不是所有圖層都包含文字，我們只想找出文字圖層。以下篩選方式：

```java
for (Layer layer : psdImage.getLayers()) {
    if (!(layer instanceof TextLayer)) {
        continue;
    }
    // Process only text layers…
}
```

此迴圈會遍歷每個圖層，並跳過非 `TextLayer` 的實例。

## 步驟 4：存取文字段落

辨識出文字圖層後，即可取得其文字段落進行編輯。魔法就從這裡開始！

```java
TextLayer textLayer = (TextLayer) layer;
ITextPortion[] portions = textLayer.getTextData().getItems();
```

把文字段落想像成可以獨立編輯的單字或句子。

## 步驟 5：修改文字段落

現在開始編輯文字。我們會修改既有文字、移除部分段落，甚至新增文字：

```java
portions[0].setText("Hello ");
portions[1].setText("World");
// Removing text portions
textLayer.getTextData().removePortion(3);
textLayer.getTextData().removePortion(2);
// Adding new text portion
ITextPortion createdPortion = textLayer.getTextData().producePortion();
createdPortion.setText("!!!\r");
textLayer.getTextData().addPortion(createdPortion);
```

您可以看到重新寫入或刪除段落是多麼直接。

## 步驟 6：對齊與樣式文字

修改完文字後，可能需要調整樣式。準備好改頭換面了嗎？讓我們調整文字對齊與顏色：

```java
// Set right justification
portions[0].getParagraph().setJustification(1); // Right
portions[1].getParagraph().setJustification(1);
portions[2].getParagraph().setJustification(1);

// Set fill colors individually
portions[0].getStyle().setFillColor(Color.getAquamarine());
portions[1].getStyle().setFillColor(Color.getViolet());
portions[2].getStyle().setFillColor(Color.getLightBlue());
```

此處我們 **change text color PSD** 為每個段落設定不同的 `fillColor`，讓每個詞彙都有自己的視覺識別。

## 步驟 7：更新圖層資料

完成所有變更後，需要將這些變更寫回圖層資料：

```java
textLayer.getTextData().updateLayerData();
```

此呼叫會將修改提交至底層 PSD 結構。

## 步驟 8：儲存已修改的 PSD 檔案

最後，將變更寫入新的 PSD 檔案：

```java
psdImage.save(outPsdFilePath, new PsdOptions(psdImage));
```

指定輸出路徑，即可產生編輯後的檔案。

## 步驟 9：釋放資源

為了降低記憶體使用，完成後務必釋放影像資源：

```java
finally {
    psdImage.dispose();
}
```

清理資源可防止記憶體泄漏，特別是在批次處理大量檔案時。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|-------|--------|-----|
| **NullPointerException on `portions[2]`** | 原始 PSD 的段落少於三個。 | 在存取索引前先以 `portions.length` 檢查段落數量。 |
| **Colors not applied** | 使用了過舊的 Aspose.PSD 版本。 | 升級至最新的 Aspose.PSD for Java 版本。 |
| **File not found** | `sourceDir` 或 `outputDir` 路徑不正確。 | 使用絕對路徑或再次確認相對路徑。 |
| **License not set** | 試用版可能會加上浮水印。 | 使用 `License license = new License(); license.setLicense("Aspose.PSD.lic");` 設定有效授權。 |

## 常見問答

### 什麼是 Aspose.PSD for Java？
Aspose.PSD for Java 是一套讓開發者以程式方式操作 Photoshop PSD 檔案的函式庫。

### 我可以免費使用 Aspose.PSD 嗎？
可以，您可以先在 Aspose 官方網站取得免費試用版，再決定是否購買。

### 我需要哪些前置條件？
您需要安裝 Java Development Kit (JDK)、下載 Aspose.PSD 函式庫，並具備基本的 Java 程式設計知識。

### 免費試用有什麼限制？
免費試用版可能在功能上有一些限制，例如會加上浮水印或使用次數受限。

### 在哪裡可以找到更多關於 Aspose.PSD 的資訊？
您可以在 [here](https://reference.aspose.com/psd/java/) 查看完整文件與 API 參考。

---

**最後更新：** 2026-03-26  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}