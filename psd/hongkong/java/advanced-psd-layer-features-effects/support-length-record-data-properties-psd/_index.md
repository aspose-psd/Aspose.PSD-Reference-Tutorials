---
date: 2026-09-23
description: 了解如何使用 Aspose.PSD for Java 修改 PSD 向量形狀並批量處理 PSD 檔案。提供詳細步驟、技巧以及程式碼佔位符，打造完整解決方案。
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: 在 PSD 中支援 Length Record Data 屬性 - Java
og_description: 了解如何使用 Aspose.PSD for Java 修改 PSD 向量形狀並批量處理 PSD 檔案。提供逐步指南、程式碼佔位符與專家技巧。
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: 使用 Aspose.PSD for Java 修改 PSD 向量形狀
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: 使用 Aspose.PSD for Java 修改 PSD 向量形狀
url: /zh-hant/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 修改 PSD 向量形狀

## 簡介
如果您需要以程式方式**修改 PSD 向量形狀**，Aspose.PSD for Java 可讓您直接從 Java 程式碼完整控制 Photoshop 檔案。本教學將帶您了解支援 length record 屬性——這是在編輯向量形狀圖層時的關鍵步驟。完成後，您將能開啟 PSD、調整其向量形狀資料，並在不啟動 Photoshop 的情況下儲存更新的檔案。

## 快速回答
- **「modify PSD vector shapes」是什麼意思？** 調整 PSD 檔案中基於向量的圖層的幾何形狀、路徑操作或其他屬性。  
- **哪個函式庫處理此功能？** Aspose.PSD for Java。  
- **我需要授權嗎？** 免費試用可用於評估；正式使用則需商業授權。  
- **實作需要多長時間？** 基本的形狀修改腳本大約需要 10‑15 分鐘。  
- **主要前置條件是什麼？** Java JDK、Aspose.PSD for Java，以及一個範例 PSD 檔案。  

## 什麼是「支援 length record 屬性」？
支援 length record 屬性表示存取並更新描述 PSD 內每條向量路徑的 `LengthRecord` 物件。這些記錄儲存路徑的長度、類型以及與其他路徑的連接方式等資訊。修改它們即可控制形狀之間的合併、交叉或相減，從而實現精確的向量編輯。

## 為什麼使用 Aspose.PSD for Java 來支援 length record 屬性？
載入 PSD、編輯向量資料並儲存——全部不需 Photoshop。Aspose.PSD 在一般伺服器上可於 2 秒內處理上百頁的 PSD，提供超過 150 個類別（其中包含 30 多種向量相關類型），且可在 Windows、Linux 或 macOS 上執行，支援任何 JDK 11+。這個以效能為導向的函式庫免除昂貴桌面軟體的需求。

## 前置條件
1. **Java Development Kit (JDK)** – 從 [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載或使用您偏好的套件管理員。  
2. **Aspose.PSD for Java** – 從 [Aspose releases page](https://releases.aspose.com/psd/java/) 取得最新的 JAR。  
3. **IDE** – IntelliJ IDEA、Eclipse，或任何相容 Java 的編輯器。  
4. **PSD 檔案** – 在 Photoshop 中建立，或取得範例 PSD 以進行實驗。  
5. **基本的 Java 知識** – 熟悉類別、物件與例外處理。  

## 匯入套件
匯入語句將核心 Aspose.PSD 類別（例如 `PsdImage`、`VsmsResource` 與 `LengthRecord`）帶入作用域。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## 步驟 1：設定來源與輸出目錄
定義原始 PSD 所在位置以及修改後檔案的寫入位置。

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## 步驟 2：載入 PSD 檔案
使用 `Image.load` 開啟檔案，並將其轉型為 `PsdImage` 以使用 PSD 專屬功能。

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## 步驟 3：在圖層中定位 Vsms 資源
`VsmsResource` 是儲存圖層向量形狀資料的容器。遍歷第二層的資源以找到它。

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## 步驟 4：存取 length 記錄
`LengthRecord` 代表一條獨立的向量路徑。取得您打算修改的記錄。

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## 步驟 5：修改路徑操作屬性
`PathOperations` 定義個別形狀之間的互動方式（例如排除、交叉、相減）。變更這些值會更新向量圖層的視覺組成。

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## 步驟 6：儲存修改後的 PSD 檔案
將變更持久化至新檔案。

```java
psdImage.save(outPsdFilePath);
```

## 步驟 7：清理資源
釋放 `PsdImage` 實例以釋放記憶體，避免資源洩漏。

```java
psdImage.dispose();
```

## 如何使用支援 length record 屬性批次處理 PSD 檔案
將單一檔案的工作流程包裝在迴圈中，遍歷 PSD 目錄，為每個檔案更新 `inPsdFilePath` 與 `outPsdFilePath`。此方法可在數分鐘內對數十或數百個檔案套用相同的向量形狀調整，適合自動化資產管線。

## 常見陷阱與技巧
- **Null checks** – 在存取成員之前，務必確認 `resource` 不為 `null`。  
- **Path index bounds** – 確保您使用的索引（例如 `[2]`、`[7]`、`[11]`）在您編輯的特定 PSD 中存在。  
- **License** – 未使用有效授權執行時，儲存的 PSD 會嵌入浮水印。  

## 結論
您現在擁有一個完整的端對端範例，說明如何透過支援 length record 屬性，使用 Aspose.PSD for Java **修改 PSD 向量形狀**。無論是自動化資產管線或構建自訂設計工具，這些 API 都提供了在不使用 Photoshop 的情況下操作向量圖層的彈性。可嘗試其他 `PathOperations` 值，或結合多個 `LengthRecord` 編輯，以建立複雜形狀。

## 常見問題

**Q: 如何處理不含向量形狀圖層的 PSD？**  
A: `VsmsResource` 會不存在，導致 `resource` 為 `null`。加入檢查並跳過修改步驟或通知使用者。

**Q: 我可以變更其他屬性，例如填色或筆劃寬度嗎？**  
A: 可以，`LengthRecord` 提供填色、筆劃與不透明度的設定子。請參閱 API 文件取得完整列表。

**Q: 能否批次處理多個 PSD 檔案？**  
A: 完全可以。將程式碼包在迴圈中，遍歷 PSD 目錄，並在每次迭代時調整輸入與輸出路徑。

**Q: 從檔案路徑載入時需要手動關閉串流嗎？**  
A: `Image.load` 會自動處理檔案串流，但若從 `InputStream` 載入，請記得在使用後關閉它。

**Q: 這些 API 需要哪個版本的 Aspose.PSD？**  
A: `LengthRecord` 與 `PathOperations` 類別自 Aspose.PSD 20.10 起即已提供。建議使用最新版本（撰寫時為 24.11）。  

**最後更新：** 2026-09-23  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose

## 相關教學

- [將 PSD 轉換為 PNG 並建立向量遮罩 Java – PSD 檔案中的 Vmsk 資源](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [使用 Aspose.PSD for Java 轉換 PSD 為 PNG 並支援圖層遮罩](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [新增圖層支援 PSD 檔案](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}