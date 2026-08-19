---
date: 2026-04-03
description: 學習如何使用 Aspose.PSD for Java 透過扁平化圖層來減少 PSD 檔案大小。此一步一步的指南展示如何快速扁平化 PSD
  檔案。
keywords:
- reduce psd file size
- how to flatten psd
- flatten visible layers psd
linktitle: 透過合併圖層減少 PSD 檔案大小 – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: 透過平面化圖層減少 PSD 檔案大小 – Aspose.PSD Java
url: /zh-hant/java/psd-layer-management-effects/flatten-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 透過合併圖層減少 PSD 檔案大小 – Aspose.PSD Java

## 介紹

如果你曾經打開 Photoshop 檔案並想知道如何 **reduce PSD file size**，合併圖層是最有效的技巧之一。使用 Aspose.PSD for Java，你可以以程式方式將整個 PSD 合併，或只合併你選擇的圖層，讓你在不犧牲視覺品質的前提下，細緻控制檔案大小。在本教學中，我們將示範兩種做法——合併整張影像以及合併特定圖層——讓你快速縮小 PSD 檔案並保持工作流程順暢。

## 快速解答
- **flattening** 做什麼？它會將可見圖層合併成單一背景圖層，移除圖層資訊，通常能減少檔案大小。  
- **Can I flatten only selected layers?** 是的，你可以合併特定圖層，同時保留其他圖層不變。  
- **Do I need a license?** 免費試用版可用於開發；商業授權則需於正式環境使用。  
- **Which Java version is required?** JDK 8 或以上。  
- **Will flattening affect image quality?** 不會，視覺外觀保持不變，僅圖層結構會改變。

## 什麼是「reduce PSD file size」？
減少 PSD 檔案大小是指移除不必要的資料——例如多餘的圖層、隱藏的通道或過多的中繼資料——使檔案變得更輕盈、載入、分享或處理速度更快。合併圖層是一種常見的做法，因為它會捨棄各個圖層物件，同時保留最終的合成影像。

## 為什麼要使用 Aspose.PSD for Java 合併圖層？
- **Automation:** 無需手動開啟 Photoshop；可直接整合至 Java 應用程式。  
- **Precision:** 可選擇合併整個文件或僅合併可見圖層 (`flattenImage`) 或合併選取的圖層 (`mergeLayers`)。  
- **Performance:** 較小的檔案載入更快，且在後續處理時佔用較少記憶體。  
- **Cross‑platform:** 可在任何支援 Java 的作業系統上執行。

## 前置條件

1. **Java Development Kit (JDK)：** 已安裝 JDK 8 或更新版本。  
2. **Aspose.PSD for Java：** 從 [here](https://releases.aspose.com/psd/java/) 下載程式庫。  
3. **IDE：** IntelliJ IDEA、Eclipse 或任何相容 Java 的開發環境。  
4. **Basic Java knowledge：** 有助於理解，但非執行步驟的必要條件。  
5. **Sample PSD：** 含多個圖層的檔案（此處使用 `ThreeRegularLayersSemiTransparent.psd`）。

現在所有環境已備妥，讓我們深入程式碼。

## 匯入套件

首先，匯入必要的 Aspose.PSD 類別：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

這些匯入讓我們能載入 PSD 檔案、操作圖層，並儲存結果。

## 步驟 1：合併整個 PSD 影像

合併整張影像是最快速 **reduce PSD file size** 的方法，因為它會移除所有單獨的圖層資料。

### 1.1 載入 PSD 檔案

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 1.2 合併影像

```java
im.flattenImage();
```

### 1.3 儲存合併後的影像

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

你的新檔案現在只包含單一背景圖層，通常會使 PSD 檔案變得更小。

## 步驟 2：合併特定圖層（如何選擇性合併 PSD）

有時你只想 **flatten visible layers** 或合併部分圖層，同時保留其他圖層可編輯。

### 2.1 再次載入 PSD 檔案

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 2.2 識別並選取圖層

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

### 2.3 合併圖層

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

### 2.4 用合併後的圖層取代現有圖層

```java
img.setLayers(new Layer[]{layer2});
```

### 2.5 儲存更新後的 PSD 檔案

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

現在 PSD 只包含合併後的圖層，達成減少檔案大小的同時，保留了你想保留的圖層。

## 常見問題與技巧

- **Backup before flattening：** 圖層一旦合併就無法復原，請保留原始 PSD 的備份。  
- **Visibility matters：** `flattenImage()` 只會合併 *可見* 圖層。請隱藏任何不想包含的圖層。  
- **Memory usage：** 大型 PSD 可能佔用大量記憶體；建議在具備足夠記憶體的機器上處理。  
- **Blending modes：** 合併時會遵守每個圖層的混合模式，視覺結果與 Photoshop 中相同。

## 常見問答

**Q: 我可以在 Aspose.PSD 中復原圖層合併嗎？**  
A: 不行，合併是不可逆的。請務必保留原始檔案的備份。

**Q: 是否可以只合併可見圖層？**  
A: 可以。`flattenImage()` 會遵守圖層可見性，請在呼叫方法前隱藏不想合併的圖層。

**Q: 合併圖層會減少檔案大小嗎？**  
A: 通常會。移除圖層資料與中繼資料通常會使 PSD 更小，雖然具體減少幅度取決於內容。

**Q: 我可以合併具有不同混合模式的圖層嗎？**  
A: 當然可以。Aspose.PSD 在合併圖層時會保留各自混合模式所產生的視覺效果。

**Q: 若嘗試合併非相鄰的圖層會發生什麼？**  
A: Aspose.PSD 允許合併任意圖層，不論其在堆疊中的順序；結果會呈現合併後的外觀。

**最後更新：** 2026-04-03  
**測試環境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}