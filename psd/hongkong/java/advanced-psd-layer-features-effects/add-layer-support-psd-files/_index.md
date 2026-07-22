---
date: 2026-02-17
description: 了解如何使用 Aspose.PSD for Java 提取 PSD 圖層並將其轉換為 PNG。適合需要強大圖形處理功能的開發者。
linktitle: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
  Java
second_title: Aspose.PSD Java API
title: 使用 Aspose.PSD Java 提取 PSD 圖層並為 PSD 檔案新增圖層支援
url: /zh-hant/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 提取 PSD 圖層並為 PSD 檔案新增圖層支援（使用 Aspose.PSD Java）

## 簡介
在圖形設計師與開發人員的日常工作中，處理 Photoshop Document（PSD）檔案是常見情況。最常見的任務之一是 **提取 PSD 圖層**，以便進行編輯、重複使用或轉換為其他格式，例如 PNG。在 Java 應用程式中，Aspose.PSD 讓此過程變得簡單且程式碼友好。在本教學中，我們將逐步說明如何提取 PSD 圖層、啟用圖層支援，並 **將 PSD 圖層轉換為 PNG**——提供清晰說明與實用技巧。

## 快速解答
- **什麼是「提取 PSD 圖層」？** 指載入 PSD 檔案並存取每個單獨的圖層以進行操作或匯出。  
- **哪個 Java 函式庫負責此功能？** Aspose.PSD for Java 提供完整的 PSD 處理功能，無需 Photoshop。  
- **能否一次性將 PSD 圖層轉換為 PNG？** 可以——只要使用正確的載入選項載入檔案，並以保留透明度的 PNG 選項儲存。  
- **正式環境是否需要授權？** 生產環境需要商業授權；可使用免費試用版進行評估。  
- **需要哪個 Java 版本？** JDK 8 以上（本教學以 JDK 11 為例）。

## 如何使用 Aspose.PSD for Java 擷取 PSD 圖層
以下是一個逐步指南，涵蓋從環境設定到儲存最終 PNG 的全部步驟。依照每個編號步驟操作，即可在數分鐘內得到可運作的解決方案。

## 為什麼要提取 PSD 圖層並將其轉換為 PNG？
- **重複使用資源：** 從主 PSD 中直接提取圖示、按鈕或 UI 元件，無需手動匯出。  
- **自動化：** 即時產生縮圖或適合網頁使用的圖像。  
- **保留透明度：** PNG 支援 alpha 通道，適合網頁圖形。  
- **跨平台：** 伺服器上不需要 Photoshop；Aspose.PSD 可在任何支援 Java 的環境執行。

## 前提條件

在開始之前，請確保您已具備以下條件：

1. **Java 開發環境** – 已安裝 JDK。您可以從 [Oracle 網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。
2. **Aspose.PSD for Java** – 從官方下載頁面[此處](https://releases.aspose.com/psd/java/)取得最新程式庫。
3. **Java 基礎** – 熟悉 Java 程式的編譯與運作。
4. **整合開發環境 (IDE)** – IntelliJ IDEA、Eclipse 或您喜歡的任何編輯器。
5. **PSD 文件** – 使用您現有的任何 PSD 文件，或下載一個範例 PSD 文件進行測試。

準備好這些條件後，您就可以開始擷取 PSD 圖層了。

## 導入包

首先，從 Aspose.PSD 庫導入我們需要的類別。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：定義目錄

設定來源 PSD 和輸出 PNG 的路徑。調整 `dataDir` 指向檔案所在的資料夾。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – 將 `"您的文件目錄"` 替換為**您的實際資料夾路徑**。
- `sourceFileName` – 要處理的 PSD 檔案的完整路徑。
- `output` – 包含提取圖層的 PNG 檔案的目標路徑。

## 步驟 2：設定載入選項

配置 `PsdLoadOptions` 可確保所有圖層效果和資源正確加載，這在**提取 PSD 圖層**時至關重要。

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – 載入附加到圖層的其他效果（例如陰影）。
- `setUseDiskForLoadEffectsResource(true)` – 將佔用大量資源的資源卸載到磁碟，從而減輕記憶體壓力。

## 步驟 3：載入 PSD 文件

現在，我們使用上面定義的選項將 PSD 檔案載入到 `PsdImage` 物件中。

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

此時，`image` 物件包含所有圖層、蒙版和效果，可以進行擷取。

## 步驟 4：設定儲存選項

配置 PNG 檔案的儲存方式。使用 `TruecolorWithAlpha` 可以保留原始圖層的透明度。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## 步驟 5：儲存影像（將 PSD 圖層轉換為 PNG）

將載入的 PSD 檔案（及其所有圖層）匯出為單一 PNG 檔案。此步驟有效地**一次性將 PSD 圖層轉換為 PNG**。

```java
image.save(output, saveOptions);
```

如果您需要將每個圖層作為單獨的 PNG 文件，可以遍歷 `image.getLayers()`——但對於許多用例來說，合併後的 PNG 文件就足夠了。

## 步驟 6：完成

新增一條友善的控制台訊息，以便您知道轉換過程已成功。

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## 常見問題及技巧

- **記憶體不足錯誤：** 如果您正在處理非常大的 PSD 文件，請啟用 `setUseDiskForLoadEffectsResource(true)` 以卸載臨時資料。

- **缺少效果：** 請確保已設定 `setLoadEffectsResource(true)`；否則某些圖層效果可能會被忽略。

- **路徑問題：** 使用 `java.nio.file` 中的 `Paths.get(...)` 進行**平台無關的**路徑處理。

## 常見問題解答

**問：什麼是 Aspose.PSD for Java？ ** 答：Aspose.PSD for Java 是一個函式庫，可讓您在未安裝 Photoshop 的情況下操作 PSD 檔案。

**問：我可以使用 Aspose.PSD 處理其他檔案格式嗎？ ** 答：可以！雖然 Aspose 主要用於 PSD 文件，但也提供了適用於各種其他格式的程式庫。

**問：是否有試用版？ ** 答：當然有！您可以[在此處](https://releases.aspose.com/)下載免費試用版。

**問：如果我需要幫助，哪裡可以獲得支持？ ** 答：您可以在Aspose論壇[在此處](https://forum.aspose.com/c/psd/34)取得支援。

**問：我可以將PNG轉換回PSD嗎？ ** 答：Aspose.PSD庫更著重於讀取和處理PSD文件，而不是將其他格式轉換回PSD。

**問：如何將每個圖層提取為單獨的PNG檔案？ ** 答：遍歷`image.getLayers()`，為每個圖層建立一個新的`Bitmap`對象，並使用各自的`PngOptions`屬性儲存。這樣，您就可以獲得每個圖層的單獨PNG檔案。

## 總結
現在您已學會如何 **提取 PSD 圖層**、啟用完整的圖層支援，並 **將 PSD 圖層轉換為 PNG**，使用 Aspose.PSD for Java。無論是建構自動化資產管線，或為桌面應用程式加入圖形功能，此方法皆能在不依賴 Photoshop 的情況下，提供對 Photoshop 檔案的細緻控制。歡迎進一步探索，例如套用濾鏡、程式化合併圖層，或將每個圖層個別匯出。

---

**上次更新時間：** 2026年2月17日
**測試版本：** Aspose.PSD for Java 24.11（撰寫本文時的最新版本）
**作者：** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}