---
date: 2026-03-21
description: 學習如何使用 Aspose.PSD for Java 匯出圖像、將 PSD 轉換為點陣圖，並在多執行緒環境中刪除暫存檔案。提升效能，保持工作區整潔。
linktitle: Export Images in Multi‑Threaded Environment
second_title: Aspose.PSD Java API
title: 如何在多執行緒環境中匯出圖像時刪除臨時檔案 – Aspose.PSD for Java
url: /zh-hant/java/psd-conversion/export-images-multi-thread/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 多執行緒圖像匯出教學 – Aspose.PSD for Java  

您是否想在提升 Java 應用程式於多執行緒環境下的圖像匯出功能的同時 **delete temporary files**？Aspose.PSD for Java 可輕鬆實現 **convert PSD to raster**、使用 **save pixels java**，並保持檔案系統整潔。在本教學中，我們將逐步說明一個完整、可投入生產的範例，展示如何匯出圖像、安全管理執行緒，並自動清除任何遺留檔案。

## 快速解答
- **Aspose.PSD 能自動 delete temporary files 嗎？** 是的 – 您可以在處理後以程式方式將其移除。  
- **支援多執行緒圖像處理嗎？** 絕對支援；此函式庫在同時匯出時具備執行緒安全性。  
- **哪個方法在 Java 中儲存像素資料？** `savePixels` 在 `RasterImage` 實例上。  
- **在生產環境使用是否需要授權？** 需要有效的 Aspose.PSD 授權；亦提供免費試用版。  
- **相容的 Java 版本為何？** Java 1.7 及以上。

## 在圖像匯出的情境下，什麼是「delete temporary files」？
當您從 PSD 檔案匯出圖像時，通常會產生中間檔案（例如來源 PSD 的副本、暫存的點陣資料）。刪除這些 **delete temporary files** 可防止磁碟雜亂、降低儲存成本，並避免意外使用過時的資料。

## 為何在多執行緒圖像處理中使用 Aspose.PSD？
- **高效能：** 同時平行處理多個 PSD 檔案，無瓶頸。  
- **執行緒安全：** 核心 API 設計為在多執行緒存取時仍能正確運作。  
- **豐富功能集：** 可直接 **convert PSD to raster** 為點陣格式、編輯圖層，並以細緻的控制使用 **save pixels java**。  
- **內建清理機制：** 您自行決定何時以及如何 **delete temporary files**，從而完整掌控資源管理。

## 前置條件
- 具備 Java 程式設計的基礎知識。  
- Java 開發環境 (JDK 1.7+)。  
- 已下載並安裝 Aspose.PSD for Java 函式庫。您可在此取得下載連結 [here](https://releases.aspose.com/psd/java/)。

## 匯入套件
將所需的匯入加入您的 Java 類別。這些類別提供顏色處理、點陣圖像操作以及基於串流的載入功能。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.FileStream;
import java.io.File;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
```

## 步驟 1：設定文件目錄  
指定來源 PSD 檔案所在的位置。將路徑存於變數可方便於執行緒間重複使用。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：載入 PSD 圖像  
以串流方式開啟 PSD 檔案，並設定 `PsdOptions`，讓 Aspose.PSD 知道從何處讀取資料。

```java
String imageDataPath = dataDir + "sample.psd";
FileInputStream fileStream = new FileInputStream(imageDataPath);
PsdOptions psdOptions = new PsdOptions();
psdOptions.setSource(new StreamSource(fileStream));
```

## 步驟 3：處理圖像 – Convert PSD to Raster 與 Save Pixels  
從 PSD 選項建立 `RasterImage`，修改少量像素，然後將點陣資料儲存回檔案系統。此範例示範 **convert psd to raster** 以及 **save pixels java** 工作流程。

```java
RasterImage image = (RasterImage)Image.create(psdOptions, 10, 10);
Color[] pixels = new Color[4];
for (int i = 0; i < 4; ++i) {
    pixels[i] = Color.fromArgb(40, 30, 20, 10);
}
image.savePixels(new Rectangle(0, 0, 2, 2), pixels);
image.save();
```

## 步驟 4：清理 – Delete Temporary Files  
匯出完成後，最佳做法是刪除所有建立的暫存檔案（包括若為副本的原始 PSD）。這正是我們的 **delete temporary files** 策略核心。

```java
File f = new File(imageDataPath);
if (f.exists()) {
    f.delete();
}
```

> **Pro tip:** 將清理程式碼包在 `finally` 區塊中，或使用 Java 的 try‑with‑resources，以確保即使發生例外仍能刪除檔案。

## 常見問題與解決方案
| 問題 | 原因 | 解決方法 |
|------|------|----------|
| `FileNotFoundException` on `FileInputStream` | 錯誤的路徑或缺少檔案權限 | 確認 `dataDir` 並確保應用程式具備讀寫權限。 |
| 圖像未正確儲存 | 在 `savePixels` 後未呼叫 `image.save()` | 確保在像素修改後執行 `image.save()`。 |
| 程式當機後暫存檔仍然存在 | 未執行清理程式碼 | 使用關閉鉤子或 finally 區塊以保證刪除。 |

## 常見問答

### Aspose.PSD 是否相容所有 Java 版本？
Aspose.PSD 相容於 Java 1.7 及以上版本。

### 我可以使用 Aspose.PSD 同時處理多張圖像嗎？
是的，Aspose.PSD 支援多執行緒，可同時處理多張圖像。

### 我在哪裡可以找到 Aspose.PSD 的其他文件？
您可參考文件 [here](https://reference.aspose.com/psd/java/)。

### 是否提供 Aspose.PSD for Java 的免費試用？
是的，您可在此取得免費試用版 [here](https://releases.aspose.com/)。

### 如何取得 Aspose.PSD 的暫時授權？
請前往 [this link](https://purchase.aspose.com/temporary-license/) 取得暫時授權。

**Additional Q&A**

**Q:** 圖像匯出時，管理工作執行緒池的最佳方式是什麼？  
**A:** 使用 `java.util.concurrent.ExecutorService`（例如 `Executors.newFixedThreadPool`）提交匯出任務，讓框架負責執行緒生命週期。

**Q:** 我可以匯出成除 PSD 之外的其他格式嗎？  
**A:** 可以，Aspose.PSD 能透過相應的 `ImageOptions` 類別將點陣圖儲存為 PNG、JPEG、BMP 等多種格式。

**Q:** 若共享 `RasterImage` 實例，如何確保執行緒安全？  
**A:** 不要在多執行緒間共享同一個 `RasterImage`；每個任務建立獨立的圖像，或在必須共享時使用同步機制。

## 結論
在本教學中，我們探討了在 **multi‑threaded** 環境下使用 Aspose.PSD for Java 匯出圖像時，如何 **delete temporary files**。您學會了 **convert PSD to raster**、使用 **save pixels java** 操作像素資料，並透過程式方式移除暫存檔案以保持工作區整潔。將這些模式套用於提升效能、降低儲存開銷，並建構穩健的 Java 圖像處理管線。

---

**最後更新：** 2026-03-21  
**測試版本：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}