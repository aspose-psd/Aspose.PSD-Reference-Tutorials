---
date: 2026-02-07
description: 學習如何將 PSD 另存為 PNG、匯出含 Alpha 通道的 PNG，並使用 Aspose.PSD for Java 加入投影圖層——完整的逐步指南。
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: 將 PSD 另存為 PNG 並在 Aspose.PSD for Java 中套用渲染陰影
url: /zh-hant/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 儲存為 PNG 並在 Aspose.PSD for Java 中套用渲染陰影

## Introduction

如果你在 Java 中處理 Photoshop 檔案，**將 PSD 儲存為 PNG** 是最常見的工作之一。使用 Aspose.PSD，你不僅可以**將 PSD 轉換為 PNG**，還能透過**加入投影圖層**來增強影像。本教學將逐步說明完整流程——載入 PSD、套用渲染投影，最後**將 PSD 儲存為 PNG** 檔案——讓你能自信地將此工作流程整合到自己的專案中。

## Quick Answers
- **哪個函式庫負責 PSD 轉 PNG 轉換？** Aspose.PSD for Java.  
- **投影實作需要多久？** 基本範例大約 10‑15 分鐘。  
- **執行程式碼需要授權嗎？** 免費試用可用於評估；正式環境需購買授權。  
- **可以同時對多個圖層套用投影嗎？** 可以——只要在迴圈中處理目標圖層即可。  
- **需要哪個版本的 Java？** Java 8 或以上。

## What is “save PSD as PNG” and why does it matter?

將 PSD 儲存為 PNG 會產生一種廣受支援、無損且保留透明度的影像。當你需要在網站、行動應用程式或更大的影像處理流程中顯示 Photoshop 資產時，這是必備的。同時加入投影，能在不開啟 Photoshop 的情況下產生精緻的視覺效果。

## Why use Aspose.PSD for this workflow?

* **從程式碼完整掌控** – 無需啟動 Photoshop 或依賴外部工具。  
* **保留圖層效果** – 投影、發光等效果會如原始檔案般精確呈現。  
* **匯出具 Alpha 通道的 PNG** – PNG 輸出保留透明背景，直接可用於網頁或 UI。  
* **跨平台** – 在任何支援 Java 8+ 的作業系統上皆可執行。

## Prerequisites

在開始之前，請確保你已具備：

- **Java 開發環境** – 已安裝 JDK 8 或更新版本。  
- **Aspose.PSD for Java** – 從 [Aspose.PSD 下載頁面](https://releases.aspose.com/psd/java/) 下載最新 JAR。  
- **PSD 檔案** – 檔案需至少包含一個你想套用投影的圖層（例如 *Shadow.psd*）。  

## Import Packages

首先，匯入我們將使用的類別。這樣即可存取影像載入、圖層效果與 PNG 匯出選項。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step‑by‑Step Guide

### Step 1: Define Document Directory  
告訴程式你的來源 PSD 檔案所在的目錄。

```java
String dataDir = "Your Document Directory";
```

### Step 2: Set PSD and PNG File Paths  
指定輸入的 PSD 與輸出的 PNG（將包含渲染後的投影）。

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Step 3: Load PSD File with Effects  
啟用載入效果資源，以便我們能操作投影效果。

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Step 4: Access Drop Shadow Effect  
從第二個圖層（索引 1）取得第一個投影效果。這裡可以驗證或修改參數。

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Step 5: Validate Shadow Effect Properties  
在儲存前確認效果屬性符合預期。你也可以微調這些值以得到不同的外觀。

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

> **專業提示：** 調整 `setSpread()` 或 `setNoise()` 可產生較柔和或較具紋理的投影。

### Step 6: Save as PNG – the “save PSD as PNG” step  
將修改後的影像匯出為 PNG，保留 Alpha 通道，使投影能正確混合。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

此時你已成功 **將 PSD 轉換為 PNG**、**匯出具 Alpha 的 PNG**，並在單一工作流程中套用渲染投影。

## Export PNG with Alpha Transparency

當你需要 PNG 輸出保留透明背景（尤其是 UI 蓋層或網頁圖形）時，請如上一步所示使用 `PngColorType.TruecolorWithAlpha`。這可確保投影位於透明畫布上，而非實心背景。

## Add Drop Shadow Layer Using Java

如果你的 PSD 包含多個需要投影的圖層，只需在迴圈中對 `im.getLayers()` 逐層執行 **Step 4** 與 **Step 5**。每次迭代都可以建立或修改 `DropShadowEffect` 實例，讓你對每個圖層的透明度、距離、大小與角度進行精細控制。

## Java Convert Photoshop PNG – Common Use Cases

* **Web 資產管線** – 將設計師提供的 PSD 轉換為即時可用的 PNG，並內建投影。  
* **行動應用程式資源** – 即時產生透明 PNG 圖示，免除手動匯出。  
* **批次處理** – 在伺服器端工作中自動轉換數百個 PSD 檔案。

## Common Issues and Solutions

| 問題 | 可能原因 | 解決方法 |
|-------|--------------|-----|
| **投影未顯示** | `Opacity` 設為 0 或圖層被隱藏 | 確認 `shadowEffect.getOpacity()` 大於 0 且圖層可見。 |
| **PNG 看起來是平面的（無透明度）** | 使用了錯誤的 `PngColorType` | 如上所示使用 `PngColorType.TruecolorWithAlpha`。 |
| **載入時拋出例外** | 未載入效果資源 | 確保已呼叫 `loadOptions.setLoadEffectsResource(true)`。 |
| **圖層索引不正確** | PSD 結構與預期不同 | 檢查 `im.getLayers()` 並選擇正確的索引。 |

## Frequently Asked Questions

**Q: 可以同時對多個圖層套用投影嗎？**  
A: 可以。對 `im.getLayers()` 迴圈，為每個目標圖層新增或修改 `DropShadowEffect`。

**Q: ‘Spread’ 參數控制什麼？**  
A: `Spread` 決定投影從完全不透明過渡到透明的突變程度。數值越高，邊緣越硬。

**Q: Aspose.PSD 是否相容所有 Photoshop 版本？**  
A: Aspose.PSD 支援從 Photoshop 3.0 到最新版本的 PSD 檔案，能處理大多數圖層類型與效果。

**Q: 如何在購買授權前測試程式碼？**  
A: 從 [Aspose.PSD 下載頁面](https://releases.aspose.com/psd/java/) 下載免費試用版，並在未設定授權金鑰的情況下執行範例。

**Q: 若遇到問題該向哪裡尋求協助？**  
A: 可在 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 發問，社群與 Aspose 工程師會提供協助。

## Conclusion

現在你已掌握如何 **將 PSD 儲存為 PNG**、**匯出具 Alpha 的 PNG**、**轉換 Photoshop PNG** 檔案，並使用 Aspose.PSD for Java **套用投影圖層**。這套組合讓你能自動化高品質的影像前處理，適用於網站、行動或桌面應用程式——完全不需開啟 Photoshop。

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}