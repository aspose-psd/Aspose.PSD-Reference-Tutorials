---
date: 2026-02-17
description: 學習如何將 PSD 匯出為 PNG，並使用 Aspose.PSD for Java 處理未壓縮的圖像串流。
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: 將 PSD 匯出為 PNG – 建立 PSD 圖形物件 – Java 中的未壓縮串流
url: /zh-hant/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 PSD 為 PNG – 建立 PSD 圖形物件 – Java 中的未壓縮串流

## 介紹
歡迎來到 Java 圖像處理的世界！在本教學中，您將 **建立 PSD 圖形物件**、處理未壓縮的圖像串流，並學習如何使用 Aspose.PSD for Java **將 PSD 匯出為 PNG**。無論您是希望自動化工作流程的平面設計師，或是想將強大的圖像處理功能整合到應用程式中的軟體開發人員，本指南皆為您量身打造。我們將從前置條件講解到最終匯出，確保您對整個流程有完整的了解。

## 快速回答
- **「建立 PSD 圖形物件」是什麼意思？** 它指的是為 PSD 檔案實例化一個圖形上下文，以便您可以繪製或編輯其內容。  
- **哪個函式庫處理未壓縮的串流？** Aspose.PSD for Java 完全支援原始（未壓縮）圖像資料。  
- **編輯後我可以將 PSD 匯出為 PNG 嗎？** 可以——只要取得 `Graphics` 物件，即可渲染 PSD 並儲存為 PNG。  
- **開發時需要授權嗎？** 免費試用版可用於測試；正式上線需購買商業授權。  
- **匯出是否無失真？** 匯出為 PNG 可保留圖像品質，檔案大小比 JPEG 大，但比未壓縮的 PSD 小。  

## 如何使用 Aspose.PSD for Java 匯出 PSD 為 PNG
當您需要 **將 PSD 匯出為 PNG** 時，典型的工作流程如下：

1. 載入 PSD 檔案（或建立新檔案）。  
2. 使用 `Graphics` 物件執行任何繪圖或圖層操作。  
3. 使用 `PngOptions` 儲存產生的圖像（相同的 `Graphics` 實例可重複使用）。  

即使本教學著重於處理未壓縮的串流，您建立的 `Graphics` 物件仍可在後續流程中重複使用，以將 PSD 渲染為 PNG 檔案。

## 前置條件
在進入程式碼之前，讓我們確保您已具備所有必要的條件。以下是前置需求：

### Java Development Kit (JDK)
確保您的電腦已安裝 JDK。您可以從 Oracle 官方網站下載，或使用 OpenJDK。

