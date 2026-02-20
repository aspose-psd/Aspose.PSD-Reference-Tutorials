---
date: 2026-02-20
description: 學習如何使用 Aspose.PSD for Java 支援長度記錄屬性並批次處理 PSD 檔案。逐步指南，附程式碼範例。
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: 支援長度記錄屬性 – 修改 PSD 向量形狀（Java）
url: /zh-hant/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 支援長度記錄屬性 – 修改 PSD 向量形狀 (Java)

## 介紹
如果您需要以程式方式 **修改 PSD 向量形狀**，Aspose.PSD for Java 函式庫讓您能直接在 Java 程式碼中完整控制 Photoshop 檔案。本教學將逐步說明 **支援長度記錄屬性** 的所有要點——這是編輯向量形狀圖層時不可或缺的步驟。完成後，您將能開啟 PSD、調整向量形狀屬性，並在不離開 IDE 的情況下儲存更新後的檔案。讓我們立即開始吧！

## 快速解答
- **「修改 PSD 向量形狀」是什麼意思？** 調整 PSD 檔案內以向量為基礎的圖層之幾何形狀、路徑操作或其他屬性。  
- **使用哪個函式庫？** Aspose.PSD for Java。  
- **需要授權嗎？** 可使用免費試用版進行評估；正式上線需購買商業授權。  
- **實作需要多久？** 基本的形狀修改腳本約 10‑15 分鐘即可完成。  
- **主要前置條件是什麼？** Java JDK、Aspose.PSD for Java 以及範例 PSD 檔案。

## 什麼是「支援長度記錄屬性」？
支援長度記錄屬性即是存取並更新描述 PSD 內每條向量路徑的 `LengthRecord` 物件。變更這些記錄即可控制形狀之間的合併、交叉或相減方式。

## 為什麼使用 Aspose.PSD for Java 來支援長度記錄屬性？
- **不需 Photoshop** – 直接在任何伺服器上操作 PSD 檔案。  
- **功能豐富的 API** – 以強型別類別存取圖層、資源與向量資料。  
- **跨平台** – 可在 Windows、Linux 或 macOS 上執行任意 JDK。  
- **效能導向** – 記憶體管理高效，儲存速度快。

## 前置條件
1. **Java Development Kit (JDK)** – 從 [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載或使用您慣用的套件管理工具。  
2. **Aspose.PSD for Java** – 從 [Aspose releases page](https://releases.aspose.com/psd/java/) 取得最新 JAR。  
3. **IDE** – IntelliJ IDEA、Eclipse 或任何支援 Java 的編輯器。  
4. **PSD 檔案** – 可在 Photoshop 中自行建立，或取得範例 PSD 進行測試。  
5. **基本的 Java 知識** – 熟悉類別、物件與例外處理。

## 匯入套件
首先，匯入處理 PSD 檔案與向量形狀資源所需的類別。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## 步驟 1：設定來源與輸出目錄
定義原始 PSD 所在位置以及修改後檔案的儲存路徑。

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## 步驟 2：載入 PSD 檔案
使用 `Image.load` 開啟檔案，並將其轉型為 `PsdImage` 以取得 PSD 專屬功能。

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## 步驟 3：在圖層中定位 Vsms 資源
向量形狀資料位於 `VsmsResource` 內。遍歷第二層的資源以找出它。

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## 步驟 4：存取 Length Records
每個 `LengthRecord` 代表一條獨立的向量路徑。取得您想要修改的記錄。

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## 步驟 5：修改路徑操作屬性
現在您可以透過變更 `PathOperations` 來 **修改 PSD 向量形狀**。此屬性決定形狀之間的互動方式（例如排除、交叉、相減）。

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## 步驟 6：儲存修改後的 PSD 檔案
將變更寫入新檔案。

```java
psdImage.save(outPsdFilePath);
```

## 步驟 7：清理資源
釋放 `PsdImage` 以回收記憶體。

```java
psdImage.dispose();
```

## 如何以支援長度記錄屬性的方式批次處理 PSD 檔案
若需對多個 PSD 套用相同的向量形狀調整，將上述程式碼包在迴圈中，對目錄內的檔案逐一執行。於每次迭代中更新 `inPsdFilePath` 與 `outPsdFilePath`，即可 **有效率地批次處理 PSD 檔案**。

## 常見陷阱與技巧
- **空值檢查** – 在存取路徑前務必確認 `resource` 不為 `null`。  
- **路徑索引範圍** – 確認您使用的索引（如 `[2]`、`[7]`、`[11]`）在目標 PSD 中確實存在。  
- **授權** – 未使用有效授權時，儲存的 PSD 會被加上浮水印。

## 結論
現在您已掌握完整的端對端範例，透過 Aspose.PSD for Java **支援長度記錄屬性** 來 **修改 PSD 向量形狀**。無論是自動化資產管線或打造自訂設計工具，這些 API 都能讓您在不使用 Photoshop 的情況下靈活操作向量圖層。可進一步嘗試其他 `PathOperations`，或結合多筆 `LengthRecord` 編輯以產生更複雜的形狀。

## 常見問答

**Q: 若 PSD 中沒有向量形狀圖層，該怎麼處理？**  
A: `VsmsResource` 會不存在，`resource` 會保持 `null`。請加入檢查並跳過修改步驟，或提示使用者。

**Q: 能否變更其他屬性，例如填色或筆畫寬度？**  
A: 可以，`LengthRecord` 提供填色、筆畫與不透明度等額外的 setter。請參考 API 文件取得完整說明。

**Q: 能否批次處理多個 PSD 檔案？**  
A: 完全可以。將程式碼包在遍歷 PSD 目錄的迴圈中，並在每次迭代時調整輸入與輸出路徑。

**Q: 從檔案路徑載入時需要手動關閉串流嗎？**  
A: `Image.load` 會自行處理檔案串流；若是從 `InputStream` 載入，則需在使用完畢後自行關閉。

**Q: 需要哪個版本的 Aspose.PSD 才能使用這些 API？**  
A: `LengthRecord` 與 `PathOperations` 自 Aspose.PSD 20.10 起即已提供，建議使用最新版本以取得最佳支援。

---

**最後更新時間：** 2026-02-20  
**測試環境：** Aspose.PSD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}