---
date: 2025-12-18
description: 學習如何使用 Aspose.PSD for Java 在 PSD 檔案中建立向量遮罩（Vmsk 資源）。本分步教學將示範如何新增向量遮罩、將
  PSD 轉換為 PNG，以及其他操作。
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: 使用 Java 在 PSD 檔案中建立向量遮罩（Vmsk 資源）
url: /zh-hant/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 PSD 檔案中使用 Java 建立向量遮罩 (Vmsk 資源)

## 簡介
如果您需要在 Photoshop (PSD) 檔案中 **建立向量遮罩** (Vmsk) 資源，Aspose.PSD for Java 為您提供一個乾淨、程式化的方式來完成。無論您是要構建設計自動化工具，或是為現有的圖形管線加入自訂遮罩支援，本教學都會一步一步帶領您——載入 PSD、讀取 Vmsk 資源、調整其屬性，並儲存結果。完成後，您將能熟練處理向量遮罩、將 PSD 轉換為 PNG，並以額外的向量資料擴充檔案。

## 快速答覆
- **Vmsk 資源是什麼？** 它是儲存在 PSD 檔案中的向量遮罩資料，用於定義圖層的複雜向量形狀。  
- **哪個函式庫支援它？** Aspose.PSD for Java 提供對 Vmsk 資源的完整讀寫存取。  
- **我需要授權嗎？** 有免費試用版；商業授權則在正式使用時必須取得。  
- **我可以將編輯過的 PSD 轉成 PNG 嗎？** 可以——儲存後，您可以再次載入 PSD，並使用相同的 API 匯出為 PNG。  
- **是否提供 Maven 支援？** 當然可以；Aspose.PSD 可作為 Maven 相依性加入（請參考 “aspose psd maven” 關鍵字）。

## 什麼是向量遮罩 (Vmsk 資源)？
向量遮罩 (Vmsk) 是一種非像素基礎的遮罩，使用貝茲曲線與路徑記錄來定義圖層上的透明與不透明區域。由於採用向量形式，它可以在不失真的情況下縮放——非常適合高解析度圖形。

## 為什麼要使用 Aspose.PSD 建立向量遮罩？
- **自動化：** 程式化地新增或修改遮罩，無需開啟 Photoshop。  
- **一致性：** 確保您產生的每個 PSD 都遵循相同的遮罩規則。  
- **跨平台：** 可在任何支援 Java 的作業系統上執行。  
- **整合性：** 可與其他 Aspose API（例如 PSD → PNG 轉換）結合，實現端到端工作流程。

## 先決條件
在深入程式碼之前，請確保您已具備以下條件：

