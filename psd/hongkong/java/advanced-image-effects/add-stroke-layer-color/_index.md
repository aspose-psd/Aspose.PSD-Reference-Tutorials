---
date: 2026-10-24
description: 了解如何使用 Aspose.PSD for Java 在 Java 中建立描邊圖層。此一步一步指南將示範如何新增描邊圖層、變更其顏色、調整不透明度，並儲存
  PSD。
keywords:
- create stroke layer java
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
lastmod: 2026-10-24
linktitle: 新增描邊圖層顏色
og_description: 使用 Aspose.PSD for Java 建立 Java 描邊圖層。遵循此簡明教學以新增描邊圖層、變更顏色、調整不透明度，並匯出
  PSD 檔案。
og_image_alt: Screenshot of a Java IDE showing Aspose.PSD code that creates and modifies
  a stroke layer in a PSD file
og_title: 使用 Aspose.PSD 建立 Java 描邊圖層 – 快速指南
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  headline: How to create stroke layer Java using Aspose.PSD
  type: TechArticle
- description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  name: How to create stroke layer Java using Aspose.PSD
  steps:
  - name: set up your project
    text: Create a new Java project, add the Aspose.PSD JAR to the build path, and
      verify the library loads without errors.
  - name: load the PSD file
    text: Enable loading of effect resources so the stroke information is available.
  - name: access the stroke effect layer
    text: '`StrokeEffect` is Aspose.PSD’s class that represents a vector outline applied
      to a layer. Retrieve the first stroke effect from the second layer (index 1).'
  - name: validate stroke properties
    text: '`ColorFillSettings` holds the color and opacity values for a stroke. Confirm
      the existing properties before making changes to avoid unexpected results.'
  - name: set color and opacity (how to change stroke color)
    text: Here we **change stroke color** to yellow and reduce opacity to 50 % (127
      / 255). `ColorFillSettings` also lets you specify blend mode and size.
  - name: save the modified PSD
    text: Write the updated image back to disk. The new file now contains the modified
      stroke.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD can be combined with libraries such as Apache Commons
      Imaging or Java2D for extended functionality.
    question: Can I use Aspose.PSD with other Java graphic libraries?
  - answer: Absolutely. The library supports the newest Photoshop specifications and
      over 150 PSD features.
    question: Is Aspose.PSD compatible with the latest PSD file format?
  - answer: Wrap your code in try‑catch blocks and consult the [support forum](https://forum.aspose.com/c/psd/34)
      for detailed troubleshooting examples.
    question: How do I handle exceptions while using Aspose.PSD?
  - answer: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore
      all features.
    question: Can I try Aspose.PSD before purchasing?
  - answer: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      to evaluate the library in your development environment.
    question: Where can I get a temporary license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create stroke layer
- Aspose.PSD
- Java image processing
title: 如何使用 Aspose.PSD 在 Java 中建立描邊圖層
url: /zh-hant/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD 在 Java 中建立描邊圖層

## 介紹

如果您需要以程式方式在 Photoshop 文件中 **create stroke layer Java**（建立 Java 描邊圖層），Aspose.PSD for Java 為您提供乾淨、以程式碼為先的方式。在本教學中，您將學習如何新增描邊圖層、變更其顏色、調整不透明度，並儲存結果——全部不需啟動 Photoshop。最後，您還會知道如何編輯現有圖層的描邊，讓您直接從 Java 應用程式中完整掌控創作。

## 快速回答
- **需要哪個函式庫？** Aspose.PSD for Java (latest version).  
- **我可以變更描邊顏色嗎？** Yes – use `ColorFillSettings` to set any `Color`.  
- **我需要授權嗎？** A temporary license works for evaluation; a full license is required for production.  
- **支援哪個 Java 版本？** Java 8 or higher.  
- **實作需要多長時間？** Typically under 10 minutes for a basic stroke change.

## 什麼是 PSD 中的描邊圖層？

描邊圖層是一種向量效果，會在圖層內容周圍繪製輪廓。它可以自訂顏色、粗細、不透明度與混合模式。以程式方式修改此效果可實現自動化品牌化、批次處理或動態圖形產生。

## 為何使用 Aspose.PSD 變更描邊顏色？

Aspose.PSD 支援 **150+** PSD 功能——包括向量遮色片、智慧物件與圖層效果——同時在不將整個文件載入記憶體的情況下處理數百頁檔案。此函式庫可在任何具 JVM 的作業系統上執行，為一般資產提供次秒級效能，且不需安裝 Photoshop。

## 如何在 Java 中建立描邊圖層？

載入 PSD、加入描邊效果、設定外觀，然後儲存檔案——只需幾行簡單程式碼。以下答案會先說明該做什麼，之後再深入逐步說明。

**直接答案（40‑70 個字）：**  
`PsdImage` 代表一個 PSD 文件，提供載入與儲存檔案的方法。首先使用 `PsdImage.load("input.psd", loadOptions)` 載入 PSD。建立新的 `StrokeEffect`，將其 `ColorFillSettings` 設為所需的 `Color`，調整不透明度與大小，然後將效果附加到目標圖層的 `BlendingOptions`。最後，呼叫 `psd.save("output.psd", SaveFormat.PSD)`。此流程即在 Java 中使用 Aspose.PSD 建立描邊圖層。

### 前置條件

- **Aspose.PSD library** – 從 [official documentation](https://reference.aspose.com/psd/java/) 下載。  
- **Java Development Kit (JDK)** – 版本 8 或更新。  
- **IDE** – Eclipse、IntelliJ IDEA，或任何相容 Java 的編輯器。

### 匯入套件

首先，匯入您需要的類別。這會讓您的專案取得 PSD 處理與描邊效果的 API。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

### 步驟 1：設定專案

建立新的 Java 專案，將 Aspose.PSD JAR 加入建置路徑，並確認函式庫能順利載入且不產生錯誤。

### 步驟 2：載入 PSD 檔案

啟用載入效果資源，以便取得描邊資訊。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### 步驟 3：存取描邊效果圖層

`StrokeEffect` 是 Aspose.PSD 用來表示套用於圖層的向量輪廓的類別。從第二個圖層（索引 1）取得第一個描邊效果。

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### 步驟 4：驗證描邊屬性

`ColorFillSettings` 保存描邊的顏色與不透明度值。於變更前先確認現有屬性，以避免意外結果。

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### 步驟 5：設定顏色與不透明度（如何變更描邊顏色）

此處我們將 **change stroke color** 變更為黃色，並將不透明度降低至 50 %（127 / 255）。`ColorFillSettings` 亦可讓您指定混合模式與大小。

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### 步驟 6：儲存已修改的 PSD

將更新後的影像寫回磁碟。新檔案現在包含已修改的描邊。

```java
im.save(exportPath);
```

## 如何在 Java 中變更描邊顏色？

`Color` 代表 ARGB 顏色值。載入您的 PSD，定位目標圖層，使用新的 `Color` 更新 `ColorFillSettings`，然後儲存檔案。此操作僅需幾行程式碼，對一般資產而言在一秒內完成，快速且高效。

**直接答案（40‑70 個字）：**  
使用 `layer.getEffects().getStrokeEffect()` 取得現有的描邊，呼叫 `stroke.getColorFillSettings().setColor(Color.getRed())`（或任何您需要的 `Color`），可選擇性地調整 `setOpacity((byte)200)` 以設定 78 % 不透明度，最後以 `psd.save("output.psd", SaveFormat.PSD)` 儲存 PSD。變更會即時套用，無需重新渲染整個文件。

## 如何修改描邊不透明度？

如果只需在保留原始顏色的情況下調整不透明度，請在 `ColorFillSettings` 上變更 `setOpacity` 值（0‑255）。例如，`colorStroke.setOpacity((byte)200);` 會使描邊大約 78 % 不透明。調整不透明度可讓您根據設計需求打造細緻的輪廓或完全實心的描邊。

**直接答案（40‑70 個字）：**  
從目標圖層取得 `StrokeEffect`，然後呼叫 `stroke.getColorFillSettings().setOpacity((byte)desiredValue)`，其中 `desiredValue` 的範圍為 0（透明）至 255（完全不透明）。儲存 PSD 後，新不透明度會立即生效。此方法適用於任何現有的描邊，無論其原始顏色為何。

## 如何套用描邊效果？

若圖層尚未有描邊效果，請建立 `StrokeEffect` 實例，設定其 `ColorFillSettings`，並附加至圖層的 `BlendingOptions`。同樣的 `setColor` 與 `setOpacity` 方法用於整體外觀的定義。

**直接答案（40‑70 個字）：**  
實例化 `StrokeEffect newStroke = new StrokeEffect(); newStroke.getColorFillSettings().setColor(Color.getBlue()); newStroke.getColorFillSettings().setOpacity((byte)255); layer.getBlendingOptions().setEffect(newStroke);`。附加效果後，儲存 PSD。這會在文件中任何現有圖層上新增一個全新、可完全自訂的描邊圖層。

## 變更描邊顏色的常見使用情境

- **Branding automation:** 在單次批次執行中，將企業色彩套用至數百個 PSD 資產的商標。  
- **Dynamic UI generation:** 在基於網頁的設計工具中，根據使用者選擇的主題即時變更描邊顏色。  
- **Pre‑flight preparation:** 在將檔案送至印刷前，確保所有描邊顏色符合印刷規格。

## 常見陷阱與技巧

- **Null checks** – 在轉型前務必確認 `getEffects()` 回傳非 null 陣列。  
- **Layer index** – PSD 圖層採零基索引；確保目標圖層正確。  
- **Color format** – `Color.getYellow()` 只是範例；您可使用 `new Color(r, g, b)` 建立自訂顏色。  
- **Opacity range** – 不透明度為 byte（0–255），超過 255 的值會被限制。  
- **Resource loading** – 若遺忘 `loadOptions.setLoadEffectsResource(true)`，將導致 `null` 的 effects 陣列。

## 常見問答

**Q: 我可以將 Aspose.PSD 與其他 Java 圖形函式庫一起使用嗎？**  
A: 可以，Aspose.PSD 可與 Apache Commons Imaging 或 Java2D 等函式庫結合，以擴充功能。

**Q: Aspose.PSD 是否相容最新的 PSD 檔案格式？**  
A: 絕對相容。此函式庫支援最新的 Photoshop 規範以及超過 150 項 PSD 功能。

**Q: 使用 Aspose.PSD 時如何處理例外情況？**  
A: 將程式碼包在 try‑catch 區塊中，並參考 [support forum](https://forum.aspose.com/c/psd/34) 取得詳細除錯範例。

**Q: 我可以在購買前試用 Aspose.PSD 嗎？**  
A: 當然可以！取得 [free trial](https://releases.aspose.com/) 以探索所有功能。

**Q: 我可以從哪裡取得 Aspose.PSD 的暫時授權？**  
A: 取得 [temporary license](https://purchase.aspose.com/temporary-license/) 以在開發環境中評估此函式庫。

---

**最後更新:** 2026-10-24  
**測試環境:** Aspose.PSD 24.11 for Java  
**作者:** Aspose

## 相關教學

- [如何使用 Aspose.PSD 在 Java 中變更描邊顏色](/psd/java/advanced-image-effects/add-stroke-layer-color/)
- [如何在 Java 中為 PSD 加入陰影 – 進階圖層效果](/psd/java/advanced-psd-layer-features-effects/)
- [圖案覆蓋 PSD：使用 Aspose.PSD for Java 加入效果](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}