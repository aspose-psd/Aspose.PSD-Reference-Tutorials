---
title: Aspose.PSD for .NET でレイヤーにストローク効果を追加する
linktitle: レイヤーにストローク効果を追加する
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET で画像の美観を高めます。ストローク効果を段階的に追加する方法を学びます。今すぐダウンロード、購入、または無料試用版をお試しください。
weight: 10
url: /ja/net/layer-effects/adding-stroke-effects/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for .NET でレイヤーにストローク効果を追加する

## 導入

Aspose.PSD for .NET のレイヤーにストローク効果を追加する手順を説明したチュートリアルへようこそ。ストローク効果を使用すると、画像の視覚的な魅力を簡単に高めることができます。Aspose.PSD を使用すると、.NET 開発者にとってシームレスに実現できます。このガイドでは、この強力な機能を習得できるように、明確な手順と例を示しながらプロセスを順を追って説明します。

## 前提条件

チュートリアルに進む前に、次の前提条件が満たされていることを確認してください。

- Aspose.PSD for .NET: Aspose.PSDライブラリを以下のサイトからダウンロードしてインストールします。[Webサイト](https://releases.aspose.com/psd/net/).

- ドキュメント ディレクトリ: ストローク効果を適用する PSD ドキュメントを含むディレクトリを準備します。

- 出力ディレクトリ: ストローク効果のある出力画像を保存するための別のディレクトリを用意します。

- Visual Studio: Visual Studio またはその他の推奨される .NET 開発環境が設定されていることを確認します。

## 名前空間のインポート

.NET プロジェクトに、Aspose.PSD 機能を活用するために必要な名前空間を含めます。

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## ステップ1: PSDドキュメントを読み込む

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    //PSDドキュメントを読み込むためのコードをここに記述します
}
```

## ステップ2: カラーストローク効果を追加する

```csharp
//内側の位置に塗りつぶしの色を追加します。
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## ステップ3: 外側の位置

```csharp
//外側の位置に塗りつぶしの色を追加します。
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## ステップ4: 中心位置

```csharp
//中央位置にカラー塗りつぶしを追加します。
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

グラデーションとパターンの塗りつぶしについても同様の手順を繰り返し、それに応じて設定を調整します。

## 結論

おめでとうございます! Aspose.PSD for .NET を使用してレイヤーにストローク効果を追加する方法を学習しました。さまざまな設定を試して、画像に望ましい視覚効果を実現してください。

## よくある質問

### Q1: 特定のレイヤーにのみストローク効果を適用できますか?

A1: はい、コード内のレイヤー インデックスを調整することで、特定のレイヤーをターゲットにすることができます。

### Q2: Aspose.PSD は最新の .NET フレームワークと互換性がありますか?

A2: もちろんです! Aspose.PSD は、最新の .NET フレームワークとシームレスに統合するように設計されています。

### Q3: ストロークの色をカスタマイズするにはどうすればよいですか?

 A3: 単に`Color`コード内のプロパティを使用して、目的のストロークの色を実現します。

### Q4: Aspose.PSD は複数の PSD ファイルのバッチ処理をサポートしていますか?

A4: はい、複数の PSD ファイルをループし、同様のアプローチを使用してストローク効果を適用できます。

### Q5: Aspose.PSD を購入する前に試用版を使用できますか?

 A5: もちろんです！[無料トライアル](https://releases.aspose.com/)購入する前に Aspose.PSD の機能を調べてください。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
