---
date: 2025-12-17
description: 學習如何使用 Aspose.PSD for Java，透過支援長度記錄資料屬性來修改 PSD 向量形狀。提供逐步說明與程式碼範例。
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: 如何修改 PSD 向量形狀 – 在 Java 中支援長度記錄資料屬性
url: /zh-hant/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 支援 PSD 中的長度記錄資料屬性 - Java

## 簡介
如果您需要以程式方式 **修改 PSD 向量形狀**，Aspose.PSD for Java 函式庫讓您能直接在 Java 程式碼中完整控制 Photoshop 檔案。在本教學中，我們將逐步說明如何支援長度記錄資料屬性——這是編輯向量形狀圖層的關鍵步驟。完成後，您將能開啟 PSD、調整其向量形狀屬性，並在不離開 IDE 的情況下儲存更新後的檔案。讓我們立即開始吧！

## 快速回答
- **「修改 PSD 向量形狀」是什麼意思？** 調整 PSD 檔案內向量圖層的幾何形狀、路徑操作或其他屬性。  
- **哪個函式庫負責這項工作？** Aspose.PSD for Java。  
- **需要授權嗎？** 評估可使用免費試用版；正式上線需購買商業授權。  
- **實作大約需要多久？** 基本的形狀修改腳本約 10‑15 分鐘即可完成。  
- **主要前置條件是什麼？** Java JDK、Aspose.PSD for Java 以及一個範例 PSD 檔案。

## 什麼是「修改 PSD 向量形狀」？
修改 PSD 向量形狀是指變更底層的向量路徑資料——例如長度記錄與路徑操作——使形狀的視覺外觀隨之更新。此功能在自動化圖形流水線、批次處理或自訂設計工具中特別有用。

## 為什麼使用 Aspose.PSD for Java 來修改 PSD 向量形狀？
- **不需 Photoshop** – 直接在任何伺服器上操作 PSD 檔案。  
- **功能豐富的 API** – 透過強型別類別存取圖層、資源與向量資料。  
- **跨平台** – 可在 Windows、Linux 或 macOS 上執行，支援任何 JDK。  
- **效能導向** – 記憶體管理高效，儲存速度快。

## 先決條件
1. **Java Development Kit (JDK)** – 從 [Oracle 的網站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載或使用您慣用的套件管理工具。  
2. **Aspose.PSD for Java** – 從 [Aspose 釋出頁面](https://releases.aspose.com/psd/java/) 取得最新 JAR。  
3. **IDE** – IntelliJ IDEA、Eclipse 或任何支援 Java 的編輯器。  
4. **PSD 檔案** – 可在 Photoshop 中建立，或取得範例 PSD 進行測試。  
5. **基本的 Java 知識** – 熟悉類別、物件與例外處理。

## 匯入套件
首先匯入處理 PSD 檔案與向量形狀資源所需的類別。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## 步驟 1：設定來源與輸出目錄
定義原始 PSD 所在位置以及要將修改後檔案儲存至何處。

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
向量形狀資料位於 `VsmsResource` 內。遍歷第二個圖層的資源以找出它。

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## 步驟 4：存取長度記錄
每個 `LengthRecord` 代表一條獨立的向量路徑。取得您打算修改的那些記錄。

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## 步驟 5：修改路徑操作屬性
現在您可以透過變更 `PathOperations` 來 **修改 PSD 向量形狀**。此設定決定形狀之間的互動方式（例如排除、交集、減除）。

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## 步驟 6：儲存已修改的 PSD 檔案
將變更寫入新檔案。

```java
psdImage.save(outPsdFilePath);
```

## 步驟 7：清理資源
釋放 `PsdImage` 以回收記憶體。

```java
psdImage.dispose();
```

## 常見陷阱與技巧
- **Null 檢查** – 在存取路徑前務必確認 `resource` 不為 `null`。  
- **路徑索引範圍** – 確認您使用的索引（`[2]`、`[7]`、`[11]`）在特定 PSD 中確實存在。  
- **授權** – 未使用有效授權執行時，儲存的 PSD 會被嵌入浮水印。  

## 結論
您現在已掌握一個完整的端對端範例，說明如何透過 Aspose.PSD for Java **修改 PSD 向量形狀**，同時支援長度記錄資料屬性。無論是自動化資產流水線或打造自訂設計工具，這些 API 都能讓您在不使用 Photoshop 的情況下靈活操作向量圖層。可進一步嘗試其他 `PathOperations`，或結合多個 `LengthRecord` 的編輯，以產生更複雜的形狀。

## 常見問題
### 什麼是 Aspose.PSD for Java？
Aspose.PSD for Java 是一套函式庫，讓開發者能以 Java 程式碼程式化操作與處理 Photoshop PSD 檔案。

### 我可以在免費專案中使用 Aspose.PSD 嗎？
可以，您可使用 Aspose 官方網站提供的試用版免費體驗此函式庫。

### 我可以對 PSD 檔案做哪些類型的修改？
您可以操作圖層、形狀、文字、路徑操作等，功能相當完整。

### Aspose.PSD 是否相容於其他程式語言？
是的，Aspose 為多種程式語言提供相應函式庫，包含 .NET 與 Python 等。

### 我可以在哪裡找到 Aspose.PSD 的文件？
您可以在此取得完整文件 [here](https://reference.aspose.com/psd/java/)。

## Frequently Asked Questions

**Q: How do I handle a PSD that contains no vector shape layers?**  
A: The `VsmsResource` will be absent, so `resource` will stay `null`. Add a check and skip the modification step or inform the user.

**Q: Can I change other properties like fill color or stroke width?**  
A: Yes, `LengthRecord` provides additional setters for fill, stroke, and opacity. Refer to the API docs for full details.

**Q: Is it possible to batch‑process multiple PSD files?**  
A: Absolutely. Wrap the code inside a loop that iterates over a directory of PSD files, adjusting the input and output paths each time.

**Q: Do I need to close streams manually when loading from a file path?**  
A: The `Image.load` method handles file streams internally, but if you load from an `InputStream`, remember to close it after use.

**Q: What version of Aspose.PSD is required for these APIs?**  
A: The `LengthRecord` and `PathOperations` classes are available since Aspose.PSD 20.10. Using the latest version is recommended.

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}