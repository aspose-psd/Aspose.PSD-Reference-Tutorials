---
date: 2026-02-09
description: 學習如何在 Java 中使用 Aspose PSD 字型取代功能，處理缺少字型的 PSD 檔案，快速取代缺失字型，並匯出圖像。
linktitle: Replace Fonts
second_title: Aspose.PSD Java API
title: Aspose PSD 字型替換（Java）– 替換缺失字型
url: /zh-hant/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose PSD 字體替換於 Java

## 簡介

## 快速答案
- **什麼程式庫負責字體替換？** Aspose.PSD for Java  
- **實作需要多長時間？** 約 5‑10 分鐘的基本情境  
- **預設備用字體是哪一個？** 您可以設定任何 TrueType 字體，例如 “Arial”  
- **我可以儲存為 PNG 以外的格式嗎？** 可以 – 支援 PSD、JPEG、BMP 等格式  
- **生產環境需要授權嗎？** 非試用時需使用有效的 Aspose.PSD 授權  

## 什麼是 Aspose PSD 字體替換？

Aspose PSD 字體替換是指在程式庫遇到 PSD 檔案中缺少或不支援的字體時，指定替代字體的過程。這可確保文字圖層正確渲染，無需在 Photoshop 手動編輯，並讓您自動 **handle missing fonts PSD** 檔案。

## 為什麼使用 Aspose.PSD for Java？

- **完整的 PSD 處理功能** – 透過 API 可存取圖層、遮色片、效果與文字。  
- **跨平台** – 可在任何支援 Java 的作業系統上執行。  
- **無外部相依性** – 程式庫在內部處理字體替換，無需隨應用程式額外提供字體。  

## 如何使用 Aspose PSD 替換 PSD 中缺失的字體

以下是一步一步的指南，說明如何使用自訂備用字體 **how to replace missing fonts PSD** 檔案。

## 先決條件

- **Java Development Kit (JDK)** – 已安裝 8 版或以上。  
- **Aspose.PSD for Java** – 從 [release page](https://releases.aspose.com/psd/java/) 下載最新的 JAR。  
- **IDE** – IntelliJ IDEA、Eclipse，或您偏好的任何編輯器。  

## 匯入套件

首先匯入所需的類別，這樣即可使用影像載入、載入選項與儲存功能。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：設定文件目錄

定義包含來源 PSD 檔案的資料夾。將佔位符替換為您機器上的實際路徑。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：使用替代字體載入影像

建立 `PsdLoadOptions` 實例，指定預設的替代字體（例如 **Arial**），然後載入 PSD。Aspose 會在遇到缺少字體時自動套用備用字體。

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## 步驟 3：儲存已替換的影像

完成字體替換後，您可以將影像匯出為任何支援的格式。此處將其儲存為 PNG，您亦可選擇 JPEG、BMP，甚至寫回 PSD。

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| 替換後文字出現亂碼 | 備用字體不包含所需字形 | 選擇支援所需 Unicode 範圍的字體，例如 “Arial Unicode MS”。 |
| 大型 PSD 出現 `OutOfMemoryError` | 載入高解析度檔案時堆積記憶體不足 | 增加 JVM 堆積大小 (`-Xmx2g`) 或在可用時使用串流模式載入影像。 |
| 授權例外 | 在生產環境使用試用版 | 在載入影像前套用有效的永久或臨時授權。 |

## 常見問題

**Q: 我可以在 PSD 之外的其他影像格式中替換字體嗎？**  
A: 可以。雖然主要使用情境是 PSD，Aspose.PSD 亦支援 PNG、JPEG、BMP 與 TIFF，允許在存在文字圖層的情況下進行字體替換。

**Q: 必須使用預設的替代字體嗎？**  
A: 不需要。您可以設定任何喜好的 TrueType 字體，或不設定讓 Aspose 使用內部預設值。

**Q: 使用 Aspose.PSD 有授權需求嗎？**  
A: 生產部署需要商業授權。詳情請參閱 [purchase page](https://purchase.aspose.com/buy)。

**Q: 我可以取得測試用的臨時授權嗎？**  
A: 當然可以。Aspose 提供免費的臨時授權供評估使用 – 請前往 [temporary license page](https://purchase.aspose.com/temporary-license/)。

**Q: 我可以在哪裡取得更多支援或討論 Aspose.PSD 相關問題？**  
A: 社群論壇是提問的好地方：[Aspose.PSD forum](https://forum.aspose.com/c/psd/34)。

**Q: 如何處理包含多個缺失字體的 PSD 檔案？**  
A: 如示範，只需設定一次預設替代字體 – 載入時會套用至 *所有* 缺失的字體。

**Q: 圖像儲存後還能替換字體嗎？**  
A: 必須在載入階段完成字體替換。若要之後更改字體，需以不同的替代字體重新載入 PSD 並再次儲存。

## 結論

您現在已看到完整的 **aspose psd font substitution** 工作流程於 Java——從匯入正確的類別、設定備用字體、載入 PSD，到匯出已修正的影像。將此模式整合至您的影像處理流程，以確保所有 PSD 資產的排版一致，並自動 **handle missing fonts PSD**。

---

**最後更新：** 2026-02-09  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
