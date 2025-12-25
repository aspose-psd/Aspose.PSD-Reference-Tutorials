---
date: 2025-12-25
description: 學習如何使用 Aspose.PSD for Java 及中斷監控支援將 PSD 轉換為 PNG，包括 Java 執行緒中斷範例與保存 PSD
  為 PNG 的技巧。
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: 如何在 Aspose.PSD for Java 中使用中斷監控支援將 PSD 轉換為 PNG
url: /zh-hant/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 的中斷監視器將 PSD 轉換為 PNG

## 介紹

如果您需要在完整控制長時間執行的圖像轉換的同時 **將 PSD 轉換為 PNG**，Aspose.PSD for Java 的中斷監視器就是您一直在尋找的工具。在本教學中，我們將示範一個真實的 **java 執行緒中斷範例**，讓您能在轉換過程中途停止，從而靈活地管理資源、強制超時或回應使用者取消。

## 快速解答
- **Interrupt Monitor 的作用是什麼？** 它允許您安全地發出訊號，讓正在進行的圖像轉換停止。  
- **我可以用它將 PSD 轉換為 PNG 嗎？** 可以——監視器適用於任何保存操作，包括 PNG。  
- **是否需要額外的執行緒？** 通常會在獨立執行緒中執行轉換，以便您可以中斷它。  
- **需要哪個版本的 Aspose.PSD？** 任何包含 `com.aspose.psd.multithreading.InterruptMonitor` 的近期版本皆可。  
- **生產環境需要授權嗎？** 需要，非試用情況下必須擁有有效的 Aspose.PSD 授權。

## 什麼是「使用中斷監視器將 PSD 轉換為 PNG」？

將大型 Photoshop 文件（PSD/PSB）轉換為 PNG 圖像可能會佔用大量 CPU。透過將 **Interrupt Monitor** 附加到轉換工作者，您即可程式化地中止處理程序——這對於 Web 服務、批次作業或使用者可能取消操作的 UI 應用程式而言，都是理想的解決方案。

## 為什麼要使用中斷監視器？

- **即時回應的 UI：** 防止應用程式在處理大型檔案時凍結。  
- **資源管理：** 停止超出時間或記憶體預算的轉換。  
- **錯誤處理：** 中斷發生時，優雅地清理部分輸出檔案。

## 前置條件

- Java 開發環境（JDK 8 或更新版本）。  
- Aspose.PSD for Java 程式庫 – 下載 **[here](https://releases.aspose.com/psd/java/)**。  
- 一個包含您要處理的 PSD/PSB 檔案的資料夾。

## 匯入套件

先匯入所需的類別，這樣您才能使用圖像選項、中斷監視器以及執行緒工具。

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## 步驟說明指南

### 步驟 1：設定文件目錄

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為 PSD 檔案所在的絕對路徑。

### 步驟 2：定義圖像選項與輸出路徑

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

此處使用 `PngOptions` **將 PSD 儲存為 PNG**，請依需求調整檔名。

### 步驟 3：初始化 Interrupt Monitor 與 SaveImageWorker

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

`InterruptMonitor` 實例稍後會用來停止轉換。`SaveImageWorker` 將監視器與轉換任務關聯起來。

### 步驟 4：在獨立執行緒中啟動圖像轉換

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

我們在背景執行緒上執行轉換，使主執行緒保持回應。`Thread.sleep(3000)` 呼叫模擬超時情境。

### 步驟 5：中斷處理（Java 執行緒中斷範例）

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

呼叫 `monitor.interrupt()` 會觸發 **how to interrupt monitor** 的邏輯。中斷後，我們會清除任何部分寫入的 PNG 檔案。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| 轉換永遠不會停止 | 監視器未與工作者連結 | 確保 `SaveImageWorker` 接收到相同的 `InterruptMonitor` 實例。 |
| 中斷後輸出檔案仍然保留 | 清理程式碼未執行 | 檢查 `finally` 區塊是否執行，且檔案路徑正確。 |
| 大型 PSB 檔案出現 `OutOfMemoryError` | 未使用串流選項 | 使用 `PsdImage` 搭配啟用記憶體效能載入的 `LoadOptions`。 |

## 常見問答

### Q1：什麼是 Aspose.PSD for Java 中的 Interrupt Monitor？

A1：Interrupt Monitor 讓開發者 **管理與中斷圖像轉換過程**，提供對長時間執行任務的細緻控制。

### Q2：如何取得 Aspose.PSD for Java 程式庫？

A2：您可以在 **[here](https://releases.aspose.com/psd/java/)** 下載 Aspose.PSD for Java 程式庫。

### Q3：Aspose.PSD for Java 是否提供免費試用？

A3：是的，您可以在 **[here](https://releases.aspose.com/)** 取得 Aspose.PSD 的免費試用版。

### Q4：在哪裡可以找到 Aspose.PSD for Java 的支援？

A4：請前往 Aspose.PSD for Java 支援論壇 **[here](https://forum.aspose.com/c/psd/34)**。

### Q5：如何購買 Aspose.PSD for Java 的授權？

A5：您可以在 **[here](https://purchase.aspose.com/buy)** 購買 Aspose.PSD for Java 授權。

---

**最後更新：** 2025-12-25  
**測試環境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}