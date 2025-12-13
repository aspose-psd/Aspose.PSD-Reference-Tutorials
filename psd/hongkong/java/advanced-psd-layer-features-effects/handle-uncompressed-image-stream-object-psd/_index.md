---
date: 2025-12-13
description: 學習如何使用 Aspose.PSD for Java 透過處理未壓縮的圖像流來建立 PSD 圖形物件並操作 PSD 圖層。
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: 在 Java 中建立 PSD 圖形物件 – 未壓縮串流
url: /zh-hant/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 建立 PSD 圖形物件 – Java 中的未壓縮串流

## 介紹
歡迎來到 Java 圖像處理的世界！在本教學中，您將 **建立 PSD 圖形物件**，並使用 Aspose.PSD for Java 處理未壓縮的圖像串流物件。無論您是想自動化工作流程的平面設計師，或是希望在應用程式中整合強大圖像處理功能的軟體開發人員，本指南都為您量身打造。我們將從前置條件講起，一路走到結論，確保您能夠順利上手 Aspose.PSD。

## 快速解答
- **「建立 PSD 圖形物件」是什麼意思？** 它指的是為 PSD 檔案實例化一個圖形繪圖上下文，以便您可以繪製或編輯其內容。  
- **哪個函式庫負責未壓縮串流？** Aspose.PSD for Java 完全支援原始（未壓縮）圖像資料。  
- **開發時需要授權嗎？** 免費試用版可用於測試；正式上線則需購買商業授權。  
- **建立圖形物件後可以操作 PSD 圖層嗎？** 可以——Graphics 實例允許您在任何圖層上繪圖。

## 前置條件
在開始編寫程式碼之前，請先確保您已具備以下條件：

### Java Development Kit (JDK)
請確認您的機器已安裝 JDK，可從 Oracle 官方網站下載，或使用 OpenJDK。

