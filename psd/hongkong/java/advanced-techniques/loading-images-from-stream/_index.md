---
date: 2025-12-22
description: 學習如何使用 Aspose.PSD for Java 從串流將 PSD 轉換為 PNG。請參考此逐步指南，了解如何載入 PSD 檔案並匯出為
  PNG 圖像。
linktitle: Loading Images from Stream
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 從串流將 PSD 轉換為 PNG
url: /zh-hant/java/advanced-techniques/loading-images-from-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 從串流將 PSD 轉換為 PNG（使用 Aspose.PSD for Java）

## 介紹

如果您需要在 Java 應用程式中直接從串流 **將 PSD 轉換為 PNG**，Aspose.PSD for Java 讓這個過程變得輕鬆。於本教學中，您將學會如何 **從 InputStream 載入 PSD 檔案**，將其轉換為 `PsdImage`，以及使用 `FileOutputStream` **將 PSD 匯出為 PNG**。此方法無論是處理磁碟上的檔案、接收 HTTP 上傳，或是處理記憶體中的資料，都能順利運作。

## 快速回答
- **我可以從 InputStream 載入 PSD 嗎？** 是 – 使用 `Image.load(inputStream)`。
- **Aspose.PSD 匯出 PNG 的格式是什麼？** 呼叫 `save` 時使用 `PngOptions`。
- **開發時需要授權嗎？** 測試需要臨時授權；正式環境需要完整授權。
- **API 是否相容於 Java 8+？** 當然，支援所有現代 Java 版本。
- **典型效能如何？** 載入與儲存中等大小的 PSD 通常在數百毫秒內完成。

## 什麼是「將 PSD 轉換為 PNG」？

將 Photoshop 文件（PSD）轉換為可攜式網路圖形（PNG）檔案，會將視覺圖層提取為廣受支援的點陣格式。PNG 能保留透明度與無損品質，因而非常適合用於網站資產、縮圖或進一步的影像處理。

## 為何使用 Aspose.PSD 將 PSD 轉換為 PNG？

- **不需 Photoshop** – 此函式庫在內部處理所有 PSD 規格。
- **支援串流** – 您可以使用 `InputStream`/`OutputStream` 物件，十分適合雲端或微服務架構。
- **高保真度** – 轉換過程中保留圖層、遮色片與色彩配置檔。
- **批次處理就緒** – 相同程式碼可放入迴圈，自動處理大量檔案。

## 前置條件

在開始之前，請確保您已具備：

- 可運作的 Java 開發環境（JDK 8 或以上）。
- 已將 Aspose.PSD for Java 函式庫加入專案。可從 [Aspose website](https://releases.aspose.com/psd/java/) 下載。
- 基本的 Java I/O 串流使用經驗。

## 匯入套件

在您的 Java 類別中加入必要的匯入。這些類別讓您能存取影像載入、PSD 處理與 PNG 匯出選項。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.MemoryStream;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
```

## 步驟 1：設定文件目錄

定義一個資料夾，用於存放來源 PSD 與產生的 PNG。將佔位符替換為您機器或伺服器上的實際路徑。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：定義來源與目的地路徑

指定輸入 PSD 與輸出 PNG 的完整檔名。如此一來，之後建立串流時會更簡單。

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## 步驟 3：建立輸入串流並載入影像

為 PSD 檔案開啟 `FileInputStream`，並讓 Aspose.PSD 載入。此步驟示範 **如何使用串流載入 PSD**，適用於檔案來自網路來源或資料庫 BLOB 的情況。

```java
FileInputStream inputStream = new FileInputStream(sourceFile);
Image image = Image.load(inputStream);
```

## 步驟 4：將影像轉換為 PsdImage

必須將通用的 `Image` 物件轉型為 `PsdImage`，才能存取 PSD 專屬功能。若載入的影像已是 PSD，轉型會成功；否則需額外的轉換邏輯。

```java
PsdImage psdImage = (PsdImage)image;
```

## 步驟 5：使用 PNG 選項將影像儲存至串流

為目的檔案建立 `FileOutputStream`，並使用 `PngOptions` 儲存 `PsdImage`。此步驟 **將影像儲存至串流**，同時 **將 PSD 匯出為 PNG**。

```java
FileOutputStream outputStream = new FileOutputStream(destName);
psdImage.save(outputStream, new PngOptions());
```

> **專業提示：** 請務必在 `finally` 區塊中關閉串流，或使用 try‑with‑resources，以避免資源洩漏。

恭喜！您已成功使用 Aspose.PSD for Java 從串流 **將 PSD 轉換為 PNG**。

## 如何從串流將 PSD 轉換為 PNG

此 H2 標題強調主要關鍵字並概述工作流程：

1. 使用 `Image.load(InputStream)` 載入 PSD。
2. 轉型為 `PsdImage`。
3. 使用 `PngOptions` 儲存至 `OutputStream`。

## 常見陷阱與故障排除

- **`ClassCastException`** – 確認載入的影像為 PSD 後再進行轉型。可使用 `if (image instanceof PsdImage)` 檢查。
- **資源洩漏** – 請務必關閉 `FileInputStream` 與 `FileOutputStream`。建議使用 try‑with‑resources。
- **大型檔案** – 對於非常大的 PSD，考慮使用 `MemoryStream` 以減少磁碟 I/O，但需監控堆積記憶體使用情況。

## 結論

Aspose.PSD for Java 讓開發人員能快速且可靠地 **將 PSD 轉換為 PNG**。透過從 `InputStream` 載入 PSD 並使用 `PngOptions` 儲存，您可以將此功能整合至 Web 服務、批次處理器或任何基於 Java 的影像管線。欲深入了解，請參考官方 [documentation](https://reference.aspose.com/psd/java/)。

## 常見問答

### Q1：Aspose.PSD for Java 是否適合批次影像處理？

A1：絕對適合！Aspose.PSD for Java 在批次影像處理任務上表現卓越，提供高效率與可靠性。

### Q2：我可以在購買前試用 Aspose.PSD for Java 嗎？

A2：可以，您可於此處 [here](https://releases.aspose.com/) 下載免費試用版。

### Q3：我可以在哪裡取得 Aspose.PSD for Java 的支援？

A3：加入 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 社群，即可取得協助與討論。

### Q4：測試時是否需要臨時授權？

A4：請於此處 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權，以測試 Aspose.PSD for Java。

### Q5：我可以在哪裡購買 Aspose.PSD for Java？

A5：請前往 [purchase page](https://purchase.aspose.com/buy) 購買 Aspose.PSD for Java。

## 常見問題

**Q：我可以轉換受密碼保護的 PSD 嗎？**  
A：可以。使用包含密碼的 `LoadOptions` 物件載入檔案，然後依照相同的轉換步驟進行。

**Q：是否能在不寫入磁碟的情況下將 PSD 轉換為 PNG？**  
A：絕對可以。對於輸入與輸出皆使用 `MemoryStream`，最後從輸出串流取得位元組陣列。

**Q：Aspose.PSD 在匯出 PNG 時是否保留圖層透明度？**  
A：會。PNG 匯出會保留原始 PSD 圖層的透明資訊。

**Q：支援哪些 Java 版本？**  
A：此函式庫支援 Java 8 及以上版本，包括 Java 11、17 以及更新的 LTS 版本。

**Q：大量檔案轉換時，如何提升效能？**  
A：重複使用同一個 `PngOptions` 實例，利用 executor service 以平行方式處理檔案，並確保正確關閉串流。

---

**最後更新：** 2025-12-22  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}