---
title: 在 Aspose.PSD for Java 中加入圖案效果
linktitle: 添加圖案效果
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD for Java 輕鬆增強您的 Java 影像圖案。按照我們的逐步教學添加迷人的圖案效果。
type: docs
weight: 12
url: /zh-hant/java/advanced-image-effects/add-pattern-effects/
---
## 介紹

在 Java 開發領域，增強影像模式是一項常見任務，Aspose.PSD for Java 為此提供了強大的解決方案。本教學將引導您使用 Aspose.PSD 添加圖案效果的過程，確保您的影像透過獨特的疊加和增強功能脫穎而出。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

- 您的系統上安裝了 Java 開發工具包 (JDK)。
- 下載 Aspose.PSD for Java 程式庫並將其新增至您的專案。您可以從[Aspose.PSD 網站](https://releases.aspose.com/psd/java/).

## 導入包

在您的 Java 專案中，匯入使用 Aspose.PSD 所需的套件。在 Java 類別的開頭包含以下程式碼：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.PatternOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

import java.util.UUID;
```

## 第 1 步：載入圖像

```java
//載入 PSD 映像
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

確保將“YourImagePath”和“YourExportPath”替換為專案中的實際路徑。

## 步驟 2：提取模式疊加訊息

```java
//提取有關圖案疊加的信息
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## 步驟 3：修改圖案疊加設置

```java
//修改圖案疊加設置
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

## 步驟 4：編輯圖案數據

```java
//編輯花樣數據
PattResource resource;
UUID guid = UUID.randomUUID();
String newPatternName = "$$/Presets/Patterns/Pattern=Some new pattern name\0";

for (int i = 0; i < im.getGlobalLayerResources().length; i++) {
    if (im.getGlobalLayerResources()[i] instanceof PattResource) {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName(newPatternName);
        resource.setPattern(new int[]{Color.getAqua().toArgb(), Color.getRed().toArgb(),
                        Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(),
                        Color.getWhite().toArgb(), Color.getAqua().toArgb()}, new Rectangle(0, 0, 4, 2));
    }
}
```

## 第5步：儲存編輯後的影像

```java
//儲存編輯後的影像
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## 第 6 步：驗證更改

```java
//驗證編輯文件中的更改
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

//添加斷言以確保更改已成功應用
```

## 結論

恭喜！您已經成功學習如何使用 Aspose.PSD for Java 添加圖案效果。這個強大的庫允許您創建具有自訂圖案的視覺上吸引人的圖像，為您的基於 Java 的專案提供無限的可能性。

## 常見問題解答

### Q1：我可以將 Aspose.PSD for Java 與其他 Java 映像處理庫一起使用嗎？

A1：Aspose.PSD for Java 設計為獨立工作，但如果需要，您可以將其與其他 Java 程式庫整合。

### Q2：在哪裡可以找到 Aspose.PSD for Java 的詳細文件？

 A2：請參閱[Aspose.PSD for Java 文檔](https://reference.aspose.com/psd/java/)以獲得全面的資訊。

### Q3：Aspose.PSD for Java 有免費試用版嗎？

 A3：是的，您可以免費試用。[這裡](https://releases.aspose.com/).

### Q4：如何獲得 Aspose.PSD for Java 的支援？

 A4：訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)尋求社區支持或考慮購買支持計劃。

### Q5：我可以獲得 Aspose.PSD for Java 的臨時授權嗎？

A5: 是的，您可以獲得臨時許可證。[這裡](https://purchase.aspose.com/temporary-license/).