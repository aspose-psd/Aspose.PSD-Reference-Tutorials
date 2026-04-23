---
date: 2026-03-04
description: 學習如何在 Java 中建立圖形物件，並使用 Aspose.PSD 為 PSD 檔案添加對角水印。本分步指南涵蓋 Java 圖像水印函式庫的使用。
linktitle: Add Diagonal Watermark to PSD Files with Java
second_title: Aspose.PSD Java API
title: 在 Java 中建立圖形物件 – 用於 PSD 的斜向浮水印
url: /zh-hant/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中為 PSD 檔案添加斜向水印

## 簡介
在本教學中，你將 **create graphics object java** 並使用它為 PSD 檔案添加斜向水印。無論你是保護作品的設計師，還是為圖片加上品牌的行銷人員，乾淨的水印都能讓你的作品看起來更專業且更安全。我們將逐步說明每個步驟並提供清晰的解釋，讓你能快速在自己的專案中套用此技巧。

## 快速解答
- **需要什麼函式庫？** Aspose.PSD for Java（功能強大的 java 圖像水印函式庫）。  
- **本教學涵蓋的主要關鍵字是什麼？** create graphics object java。  
- **需要授權嗎？** 免費試用版可用於測試；正式環境需購買商業授權。  
- **可以更改水印文字和樣式嗎？** 可以——你可以自訂字型、顏色、不透明度與旋轉角度。  
- **支援哪些輸出格式？** 範例儲存為 PNG，但 Aspose.PSD 可匯出為 PSD、JPEG、BMP 等多種格式。

## 什麼是 Java 中的 Graphics 物件？
**Graphics** 物件代表圖像的繪圖表面。透過建立 graphics 物件，你可以取得方法，直接在位圖或 PSD 畫布上繪製文字、形狀及其他視覺元素。這正是主要關鍵字 **create graphics object java** 的核心概念。

## 為何使用 Aspose.PSD 進行水印？
Aspose.PSD 是專為 **java image watermark library** 設計的函式庫，無需 Adobe Photoshop 即可運作。它讓你完整掌控圖層、文字渲染與影像轉換，十分適合伺服器端處理或批次作業。

## 先決條件
在深入程式碼之前，請確保你已具備以下條件：

### 1. Java 開發環境
從 [Java website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載並安裝最新的 JDK。

### 2. Aspose.PSD 函式庫
從 [Aspose Downloads page](https://releases.aspose.com/psd/java/) 下載函式庫。透過 Maven、Gradle 或手動加入 classpath 的方式將 JAR 加入專案。

### 3. 基本的 Java 知識
熟悉類別、物件與檔案 I/O 能讓你更順利跟隨教學。

### 4. IDE 設定
使用 IntelliJ IDEA、Eclipse 或 NetBeans 以獲得舒適的編程體驗。

## 匯入套件
要操作 PSD 檔案，請匯入所需的 Aspose.PSD 類別：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

現在我們已完成先決條件並匯入必要的套件，接下來一步步說明如何為 PSD 檔案添加斜向水印。

## 步驟 1：設定目錄
```java
String dataDir = "Your Document Directory";
```
將 `"Your Document Directory"` 替換為存放 PSD 原始檔案的資料夾路徑。

## 步驟 2：載入 PSD 檔案
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
`Image.load` 方法讀取檔案，並將其轉型為 `PsdImage`，以便使用 PSD 專屬功能。

## 步驟 3：建立 Graphics 物件
```java
Graphics graphics = new Graphics(psdImage);
```
此處我們 **create graphics object java**——即將在其上繪製水印的畫布。

## 步驟 4：為水印建立字型
```java
Font font = new Font("Arial", 20.0f);
```
選擇任意已安裝的字型；字型大小決定水印的顯眼程度。

## 步驟 5：為水印建立筆刷
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
`alpha` 值（第一個參數）設定透明度。alpha 為 50 時，呈現細膩、半透明的效果。

## 步驟 6：設定變換矩陣
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
我們將繪圖表面繞圖像中心旋轉 45°，產生斜向效果。

## 步驟 7：定義字串對齊方式
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
置中對齊可確保水印在旋轉後的矩形中居中顯示。

## 步驟 8：繪製水印
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
將 `"Some watermark text"` 替換為你的品牌名稱或版權聲明。矩形區域決定文字的繪製位置。

## 步驟 9：儲存影像
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
輸出會儲存為 PNG，但你也可以選擇 Aspose.PSD 支援的任何格式。

## 常見使用情境
- **品牌保護：** 添加半透明標誌以防止未經授權的再使用。  
- **批次處理：** 在伺服器上自動為大量影像庫加上水印。  
- **創意預覽：** 向客戶展示帶水印的草稿，同時保留原始檔案不受影響。

## 故障排除與技巧
- **透明度未顯示？** 提高 alpha 值（例如 `100`）以加強水印。  
- **水印偏離中心？** 確認旋轉點使用圖像寬度/高度的精確除半。  
- **效能顧慮：** 在迴圈處理多張影像時，重複使用同一個 `Graphics` 物件。

## 常見問答
### 什麼是 Aspose.PSD？
Aspose.PSD 是一套 Java 函式庫，可在不需要 Adobe Photoshop 的情況下處理與操作 PSD 檔案。

### 我可以使用其他字型來做水印嗎？
可以，你可以選擇系統中已安裝的任何字型來製作水印。

### 有沒有辦法自訂水印的透明度？
當然可以！你可以在 SolidBrush 中調整 alpha 值以改變透明度。

### 我可以加入多個水印嗎？
可以，你可以多次呼叫 `drawString` 方法，並使用不同參數來加入多個水印。

### 在哪裡可以取得更多關於 Aspose.PSD 的資訊？
你可以在此處查看文件說明 [here](https://reference.aspose.com/psd/java/)。

---

**最後更新：** 2026-03-04  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}