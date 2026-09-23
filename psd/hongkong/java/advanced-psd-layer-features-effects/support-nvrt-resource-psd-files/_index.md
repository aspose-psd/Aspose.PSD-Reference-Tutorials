---
date: 2026-09-23
description: 了解如何使用 Aspose.PSD for Java 載入 PSD 檔案、讀取圖層，並從反轉調整圖層中提取 Nvrt 資源，以及批次處理
  PSD 檔案。
keywords:
- how to load psd
- batch process psd files
- invert adjustment layer java
- nvrt resource extraction
- Aspose.PSD
lastmod: 2026-09-23
linktitle: 使用 Java 支援 PSD 檔案中的 Nvrt 資源
og_description: 了解如何使用 Aspose.PSD for Java 載入 PSD 檔案、讀取圖層，並從反轉調整圖層中提取 Nvrt 資源。同時了解如何有效率地批次處理
  PSD 檔案。
og_image_alt: 'Developer guide: Load PSD and extract Nvrt resource using Aspose.PSD
  for Java'
og_title: 如何使用 Aspose.PSD 載入 PSD 並提取 Nvrt 資源
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to load PSD files, read layers, and extract the Nvrt resource
    from invert adjustment layers using Aspose.PSD for Java, plus batch process PSD
    files.
  headline: How to load PSD and extract Nvrt resource with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      convert, and render PSD files directly from Java code.
    question: What is Aspose.PSD for Java?
  - answer: Yes, a commercial license is required for production use. You can explore
      purchasing options [purchase Aspose.PSD](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD in commercial products?
  - answer: 'The complete documentation is available here: [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).'
    question: Where can I find the documentation for Aspose.PSD?
  - answer: Absolutely! You can get a free trial of Aspose.PSD for Java [download
      free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: 'You can ask questions and get support on the Aspose forum: [Aspose Support](https://forum.aspose.com/c/psd/34).'
    question: How can I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- load PSD
- Aspose.PSD
- Java image processing
- invert adjustment layer
- Nvrt resource
title: 如何使用 Aspose.PSD 載入 PSD 並提取 Nvrt 資源
url: /zh-hant/java/advanced-psd-layer-features-effects/support-nvrt-resource-psd-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Java 載入 PSD 並從反相調整圖層提取 Nvrt 資源

當您需要以程式方式 **how to load PSD** 檔案並使用 **invert adjustment layer** 時，Java 生態系統——尤其是 Aspose.PSD 函式庫——提供完整的控制。無論您是在構建圖形編輯器、 自動化設計流程，或是從 Photoshop 文件中提取資產，精通 PSD 處理對於現代影像處理工作流程都是必不可少的。

## 快速回答
- **什麼函式庫在 Java 中處理 PSD 檔案？** Aspose.PSD for Java  
- **我可以讀取 PSD 圖層嗎？** 是的，API 提供對圖層結構的完整存取  
- **生產環境需要授權嗎？** 是的，需要商業授權  
- **支援哪個 JDK 版本？** Java 8 及以上  
- **哪裡可以下載此函式庫？** 從官方 Aspose 下載頁面  

## 什麼是反相調整圖層？
反相調整圖層會反轉其下方每個像素的顏色值，產生相片負片效果。使用 Aspose.PSD，您可以在不光柵化圖像的情況下偵測、讀取並操作此圖層，這對於需要在大量檔案中保持一致色彩校正的批次處理管線而言是理想的。

## 為什麼要在 Aspose.PSD 中使用反相調整圖層？
Aspose.PSD 支援 **30+ 輸入與輸出格式**，且可在不將整個文件載入記憶體的情況下處理高達 **2 GB** 的檔案，讓您對顏色反轉擁有精確且記憶體效能高的控制。函式庫亦會公開調整資料，讓您能自動化移除或修改大量設計庫中的反相效果。

## 如何載入 Photoshop 檔案並批次處理 PSD 檔案
先載入一次 PSD，檢查其圖層，然後在迴圈內重複相同邏輯，以 **batch process PSD files** 的方式高效處理。為每個檔案實例化新的 `PsdImage`，並即時釋放，可降低記憶體使用並維持大量操作的高吞吐量。

## 前置條件
在開始編寫程式碼之前，請確保您具備以下條件：

- **Java Development Kit (JDK)** 已安裝（建議使用 Java 8 以上）  
- **An IDE** 如 IntelliJ IDEA、Eclipse 或 VS Code  
- **Aspose.PSD for Java** 函式庫 – 從官方網站下載：[Download Aspose.PSD for Java](https://releases.aspose.com/psd/java/)  
- **Basic Java knowledge**（類別、物件、例外處理）  

## 匯入套件
`PsdImage` 類別是 Aspose.PSD 的頂層物件，代表記憶體中的單一 Photoshop 文件，提供圖層與資源的操作介面。  

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.InvertAdjustmentLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.NvrtResource;
```

## 為什麼要讀取 PSD 圖層？
讀取 PSD 圖層可讓您了解文件的結構，從而分離個別資產、了解已套用的調整，並在其他專案或格式中重複使用元件。此可見性對於自動化、資產提取以及在多個檔案間維持設計一致性至關重要。

- 提取個別資產（例如圖示、遮罩）以供重用  
- 識別包含反相調整圖層的圖層，以了解圖像編輯內容  
- 自動化設計檔案的批次處理  

## 步驟 1：指定來源目錄
設定包含您要處理的 PSD 的資料夾。

```java
String sourceDir = "Your Source Directory";
String inPsdFilePath = sourceDir + "InvertAdjustmentLayer.psd";
```

將 `"Your Source Directory"` 替換為您機器上的實際路徑。

## 步驟 2：載入 PSD 檔案
`Image.load()` 會將檔案載入為 `PsdImage` 實例，解析 PSD 結構，以便您檢查圖層、資源與調整資料。

```java
PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);
```

此方法會開啟檔案並為檢查做準備。

## 步驟 3：初始化 Nvrt 資源變數
`NvrtResource` 類別代表儲存在 Photoshop 檔案內的反相調整資料。  

```java
NvrtResource nvrtResource = null;
```

## 步驟 4：搜尋反相調整圖層
`InvertAdjustmentLayer` 是套用負色效果的特定圖層類型。透過遍歷圖層集合，您可以定位此圖層，並取得其關聯的 `NvrtResource`。

```java
try {
    for (Layer layer : psdImage.getLayers()) {
        if (layer instanceof InvertAdjustmentLayer) {
            for (LayerResource layerResource : layer.getResources()) {
                if (layerResource instanceof NvrtResource) {
                    // The NvrtResource is found
                    nvrtResource = (NvrtResource)layerResource;
                    break;
                }
            }
        }
    }
} finally {
    psdImage.dispose();
}
```

`finally` 區塊保證 PSD 圖像會被釋放，保持記憶體使用的整潔。

## 步驟 5：驗證 Nvrt 資源
透過檢查前一步填入的變數，確認資源已成功定位。

```java
Assert.isNotNull(nvrtResource);
```

如果斷言通過，表示您已成功讀取 PSD 圖層並提取 Nvrt 資源。

## 常見陷阱與技巧
- **Null checks:** 在存取 `psdImage` 與圖層物件前，務必確認它們不為 null。  
- **Resource disposal:** 忘記呼叫 `psdImage.dispose()` 可能導致長時間執行的應用程式記憶體泄漏。  
- **File path issues:** 使用絕對路徑或確保工作目錄正確設定，以避免 `FileNotFoundException`。  
- **Batch processing note:** 在迭代大量檔案時，請在迴圈內重新實例化 `PsdImage`，並在處理完每個檔案後立即釋放。

## 結論
您現在已掌握 **how to load PSD** 檔案、讀取其圖層，並使用 Java 與 Aspose.PSD 提取 **invert adjustment layer** 的 Nvrt 資源。這個基礎讓您能構建強大的圖形自動化工具、 **batch process PSD** 檔案，或將 Photoshop 資料整合到更大的工作流程中。

## 常見問答

**Q: 什麼是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一套函式庫，讓開發人員能直接在 Java 程式碼中建立、編輯、轉換與渲染 PSD 檔案。

**Q: 我可以在商業產品中使用 Aspose.PSD 嗎？**  
A: 可以，生產環境必須取得商業授權。您可以在此探索購買選項 [purchase Aspose.PSD](https://purchase.aspose.com/buy)。

**Q: 哪裡可以找到 Aspose.PSD 的文件說明？**  
A: 完整文件說明可在此取得：[Aspose.PSD Documentation](https://reference.aspose.com/psd/java/)。

**Q: 有免費試用版嗎？**  
A: 當然！您可以取得 Aspose.PSD for Java 的免費試用版 [download free trial](https://releases.aspose.com/)。

**Q: 如何取得 Aspose.PSD 的支援？**  
A: 您可以在 Aspose 論壇上提問並取得支援：[Aspose Support](https://forum.aspose.com/c/psd/34)。

---

**最後更新：** 2026-09-23  
**測試環境：** Aspose.PSD for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose

## 相關教學

- [Java 圖像處理函式庫：使用 Aspose.PSD 反相圖層](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [使用 Aspose.PSD for Java 為 PSD 檔案新增等級調整圖層](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [使用 Aspose.PSD for Java 讀取 PSD 圖層 – 使用自訂原始資料載入器](/psd/java/advanced-psd-layer-features-effects/use-custom-raw-data-loader-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}