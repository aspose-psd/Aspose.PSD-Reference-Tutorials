---
title: 在 Aspose.PSD for .NET 中使用時間軸
linktitle: 使用時間軸
second_title: Aspose.PSD .NET API
description: 使用 Aspose.PSD for .NET Timeline 類別增強 PSD 影像操作。控制框架屬性、圖層狀態並輕鬆釋放創意可能性。
type: docs
weight: 16
url: /zh-hant/net/psd-file-manipulation/timeline/
---
## 介紹
在圖形設計和影像處理的動態世界中，控制和操作影像時間軸的能力至關重要。 Aspose.PSD for .NET 透過其 Timeline 類別提供了強大的解決方案。這項進階功能使用戶能夠更改 PsdImage 的時間軸，例如更改幀延遲、編輯特定幀上的圖層狀態等。
## 先決條件
在深入研究 Timeline 類別提供的令人興奮的可能性之前，請確保您具備以下先決條件：
-  Aspose.PSD for .NET 函式庫：確保您已安裝 Aspose.PSD for .NET 函式庫。您可以從[Aspose.PSD for .NET 文檔](https://reference.aspose.com/psd/net/).
- 文檔和輸出目錄：在程式碼中定義文檔和輸出目錄的路徑。調整`baseDir`和`outputDir`根據您的項目結構的變數。
現在，讓我們逐步探索如何使用 Timeline 類別。
## 導入命名空間
若要開始使用 Timeline 類，請在程式碼中匯入必要的命名空間：
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## 第 1 步：載入 PSD 映像
首先從指定的來源檔案載入 PSD 映像。確保來源檔案路徑設定正確：
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //您用於進一步操作的程式碼位於此處
}
```
## 第 2 步：訪問時間軸
載入 PSD 影像後，使用以下程式碼存取時間軸：
```csharp
Timeline timeline = psdImage.Timeline;
```
## 第 3 步：更改處置方法
操縱特定框架的處理方法。在這個例子中，我們改變了第1幀的dispose方法：
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## 步驟 4：調整幀延遲
修改特定幀的延遲。這裡，我們將第 2 幀的延遲改為 15：
```csharp
timeline.Frames[1].Delay = 15;
```
## 第5步：編輯圖層狀態
變更特定影格上「第 1 層」的不透明度。在本例中，我們將第 2 幀的不透明度設為 50：
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## 第6步：移動圖層
將「圖層 1」移到特定影格（本例為影格 3）的左下角：
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## 第7步：新增框架
將新幀新增至時間軸：
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## 第 8 步：更改混合模式
變更特定影格（本例為影格 4）上「第 1 層」的混合模式：
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## 第 9 步：儲存更改
將變更套用回 PsdImage 實例並儲存修改後的 PSD 映像：
```csharp
psdImage.Save(outputPsd);
```
## 第10步：清理
最後，透過刪除臨時輸出檔進行清理：
```csharp
File.Delete(outputPsd);
```
## 結論

總之，Aspose.PSD for .NET 中的 Timeline 類別使開發人員能夠對 PSD 影像的時間軸進行精細控制。透過一系列簡單的步驟，您可以操縱框架屬性、圖層狀態等，從而開啟創意可能性的領域。

## 常見問題解答

### Q1：Aspose.PSD for .NET 適合初學者嗎？

A1：當然！ Aspose.PSD for .NET 提供了使用者友善的介面和全面的文檔，使初學者和經驗豐富的開發人員都可以使用它。

### 問題 2：我可以對 GIF 影像套用時間軸變更嗎？

A2：Timeline 類別是專門為 PSD 影像設計的。有關 GIF 操作，請參閱 Aspose.GIF for .NET。

### Q3：我可以在哪裡找到更多支援或討論問題？

 A3：訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)以獲得社區支持和問題討論。

### Q4：如何取得 Aspose.PSD for .NET 的臨時授權？

 A4：獲得臨時許可證。[這裡](https://purchase.aspose.com/temporary-license/).

### 問題 5：使用 Aspose.PSD for .NET 有哪些主要好處？

A5：Aspose.PSD for .NET 提供先進的影像處理功能、PSD 檔案操作和高效能渲染。