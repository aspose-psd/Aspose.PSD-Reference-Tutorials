---
date: 2026-03-04
description: 學習如何使用 Aspose.PSD for Java 以程式方式修改 PSD 圖層，透過新增填色圖層。跟隨此一步一步的指引，快速提升您的設計。
linktitle: Modify PSD Layers Programmatically – Add Fill Layers (Java)
second_title: Aspose.PSD Java API
title: 以程式方式修改 PSD 圖層 – 新增填充圖層（Java）
url: /zh-hant/java/modifying-converting-psd-images/add-fill-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 以程式方式修改 PSD 圖層 – 新增填色圖層（Java）

如果你想 **以程式方式修改 PSD 圖層**，新增填色圖層是最快速的方式之一，讓你在不開啟 Photoshop 的情況下豐富 Photoshop 文件。本教學將逐步說明如何建立新的 PSD、插入純色、漸層與圖案填色圖層，最後儲存結果——全部使用 Aspose.PSD for Java。

## 快速回答
- **可以做到什麼？** 以程式方式為 PSD 檔案新增純色、漸層與圖案填色圖層。  
- **需要哪個函式庫？** Aspose.PSD for Java（最新發行版）。  
- **需要授權嗎？** 免費試用可用於測試；正式上線需購買商業授權。  
- **實作需要多久？** 基本範例約 10‑15 分鐘即可完成。  
- **支援哪個 Java 版本？** JDK 11 或更新版本。

## 什麼是「以程式方式修改 PSD 圖層」？
以程式方式修改 PSD 圖層指的是使用程式碼在 Photoshop 文件內建立、編輯或刪除圖層，讓你在不需要手動操作 UI 的情況下，完整掌控設計工作流程。

## 為什麼要使用 Aspose.PSD 新增填色圖層？
- **自動化** – 在批次工作中產生數十個 PSD。  
- **一致性** – 在多個檔案中套用完全相同的顏色、漸層或圖案。  
- **速度** – 省去 Photoshop 中耗時的手動步驟。  
- **跨平台** – 只要支援 Java 的作業系統皆可執行。

## 前置需求
在進入程式碼之前，請先確認以下項目：

1. **Java Development Kit (JDK)** – 安裝 JDK 11 或更新版本。可從 [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下載。  
2. **Aspose.PSD for Java** – 從官方下載頁面 [here](https://releases.aspose.com/psd/java/) 取得最新函式庫。  
3. **IDE** – IntelliJ IDEA、Eclipse 或任何你慣用的編輯器。  
4. **基本的 Java 知識** – 熟悉類別與方法會比較順手，但本教學會一步步說明。

## 匯入套件
開始操作 PSD 檔案前，需要匯入相關的 Aspose.PSD 類別：

```java
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
```

這些匯入讓你可以存取 `PsdImage` 物件（即文件本身）以及我們即將使用的各種 `FillLayer` 類型。

## 以程式方式修改 PSD 圖層 – 步驟說明

### 步驟 1：設定輸出目錄
指定最終 PSD 的儲存位置，以便之後找尋。

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
```

將 `"Your Document Directory"` 替換為你機器上的絕對或相對路徑。

### 步驟 2：建立新的 Photoshop 文件
建立一個空白畫布，作為填色圖層的容器。

```java
PsdImage psdImage = new PsdImage(100, 100);
```

參數 `100, 100` 代表寬度與高度（單位：像素），可依設計需求自行調整。

### 步驟 3：新增純色填色圖層
建立一個純色填色圖層並為其命名。

```java
FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);
colorFillLayer.setDisplayName("Color Fill Layer");
psdImage.addLayer(colorFillLayer);
```

之後可透過圖層的填色設定變更實際顏色（此處未示範）。

### 步驟 4：新增漸層填色圖層
漸層填色可為畫面增添層次與視覺趣味。

```java
FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);
gradientFillLayer.setDisplayName("Gradient Fill Layer");
psdImage.addLayer(gradientFillLayer);
```

可依需求在圖層設定中切換線性或徑向漸層。

### 步驟 5：新增圖案填色圖層
圖案填色允許你在圖層上平鋪圖片或紋理。

```java
FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);
patternFillLayer.setDisplayName("Pattern Fill Layer");
patternFillLayer.setOpacity((byte)50);
psdImage.addLayer(patternFillLayer);
```

將不透明度設定為 50 % 可讓圖案與下層圖層自然融合。

### 步驟 6：儲存 PSD 檔案
將變更寫入磁碟。

```java
psdImage.save(outPsdFilePath);
```

在 Photoshop 或任何 PSD 檢視器中開啟，即可看到三個新填色圖層。

### 步驟 7：釋放資源
使用完 `PsdImage` 後務必釋放，以免佔用原生記憶體。

```java
psdImage.dispose();
```

## 常見問題與技巧
- **輸出路徑無效** – 確認目錄已存在且具有寫入權限。  
- **記憶體使用量** – 對於非常大的畫布，完成後立即呼叫 `psdImage.dispose()`。  
- **圖層順序** – 預設圖層會加入堆疊最上方；若需特定順序，可使用 `psdImage.insertLayer(layer, index)`。

## 常見問答

**Q: 使用 Aspose.PSD for Java 可以新增哪些類型的填色圖層？**  
A: 可新增純色、漸層與圖案填色圖層。

**Q: Aspose.PSD 支援其他影像格式嗎？**  
A: 支援，包含 BMP、JPEG、PNG 等多種格式。

**Q: 我可以免費使用 Aspose.PSD 嗎？**  
A: 可於此處取得 Aspose.PSD for Java 的免費試用版 [here](https://releases.aspose.com/).

**Q: 哪裡可以找到更多 Aspose.PSD 的文件？**  
A: 完整文件可在此處取得 [here](https://reference.aspose.com/psd/java/).

**Q: 有 Aspose.PSD 的支援社群嗎？**  
A: 有，請至 Aspose 論壇取得協助 [here](https://forum.aspose.com/c/psd/34)。

## 結論
現在你已學會如何 **以程式方式修改 PSD 圖層**，透過 Aspose.PSD for Java 新增各種填色圖層。此方法能為你節省時間、確保專案一致性，並開啟強大的批次處理可能性。試著變換不同的顏色、漸層與圖案，探索自動化設計創作的極限。

---

**最後更新：** 2026-03-04  
**測試環境：** Aspose.PSD for Java（最新發行版）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}