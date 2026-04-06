---
date: 2025-12-30
description: 學習如何使用 Aspose.PSD 在 Java 中結合兩張圖片來建立 PSD 檔案。跟隨我們的逐步指南，快速將圖片合併成 PSD 檔案。
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: 如何在 Java 中建立 PSD 檔案 – 使用 Aspose.PSD 合併圖像
url: /zh-hant/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中建立 PSD 檔案 – 使用 Aspose.PSD 合併圖像

## 簡介

如果您需要透過合併多張圖片 **在 Java 中建立 PSD 檔案**，Aspose.PSD 讓這項工作變得簡單。在本教學中，我們將示範如何將兩張圖片合併到同一個 PSD 畫布，說明此方法的好處，並提供可直接執行的程式碼。完成後，您將能以 **Java 方式合併兩張圖片**，並產生具專業外觀的分層檔案。

## 快速解答
- **哪個函式庫最適合將圖像合併成 PSD？** Aspose.PSD for Java。  
- **實作需要多長時間？** 基本合併約 10‑15 分鐘。  
- **需要授權嗎？** 免費試用可用於測試；正式上線需購買商業授權。  
- **可以加入超過兩張圖像嗎？** 可以 – 為每個額外圖層重複 `drawImage` 呼叫。  
- **支援哪個 Java 版本？** Java 8 及更新版本。

## 先決條件

在開始之前，請確保您已具備以下項目：

1. **Aspose.PSD Library** – download it from [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – Java 8+ is recommended.  
3. **Document Directory** – a folder on your machine where the source images and the resulting PSD will be stored.

## 匯入套件

首先在專案中匯入所需的 Aspose.PSD 類別：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## 逐步指南

### 步驟 1：建立 PSD 選項（準備檔案）

我們首先建立一個 `PsdOptions` 實例，用於保存輸出設定。

```java
PsdOptions imageOptions = new PsdOptions();
```

### 步驟 2：設定 FileCreateSource（定義 PSD 的儲存位置）

將 `FileCreateSource` 指派給選項，指向目標結果檔案。

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### 步驟 3：建立 Image 實例（初始化畫布大小）

使用該選項建立 `Image` 物件，並指定 600 × 600 像素的畫布。

```java
Image image = Image.create(imageOptions, 600, 600);
```

### 步驟 4：初始化 Graphics 並繪製第一張圖片

`Graphics` 物件讓我們在畫布上繪圖。我們先將背景清除為白色，然後在左半部繪製第一個來源圖像。

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### 步驟 5：繪製第二張圖片（完成合併）

現在我們將第二張圖像放置在同一畫布的右半部。

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### 步驟 6：儲存產生的 PSD 檔案

最後，將合併後的畫布寫入磁碟。

```java
image.save();
```

恭喜！您已成功 **將圖像合併為 PSD**，並在 Java 中建立了 PSD 檔案。

## 為什麼使用 Aspose.PSD 合併圖像？

- **Layer‑aware** – each `drawImage` call adds a separate layer you can edit later.  
- **Format flexibility** – supports PSD, PNG, JPEG, BMP, and more.  
- **No native dependencies** – pure Java, works on any OS that runs the JDK.  

## 常見問題與解決方案

| Issue | Cause | Fix |
|-------|-------|-----|
| `File not found` error when loading source images | Incorrect `dataDir` path | Verify `dataDir` points to the folder containing `example1.psd` and `example2.psd`. |
| Output PSD is blank | `graphics.clear` called after drawing | Ensure `graphics.clear(Color.getWhite())` is executed **before** any `drawImage` calls. |
| License exception at runtime | Missing or expired Aspose.PSD license | Apply a valid license using `License license = new License(); license.setLicense("Aspose.PSD.lic");` before any API call. |

## 常見問答

### Q1：Aspose.PSD 是否相容所有圖像格式？

A1：Aspose.PSD 主要聚焦於 PSD 檔案格式，但亦支援多種其他格式的輸入與輸出。

### Q2：我可以對合併後的圖像進行其他修改嗎？

A2：當然可以！合併圖像後，您可以使用 Aspose.PSD 的豐富功能進一步操作產生的 PSD。

### Q3：使用 Aspose.PSD 是否有授權需求？

A3：是的，商業使用需有效授權。可從 [here](https://purchase.aspose.com/buy) 取得。

### Q4：Aspose.PSD 是否提供免費試用？

A4：是的，您可透過免費試用在 [here](https://releases.aspose.com/) 體驗 Aspose.PSD。

### Q5：在哪裡可以取得 Aspose.PSD 相關支援？

A5：請前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 取得社群支援與討論。

---

**Last Updated:** 2025-12-30  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}