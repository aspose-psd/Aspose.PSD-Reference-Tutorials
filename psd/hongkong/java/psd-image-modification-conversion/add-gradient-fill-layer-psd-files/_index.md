---
date: 2026-03-23
description: 學習如何使用 Java 及 Aspose.PSD 建立漸層填充的 PSD 檔案。本指南示範如何以程式方式編輯 PSD 漸層圖層、調整顏色、透明度及其他屬性。
linktitle: Create Gradient Fill PSD with Java – Add Gradient Fill Layer
second_title: Aspose.PSD Java API
title: 使用 Java 建立漸層填充 PSD – 新增漸層填充圖層
url: /zh-hant/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 PSD 檔案中使用 Java 新增漸層填色圖層

## 介紹

是否曾渴望為你的 PSD 檔案增添一抹視覺魔法，並好奇 **如何使用 Java 建立 gradient fill PSD**？漸層能為設計增添層次感，但手動調整往往繁瑣。透過 **Aspose.PSD for Java**，你可以以程式方式編輯 PSD 漸層、變更顏色、調整透明度，並微調每項屬性——節省時間且確保大量檔案的一致性。

## 快速解答
- **哪個函式庫可以在 Java 中編輯 PSD 漸層？** Aspose.PSD for Java。  
- **哪個方法用於載入 PSD 檔案？** `Image.load(path)`。  
- **如何變更漸層角度？** `settings.setAngle(double)`。  
- **可以新增顏色點嗎？** 可以——建立 `GradientColorPoint` 物件並加入顏色點清單。  
- **生產環境是否需要授權？** 需要商業授權；亦提供免費試用供評估使用。

## 什麼是「create gradient fill PSD」？
建立 gradient fill PSD 意指以程式方式在 Photoshop 文件中插入或修改基於漸層的填色圖層。這讓自動化樣式、批次處理與動態影像產生成為可能，且無需開啟 Photoshop。

## 為什麼選擇 Aspose.PSD 來編輯 PSD 漸層？
- **完整的 .PSD 支援** – 可處理所有圖層類型，包括智慧物件。  
- **不需 Photoshop** – 可在任何伺服器或 CI 流程中執行。  
- **細緻的控制** – 透過簡潔的 Java API 調整角度、偏移、抖動、顏色點與透明度點等屬性。

## 前置條件

在開始之前，請確保具備以下環境：

- Java Development Kit (JDK)：需要穩定版的 JDK 來執行 Java 程式碼。可從 Oracle 官方網站下載：[Link to Oracle JDK download page]  
- Aspose.PSD for Java：此功能強大的函式庫讓你在 Java 應用程式中操作 PSD 檔案。從 Aspose 官方網站下載：[Link to Aspose.PSD for Java download]（提供免費試用）

## 匯入套件

讓我們先匯入操作 PSD 檔案所需的 Aspose.PSD 套件：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.imageoptions.PsdOptions;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;
```

上述匯入提供了載入、操作與儲存 PSD 檔案的類別與方法。

現在，讓我們踏上修改漸層填色圖層的精彩旅程！

## 如何使用 Java 建立 Gradient Fill PSD

### 步驟 1：載入 PSD 檔案

首先，需要載入包含目標漸層填色圖層的 PSD 檔案。使用 `Image.load` 方法並指定檔案路徑：

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ComplexGradientFillLayer.psd";
String outputFile = dataDir + "ComplexGradientFillLayer_output.psd";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```

此程式碼片段會從指定目錄載入 PSD 檔案，並將其存入 `image` 變數。

### 步驟 2：識別 Gradient Fill 圖層

PSD 檔案可能包含多個圖層，我們需要找出包含漸層填色的特定圖層。遍歷 `image.getLayers()` 陣列以尋找目標圖層：

```java
for (int i = 0; i < image.getLayers().length; i++) {
if (image.getLayers()[i] instanceof FillLayer) {
   FillLayer fillLayer = (FillLayer) image.getLayers()[i];
   // Further checks and modifications will happen here
   break;
}
}
```

此迴圈會檢查每個圖層。若圖層為 `FillLayer`，則會轉型為 `FillLayer` 類型並存入 `fillLayer` 變數以供後續處理。若有特定條件（例如圖層名稱），可在迴圈內加入額外檢查。

### 步驟 3：驗證 Gradient Fill 類型

並非所有填色圖層都使用漸層。以下程式碼會確認已識別的圖層確實包含 Gradient Fill：

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Gradient) {
   throw new Exception("Wrong Fill Layer");
}
```

若 `getFillType` 方法未回傳 `FillType.Gradient`，則會拋出例外，表示目前操作的圖層不是漸層填色圖層。

## 使用 Aspose.PSD 編輯 PSD 漸層

### 步驟 4：存取並修改漸層屬性

魔法就在這裡！Aspose.PSD 透過 `IGradientFillSettings` 介面提供對各種漸層填色屬性的存取。我們可以依需求取得並修改它們：

```java
IGradientFillSettings settings = (IGradientFillSettings) fillLayer.getFillSettings();

