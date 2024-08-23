---
title: 在 PSD 中應用帶有顏色填充的描邊效果 - Java
linktitle: 在 PSD 中應用帶有顏色填充的描邊效果 - Java
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 將帶有顏色填滿的描邊效果套用到 PSD 檔案。請按照此逐步指南輕鬆增強您的影像。
type: docs
weight: 21
url: /zh-hant/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
---
## 介紹

在本指南中，我們將引導您完成使用 Aspose.PSD for Java 將帶有顏色填充的描邊效果套用到 PSD 檔案的過程。無論您是經驗豐富的開發人員還是新手，這個逐步教學都將幫助您輕鬆完成工作。我們將涵蓋從設定環境到保存應用程式效果的最終影像的所有內容。

## 先決條件

在開始之前，讓我們確保您已掌握本教學所需的一切：

1. 安裝 Java 開發工具包 (JDK)：確保您的系統上安裝了 JDK 8 或更高版本。
2.  Aspose.PSD for Java 函式庫：您將需要 Aspose.PSD for Java 函式庫。您可以從[網站](https://releases.aspose.com/psd/java/).
3. 整合開發環境 (IDE)：IntelliJ IDEA、Eclipse 或您選擇的任何其他 IDE。
4. 範例 PSD 檔案：可以套用描邊效果的範例 PSD 檔案。如果沒有，您可以在 Photoshop 中建立一個簡單的 PSD 檔案或從 Internet 下載一個。
5. Java 基礎：雖然本教學適合初學者，但掌握一些 Java 基礎知識將會有所幫助。

一旦滿足了這些先決條件，您就可以開始將具有顏色填滿的描邊效果套用到 PSD 檔案中。

## 導入包

要開始使用 Aspose.PSD for Java，您需要將必要的套件匯入到您的 Java 專案中。您可以這樣做：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

這些匯入引入了處理 PSD 檔案、應用效果以及以所需格式儲存影像所需的所有必要類別。

## 第 1 步：載入 PSD 文件

我們流程的第一步是載入您要修改的 PSD 檔案。 Aspose.PSD for Java 憑藉其`PsdImage`班級。您可以這樣做：

### 1.1 設定目錄路徑

首先，定義 PSD 檔案儲存的目錄路徑：

```java
String dataDir = "Your Document Directory";
```

代替`"Your Document Directory"`與 PSD 檔案所在的實際路徑。

### 1.2 載入PSD影像

現在，使用以下命令載入 PSD 文件`PsdLoadOptions`和`PsdImage`課程：

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

在這裡，`PsdLoadOptions`配置為載入效果資源，確保 PSD 中的任何現有效果均可存取。

## 步驟2：套用顏色填滿描邊效果

載入 PSD 檔案後，下一步是將描邊效果套用到影像的圖層。這才是真正的魔法發生的地方。

每個 PSD 檔案可能包含多個圖層，您需要將效果套用至每個圖層。操作方法如下：

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    settings.setColor(Color.getDeepPink());
}
```

在這個循環中：

- `im.getLayers()`：檢索 PSD 檔案中的所有圖層。
- `StrokeEffect effect`：擷取應用於圖層的描邊效果。
- `ColorFillSettings settings`：修改描邊效果的填滿設定。
- `settings.setColor(Color.getDeepPink())`：將描邊顏色設定為深粉紅色。您可以將其變更為您喜歡的任何顏色。

## 步驟3：儲存修改後的PSD並匯出為PNG

套用描邊效果後，就可以儲存變更並匯出影像了。

### 3.1 儲存PSD文件

若要儲存修改後的 PSD 文件，請使用以下程式碼：

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

這會將套用了描邊效果的檔案儲存到指定路徑。

### 3.2 導出為PNG

為了使圖像更易於訪問，您可能需要將其匯出為 PNG 檔案。方法如下：

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

此程式碼片段將圖像儲存為具有真彩色和 Alpha 透明度的 PNG，使其可以在 Web 應用程式或其他平台中使用。

## 結論

使用 Aspose.PSD for Java 將具有色彩填滿的描邊效果套用至 PSD 檔案不僅簡單，而且功能非常強大。只需幾行程式碼，您就可以自動執行複雜的影像處理任務，從而節省時間和精力。

無論您是處理大量影像還是只需要調整幾個文件，此方法都提供了靈活高效的解決方案。現在您已經掌握了基礎知識，您可以開始嘗試不同的效果和自訂，以使您的圖像真正脫穎而出。

準備好嘗試了嗎？立即取得範例 PSD 檔案並開始新增這些令人驚嘆的效果！

## 常見問題解答

### 我可以使用 Aspose.PSD for Java 將多種效果套用到單一圖層嗎？
是的，您可以透過存取圖層的混合選項並添加所需的效果，將多種效果套用到單一圖層。

### 是否可以自動化處理一批 PSD 檔案？
絕對地！您可以循環瀏覽 PSD 檔案的目錄、套用描邊效果並自動儲存結果。

### 如何使用 Aspose.PSD for Java 恢復對 PSD 檔案所做的變更？
要恢復更改，您需要在儲存任何修改之前重新載入原始 PSD 檔案。 Aspose.PSD 中沒有直接撤銷功能。

### 我可以自訂筆劃寬度和位置嗎？
是的，Aspose.PSD for Java 允許您透過以下方式自訂筆劃寬度、位置和其他屬性：`StrokeEffect`班級。

### Aspose.PSD for Java 函式庫可以免費使用嗎？
 Aspose.PSD for Java 提供免費試用版，但要完全存取所有功能，您需要購買授權。您可以探索[購買選擇權](https://purchase.aspose.com/buy)在他們的網站上。