---
date: 2026-02-22
description: 學習如何在使用 Aspose.PSD for Java 時，實作 IPartialRawDataLoader 介面以自訂 PSD 檔案的原始資料載入。提供設定與清理的逐步指南。
linktitle: Use Custom Raw Data Loader in PSD Files - Java
second_title: Aspose.PSD Java API
title: 為 PSD 檔案實作 IPartialRawDataLoader - Java
url: /zh-hant/java/advanced-psd-layer-features-effects/use-custom-raw-data-loader-psd-files/
weight: 29
---

". The subheadings under FAQ need translation.

Make sure to keep markdown formatting.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 PSD 檔案中使用自訂原始資料載入器 - Java

## 簡介
在 Java 中處理 PSD 檔案可能會讓人感到壓力，尤其是面對原始資料時。但別擔心！透過使用 Aspose.PSD for Java，您可以輕鬆操作與擷取 PSD 檔案中的原始像素資料，方法是使用 **自訂原始資料載入器**。在本教學中，您將學會 **實作 IPartialRawDataLoader 介面**，從而精確控制像素串流。此指南將帶您一步步完成整個流程——從專案設定到資源清理——讓您自信地處理 PSD 圖層。

## 快速解答
- **自訂原始資料載入器的功能是什麼？** 它讓您在讀取 PSD 檔案時攔截並處理原始像素位元組。  
- **哪個函式庫提供此功能？** Aspose.PSD for Java 包含 `IPartialRawDataLoader` 介面。  
- **我需要授權嗎？** 免費試用版可用於測試；正式環境需購買商業授權。  
- **需要哪個 Java 版本？** Java 8 或以上（建議使用 JDK 11）。  
- **可以在多個檔案間重複使用載入器嗎？** 可以——只需實例化一次，即可在多張圖片間重複使用。

## 如何實作 IPartialRawDataLoader 介面
實作 `IPartialRawDataLoader` 介面可讓您插入自訂的原始資料載入流程。以下我們將建立一個簡易類別，滿足介面合約，並示範您可以在何處加入自己的邏輯（例如記錄、轉換、串流）。

## 什麼是自訂原始資料載入器？
**自訂原始資料載入器** 是由使用者自行實作、符合 `IPartialRawDataLoader` 介面的類別。它會接收原始像素緩衝區、矩形座標以及可選的載入選項，讓您完整掌控像素資料的讀取、轉換或儲存方式。此功能特別適用於自訂影像分析、即時顏色轉換，或在不將整張圖片載入記憶體的情況下串流大型 PSD。

## 為什麼在 Aspose.PSD 中使用自訂原始資料載入器？
- **效能調校：** 只處理所需區域，降低記憶體佔用。  
- **專屬工作流程：** 直接在像素串流上套用自有的壓縮、加密或分析。  
- **整合彈性：** 可接入現有的影像流程或第三方處理函式庫。

## 先決條件
在深入實作之前，先確保您已具備以下條件，以便在 Java 中順利使用 Aspose.PSD：

