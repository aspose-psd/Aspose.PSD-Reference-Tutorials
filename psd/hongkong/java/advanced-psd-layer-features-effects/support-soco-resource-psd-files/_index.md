---
date: 2026-02-25
description: 在本分步指南中，學習如何使用 Aspose.PSD for Java 透過修改填充圖層來更改純色並批量編輯 PSD 檔案。
linktitle: How to Change Solid Color in PSD Files Using Java
second_title: Aspose.PSD Java API
title: 如何使用 Java 更改 PSD 檔案的純色
url: /zh-hant/java/advanced-psd-layer-features-effects/support-soco-resource-psd-files/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Java 更改 PSD 檔案中的 Solid Color

## Introduction
如果您需要在 Photoshop PSD 中 **編輯 SoCo** 資源，甚至 **更改 PSD 圖層顏色**，Aspose.PSD for Java 讓這個過程出奇地簡單。在本教學中，我們將逐步說明整個流程——從設定環境到儲存編輯後的檔案——讓您能以程式方式 **更改實心顏色**、批次編輯 PSD 檔案，並將此邏輯整合到更大的 Java 應用程式中。無論您是自動化批次工作流程，還是構建自訂圖形編輯器，以下步驟都能為您奠定堅實的基礎。

## Quick Answers
- **What is SoCo?** Photoshop 的 “Solid Color” 資源，用於定義圖層的單一顏色填充。  
- **Which library helps edit it?** Aspose.PSD for Java。  
- **Do I need a license?** 免費試用版可用於探索；正式環境需購買商業授權。  
- **Can I change the layer color?** 可以——使用 `SoCoResource.setColor()` 取代現有顏色。  
- **How long does it take?** 通常在 10 分鐘內即可完成實作與測試。

## What is “how to edit soco” in the context of PSD files?
「how to edit soco」這個說法指的是以程式方式存取與修改 Photoshop 為填充圖層儲存的 Solid Color（SoCo）資源。透過編輯此資源，您可以在不手動開啟 Photoshop 的情況下變更圖層的視覺外觀。

## Why edit SoCo resources with Java?
- **Automation:** 在不需要手動點擊的情況下處理數百個 PSD。  
- **Consistency:** 確保所有檔案使用相同的顏色值。  
- **Integration:** 將影像處理與其他基於 Java 的業務邏輯結合。  
- **Batch edit PSD:** 同一段程式碼可放入迴圈，一次處理多個檔案。

## Prerequisites
在開始之前，請確保您已具備以下項目：

1. **Java Development Kit (JDK)** – 從 [Oracle 官方網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java** – 從官方下載頁面 [此處](https://releases.aspose.com/psd/java/) 取得程式庫。  
3. **IDE** – IntelliJ IDEA、Eclipse，或您偏好的任何編輯器。  
4. **Basic Java knowledge** – 熟悉類別、物件與例外處理。

準備好以上項目後，即可匯入所需的套件。

## Import Packages
第一步是將 Aspose.PSD 類別匯入作用域：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.SoCoResource;
```

## Step‑by‑Step Guide

### Step 1: Setup the File Paths
定義來源 PSD 檔案所在位置以及編輯後檔案的儲存路徑。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath = dataDir + "SoCoResource_Edited.psd";
```

將 `"Your Document Directory"` 替換為您機器上實際的資料夾路徑。

### Step 2: Load the PSD Image
開啟 PSD 檔案，以便操作其圖層。

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### Step 3: Iterate Through Layers
遍歷文件中的每個圖層，以尋找包含 SoCo 資源的圖層。

```java
try {
    for (Layer layer : im.getLayers()) {
        // Process layers here
    }
}
```

### Step 4: Check for FillLayer and SoCoResource
辨識 `FillLayer` 物件，然後在其中尋找 `SoCoResource`。

```java
if (layer instanceof FillLayer) {
    FillLayer fillLayer = (FillLayer) layer;
    
    for (LayerResource resource : fillLayer.getResources()) {
        if (resource instanceof SoCoResource) {
            SoCoResource socoResource = (SoCoResource) resource;
            // Manipulate the SoCoResource here
            break;
        }
    }
}
```

### Step 5: Modify the Color of SoCoResource
現在您可以透過更新 SoCo 資源的顏色值來 **更改 PSD 圖層顏色**。

```java
assert Color.fromArgb(63, 83, 141).equals(socoResource.getColor());
socoResource.setColor(Color.getRed());
```

此斷言驗證原始顏色，`setColor` 則將其切換為紅色。

### Step 6: Save the Edited PSD Image
完成變更後，將更新後的檔案寫回磁碟。

```java
im.save(exportPath);
```

### Step 7: Clean Up Resources
釋放 `PsdImage` 物件，以釋放原生記憶體。

```java
finally {
    im.dispose();
}
```

## How to Change Solid Color in a Fill Layer
上述程式碼示範了在填充圖層中 **更改實心顏色** 的核心。只要將 `Color.getRed()` 呼叫替換為任意 `Color.fromArgb(r, g, b)`，即可設定所需的任何實心顏色。此方法適用於所有使用 SoCo 資源的 PSD，因而非常適合 **修改填充圖層** 的情境。

## Batch Edit PSD Files
若要 **批次編輯 PSD** 檔案，只需將整個步驟區塊包裹在遍歷檔案路徑集合的迴圈中。相同的 `setColor` 操作會套用到每個文件，讓您能快速一次更新多個設計。

## Common Issues & Tips
- **Null resources:** 在迭代前務必確認 `fillLayer.getResources()` 不為 null。  
- **Unsupported color formats:** `Color.getRed()` 只適用於標準 RGB；若需自訂值請使用 `Color.fromArgb()`。  
- **Performance:** 對於大型 PSD，建議在獨立執行緒中處理圖層，以保持 UI 響應。  
- **Edit solid color layer:** 若圖層未包含 SoCo 資源，可能需要手動新增——Aspose.PSD 提供建立新資源的 API。

## Frequently Asked Questions

**Q: 我可以批次編輯多個 PSD 檔案嗎？**  
A: 當然可以。將程式碼包在遍歷檔案路徑清單的迴圈中，對每個檔案套用相同的 SoCo 修改。

**Q: 更改 SoCo 顏色會影響其他圖層嗎？**  
A: 不會。變更僅限於您編輯的包含 SoCo 資源的特定 `FillLayer`。

**Q: 若 PSD 沒有 SoCo 資源該怎麼辦？**  
A: 內部迴圈會直接跳過該圖層。必要時您可以加入備援機制，建立新的 SoCo 資源。

**Q: 有沒有辦法在儲存前預覽顏色變更？**  
A: 您可以將 `PsdImage` 匯出為常見格式如 PNG（`im.save("preview.png")`）以驗證結果。

**Q: 我需要手動關閉影像嗎？**  
A: `finally` 區塊中的 `im.dispose()` 會確保釋放所有原生資源，即使發生例外亦如此。

---

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}