---
date: 2026-01-01
description: 了解如何使用 Aspose.PSD 在 Java 中建立 PSD 圖像。本指南示範如何設定路徑以及使用 Java 建立 Photoshop
  文件，並提供逐步程式碼說明。
linktitle: Create Image by Setting Path
second_title: Aspose.PSD Java API
title: 如何建立 PSD – 於 Aspose.PSD for Java 中設定路徑以建立圖像
url: /zh-hant/java/image-editing/create-image-by-setting-path/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何建立 PSD – 透過設定路徑在 Aspose.PSD for Java 中建立影像

## 介紹

歡迎閱讀本步驟教學，說明如何使用 Aspose.PSD for Java **建立 PSD** 影像。我們將帶領您設定檔案路徑、配置選項，並以程式方式產生 Photoshop 文件。完成後，您將了解如何 **java create photoshop document** 檔案，並可進一步編輯或整合至您的應用程式中。

## 快速解答
- **Aspose.PSD 的功能是什麼？** 它提供純 Java API，能在不安裝 Photoshop 的情況下讀取、編輯與建立 Photoshop (PSD) 檔案。  
- **我可以設定自訂輸出路徑嗎？** 可以 – 使用 `FileCreateSource` 來指定精確的位置與檔名。  
- **支援哪些壓縮方式？** RLE、ZIP 與 RAW；本範例使用 RLE 進行無損壓縮。  
- **開發時需要授權嗎？** 免費試用版可用於測試；正式上線需購買商業授權。  
- **支援哪些 Java 版本？** Aspose.PSD 相容於 Java 8 及以上版本。

## 什麼是「如何建立 PSD」？

建立 PSD 檔案即是產生相容於 Photoshop 的影像，保留圖層、通道及其他 Photoshop 專屬資料。Aspose.PSD 抽象化了複雜的檔案格式，讓您專注於業務邏輯。

## 為什麼使用 Java 來 **java create photoshop document**？

- **跨平台** – Java 可在任何環境執行，讓您的 PSD 產生可在 Windows、Linux 或 macOS 上運作。  
- **無需 Photoshop 依賴** – 可在未安裝 Adobe Photoshop 的情況下產生或修改 PSD 檔案。  
- **完整控制** – 透過簡潔的物件模型設定壓縮方式、色彩模式、尺寸等。

## 前置條件

在開始之前，請確保您已具備：

- 基本的 Java 程式設計知識。  
- 已安裝 Aspose.PSD for Java 套件。您可於 [here](https://releases.aspose.com/psd/java/) 下載。

## 匯入套件

在您的 Java 專案中匯入必要的套件：

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## 步驟 1：設定文件目錄的路徑

設定影像將被建立的文件目錄路徑。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：定義輸出檔名

定義輸出檔名，並包含文件目錄路徑。

```java
String desName = dataDir + "CreatingAnImageBySettingPath_out.psd";
```

## 步驟 3：設定 PsdOptions

建立 `PsdOptions` 實例，並設定其屬性，例如壓縮方式。

```java
PsdOptions psdOptions = new PsdOptions();
psdOptions.setCompressionMethod(CompressionMethod.RLE);
```

## 步驟 4：設定 Source 屬性

為 `PsdOptions` 實例定義 source 屬性，指定輸出檔案及其是否為暫存檔。

```java
psdOptions.setSource(new FileCreateSource(desName, false));
```

## 步驟 5：建立 Image

建立 `Image` 實例，並傳入 `PsdOptions` 物件與影像尺寸，呼叫 `create` 方法。

```java
Image image = Image.create(psdOptions, 500, 500);
```

## 步驟 6：儲存影像

儲存已建立的影像。

```java
image.save();
```

重複上述步驟，即可成功使用 Aspose.PSD for Java 透過設定路徑建立影像。

## 常見問題與技巧

- **目錄無效** – 確認 `dataDir` 以正確的檔案分隔符結尾（`/` 或 `\\`）。  
- **權限錯誤** – 以對目標資料夾具有寫入權限的方式執行應用程式。  
- **未設定授權** – 若收到授權例外，請在建立影像前載入 Aspose.PSD 授權。

## 結論

在本教學中，我們說明了如何使用 Aspose.PSD for Java **建立 PSD** 檔案，示範了 **如何設定路徑**，並展示了產生 Photoshop 文件的完整流程。此方式讓 Java 開發者能將 PSD 建立直接嵌入工作流程，無論是自動化報表、動態圖形或批次處理皆適用。

## 常見問答

### Q1：Aspose.PSD 是否相容於不同的 Java IDE？

A1：是的，Aspose.PSD 可無縫運作於各種 Java 整合開發環境 (IDE)。

### Q2：我可以在商業專案中使用 Aspose.PSD 嗎？

A2：可以，您可在個人或商業專案中使用 Aspose.PSD。請參閱 [purchase page](https://purchase.aspose.com/buy) 了解授權細節。

### Q3：如何取得 Aspose.PSD 的支援？

A3：請前往 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 取得社群支援與討論。

### Q4：是否提供免費試用？

A4：是的，您可於 [here](https://releases.aspose.com/) 取得免費試用。

### Q5：測試是否需要臨時授權？

A5：您可於 [here](https://purchase.aspose.com/temporary-license/) 取得測試用臨時授權。

**Q：建立後可以變更影像尺寸嗎？**  
A：可以，您可在儲存前使用 `image.resize(width, height)` 重新調整尺寸。

**Q：支援哪些色彩模式？**  
A：Aspose.PSD 支援 RGB、CMYK、灰階與索引色模式。

---

**最後更新：** 2026-01-01  
**測試版本：** Aspose.PSD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}