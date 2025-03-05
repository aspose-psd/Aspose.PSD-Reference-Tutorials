---
title: Aspose.PSD for .NET での MLST リソース処理の習得
linktitle: MLST リソースの取り扱い
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用して Photoshop ファイルのレイヤー状態を操作する方法を学びます。効率的な MLST リソース処理については、ステップバイステップ ガイドに従ってください。
type: docs
weight: 14
url: /ja/net/psd-file-manipulation/mlst-resources/
---
## 導入
Aspose.PSD for .NET での MLST (Multiple Layer States) リソースの処理に関する詳細なチュートリアルへようこそ。Aspose.PSD for .NET は、Photoshop ファイルの操作に広範な機能を提供する強力なライブラリです。このチュートリアルでは、レイヤー状態を効率的に操作するための低レベルのメカニズムを提供する MLST リソースのサポートに焦点を当てます。
## 前提条件
チュートリアルに進む前に、次の前提条件が満たされていることを確認してください。
-  Aspose.PSD for .NETライブラリ: ライブラリがインストールされていることを確認してください。インストールされていない場合は、[Aspose.PSD for .NET のダウンロード ページ](https://releases.aspose.com/psd/net/).
- ドキュメントと出力ディレクトリ: ドキュメントディレクトリを設定します (`baseDir`) および出力ディレクトリ (`outputDir`) を、提供されたコードに含めます。
## 名前空間のインポート
.NET プロジェクトに、Aspose.PSD を操作するために必要な名前空間を含めます。
```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures;
```
## ステップ1: ディレクトリパスを設定する
```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```
「ドキュメント ディレクトリ」と「出力ディレクトリ」をプロジェクト内の実際のパスに置き換えてください。
## ステップ2: PSDイメージを読み込む
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
string outputPsd = Path.Combine(outputDir, "output_image1219.psd");
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    //操作用のコードは後続の手順で追加されます。
}
```
## ステップ3: MLSTリソースにアクセスする
```csharp
Layer layer1 = image.Layers[1];
ShmdResource shmdResource = (ShmdResource)layer1.Resources[8];
MlstResource mlstResource = (MlstResource)shmdResource.SubResources[0];
```
## ステップ4: レイヤーの状態を操作する
```csharp
ListStructure layerStatesList = (ListStructure)mlstResource.Items[1];
DescriptorStructure layersStateOnFrame1 = (DescriptorStructure)layerStatesList.Types[1];
BooleanStructure layerEnabled = (BooleanStructure)layersStateOnFrame1.Structures[0];
//フレーム1のレイヤー1を無効にする
layerEnabled.Value = false;
```
## ステップ5: 変更した画像を保存する
```csharp
image.Save(outputPsd);
```
## ステップ6: クリーンアップ
```csharp
File.Delete(outputPsd);
Console.WriteLine("SupportOfMlstResource executed successfully");
```
## 結論

おめでとうございます。Aspose.PSD for .NET で MLST リソースを処理する方法を学習しました。この機能は、Photoshop ファイル内のレイヤー状態をプログラムで操作するための堅牢なメカニズムを提供します。

## よくある質問

### Q1: Aspose.PSD for .NET を使用して、異なる Photoshop バージョンで作成された PSD ファイルを操作できますか?

A1: はい、Aspose.PSD for .NET はさまざまな Photoshop バージョンで作成された PSD ファイルをサポートしています。

### Q2: Aspose.PSD for .NET の無料試用版はありますか?

 A2: はい、無料トライアルは[リリースページ](https://releases.aspose.com/).

### Q3: Aspose.PSD for .NET の詳細なドキュメントはどこで入手できますか?

A3: ドキュメントは入手可能です[ここ](https://reference.aspose.com/psd/net/).

### Q4: Aspose.PSD for .NET のサポートを受けるにはどうすればよいですか?

 A4: 訪問[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティサポートのため。

### Q5: Aspose.PSD for .NET のライセンスを購入するにはどうすればよいですか?

 A5: ライセンスを購入することができます[ここ](https://purchase.aspose.com/buy).