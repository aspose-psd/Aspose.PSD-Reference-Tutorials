---
date: 2025-12-05
description: 學習如何在 Java 中執行 Aspose PSD 字型取代。本步驟式 Java 圖像處理教學將向您展示如何高效地在 PSD 檔案中更換字型。
linktitle: Replace Fonts
second_title: Aspose.PSD Java API
title: Aspose PSD 字型替換（Java）– 替換 PSD 檔案中的字型
url: /zh-hant/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose PSD 字體替換（Java）

## 簡介

如果您需要在 Photoshop（PSD）檔案中替換遺失或不想要的字體，**Aspose PSD 字體替換** 讓這個過程變得輕鬆。在 Java 應用程式中，您可以載入 PSD，告訴 Aspose 使用哪一種備援字體，然後將結果儲存為任意格式。本教學將帶您完整了解 **aspose psd font replacement** 工作流程，從專案設定到匯出已更新的影像。

## 快速回答
- **哪個函式庫負責字體替換？** Aspose.PSD for Java  
- **實作需要多久？** 基本情境約 5‑10 分鐘  
- **預設的備援字體是什麼？** 您可以設定任何 TrueType 字體，例如 “Arial”  
- **可以儲存成 PNG 以外的格式嗎？** 可以 – 支援 PSD、JPEG、BMP 等多種格式  
- **正式環境需要授權嗎？** 非試用使用時必須擁有有效的 Aspose.PSD 授權  

## 什麼是 Aspose PSD 字體替換？

Aspose PSD 字體替換是指在程式庫遇到 PSD 檔案中缺失或不支援的字體時，使用您指定的替代字體來呈現文字層。這可確保文字層正確渲染，無需在 Photoshop 中手動編輯。

## 為什麼使用 Aspose.PSD for Java？

- **完整的 PSD 處理功能** – 透過 API 可存取圖層、遮色片、效果與文字。  
- **跨平台** – 可在任何支援 Java 的作業系統上執行。  
- **無外部相依** – 程式庫內部自行處理字體替換，無需隨應用程式額外攜帶字體檔案。  

## 先決條件

在開始之前，請確保您已具備：

- **Java Development Kit (JDK)** – 已安裝 8 版或以上。  
- **Aspose.PSD for Java** – 從 [release page](https://releases.aspose.com/psd/java/) 下載最新 JAR。  
- **IDE** – 如 IntelliJ IDEA、Eclipse 或您慣用的編輯器。  

## 匯入套件

先匯入所需的類別，以取得影像載入、載入選項與儲存功能。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：設定文件目錄

定義包含來源 PSD 檔案的資料夾路徑，將佔位符替換為您機器上的實際路徑。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：使用替代字體載入影像

建立 `PsdLoadOptions` 實例，指定預設的替代字體（例如 **Arial**），然後載入 PSD。Aspose 會在遇到缺失字體時自動套用此備援字體。

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## 步驟 3：儲存已替換的影像

完成字體替換後，您可以將影像匯出為任何支援的格式。此處示範儲存為 PNG，您也可以選擇 JPEG、BMP，甚至寫回 PSD。

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## 常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|------|------|----------|
| 替換後文字出現亂碼 | 替代字體不包含所需的字形 | 選擇支援所需 Unicode 範圍的字體（例如 “Arial Unicode MS”）。 |
| `OutOfMemoryError` 發生於大型 PSD | 在記憶體不足的情況下載入高解析度檔案 | 增加 JVM 堆積大小（`-Xmx2g`）或在可用時使用串流模式載入影像。 |
| 授權例外 | 在正式環境使用試用版 | 在載入影像前套用有效的永久或臨時授權。 |

## 常見問答

**Q: 我可以在 PSD 之外的其他影像格式中替換字體嗎？**  
A: 可以。雖然主要使用情境是 PSD，但 Aspose.PSD 亦支援 PNG、JPEG、BMP 與 TIFF，允許在存在文字圖層的情況下進行字體替換。

**Q: 預設的替代字體是必須的嗎？**  
A: 不必。您可以設定任何您偏好的 TrueType 字體，或不設定讓 Aspose 使用內部的預設字體。

**Q: 使用 Aspose.PSD 是否有授權需求？**  
A: 在正式環境部署需要商業授權。詳情請參閱 [購買頁面](https://purchase.aspose.com/buy)。

**Q: 我可以取得臨時授權來測試嗎？**  
A: 當然可以。Aspose 提供免費的臨時授權供評估使用——請前往 [臨時授權頁面](https://purchase.aspose.com/temporary-license/)。

**Q: 我可以在哪裡取得額外支援或討論 Aspose.PSD 相關問題？**  
A: 社群論壇是提問的好地方：[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)。

**Q: 如何處理包含多個缺失字體的 PSD 檔案？**  
A: 只需設定一次預設替代字體（如示範），它會在載入過程中套用至 *所有* 缺失的字體。

**Q: 儲存影像後還能替換字體嗎？**  
A: 字體替換必須在載入階段完成。若要之後更換字體，需要使用不同的替代字體重新載入 PSD 並再次儲存。

## 結論

您現在已完整了解 **aspose psd font replacement** 在 Java 中的工作流程——從匯入正確的類別、設定備援字體、載入 PSD，到匯出修正後的影像。將此模式整合到您的影像處理管線中，可確保所有 PSD 資產的字體一致性。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-12-05  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時最新）  
**作者：** Aspose  

---