### Aspose.PSD for Java
您需要下載並安裝 Aspose.PSD 函式庫。此功能強大的函式庫可輕鬆操作 PSD 檔案。您可從 [this link](https://releases.aspose.com/psd/java/) 取得最新版本。

### 整合開發環境 (IDE)
建議使用 IDE 來編寫與測試 Java 程式碼。您可以使用 IntelliJ IDEA、Eclipse，或其他您偏好的開發環境。

### 基本的 Java 知識
熟悉 Java 程式設計能讓此流程更順暢。請確保您了解類別、方法與例外處理等基礎概念。

一切就緒後，讓我們捲起袖子，進入最令人興奮的部分——編寫程式！

## 匯入套件
首先，我們需要匯入使用 Aspose.PSD 所需的套件。以下列出處理 PSD 檔案時常用的匯入語句。

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

接下來，我們將把程式碼拆解成易於理解的步驟，確保您能輕鬆跟隨。我們會設定環境、載入 PSD 檔案、進行操作，最後儲存輸出。

## 步驟 1：定義文件目錄
在開始編寫程式碼之前，您需要先定義 PSD 檔案所在的目錄。這相當於為您的專案設定基礎路徑。

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為實際放置 PSD 檔案（例如 layers.psd）的路徑。這可避免檔案尋找的麻煩。

## 步驟 2：建立 ByteArrayOutputStream
您需要一個地方暫存修改後的圖像，之後再進行處理。`ByteArrayOutputStream` 可協助您輕鬆捕獲圖像資料。

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

此行會初始化一個名為 `ms` 的新 `ByteArrayOutputStream` 物件。您將使用此物件儲存未壓縮的圖像。

## 步驟 3：載入 PSD 檔案
現在是載入實際 PSD 檔案的時候了，魔法即將展開！

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

此行會將您的 PSD 檔案載入為 `PsdImage` 物件。請確認路徑正確，否則會拋出錯誤，就像未預警的小測驗。

## 步驟 4：設定 PsdOptions 以儲存
您需要指定圖像的儲存方式——當然是未壓縮！

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

此處建立 `PsdOptions` 物件，並將壓縮方式設定為 `Raw`。此方法可確保圖像保留完整品質，且不進行任何壓縮即儲存。

## 步驟 5：將圖像儲存至輸出串流
```java
psdImage.save(ms, saveOptions);
```

此行使用第 4 步設定的選項，將您修改過的圖像儲存至第 2 步建立的 `ByteArrayOutputStream` 中。`save` 方法會依照設定正確編碼圖像。

## 步驟 6：重設輸出串流
儲存完成後，輸出串流已位於結尾。您需要將其重設，以便從開頭讀取。

```java
ms.reset();
```

此 `reset` 方法會讓您的 `ByteArrayOutputStream` 再次從開頭讀取。可以把它想像成在播放最愛歌曲前倒帶。

## 步驟 7：載入新建立的圖像
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

此處將圖像從 `ByteArrayOutputStream` 重新載入為新的 `PsdImage` 物件。您可以在此檢查先前工作的結果。

## 步驟 8：建立 Graphics 物件
若要進一步修改或渲染圖像，您需要建立一個 graphics 物件。

```java
Graphics graphics = new Graphics(psdImage);
```

此行使用您的 `psdImage` 初始化 `Graphics` 物件。現在您可以使用此 graphics 物件依需求繪製或操作圖像，就像手持畫筆一般！

## 使用 Graphics 物件操作 PSD 圖層
現在您已擁有 **Graphics** 實例，即可 **操作 PSD 圖層**——例如繪製形狀、加入文字，或對特定圖層套用濾鏡。graphics 上下文直接作用於底層像素資料，讓您對每個圖層的外觀擁有精細的控制。

## 常見問題與解決方案
- **載入檔案時出現 NullPointerException** – 請再次確認 `dataDir` 路徑，並確保檔名正確。  
- **即使使用 Raw 仍得到壓縮輸出** – 請確認在呼叫 `save` 方法前已執行 `saveOptions.setCompressionMethod(CompressionMethod.Raw);`。  
- **Graphics 物件顯示空白** – 請確保您在正確的 `PsdImage` 實例上繪圖（使用您載入的那個，而非新建立的，除非有特別需求）。

## 常見問答
### 什麼是 Aspose.PSD？
Aspose.PSD 是一套 .NET 函式庫，讓開發人員能以程式方式建立、編輯與操作 Photoshop PSD 檔案及相關影像格式。

### 如何下載 Aspose.PSD for Java？
您可從 [release page](https://releases.aspose.com/psd/java/) 下載。

### 有免費試用版嗎？
是的，您可從 [here](https://releases.aspose.com/) 取得免費試用版。

### 可以取得 Aspose.PSD 的支援嗎？
當然可以！您可在 [Aspose support forum](https://forum.aspose.com/c/psd/34) 尋求協助。

### 如何取得 Aspose.PSD 的臨時授權？
只需前往 [temporary license page](https://purchase.aspose.com/temporary-license/) 即可取得。

## 常見問答

**Q: 我可以使用 graphics 物件僅編輯特定圖層嗎？**  
A: 可以。載入 PSD 後，透過 `psdImage.getLayers().get_Item(index)` 取得目標圖層，並將其傳入 `Graphics` 建構子。

**Q: Raw 壓縮方式會影響檔案大小嗎？**  
A: Raw 會以未壓縮方式儲存像素資料，因此檔案大小會比壓縮的 PSD 大，但圖像品質保持不變。

**Q: 編輯完的 PSD 可以匯出為其他格式（例如 PNG）嗎？**  
A: 當然可以。編輯完成後，使用帶有 `PngOptions` 的適當 `Image.save` 重載，即可 **將 PSD 匯出為 PNG**。

**Q: 需要哪個版本的 Java？**  
A: Aspose.PSD for Java 支援 JDK 8 及以上版本。

**Q: 處理完畢後如何釋放資源？**  
A: 呼叫 `psdImage.dispose()` 並關閉所有串流，以釋放本機資源。

---

**最後更新：** 2026-02-17  
**測試環境：** Aspose.PSD for Java（最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}