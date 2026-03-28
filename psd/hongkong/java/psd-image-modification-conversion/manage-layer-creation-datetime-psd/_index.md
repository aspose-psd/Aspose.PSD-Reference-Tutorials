---
date: 2026-03-28
description: 學習如何使用 Aspose.PSD for Java 建立新的 PSD 圖層並管理其建立日期時間。本分步指南涵蓋載入、讀取、驗證及新增圖層。
linktitle: Create New PSD Layer and Manage Creation DateTime in Java
second_title: Aspose.PSD Java API
title: 在 Java 中建立新 PSD 圖層並管理建立日期時間
url: /zh-hant/java/psd-image-modification-conversion/manage-layer-creation-datetime-psd/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中建立新 PSD 圖層並管理建立日期時間

## 簡介
當你以程式方式處理 Photoshop (PSD) 檔案時，能夠 **create new PSD layer** 物件並追蹤其建立時間戳記，真的是一個顛覆性的功能。無論你是為設計資產建立版本控制系統、自動化批次編輯，或只是需要協作專案的稽核追蹤，了解如何讀取與設定圖層的建立日期，都能讓你完整記錄每一次變更的來源。本教學將使用 Aspose.PSD for Java，從載入 PSD、取得圖層的建立日期、驗證，最後新增一個全新的調整圖層，完整說明整個流程。

## 快速解答
- **什麼程式庫在 Java 中處理 PSD 檔案？** Aspose.PSD for Java  
- **我可以讀取圖層的建立日期嗎？** 可以，使用 `layer.getLayerCreationDateTime()`  
- **是否可以新增調整圖層？** 當然可以 – `im.addLevelsAdjustmentLayer()` 會建立一個  
- **生產環境需要授權嗎？** 非試用部署需購買商業授權  
- **支援哪個 Java 版本？** JDK 8 或更新版本  

## 什麼是「create new PSD layer」？
建立新 PSD 圖層指的是以程式方式在現有 PSD 文件中插入全新的圖層物件——例如調整圖層、文字圖層或像素圖層。此操作讓你在不手動開啟 Photoshop 的情況下擴充或修改圖像。

## 為什麼要管理圖層建立日期時間？
追蹤每個圖層的建立日期時間可協助你：
- **稽核修訂** – 精確知道圖層何時被加入。  
- **跨團隊同步資產**，透過比對時間戳記。  
- **自動化工作流程**，例如隱藏超過一個月的舊圖層。  

## 先決條件
在開始之前，請確保已準備好以下項目：

1. **Java Development Kit (JDK)** – 版本 8 或更新。  
2. **IDE** – IntelliJ IDEA、Eclipse、NetBeans，或任何你慣用的編輯器。  
3. **Aspose.PSD for Java** – 你可以 [在此下載](https://releases.aspose.com/psd/java/) 進行安裝。  
4. **基本的 Java 知識** – 若你是 Java 新手也沒關係，程式碼已完整註解。

全部就緒了嗎？太棒了！讓我們直接進入程式編寫的有趣部分。

## 匯入套件
首先，匯入 Aspose.PSD 類別與 Java 工具類別，這些匯入讓你能存取影像處理、圖層操作與日期格式化功能。

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

## 步驟 1：設定文件目錄
指定包含目標 PSD 的資料夾路徑，將佔位符替換為你機器上的絕對路徑。

```java
String dataDir = "Your Document Directory";
```

## 步驟 2：載入 PSD 檔案
建立 `PsdImage` 實例以載入目標檔案。此物件是所有圖層操作的入口點。

```java
String sourceName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceName);
```

## 步驟 3：存取圖層及其建立日期
取得第一個圖層（索引 0）並擷取其建立時間戳記。此日期稍後可用於比較或記錄。

```java
Layer layer = im.getLayers()[0];
Date creationDateTime = layer.getLayerCreationDateTime();
```

## 步驟 4：格式化建立日期
將原始 `Date` 物件轉換為可讀的字串。若想使用其他格式，可調整模式字串。

```java
DateFormat dateFormat = new SimpleDateFormat("yyyy/MM/dd HH:mm:ss");
```

## 步驟 5：驗證建立日期
為示範起見，我們將取得的日期與預期值做比較。實務上可能會與資料庫記錄或設定檔比較。

```java
Date expectedDateTime = new Date("2018/7/17 8:57:24");
Assert.areEqual(expectedDateTime, creationDateTime);
```

## 步驟 6：建立新圖層
現在我們實際 **create new PSD layer** 物件。此處我們加入 Levels 調整圖層，讓你在不改變原始像素的情況下微調色調範圍。

```java
Date now = new Date();
Layer createdLayer = im.addLevelsAdjustmentLayer();
```

> **專業提示：** `now` 變數會捕捉你加入圖層的瞬間，若需要自訂時間戳記，可稍後將其存為中繼資料。

## 常見問題與解決方案
| 問題 | 發生原因 | 解決方法 |
|------|----------|----------|
| 在 `layer.getLayerCreationDateTime()` 上發生 `NullPointerException` | PSD 沒有圖層或圖層索引超出範圍。 | 在存取前先確認 `im.getLayers().length > 0`。 |
| 日期驗證不符 | `Date` 建構子會以依地區設定的方式解析字串。 | 使用 `SimpleDateFormat.parse("2018/07/17 08:57:24")` 以確保可靠的解析。 |
| 新圖層在 Photoshop 中不可見 | 調整圖層預設可能是隱藏的。 | 建立後呼叫 `createdLayer.setVisible(true);`。 |

## 結論
現在你已瞭解如何 **create new PSD layer** 物件、讀取其建立時間戳記、驗證這些時間戳記，並加入調整圖層——全部透過 Aspose.PSD for Java 完成。此功能為任何基於 Java 的影像處理管線開啟了自動化、稽核追蹤與協作工作流程的大門。

如果你喜歡本教學，請探索其他 Aspose.PSD 功能，如合併圖層、套用濾鏡或匯出至不同格式。可能性無限！

## 常見問答
### 什麼是 Aspose.PSD？  
Aspose.PSD 是一套功能強大的程式庫，可程式化操作 Photoshop (PSD) 檔案。

### 我可以免費使用 Aspose.PSD 嗎？  
可以！你可以從 [此處](https://releases.aspose.com/) 開始免費試用。

### 長期使用需要購買授權嗎？  
是的，當你準備好後可於 [此處](https://purchase.aspose.com/buy) 取得授權。

### 哪裡可以找到更多關於 Aspose.PSD 的資訊？  
你可以查閱 [文件](https://reference.aspose.com/psd/java/) 取得詳細指南與 API 參考。

### 如果遇到 Aspose.PSD 的問題，我該如何尋求支援？  
歡迎前往 [支援論壇](https://forum.aspose.com/c/psd/34) 尋求社群協助。

---

**Last Updated:** 2026-03-28  
**Tested With:** Aspose.PSD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}