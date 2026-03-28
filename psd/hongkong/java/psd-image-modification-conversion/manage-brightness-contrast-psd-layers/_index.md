---
date: 2026-03-28
description: 學習如何使用 Aspose.PSD for Java 調整 PSD 的亮度，包括如何更改 PSD 圖層的亮度與對比度。適合開發人員與平面設計師。
linktitle: Adjust Brightness PSD Java – Manage Brightness & Contrast
second_title: Aspose.PSD Java API
title: 調整亮度 PSD Java – 管理亮度與對比度
url: /zh-hant/java/psd-image-modification-conversion/manage-brightness-contrast-psd-layers/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 調整亮度 PSD Java – 管理亮度與對比

## 介紹

您是經常處理 PSD（Photoshop Document）檔案的平面設計師或開發人員嗎？是否需要在不離開 Java 環境的情況下快速且可靠地 **adjust brightness psd java**？在本教學中，我們將示範如何使用 Aspose.PSD for Java 來變更 PSD 圖層的亮度與對比度。您將獲得可重複使用的程式碼片段，能整合至任何自動化影像處理流程。讓我們捲起袖子，立即開始吧！

## 快速回答
- **需要哪個函式庫？** Aspose.PSD for Java  
- **可以一次變更多個圖層嗎？** 可以 – 只要遍歷所有 `BrightnessContrastLayer` 物件。  
- **需要哪個 Java 版本？** JDK 8 或以上。  
- **正式環境需要授權嗎？** 需要，非評估用途必須使用商業授權。  
- **程式碼是否相容於 Maven/Gradle 專案？** 完全相容 – 只要加入 Aspose.PSD 相依性即可。

## 什麼是 “adjust brightness psd java”？

在 Java 中調整 PSD 檔案的亮度，意指以程式方式修改 `BrightnessContrastLayer` 的數值，讓您能自動化原本必須在 Photoshop 手動完成的視覺微調。

## 為什麼要在 PSD 圖層中調整亮度與對比度？

- **加速批次處理** – 非常適合大型設計庫。  
- **保留圖層結構** – 只會變更目標調整圖層，保留遮色片與效果。  
- **整合至 CI/CD 流程** – 自動產生預覽圖或縮圖。

## 前置條件

在開始這段使用 Java 操作 PSD 檔案的精彩旅程之前，請先確保已正確安裝以下項目。以下是完成本教學所需的條件：

1. **Java Development Kit (JDK)** – 請確保已在機器上安裝 JDK 8 以上版本。可從 [Oracle 的網站](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html) 下載。  
2. **Aspose.PSD for Java Library** – 操作 PSD 檔案必須使用 Aspose.PSD 函式庫。可從 [release page](https://releases.aspose.com/psd/java/) 下載最新版本。  
3. **您慣用的 IDE** – 建議使用 IntelliJ IDEA、Eclipse 或 NetBeans 等整合開發環境撰寫與執行 Java 程式碼。  
4. **基本的 Java 知識** – 熟悉 Java 程式語言有助於理解本文的程式碼片段。

完成上述前置作業後，即可繼續。現在，打開您最喜愛的程式碼編輯器，開始編寫程式吧！

## 匯入套件

在編寫程式之前，首先需要匯入必要的套件。使用 Aspose.PSD 前，請確保已將函式庫加入 classpath。以下示範如何完成此步驟：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BrightnessContrastLayer;
```

完成上述設定後，即可順利使用 Aspose.PSD 處理 PSD 檔案！

現在，我們已經準備就緒，接下來進入本教學的核心：調整 PSD 圖層的亮度與對比度。以下步驟將清晰說明每個操作，方便您跟隨。

## 步驟 1：定義文件目錄

先設定 PSD 檔案所在的目錄，以便統一管理檔案。

```java
String dataDir = "Your Document Directory";
```

將 `"Your Document Directory"` 替換為實際的 PSD 檔案資料夾路徑。

## 步驟 2：指定來源與目的檔名

接著，設定來源 PSD 檔名以及編輯後要儲存的目的檔名。

```java
String sourceFileName = dataDir + "BrightnessContrastModern.psd";
String psdPathAfterChange = dataDir + "BrightnessContrastModernChanged.psd";
```

此範例假設目錄中已有名為 `BrightnessContrastModern.psd` 的檔案。

## 步驟 3：載入 PSD 檔案

現在將 PSD 檔案載入程式，以便後續操作。

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

上述程式碼會建立 `PsdImage` 例項，代表您的 PSD 檔案，之後即可存取所有圖層。

## 步驟 4：遍歷圖層

接下來遍歷 PSD 中的每一個圖層，找出可調整亮度與對比度的圖層。

```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof BrightnessContrastLayer) {
        BrightnessContrastLayer brightnessContrastLayer = (BrightnessContrastLayer)im.getLayers()[i];
```

`for` 迴圈會逐一檢查每個圖層，若圖層是 `BrightnessContrastLayer` 的實例，即可進行後續調整。

## 步驟 5：調整亮度與對比度

在迴圈內，為每個 `BrightnessContrastLayer` 設定亮度與對比度。

```java
        brightnessContrastLayer.setBrightness(50);
        brightnessContrastLayer.setContrast(50);
    }
}
```

本例將亮度與對比度皆設為 `50`。您可依需求自行調整數值，數值越高亮度/對比度越強，數值越低則相反。

## 步驟 6：儲存變更

最後，將修改後的 PSD 檔案寫回指定的目的路徑。

```java
im.save(psdPathAfterChange);
```

上述程式碼會以新的亮度與對比度設定儲存編輯後的 PSD 檔案。

## 常見問題與解決方案

| 問題 | 發生原因 | 解決方案 |
|------|----------|----------|
| **找不到 `BrightnessContrastLayer`** | PSD 可能使用其他調整類型（例如 Levels）。 | 核對圖層類型或將調整轉換為 `BrightnessContrastLayer`。 |
| **儲存的檔案顯示損毀** | 未授權或使用過舊的 Aspose.PSD 版本。 | 套用有效授權並確保使用最新函式庫。 |
| **數值超出範圍** | 亮度/對比度必須介於 -100 到 100 之間。 | 在呼叫 `setBrightness` / `setContrast` 前先將數值限制在範圍內。 |

## 常見問答

**Q: 什麼是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一套讓開發人員以程式方式操作 PSD 檔案的函式庫，能自動化 Photoshop 相關工作。

**Q: 能否一次調整多個圖層的亮度與對比度？**  
A: 可以，本文示範的做法會遍歷 PSD 中的所有圖層，從而同時調整多個 `BrightnessContrastLayer`。

**Q: 如何取得 Aspose.PSD 的臨時授權？**  
A: 可前往 [temporary license page](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 有提供免費試用版嗎？**  
A: 有，您可從 [release page](https://releases.aspose.com/) 下載 Aspose.PSD 的免費試用版。

**Q: 哪裡可以取得 Aspose.PSD 的其他支援？**  
A: 可在其 [support forum](https://forum.aspose.com/c/psd/34) 取得技術支援。

---

**最後更新：** 2026-03-28  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}