---
date: 2026-01-27
description: 學習如何在 Java 中使用 Aspose.PSD 設定 JPEG 壓縮模式和顏色類型。此一步一步的指南讓圖像處理變得簡單且高效。
linktitle: Set JPEG Compression Mode and Color Type in Java
second_title: Aspose.PSD Java API
title: 在 Java 中設定 JPEG 壓縮模式與顏色類型
url: /zh-hant/java/java-jpeg-image-processing/set-jpeg-color-compression-type-java/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 設定 JPEG 壓縮模式與顏色類型於 Java

## 介紹
在當今的數位時代，管理與操作影像已成為常見需求，無論是網站開發、平面設計，或是軟體工程。如果你正在尋找一套強大的工具來處理 PSD 檔並以特定的 **jpeg compression mode** 與顏色設定轉換為 JPEG，Aspose.PSD for Java 絕對是不二之選。本教學將逐步說明，從載入 PSD 檔案到以所需的 JPEG 壓縮模式與顏色類型儲存。

## 快速解答
- **什麼程式庫在 Java 中處理 JPEG 壓縮模式？** Aspose.PSD for Java。  
- **哪個列舉設定壓縮類型？** `JpegCompressionMode`。  
- **需要多少行程式碼才能套用設定？** 只要四個簡潔的程式碼區塊。  
- **生產環境需要授權嗎？** 需要，非試用版必須購買商業授權。  
- **可以獨立變更顏色模式嗎？** 當然可以 – 使用 `JpegCompressionColorMode`。

## 什麼是 jpeg compression mode？
`jpeg compression mode` 決定影像資料在 JPEG 檔案中的編碼方式。它可以是 **baseline**（標準）或 **progressive**（漸進），這會影響檔案大小、載入行為與視覺品質。選擇適當的模式對於網站效能與儲存空間的最佳化至關重要。

## 為什麼使用 Aspose.PSD 進行 JPEG 壓縮模式？
- **完整控制** 顏色與壓縮，無需外部工具。  
- **跨平台** Java API 可在 Windows、Linux 與 macOS 上執行。  
- **無外部相依性** – 所有功能皆內建於程式庫。  
- **高保真度** 從 PSD 轉換為 JPEG，保留圖層與特效。

## 前置條件
在撰寫程式碼之前，請先確保：

1. 系統已安裝 Java Development Kit (JDK)。  
2. 已取得 Aspose.PSD for Java 程式庫。可從[官方網站](https://releases.aspose.com/psd/java/)下載。  
3. 具備基本的 Java 程式設計概念。

## 匯入套件
首先，需要從 Aspose.PSD 程式庫匯入必要的套件。這些匯入對於處理 PSD 檔案與套用 JPEG 設定至關重要。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.psd.fileformats.jpeg.JpegCompressionMode;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## 步驟 1：載入 PSD 圖像
首先，必須載入 PSD 圖像。此步驟需要指定 PSD 檔所在的目錄，並使用 Aspose.PSD 程式庫將影像讀入。

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "PsdImage.psd");
```

## 步驟 2：設定 JPEG 選項（包含 jpeg compression mode）
接著，建立 `JpegOptions` 物件，並設定其屬性以指定顏色類型與 **jpeg compression mode**。

```java
JpegOptions options = new JpegOptions();
options.setColorType(JpegCompressionColorMode.Grayscale);
options.setCompressionType(JpegCompressionMode.Progressive);
```

## 步驟 3：儲存圖像
最後，使用先前設定的選項將處理後的影像儲存。此步驟會輸出帶有指定顏色與 **jpeg compression mode** 設定的 JPEG 檔案。

```java
image.save(dataDir + "ColorTypeAndCompressionType_output.jpg", options);
```

## 常見問題與解決方案
- **不支援的顏色模式** – 請確認來源 PSD 確實包含你欲轉換的色深（例如灰階）。  
- **找不到檔案** – 請檢查 `dataDir` 是否指向正確的資料夾，且 PSD 檔名完全相符。  
- **授權未套用** – 若看到浮水印或評估訊息，請在載入影像前先加入有效的 Aspose.PSD 授權。

## 常見問答

**Q: 什麼是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一套 Java 程式庫，讓開發者能以程式方式建立、編輯與操作 PSD 與 PSB 檔案，支援廣泛的圖形設計工作。

**Q: 可以免費使用 Aspose.PSD for Java 嗎？**  
A: 可以，您可以使用[Aspose.PSD for Java 的免費試用版](https://releases.aspose.com/)。若需完整功能，必須購買授權。

**Q: 什麼是 JpegCompressionColorMode 與 JpegCompressionMode？**  
A: `JpegCompressionColorMode` 與 `JpegCompressionMode` 為 Aspose.PSD 程式庫中的列舉，分別用於指定 JPEG 圖像的顏色模式與壓縮類型。

**Q: 在哪裡可以找到 Aspose.PSD for Java 的文件說明？**  
A: 您可以在[此處](https://reference.aspose.com/psd/java/)查閱相關文件。

**Q: Aspose.PSD for Java 適合用於 Web 應用程式嗎？**  
A: 適合，Aspose.PSD for Java 可整合至 Web 應用程式，於伺服器端執行影像處理工作。

## 結論
以程式方式操作影像屬性可大幅節省時間與人力，特別是面對大量影像或複雜圖形任務時。Aspose.PSD for Java 提供強大且彈性的工具組，協助處理 PSD 檔並以特定設定轉換為 JPEG。依照本指南操作，你將能輕鬆為影像設定 JPEG 顏色與 **jpeg compression mode**。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-27  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose