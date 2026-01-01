---
date: 2026-01-01
description: 學習如何在 Aspose.PSD 中使用串流建立 Java 位圖、儲存影像檔案，以及有效設定每像素位元數。
linktitle: Create Image using Stream
second_title: Aspose.PSD Java API
title: 在 Aspose.PSD 中使用 Stream 建立 Java 位圖
url: /zh-hant/java/image-editing/create-image-using-stream/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Stream 在 Aspose.PSD 中建立 bitmap java

## 簡介

如果您需要即時 **create bitmap java** 圖像，Aspose.PSD for Java 為您提供乾淨、基於串流的方式，既快速又節省記憶體。在本教學中，我們將逐步說明如何從串流產生 bitmap 圖像、設定每像素位元數，最後 **save image file java** 至磁碟。完成後，您將了解為何此方法非常適合伺服器端影像處理、批次工作或任何希望避免暫存檔的情境。

## 快速解答
- **「create bitmap java」是什麼意思？** 它指的是使用 Java 程式碼以程式方式產生 BMP 圖像。  
- **哪個函式庫負責處理串流？** Aspose.PSD 的 `StreamSource` 與 `FileCreateSource` 類別。  
- **我可以設定顏色深度嗎？** 可以 – 使用 `BmpOptions.setBitsPerPixel(int)`（例如 24 bpp）。  
- **如何儲存結果？** 呼叫 `image.save(outputPath)` 以 **save image file java**。  
- **在正式環境需要授權嗎？** 商業使用需具備有效的 Aspose.PSD 授權。

## 建立 bitmap java 的先決條件

在開始之前，請確保您已具備以下項目：

- **Java Development Kit (JDK)** – 任意近期版本（8 或以上）。  
- **Aspose.PSD for Java** – 從[文件說明](https://reference.aspose.com/psd/java/)下載最新的 JAR。  
- **IDE** – Eclipse、IntelliJ IDEA，或您偏好的任何 Java 相容編輯器。

## 匯入 bitmap 產生所需的套件

首先匯入所需的命名空間。這些讓您能使用影像建立、BMP 選項與串流處理功能。

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.BmpOptions;
import com.aspose.psd.sources.FileCreateSource;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.Stream;
import java.io.FileInputStream;
```

## 步驟 1：設定文件目錄

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為您存放來源與輸出檔案的絕對路徑。

## 步驟 2：定義輸出檔案名稱

```java
String desName = dataDir + "CreatingImageUsingStream_out.bmp";
```

此路徑即 **save image file java** 操作寫入 bitmap 的位置。

## 步驟 3：設定 BmpOptions（設定每像素位元數）

```java
BmpOptions imageOptions = new BmpOptions();
imageOptions.setBitsPerPixel(24);
```

此處我們 **set bits per pixel** 為 24 bpp，產生真彩色 bitmap。如需其他顏色深度，請調整此數值。

## 步驟 4：建立 FileCreateSource（串流來源）

```java
FileCreateSource stream = new FileCreateSource(dataDir + "sample_out.bmp");
imageOptions.setSource(stream);
```

`FileCreateSource` 包裝檔案串流，使 Aspose.PSD 能直接寫入目標而無需中間緩衝區。

## 步驟 5：產生 Bitmap 圖像

```java
Image image = Image.create(imageOptions, 500, 500);
```

此行使用先前定義的選項 **generates a bitmap java** 產生 500 × 500 像素的圖像。

## 步驟 6：執行影像處理並儲存

```java
// Perform desired image processing operations here
// For example, you could draw shapes, apply filters, etc.

// Save the processed bitmap to disk
image.save(desName);
```

在完成任何可選的操作後，呼叫 `image.save` 會 **saves the image file java** 至 `desName` 指定的位置。

## 結論

您現在已學會如何在 Aspose.PSD 中使用串流 **create bitmap java** 圖像、透過 **set bits per pixel** 控制顏色深度，並高效 **save image file java**。請嘗試不同的尺寸、像素格式或額外的處理步驟，以符合您的專案需求。

## 常見問題

### Q1: 我可以將 Aspose.PSD 與其他 Java 函式庫一起使用嗎？

A1: 可以，Aspose.PSD 設計為能無縫整合其他 Java 函式庫，為您的專案提供多樣性。

### Q2: 我可以在哪裡取得 Aspose.PSD 相關問題的支援？

A2: 前往 [Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34) 獲取社群支援與討論。

### Q3: 是否提供 Aspose.PSD 的免費試用？

A3: 有，您可在[此處](https://releases.aspose.com/)取得免費試用。

### Q4: 如何取得 Aspose.PSD 的臨時授權？

A4: 請於[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。

### Q5: Aspose.PSD 的系統需求是什麼？

A5: 請參考[文件說明](https://reference.aspose.com/psd/java/)以取得詳細系統需求。

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD Java latest release  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}