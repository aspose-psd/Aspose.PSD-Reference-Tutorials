---
title: 在 Aspose.PSD for Java 中加入描邊圖層顏色
linktitle: 新增描邊圖層顏色
second_title: Aspose.PSD Java API
description: 透過我們有關新增描邊圖層顏色的逐步指南，探索 Aspose.PSD for Java 的強大功能。輕鬆提升您的圖形設計。
type: docs
weight: 14
url: /zh-hant/java/advanced-image-effects/add-stroke-layer-color/
---
## 介紹

使用 Aspose.PSD 釋放 Java 應用程式圖形設計的潛力。在本教程中，我們將深入研究使用 Aspose.PSD for Java 添加描邊圖層顏色的迷人世界。使用流行的筆觸增強您的圖形，輕鬆創建具有視覺吸引力的設計。

## 先決條件

在開始這趟創意之旅之前，請確保您具備以下先決條件：

-  Aspose.PSD 庫：按照以下步驟下載並設定 Aspose.PSD 庫[文件](https://reference.aspose.com/psd/java/).

- Java 開發工具包 (JDK)：確保您的系統上安裝了 Java。

- 整合開發環境（IDE）：選擇您喜歡的IDE； Eclipse 或 IntelliJ 是流行的選擇。

## 導入包

讓我們先導入必要的套件來實現 Aspose.PSD 的魔力。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## 第 1 步：設定您的項目

首先在您首選的 IDE 中建立一個新的 Java 專案。確保 Aspose.PSD 庫已新增至您的專案。

## 第 2 步：載入 PSD 文件

使用Aspose.PSD載入PSD文件，從而能夠載入效果資源。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## 步驟3：存取描邊層

存取 PSD 檔案中的描邊效果圖層。

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## 第 4 步：驗證筆畫屬性

確保筆劃屬性符合預期。

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## 第 5 步：設定顏色和不透明度

修改描邊圖層的顏色和不透明度。

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## 第6步：儲存修改後的PSD

使用新新增的描邊圖層顏色儲存修改後的 PSD 檔案。

```java
im.save(exportPath);
```

## 結論

恭喜！您已使用 Aspose.PSD for Java 成功將描邊圖層顏色新增至 PSD 檔案。嘗試不同的顏色和設置，讓您的圖形設計栩栩如生。

## 常見問題解答

### Q1：我可以將Aspose.PSD與其他Java圖形庫一起使用嗎？

A1：是的，Aspose.PSD 可以與其他 Java 圖形庫整合以增強功能。

### Q2：Aspose.PSD 與最新的 PSD 檔案格式相容嗎？

A2：當然！ Aspose.PSD 與最新的 PSD 檔案格式規格保持同步，確保相容性。

### Q3：使用Aspose.PSD時如何處理異常？

 A3：請參閱[支援論壇](https://forum.aspose.com/c/psd/34)尋求處理異常和故障排除方面的協助。

### Q4: 我可以在購買前試用Aspose.PSD嗎？

 A4：當然！抓住一個[免費試用](https://releases.aspose.com/)在做出承諾之前探索 Aspose.PSD 的功能。

### Q5: 我可以在哪裡獲得 Aspose.PSD 的臨時授權？

 A5：獲得[臨時執照](https://purchase.aspose.com/temporary-license/)讓 Aspose.PSD 評估其在您的專案中的功能。