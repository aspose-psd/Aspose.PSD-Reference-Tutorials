---
date: 2026-02-14
description: 學習如何使用 Aspose.PSD for Java 為 PSD 添加內陰影，並透過此一步一步的教學以程式方式套用 PSD 圖層效果，內含技巧與最佳實踐。
linktitle: Add Inner Shadow PSD Layer Effect in Java
second_title: Aspose.PSD Java API
title: 如何在 Java 中添加 PSD 圖層內陰影效果
url: /zh-hant/java/advanced-psd-layer-features-effects/add-inner-shadow-layer-effect-psd/
weight: 12
---

 paths.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中添加內陰影 PSD 圖層效果

## Introduction
如果您需要以程式方式**添加內陰影 PSD**，您來對地方了。在本指南中，我們將示範如何使用 Aspose.PSD for Java 為任何 Photoshop 文件**添加內陰影**。無論您是在構建批次處理工具、自動化設計流水線，或僅僅在嘗試圖像效果，以下步驟都會為您提供一個穩固、可投入生產的解決方案，您可以將其整合到 Java 應用程式中。

## Quick Answers
- **需要什麼函式庫？** Aspose.PSD for Java.  
- **實作需要多長時間？** 基本設定大約需要 10‑15 分鐘。  
- **需要安裝 Photoshop 嗎？** 不需要，該函式庫可獨立於 Photoshop 運作。  
- **可以更改陰影顏色嗎？** 可以 – `setColor` 方法接受任何 `Color`。  
- **正式環境需要授權嗎？** 需要商業授權；亦提供免費試用版。

## What is “add inner shadow psd”?
在 PSD 檔案中添加內陰影是指建立一種細微的內部陰影效果，使圖層內部呈現深度感。此效果常用於讓 UI 元件、圖示或文字在不加入外部發光的情況下更突出。

## Why apply PSD layer effect with Java?
使用 Java **套用 PSD 圖層效果** 可讓您自動化重複的設計工作、將影像處理整合至後端服務，並即時產生資產，無需手動操作 Photoshop。Aspose.PSD 提供乾淨的物件導向 API，抽象化 PSD 檔案格式的複雜性。

## Prerequisites
Before diving into code, make sure you have:

1. **Java Development Kit (JDK 11 或以上)** – download from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA、Eclipse 或 NetBeans（任一皆可）。  
4. **Basic Java knowledge** – 您應該熟悉類別、物件與例外處理。  
5. **Sample PSD file** – 一個至少包含一個圖層的簡易 PSD，用於測試內陰影效果。

## Import Required Packages
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layereffects.IShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```
這些匯入讓您可以使用載入 PSD、操作圖層以及設定陰影效果所需的核心類別。

## How to add inner shadow psd in a PSD file using Java
Below is a step‑by‑step guide. Each step includes a short explanation followed by the exact code you need to copy.

### Step 1: Define source and destination directories
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String destName = outputDir + "sample_out.psd";
```
將佔位路徑替換為您機器上的實際位置。

### Step 2: Load the PSD file with effect resources
```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage image = (PsdImage) Image.load(sourceFile, loadOptions);
```
`setLoadEffectsResource(true)` 確保載入任何現有的圖層效果，讓我們可以對其進行修改。

### Step 3: Access the target layer
```java
try {
    Layer layer = image.getLayers()[image.getLayers().length - 1];
```
此處取得文件中的**最後一個圖層**，通常是您想編輯的圖層。如需其他圖層，請調整索引值。

### Step 4: Configure the inner shadow effect
```java
    IShadowEffect shadowEffect = (IShadowEffect) layer.getBlendingOptions().getEffects()[0];
    shadowEffect.setColor(Color.getGreen());
    shadowEffect.setOpacity((byte) 128);
    shadowEffect.setDistance(1);
    shadowEffect.setUseGlobalLight(false);
    shadowEffect.setSize(2);
    shadowEffect.setAngle(45);
    shadowEffect.setSpread(50);
    shadowEffect.setNoise(5);
```
此區塊**套用內陰影**並自訂外觀：
- **Color** – 設為綠色（可更換為任意 `Color`）。  
- **Opacity** – 50 % 透明度（`255` 中的 `128`）。  
- **Distance、Size、Angle** – 控制陰影的偏移與擴散。  
- **Spread & Noise** – 增加藝術變化。

### Step 5: Save the modified PSD
```java
    image.save(destName, new PsdOptions(image));
```
檔案 `sample_out.psd` 現已包含內陰影效果。

### Step 6: Clean up resources
```java
} finally {
    image.dispose();
}
```
釋放 `image` 物件可釋放記憶體並防止洩漏，這在迴圈處理大量檔案時尤為重要。

## Common Use Cases
- **自動化品牌流水線** – 在發布前為商標添加一致的內陰影。  
- **動態 UI 資產產生** – 為網頁或行動應用即時產生具深度的按鈕狀態。  
- **批次處理舊有 PSD 資源庫** – 在不開啟 Photoshop 的情況下為舊設計加上現代陰影。

## Common Issues and Solutions
| Issue | Why It Happens | Fix |
|-------|----------------|-----|
| **`ArrayIndexOutOfBoundsException` on `getEffects()[0]`** | 目標圖層尚未附加任何效果。 | 在轉型前先透過 `layer.getBlendingOptions().addEffect(new ShadowEffect())` 新增 `IShadowEffect`。 |
| **Shadow color not changing** | 圖層已有其他效果類型覆蓋了陰影。 | 確保編輯正確的效果索引，或使用 `layer.getBlendingOptions().clearEffects()` 清除現有效果。 |
| **File not saved** | 目的目錄不存在或沒有寫入權限。 | 事先建立目錄 (`new File(outputDir).mkdirs();`) 或選擇可寫入的路徑。 |

## Frequently Asked Questions

**Q: 什麼是 Aspose.PSD？**  
A: Aspose.PSD 是一個用於處理 PSD 檔案的 Java 函式庫，讓開發者能以程式方式操作圖層效果、遮罩與影像屬性。

**Q: 使用 Aspose.PSD 是否需要 Photoshop？**  
A: 不需要，該函式庫可獨立於 Photoshop 操作 PSD 檔案。

**Q: 可以在同一圖層套用多個效果嗎？**  
A: 當然可以！您可以像存取內陰影效果那樣，分別存取每種效果類型以套用多個效果。

**Q: Aspose.PSD 是否免費？**  
A: Aspose.PSD 為商業產品；不過可透過 Aspose 取得免費試用版。

**Q: 哪裡可以找到更多文件？**  
A: 您可在此處取得 Aspose.PSD 的完整文件 [here](https://reference.aspose.com/psd/java/).

## Conclusion
您現在已了解如何使用 Aspose.PSD for Java **添加內陰影 PSD** 以及 **套用 PSD 圖層效果**。此方法可讓您自動化精細的設計調整、整合至後端服務，或為大型影像庫建構批次處理器。歡迎嘗試其他效果類型——投影、發光、斜角等，以擴充您的工具箱。

---

**Last Updated:** 2026-02-14  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}