### 您需要的項目
- Java Development Kit (JDK)：確保您的機器已安裝 JDK。若未安裝，可從 [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html) 下載。  
- Aspose.PSD for Java Library：這是一套功能強大的 PSD 檔案管理函式庫。您可從 [Aspose release page](https://releases.aspose.com/psd/java/) 下載。想先試用的使用者，也可從 [free trial](https://releases.aspose.com/) 取得免費試用版。  
- IDE：任何 Java IDE（如 IntelliJ IDEA、Eclipse 等）皆可用於本專案。

### 設定工作環境
1. **建立新 Java 專案** – 在您偏好的 IDE 中開啟並建立一個全新的專案。  
2. **加入 Aspose 函式庫** – 下載 Aspose JAR 後，將其加入專案的建置路徑，以便存取所有與 PSD 相關的類別。  

環境就緒後，讓我們進入實作階段。

## 如何使用 Java 在 PSD 檔案中建立向量遮罩
以下為逐步說明。程式碼區塊保持原樣，我們僅加入說明文字，使每一步都清晰易懂。

## 匯入套件
在處理 PSD 檔案之前，我們需要從 Aspose.PSD 函式庫匯入必要的類別。

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

現在環境已設定好，讓我們逐一說明每個操作。

## 步驟 1：載入您的 PSD 檔案
首先要做的事就是載入 PSD 檔案，這是所有操作的起點。

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- 我們將 `dataDir` 設為 PSD 檔案所在的目錄。  
- 我們建立 `sourceFileName` 字串，將目錄與 PSD 檔名結合。  
- 最後，我們使用 `Image.load()` 將 PSD 檔載入為 `PsdImage` 物件。

## 步驟 2：取得 Vmsk 資源
現在已載入 PSD 圖像，接著取得 Vmsk 資源。

```java
VmskResource resource = getVmskResource(im);
```

- 我們呼叫 `getVmskResource()` 方法，該方法負責在影像中搜尋並取得 Vmsk 資源。

## 步驟 3：驗證 Vmsk 資源屬性
在進行修改之前，必須先驗證 Vmsk 資源是否處於預期狀態。

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- 在此，我們檢查 Vmsk 資源的多項屬性，確保它未被停用、未反轉、已連結，且路徑數量正確。

## 步驟 4：存取每條路徑並驗證
讓我們更深入檢查 Vmsk 資源內的路徑。

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

- 我們擷取三筆特定的路徑記錄，並驗證其類型與屬性，以確保符合我們的條件。

## 步驟 5：編輯 Vmsk 資源
現在進入修改階段！您可以依需求調整 Vmsk 資源的屬性。

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- 在此區塊，我們切換 Vmsk 資源的多項屬性。將它們設為 `true` 後，即可控制遮罩在 PSD 檔中的行為。

## 步驟 6：修改貝茲節點座標
貝茲節點對向量路徑至關重要。讓我們在此修改一些數值。

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- 我們存取特定的 `BezierKnotRecord` 路徑，並變更其座標，以重新塑形向量遮罩。

## 步驟 7：儲存已修改的 PSD 檔案
完成所有編輯後，即可儲存已修改的 PSD 檔案。

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- 我們設定匯出 PSD 檔的路徑，然後呼叫 `im.save()` 將變更寫入新檔案。

## 步驟 8：清理資源
最後，我們必須確保正確釋放影像以釋放資源。

```java
im.dispose();
```

- 完成後釋放任何資源是最佳實踐，可避免應用程式發生記憶體洩漏。

## 結論
恭喜！您已完成使用 Aspose.PSD for Java 在 PSD 檔案中 **建立向量遮罩** (Vmsk) 資源的完整流程。從載入影像、取得並驗證 Vmsk 資源、編輯其屬性，到儲存已修改的 PSD，您現在具備自動化向量遮罩工作流程的堅實基礎。可運用這些技巧豐富設計管線、與其他 Aspose API（如 PSD 轉 PNG）整合，或打造自訂圖形工具。

## 常見問答
### 什麼是 Vmsk 資源？
Vmsk 資源是 PSD 檔案中的向量遮罩，允許建立複雜的向量形狀與編輯功能。

### 我可以在 Maven 專案中使用 Aspose.PSD 嗎？
可以，您可在 Maven 專案中加入 Aspose.PSD 相依性，使用其在儲存庫中的座標。

### 我可以將已修改的 PSD 檔案儲存為哪些格式？
您可以將它們儲存回 PSD 檔，或匯出為 PNG、JPEG 等其他格式。

### 是否提供 Aspose.PSD 的免費試用？
是的，您可取得 Aspose.PSD 的免費試用版以測試功能。請前往 [free trial link](https://releases.aspose.com/)。

### 我該如何取得 Aspose.PSD 的支援？
您可加入 [Aspose forum](https://forum.aspose.com/c/psd/34) 取得支援與除錯協助。

## 常見問題
**Q: 如何在現有圖層加入新的向量遮罩？**  
A: 建立 `VmskResource`，填入必要的路徑記錄（例如 `BezierKnotRecord`），再將其附加至圖層的資源集合中。

**Q: 我可以在不開啟 Photoshop 的情況下直接將編輯過的 PSD 轉成 PNG 嗎？**  
A: 可以——儲存 PSD 後，再以 `Image.load()` 載入，並呼叫 `im.save("output.png")` 指定 PNG 格式。

**Q: 有辦法在 CI/CD 流程中自動化此操作嗎？**  
A: 當然可以。由於全程使用純 Java，您可將其嵌入 Maven/Gradle 建置、Docker 容器或任何支援 Java 的 CI 系統中。

**Q: 哪些版本的 Aspose.PSD 相容於 Java 11 以上？**  
A: 所有近期發行版（2024‑2025）皆支援 Java 8 以上，包括 Java 11、17 以及更新的 LTS 版本。

**Q: 開發建置是否需要授權？**  
A: 免費評估授權可用於開發與測試。正式上線時則需商業授權。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose