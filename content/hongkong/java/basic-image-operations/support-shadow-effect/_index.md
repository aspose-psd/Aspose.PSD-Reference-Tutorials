---
title: Aspose.PSD for Java 支援陰影效果
linktitle: 支援陰影效果
second_title: Aspose.PSD Java API
description: 了解如何使用 Aspose.PSD for Java 為影像添加迷人的陰影效果。透過此逐步教學提升您的圖形設計。
type: docs
weight: 13
url: /zh-hant/java/basic-image-operations/support-shadow-effect/
---
## 介紹

使用陰影效果增強影像是圖形設計中的常見做法，可以增加深度和真實感。 Aspose.PSD for Java 為陰影效果提供了強大的支持，使開發人員能夠輕鬆地將這些效果整合到他們的 Java 應用程式中。在本教程中，我們將逐步探索如何使用 Aspose.PSD 支援陰影效果。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

- Java 程式設計的基礎知識。
-  Aspose.PSD for Java 已安裝。你可以下載它[這裡](https://releases.aspose.com/psd/java/).

## 導入包

確保您已匯入必要的套件以在 Java 應用程式中利用 Aspose.PSD 功能。使用以下程式碼片段作為指導：

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## 第 1 步：載入 PSD 映像

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## 步驟2：檢索陰影效果

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## 步驟 3：驗證預設設定

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

## 第四步：自訂陰影效果

```java
shadowEffect.setColor(Color.getGreen());
shadowEffect.setOpacity((byte)128);
shadowEffect.setDistance(11);
shadowEffect.setUseGlobalLight(false);
shadowEffect.setSize(9);
shadowEffect.setAngle(45);
shadowEffect.setSpread(3);
shadowEffect.setNoise(50);
```

## 步驟5：儲存修改後的影像

```java
im.save(psdPathAfterChange);
```

## 結論

透過這些簡單的步驟，您可以輕鬆地在 Aspose.PSD for Java 中支援陰影效果，增強影像的視覺吸引力。

## 常見問題解答

### Q1：Aspose.PSD for Java適合專業的圖形設計專案嗎？

A1：當然！ Aspose.PSD for Java 是一個功能強大的函式庫，專為專業圖形設計任務而設計。

### Q2：我可以在商業應用程式中使用Aspose.PSD for Java嗎？

 A2：是的，Aspose.PSD for Java 是商業產品。您可以購買[這裡](https://purchase.aspose.com/buy).

### Q3：有免費試用嗎？

A3：是的，您可以探索免費試用版。[這裡](https://releases.aspose.com/).

### Q4：哪裡可以找到詳細的文件？

 A4：參考綜合文檔[這裡](https://reference.aspose.com/psd/java/).

### Q5：如何獲得 Aspose.PSD for Java 的支援？

A5：加入社群論壇。[這裡](https://forum.aspose.com/c/psd/34)如有任何支援查詢。