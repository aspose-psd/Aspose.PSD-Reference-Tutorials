---
date: 2026-02-07
description: 學習如何使用 Aspose.PSD for Java 更改 PSD 檔案中的描邊顏色。請跟隨本分步指南，修改描邊圖層的顏色、不透明度等設定。
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: 如何在 Aspose.PSD for Java 中更改描邊顏色
url: /zh-hant/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.PSD for Java 中更改描邊顏色

## 介紹

如果您需要以程式方式在 Photoshop 文件中**更改描邊顏色**，Aspose.PSD for Java 讓這變得簡單。在本教學中，我們將逐步說明如何新增描邊圖層、變更其顏色、調整不透明度，並儲存結果。最後，您還會看到如何修改任何現有圖層的描邊，讓您能從 Java 程式碼中完整掌控創意。

## 快速回答
- **需要的函式庫是什麼？** Aspose.PSD for Java（最新版本）。  
- **我可以更改描邊顏色嗎？** 可以 – 使用 `ColorFillSettings` 來設定任意 `Color`。  
- **我需要授權嗎？** 臨時授權可用於評估；正式使用則需完整授權。  
- **支援哪個 Java 版本？** Java 8 或更高版本。  
- **實作需要多長時間？** 基本的描邊變更通常在 10 分鐘以內完成。

## 什麼是 PSD 中的描邊圖層？

描邊圖層是一種向量效果，會在圖層內容周圍繪製輪廓線。它可自訂顏色、粗細、不透明度與混合模式。以程式方式修改此效果，可實現自動化品牌化、批次處理或動態圖形產生。

## 為何使用 Aspose.PSD 變更描邊顏色？

- **不需 Photoshop** – 完全在 Java 中操作。  
- **完整符合 PSD 規範** – 支援所有現代 PSD 功能。  
- **高效能** – 快速處理大型檔案。  
- **跨平台** – 在任何安裝 JVM 的作業系統上執行。

## 如何以程式方式變更描邊顏色

以下是一個簡潔的逐步說明，示範如何使用 Aspose.PSD for Java 變更描邊顏色。每一步都包含簡短說明，並附上原始程式碼區塊（未更動）。

### 前置條件

- **Aspose.PSD 函式庫** – 從[官方文件](https://reference.aspose.com/psd/java/)下載。  
- **Java Development Kit (JDK)** – 8 版或更新版本。  
- **IDE** – Eclipse、IntelliJ IDEA 或任何相容 Java 的編輯器。

### 匯入套件

首先，匯入您需要的類別。這樣您的專案即可使用 PSD 處理與描邊效果的 API。

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

建立新的 Java 專案，將 Aspose.PSD JAR 加入建置路徑，並確認函式庫能正常載入且無錯誤。

### 步驟 2：載入 PSD 檔案

啟用載入效果資源，以取得描邊資訊。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### 步驟 3：存取描邊效果圖層

從第二層（索引 1）取得第一個描邊效果。

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### 步驟 4：驗證描邊屬性

在進行變更前先確認現有屬性，以避免意外結果。

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### 步驟 5：設定顏色與不透明度（如何更改描邊顏色）

此處我們將**描邊顏色**更改為黃色，並將不透明度降低至 50 %（127 / 255）。

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### 步驟 6：儲存已修改的 PSD

將更新後的圖像寫回磁碟。新檔案現在包含已修改的描邊。

```java
im.save(exportPath);
```

## 常見的描邊顏色變更使用情境

- **品牌自動化**：在一次批次執行中，將企業色彩套用至數百個 PSD 資產的商標。  
- **動態 UI 產生**：根據使用者在網路設計工具中選擇的主題即時變更描邊顏色。  
- **前置檢查**：在將檔案送至印刷前，確保所有描邊顏色符合印刷規格。

## 常見陷阱與技巧

- **空值檢查** – 在轉型前務必確認 `getEffects()` 回傳的陣列非 null。  
- **圖層索引** – PSD 圖層採零基索引；請確保目標圖層正確。  
- **顏色格式** – `Color.getYellow()` 只是範例；您可以使用 `new Color(r, g, b)` 建立自訂顏色。  
- **不透明度範圍** – 不透明度為位元組（0–255）；超過 255 的值會被限制。  
- **資源載入** – 若遺漏 `loadOptions.setLoadEffectsResource(true)`，將導致 `null` 的效果陣列。

## 常見問與答

**Q: 我可以將 Aspose.PSD 與其他 Java 圖形函式庫一起使用嗎？**  
A: 可以，Aspose.PSD 可與 Apache Commons Imaging 或 Java2D 等函式庫結合，以擴充功能。

**Q: Aspose.PSD 是否相容最新的 PSD 檔案格式？**  
A: 絕對相容。此函式庫會定期更新，以支援最新的 Photoshop 規格。

**Q: 使用 Aspose.PSD 時，我該如何處理例外情況？**  
A: 請參考[支援論壇](https://forum.aspose.com/c/psd/34)以取得詳細除錯資訊與範例錯誤處理程式碼。

**Q: 我可以在購買前試用 Aspose.PSD 嗎？**  
A: 當然可以！取得[免費試用](https://releases.aspose.com/)以探索全部功能。

**Q: 我可以從哪裡取得 Aspose.PSD 的臨時授權？**  
A: 取得[臨時授權](https://purchase.aspose.com/temporary-license/)以在開發環境中評估此函式庫。

---

**最後更新：** 2026-02-07  
**測試環境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}