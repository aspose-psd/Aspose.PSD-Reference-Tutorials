---
date: 2026-06-03
description: 了解如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG、建立 Java 向量遮罩、加入向量遮罩 PSD，並以程式方式操作
  Vmsk 資源。
keywords:
- convert psd to png
- add vector mask psd
- psd vector mask tutorial
- aspose psd maven
linktitle: 將 PSD 轉換為 PNG 並使用 Java 建立向量遮罩 – PSD 檔案中的 Vmsk 資源
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to convert PSD to PNG and create vector mask Java using Aspose.PSD
    for Java, add vector mask PSD, and manipulate Vmsk resources programmatically.
  headline: Convert PSD to PNG and Create Vector Mask Java – Vmsk Resource in PSD
    Files
  type: TechArticle
- questions:
  - answer: Create a `VmskResource`, populate it with the required path records (e.g.,
      `BezierKnotRecord`), and attach it to the layer’s resources collection.
    question: How do I add a new vector mask to an existing layer?
  - answer: Yes—after saving the PSD, load it again with `Image.load()` and call `im.save("output.png")`
      specifying the PNG format.
    question: Can I convert the edited PSD directly to PNG without opening Photoshop?
  - answer: Absolutely. Since the process is pure Java, you can embed it in Maven/Gradle
      builds, Docker containers, or any CI system that supports Java.
    question: Is there a way to automate this in a CI/CD pipeline?
  - answer: All recent releases (2024‑2025) support Java 8 and above, including Java
      11, 17, and newer LTS versions.
    question: What versions of Aspose.PSD are compatible with Java 11+?
  - answer: A free evaluation license works for development and testing. For production
      deployments, a commercial license is required.
    question: Do I need a license for development builds?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 將 PSD 轉換為 PNG 並使用 Java 建立向量遮罩 – PSD 檔案中的 Vmsk 資源
url: /zh-hant/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 PSD 轉換為 PNG 並在 Java 中建立向量遮罩 – PSD 檔案中的 Vmsk 資源

## 簡介
如果您需要在 Photoshop 檔案中同時 **convert PSD to PNG** 並 **create vector mask** (Vmsk) 資源，Aspose.PSD for Java 為您提供乾淨且程式化的解決方案。無論您是構建設計自動化工具、驗證資產的 CI 流程，或是以自訂遮罩擴充圖形工作流程，本教學都會一步步帶領您——載入 PSD、讀取 Vmsk 資源、調整其屬性、匯出為 PNG，並儲存修改後的檔案。完成後，您將能熟練處理向量遮罩、執行 PSD → PNG 轉換，並以 **convert PSD to PNG** 技術為檔案加入額外的向量資料。

## 快速解答
- **What is a Vmsk resource?** 它是儲存在 PSD 檔案內的向量遮罩資料，用於定義圖層的複雜向量形狀。  
- **Which library supports it?** Aspose.PSD for Java 提供對 Vmsk 資源的完整讀寫存取。  
- **Do I need a license?** 提供免費試用版；商業環境需要購買授權。  
- **Can I convert the edited PSD to PNG?** 可以——儲存後，您可以載入 PSD 並使用相同的 API 匯出為 PNG。  
- **Is Maven support available?** 當然可以；可將 Aspose.PSD 作為 Maven 依賴加入（請參考 “aspose psd maven” 關鍵字）。

## 什麼是向量遮罩（Vmsk 資源）？
向量遮罩（Vmsk）是一種非像素的遮罩，使用貝茲曲線與路徑記錄來定義圖層上的透明與不透明區域。由於採用向量方式，它可在不失真情況下任意縮放，非常適合高解析度圖形。它可以包含多條路徑，每條路徑由貝茲節點組成，並支援遮罩屬性，如不透明度、填充以及與圖層遮罩的連結。

