---
date: 2026-02-22
description: 學習如何使用 Aspose.PSD for Java 建立向量遮罩、加入向量遮罩 PSD，並以程式方式操作 Vmsk 資源。
linktitle: Create Vector Mask Java – Vmsk Resource in PSD Files
second_title: Aspose.PSD Java API
title: 在 Java 中建立向量遮罩 – PSD 檔案中的 Vmsk 資源
url: /zh-hant/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 PSD 檔案中建立向量遮罩（Java） – Vmsk 資源

## 簡介
如果您需要在 Photoshop (PSD) 檔案中 **create vector mask** (Vmsk) 資源，Aspose.PSD for Java 為您提供乾淨且程式化的解決方案。無論您是要構建設計自動化工具，或是為現有圖形管線加入自訂遮罩支援，本教學都會一步步帶您完成——載入 PSD、讀取 Vmsk 資源、調整其屬性，最後儲存結果。完成後，您將能熟練操作向量遮罩、將 PSD 轉換為 PNG，並以 **create vector mask java** 技術為檔案加入額外的向量資料。

## 快速答覆
- **什麼是 Vmsk 資源？** 它是儲存在 PSD 檔案中的向量遮罩資料，用於定義圖層的複雜向量形狀。  
- **哪個函式庫支援它？** Aspose.PSD for Java 提供對 Vmsk 資源的完整讀寫存取。  
- **我需要授權嗎？** 提供免費試用版；正式上線需購買商業授權。  
- **我可以將編輯過的 PSD 轉成 PNG 嗎？** 可以——儲存後，您可以再次載入 PSD，使用相同的 API 匯出為 PNG。  
- **是否提供 Maven 支援？** 當然可以；可將 Aspose.PSD 加入 Maven 相依性（參考 “aspose psd maven” 關鍵字）。

## 什麼是向量遮罩（Vmsk 資源）？
向量遮罩 (Vmsk) 是一種非像素式的遮罩，使用貝茲曲線與路徑記錄來定義圖層的透明與不透明區域。由於採用向量方式，它可以在不失真的情況下任意縮放，非常適合高解析度圖形。

## 為何使用 Aspose.PSD 建立向量遮罩？
- **自動化：** 程式化地新增或修改遮罩，無需開啟 Photoshop。  
- **一致性：** 確保每個產生的 PSD 都遵循相同的遮罩規則。  
- **跨平台：** 可在任何支援 Java 的作業系統上執行。  
- **整合性：** 可與其他 Aspose API（例如 PSD → PNG 轉換）結合，實現端到端工作流程。  
- **可擴充性：** 向量遮罩在任何尺寸下都保持清晰，適合響應式設計。

## 此議題對 Java 開發者的重要性
使用 **create vector mask java** 技術，您可以將複雜的圖形邏輯直接嵌入後端服務、CI 流程或桌面工具中。無需設計師手動加入遮罩，程式即可即時產生或調整，節省時間並降低人為錯誤。

## 先決條件
在深入程式碼之前，請確保您已具備以下條件：

