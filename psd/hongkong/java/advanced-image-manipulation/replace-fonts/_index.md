---
date: 2026-06-23
description: 了解如何使用 Aspose.PSD for Java 將 PSD 儲存為 PNG、取代缺失字型，並匯出影像——快速處理缺失字型的 PSD
  檔案。
keywords:
- save psd as png
- how to replace fonts
- convert psd to bmp
- export psd to jpeg
- handle missing fonts psd
linktitle: 取代字型
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PSD as PNG, replace missing fonts, and export images
    using Aspose.PSD for Java – handle missing fonts PSD files quickly.
  headline: How to Save PSD as PNG and Replace Missing Fonts in Java with Aspose
  type: TechArticle
- questions:
  - answer: Yes. While the primary use‑case is PSD, Aspose.PSD also supports PNG,
      JPEG, BMP, and TIFF, allowing font replacement wherever text layers exist.
    question: Can I replace fonts in other image formats besides PSD?
  - answer: No. You can set any TrueType font you prefer, or omit the setting to let
      Aspose use its internal default.
    question: Is the default replacement font mandatory?
  - answer: A commercial license is required for production deployments. See the [purchase
      page](https://purchase.aspose.com/buy) for details.
    question: Are there licensing requirements for using Aspose.PSD?
  - answer: Absolutely. Aspose offers free temporary licenses for evaluation – visit
      the [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: Can I obtain a temporary license for testing?
  - answer: 'The community forum is a great place to ask questions: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).'
    question: Where can I find additional support or discuss Aspose.PSD‑related issues?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 如何在 Java 中使用 Aspose 將 PSD 儲存為 PNG 並取代缺失字型
url: /zh-hant/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 另存為 PNG – 在 Java 中取代缺失字型

## 介紹

如果您需要在 Photoshop (PSD) 檔案中替換缺失或不想要的字型，同時 **將 PSD 另存為 PNG**，Aspose PSD 字型取代功能可讓此過程變得輕鬆。於 Java 應用程式中，您可以載入 PSD，告訴 Aspose 使用哪一個備援字型，然後以任意格式匯出已修正的影像。本教學將帶您完整走過工作流程——從專案設定到匯出更新後的 PNG——讓您在不開啟 Photoshop 的情況下，可靠地 **處理缺失字型的 PSD** 情境。

## 快速解答
- **什麼函式庫負責字型取代？** Aspose.PSD for Java  
- **實作需要多長時間？** 基本情境約 5‑10 分鐘  
- **預設備援字型是哪一個？** 您可以設定任何 TrueType 字型，例如 “Arial”。  
- **我可以另存為 PNG 以外的格式嗎？** 可以——支援 PSD、JPEG、BMP 等多種格式  
- **生產環境需要授權嗎？** 非試用版需具備有效的 Aspose.PSD 授權  

## 什麼是 Aspose PSD 字型取代？

Aspose PSD 字型取代是指在 PSD 檔案中指定一種替代字型，當函式庫遇到缺失或不支援的字型時會使用該字型。此機制可確保文字圖層正確呈現，無需在 Photoshop 中手動編輯，並讓您自動 **處理缺失字型的 PSD** 檔案。

## 為什麼使用 Aspose.PSD for Java？

Aspose.PSD for Java 提供完整且高效能的解決方案，讓您直接在 Java 程式碼中處理 Photoshop 檔案，免除對 Photoshop 本身的需求。它支援多種圖層類型、效果與大型檔案，同時提供簡易的 API 來執行字型取代、影像轉換與中繼資料處理等工作。

- **完整的 PSD 處理功能** – Aspose.PSD 支援 **30 多種圖層類型**、**20 多種效果**，且可在不將整個文件載入記憶體的情況下處理高達 **2 GB** 的檔案。  
- **跨平台** – 可在任何支援 Java 8+ 的作業系統上執行。  
- **無外部相依性** – 函式庫內部處理字型取代，無需隨應用程式額外提供字型。  

## 如何使用 Aspose PSD 取代 PSD 中缺失的字型

要取代缺失的字型，您需要先在載入選項中設定備援字型並載入 PSD，之後再渲染或另存影像。函式庫會自動以您指定的字型取代缺失的字型，確保最終視覺輸出符合預期，無需手動編輯。

## 前置條件

- **Java Development Kit (JDK)** – 已安裝 8 版或以上。  
- **Aspose.PSD for Java** – 從[發佈頁面](https://releases.aspose.com/psd/java/)下載最新的 JAR。  
- **開發環境** – IntelliJ IDEA、Eclipse 或您慣用的任何編輯器。  

## 匯入套件

`PsdImage` 類別在記憶體中表示 Photoshop 文件，提供對圖層、文字與渲染功能的存取。`PsdLoadOptions` 控制檔案的讀取方式，包括備援字型，而 `SaveOptions`（或特定格式的子類別）則定義影像的寫入方式。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## 步驟 1：設定文件目錄

指定包含來源 PSD 檔案的資料夾。將佔位符替換為您機器上的實際路徑。

`File` 物件僅指向您要處理的 PSD，無需額外設定。  

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：以取代字型載入影像

建立 `PsdLoadOptions` 實例，設定預設的取代字型（例如 **Arial**），然後載入 PSD。Aspose 會在遇到缺失字型時自動套用備援字型。

`PsdLoadOptions` 讓您定義載入行為，包括在匯入階段取代任何缺失字型的備援字型。  

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## 步驟 3：將取代後的影像另存為 PNG

完成字型取代後，您可以以任何支援的格式匯出影像。此處將其另存為 PNG，您亦可選擇 JPEG、BMP，甚至寫回 PSD。

`PsdImage` 的 `save` 方法接受 `SaveOptions` 物件；使用 `PngOptions` 可確保輸出為適合網路或後續處理的無損 PNG。  

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## 如何在取代字型後將 PSD 另存為 PNG？

先以備援字型載入 PSD，然後呼叫 `psdImage.save("output.png", new PngOptions())`。此單行儲存操作會寫入完整渲染的 PNG，呈現已取代的字型，讓您在任何地方嵌入影像而不必擔心缺失字型。請確保在儲存前已套用取代字型，並可透過 `PngOptions` 物件調整 PNG 壓縮設定，以取得最佳檔案大小。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| 取代後文字顯示亂碼 | 備援字型不包含所需字形 | 選擇支援所需 Unicode 範圍的字型，例如 “Arial Unicode MS”。 |
| `OutOfMemoryError` 發生於大型 PSD | 在記憶體不足的情況下載入高解析度檔案 | 增加 JVM 堆積大小（`-Xmx2g`），或在支援時以串流模式載入影像。 |
| 授權例外 | 在生產環境使用試用版 | 在載入影像前套用有效的永久或暫時授權。 |

## 常見問答

**Q: 我可以在 PSD 以外的其他影像格式中取代字型嗎？**  
A: 可以。雖然主要使用情境是 PSD，Aspose.PSD 亦支援 PNG、JPEG、BMP 與 TIFF，讓您在任何含文字圖層的影像中執行字型取代。

**Q: 必須使用預設的取代字型嗎？**  
A: 不必。您可以設定任何喜好的 TrueType 字型，或省略設定，讓 Aspose 使用內建的預設字型。

**Q: 使用 Aspose.PSD 有授權需求嗎？**  
A: 生產環境需要商業授權。詳情請參閱[購買頁面](https://purchase.aspose.com/buy)。

**Q: 我可以取得暫時授權來測試嗎？**  
A: 當然可以。Aspose 提供免費的暫時授權供評估使用——請前往[暫時授權頁面](https://purchase.aspose.com/temporary-license/)。

**Q: 我可以在哪裡取得額外支援或討論 Aspose.PSD 相關問題？**  
A: 社群論壇是提問的好地方：[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)。

**Q: 如何處理包含多個缺失字型的 PSD 檔案？**  
A: 如前所示只需設定一次預設取代字型——在載入過程中會套用至 *所有* 缺失的字型。

**Q: 可以在影像儲存後再取代字型嗎？**  
A: 必須在載入階段完成字型取代。若要之後更改字型，需以不同的取代字型重新載入 PSD 並再次儲存。

## 結論

您現在已看到完整的 Java **將 PSD 另存為 PNG** 工作流程——從匯入正確的類別、設定備援字型、載入 PSD，到匯出已修正的 PNG。將此模式整合到您的影像處理流程中，可確保所有 PSD 資產的字體一致，並自動 **處理缺失字型的 PSD**。

---

**最後更新：** 2026-06-23  
**測試版本：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose

## 相關教學

- [在 Aspose.PSD for Java 中設定取代缺失字型](/psd/java/advanced-techniques/settings-replacing-missing-fonts/)
- [在 Aspose.PSD for Java 中將 PSD 另存為 PNG 並套用渲染陰影](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG 並等比例調整大小](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}