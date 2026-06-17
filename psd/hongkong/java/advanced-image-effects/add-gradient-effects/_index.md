---
date: 2026-04-08
description: 學習如何使用 Aspose.PSD 在 Java 圖像中建立徑向漸層效果。請遵循此一步一步的指南，以實現無縫整合。
keywords:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
linktitle: 新增漸層效果
second_title: Aspose.PSD Java API
title: 如何在 Aspose.PSD for Java 中建立徑向漸層效果
url: /zh-hant/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.PSD for Java 中建立徑向漸層效果

## 簡介

歡迎閱讀本教學，內容是 **如何建立徑向漸層** 效果於 Aspose.PSD for Java！如果您想以驚豔的漸層覆蓋提升影像效果，您來對地方了。本指南將帶您使用 Aspose.PSD——一個功能強大的 Java 圖像處理函式庫，逐步完成整個流程。完成本教學後，您將能熟練地以程式方式加入、客製化並儲存徑向漸層覆蓋。

## 快速解答
- **我可以達成什麼？** 在 PSD 圖層上新增、編輯與混合徑向漸層覆蓋。  
- **需要哪個函式庫？** Aspose.PSD for Java（最新版本）。  
- **需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買商業授權。  
- **實作需要多久？** 基本的徑向漸層覆蓋大約 10‑15 分鐘即可完成。  
- **是否相容於 Java 8+？** 是，API 支援 Java 8 及更新的執行環境。

## 先決條件

在開始本教學之前，請確保已具備以下先決條件：

1. **Aspose.PSD for Java Library** – 確認已下載並安裝 Aspose.PSD for Java 函式庫。您可於 [here](https://reference.aspose.com/psd/java/) 取得函式庫與文件。  
2. **Java Development Environment** – 在您的機器上設置 Java 開發環境（JDK 8 或以上，您慣用的 IDE）。

現在環境已備妥，讓我們繼續以下的步驟說明。

## 匯入套件

先在 Java 專案中匯入必要的套件，確保您可以使用 Aspose.PSD 的功能。以下是一個基本範例：

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

## 什麼是漸層覆蓋效果？

**漸層覆蓋效果** 是一種圖層樣式，會在選取區域內以兩種或多種顏色之間的平滑過渡進行繪製。在 Photoshop（因此在 PSD 檔案中）此效果可調整混合模式、顏色與位置，以創造精緻的視覺設計。Aspose.PSD 透過 `GradientOverlayEffect` 類別公開此效果，讓您能以程式方式讀取與修改其屬性。

## 如何建立徑向漸層效果

以下我們將實作步驟拆解為清晰的編號說明。每一步皆包含簡短說明，並附上原始程式碼區塊（保持不變）。

### 步驟 1：載入 PSD 檔案並存取漸層覆蓋

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

在此步驟，我們載入 PSD 檔案，並從第二層（索引 1）取得第一個 `GradientOverlayEffect`。`loadOptions.setLoadEffectsResource(true)` 的呼叫確保效果資源可供編輯。

### 步驟 2：驗證初始設定

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

在進行變更前，先確認目前的混合模式、透明度與可見性是個好習慣。這有助於您了解漸層覆蓋的基礎狀態。

### 步驟 3：修改漸層設定

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

此處您可以自訂漸層的顏色、透明度與混合模式。範例將顏色改為綠色，將透明度降至 193（255 為滿值），並將混合模式切換為 **Lighten**。您也可以嘗試其他 `BlendMode` 值，例如 `Multiply`、`Screen` 或 `Overlay`。

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

重新載入已儲存的檔案（或根據工作流程載入原始檔），再次檢查漸層覆蓋，以確認變更已正確套用。

## 為什麼要建立徑向漸層覆蓋？

徑向漸層能為設計增添深度與焦點，使元素呈現立體感或聚光效果。它們特別適用於：

- **背景填充**，將視線引向中心主題。  
- **按鈕或圖示的高亮**，提供微妙的光暈。  
- **創意相片效果**，如暈影或光束。

使用 Aspose.PSD 可自動化大量檔案的此類效果，為您節省大量手動 Photoshop 的時間。

## 常見問題與技巧

- **效果未顯示：** 確認 `gradientOverlay.isVisible()` 回傳 `true`。部分 PSD 檔案預設隱藏效果。  
- **圖層索引錯誤：** 圖層索引從 0 開始，請再次確認您定位的圖層正確（`im.getLayers()[1]` 代表第二層）。  
- **透明度型別轉換：** `setOpacity` 方法需要 `byte` 型別。傳入 `int` 會導致編譯錯誤，請如範例中明確轉型。  
- **資源載入：** 若存取效果時得到 `null`，請確保在載入影像前已設定 `loadOptions.setLoadEffectsResource(true)`。

## 常見問答

### Q1：我可以在單一影像上套用多個漸層效果嗎？

A1：可以，您只需對每個效果重複修改步驟即可。

### Q2：還可以將哪些其他效果與漸層覆蓋結合使用？

A2：Aspose.PSD 提供多種效果，包括陰影、發光等。請參考文件以取得更多選項。

### Q3：如果效果未正確呈現，我該如何排除問題？

A3：請檢查文件與社群論壇的說明，網址為 [Aspose.PSD Support](https://forum.aspose.com/c/psd/34)。

### Q4：Aspose.PSD for Java 有提供試用版嗎？

A4：有，您可在 [here](https://releases.aspose.com/) 取得免費試用。

### Q5：我該從哪裡購買 Aspose.PSD for Java 的授權？

A5：請前往 [purchase page](https://purchase.aspose.com/buy) 了解授權資訊。

## 其他常見問答

**Q：我可以以程式方式變更漸層方向嗎？**  
A：可以。使用 `GradientOverlayEffect.setAngle(float angle)` 方法設定以度數表示的漸層角度。

**Q：Aspose.PSD 支援徑向漸層嗎？**  
A：絕對支援。透過 `GradientOverlayEffect` 的屬性將漸層樣式設為 `GradientStyle.Radial` 即可。

**Q：將 PSD 轉換為其他格式（例如 PNG）時，漸層覆蓋會被保留嗎？**  
A：在將 PSD 點陣化（例如儲存為 PNG）時，漸層覆蓋的視覺結果會保留下來，但效果本身會成為像素資料的一部份。

**Q：我要如何從圖層中移除漸層覆蓋？**  
A：取得該圖層的 `BlendingOptions`，在 `Effects` 集合中找到 `GradientOverlayEffect`，然後使用 `remove(effect)` 移除。

**Q：能否為漸層變化製作動畫？**  
A：雖然 Aspose.PSD 本身不直接支援動畫，但您可以產生一系列不同漸層參數的 PSD 檔案，之後再使用其他程式庫將它們合成影片或 GIF。

## 結論

恭喜您！您已學會 **如何建立徑向漸層** 效果於 Aspose.PSD for Java。依循上述步驟，您可以以程式方式新增、修改與儲存漸層覆蓋，完整掌控 PSD 資產的創意表現。請盡情嘗試不同的顏色、混合模式與透明度，打造出符合需求的視覺衝擊。

---

**最後更新：** 2026-04-08  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}