// Modify properties (replace with desired values)
settings.setAngle(0.0);  // Set angle to 0 degrees
settings.setDither(false);  // Disable dithering
settings.setAlignWithLayer(true); // Align gradient with layer
settings.setReverse(true);  // Reverse gradient direction
settings.setHorizontalOffset(25);  // Set horizontal offset
settings.setVerticalOffset(-15);  // Set vertical offset
```

此程式碼取得 `IGradientFillSettings` 物件，並修改角度、抖動、對齊方式與偏移等屬性。請將範例值替換為你想要的設定，以實現理想的漸層效果。

### 步驟 5：操作顏色與透明度點

漸層是由色彩點與透明度點在光譜上定義的。Aspose.PSD 允許你精確調整這些點：

```java
List<IGradientColorPoint> colorPoints = new ArrayList<IGradientColorPoint>();
Collections.addAll(colorPoints, settings.getColorPoints());
List<IGradientTransparencyPoint> transparencyPoints = new ArrayList<IGradientTransparencyPoint>();
Collections.addAll(transparencyPoints, settings.getTransparencyPoints());

// Add a new color point
GradientColorPoint gr1 = new GradientColorPoint();
gr1.setColor(Color.getViolet());
gr1.setLocation(4096);
gr1.setMedianPointLocation(75);
colorPoints.add(gr1);

// Modify an existing color point
colorPoints.get(1).setLocation(3000);

// Add a new transparency point
GradientTransparencyPoint gr2 = new GradientTransparencyPoint();
gr2.setOpacity(80.0);
gr2.setLocation(4096);
gr2.setMedianPointLocation(25);
transparencyPoints.add(gr2);

// Modify an existing transparency point
transparencyPoints.get(2).setLocation(3000);

settings.setColorPoints(colorPoints.toArray(new IGradientColorPoint[0]));
settings.setTransparencyPoints(transparencyPoints.toArray(new IGradientTransparencyPoint[0]));
```

### 步驟 6：更新並儲存 PSD 檔案

完成所有修改後，更新填色圖層並儲存 PSD 檔案：

```java
fillLayer.update();
image.save(outputFile, new PsdOptions(image));
```

`fillLayer.update()` 方法會將變更套用至漸層填色圖層，`image.save` 則會將修改後的 PSD 檔案寫入指定的輸出路徑。

## 常見問題與解決方案

- **例外 “Wrong Fill Layer”** – 請確認目標圖層確實是使用漸層的 `FillLayer`。在轉型前檢查圖層名稱或索引。  
- **顏色點未反映變更** – 修改點清單後，務必呼叫 `settings.setColorPoints(...)` 與 `settings.setTransparencyPoints(...)`，將更新寫回圖層。  
- **大型 PSD 的效能** – 若處理大量檔案，請重複使用同一個 `PsdOptions` 實例，並在完成後立即以 `image.dispose()` 釋放記憶體。

## 常見問答

**Q: 可以在漸層中加入多個顏色與透明度點嗎？**  
A: 當然可以！你可以依需求新增任意數量的顏色與透明度點，只要建立新點並加入相應的清單即可。

**Q: 如何從漸層中移除某個顏色或透明度點？**  
A: 使用清單的 `remove` 方法，例如 `colorPoints.remove(index)`，在呼叫 `setColorPoints` 前將不需要的點刪除。

**Q: 能改變漸層類型（線性、徑向等）嗎？**  
A: 目前 Aspose.PSD 只支援線性漸層。未來版本可能會加入更多類型，亦可透過調整顏色與透明度點模擬其他效果。

**Q: 修改漸層會不會影響效能？**  
A: 影響程度取決於漸層的複雜度與修改次數。一般使用情境下開銷很小，但若批次處理大型檔案，建議進行記憶體管理優化。

**Q: 能否將此技巧套用於 PSD 檔案中的多個 Gradient Fill 圖層？**  
A: 可以。遍歷 `image.getLayers()`，檢查每個 `FillLayer` 的 `FillType` 是否為 `FillType.Gradient`，然後對需要的圖層套用相同的修改。

**Q: 生產環境是否需要商業授權？**  
A: 需要有效的 Aspose.PSD 授權才能在生產環境部署。亦提供免費試用供評估使用。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**最後更新：** 2026-03-23  
**測試環境：** Aspose.PSD for Java 24.11 (latest)  
**作者：** Aspose