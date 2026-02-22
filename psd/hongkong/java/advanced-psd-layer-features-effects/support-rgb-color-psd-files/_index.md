---
date: 2026-02-22
description: 學習如何將 PSD 轉換為 JPEG、將 PSD 匯出為 JPG，並在 Java 中使用 Aspose.PSD 設定 JPEG 品質。完整的
  Aspose.PSD 教程，適用於鮮豔的 RGB 圖像。
linktitle: Convert PSD to JPEG and Support RGB Color with Aspose.PSD Java
second_title: Aspose.PSD Java API
title: 將 PSD 轉換為 JPEG 並支援 RGB 色彩（使用 Aspose.PSD Java）
url: /zh-hant/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/
weight: 20
---

.PSD Java". Keep style.

Then "## Introduction" translate.

Then paragraph: translate.

Need to keep **bold** parts.

Also keep code snippets placeholders.

Also lists.

Also table.

Also FAQ.

Also last updated etc.

Let's produce translation.

Be careful not to translate URLs.

Also not translate code block placeholders.

Also not translate file names like `inRgb16.psd`.

Also not translate variable names.

Also not translate "JpegOptions" etc.

Now produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 轉換為 JPEG 並支援 RGB 顏色 – Aspose.PSD Java

## 介紹
在程式化處理 Photoshop 檔案時，**將 PSD 轉換為 JPEG** 並使用鮮豔的 RGB 色彩模式是開發人員必備的能力。Aspose.PSD for Java 提供一個功能強大、易於使用的框架，讓您可以 **將 PSD 匯出為 JPG**、調整影像品質，並保留每通道 16 位元的資料。在本教學中，我們將一步步示範完整的 **aspose psd tutorial**，說明如何載入 RGB PSD、在 Java 中設定 JPEG 品質，並將結果同時儲存為 PSD 與 JPEG 檔案。戴上程式碼帽子，讓我們一起踏入多彩的影像處理世界吧！

## 快速答覆
- **Aspose.PSD 能讀取 16 位元 RGB PSD 檔案嗎？** 能，完整支援每通道 16 位元的 RGB 影像。  
- **哪個方法可將 PSD 轉換為 JPEG？** 使用 `image.save(outputPath, new JpegOptions())`。  
- **如何在 Java 中設定 JPEG 品質？** 在 `JpegOptions` 實例上呼叫 `saveOptions.setQuality(100)`。  
- **正式環境需要授權嗎？** 生產環境必須購買商業授權；亦提供免費試用版。  
- **相同程式碼可用於其他格式嗎？** 可以，Aspose.PSD 亦支援 PNG、BMP、TIFF 等格式，使用方式類似。

## 什麼是「將 PSD 轉換為 JPEG」？
將 PSD 檔案轉換為 JPEG 意指將多層的 Photoshop 文件合併、平面化，並以壓縮的 JPEG 影像格式編碼。當您需要輕量、適合網路使用的設計稿，同時保留原始 PSD 以便未來編輯時，這個功能就非常有用。

## 為什麼要將 PSD 轉換為 JPEG？
- **可攜性：** JPEG 檔案在瀏覽器、行動裝置與文件編輯器上皆得到普遍支援。  
- **檔案縮小：** JPEG 壓縮可大幅減少檔案大小，相較於原始 PSD 更易傳輸。  
- **快速分享：** 非常適合用於預覽、客戶審核或嵌入報告中。  
- **工作流程一致：** 若需在批次處理中 **將 Photoshop 轉換為 JPEG**，只要呼叫相同的 API，即可免除自行撰寫影像處理程式碼。

## 常見使用情境
- 為線上作品集產生縮圖預覽。  
- 從設計流程匯出最終作品，以在網站上展示。  
- 自動化電子報的影像準備，JPEG 為必需格式。

## 前置條件
在開始編寫程式碼之前，請先確保您具備以下項目：

