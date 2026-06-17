---
date: 2026-04-22
description: 學習如何使用 Aspose.PSD for Java 更改描邊顏色。請跟隨此一步一步的指南，修改描邊圖層的顏色、不透明度等。
keywords:
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
- add stroke layer psd
linktitle: 新增描邊圖層顏色
second_title: Aspose.PSD Java API
title: 如何在 Java 中使用 Aspose.PSD 更改描邊顏色
url: /zh-hant/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD 在 Java 中更改筆畫顏色

## 介紹

如果您需要在 Photoshop 文件中以程式方式 **change stroke color java**，Aspose.PSD for Java 讓此操作變得簡單。在本教學中，我們將逐步示範如何新增筆畫圖層、變更其顏色、調整不透明度，並儲存結果。最後您還會看到如何修改任何既有圖層的筆畫，讓您能從 Java 程式碼中完整掌控創意。

## 快速回答
- **需要哪個函式庫？** Aspose.PSD for Java (latest version)。  
- **我可以更改筆畫顏色嗎？** 可以 – 使用 `ColorFillSettings` 設定任意 `Color`。  
- **我需要授權嗎？** 臨時授權可用於評估；正式授權則需於正式環境使用。  
- **支援哪個 Java 版本？** Java 8 或更高版本。  
- **實作需要多長時間？** 基本筆畫變更通常在 10 分鐘內完成。

## 什麼是 PSD 中的筆畫圖層？

筆畫圖層是一種向量效果，會在圖層內容周圍繪製輪廓。它可以自訂顏色、粗細、不透明度與混合模式。以程式方式修改此效果，可實現自動化品牌化、批次處理或動態圖形產生。

## 為什麼使用 Aspose.PSD 更改筆畫顏色？

- **無需 Photoshop** – 完全在 Java 中操作。  
- **完整 PSD 規格相容** – 支援所有現代 PSD 功能。  
- **高效能** – 快速處理大型檔案。  
- **跨平台** – 只要有 JVM，即可在任何作業系統執行。

## 如何在 Java 中以程式方式更改筆畫顏色

以下是一個簡潔的逐步說明，示範如何使用 Aspose.PSD for Java 變更筆畫顏色。每一步都包含簡短說明，並附上原始程式碼區塊（保持不變）。

### 前置條件

- **Aspose.PSD 函式庫** – 從 [official documentation](https://reference.aspose.com/psd/java/) 下載。  
- **Java Development Kit (JDK)** – 版本 8 或更新。  
- **IDE** – Eclipse、IntelliJ IDEA，或任何支援 Java 的編輯器。

### 匯入套件

首先匯入所需的類別，讓專案能使用 PSD 處理與筆畫效果 API。

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

建立新的 Java 專案，將 Aspose.PSD JAR 加入建置路徑，並確認函式庫能正確載入且不產生錯誤。

### 步驟 2：載入 PSD 檔案

啟用載入效果資源，以確保筆畫資訊可用。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### 步驟 3：存取筆畫效果圖層

從第二層（索引 1）取得第一個筆畫效果。

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### 步驟 4：驗證筆畫屬性

在進行變更前先確認現有屬性，以避免意外結果。

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### 步驟 5：設定顏色與不透明度（如何更改筆畫顏色）

此處我們 **change stroke color** 為黃色，並將不透明度降低至 50 %（127 / 255）。

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### 步驟 6：儲存已修改的 PSD

將更新後的影像寫回磁碟。新檔案現在包含已修改的筆畫。

```java
im.save(exportPath);
```

## 如何修改筆畫不透明度

如果只想調整不透明度而保留原始顏色，只需變更 `setOpacity` 的值（0‑255）。例如 `colorStroke.setOpacity((byte)200);` 會使筆畫大約 78 % 不透明。

## 如何套用筆畫效果

若圖層尚未有筆畫效果，可建立 `StrokeEffect` 實例，設定其 `ColorFillSettings`，再將其附加至圖層的 `BlendingOptions`。`setColor` 與 `setOpacity` 方法同樣用於定義外觀。

## PSD 筆畫教學：向 PSD 添加筆畫圖層

上述步驟示範了向既有圖層添加筆畫。若要建立全新筆畫圖層，可先複製目標圖層，然後套用 `StrokeEffect`。此方式適合在不改動原始圖層的情況下加入筆畫。

## 更改筆畫顏色的常見使用情境

- **品牌自動化：** 在單一次批次執行中，將企業色套用至數百個 PSD 資產的商標。  
- **動態 UI 產生：** 依使用者在網頁設計工具中選擇的主題即時變更筆畫顏色。  
- **前置檢查：** 在送印前確保所有筆畫顏色符合印刷規格。

## 常見陷阱與技巧

- **Null checks** – 在轉型前務必確認 `getEffects()` 回傳的陣列非 null。  
- **Layer index** – PSD 圖層採零基索引，請確保目標圖層索引正確。  
- **Color format** – `Color.getYellow()` 只是範例，您可使用 `new Color(r, g, b)` 建立自訂顏色。  
- **Opacity range** – 不透明度為 byte（0–255），超過 255 的值會被截斷。  
- **Resource loading** – 若遺漏 `loadOptions.setLoadEffectsResource(true)`，將導致 `null` 的 effects 陣列。

## 常見問答

**Q: 我可以將 Aspose.PSD 與其他 Java 圖形函式庫一起使用嗎？**  
A: 可以，Aspose.PSD 可與 Apache Commons Imaging 或 Java2D 等函式庫結合，以擴充功能。

**Q: Aspose.PSD 是否相容於最新的 PSD 檔案格式？**  
A: 絕對相容。此函式庫會定期更新，以支援最新的 Photoshop 規格。

**Q: 使用 Aspose.PSD 時，我該如何處理例外情況？**  
A: 請參考 [support forum](https://forum.aspose.com/c/psd/34) 以取得詳細的除錯說明與範例錯誤處理程式碼。

**Q: 我可以在購買前試用 Aspose.PSD 嗎？**  
A: 當然可以！取得 [free trial](https://releases.aspose.com/) 以探索全部功能。

**Q: 我可以從哪裡取得 Aspose.PSD 的臨時授權？**  
A: 取得 [temporary license](https://purchase.aspose.com/temporary-license/) 以在開發環境中評估此函式庫。

**最後更新：** 2026-04-22  
**測試環境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}