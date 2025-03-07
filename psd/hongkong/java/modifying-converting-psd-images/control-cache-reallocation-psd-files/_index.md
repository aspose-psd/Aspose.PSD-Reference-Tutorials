---
title: 控制 PSD 檔案中的快取重新分配
linktitle: 控制 PSD 檔案中的快取重新分配
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD for Java 管理 PSD 檔案中的快取重新分配。了解如何有效優化記憶體和檔案處理—這對於開發人員來說是理想的選擇。
weight: 22
url: /zh-hant/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 控制 PSD 檔案中的快取重新分配

## 介紹
當以程式方式處理影像和 Photoshop 檔案時，效率是關鍵因素。 Aspose.PSD for Java 提供了強大的功能來無縫管理和操作 PSD 檔案。優化效能的基本面向之一是控制快取重新分配。快取管理有助於保持記憶體和磁碟使用之間的平衡，確保您的應用程式平穩運行，不會出現意外崩潰或速度減慢。 
## 先決條件
在我們進入編碼部分之前，您需要確保以下幾點，以便一切順利運行：
1. Java 開發工具包 (JDK)：確保您的電腦上安裝了 JDK。您可以從以下位置下載：[甲骨文網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java：您需要下載Aspose.PSD庫。您可以找到最新版本[這裡](https://releases.aspose.com/psd/java/).
3. IDE 設定：像 IntelliJ IDEA 或 Eclipse 這樣的整合開發環境 (IDE) 將使您更輕鬆地管理程式碼。
4. 對 Java 的基本了解：熟悉 Java 程式設計將幫助您更好地理解概念和程式碼片段。
5.  Aspose 許可證（選購）：如果您希望刪除浮水印並獲得完整功能，請考慮購買許可證[這裡](https://purchase.aspose.com/buy)或嘗試免費試用[這裡](https://releases.aspose.com/).
## 導入包
在開始編寫程式碼之前，我們先確保導入了必要的套件。以下是 Java 檔案開頭應包含的內容的簡要清單：
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
## 第 1 步：設定您的資料目錄
首先，您需要設定一個用於儲存快取檔案的目錄。這對於有效管理快取至關重要。
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- 字串 dataDir：定義文件快取的目錄。
- Cache.setCacheFolder(dataDir)：此方法將快取資料夾設定到指定目錄。 Aspose 建立的任何快取現在都將儲存在此處，而不是預設的暫存目錄。
## 步驟 2：配置快取到磁碟
接下來，我們將指定我們希望快取僅儲存在磁碟上。如果您的應用程式使用大檔案並且您希望確保記憶體保持空閒，這尤其有用。
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly)：此選項可確保快取不會儲存在記憶體中，這有利於處理大型 PSD 檔案而不消耗太多 RAM。
## 步驟 3：設定最大磁碟和記憶體快取大小
現在，讓我們限制快取大小。這一點至關重要，因為無限的快取可能會導致效能問題。
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1GB
Cache.setMaxMemoryForCache(1073741824); // 1GB
```

- Cache.setMaxDiskSpaceForCache(1073741824)：這為磁碟上的快取設定了 1 GB 的限制。您可以根據需要調整此大小。
- Cache.setMaxMemoryForCache(1073741824)：同樣，這會限制記憶體中的緩存，確保您的應用程式不會使用過多的記憶體。
## 第 4 步：管理快取重新分配策略
管理快取的重新分配方式對於維持效能至關重要。以下是設定方法。
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false)：當設定為 false 時，這允許 Aspose 更靈活地管理快取重新分配，從而帶來更好的效能。
## 第 5 步：檢查分配的快取大小
此步驟是關於監視目前在記憶體或磁碟上為快取分配了多少位元組。讓我們實現一下：
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- 長 l1：儲存磁碟上分配的位元組數。
- long l2：儲存記憶體中分配的位元組數。 
您可以隨時檢查這些值，以確保您的應用程式按預期管理記憶體和磁碟使用量。
## 第 6 步：建立 PSD 映像
現在我們已經設定了快取配置，讓我們建立一個簡單的 PSD 映像。
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- PsdOptions 選項：此物件可讓您在建立 Photoshop 影像時指定選項。
- 顏色[color：包含將在影像調色盤中使用的顏色的陣列。
## 步驟 7：將像素資料儲存到影像中
現在，讓我們用像素資料填充圖像並保存它。
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- 顏色[] 像素：這是顏色物件的陣列。在這裡，我們用白色像素填充它。
- image.savePixels(image.getBounds(), Pixels)：此方法將像素資料儲存到影像中。它用我們定義的顏色更新圖像。
## 步驟 8：建立映像後監控指派的快取
創建圖像後，最好再次檢查為快取分配了多少位元組。
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes：建立映像後捕獲磁碟上的目前分配。
- long memoryBytes：捕獲記憶體中的目前分配。 
此步驟將幫助您確定操作後消耗了多少快取。
## 第 9 步：檢查是否正確處置
最後，確保正確處理所有 Aspose.PSD 物件以避免記憶體洩漏至關重要。
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 和 l2：這些變數將幫助您檢查最終分配。如果它們不為零，則表示某些物體尚未正確處置。
## 結論
控制 Aspose.PSD for Java 中的快取重新分配可以顯著提高應用程式的效能。透過執行上述步驟，您可以有效地管理快取、最大限度地減少記憶體使用並有效率地建立精美的 PSD 檔案。擁抱這些技術，看著您的應用程式以最佳效能蓬勃發展！
## 常見問題解答
### 什麼是 Aspose.PSD？
Aspose.PSD 是一個供 .NET 和 Java 開發人員以程式設計方式建立、操作和轉換 Photoshop (PSD) 檔案的程式庫。
### 如何檢查分配的快取大小？
使用類似的方法`Cache.getAllocatedDiskBytesCount()`和`Cache.getAllocatedMemoryBytesCount()`監控當前快取使用情況。
### 我可以為快取設定自訂目錄嗎？
是的，您可以使用指定不同的目錄`Cache.setCacheFolder("Your Directory Path")`.
### Aspose.PSD 可以免費使用嗎？
Aspose.PSD 是一個付費庫，但您可以從他們的免費試用版開始[網站](https://releases.aspose.com/).
### 如果我不丟棄物品會怎樣？
不釋放物件可能會導致記憶體洩漏，導致應用程式使用不必要的資源。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