1. **Java Development Kit (JDK)** – 任一近期版本（8 以上）。  
2. **Aspose.PSD for Java** – 前往 **[此處](https://releases.aspose.com/psd/java/)** 下載程式庫。  
3. **IDE** – IntelliJ IDEA、Eclipse、NetBeans，或任何支援 Java 的編輯器。  
4. **基本的 Java 知識** – 必須熟悉類別與方法的使用。  
5. **範例 PSD 檔案** – 例如 `inRgb16.psd` 的 RGB 檔案，用於測試。

## 匯入套件
在進入主要邏輯之前，先匯入必要的類別：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.JpegOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 步驟說明

### 步驟 1：設定文件目錄
定義存放 PSD 檔案的資料夾路徑。

```java
String dataDir = "Your Document Directory";
```

*將 `"Your Document Directory"` 替換為您機器上實際的路徑。*

### 步驟 2：定義檔案名稱
指定輸入的 PSD 以及 JPEG 與 PSD 的輸出路徑。

```java
String sourceFileName = dataDir + "inRgb16.psd";
String outputFilePathJpg = dataDir + "outRgb16.jpg";
String outputFilePathPsd = dataDir + "outRgb16.psd";
```

### 步驟 3：建立 `PsdLoadOptions`
實例化 `PsdLoadOptions` 以控制 PSD 的載入方式。

```java
PsdLoadOptions options = new PsdLoadOptions();
```

### 步驟 4：載入 PSD 影像
使用上述建立的選項載入來源檔案。

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, options);
```

### 步驟 5：儲存 PSD 檔案（可選）
如果需要在處理後保留副本，可再次以 PSD 格式儲存。

```java
image.save(outputFilePathPsd, new PsdOptions(image));
```

### 步驟 6：準備 JPEG 選項 – *set jpeg quality java*
設定 JPEG 輸出參數，特別是品質等級。

```java
JpegOptions saveOptions = new JpegOptions();
saveOptions.setQuality(100);
```

### 步驟 7：儲存為 JPEG – *convert PSD to JPEG*
最後，將影像匯出為 JPEG 檔案。

```java
image.save(outputFilePathJpg, saveOptions);
```

## 如何在 Java 中設定 JPEG 品質？
`JpegOptions` 類別提供對輸出品質的細緻控制。透過呼叫 `setQuality(int)`，您可以指定壓縮程度（0‑100）。數值 **100** 代表保留最高視覺忠實度，較低的數值則會以較小檔案大小換取畫質下降。

## 常見問題與解決方案
| 問題 | 解決方案 |
|------|----------|
| **轉換後影像顏色暗淡** | 確認來源 PSD 為 RGB 模式；CMYK PSD 必須先轉換色彩配置檔才能儲存為 JPEG。 |
| **大型檔案導致 OutOfMemoryError** | 增加 JVM 堆積大小（`-Xmx2g`）或使用 `PsdImage` API 以分塊方式處理影像。 |
| **JPEG 品質未生效** | 確認已將 `JpegOptions` 實例傳遞給 `image.save()`；預設品質為 75。 |

## 常見問答

**Q: 我可以在其他程式語言中使用 Aspose.PSD 嗎？**  
A: 可以，Aspose.PSD 亦提供 .NET、Python 等平台的版本，詳情請參閱官方網站。

**Q: Aspose.PSD 有免費試用嗎？**  
A: 當然！您可以在 **[此處](https://releases.aspose.com/)** 取得免費試用。

**Q: 如何取得 Aspose 產品的支援？**  
A: 如需諮詢與協助，請前往 **[Aspose 支援論壇](https://forum.aspose.com/c/psd/34)**。

**Q: 能否使用 Aspose 於 PSD 影像套用濾鏡或特效？**  
A: 可以，Aspose.PSD 提供豐富的 API 供圖層操作、濾鏡與特效使用。

**Q: Aspose.PSD for Java 對初學者友善嗎？**  
A: 只要具備基本的 Java 知識，配合完整的文件與範例，即可輕鬆上手。

---

**最後更新：** 2026-02-22  
**測試環境：** Aspose.PSD for Java 24.12（最新）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}