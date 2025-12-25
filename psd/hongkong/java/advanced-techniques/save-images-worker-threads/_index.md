---
date: 2025-12-25
description: 學習 Java 圖像處理教學，使用工作執行緒將 PSD 檔案儲存為 JPG。本指南說明如何透過執行緒有效地儲存圖像。
linktitle: Save Images using Worker Threads
second_title: Aspose.PSD Java API
title: Java 影像處理教學 – 使用工作執行緒儲存影像
url: /zh-hant/java/advanced-techniques/save-images-worker-threads/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 圖像處理教學 – 使用工作執行緒儲存圖像

## 簡介

歡迎閱讀本 **java 圖像處理教學**，我們將示範如何使用 Aspose.PSD for Java 的 **工作執行緒**，將 PSD 檔案儲存為 JPG（或其他格式）。多執行緒的圖像處理能顯著縮短執行時間，尤其在需要轉換大量檔案時更為明顯。接下來的幾分鐘內，您將了解執行緒的重要性、如何安全地設定，以及完整可直接執行的程式碼範例。

## 快速回答
- **本教學涵蓋什麼內容？** 使用 Aspose.PSD for Java 透過工作執行緒儲存圖像。  
- **為什麼要使用執行緒？** 以平行方式處理多張圖像，提高吞吐量。  
- **需要授權嗎？** 正式環境需要臨時授權；測試可使用免費試用版。  
- **支援哪個 Java 版本？** Java 8 或以上。  
- **可以將 PSD 轉成 JPG 嗎？** 可以——本教學示範儲存為任何支援的格式。

## 什麼是 java 圖像處理教學？

*java 圖像處理教學* 旨在教導您如何在 Java 中以程式方式操作、轉換與匯出圖像檔案。本指南的重點在於 **高效儲存圖像**，透過將大量 I/O 工作交由背景執行緒處理。

## 為什麼要使用工作執行緒儲存圖像？

- **效能提升：** 平行執行可利用多核心 CPU，減少整體處理時間。  
- **保持回應性：** 主程式在儲存大型檔案時仍能保持流暢。  
- **可擴充性：** 輕鬆將此方式擴展至批次處理上千個檔案。

## 前置條件

在開始之前，請確保具備以下條件：

- 具備 Java 程式設計的基礎知識。  
- 已安裝 Aspose.PSD for Java 套件。您可以在 [此處](https://releases.aspose.com/psd/java/) 下載。  
- 已設定好 Java 開發環境（JDK 8 或更新版本）。

## 匯入套件

在您的 Java 專案中，先匯入使用 Aspose.PSD 所需的套件：

```java
import com.aspose.psd.Image;
import com.aspose.psd.ImageOptionsBase;
import com.aspose.psd.coreexceptions.OperationInterruptedException;
import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.multithreading.InterruptMonitor;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

### 步驟 1：初始化 `SaveImageWorker`

建立名為 `SaveImageWorker` 的類別，並初始化所需變數。此工作執行緒封裝單一次儲存操作所需的全部資料。

```java
public class SaveImageWorker {
    // ... (Refer to provided code for variable declarations)
    
    public SaveImageWorker(String inputPath, String outputPath, ImageOptionsBase saveOptions, InterruptMonitor monitor) {
        // Constructor logic
    }
    
    // ... (Refer to provided code for additional methods)
}
```

### 步驟 2：定義 `ThreadProc` 方法

實作 `ThreadProc` 方法，以在處理中斷時仍能優雅地將圖像從一種格式轉換為另一種格式。

```java
public String ThreadProc() {
    Image image = Image.load(this.inputPath);

    InterruptMonitor.setThreadLocalInstance(this.monitor);

    try {
        image.save(this.outputPath, this.saveOptions);
    } catch (OperationInterruptedException e) {
        System.out.println("The save thread #" + Thread.currentThread().getId() + " finishes at " + getDateTime().toString());
        System.out.println(e);
    } catch (Exception e) {
        System.out.println(e);
    } finally {
        InterruptMonitor.setThreadLocalInstance(null);
    }

    return "Hello Aspose";
}
```

### 步驟 3：在應用程式中使用 `SaveImageWorker`

在主程式中建立 `SaveImageWorker` 實例，並呼叫 `ThreadProc` 於背景執行緒執行儲存操作。

```java
public class MainApplication {
    public static void main(String[] args) {
        // ... (Initialize inputPath, outputPath, saveOptions, and monitor)
        
        SaveImageWorker saveImageWorker = new SaveImageWorker(inputPath, outputPath, saveOptions, monitor);
        String result = saveImageWorker.ThreadProc();
        
        // ... (Handle the result as needed)
    }
}
```

## 常見問題與解決方案

| 問題 | 為何會發生 | 解決方式 |
|------|------------|----------|
| **執行緒卡住** | `InterruptMonitor` 未被清除 | 確保在 `finally` 區塊中執行 `InterruptMonitor.setThreadLocalInstance(null)`。 |
| **不支援的格式** | 使用了錯誤的 `ImageOptionsBase` 子類別 | 使用 `JpegOptions`、`PngOptions` 等與目標輸出相符的類別。 |
| **記憶體不足** | 大型 PSD 在 UI 執行緒載入 | 在工作執行緒內完成載入與儲存；對於超大檔案可考慮串流處理。 |

## 常見問答

### Q1: Aspose.PSD for Java 是否適合多執行緒圖像處理？

A1: 是的，Aspose.PSD for Java 內建多執行緒支援，讓您在圖像處理任務中提升效能。

### Q2: 哪裡可以找到 Aspose.PSD for Java 的詳細文件？

A2: 您可前往文件 [此處](https://reference.aspose.com/psd/java/) 取得完整資訊。

### Q3: 如何取得 Aspose.PSD for Java 的臨時授權？

A3: 可在 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權，以探索全部功能。

### Q4: Aspose.PSD for Java 提供哪些支援選項？

A4: 如需協助或詢問，請造訪 [Aspose.PSD for Java 論壇](https://forum.aspose.com/c/psd/34) 與社群及專家交流。

### Q5: 哪裡可以購買 Aspose.PSD for Java？

A5: 前往 [購買頁面](https://purchase.aspose.com/buy) 完成購買。

### Q6: 我可以使用此方式將 PSD 轉成 JPG 嗎？

A6: 當然可以。呼叫 `image.save(...)` 時，將 `JpegOptions` 作為 `saveOptions` 參數傳入。

### Q7: 為了最佳效能，我應該產生多少個執行緒？

A7: 一般建議與可用 CPU 核心數相同（`Runtime.getRuntime().availableProcessors()`），但仍需依實際工作負載測試調整。

## 結論

您已掌握一套 **java 圖像處理教學**，學會如何使用 Aspose.PSD for Java 透過執行緒 **儲存圖像**。將儲存邏輯封裝於工作類別，並善用 `InterruptMonitor`，即可同時獲得速度與穩定性。未來可將此模式擴展至批次處理資料夾、加入進度回報，或整合至更大型的圖像處理管線中。

---

**最後更新：** 2025-12-25  
**測試環境：** Aspose.PSD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}