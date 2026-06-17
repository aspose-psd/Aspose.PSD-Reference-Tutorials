---
date: 2026-06-08
description: 了解如何使用 Aspose.PSD for Java 將 PSD 另存為 PNG，並在需要時中斷轉換。有效管理圖像工作流程。
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: 支援中斷監控
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 如何在 Aspose.PSD for Java 中使用中斷監控將 PSD 另存為 PNG
url: /zh-hant/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 的中斷監視器將 PSD 儲存為 PNG

## 介紹

如果您需要在保持對長時間轉換完整控制的同時 **將 PSD 儲存為 PNG**，Aspose.PSD for Java 的中斷監視器正好提供此功能。在本教學中，我們將逐步說明如何設定監視器、將 PSD 檔案轉換為 PNG，以及在需要時安全地中止操作。您還會看到此功能如何融入典型的影像處理工作流程，以及為何它是打造穩健應用程式的必備工具。

## 快速答覆
- **我可以中斷 PSD 轉 PNG 的轉換嗎？** 是的，使用 `InterruptMonitor` 可依需求停止處理。  
- **哪個方法可將 PSD 儲存為 PNG？** 呼叫 `save(outputPath, new PngOptions())`。  
- **正式環境需要授權嗎？** 需要商業授權；亦提供免費試用版。  
- **支援哪個 Java 版本？** 完全支援 Java 8 及以上版本。  
- **此函式庫是執行緒安全的嗎？** 轉換可在不同執行緒中執行；監視器能安全處理中斷。

## 前置條件

在深入了解中斷監視器的使用細節之前，請先確保具備以下前置條件：

- **Java 開發環境：** 在您的系統上建立 Java 開發環境。  
- **Aspose.PSD 函式庫：** 取得 Aspose.PSD for Java 函式庫。您可在此下載 [here](https://releases.aspose.com/psd/java/)。亦可造訪 Aspose 主站 [here](https://releases.aspose.com/)。  
- **文件目錄：** 為您的 PSD 文件準備指定的目錄。

## 匯入套件

首先在您的 Java 專案中匯入必要的套件，以確保能使用 Aspose.PSD 的功能。

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

接下來，我們將把範例程式碼拆解為逐步指南，說明如何在 Aspose.PSD for Java 專案中加入中斷監視器。

## 如何使用中斷監視器將 PSD 儲存為 PNG？

`PsdImage` 代表已載入記憶體的 PSD 文件。  
`SaveImageWorker` 在獨立執行緒中執行影像轉換。  

使用 `new PsdImage("source.psd")` 載入 PSD 檔案，將 `InterruptMonitor` 附加至 `SaveImageWorker`，然後呼叫 `save("output.png", new PngOptions())`。監視器會偵測取消請求，並乾淨利落地中止轉換，於毫秒內將控制權回傳給您的應用程式。

### 步驟 1：設定文件目錄

```java
String dataDir = "Your Document Directory";
```

請將 “Your Document Directory” 替換為實際存放 PSD 文件的路徑。

### 步驟 2：定義影像選項與輸出路徑

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

指定影像選項、來源 PSD 檔案，以及轉換後影像的目標輸出路徑。

### 步驟 3：初始化中斷監視器與 SaveImageWorker

`InterruptMonitor` 類別會監控正在執行的轉換，並在呼叫 `requestInterrupt()` 時中斷它。  

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

建立 `InterruptMonitor` 與 `SaveImageWorker` 的實例，將監視器與影像轉換工作者連結起來。

### 步驟 4：啟動影像轉換執行緒

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

為影像轉換程序啟動新執行緒，並設定逾時時間以預期可能的中斷。

### 步驟 5：中斷處理程序

呼叫 `monitor.requestInterrupt()` 會向監視器發出中止正在進行的轉換的訊號。  

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

使用 `InterruptMonitor` 中斷影像轉換程序，並等待中斷完成。最後，透過刪除輸出檔案進行清理。

## 為何在 PSD 轉 PNG 時使用中斷監視器？

Aspose.PSD 支援超過 **30 種**輸出格式，包括 PNG、JPEG、BMP 與 TIFF，且可在不將整個文件載入記憶體的情況下處理高達 **500 MB** 的檔案。加入中斷監視器可減少 CPU 浪費，提升批次處理流程的回應速度，尤其在轉換時間超出預期時更為顯著。

## 常見問題與解決方案

- **轉換無限掛起：** 請確保在呼叫 `save` 之前已附加監視器。  
- **中斷後輸出檔案損毀：** 監視器會乾淨地中止；但仍建議在使用前檢查檔案是否存在。  
- **執行緒安全性疑慮：** 每個轉換請於獨立執行緒中執行；監視器僅影響其所屬的工作者。

## 常見問答

**Q1：什麼是 Aspose.PSD for Java 的中斷監視器？**  
A：中斷監視器讓開發者能暫停或取消長時間的影像轉換，提供即時的資源使用控制。

**Q2：如何取得 Aspose.PSD for Java 函式庫？**  
A：您可在此下載 Aspose.PSD for Java 函式庫 [here](https://releases.aspose.com/psd/java/).

**Q3：Aspose.PSD for Java 有提供免費試用嗎？**  
A：有，您可在此體驗 Aspose.PSD 的免費試用版 [here](https://releases.aspose.com/).

**Q4：在哪裡可以取得 Aspose.PSD for Java 的支援？**  
A：請前往 Aspose.PSD for Java 支援論壇 [here](https://forum.aspose.com/c/psd/34).

**Q5：如何購買 Aspose.PSD for Java 的授權？**  
A：您可在此購買 Aspose.PSD for Java 授權 [here](https://purchase.aspose.com/buy).

**Q6：我可以平行將多個 PSD 檔案轉換為 PNG 嗎？**  
A：可以，為每個檔案建立獨立執行緒，並為每個轉換工作者附加個別的 `InterruptMonitor`。

**Q7：在 PSD 轉 PNG 時，函式庫會處理色彩描述檔嗎？**  
A：當然會；Aspose.PSD 會保留內嵌的 ICC 描述檔，並自動套用至輸出 PNG。

---

**最後更新：** 2026-06-08  
**測試環境：** Aspose.PSD 23.12 for Java  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [在 Aspose.PSD for Java 中將 PSD 儲存為 PNG 並套用渲染陰影](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [使用 Aspose.PSD for Java 匯出 PSD 為 PNG 並新增一般圖層](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [在 PSD 檔案中支援中斷監視器 - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}