---
date: 2026-01-17
description: 學習如何在 Java 中使用 Aspose.PSD 建立貝塞爾曲線圖像。本分步指南涵蓋繪製貝塞爾曲線的 Java 技術、筆寬設定以及匯出結果。
linktitle: How to Create Bezier Curve Image in Java
second_title: Aspose.PSD Java API
title: 如何在 Java 中建立貝塞爾曲線圖像
url: /zh-hant/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中建立貝塞爾曲線圖像

## 介紹
如果您需要為 Java 桌面或伺服器端應用程式 **建立貝塞爾曲線圖像**，Aspose.PSD for Java 可讓此工作變得輕鬆無憂。在本教學中，我們將逐步說明如何繪製平滑的貝塞爾曲線、調整畫筆寬度，並將結果儲存為點陣圖。完成後，您將熟悉 `drawBezier()` 方法，並能在任何 Java 專案中整合向量風格的圖形。

## 快速解答
- **哪個函式庫最適合在 Java 中繪製曲線？** Aspose.PSD for Java 提供完整的圖形 API。  
- **建立基本貝塞爾曲線圖像需要多久？** 通常在設定好 SDK 後不到 10 分鐘即可完成。  
- **支援哪些圖像格式匯出？** BMP、PNG、JPEG、TIFF 等多種格式。  
- **我可以更改曲線的畫筆寬度嗎？** 可以 – `Pen` 建構子允許您指定任意寬度。  
- **正式環境需要授權嗎？** 非評估部署必須購買商業授權。

## 什麼是「建立貝塞爾曲線圖像」？
建立貝塞爾曲線圖像是指產生一張包含數學定義曲線的點陣圖。曲線由起點、兩個控制點與終點構成，讓您能製作平滑且可縮放的形狀，無論尺寸大小皆保持良好外觀。

## 為什麼使用 Aspose.PSD for Java？
- **豐富的圖形基元** – 可繪製線條、形狀與曲線，無需處理低階像素操作。  
- **跨平台** – 可在任何支援 Java 的作業系統上執行。  
- **高解析度支援** – 能處理大型畫布而不會佔用過多記憶體。  
- **輕鬆匯出** – 只需一行程式碼即可在 BMP、PNG、JPEG、TIFF 等格式間切換。

## 前置條件
在開始之前，請確保您已具備以下條件：

1. **Java Development Kit (JDK)** – 任意近期版本（8 版或更新）。  
2. **Aspose.PSD for Java JAR** – 從 [here](https://releases.aspose.com/psd/java/) 下載，並加入專案的 classpath。  
3. **IDE** – Eclipse、IntelliJ IDEA 或您偏好的任何編輯器，並已配置 JDK。

## 匯入套件
在深入實作之前，先匯入必要的 Aspose.PSD 類別：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## 步驟說明

### 步驟 1：建立圖像實例
首先，您需要建立 `PsdImage` 類別的實例，該類別在記憶體中代表一個 PSD 圖像。

```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```

*說明*：`PsdImage` 以 **100 × 100 像素** 的寬度與高度建立 – 您可以提升這些數值以取得更高解析度的輸出。

### 步驟 2：初始化圖形上下文
接著，初始化 `Graphics` 類別的實例，以在圖像上執行繪圖操作。

```java
Graphics graphics = new Graphics(image);
```

*說明*：`Graphics` 物件將繪圖指令連結至我們剛建立的 `image`。

### 步驟 3：清除圖形表面
使用特定的背景顏色（此處為 `Color.getYellow()`）清除圖形表面。

```java
graphics.clear(Color.getYellow());
```

*說明*：此設定明亮的黃色背景，使黑色貝塞爾曲線更加突出。

### 步驟 4：初始化畫筆以繪圖
設定 `Pen` 物件的顏色與寬度等屬性，以定義曲線的繪製方式。

```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```

*說明*：畫筆為黑色，寬度為 **3 像素** – 您可調整寬度以讓曲線變粗或變細（`java graphics pen width`）。

### 步驟 5：定義貝塞爾曲線參數
為貝塞爾曲線指定控制點與終點。

```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```

*說明*：  
- `startX`、`startY` – 曲線的起始點。  
- `controlX1`、`controlY1` – 第一個控制點。  
- `controlX2`、`controlY2` – 第二個控制點。  
- `endX`、`endY` – 終點。

### 步驟 6：繪製貝塞爾曲線
使用 `drawBezier()` 方法，結合先前定義的 `Pen` 與控制點，在圖像上繪製貝塞爾曲線。

```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```

*說明*：此單一呼叫會渲染出平滑的 **draw bezier curve java** 線條，依照您提供的控制點繪製。

### 步驟 7：儲存圖像
將繪製好的圖像儲存為 BMP 檔案格式。

```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

*說明*：`BmpOptions` 物件告訴 Aspose.PSD 以 BMP 格式寫入檔案。如需其他格式，可改用 `PngOptions`、`JpegOptions` 等。

## 常見問題與解決方案
- **曲線呈平直** – 請再次確認控制點座標；它們不能與起點/終點共線。  
- **圖像為空白** – 確保在繪圖前已呼叫 `graphics.clear()`，且 `Pen` 顏色與背景形成對比。  
- **大型畫布導致 OutOfMemoryError** – 增加 JVM 堆積大小（`-Xmx`）或使用分塊圖像。

## 常見問答

### 我可以在同一圖像中繪製多條貝塞爾曲線嗎？
可以，您可以在迴圈中重複此流程，依需求變更控制點與終點，以繪製多條曲線。

### 如何變更貝塞爾曲線的顏色？
在呼叫 `drawBezier()` 前，修改 `Pen` 物件的顏色屬性（範例中為 `Color.getBlack()`）。

### Aspose.PSD for Java 是否適用於高解析度圖像？
是，Aspose.PSD for Java 支援高解析度圖像，且具有效率的記憶體管理。

### 我可以將圖像匯出為 BMP 以外的格式嗎？
可以，Aspose.PSD for Java 支援將圖像匯出為 PNG、JPEG、TIFF 等多種格式。

### 我可以在哪裡找到更多範例與文件？
請前往 [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) 取得完整指南與程式碼範例。

## 結論
透過本 **bezier curve tutorial java**，您現在已了解如何使用 Aspose.PSD for Java **建立貝塞爾曲線圖像**。請嘗試不同的控制點、畫筆顏色與線寬，以在 Java 應用程式中產生各式藝術效果。

---

**最後更新：** 2026-01-17  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}