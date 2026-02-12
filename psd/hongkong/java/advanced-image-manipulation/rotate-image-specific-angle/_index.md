---
date: 2026-02-12
description: 學習如何在 Java 中使用 Aspose.PSD 以特定角度旋轉圖像。本指南展示如何旋轉圖像、按度數旋轉圖像以及處理背景顏色。
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 按特定角度旋轉圖像
url: /zh-hant/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在特定角度使用 Aspose.PSD for Java 旋轉圖像

## 簡介

如果您需要在 Java 應用程式中以程式方式 **如何旋轉圖像**，Aspose.PSD for Java 提供了乾淨且高效能的 API，負責繁重的運算。無論您是在建構照片編輯器、產生縮圖，或是為 Web 服務準備資源，精確角度的圖像旋轉都是常見需求。本教學將完整說明從載入 PSD 檔案到儲存旋轉結果的每一步，並強調快取與背景處理等最佳實踐。

## 快速答覆
- **哪個程式庫最適合在 Java 中旋轉圖像？** Aspose.PSD for Java。  
- **我可以以任意角度旋轉嗎？** 是的，`rotate` 方法接受 `float` 角度（正值或負值）。  
- **開發時需要授權嗎？** 免費試用可用於測試；正式環境需購買授權。  
- **支援哪些圖像格式？** PSD、JPEG、PNG、TIFF、GIF、BMP 等多種格式。  
- **如何為空白區域設定背景顏色？** 傳遞 `Color` 實例給 `rotate` 方法。

## 什麼是 Java 中的圖像旋轉？

圖像旋轉是指將像素矩陣繞著一個樞紐點（通常是中心）依指定角度旋轉。在 Java 中，您可以使用 `Graphics2D` 手動實作，但 Aspose.PSD 會抽象化數學運算、處理不同的色深，並在處理 PSD 檔案時保留圖層資訊。

## 為什麼使用 Aspose.PSD 來旋轉圖像？

- **Precision:** 以任意小數度數旋轉且不失真。  
- **Performance:** 內建快取 (`image.cacheData()`) 可加速大型檔案。  
- **Background Control:** 指定背景顏色以填補旋轉後產生的空白。  
- **Format Flexibility:** 載入 PSD，輸出 JPEG、PNG 或任何支援的格式。

## 前置條件

在開始之前，請確保您具備以下項目：

1. **Java Development Kit (JDK 8 or later)** – a working Java IDE or command‑line setup.  
2. **Aspose.PSD for Java** – download the latest JAR from the [Aspose.PSD Java page](https://reference.aspose.com/psd/java/).  
3. **Sample PSD file** – e.g., `sample.psd` placed in a folder you can reference from your code.

## 匯入套件

首先匯入我們需要的類別。無論您選擇的旋轉角度為何，這些匯入都保持不變。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 步驟說明

### 步驟 1：定義文件目錄

設定保存來源 PSD 與輸出結果的資料夾路徑。

```java
String dataDir = "Your Document Directory";
```

> **專業提示：** 使用絕對路徑或 `System.getProperty("user.dir")` 以避免相對路徑的問題。

### 步驟 2：指定來源與目標檔案路徑

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

您可以依需求將 `destName` 改為任何支援的副檔名（`.png`、`.tiff` 等）。

### 步驟 3：載入圖像

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` 會自動偵測檔案格式，並回傳具體的 `RasterImage` 供點陣圖操作使用。

### 步驟 4：快取圖像資料（可選但建議）

```java
if (!image.isCached())
{
    image.cacheData();
}
```

快取會將圖像像素存入記憶體，提升後續轉換的速度——對大型 PSD 檔案特別有幫助。

### 步驟 5：旋轉圖像

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – 以度數表示的旋轉角度（float）。變更此值即可旋轉任意角度，例如 `-45f` 代表逆時針。  
- **true** – 在擴展畫布以容納旋轉後圖像時，保持原始長寬比。  
- **Color.getRed()** – 旋轉後產生的空白角落的背景顏色。可依需求改為 `Color.getWhite()` 或其他自訂顏色。

#### 以度數旋轉圖像（Java）

`rotate` 方法接受任何浮點值，因此您可以 **以度數旋轉圖像**，例如 `30f`、`90f` 或 `-15f`。正值為順時針旋轉，負值為逆時針旋轉。

#### 使用 Aspose.PSD 以特定角度旋轉圖像

因為此方法使用 `float`，您可以指定 **特定角度旋轉圖像**，如 `22.5f`，以在圖形設計工作流程中取得精確控制。

#### Rotate Image Java 範例摘要

上述所有步驟展示了一個完整的 **rotate image java** 工作流程——從載入檔案到儲存旋轉後的輸出。

### 步驟 6：儲存結果

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` 讓您控制品質、壓縮以及其他 JPEG 專屬設定。若需無損輸出，可改用 `PngOptions`。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| **旋轉後出現空白角落** | 未提供背景顏色 | 傳遞 `Color`（例如 `Color.getWhite()`）給 `rotate`。 |
| **大型 PSD 檔案記憶體不足錯誤** | 未快取圖像 | 在處理前呼叫 `image.cacheData()`。 |
| **角度方向不正確** | 負角度與正角度混淆 | 使用負值進行順時針旋轉（或根據座標系統相反）。 |
| **變更未儲存** | 忘記呼叫 `save` | 確保在旋轉後執行 `image.save(...)`。 |

## 常見問答

**Q: 可以使用 Aspose.PSD for Java 旋轉帶透明度的圖像嗎？**  
A: 可以。此函式庫會保留 alpha 通道；若想要透明的角落，只需不要指定不透明的背景顏色。

**Q: 支援的圖像格式在旋轉時有任何限制嗎？**  
A: 沒有。Aspose.PSD 支援 PSD、JPEG、PNG、TIFF、GIF、BMP、JPEG2000、WMF、EMF 等多種格式。

**Q: 可以使用負角度旋轉圖像嗎？**  
A: 當然可以。傳遞負的 float 給 `rotate`（例如 `-30f`）即可順時針旋轉。

**Q: Aspose.PSD 在旋轉時提供即時圖像預覽嗎？**  
A: 此 API 僅為伺服器端使用。若需即時預覽，請將旋轉後的位圖整合至 UI 框架（Swing、JavaFX）並重新刷新畫面。

**Q: 有 Aspose.PSD 的社群論壇可以求助嗎？**  
A: 有，請前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 提問與交流。

## 結論

您現在已了解 **如何旋轉圖像** 檔案於特定角度，並使用 Aspose.PSD for Java 完成。透過快取、背景顏色控制與彈性輸出選項，您可以將精確的旋轉功能整合至任何基於 Java 的影像工作流程中。

---

**最後更新：** 2026-02-12  
**測試環境：** Aspose.PSD for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}