### Aspose.PSD for Java
您需要下載並安裝 Aspose.PSD 函式庫。此強大函式庫讓您輕鬆操作 PSD 檔案。可從[此連結](https://releases.aspose.com/psd/java/)取得最新版本。

### Integrated Development Environment (IDE)
建議使用 IDE 來編寫與測試 Java 程式碼，例如 IntelliJ IDEA、Eclipse 或其他您慣用的開發環境。

### Basic Understanding of Java
具備 Java 基礎（如類別、方法、例外處理）會讓整個流程更順暢。

一切就緒後，讓我們捲起袖子，進入最精彩的部分——編碼吧！

## 匯入套件
首先，我們需要匯入使用 Aspose.PSD 所必須的套件。以下是處理 PSD 檔案時常用的匯入語句。

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

接下來，我們將把程式碼拆解成易於理解的步驟，讓您能輕鬆跟隨。內容包括設定、載入 PSD、操作以及儲存輸出。

## Step 1: Define Your Document Directory
在撰寫程式碼之前，請先定義 PSD 檔案所在的目錄。這相當於為您的專案設定工作基礎。

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為實際存放 PSD 檔案（例如 layers.psd）的路徑，方便程式正確找尋檔案。

## Step 2: Create a Byte Array Output Stream
您需要一個地方暫存修改後的圖像資料。`ByteArrayOutputStream` 能輕鬆捕捉圖像位元組。

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

此行程式碼會建立一個名為 `ms` 的 `ByteArrayOutputStream` 物件，之後將用它來儲存未壓縮的圖像。

## Step 3: Load the PSD File
現在是載入實際 PSD 檔案的時候了，魔法即將展開！

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

此行程式碼會將您的 PSD 檔案載入為 `PsdImage` 物件。請務必確認路徑正確，否則會拋出錯誤。

## Step 4: Set Up the PsdOptions for Saving
接下來需要指定儲存方式——未壓縮，當然！

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

在此您建立 `PsdOptions` 物件，並將壓縮方式設定為 `Raw`。此設定可確保圖像保留完整品質，且不會進行任何壓縮。

## Step 5: Save the Image to the Output Stream
```java
psdImage.save(ms, saveOptions);
```

此行程式碼會使用第 4 步設定的選項，將修改後的圖像儲存至第 2 步建立的 `ByteArrayOutputStream` 中。`save` 方法會依設定正確編碼圖像。

## Step 6: Reset the Output Stream
儲存完成後，輸出串流已指向結尾。需要將指標重設回開頭才能再次讀取。

```java
ms.reset();
```

`reset` 方法會把 `ByteArrayOutputStream` 的讀寫位置重新指向起始點，就像倒帶磁帶，準備播放您最喜愛的歌曲。

## Step 7: Load the Newly Created Image
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

此處我們從 `ByteArrayOutputStream` 重新載入圖像，建立新的 `PsdImage` 物件，以便檢查先前的處理結果。

## Step 8: Create Graphics Object
```java
Graphics graphics = new Graphics(psdImage);
```

此行程式碼會以 `psdImage` 為基礎，初始化一個 `Graphics` 物件。現在您可以使用此圖形物件進行繪圖或其他操作，就像手握畫筆一般。

## Manipulate PSD Layers with Graphics Object
有了 **Graphics** 實例後，您即可 **操作 PSD 圖層**——例如繪製形狀、加入文字或對特定圖層套用濾鏡。圖形上下文直接作用於底層像素資料，讓您對每個圖層的外觀擁有精細控制。

## Common Issues and Solutions
- **載入檔案時出現 NullPointerException** – 請再次確認 `dataDir` 路徑與檔名是否正確。  
- **即使使用 Raw 仍得到壓縮輸出** – 請確保在呼叫 `save` 方法前已執行 `saveOptions.setCompressionMethod(CompressionMethod.Raw);`。  
- **Graphics 物件顯示為空白** – 請確認您正對正確的 `PsdImage` 實例繪圖（使用已載入的實例，而非新建立的除非有意如此）。

## 常見問題

### 什麼是 Aspose.PSD？
Aspose.PSD 是一套 .NET 函式庫，讓開發者能以程式方式建立、編輯與操作 Photoshop PSD 檔案及相關影像格式。

### 如何下載 Aspose.PSD for Java？
您可以從[發行頁面](https://releases.aspose.com/psd/java/)下載。

### Aspose.PSD 有免費試用版嗎？
有，您可以在[此處](https://releases.aspose.com/)取得免費試用版。

### 是否提供 Aspose.PSD 的支援服務？
當然！您可於[Aspose 支援論壇](https://forum.aspose.com/c/psd/34)尋求協助。

### 如何取得 Aspose.PSD 的臨時授權？
只需前往[臨時授權頁面](https://purchase.aspose.com/temporary-license/)即可開始。

## Frequently Asked Questions

**Q: 我可以只使用 graphics 物件編輯單一特定圖層嗎？**  
A: 可以。載入 PSD 後，透過 `psdImage.getLayers().get_Item(index)` 取得目標圖層，並將其傳入 `Graphics` 建構子。

**Q: Raw 壓縮方式會影響檔案大小嗎？**  
A: Raw 會以未壓縮方式儲存像素資料，因此檔案大小會比壓縮的 PSD 大，但圖像品質保持不變。

**Q: 能否將編輯後的 PSD 匯出為其他格式（例如 PNG）？**  
A: 完全可以。編輯完畢後，使用 `Image.save` 並搭配 `PngOptions` 即可匯出。

**Q: 需要哪個版本的 Java？**  
A: Aspose.PSD for Java 支援 JDK 8 及以上版本。

**Q: 處理完畢後如何釋放資源？**  
A: 呼叫 `psdImage.dispose()`，並關閉所有串流，以釋放本機資源。

---  

**最後更新：** 2025-12-13  
**測試環境：** Aspose.PSD for Java（最新發行版）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}