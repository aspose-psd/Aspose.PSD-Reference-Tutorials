---
date: 2026-04-22
description: 學習如何將 PSD 儲存為 PNG、匯出含 Alpha 的 PNG，並使用 Aspose.PSD for Java 新增投影圖層——完整的逐步指南。
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- preserve png transparency
linktitle: 套用渲染投影
second_title: Aspose.PSD Java API
title: 將 PSD 儲存為 PNG 並在 Aspose.PSD for Java 中套用渲染投影陰影
url: /zh-hant/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 另存為 PNG 並在 Aspose.PSD for Java 中套用渲染陰影

## 簡介

如果你在 Java 中處理 Photoshop 檔案，**saving PSD as PNG** 是你最常會遇到的任務之一。在許多專案中，你需要**save psd as png** 以將資產發佈到網站或行動應用程式，同時保留透明度和視覺效果。使用 Aspose.PSD，你不僅可以**convert PSD to PNG**，還能透過**adding a drop shadow layer** 來增強影像。在本教學中，我們將完整示範整個流程——載入 PSD、套用渲染陰影，最後**saving the PSD as a PNG** 檔案——讓你能自信地將此工作流程整合到自己的專案中。

## 快速回答
- **哪個函式庫負責 PSD 轉 PNG 的轉換？** Aspose.PSD for Java.  
- **實作 drop‑shadow 需要多久？** About 10‑15 minutes for a basic example.  
- **執行程式碼是否需要授權？** A free trial works for evaluation; a license is required for production.  
- **可以將陰影套用到多個圖層嗎？** Yes—just loop through the desired layers, which also lets you perform a batch psd to png conversion.  
- **需要哪個 Java 版本？** Java 8 or higher.

## 什麼是「save PSD as PNG」以及為何重要？

**Saving a PSD as PNG** 會產生一種廣受支援、無損且保留透明度的影像。當你需要在網站、行動應用程式或更大的影像處理流程中顯示 Photoshop 資產時，這是必須的。同時加入陰影可讓你在不開啟 Photoshop 的情況下產生精緻的視覺效果。

## 為何在此工作流程中使用 Aspose.PSD？

* **Full control from code** – 無需啟動 Photoshop 或依賴外部工具。  
* **Preserves layer effects** – 陰影、發光及其他效果會如同原始檔案中呈現的方式精確渲染。  
* **Export PNG with alpha** – PNG 輸出會保留透明背景，確保你 **preserve PNG transparency** 用於 UI 或網頁。  
* **Cross‑platform** – 可在任何支援 Java 8+ 的作業系統上執行。  

## 先決條件

在深入之前，請確保你已具備：

- **Java Development Environment** – 已安裝 JDK 8 或更新版本。  
- **Aspose.PSD for Java** – 從 [Aspose.PSD download page](https://releases.aspose.com/psd/java/) 下載最新的 JAR。  
- **A PSD file** – 該檔案應至少包含一個你想套用陰影的圖層（例如 *Shadow.psd*）。  

## 匯入套件

首先，匯入我們需要的類別。這讓我們能存取影像載入、圖層效果以及 PNG 匯出選項。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## 逐步指南

### 步驟 1：定義文件目錄  
告訴程式你的來源 PSD 檔案所在的位置。

```java
String dataDir = "Your Document Directory";
```

### 步驟 2：設定 PSD 與 PNG 檔案路徑  
指定輸入的 PSD 以及將包含渲染陰影的輸出 PNG。

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### 步驟 3：載入帶有效果的 PSD 檔案  
啟用載入效果資源，以便我們能操作 drop‑shadow 效果。

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### 步驟 4：存取 Drop Shadow 效果  
從第二層（索引 1）取得第一個 drop‑shadow 效果。這裡我們將驗證或修改參數。

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### 步驟 5：驗證陰影效果屬性  
在儲存前，確保效果的屬性符合預期。你也可以微調這些值以獲得不同的外觀。

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **Pro tip:** 調整 `setSpread()` 或 `setNoise()` 以產生較柔和或更具紋理的陰影。

### 步驟 6：另存為 PNG – 「save PSD as PNG」步驟  
將修改後的影像匯出為 PNG，保留 alpha 通道，使陰影正確混合。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

此時，你已成功 **converted PSD to PNG**、**exported PNG with alpha**，並在單一工作流程中套用了渲染陰影。

## 匯出具 Alpha 透明度的 PNG

當你需要 PNG 輸出保留透明背景——尤其是用於 UI 疊加或網頁圖形時——請確保使用如上儲存步驟所示的 `PngColorType.TruecolorWithAlpha`。這可保證陰影位於透明畫布上，而非實心背景，協助你 **preserve PNG transparency**。

## 使用 Java 新增 Drop Shadow 圖層

如果你的 PSD 包含多個需要陰影的圖層，只需在迴圈中重複 **Step 4** 和 **Step 5**，該迴圈遍歷 `im.getLayers()`。每次迭代都可以建立或修改 `DropShadowEffect` 實例，讓你對每個圖層的不透明度、距離、大小和角度進行細緻控制。此方法亦可實現 **batch psd to png** 轉換，讓每個檔案都套用相同的陰影處理。

## Saving PSD as PNG 的常見使用情境

* **Web asset pipelines** – 將設計師提供的 PSD 轉換為具備內建陰影的網頁就緒 PNG。  
* **Mobile app resources** – 即時產生透明 PNG 圖示，避免手動匯出。  
* **Batch processing** – 在伺服器端作業中自動轉換數百個 PSD 檔案，確保每個 PNG 保留 alpha 通道與視覺效果。  

## 常見問題與解決方案

| 問題 | 可能原因 | 解決方法 |
|-------|--------------|-----|
| **Shadow not visible** | `Opacity` 設為 0 或圖層被隱藏 | 確認 `shadowEffect.getOpacity()` > 0 且圖層可見。 |
| **PNG appears flat (no transparency)** | 使用了錯誤的 `PngColorType` | 如範例所示使用 `PngColorType.TruecolorWithAlpha`。 |
| **Exception on loading** | 未載入效果 | 確保已呼叫 `loadOptions.setLoadEffectsResource(true)`。 |
| **Incorrect layer index** | PSD 結構不同 | 檢查 `im.getLayers()` 並選擇正確的索引。 |

## 常見問答

**Q: 我可以同時將 drop shadows 套用到多個圖層嗎？**  
A: 可以。遍歷 `im.getLayers()`，為每個目標圖層新增或修改 `DropShadowEffect`，同時也能執行 batch psd to png 轉換。

**Q: ‘Spread’ 參數控制什麼？**  
A: `Spread` 決定陰影從完全不透明過渡到透明的突變程度。數值越高，邊緣越硬。

**Q: Aspose.PSD 是否相容所有 Photoshop 版本？**  
A: Aspose.PSD 支援從 Photoshop 3.0 到最新版本的 PSD 檔案，處理大多數圖層類型與效果。

**Q: 如何在購買授權前測試程式碼？**  
A: 從 [Aspose.PSD download page](https://releases.aspose.com/psd/java/) 下載免費試用版，並在未提供授權金鑰的情況下執行範例。

**Q: 若遇到問題該向哪裡尋求協助？**  
A: 可在 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 發問，社群與 Aspose 工程師會提供協助。

## 結論

現在你已了解如何使用 Aspose.PSD for Java **save psd as png**、**export PNG with alpha**、**convert PSD to PNG**，以及 **apply a drop shadow layer**。此組合讓你能自動化高品質的影像準備，適用於網站、行動或桌面應用程式——無需開啟 Photoshop。

---

**最後更新：** 2026-04-22  
**測試環境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}