1. **基本的 Java 知識** – 熟悉 Java 程式設計是必要的。  
2. **開發環境** – IntelliJ IDEA、Eclipse，或任何具備命令列建置工具的編輯器。  
3. **Aspose.PSD 函式庫** – 從[網站](https://releases.aspose.com/psd/java/)下載 Aspose.PSD for Java 函式庫。您可以選擇免費試用版或購買授權。  
4. **Java Development Kit (JDK)** – 確認已安裝最新的 JDK。可從[Oracle 官方網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)下載，或使用 OpenJDK。  
5. **PSD 檔案知識** – 了解圖層與像素資料有助於充分利用載入器。  

一旦完成上述準備，即可開始撰寫程式碼！

## 匯入套件
要在專案中有效使用 Aspose.PSD，必須匯入相關套件。以下是自訂載入器範例所需的最小匯入：

```java
import com.aspose.psd.*;
```

這些套件提供了操作 PSD 檔案以及實作 **自訂原始資料載入器** 所需的所有類別與介面。

## 步驟 1：建立 RawDataTester 類別
第一步是定義一個實作 `IPartialRawDataLoader` 介面的類別。此類別將包含處理原始像素資料的方法。

```java
class RawDataTester implements IPartialRawDataLoader {
    public void process(Rectangle rectangle, byte[] pixels, Point start, Point end) {
        // Process raw pixel data here
    }
    public void process(Rectangle rectangle, byte[] pixels, Point start, Point end, LoadOptions loadOptions) {
        // Process raw pixel data with load options here
    }
}
```

`RawDataTester` 類別提供兩個 `process` 方法的重載。您可以依需求自行調整這些方法，以記錄像素資訊、套用自訂轉換，或將資料串流至其他服務。

## 步驟 2：設定 PSD 檔案路徑
接下來，指定存放 PSD 檔案的來源目錄。

```java
String sourceDir = "Your Source Directory";
String inFilePath = sourceDir + "CmykWithAlpha.psd";
```

將 `"Your Source Directory"` 替換為實際指向 PSD 檔案的路徑，並確保檔名與欲載入的 PSD 相符。

## 步驟 3：載入 PSD 檔案
現在，使用 `Image.load` 方法載入 PSD 檔案，取得影像的記憶體表示。

```java
RasterImage image = (RasterImage)Image.load(inFilePath);
```

將載入的物件轉型為 `RasterImage` 是必要的，因為它會公開稍後要使用的 `loadRawData` 方法。

## 步驟 4：初始化 RawDataSettings
影像載入完成後，您可以初始化 `RawDataSettings`。這些設定決定原始像素資料的處理方式。

```java
try {
    RawDataSettings rawDataSettings = image.getRawDataSettings();
```

此步驟會抽取 PSD 檔案中與原始資料相關的設定，讓您得以自訂載入行為。

## 步驟 5：使用自訂載入器載入原始資料
實例化您的自訂載入器（`RawDataTester`），並使用它從影像中載入原始資料。

```java
    RawDataTester loader = new RawDataTester();
    image.loadRawData(image.getBounds(), rawDataSettings, loader);
```

`loadRawData` 呼叫會將像素資料透過 `RawDataTester` 實作串流，讓您完整掌控每個位元組區塊。

## 步驟 6：清理資源
成功載入原始資料後，務必釋放使用過的資源，以防止記憶體洩漏。

```java
} finally {
    image.dispose();
}
```

`finally` 區塊保證無論成功或失敗，影像資源都會被正確釋放。

## 常見問題與除錯
- **路徑錯誤：** 請再次確認檔案路徑；缺少斜線或拼寫錯誤會導致 `FileNotFoundException`。  
- **型別轉換錯誤：** 確認載入的影像確實為 `RasterImage`；否則會拋出 `ClassCastException`。  
- **載入器未被呼叫：** 檢查 `RawDataTester` 方法是否正確覆寫；若未覆寫，將使用預設載入器。  
- **記憶體使用量：** 處理極大 PSD 時，建議僅載入特定矩形區域，而非整個範圍，以降低記憶體消耗。

## 常見問答
### 什麼是 Aspose.PSD for Java？
Aspose.PSD for Java 是一套函式庫，讓開發者能以程式方式操作 PSD 檔案，包括讀取、寫入與編輯 PSD 圖層。

### 如何下載 Aspose.PSD？
您可以從[發行頁面](https://releases.aspose.com/psd/java/)下載 Aspose.PSD for Java。

### 我可以免費使用 Aspose.PSD 嗎？
可以，Aspose.PSD 提供免費試用版，您可在[此處](https://releases.aspose.com/)取得。

### 如果遇到問題或需要支援該怎麼辦？
若需支援或社群協助，請前往 [Aspose 論壇](https://forum.aspose.com/c/psd/34)。

### 如何取得 Aspose.PSD 的臨時授權？
您可前往 [臨時授權頁面](https://purchase.aspose.com/temporary-license/)取得臨時授權，以評估所有功能。

---

**最後更新：** 2026-02-22  
**測試環境：** Aspose.PSD for Java（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}