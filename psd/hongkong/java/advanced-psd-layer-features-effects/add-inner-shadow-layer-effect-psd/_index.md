---
date: 2026-06-23
description: 學習如何使用 Aspise.PSD for Java 添加內部陰影 PSD，並透過此一步步教學以程式方式套用 PSD 圖層效果，內容包括提示與最佳實踐。
keywords:
- how to add inner shadow
- create inner shadow effect
- Aspose.PSD Java layer effect
linktitle: 在 Java 中添加內部陰影 PSD 圖層效果
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to add inner shadow PSD using Aspise.PSD for Java and apply
    PSD layer effect programmatically with this step‑by‑step tutorial, including tips
    and best practices.
  headline: How to Add Inner Shadow PSD Layer Effect in Java
  type: TechArticle
- description: Learn how to add inner shadow PSD using Aspise.PSD for Java and apply
    PSD layer effect programmatically with this step‑by‑step tutorial, including tips
    and best practices.
  name: How to Add Inner Shadow PSD Layer Effect in Java
  steps:
  - name: Define source and destination directories
    text: Replace the placeholder paths with the actual locations on your machine.
      Using absolute paths avoids confusion when the code runs from different working
      directories.
  - name: Load the PSD file with effect resources
    text: The `PsdImage` class loads a PSD file and provides access to its layers
      and effect resources. `setLoadEffectsResource(true)` ensures that any existing
      layer effects are loaded, allowing us to modify them without overwriting unrelated
      data.
  - name: Access the target layer
    text: The `Layer` object represents an individual layer within a PSD document.
      Here we grab the **last layer** in the document, which is often the one you
      want to edit. Adjust the index if you need a different layer. `Layer layer =
      image.getLayers().get(image.getLayers().size() - 1);` – this line retrieve
  - name: Configure the inner shadow effect
    text: 'This block **applies the inner shadow** and customizes its appearance:
      - **Color** – set to green (change to any `Color` you prefer). - **Opacity**
      – 50 % transparency (`128` out of `255`). - **Distance, Size, Angle** – control
      the shadow’s offset and spread. - **Spread & Noise** – add artistic vari'
  - name: Save the modified PSD
    text: The file `sample_out.psd` now contains the inner shadow effect. Saving with
      `image.save(outputPath, new PsdOptions())` preserves all existing layers and
      effects.
  - name: Clean up resources
    text: Disposing of the `image` object frees memory and prevents leaks, which is
      especially important when processing many files in a loop. Always wrap the usage
      in a try‑with‑resources block or call `image.dispose()` in a finally clause.
  type: HowTo
