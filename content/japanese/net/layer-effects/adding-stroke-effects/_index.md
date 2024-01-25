---
title: Aspose.PSD for .NET のレイヤーにストローク エフェクトを追加する
linktitle: レイヤーにストローク効果を追加する
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用して画像の美しさを高めます。ストローク効果を追加する方法を段階的に学習します。今すぐダウンロード、購入、または無料トライアルを試してください。
type: docs
weight: 10
url: /ja/net/layer-effects/adding-stroke-effects/
---
## 導入

Aspose.PSD for .NET のレイヤーにストローク効果を追加するためのこのステップバイステップのチュートリアルへようこそ。ストローク効果を使用すると、画像の視覚的な魅力を簡単に高めることができ、Aspose.PSD を使用すると、.NET 開発者にとってそれがシームレスになります。このガイドでは、この強力な機能を習得するのに役立つ明確な手順と例を提供しながら、プロセスを順を追って説明します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

- Aspose.PSD for .NET: Aspose.PSD ライブラリを次の場所からダウンロードしてインストールします。[Webサイト](https://releases.aspose.com/psd/net/).

- ドキュメント ディレクトリ: ストローク エフェクトを適用する PSD ドキュメントを含むディレクトリを準備します。

- 出力ディレクトリ: ストローク エフェクトを含む出力イメージを保存するための別のディレクトリを用意します。

- Visual Studio: Visual Studio またはその他の優先 .NET 開発環境がセットアップされていることを確認します。

## 名前空間のインポート

.NET プロジェクトに、Aspose.PSD 機能を利用するために必要な名前空間を含めます。

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## ステップ 1: PSD ドキュメントをロードする

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    //PSD ドキュメントをロードするためのコードはここにあります
}
```

## ステップ 2: カラーストローク効果を追加する

```csharp
//内側の位置に色の塗りつぶしを追加します
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## ステップ 3: アウトサイド ポジション

```csharp
//外側の位置に色の塗りつぶしを追加します
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## ステップ 4: 中心位置

```csharp
//中央の位置に色の塗りつぶしを追加します
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

同様の手順をグラデーションとパターンの塗りつぶしに対して繰り返し、それに応じて設定を調整します。

## 結論

おめでとう！ Aspose.PSD for .NET を使用してレイヤーにストローク効果を追加する方法を学習しました。さまざまな設定を試して、画像に望ましい視覚的効果をもたらします。

## よくある質問

### Q1: ストロークエフェクトを特定のレイヤーにのみ適用できますか?

A1: はい、コード内のレイヤー インデックスを調整することで、特定のレイヤーをターゲットにすることができます。

### Q2: Aspose.PSD は最新の .NET Framework と互換性がありますか?

A2：もちろんです！ Aspose.PSD は、最新の .NET フレームワークとシームレスに統合するように設計されています。

### Q3: ストロークの色をカスタマイズするにはどうすればよいですか?

 A3:単に変更するだけです。`Color`コード内のプロパティを使用して、目的のストロークの色を実現します。

### Q4: Aspose.PSD は複数の PSD ファイルのバッチ処理をサポートしていますか?

A4: はい、複数の PSD ファイルをループし、同様のアプローチを使用してストローク エフェクトを適用できます。

### Q5: Aspose.PSD を購入する前に試用版を使用できますか?

 A5：確かに！をつかみます[無料トライアル](https://releases.aspose.com/)購入する前に、Aspose.PSD の機能を確認してください。