---
date: 2025-11-30
description: 學習如何使用 Aspose.PSD for Java 添加描邊並更改 PSD 描邊顏色。請遵循此一步一步的指南來修改描邊圖層的顏色和不透明度。
language: zh-hant
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: 如何在 Aspose.PSD for Java 中添加描邊圖層顏色
url: /java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.PSD for Java 中新增筆劃圖層顏色

## 介紹

如果您需要 **如何新增筆劃** 到 Photoshop 文件（以程式方式），Aspose.PSD for Java 讓這件事變得相當簡單。在本教學中，我們將示範如何新增筆劃圖層顏色、調整其不透明度，並儲存結果。最後您還會看到如何 **如何變更筆劃顏色**（或 *變更 PSD 筆劃顏色*）於任何既有圖層，讓您能從 Java 程式碼取得完整的創意控制。

## 快速解答
- **需要哪個函式庫？** Aspose.PSD for Java（最新版本）。  
- **可以變更筆劃顏色嗎？** 可以 – 使用 `ColorFillSettings` 設定任意 `Color`。  
- **需要授權嗎？** 評估期間可使用臨時授權；正式環境必須購買正式授權。  
- **支援哪個 Java 版本？** Java 8 或以上。  
- **實作需要多久？** 基本的筆劃變更通常在 10 分鐘以內完成。

## 什麼是 PSD 中的筆劃圖層？
筆劃圖層是一種向量效果，會在圖層內容周圍繪製輪廓。它可以自訂顏色、粗細、不透明度與混合模式。以程式方式修改此效果，可實現自動化品牌化、批次處理或動態圖形產生。

## 為什麼使用 Aspose.PSD 變更筆劃顏色？
- **不需 Photoshop** – 完全在 Java 中完成。  
- **完整符合 PSD 規範** – 支援所有現代 PSD 功能。  
- **高效能** – 快速處理大型檔案。  
- **跨平台** – 只要有 JVM 的作業系統皆可執行。

## 前置需求

- **Aspose.PSD 函式庫** – 從[官方文件](https://reference.aspose.com/psd/java/)下載。  
- **Java Development Kit (JDK)** – 版本 8 或更新。  
- **IDE** – Eclipse、IntelliJ IDEA，或任何支援 Java 的編輯器。

## 匯入套件

首先，匯入您需要的類別。這樣專案才能使用 PSD 處理與筆劃效果的 API。

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

## 步驟 1：設定專案

建立新的 Java 專案，將 Aspose.PSD JAR 加入 Build Path，並確認函式庫能正確載入且不產生錯誤。

## 步驟 2：載入 PSD 檔案

啟用載入效果資源，以確保筆劃資訊可被取得。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## 步驟 3：存取筆劃效果圖層

從第二個圖層（索引 1）取得第一個筆劃效果。

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## 步驟 4：驗證筆劃屬性

在進行變更前先確認現有屬性，以避免意外結果。

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## 步驟 5：設定顏色與不透明度（如何變更筆劃顏色）

此處我們 **變更 PSD 筆劃顏色** 為黃色，並將不透明度降低至 50 %（127 / 255）。

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## 步驟 6：儲存已修改的 PSD

將更新後的影像寫回磁碟。新檔案現在已包含修改過的筆劃。

```java
im.save(exportPath);
```

## 常見問題與技巧

- **空值檢查** – 在轉型前務必確認 `getEffects()` 回傳的陣列非 null。  
- **圖層索引** – PSD 圖層採零基索引；請確保目標圖層正確。  
- **顏色格式** – `Color.getYellow()` 只是一個範例，您也可以使用 `new Color(r, g, b)` 建立自訂顏色。  
- **不透明度範圍** – 不透明度為 byte（0–255），超過 255 的值會被截斷。

## 結論

您現在已學會 **如何新增筆劃** 到 PSD 檔案，以及 **如何變更筆劃顏色**，全部透過 Aspose.PSD for Java 完成。可自行嘗試不同的顏色、混合模式與不透明度，打造符合專案需求的視覺風格。

## 常見問答

**Q: 可以將 Aspose.PSD 與其他 Java 圖形函式庫一起使用嗎？**  
A: 可以，Aspose.PSD 能與 Apache Commons Imaging 或 Java2D 等函式庫結合，擴充功能。

**Q: Aspose.PSD 是否相容最新的 PSD 檔案格式？**  
A: 完全相容。函式庫會定期更新，以支援最新的 Photoshop 規範。

**Q: 使用 Aspose.PSD 時該如何處理例外狀況？**  
A: 請參考[支援論壇](https://forum.aspose.com/c/psd/34)取得詳細除錯說明與範例錯誤處理程式碼。

**Q: 可以先試用 Aspose.PSD 再決定購買嗎？**  
A: 當然可以！取得[免費試用](https://releases.aspose.com/)以探索全部功能。

**Q: 哪裡可以取得 Aspose.PSD 的臨時授權？**  
A: 前往[臨時授權](https://purchase.aspose.com/temporary-license/)頁面，在開發環境中評估函式庫。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-11-30  
**測試環境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

---