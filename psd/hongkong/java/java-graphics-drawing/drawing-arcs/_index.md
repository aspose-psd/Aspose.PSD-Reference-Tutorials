---
date: 2026-01-17
description: 學習如何使用 Aspose.PSD for Java 在 Java 圖形中繪製弧形。逐步教學，附有程式碼範例，適用於圖形應用程式。
linktitle: Java Graphics Draw Arc with Aspose.PSD
second_title: Aspose.PSD Java API
title: Java 圖形使用 Aspose.PSD 繪製弧形 – 步驟指南
url: /zh-hant/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD 的 Java 圖形繪製弧線

## 介紹
在本教學中，您將了解如何使用 Aspose.PSD for Java 函式庫 **java graphics draw arc**。以程式方式繪製弧線對於自訂 UI 元件、資料視覺化或任何需要精確曲線控制的圖形都非常方便。我們將逐步說明從專案設定、弧線繪製到結果儲存的每個步驟，讓您立即在 Java 應用程式中加入此功能。

## 快速回答
- **哪個函式庫可以讓 Java 輕鬆繪製弧線？** Aspose.PSD for Java.  
- **開發時需要授權嗎？** 免費試用版可用於測試；正式環境需購買授權。  
- **支援哪些輸出格式？** BMP、PNG、JPEG、TIFF、GIF 等。  
- **可以調整弧線的粗細或顏色嗎？** 可以——調整 `Pen` 物件的屬性。  
- **程式碼是否相容於 Java 8 以上？** 完全相容，API 目標為 Java 8 及以上版本。

## 什麼是「java graphics draw arc」？
此詞語指的是使用 Java 程式碼在圖形畫布上繪製曲線段（弧線）。透過 Aspose.PSD，您可以取得高階的 `Graphics` 類別，簡化繪圖操作，並在背後自動處理顏色管理、抗鋸齒與檔案匯出。

## 為何使用 Aspose.PSD 繪製弧線？
- **完整的 PSD 支援** – 無需安裝 Photoshop 即可建立或編輯 Photoshop 檔案。  
- **豐富的繪圖 API** – 如 `drawArc` 等方法讓您在一次呼叫中指定尺寸、角度與樣式。  
- **跨格式匯出** – 只需幾行程式碼即可將弧線儲存為 BMP、PNG、JPEG 等格式。  
- **效能導向** – 為大尺寸影像與批次處理進行最佳化。

## 前置條件
1. **Java 開發環境** – 安裝 Java（JDK 8 或更新版本）。可從 [Oracle 的網站](https://www.oracle.com/java/) 下載。  
2. **Aspose.PSD for Java** – 從[下載頁面](https://releases.aspose.com/psd/java/)取得函式庫，並將 JAR 加入專案的 classpath。

## 匯入套件
首先，將必要的 Aspose.PSD 類別匯入作用域：

```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

這些匯入讓您可以使用顏色定義、繪圖工具、影像容器以及檔案儲存選項。

## 步驟說明

### 步驟 1：設定 Java 專案
建立新的 Maven 或 Gradle 專案，加入 Aspose.PSD JAR，並確認 IDE 能正確解析匯入且沒有錯誤。

### 步驟 2：初始化影像與圖形物件
建立空白的 `PsdImage` 畫布與 `Graphics` 實例以進行繪圖：

```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```

將 `"Your Document Directory"` 替換為您希望儲存輸出檔案的資料夾路徑。

### 步驟 3：定義弧線參數
指定形塑弧線的尺寸與角度：

```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```

請自行調整這些數值，以符合您需要的視覺風格。

### 步驟 4：繪製並儲存弧線
使用 `drawArc` 方法，然後匯出影像：

```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

此程式碼會在黃色背景上繪製黑色弧線，並將結果寫入 `Arc.bmp`。若想使用其他格式或品質，可修改 `outputPath` 與 `BmpOptions`。

## 常見問題與解決方案
- **檔案未找到錯誤** – 確認 `dataDir` 以路徑分隔符 (`/` 或 `\\`) 結尾，且目錄已存在。  
- **弧線顯示為直線** – 確認 `width` 與 `height` 大於零，且 `sweepAngle` 不是 360° 的倍數（那會繪製完整橢圓）。  
- **顏色未套用** – 使用 `new Pen(Color.getRed())` 或設定 `pen.setWidth(2)` 以更明顯看到效果。

## 常見問答

**Q: Aspose.PSD for Java 能處理除弧線之外的其他形狀嗎？**  
A: 可以，它支援矩形、橢圓、直線，以及透過相同的 `Graphics` API 繪製自訂路徑。

**Q: 如何變更弧線的粗細或顏色？**  
A: 建立具有指定 `Color` 與 `Width` 的 `Pen`（例如 `new Pen(Color.getBlue(), 3)`），然後將其傳入 `drawArc`。

**Q: 能否將弧線匯出為 BMP 以外的格式？**  
A: 當然可以。使用 `PngOptions`、`JpegOptions`、`TiffOptions` 等取代 `BmpOptions`。

**Q: 在哪裡可以找到更多範例與支援？**  
A: 前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)取得社群協助、官方文件與程式碼範例。

## 結論
現在您已擁有一個完整、可投入生產的範例，示範如何使用 Aspose.PSD for Java **java graphics draw arc**。只要調整參數、筆刷設定與輸出選項，即可將自訂弧線整合至任何基於 Java 的圖形工作流程。

---

**最後更新：** 2026-01-17  
**測試環境：** Aspose.PSD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}