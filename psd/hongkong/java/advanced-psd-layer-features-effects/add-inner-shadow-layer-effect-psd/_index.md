---
date: 2025-12-09
description: 學習如何使用 Aspose.PSD for Java 為 PSD 添加內部陰影，並以程式方式套用 PSD 圖層效果，透過本一步一步的教學，包括技巧與最佳實踐。
language: zh-hant
linktitle: Add Inner Shadow PSD Layer Effect in Java
second_title: Aspose.PSD Java API
title: 在 Java 中加入內陰影 PSD 圖層效果
url: /java/advanced-psd-layer-features-effects/add-inner-shadow-layer-effect-psd/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中新增內部陰影 PSD 圖層效果

## Introduction
如果你需要以程式方式 **add inner shadow psd**，你來對地方了。在本教學中，我們將示範如何使用 Aspose.PSD for Java 來 **apply PSD layer effect** — 具體而言是內部陰影 — 於任何 Photoshop 文件。無論你是建立批次處理工具、自動化設計流程，或只是試驗影像效果，以下步驟都能提供一個穩固、可投入生產的解決方案。

## Quick Answers
- **需要什麼函式庫？** Aspose.PSD for Java.  
- **實作需要多久？** 基本設定大約 10‑15 分鐘。  
- **需要安裝 Photoshop 嗎？** 不需要，函式庫可獨立於 Photoshop 運作。  
- **可以更改陰影顏色嗎？** 可以 – `setColor` 方法接受任何 `Color`。  
- **生產環境需要授權嗎？** 需要商業授權；亦提供免費試用版。

## What is “add inner shadow psd”?
在 PSD 檔案中加入內部陰影，表示在圖層內部創建細微的陰影效果，使其呈現出深度感。此效果常用於讓 UI 元件、圖示或文字在不加入外部發光的情況下突顯。

## Why apply PSD layer effect with Java?
使用 Java **apply PSD layer effect** 可讓你自動化重複的設計任務，將影像處理整合至後端服務，並即時產生資產，無需手動操作 Photoshop。Aspose.PSD 提供乾淨的物件導向 API，抽象化 PSD 檔案格式的複雜性。

## Prerequisites
在開始撰寫程式碼之前，請確保你已具備以下條件：

1. **Java Development Kit (JDK 11 或更新版本)** – 從 [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java** – 從 [Aspose releases page](https://releases.aspose.com/psd/java/) 取得最新 JAR。  
3. **IDE** – IntelliJ IDEA、Eclipse 或 NetBeans（皆可）。  
4. **基本的 Java 知識** – 需要熟悉類別、物件與例外處理。  
5. **範例 PSD 檔案** – 至少包含一個圖層的簡易 PSD，用於測試內部陰影效果。

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
這些匯入讓你能存取載入 PSD、操作圖層以及設定陰影效果所需的核心類別。

## How to add inner shadow psd in a PSD file using Java
以下是一個逐步指南。每一步都包含簡短說明，並附上需要複製的完整程式碼。

### Step 1: Define source and destination directories
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String destName = outputDir + "sample_out.psd";
```
將佔位路徑替換為你機器上的實際位置。

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
此處取得文件中的 **最後一個圖層**，通常是你想編輯的圖層。如需其他圖層，請調整索引。

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
此區塊 **applies the inner shadow** 並自訂其外觀：
- **Color** – 設為綠色（可更改為任何你喜歡的 `Color`）。  
- **Opacity** – 50 % 透明度（`255` 中的 `128`）。  
- **Distance, Size, Angle** – 控制陰影的偏移與擴散。  
- **Spread & Noise** – 添加藝術化的變化。

### Step 5: Save the modified PSD
```java
    image.save(destName, new PsdOptions(image));
```
檔案 `sample_out.psd` 現已包含內部陰影效果。

### Step 6: Clean up resources
```java
} finally {
    image.dispose();
}
```
釋放 `image` 物件可釋放記憶體並防止泄漏，這在迴圈處理大量檔案時尤為重要。

## Common Issues and Solutions
| 問題 | 發生原因 | 解決方案 |
|-------|----------------|-----|
| **`ArrayIndexOutOfBoundsException` on `getEffects()[0]`** | 目標圖層尚未附加任何效果。 | 在轉型前，透過 `layer.getBlendingOptions().addEffect(new ShadowEffect())` 新增 `IShadowEffect`。 |
| **Shadow color not changing** | 圖層已有其他效果類型覆蓋了陰影。 | 確認正在編輯正確的效果索引，或使用 `layer.getBlendingOptions().clearEffects()` 清除現有效果。 |
| **File not saved** | 目標目錄不存在或缺乏寫入權限。 | 事先建立目錄（`new File(outputDir).mkdirs();`），或選擇可寫入的路徑。 |

## Frequently Asked Questions

**Q: 什麼是 Aspose.PSD？**  
A: Aspose.PSD 是一個用於處理 PSD 檔案的 Java 函式庫，讓開發者能以程式方式操作圖層效果、遮罩與影像屬性。

**Q: 使用 Aspose.PSD 需要 Photoshop 嗎？**  
A: 不需要，Aspose.PSD 可獨立於 Photoshop 進行 PSD 檔案操作。

**Q: 可以在同一圖層套用多個效果嗎？**  
A: 當然可以！只要像存取內部陰影效果那樣，分別存取每種效果類型即可套用多個效果。

**Q: Aspose.PSD 免費嗎？**  
A: Aspose.PSD 為商業產品；不過可透過 Aspose 取得免費試用版。

**Q: 在哪裡可以找到更多文件？**  
A: 您可於此處取得 Aspose.PSD 的完整文件 [here](https://reference.aspose.com/psd/java/)。

## Conclusion
現在您已了解如何使用 Aspose.PSD for Java **add inner shadow psd** 以及 **apply PSD layer effect**。此方法可自動化複雜的設計調整、整合至後端服務，或為大型影像庫建立批次處理器。歡迎嘗試其他效果類型——投影、發光、斜角等，擴充您的工具箱。

---

**最後更新：** 2025-12-09  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}