## 為何使用 Aspose.PSD 建立向量遮罩？
以程式方式建立向量遮罩可免除手動 Photoshop 編輯的需求，確保大量檔案的一致性，並能整合至自動化建置或部署流程。使用 Aspose.PSD，您可以產生精確的遮罩幾何形狀、套用至任意圖層，且保留完整的可編輯性，這對於動態圖形產生與響應式設計工作流程至關重要。
- **Automation:** 程式化地新增或修改遮罩，無需開啟 Photoshop。  
- **Consistency:** 確保每個產生的 PSD 都遵循相同的遮罩規則。  
- **Cross‑platform:** 可在任何支援 Java 的作業系統上執行。  
- **Integration:** 可與其他 Aspose API（例如 convert PSD → PNG）結合，實現端到端工作流程。  
- **Scalability:** 向量遮罩在任何尺寸下皆保持清晰，適合響應式設計。

## 為何這對 Java 開發者很重要
使用 **create vector mask java** 技術，可將複雜的圖形邏輯直接嵌入後端服務、CI 流程或桌面工具中。您不再需要設計師手動加入遮罩；程式碼即可即時產生或調整遮罩，節省時間並降低人為錯誤。

## 先決條件
在深入程式碼之前，請確保您已具備以下條件：

### 所需項目
- **Java Development Kit (JDK)：** 安裝 JDK 8 或更新版本。可從 [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html) 下載。  
- **Aspose.PSD for Java Library：** 這個功能強大的函式庫負責管理 PSD 檔案。可從 [Aspose release page](https://releases.aspose.com/psd/java/) 下載。若要快速開始，可在同一頁面取得免費試用版或前往 [free trial](https://releases.aspose.com/)。  
- **IDE：** 任意 Java IDE（IntelliJ IDEA、Eclipse、NetBeans）皆可使用。

### 設定工作區
1. **Create a New Java Project** – 在您偏好的 IDE 中開啟並建立一個新專案。  
2. **Add the Aspose Library** – 下載 Aspose JAR 後，將其加入專案的建置路徑，以便存取所有 PSD 相關類別。

環境就緒後，讓我們逐步說明實作內容。

## 如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG？
使用 `PsdImage.load()` 載入來源 PSD，必要時編輯其向量遮罩，然後呼叫 `save()` 並指定 `ExportFormat.Png`。Aspose.PSD 會自動處理所有色彩配置、圖層與遮罩資料，產生與原始視覺外觀相同的像素完美 PNG。此兩步流程適用於任何 PSD，無論大小，且可在任何支援 Java 的平台上執行。

## 匯入套件
`com.aspose.psd` 套件提供處理 PSD 檔案的核心類別，包括影像載入、資源操作與匯出功能。

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

現在我們已完成前置作業，接下來逐步說明每個操作。

## 步驟 1：載入 PSD 檔案
載入檔案會取得一個 `PsdImage` 物件，該物件在記憶體中代表整個文件。

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- 我們將 `dataDir` 設為 PSD 檔案所在的目錄。  
- 我們建立 `sourceFileName` 字串，將目錄與 PSD 檔名結合。  
- 最後，使用 `Image.load()` 載入 PSD 檔案，取得 `PsdImage` 物件。

## 步驟 2：取得 Vmsk 資源
`VmskResource` 類別封裝了儲存在 PSD 圖層內的向量遮罩資料。取得它即可檢視或修改遮罩路徑。

```java
VmskResource resource = getVmskResource(im);
```

- 我們呼叫 `getVmskResource()` 方法，該方法負責在影像中搜尋並取得 Vmsk 資源。

## 步驟 3：驗證 Vmsk 資源屬性
在進行變更之前，請驗證遮罩已啟用、方向正確，且包含預期的路徑數量。

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- 這裡我們檢查 Vmsk 資源的各項屬性，確保它未被停用、未反轉、已正確連結，且路徑數量正確。

## 步驟 4：存取每條路徑並驗證
每個路徑記錄描述向量形狀的一部分。檢查它們可確保您使用正確的幾何資訊。

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- 我們抽取三筆特定的路徑記錄，並驗證其類型與屬性，以確保符合我們的條件。

## 步驟 5：編輯 Vmsk 資源
現在進入修改階段！您可以切換遮罩的行為旗標，以符合工作流程。

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- 在此程式碼區塊中，我們切換 Vmsk 資源的多項屬性。將它們設為 `true` 後，即可控制遮罩在 PSD 檔案中的行為。

## 步驟 6：修改 Bézier 節點座標
Bézier 節點定義每個向量段的曲率。調整它們可在不光柵化的情況下重新塑形遮罩。

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- 我們存取特定的 `BezierKnotRecord` 路徑，並變更其座標，以重新塑形向量遮罩。

## 步驟 7：儲存已修改的 PSD 檔案
完成所有編輯後，將變更寫入新的 PSD 檔案。

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- 我們設定匯出 PSD 檔案的路徑，然後呼叫 `im.save()` 將變更寫入此新檔案。

## 步驟 8：將 PSD 匯出為 PNG
現在 PSD 已包含更新的遮罩，直接匯出為 PNG。此步驟示範 **convert PSD to PNG** 工作流程。

```java
im.dispose();
```

- 使用 `im.save("output.png", ExportFormat.Png)` 產生高品質的 PNG，呈現已編輯的向量遮罩。

## 清理資源
最後，我們需要確保正確釋放影像以釋放資源。

CODE_BLOCK_PLACEHOLDER_9_END

- 完成後釋放任何資源是一個良好慣例，可避免應用程式發生記憶體泄漏。

## 常見問題與解決方案
| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **`VmskResource` not found** | PSD 檔案未包含向量遮罩圖層。 | 確認來源 PSD 具有向量遮罩，或在執行程式碼前於 Photoshop 手動加入。 |
| **`ArrayIndexOutOfBoundsException` on path access** | 預期的路徑記錄數量不符。 | 檢查 `resource.getPaths().length`，並相應調整索引的使用方式。 |
| **License exception** | 未使用有效的 Aspose.PSD 授權執行。 | 使用 `License license = new License(); license.setLicense("Aspose.PSD.lic");` 申請試用或購買授權。 |
| **Memory leak** | 長時間執行的程序未釋放影像。 | 始終在 `finally` 區塊中呼叫 `im.dispose()`，或在支援的情況下使用 try‑with‑resources。 |

## 常見問答

**Q: 如何為現有圖層新增向量遮罩？**  
A: 建立 `VmskResource`，填入所需的路徑記錄（例如 `BezierKnotRecord`），並將其附加至圖層的資源集合。

**Q: 我可以在不開啟 Photoshop 的情況下直接將編輯過的 PSD 轉換為 PNG 嗎？**  
A: 可以——儲存 PSD 後，使用 `Image.load()` 再次載入，並呼叫 `im.save("output.png")` 指定 PNG 格式。

**Q: 是否有辦法在 CI/CD 流程中自動化此操作？**  
A: 當然可以。由於整個流程純粹使用 Java，您可以將其嵌入 Maven/Gradle 建置、Docker 容器或任何支援 Java 的 CI 系統中。

**Q: 哪些版本的 Aspose.PSD 與 Java 11 以上相容？**  
A: 所有近期版本（2024‑2025）皆支援 Java 8 以上，包括 Java 11、17 以及更新的 LTS 版本。

**Q: 開發建置是否需要授權？**  
A: 免費評估授權可用於開發與測試。正式上線時則需購買商業授權。

---
**最後更新：** 2026-06-03  
**測試環境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose

## 相關教學

- [在 Java 中匯出支援圖層遮罩的 PSD 為 PNG](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [如何使用 Aspose.PSD for Java 將 PSD 轉換為 PNG 並等比例調整大小](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [使用顏色覆蓋將 PSD 轉換為 PNG – Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}