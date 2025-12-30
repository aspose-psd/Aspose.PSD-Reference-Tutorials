---
date: 2025-12-30
description: 了解如何在 Aspose.PSD for Java 中套用覆蓋層、設定覆蓋層不透明度，並自訂覆蓋層顏色。一步一步的指南，附有程式碼範例。
linktitle: Apply Color Overlay Effect
second_title: Aspose.PSD Java API
title: 如何在 Aspose.PSD for Java 中套用覆蓋效果
url: /zh-hant/java/image-editing/color-overlay-effect/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.PSD for Java 中套用 Overlay 效果

## 介紹

歡迎來到使用 Aspose.PSD for Java 進行圖形設計與影像處理的世界！在本教學中，我們將示範 **如何對 PSD 圖層套用 overlay**、設定 overlay 不透明度，並自訂 overlay 顏色。無論您是要建立批次處理工具，或是為設計加入品牌色彩，本指南都會以清晰的說明與可直接執行的程式碼，逐步帶您完成。

## 快速回答
- **使用哪個函式庫？** Aspose.PSD for Java  
- **主要目標？** 學習套用 overlay、設定 overlay 不透明度，以及自訂 overlay 顏色  
- **先備條件？** Java SDK、Aspose.PSD for Java、一個可編輯的 PSD 檔案  
- **典型實作時間？** 基本 overlay 約 10‑15 分鐘  
- **之後可以更改 overlay 顏色嗎？** 可以 – 只要修改 `ColorOverlayEffect` 屬性並重新儲存檔案即可  

## 先備條件

在開始之前，請確保您具備以下項目：

1. **Java 開發環境** – 已安裝 JDK 8 或更高版本。  
2. **Aspose.PSD 函式庫** – 從 [此處](https://releases.aspose.com/psd/java/) 下載並安裝 Aspose.PSD for Java。  
3. **PSD 文件** – 一個 PSD 檔案（例如 *ColorOverlay.psd*），內含至少一個您想套用 overlay 的圖層。  

## 匯入套件

在您的 Java 專案中匯入必要的套件，以便編譯器能找到您將使用的類別。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## 步驟說明

### 步驟 1：設定文件目錄

```java
String dataDir = "Your Document Directory";
```

將 **Your Document Directory** 替換為您 PSD 檔案所在的絕對路徑。

### 步驟 2：載入含有效果的 PSD 檔案

```java
String sourceFileName = dataDir + "ColorOverlay.psd";
String psdPathAfterChange = dataDir + "ColorOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

`setLoadEffectsResource(true)` 旗標會告訴 Aspose.PSD 載入任何現有的圖層效果，這是之後存取 overlay 所必需的。

### 步驟 3：取得 Color Overlay 效果

```java
com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect colorOverlay = (com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect)
        (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

此處我們取得第二個圖層（索引 1）的第一個效果。若您的 PSD 結構不同，請自行調整索引。

### 步驟 4：自訂 Overlay 顏色並設定不透明度

```java
colorOverlay.setColor(Color.getGreen());
colorOverlay.setOpacity((byte) 128);
```

- **自訂 overlay 顏色** – 可使用 `Color` 中的任何靜態顏色，或以 `new Color(r, g, b)` 建立自訂顏色。  
- **設定 overlay 不透明度** – 不透明度值介於 0（完全透明）至 255（完全不透明）之間。此範例將其設為 50 %（`128`）。  

> **小技巧：** 若要 **動態變更 PSD overlay 顏色**，可從設定檔讀取所需的十六進位值，並使用 `Color.fromArgb()` 轉換。

### 步驟 5：儲存已修改的 PSD 檔案

```java
im.save(psdPathAfterChange);
```

編輯後的檔案 *ColorOverlayChanged.psd* 現已包含新的 overlay 顏色與不透明度。

## 為何選擇 Aspose.PSD 進行 Overlay 操作？

- **完整 PSD 相容性** – 所有圖層效果、遮色片與智慧物件皆得以保留。  
- **跨平台** – 同一段 Java 程式碼可在 Windows、Linux 與 macOS 上執行。  
- **不需 Adobe Photoshop** – 非常適合自動化工作流程或伺服器端處理。  

## 常見應用情境

- **品牌化** – 大量為行銷素材套用企業色彩 overlay。  
- **主題化** – 動態調整 UI 模型以符合深色或淺色主題。  
- **校樣** – 快速測試不同 overlay 不透明度對可讀性的影響。  

## 常見問題與解決方案

| 問題 | 解決方案 |
|------|----------|
| **Overlay 未顯示** | 確認已設定 `loadOptions.setLoadEffectsResource(true)`，且目標圖層確實具有 `ColorOverlayEffect`。 |
| **圖層索引錯誤** | 使用 `im.getLayers()` 檢查圖層名稱，選取正確的索引。 |
| **不透明度過淡或過深** | 調整位元值（0‑255），記得 255 代表完全不透明。 |
| **顏色未套用** | 確認使用 `colorOverlay.setColor()` 並傳入有效的 `Color` 例項。 |

## 常見問答

**Q: 可以在同一圖層套用多個 overlay 嗎？**  
A: 不行，一個圖層只能有一個 Color Overlay Effect。若需多重顏色效果，請複製圖層並分別套用不同的 overlay。

**Q: Aspose.PSD 是否相容各種 Java IDE？**  
A: 相容，支援 Eclipse、IntelliJ IDEA、NetBeans 以及任何支援 Maven 或 Gradle 的 IDE。

**Q: 可以將 Aspose.PSD 用於商業專案嗎？**  
A: 可以，無論是個人或商業應用皆可使用。授權細節請參閱 [此處](https://purchase.aspose.com/buy)。

**Q: 如何取得 Aspose.PSD 的支援？**  
A: 前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 取得社群協助，或購買 [臨時授權](https://purchase.aspose.com/temporary-license/) 以獲得優先支援。

**Q: 有提供免費試用嗎？**  
A: 有，請先試用 [免費試用版](https://releases.aspose.com/) 再決定是否購買。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-12-30  
**測試環境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

---