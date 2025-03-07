---
title: 在 Aspose.PSD for .NET 中在執行時加入效果
linktitle: 在運行時加入效果
second_title: Aspose.PSD .NET API
description: 使用 Aspose.PSD for .NET 探索動態影像增強功能。運行時輕鬆添加效果。
weight: 10
url: /zh-hant/net/image-effects/add-effect-runtime/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Aspose.PSD for .NET 中在執行時加入效果

## 介紹

增強影像的視覺吸引力是圖形設計和影像處理應用中的常見要求。在本教學中，我們將探討如何使用 Aspose.PSD for .NET 在執行階段新增效果。 Aspose.PSD 是一個功能強大的 API，可讓開發人員無縫地處理 Adobe Photoshop 檔案。 

## 先決條件

在我們深入了解逐步指南之前，請確保您具備以下條件：

- C# 和 .NET 架構的基礎知識。
- 已安裝 Aspose.PSD for .NET。您可以從以下位置下載：[這裡](https://releases.aspose.com/psd/net/).

## 導入命名空間

首先，請確保在 C# 專案中包含必要的命名空間。這些命名空間對於利用 Aspose.PSD 提供的功能至關重要。

```csharp
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageLoadOptions;
```

## 第 1 步：設定您的文件目錄

```csharp
string dataDir = "Your Document Directory";
```

將「您的文件目錄」替換為 PSD 檔案所在的實際路徑。

## 步驟 2： 載入具有效果資源的 PSD 映像

```csharp
string sourceFileName = dataDir + "ThreeRegularLayers.psd";
string exportPath = dataDir + "ThreeRegularLayersChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
```

此步驟載入PSD影像，從而實現效果資源的載入。

## 第三步：新增顏色疊加效果

```csharp
var effect = im.Layers[1].BlendingOptions.AddColorOverlay();
effect.Color = Color.Green;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

在這裡，我們為 PSD 影像的第二層添加顏色疊加效果。您可以根據自己的喜好自訂顏色、不透明度和混合模式。

## 第四步：儲存修改後的影像

```csharp
im.Save(exportPath);
```

最後，將套用了效果的影像儲存到指定的匯出路徑。

## 結論

在執行時間在 Aspose.PSD for .NET 中加入效果是一個簡單的過程。只需幾行程式碼，您就可以動態增強影像的視覺吸引力。嘗試不同的效果和參數以獲得所需的結果。

## 常見問題解答

### Q1：Aspose.PSD 與最新的.NET 框架相容嗎？

A1：是的，Aspose.PSD 會定期更新，以確保與最新的 .NET 框架版本相容。

### Q2：我可以在一個圖層上套用多種效果嗎？

A2：當然！您可以在一個圖層上連結多個效果以創建複雜的視覺增強效果。

### Q3：我可以新增的效果類型有限制嗎？

A3：Aspose.PSD 提供了廣泛的效果，但建議檢查文件以了解支援的效果的具體細節。

### Q4：如何取得用於測試目的的臨時許可證？

 A4：您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/)用於測試和評估。

### Q5：我可以在哪裡找到更多支持和社區討論？

 A5：訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)以尋求支持和討論。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
