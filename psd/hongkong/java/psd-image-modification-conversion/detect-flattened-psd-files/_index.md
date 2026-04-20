---
date: 2026-03-23
description: 學習如何使用 Aspose.PSD for Java 檢測已平面化的 PSD 檔案，逐步完成本完整教學。
linktitle: Detect Flattened PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD for Java 偵測已平面化的 PSD
url: /zh-hant/java/psd-image-modification-conversion/detect-flattened-psd-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 檢測已平面化的 PSD（使用 Aspose.PSD for Java）

## 介紹

如果您需要以程式方式 **detect flattened PSD** 檔案，您來對地方了。在本教學中，我們將示範如何使用 Aspose.PSD for Java 判斷 Photoshop 文件是否已被平面化——即所有圖層已合併為單一背景圖層。提前知道這點可避免日後出現意外的編輯限制。打開您喜愛的 IDE，讓我們開始吧！

## 快速解答
- **What does “flattened PSD” mean?** 所有圖層已合併為一層，失去可編輯性。  
- **Which library can detect it?** Aspose.PSD for Java 提供 `isFlatten()` 方法。  
- **Do I need a license for testing?** 可使用免費試用版；正式環境需購買授權。  
- **What Java version is required?** JDK 8 或更高版本。  
- **How long does the implementation take?** 基本檢查通常在 10 分鐘以內完成。

## 什麼是已平面化的 PSD 檔案？

已平面化的 PSD 檔案是指所有圖層已合併為單一合成圖層的 Photoshop 文件。此舉可減少檔案大小，但除非您有未平面化的備份，否則無法再進行基於圖層的編輯。

## 為何要偵測已平面化的 PSD？

提前偵測已平面化的 PSD 可讓您決定是否：

- 提示使用者提供可編輯的版本。  
- 執行全圖處理而非針對圖層的操作。  
- 避免在存取不存在的圖層時產生執行時錯誤。

## 前置條件

在深入程式碼之前，請確保您已具備以下條件：

1. **Java Development Kit (JDK)** – 版本 8 或更新。  
2. **Aspose.PSD for Java** – 從 [here](https://releases.aspose.com/psd/java/) 下載程式庫。  
3. **Basic Java knowledge** – 您應該能熟悉匯入程式庫並執行簡單的 Java 程式。  
4. **An IDE** – IntelliJ IDEA、Eclipse、NetBeans，或您偏好的任何編輯器。

現在基本條件已備妥，讓我們繼續實作。

## 匯入套件

在 Java 原始檔的最上方，匯入您需要的 Aspose.PSD 類別：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
```

## 如何偵測已平面化的 PSD 檔案

以下為逐步指南。每一步皆包含簡短說明，並附上您需要複製的完整程式碼。

### 步驟 1：設定資料目錄

指定存放欲檢查 PSD 檔案的資料夾路徑。

```java
String dataDir = "Your Document Directory"; // Update this path
```

### 步驟 2：載入 PSD 檔案

使用 `Image.load()` 將 PSD 檔案載入為 `PsdImage` 物件。

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

### 步驟 3：檢查 PSD 是否已平面化

呼叫 `isFlatten()` 方法。若檔案已平面化則回傳 `true`，否則回傳 `false`。

```java
System.out.println(psdImage.isFlatten());
```

控制台將會輸出 `true`（已平面化的文件）或 `false`（仍包含獨立圖層的文件）。

## 常見問題與解決方案

- **FileNotFoundException** – 請確認 `dataDir` 指向正確的資料夾，且檔名完全相符（包括大小寫）。  
- **Unsupported file format** – 請確保檔案為有效的 PSD；其他相容的 Photoshop 格式（例如 PSB）可能需要不同的處理方式。  
- **LicenseException** – 若出現授權錯誤，請安裝有效的 Aspose.PSD 授權，或使用試用版進行評估。

## 常見問答

**Q: What is a flattened PSD file?**  
A: 已平面化的 PSD 檔案將所有圖層合併為單一背景圖層，因而無法再進行基於圖層的編輯。

**Q: Can I unflatten a PSD file after it’s flattened?**  
A: 不能。圖層一旦合併，除非有未平面化的備份，否則無法復原原始圖層結構。

**Q: Does Aspose.PSD support other file formats?**  
A: 支援。Aspose.PSD 可處理 PSD、PSB、BMP、JPEG、PNG、TIFF 等多種影像格式。

**Q: How do I get started with Aspose?**  
A: 只需從 [here](https://releases.aspose.com/psd/java/) 下載程式庫，並將 JAR 檔案加入專案的 classpath 即可。

**Q: Is there a way to test Aspose.PSD for free?**  
A: 當然！您可從 [this link](https://releases.aspose.com/) 下載試用版，開始免費試用。

## 結論

現在您已了解如何使用 Aspose.PSD for Java **detect flattened PSD** 檔案。此簡單檢查可協助您為影像選擇正確的處理流程，避免意外的編輯障礙。歡迎探索 Aspose.PSD 的其他功能，如圖層操作、影像轉換與中繼資料處理，以進一步提升工作流程。

---

**最後更新：** 2026-03-23  
**測試環境：** Aspose.PSD for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}