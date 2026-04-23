---
date: 2026-03-13
description: 學習如何使用 Aspose.PSD for Java 建立 PSD 圖像 Java 專案，同時管理快取重新分配，並有效優化記憶體與磁碟使用。
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: 使用 Java 建立 PSD 圖像 – 控制快取重新分配
url: /zh-hant/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 控制 PSD 檔案的快取重新分配

## 介紹
如果您需要高效地 **create PSD image java** 專案，控制快取重新分配是必不可少的。以程式方式處理影像與 Photoshop 檔案時，效能是關鍵因素。Aspose.PSD for Java 提供強大的功能，讓您無縫管理與操作 PSD 檔案。最佳化效能的基本要素之一就是控制快取重新分配。快取管理有助於在記憶體與磁碟使用之間保持平衡，確保您的應用程式順暢執行，不會因為意外崩潰或變慢而受到影響。

## 快速回答
- **快取重新分配的作用是什麼？** 在處理大型 PSD 檔案時，平衡記憶體與磁碟的使用。  
- **哪種快取類型最適合大型影像？** `CacheOnDiskOnly` 會將快取儲存於磁碟，讓記憶體保持空閒。  
- **我可以分配多少磁碟空間？** 最多 1 GB（或使用 `setMaxDiskSpaceForCache` 設定的任何大小）。  
- **使用這些功能需要授權嗎？** 授權會移除試用限制；請參閱 Aspose 購買頁面。  
- **我可以在執行時監控快取使用情況嗎？** 可以，使用 `Cache.getAllocatedDiskBytesCount()` 與 `Cache.getAllocatedMemoryBytesCount()`。

## 為什麼要控制快取重新分配？
在 **create PSD image java** 應用程式中處理高解析度或多圖層檔案時，管理快取至關重要。適當的快取設定可防止記憶體不足錯誤、減少 GC 暫停，並在伺服器或桌面應用程式上提供可預測的效能。