### 所需環境
- Java Development Kit (JDK)：確保您的機器已安裝 JDK。若未安裝，可從 [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html) 下載。  
- Aspose.PSD for Java Library：這是一套強大的 PSD 檔案管理函式庫。可從 [Aspose release page](https://releases.aspose.com/psd/java/) 下載。想先試用的使用者，也可從 [free trial](https://releases.aspose.com/) 取得免費試用版。  
- IDE：任何支援 Java 的開發環境（如 IntelliJ IDEA、Eclipse 等）皆可用於本專案。

### 設定工作環境
1. **Create a New Java Project** – 在您偏好的 IDE 中開啟並建立一個新專案。  
2. **Add the Aspose Library** – 下載 Aspose JAR 後，將其加入專案的建置路徑，以便存取所有 PSD 相關類別。

環境就緒後，讓我們進入實作階段。

## 如何使用 Java 在 PSD 檔案中建立向量遮罩
以下為逐步說明。程式碼區塊保持原樣，我們僅加入說明文字，使每一步都清晰易懂。

### 匯入套件
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

現在環境已設定完畢，讓我們逐一說明各項操作。

### 步驟 1：載入 PSD 檔案
首先要做的事就是載入 PSD 檔案，這是所有操作的起點。

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- 我們將 `dataDir` 設為 PSD 檔案所在的目錄。  
- 我們建立 `sourceFileName` 字串，將目錄與 PSD 檔名結合。  
- 最後，我們使用 `Image.load()` 將 PSD 檔載入為 `PsdImage` 物件。

### 步驟 2：取得 Vmsk 資源
現在已載入 PSD 圖像，接著取得 Vmsk 資源。

```java
VmskResource resource = getVmskResource(im);
```

- 我們呼叫 `getVmskResource()` 方法，該方法會在影像中搜尋並取得 Vmsk 資源。

### 步驟 3：驗證 Vmsk 資源屬性
在進行修改之前，必須先驗證 Vmsk 資源是否處於預期狀態。

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- 這裡我們檢查 Vmsk 資源的多項屬性，確保它未被停用、未反相、已連結，且路徑數量正確。

### 步驟 4：存取每條路徑並驗證
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

- 我們取出三筆特定的路徑記錄，並驗證其類型與屬性，以符合我們的條件。

### 步驟 5：編輯 Vmsk 資源
現在進入修改階段！您可以依需求調整 Vmsk 資源的屬性。

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- 在此區塊中，我們切換 Vmsk 資源的多項屬性。將它們設為 `true` 後，即可控制遮罩在 PSD 中的行為。

### 步驟 6：修改貝茲結點座標
貝茲結點是向量路徑的關鍵，讓我們在此修改部分座標。

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- 我們存取特定的 `BezierKnotRecord` 路徑，變更其座標，以重新塑形向量遮罩。

### 步驟 7：儲存已修改的 PSD 檔案
完成所有編輯後，即可儲存已修改的 PSD 檔案。

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- 我們設定匯出 PSD 檔的路徑，然後呼叫 `im.save()` 將變更寫入新檔案。

### 步驟 8：清理資源
最後，我們必須正確釋放影像以釋放資源。

```java
im.dispose();
```

- 完成後釋放任何資源是良好慣例，可避免應用程式記憶體泄漏。

## 常見問題與解決方案
| 問題 | 發生原因 | 解決方法 |
|------|----------|----------|
| **`VmskResource` not found** | PSD 檔未包含向量遮罩圖層。 | 確認來源 PSD 已有向量遮罩，或在 Photoshop 中手動加入後再執行程式碼。 |
| **`ArrayIndexOutOfBoundsException` on path access** | 預期的路徑記錄數量不符。 | 檢查 `resource.getPaths().length`，並相應調整索引使用方式。 |
| **License exception** | 未使用有效的 Aspose.PSD 授權執行。 | 使用 `License license = new License(); license.setLicense("Aspose.PSD.lic");` 申請試用或正式授權。 |
| **Memory leak** | 長時間執行的程序未釋放影像。 | 確保在 `finally` 區塊中呼叫 `im.dispose()`，或在支援的情況下使用 try‑with‑resources。 |

## 常見問答

**Q: 如何為現有圖層新增向量遮罩？**  
A: 建立 `VmskResource`，填入所需的路徑記錄（例如 `BezierKnotRecord`），再將其附加至圖層的 resources 集合中。

**Q: 我能直接將編輯過的 PSD 轉成 PNG 而不開啟 Photoshop 嗎？**  
A: 可以——儲存 PSD 後，再以 `Image.load()` 載入，呼叫 `im.save("output.png")` 並指定 PNG 格式。

**Q: 有辦法在 CI/CD 流程中自動化此操作嗎？**  
A: 當然可以。由於全程使用 Java，您可將其嵌入 Maven/Gradle 建置、Docker 容器或任何支援 Java 的 CI 系統中。

**Q: 哪些版本的 Aspose.PSD 相容於 Java 11 以上？**  
A: 所有近期版本（2024‑2025）皆支援 Java 8 以上，包括 Java 11、17 以及更新的 LTS 版本。

**Q: 開發建置是否需要授權？**  
A: 免費評估授權可用於開發與測試。正式上線部署則需商業授權。

---

**最後更新：** 2026-02-22  
**測試環境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}