---
title: 掌握 Aspose.PSD for .NET 中的 MLST 資源處理
linktitle: 處理 MLST 資源
second_title: Aspose.PSD .NET API
description: 學習使用 Aspose.PSD for .NET 操作 Photoshop 檔案中的圖層狀態。請按照我們的逐步指南進行高效率的 MLST 資源處理。
weight: 14
url: /zh-hant/net/psd-file-manipulation/mlst-resources/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 掌握 Aspose.PSD for .NET 中的 MLST 資源處理

## 介紹
歡迎來到在 Aspose.PSD for .NET 中處理 MLST（多層狀態）資源的深入教學。 Aspose.PSD for .NET 是一個功能強大的程式庫，提供了處理 Photoshop 檔案的廣泛功能。在本教程中，我們將重點關注 MLST 資源的支持，提供有效操作層狀態的低階機制。
## 先決條件
在我們深入研究本教程之前，請確保您具備以下先決條件：
-  Aspose.PSD for .NET Library：確保您已安裝該程式庫。如果沒有，您可以從以下位置下載[Aspose.PSD for .NET 下載頁面](https://releases.aspose.com/psd/net/).
- 文檔和輸出目錄：設定文檔目錄（`baseDir`）和輸出目錄（`outputDir`）在提供的程式碼中。
## 導入命名空間
在您的 .NET 專案中，包含使用 Aspose.PSD 所需的命名空間：
```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures;
```
## 第 1 步：設定目錄路徑
```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```
確保將“您的文件目錄”和“您的輸出目錄”替換為專案中的實際路徑。
## 第 2 步：載入 PSD 映像
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
string outputPsd = Path.Combine(outputDir, "output_image1219.psd");
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    //操作代碼將在後續步驟中新增。
}
```
## 步驟3：存取MLST資源
```csharp
Layer layer1 = image.Layers[1];
ShmdResource shmdResource = (ShmdResource)layer1.Resources[8];
MlstResource mlstResource = (MlstResource)shmdResource.SubResources[0];
```
## 第 4 步：操縱圖層狀態
```csharp
ListStructure layerStatesList = (ListStructure)mlstResource.Items[1];
DescriptorStructure layersStateOnFrame1 = (DescriptorStructure)layerStatesList.Types[1];
BooleanStructure layerEnabled = (BooleanStructure)layersStateOnFrame1.Structures[0];
//在第 1 幀上停用第 1 層
layerEnabled.Value = false;
```
## 步驟5：儲存修改後的影像
```csharp
image.Save(outputPsd);
```
## 第 6 步：清理
```csharp
File.Delete(outputPsd);
Console.WriteLine("SupportOfMlstResource executed successfully");
```
## 結論

恭喜！您已成功學習如何處理 Aspose.PSD for .NET 中的 MLST 資源。此功能提供了一種強大的機制，可以透過程式設計來操縱 Photoshop 檔案中的圖層狀態。

## 常見問題解答

### Q1：我可以使用 Aspose.PSD for .NET 來處理在不同 Photoshop 版本中建立的 PSD 檔案嗎？

A1：是的，Aspose.PSD for .NET 支援在各種 Photoshop 版本中建立的 PSD 檔案。

### 問題 2：Aspose.PSD for .NET 是否有免費試用版？

 A2：是的，您可以從[發布頁面](https://releases.aspose.com/).

### Q3：在哪裡可以找到 Aspose.PSD for .NET 的詳細文件？

A3：文檔可用[這裡](https://reference.aspose.com/psd/net/).

### 問題 4：如何獲得 Aspose.PSD for .NET 支援？

 A4：訪問[Aspose.PSD 論壇](https://forum.aspose.com/c/psd/34)以獲得社區支持。

### Q5：如何購買 Aspose.PSD for .NET 的授權？

 A5：您可以購買許可證[這裡](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