## 前置條件
在進入程式碼部分之前，請先確保以下項目已就緒，以確保一切順利運行：
1. **Java Development Kit (JDK)：** 確認您的機器已安裝 JDK。您可以從 [Oracle 的網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java：** 需要下載 Aspose.PSD 程式庫。最新版本可在 [此處](https://releases.aspose.com/psd/java/) 取得。  
3. **IDE 設定：** 使用 IntelliJ IDEA 或 Eclipse 等整合開發環境 (IDE) 會讓您更容易管理程式碼。  
4. **基本的 Java 知識：** 熟悉 Java 程式設計有助於您更好地理解概念與程式碼片段。  
5. **Aspose 授權（可選）：** 若希望移除浮水印並取得完整功能，請考慮在 [此處](https://purchase.aspose.com/buy) 購買授權，或在 [此處](https://releases.aspose.com/) 試用免費版。

## 匯入套件
在開始撰寫程式碼之前，先確定已匯入必要的套件。以下是在 Java 檔案開頭需要加入的簡要清單：
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```

## 如何在 Java 中建立 PSD 影像並控制快取
以下提供逐步說明，將快取設定直接結合至 Java 中建立 PSD 影像的流程。

### 步驟 1：設定資料目錄
首先，您需要建立一個目錄來存放快取檔案。這對於有效管理快取至關重要。
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`：定義文件快取的目錄。  
- `Cache.setCacheFolder(dataDir)`：此方法將快取資料夾設定為指定目錄。Aspose 所產生的快取將儲存在此處，而非預設的暫存目錄。

### 步驟 2：將快取設定為僅使用磁碟
接下來，我們會指定快取僅儲存於磁碟。若您的應用程式處理大型檔案且希望保持記憶體空閒，這非常有用。
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`：此選項確保快取不會佔用記憶體，有助於處理大型 PSD 檔案而不會耗盡 RAM。

### 步驟 3：設定磁碟與記憶體快取的最大容量
現在，限制快取大小。若快取無限制，可能會導致效能問題。
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`：將磁碟快取上限設定為 1 GB。您可依需求調整此大小。  
- `Cache.setMaxMemoryForCache(1073741824)`：同理，限制記憶體快取，確保應用程式不會使用過多記憶體。

### 步驟 4：管理快取重新分配策略
快取的重新分配方式對維持效能相當重要。以下說明如何設定。
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`：設定為 `false` 時，允許 Aspose 更彈性地管理快取重新分配，從而提升效能。

### 步驟 5：檢查已分配的快取大小
此步驟用於監控目前已在記憶體或磁碟上分配的位元組數。讓我們實作它：
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`：儲存磁碟上已分配的位元組數。  
- `long l2`：儲存記憶體中已分配的位元組數。  
您可以隨時檢查這些值，以確保應用程式如預期般管理記憶體與磁碟使用。

### 步驟 6：建立 PSD 影像
快取設定完成後，讓我們建立一個簡單的 PSD 影像。
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`：此物件允許您在建立 Photoshop 影像時指定選項。  
- `Color[] color`：包含影像調色盤中將使用的顏色陣列。

### 步驟 7：將像素資料寫入影像
現在，將像素資料填入影像並儲存。
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`：顏色物件陣列，此處以白色像素填充。  
- `image.savePixels(image.getBounds(), pixels)`：此方法將像素資料寫入影像，更新影像的顏色資訊。

### 步驟 8：影像建立後監控已分配的快取
建立影像後，建議再次檢查快取的位元組分配情況。
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`：在影像建立後，捕捉磁碟上目前的分配量。  
- `long memoryBytes`：捕捉記憶體中的目前分配量。  
此步驟可協助您了解操作後快取的消耗情形。

### 步驟 9：檢查是否正確釋放
最後，務必確保所有 Aspose.PSD 物件已正確釋放，以避免記憶體洩漏。
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` 與 `l2`：這兩個變數可協助您檢查最終的分配情況。若數值不為零，表示仍有物件未被正確釋放。

## 常見問題與解決方案
- **未建立快取資料夾** – 請確認應用程式對您傳入 `Cache.setCacheFolder` 的路徑具有寫入權限。  
- **記憶體不足錯誤** – 再次確認在載入大型 PSD 檔案前已套用 `Cache.setCacheType(CacheType.CacheOnDiskOnly)`。  
- **快取大小異常** – 在每個主要操作之後使用 `Cache.getAllocated*BytesCount()` 方法追蹤快取成長。

## 常見問答

**Q: 什麼是 Aspose.PSD？**  
A: Aspose.PSD 是一套供 .NET 與 Java 開發人員以程式方式建立、操作與轉換 Photoshop (PSD) 檔案的函式庫。

**Q: 如何檢查已分配的快取大小？**  
A: 使用 `Cache.getAllocatedDiskBytesCount()` 與 `Cache.getAllocatedMemoryBytesCount()` 來監控目前的快取使用情形。

**Q: 我可以自訂快取目錄嗎？**  
A: 可以，使用 `Cache.setCacheFolder("Your Directory Path")` 來指定不同的目錄。

**Q: Aspose.PSD 可以免費使用嗎？**  
A: Aspose.PSD 為付費函式庫，但您可在其 [網站](https://releases.aspose.com/) 取得免費試用版。

**Q: 若未釋放物件會發生什麼事？**  
A: 未釋放物件會導致記憶體洩漏，使您的應用程式使用過多資源，最終可能因記憶體耗盡而當機。

## 結論
在 **create PSD image java** 應用程式中控制快取重新分配，對效能有顯著影響。依照上述步驟，您即可有效管理快取、降低記憶體消耗，並使用 Aspose.PSD for Java 產生高品質的 PSD 檔案。運用這些技巧，您的專案將運行更順暢、可擴展性更佳。

---

**最後更新：** 2026-03-13  
**測試環境：** Aspose.PSD for Java（最新發行版）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}