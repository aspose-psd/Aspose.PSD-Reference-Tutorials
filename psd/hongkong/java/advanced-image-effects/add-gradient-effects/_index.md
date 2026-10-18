---
date: 2026-10-18
description: 了解如何使用 Aspose.PSD 在 Java 圖像中建立徑向漸層效果。遵循此一步一步的指南，輕鬆完成整合。
keywords:
- create radial gradient java
- apply gradient overlay psd
- add radial gradient image
lastmod: 2026-10-18
linktitle: 新增漸層效果
og_description: 了解如何使用 Aspose.PSD 建立 Java 徑向漸層效果。本教學示範如何在數分鐘內新增、客製化及儲存漸層覆蓋層。
og_image_alt: Screenshot of Aspose.PSD Java code creating a radial gradient effect
og_title: 使用 Aspose.PSD 建立 Java 徑向漸層 – 步驟指南
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  headline: How to create radial gradient effects in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  name: How to create radial gradient effects in Aspose.PSD for Java
  steps:
  - name: Load the PSD file and access the gradient overlay
    text: '`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable
      loading of effect resources. `Image.load` reads the file into an `Image` object.
      In this step, we load a PSD file and retrieve the first `GradientOverlayEffect`
      from the second layer (index 1). The `loadOptions.setLoadEffec'
  - name: Verify Initial Settings
    text: Before making changes, it’s a good practice to confirm the current blend
      mode, opacity, and visibility. This helps you understand the baseline state
      of the gradient overlay.
  - name: Modify Gradient Settings
    text: Here you can customize the gradient’s color, opacity, and blend mode. The
      example changes the color to green, reduces opacity to 193 (out of 255), and
      switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode`
      values such as `Multiply`, `Screen`, or `Overlay`.
  - name: Save the Edited Image
    text: After applying your modifications, persist the changes by saving the PSD
      to a new file. This step ensures the original file remains untouched.
  - name: Verify Changes
    text: The snippet above demonstrates how to open a PSD, pull the second layer’s
      first effect (assumed to be a gradient overlay), and prepare it for modification.
  - name: Verify the original settings (optional but recommended)
    text: Before you change anything, checking the existing blend mode, opacity, and
      visibility helps you understand the baseline. The `Assert` calls in the code
      confirm that the effect is currently set to **Normal** blend mode, fully opaque,
      and visible.
  - name: Adjust gradient properties to achieve a radial style
    text: 'You can change the gradient’s color, opacity, and blend mode. For a true
      radial effect, set the gradient style: *Pro tip:* Use `Color.getGreen()` or
      any `java.awt.Color` instance to define the start color, and `gradientOverlay.setColor2(Color.getBlue())`
      for the end color.'
  - name: Save the edited PSD
    text: Calling `im.save(exportPath);` writes the modified image to disk. The saved
      file retains the radial gradient overlay and can be opened in Photoshop, previewed
      in browsers, or converted to other formats.
  type: HowTo
