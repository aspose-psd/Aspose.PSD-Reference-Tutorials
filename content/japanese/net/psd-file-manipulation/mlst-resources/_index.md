---
title: Aspose.PSD for .NET での MLST リソース処理をマスターする
linktitle: MLSTリソースの処理
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用して Photoshop ファイルのレイヤー状態を操作する方法を学びます。 MLST リソースを効率的に処理するには、ステップバイステップのガイドに従ってください。
type: docs
weight: 14
url: /ja/net/psd-file-manipulation/mlst-resources/
---
## 導入
Aspose.PSD for .NET での MLST (Multiple Layer States) リソースの処理に関する詳細なチュートリアルへようこそ。 Aspose.PSD for .NET は、Photoshop ファイルを操作するための広範な機能を提供する強力なライブラリです。このチュートリアルでは、レイヤー状態を効率的に操作するための低レベルのメカニズムを提供する MLST リソースのサポートに焦点を当てます。
## 前提条件
チュートリアルを詳しく説明する前に、次の前提条件が満たされていることを確認してください。
-  Aspose.PSD for .NET Library: ライブラリがインストールされていることを確認してください。そうでない場合は、からダウンロードできます。[.NET 用 Aspose.PSD ダウンロード ページ](https://releases.aspose.com/psd/net/).
- ドキュメント ディレクトリと出力ディレクトリ: ドキュメント ディレクトリを設定します (`baseDir`) と出力ディレクトリ (`outputDir`) 提供されたコードに含まれています。
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
## ステップ 1: ディレクトリ パスを設定する
```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```
「ドキュメント ディレクトリ」と「出力ディレクトリ」をプロジェクト内の実際のパスに置き換えてください。
## ステップ 2: PSD 画像をロードする
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
string outputPsd = Path.Combine(outputDir, "output_image1219.psd");
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    //操作用のコードは後続の手順で追加します。
}
```
## ステップ 3: MLST リソースにアクセスする
```csharp
Layer layer1 = image.Layers[1];
ShmdResource shmdResource = (ShmdResource)layer1.Resources[8];
MlstResource mlstResource = (MlstResource)shmdResource.SubResources[0];
```
## ステップ 4: 画層状態を操作する
```csharp
ListStructure layerStatesList = (ListStructure)mlstResource.Items[1];
DescriptorStructure layersStateOnFrame1 = (DescriptorStructure)layerStatesList.Types[1];
BooleanStructure layerEnabled = (BooleanStructure)layersStateOnFrame1.Structures[0];
//フレーム 1 のレイヤー 1 を無効にする
layerEnabled.Value = false;
```
## ステップ 5: 変更したイメージを保存する
```csharp
image.Save(outputPsd);
```
## ステップ 6: クリーンアップ
```csharp
File.Delete(outputPsd);
Console.WriteLine("SupportOfMlstResource executed successfully");
```
## 結論

おめでとう！ Aspose.PSD for .NET で MLST リソースを処理する方法を学習しました。この機能は、Photoshop ファイルのレイヤー状態をプログラムで操作するための堅牢なメカニズムを提供します。

## よくある質問

### Q1: Aspose.PSD for .NET を使用して、Photoshop の異なるバージョンで作成された PSD ファイルを操作できますか?

A1: はい、Aspose.PSD for .NET は、Photoshop のさまざまなバージョンで作成された PSD ファイルをサポートしています。

### Q2: Aspose.PSD for .NET の無料トライアルはありますか?

 A2: はい、次のサイトから無料トライアルをダウンロードできます。[リリースページ](https://releases.aspose.com/).

### Q3: Aspose.PSD for .NET の詳細なドキュメントはどこで見つけられますか?

A3: ドキュメントは入手可能です。[ここ](https://reference.aspose.com/psd/net/).

### Q4: Aspose.PSD for .NET のサポートを受けるにはどうすればよいですか?

 A4: にアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティサポートのために。

### Q5: Aspose.PSD for .NET のライセンスはどのように購入すればよいですか?

 A5: ライセンスを購入することができます。[ここ](https://purchase.aspose.com/buy).