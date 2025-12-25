---
date: 2025-12-25
description: 了解如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG 並將圖像儲存至串流。本分步指南示範如何高效地將 PSD
  匯出為 PNG。
linktitle: Save Images to Stream
second_title: Aspose.PSD Java API
title: 將 PSD 轉換為 PNG 並以 Aspose.PSD for Java 儲存至串流
url: /zh-hant/java/advanced-techniques/save-images-to-stream/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 轉換為 PNG 並儲存至串流（使用 Aspose.PSD for Java）

## 簡介

在本教學中，您將學習 **如何將 PSD 轉換為 PNG**，並使用 Aspose.PSD Java 函式庫直接將產生的影像儲存至串流。無論您是要建立需要即時提供 PNG 縮圖的 Web 服務，或是處理 Photoshop 檔案的桌面應用程式，本指南都會一步步帶您完成從載入 PSD 檔案到匯出 PNG，且不需寫入中間檔案至磁碟的全過程。

## 快速答覆
- **「convert PSD to PNG」是什麼意思？** 它將 Photoshop 文件（PSD）轉換為可攜式網路圖形（PNG）影像，將透明度與圖層保留為平面光柵。
- **哪個函式庫負責轉換？** Aspose.PSD for Java 提供強大的 API，用於載入、編輯與匯出 PSD 檔案。
- **開發時需要授權嗎？** 免費試用版可用於評估；正式上線時需購買永久授權。
- **可以直接將 PNG 串流傳送給客戶端嗎？** 可以——將 PNG 儲存至 `FileOutputStream`（或任何 `OutputStream`）即可避免產生暫存檔。
- **需要哪個 Java 版本？** 支援 Java 8 以上。

## 什麼是「convert PSD to PNG」？
將 PSD 轉換為 PNG 指的是將具有多圖層的 Photoshop 檔案展平為單一圖層的 PNG 影像，該格式在瀏覽器與行動裝置上皆得到廣泛支援。當您需要從複雜的設計檔案中提取輕量、可直接在網頁使用的視覺素材時，常會使用此操作。

## 為什麼要使用 Aspose.PSD for Java？
- **完整的 PSD 相容性：** 處理所有 Photoshop 功能，包括調整圖層、遮色片與智慧物件。
- **不需原生 Photoshop：** 完全以 Java 執行，適合伺服器端處理。
- **支援串流的 API：** 可直接寫入 `OutputStream`，非常適合 HTTP 回應或記憶體內處理。

## 先決條件

在開始編寫程式碼之前，請確保您已具備：

1. **Java 開發環境** – 已安裝 JDK 8 或更新版本。
2. **Aspose.PSD 函式庫** – 下載並將 Aspose.PSD JAR 加入專案中。您可於[此處](https://reference.aspose.com/psd/java/)取得函式庫與相關文件。

## 匯入套件

在 Java 專案中，匯入必要的 Aspose.PSD 套件以開始使用：

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;

import java.io.FileNotFoundException;
import java.io.FileOutputStream;
```

這些匯入讓您能使用核心的 `Image` 類別來載入檔案、`PsdImage` 類型進行 PSD 專屬操作，以及 `PngOptions` 來控制 PNG 匯出設定。

## 逐步指南

### 步驟 1：設定文件目錄

首先，定義存放來源 PSD 檔案的資料夾。更新此路徑即可在不同專案間重複使用程式碼。

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為 `sample.psd` 所在資料夾的絕對或相對路徑。

### 步驟 2：指定來源與目的地

接著，組合輸入 PSD 與輸出 PNG 的完整檔名。您也可以將目的地指向任意 `OutputStream`（例如，用於記憶體內的 `ByteArrayOutputStream`）。

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

### 步驟 3：載入 PSD 影像

現在將 PSD 檔案載入記憶體。將其轉型為 `PsdImage` 後，即可存取 PSD 專屬的屬性與方法。

```java
Image image = Image.load(sourceFile);
PsdImage psdImage = (PsdImage)image;
```

### 步驟 4：儲存至串流

最後，建立 `FileOutputStream`（或其他 `OutputStream`），並指示 Aspose.PSD 直接將 PNG 資料寫入。若有需要，可透過 `PngOptions` 物件調整壓縮等級、顏色類型等設定。

```java
FileOutputStream outputStream = new FileOutputStream(destName);
psdImage.save(outputStream, new PngOptions());
```

`result.png` PNG 檔案現在已包含從 `sample.psd` 提取的展平影像。您可以對多個檔案重複此步驟，或將此邏輯整合至 Web 端點，以串流方式將 PNG 回傳給客戶端。

## 常見問題與技巧

- **FileNotFoundException** – 確認 `dataDir` 路徑以適合您作業系統的分隔符（`/` 或 `\\`）結尾。
- **記憶體使用量** – 大型 PSD 檔案可能佔用大量記憶體。儲存完成後可考慮呼叫 `psdImage.dispose()` 釋放資源。
- **自訂 PNG 設定** – 如需特定 PNG 特性，可使用 `PngOptions` 設定 `ColorType`、`CompressionLevel` 或 `Interlaced`。

## 常見問答

**Q:** *Aspose.PSD for Java 是否適合專業專案？*  
**A:** 是，Aspose.PSD 在企業級 Java 應用中廣泛使用，提供可靠的 PSD 操作。

**Q:** *我可以在哪裡取得更多支援或提問？*  
**A:** 前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 獲得社群協助與官方支援。

**Q:** *我可以在購買前試用 Aspose.PSD 嗎？*  
**A:** 當然可以——可透過 [免費試用](https://releases.aspose.com/) 來評估函式庫功能。

**Q:** *我要如何取得開發用的臨時授權？*  
**A:** 可於[此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權，用於測試與內部使用。

**Q:** *我可以在哪裡購買 Aspose.PSD for Java 的完整版本？*  
**A:** 請於[此處](https://purchase.aspose.com/buy) 購買完整版本。

## 結論

您現在已掌握 **如何將 PSD 轉換為 PNG**，並使用 Aspose.PSD for Java 將結果儲存至串流。此技術省去中間檔案的需求，降低 I/O 開銷，且完美契合現代高效能的 Java 應用程式。歡迎將程式碼套用於批次處理、REST API 或任何需要即時影像轉換的情境。

---

**最後更新：** 2025-12-25  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}