- questions:
  - answer: Aspose.PSD is a Java library that enables developers to create, edit,
      convert, and render Photoshop PSD files without needing Photoshop installed.
    question: What is Aspose.PSD?
  - answer: No, you do not need Photoshop to use Aspose.PSD. The library functions
      independently for PSD file manipulation.
    question: Do I need Photoshop to use Aspose.PSD?
  - answer: Absolutely! You can apply multiple effects by accessing each effect type
      similarly to how we accessed the inner shadow effect.
    question: Can I apply multiple effects to the same layer?
  - answer: Aspose.PSD is a commercial product; however, you can use a free trial
      available through Aspose.
    question: Is Aspose.PSD free?
  - answer: You can find comprehensive documentation for Aspose.PSD [here](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 如何在 Java 中添加內部陰影 PSD 圖層效果
url: /zh-hant/java/advanced-psd-layer-features-effects/add-inner-shadow-layer-effect-psd/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中添加內陰影 PSD 圖層效果

## 介紹
如果您需要以程式方式 **add inner shadow PSD**，恭喜您來對地方了。本指南將示範如何使用 Aspose.PSD for Java 為任何 Photoshop 文件添加內陰影。無論您是構建批次處理工具、自動化設計流水線，或僅是試驗圖像效果，以下步驟都能提供一個穩固、可投入生產環境的解決方案，讓您輕鬆整合至 Java 應用程式中。

**為何重要：** Aspose.PSD 支援 **超過 50 種輸入與輸出格式**，且可在 **不將整個文件載入記憶體** 的情況下操作 **多達 1 000 層**，非常適合大規模自動化。

## 快速回答
- **需要哪個函式庫？** Aspose.PSD for Java。  
- **實作需要多久？** 基本設定約 10‑15 分鐘。  
- **需要安裝 Photoshop 嗎？** 不需要，函式庫可獨立運作。  
- **可以更改陰影顏色嗎？** 可以 – `setColor` 方法接受任何 `Color`。  
- **生產環境需要授權嗎？** 需要商業授權；亦提供免費試用版。

## 什麼是 “add inner shadow psd”？
在 PSD 檔案中加入內陰影，即為圖層內部創建細緻的陰影效果，營造出深度感。**`InnerShadowEffect` 類別定義了顏色、透明度、距離、大小、角度、擴散與雜訊等參數，控制陰影在選取圖層內的呈現方式。** 這段說明以一句話概括核心概念，並簡要說明其視覺影響。

## 為何使用 Java 套用 PSD 圖層效果？
以 Java 套用 PSD 圖層效果可自動化重複的設計工作、將影像處理整合至後端服務，並在不需手動 Photoshop 操作的情況下即時產生素材。**Aspose.PSD for Java 處理上百頁文件的速度比原生 Photoshop 腳本快 2‑3 倍，且可在任何支援 JVM 的平台上執行，包括 Linux、Windows 與 macOS。** 這種效能與跨平台支援是開發者選擇 Java 進行大規模影像流水線的主要原因。

## 前置條件
在撰寫程式碼之前，請確保您已具備以下項目：

1. **Java Development Kit (JDK 11 或以上)** – 從 [Oracle 網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java** – 從 [Aspose 下載頁面](https://releases.aspose.com/psd/java/) 取得最新 JAR。  
3. **IDE** – IntelliJ IDEA、Eclipse 或 NetBeans（任一皆可）。  
4. **基本的 Java 知識** – 需熟悉類別、物件與例外處理。  
5. **範例 PSD 檔案** – 一個至少包含一個圖層的簡易 PSD，用於測試內陰影效果。

## 匯入必要套件
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layereffects.IShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```
上述匯入語句讓您取得載入 PSD、操作圖層與設定陰影效果所需的核心類別。

## 如何在 PSD 檔案中使用 Java 添加內陰影
載入來源 PSD、定位目標圖層、設定 `InnerShadowEffect`，最後將結果儲存——整個流程清晰且可封裝為方法或批次工作。`InnerShadowEffect` 類別代表可配置屬性的內陰影圖層效果，如顏色、透明度、距離與大小。**此流程包含五個核心動作：設定路徑、以效果資源開啟影像、取得圖層、套用內陰影，最後寫回磁碟。** 按照這些步驟可確保效果正確套用且資源即時釋放。

### 步驟 1：定義來源與目的目錄
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String destName = outputDir + "sample_out.psd";
```
將佔位路徑替換為您機器上的實際位置。使用絕對路徑可避免程式在不同工作目錄下執行時產生混淆。

### 步驟 2：載入含效果資源的 PSD 檔案
```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage image = (PsdImage) Image.load(sourceFile, loadOptions);
```
`PsdImage` 類別負責載入 PSD 檔案並提供圖層與效果資源的存取。`setLoadEffectsResource(true)` 可確保載入現有圖層效果，讓我們在不覆寫其他資料的前提下進行修改。

### 步驟 3：存取目標圖層
```java
try {
    Layer layer = image.getLayers()[image.getLayers().length - 1];
```
`Layer` 物件代表 PSD 文件中的單一圖層。此處我們取得文件中的 **最後一個圖層**，通常就是您想編輯的圖層。若需其他圖層，請調整索引。  
`Layer layer = image.getLayers().get(image.getLayers().size() - 1);` – 這行程式碼取得將套用內陰影的圖層物件。

### 步驟 4：設定內陰影效果
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
此程式碼 **套用內陰影** 並自訂其外觀：  
- **Color** – 設為綠色（可自行改為任何 `Color`）。  
- **Opacity** – 50 % 透明度（`128` / `255`）。  
- **Distance、Size、Angle** – 控制陰影的偏移與範圍。  
- **Spread & Noise** – 增添藝術變化。  
`InnerShadowEffect` 物件會加入圖層的混合選項，使效果成為 PSD 圖層堆疊的一部份。

### 步驟 5：儲存已修改的 PSD
```java
    image.save(destName, new PsdOptions(image));
```
`sample_out.psd` 現已包含內陰影效果。使用 `image.save(outputPath, new PsdOptions())` 可保留所有既有圖層與效果。

### 步驟 6：釋放資源
```java
} finally {
    image.dispose();
}
```
釋放 `image` 物件可釋放記憶體並防止洩漏，這在大量檔案循環處理時尤為重要。請務必將使用區塊包在 try‑with‑resources 中，或在 finally 區段呼叫 `image.dispose()`。

## 常見使用情境
- **自動化品牌流水線** – 在發佈前為商標加入一致的內陰影。  
- **動態 UI 素材產生** – 為網頁或行動應用即時產生具深度感的按鈕狀態。  
- **批次處理舊有 PSD 資料庫** – 在不開啟 Photoshop 的情況下為舊設計加入現代陰影。

## 常見問題與解決方案
| 問題 | 為何會發生 | 解決方式 |
|------|------------|----------|
| **`ArrayIndexOutOfBoundsException` 於 `getEffects()[0]`** | 目標圖層尚未附加任何效果。 | 在轉型前先透過 `layer.getBlendingOptions().addEffect(new InnerShadowEffect())` 新增 `InnerShadowEffect`。 |
| **陰影顏色未變更** | 圖層已有其他效果類型覆寫陰影。 | 確認編輯正確的效果索引，或使用 `layer.getBlendingOptions().clearEffects()` 清除既有效果後再設定。 |
| **檔案未儲存** | 目的目錄不存在或缺乏寫入權限。 | 事先建立目錄 (`new File(outputDir).mkdirs();`) 或選擇可寫入的路徑。 |

## 常見問答

**Q: 什麼是 Aspose.PSD？**  
A: Aspose.PSD 是一套 Java 函式庫，讓開發者在不安裝 Photoshop 的情況下，建立、編輯、轉換與渲染 Photoshop PSD 檔案。

**Q: 使用 Aspose.PSD 必須安裝 Photoshop 嗎？**  
A: 不需要，該函式庫可獨立操作 PSD 檔案。

**Q: 可以在同一圖層上套用多個效果嗎？**  
A: 當然可以！只要像操作內陰影一樣，依序存取並加入其他效果即可。

**Q: Aspose.PSD 是免費的嗎？**  
A: Aspose.PSD 為商業產品；不過可透過 Aspose 取得免費試用版。

**Q: 哪裡可以找到更多文件？**  
A: 您可以在 [此處](https://reference.aspose.com/psd/java/) 找到完整的 Aspose.PSD 文件說明。

## 結論
現在您已了解如何使用 Aspose.PSD for Java **add inner shadow PSD** 以及 **apply PSD layer effect**。此方法可讓您自動化高階設計調整，整合至後端服務，或為大型影像庫建構批次處理器。歡迎嘗試其他效果類型——如投影、發光、斜角等，擴充您的工具箱，打造更豐富的視覺資產。

---

**最後更新：** 2026-06-23  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [Save PSD as PNG and Apply Rendering Drop Shadow in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Add Pattern Overlay Effects in Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [How to Apply Gradient Effects in Aspose.PSD for Java](/psd/java/advanced-image-effects/add-gradient-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}