- questions:
  - answer: Yes. Retrieve the layer’s `BlendingOptions`, iterate through the `Effects`
      collection, and add a new `GradientOverlayEffect` for each gradient you need.
    question: Can I apply multiple gradient effects to a single image?
  - answer: Aspose.PSD provides shadows, glows, bevels, and more. Each effect appears
      in the `Effects` array and can be configured independently.
    question: What other effects can I combine with gradient overlays?
  - answer: Verify that the PSD was loaded with `setLoadEffectsResource(true)`, check
      layer visibility, and confirm you are modifying the correct effect index.
    question: How can I troubleshoot if the effects are not rendering correctly?
  - answer: Yes, you can get a free trial [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing
      information.
    question: Where can I purchase a license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
title: 如何在 Aspose.PSD for Java 中建立徑向漸層效果
url: /zh-hant/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.PSD for Java 中建立徑向漸層效果

## 簡介

在本指南中，您將學習如何使用 Aspose.PSD 函式庫 **create radial gradient java** 效果。徑向漸層非常適合在不開啟 Photoshop 的情況下，為您的 PSD 圖層添加深度、焦點或細微的光暈。完成本教學後，您將能夠載入 PSD、套用漸層覆蓋、調整其屬性，並儲存結果——全部透過 Java 程式碼完成。

## 快速回答
- **我可以達成什麼？** 在 PSD 圖層上新增、編輯與混合徑向漸層覆蓋。  
- **需要哪個函式庫？** Aspose.PSD for Java（最新版本）。  
- **需要授權嗎？** 免費試用可用於開發；商業授權則需於正式環境使用。  
- **實作需要多久？** 基本徑向漸層覆蓋大約需要 10‑15 分鐘。  
- **是否相容於 Java 8 以上？** 是，API 支援 Java 8 及更新的執行環境。

## 先決條件

在開始本教學之前，請確保已具備以下先決條件：

1. **Aspose.PSD for Java 函式庫** – 確認已下載並安裝 Aspose.PSD for Java 函式庫。您可於 [Aspose.PSD Java documentation page](https://reference.aspose.com/psd/java/) 找到函式庫與文件。  
2. **Java 開發環境** – 在您的機器上設定 Java 開發環境（JDK 8 或以上，您選擇的 IDE）。  
3. **最新的 Aspose.PSD 版本** – 從 [Aspose releases page](https://releases.aspose.com/) 下載最新版本。  
4. **支援資源** – 若遇到問題，請參考 [Aspose.PSD Support forum](https://forum.aspose.com/c/psd/34)。  
5. **授權購買** – 當您準備好投入正式環境時，可透過 [purchase page](https://purchase.aspose.com/buy) 取得授權。  

現在您已完成所有設定，讓我們繼續以下步驟說明。

## 什麼是漸層覆蓋效果？

漸層覆蓋效果會在圖層的選取區域內，以平滑的方式在兩種或多種顏色之間過渡。在 Photoshop 中，此效果可進行混合、著色與定位，以打造精緻的視覺設計。`GradientOverlayEffect` 類別是 Aspose.PSD 對此圖層樣式的表示，提供顏色定位點、不透明度、混合模式與漸層樣式等屬性。

## 如何建立徑向漸層效果

載入 PSD、定位目標圖層、調整 `GradientOverlayEffect` 屬性，最後儲存檔案。完整工作流程在載入影像後，只需四行簡潔的 Java 程式碼即可完成。

### 步驟 1：載入 PSD 檔案並存取漸層覆蓋

`PsdLoadOptions` 用於設定 PSD 檔案的載入方式，讓您能啟用效果資源的載入。`Image.load` 會將檔案讀取為 `Image` 物件。

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

在此步驟中，我們載入 PSD 檔案，並從第二層（索引 1）取得第一個 `GradientOverlayEffect`。呼叫 `loadOptions.setLoadEffectsResource(true)` 可確保效果資源可供編輯。

### 步驟 2：驗證初始設定

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

在進行變更之前，先確認目前的混合模式、不透明度與可見性是一個良好的做法。這有助於了解漸層覆蓋的基礎狀態。

### 步驟 3：修改漸層設定

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

在此您可以自訂漸層的顏色、不透明度與混合模式。範例將顏色改為綠色，不透明度降低至 193（滿分 255），並將混合模式切換為 **Lighten**。您亦可嘗試其他 `BlendMode` 值，如 `Multiply`、`Screen` 或 `Overlay`。

### 步驟 4：儲存編輯後的影像

```java
// Save the edited image
im.save(exportPath);
```

套用修改後，將 PSD 儲存為新檔案以保留變更。此步驟可確保原始檔案保持不變。

### 步驟 5：驗證變更

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

上述程式碼示範了如何開啟 PSD、取得第二層的第一個效果（假設為漸層覆蓋），並為修改做準備。

### 步驟 2：驗證原始設定（可選，但建議）

在變更任何設定之前，檢查現有的混合模式、不透明度與可見性，有助於了解基礎狀態。程式碼中的 `Assert` 呼叫確認該效果目前設定為 **Normal** 混合模式、完全不透明且可見。

### 步驟 3：調整漸層屬性以實現徑向樣式

您可以變更漸層的顏色、不透明度與混合模式。若要實現真正的徑向效果，請設定漸層樣式：

```java
gradientOverlay.setGradientStyle(GradientStyle.Radial);
gradientOverlay.setAngle(0f); // angle is ignored for radial, but required by API
gradientOverlay.setScale(100f); // 100 % fills the layer
```

*小技巧：* 使用 `Color.getGreen()` 或任何 `java.awt.Color` 例項來定義起始顏色，並使用 `gradientOverlay.setColor2(Color.getBlue())` 設定結束顏色。

### 步驟 4：儲存編輯後的 PSD

呼叫 `im.save(exportPath);` 會將修改後的影像寫入磁碟。儲存的檔案保留徑向漸層覆蓋，可在 Photoshop 中開啟、於瀏覽器預覽，或轉換為其他格式。

## 為什麼要建立徑向漸層覆蓋？

徑向漸層能為設計增添深度與焦點，使元素呈現立體或聚光效果。它們特別適用於：

- **背景填充**，將視線引向中心主題。  
- **按鈕或圖示的高亮**，需要細微光暈時。  
- **創意照片效果**，如暈影或光束。  

Aspose.PSD 支援超過 **50 種** 輸入與輸出格式，且能在不將整個文件載入記憶體的情況下處理上百頁的 PSD 檔案，讓您能在大型資產庫中自動化產生漸層。

## 常見問題與技巧

- **效果未顯示：** 確認 `gradientOverlay.isVisible()` 回傳 `true`。某些 PSD 檔案預設會隱藏效果。  
- **圖層索引錯誤：** 圖層索引從 0 開始，請再次確認目標圖層正確（`im.getLayers()[1]` 代表第二層）。  
- **不透明度型別轉換：** `setOpacity` 方法需要 `byte`，傳入 `int` 會導致編譯錯誤，請如範例中明確轉型。  
- **資源載入：** 若在存取效果時得到 `null`，請確認在載入影像前已設定 `loadOptions.setLoadEffectsResource(true)`。

## 常見問答

**Q: 我可以在單一影像上套用多個漸層效果嗎？**  
A: 可以。取得圖層的 `BlendingOptions`，遍歷 `Effects` 集合，並為每個需要的漸層新增 `GradientOverlayEffect`。

**Q: 我可以將哪些其他效果與漸層覆蓋結合？**  
A: Aspose.PSD 提供陰影、發光、斜角等多種效果。每個效果皆出現在 `Effects` 陣列中，可獨立設定。

**Q: 若效果未正確呈現，我該如何排除故障？**  
A: 確認載入 PSD 時已使用 `setLoadEffectsResource(true)`，檢查圖層可見性，並確認您正在修改正確的效果索引。

**Q: 是否提供 Aspose.PSD for Java 的試用版？**  
A: 有，您可以在此取得免費試用 [here](https://releases.aspose.com/)。

**Q: 我可以從哪裡購買 Aspose.PSD for Java 的授權？**  
A: 請造訪 [purchase page](https://purchase.aspose.com/buy) 了解授權資訊。

## 其他常見問答

**Q: 我可以以程式方式變更漸層方向嗎？**  
A: 可以。使用 `GradientOverlayEffect.setAngle(float angle)` 方法設定漸層角度（單位為度）。對於徑向漸層角度會被忽略，但仍需呼叫此方法。

**Q: Aspose.PSD 是否支援徑向漸層？**  
A: 當然支援。只要將漸層樣式設定為 `GradientStyle.Radial` 即可。

**Q: 轉換 PSD 為其他格式（例如 PNG）時，漸層覆蓋會被保留嗎？**  
A: 當您將 PSD 點陣化（例如儲存為 PNG）時，視覺上的漸層效果會保留，但效果本身會成為像素資料的一部分。

**Q: 我該如何從圖層中移除漸層覆蓋？**  
A: 取得圖層的 `BlendingOptions`，在 `Effects` 集合中找到 `GradientOverlayEffect`，然後使用 `remove(effect)` 移除。

**Q: 是否可以讓漸層變化產生動畫？**  
A: 雖然 Aspose.PSD 本身不直接支援動畫，但您可以產生一系列不同漸層參數的 PSD 檔案，然後使用其他程式庫將它們組合成影片或 GIF。

## 結論

恭喜！您已學會使用 Aspose.PSD for Java 為影像 **how to create radial gradient java** 效果。依照上述步驟，您可以以程式方式新增、修改與儲存漸層覆蓋，完整掌握 PSD 資產的創意控制。請嘗試不同的顏色、混合模式與不透明度，以達到所需的視覺效果。

---

**Last Updated:** 2026-10-18  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  








```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## 相關教學

- [使用 Aspose.PSD 於 Java 建立漸層填充 PSD – 新增漸層填充圖層](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [圖樣覆蓋 PSD：使用 Aspose.PSD for Java 新增效果](/psd/java/advanced-image-effects/add-pattern-effects/)
- [在 Java 中使用 Aspose.PSD 套用顏色覆蓋並設定不透明度](/psd/java/image-editing/color-overlay-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}