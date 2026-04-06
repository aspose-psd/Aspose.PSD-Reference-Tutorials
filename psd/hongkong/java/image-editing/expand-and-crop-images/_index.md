---
date: 2026-01-07
description: 學習如何使用 Aspose.PSD for Java 進行 Java 圖片裁切。一步一步的圖像裁切、調整尺寸及將 PSD 轉換為 JPEG
  的指南。
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: 裁剪圖像 Java - 使用 Aspose.PSD for Java 進行擴展與裁剪
url: /zh-hant/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 裁剪圖像 Java：使用 Aspose.PSD for Java 擴展與裁剪圖像

## 簡介

在本教學中，您將學會如何使用 Aspose.PSD 程式庫 **crop image java**。無論您需要擴展畫布、裁剪不需要的邊緣，或是將 PSD 檔案轉換為 JPEG，以下步驟都會引導您完成乾淨且可重複的流程。我們將說明前置條件、匯入語句，以及每個程式碼步驟的清晰解說，讓您能將此技術應用於實務專案。

## 快速答覆
- **什麼程式庫處理 crop image java？** Aspose.PSD for Java.  
- **開發是否需要授權？** 免費試用可用於測試；正式環境需商業授權。  
- **在裁剪時能將 PSD 轉換為 JPEG 嗎？** 可以，使用 `JpegOptions` 搭配裁剪矩形。  
- **支援 Java 8 嗎？** Aspose.PSD 支援 Java 8 及更新版本。  
- **實作需要多長時間？** 基本裁剪操作通常在 10 分鐘以內完成。  

## 什麼是「crop image java」？

在 Java 中裁剪圖像是指選取來源圖片的矩形區域，並捨棄其餘部分。使用 Aspose.PSD，您可以透過 `Rectangle` 物件定義此區域，然後將結果儲存為不同格式（例如 JPEG）。

## 為什麼使用 Aspose.PSD for Java 進行圖像裁剪？

- **完整的 PSD 支援** – 直接操作分層 PSD 檔案，無需先轉換。  
- **高效能點陣處理** – 大圖像的記憶體使用更有效率。  
- **內建轉換** – 在裁剪或擴展畫布的同時，輕鬆匯出為 JPEG、PNG、BMP 等格式。  
- **跨平台** – 在任何支援 Java 的系統上皆可執行。  

## 先決條件

在開始之前，請確保您已具備：

1. **Java Development Kit (JDK)** – 已安裝 Java 8 或更新版本。  
2. **Aspose.PSD for Java** – 從官方網站 **[此處](https://releases.aspose.com/psd/java/)** 下載程式庫。  

> **專業提示：** 將 Aspose.PSD JAR 加入專案的 classpath 或 Maven/Gradle 相依性，以避免 `ClassNotFoundException`。

## 匯入套件

將所需的匯入語句加入您的 Java 原始檔。這些類別讓您能存取圖像載入、點陣操作、矩形定義與 JPEG 匯出選項。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 步驟 1：設定文件目錄

指定包含來源 PSD 檔案的資料夾。將佔位符替換為您機器上的實際路徑。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：指定來源與目標路徑

定義從哪裡讀取 PSD，以及將裁剪後的 JPEG 寫入何處。

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## 步驟 3：載入並快取圖像

將 PSD 載入 `RasterImage` 物件。快取可提升後續操作（如裁剪）的效能。

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## 步驟 4：建立裁剪矩形

建立描述您想保留區域的 `Rectangle`。座標可為負值，以 **擴展** 畫布後再裁剪，這在需要在原始圖像周圍添加邊框時非常有用。

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **為什麼使用負座標？**  
> 負的 X/Y 值會將裁剪區域向左/上移動，等同於在原始內容四周加入空白（擴展）後再進行最終裁剪。

## 步驟 5：儲存裁剪後的圖像

最後，使用 `JpegOptions` 儲存結果圖像。此步驟同時示範 **convert psd jpeg** 時套用裁剪矩形的做法。

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **結果：** `jpeg_out.jpg` 現在包含一張 300 × 300 像素的圖像，該圖像在每側先擴展了 200 像素，然後依照定義的矩形進行裁剪。

恭喜！您已成功執行 **java image cropping**，同時擴展畫布並將 PSD 檔案轉換為 JPEG——全部只需幾行簡潔的程式碼。

## 常見使用情境

- **為網站準備資產** – 在上傳前裁剪與調整螢幕截圖或設計稿的尺寸。  
- **產生縮圖** – 從大型 PSD 中擷取特定區域作為預覽。  
- **自動批次處理** – 迭代資料夾中的 PSD 檔案，對每個檔案套用相同的裁剪矩形。  

## 故障排除與技巧

| 問題 | 建議解決方案 |
|------|--------------|
| `OutOfMemoryError` when loading large PSDs | 於早期呼叫 `rasterImage.cacheData()`，並考慮增加 JVM 堆積大小 (`-Xmx`)。 |
| Cropped area is off‑center | 核對矩形的 X/Y 偏移值；記得負值會擴展畫布。 |
| Output JPEG looks blurry | 調整 `JpegOptions` 的品質設定（例如 `new JpegOptions { Quality = 90 }`）。 |

## 常見問題

### Q1: Aspose.PSD 是否相容於不同的 Java 版本？

A1: 是的，Aspose.PSD 支援多種 Java 版本，確保與廣泛的開發環境相容。

### Q2: 我可以在商業專案中使用 Aspose.PSD 嗎？

A2: 當然可以，Aspose.PSD 提供商業授權，允許在個人與商業專案中使用。

### Q3: 支援的圖像檔案格式有什麼限制嗎？

A3: Aspose.PSD 支援多種圖像檔案格式，包括 PSD、JPEG、PNG 等。完整清單請參考[文件說明](https://reference.aspose.com/psd/java/)。

### Q4: 如何取得 Aspose.PSD 相關問題的支援？

A4: 請前往[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)尋求社群或官方支援團隊的協助。

### Q5: 是否提供免費試用？

A5: 有的，您可以在此[下載](https://releases.aspose.com/)免費試用 Aspose.PSD。

---

**最後更新：** 2026-01-07  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}