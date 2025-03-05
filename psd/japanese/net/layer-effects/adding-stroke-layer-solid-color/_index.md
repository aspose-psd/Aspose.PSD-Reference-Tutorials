---
title: Aspose.PSD for .NET で単色のストローク レイヤーを追加する
linktitle: 単色ストロークレイヤーの追加
second_title: Aspose.PSD .NET API
description: Aspose.PSD を使用して .NET 画像操作スキルを強化します。単色でストローク レイヤーを追加する方法を段階的に学習します。
type: docs
weight: 11
url: /ja/net/layer-effects/adding-stroke-layer-solid-color/
---
## 導入

.NET 開発の分野では、視覚的に魅力的な画像を作成することが一般的な要件です。Aspose.PSD for .NET は、画像をシームレスに操作および強化するための強力なツール セットを提供します。重要な機能の 1 つは、単色のストローク レイヤーを追加することです。これにより、画像に鮮やかさと深みがもたらされます。このチュートリアルでは、Aspose.PSD for .NET を使用して、プロセスを段階的に説明します。

## 前提条件

チュートリアルに進む前に、次の前提条件を満たしていることを確認してください。

- .NET 開発に関する基本的な知識。
- マシンに Visual Studio がインストールされています。
- Aspose.PSD for .NETライブラリ。以下からダウンロードできます。[Webサイト](https://releases.aspose.com/psd/net/).

## 名前空間のインポート

まず、Aspose.PSD for .NET の機能を活用するために必要な名前空間をインポートします。

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## ステップ1: PSDファイルを読み込む

まず、ストローク レイヤーで強化したい PSD ファイルを読み込みます。ファイル パスが正しいことを確認します。

```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "Stroke.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    //以降の手順のコードはここに追加されます
}
```

## ステップ2: ストローク効果のプロパティにアクセスする

PSD ファイルからストローク効果のプロパティを取得します。

```csharp
var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

if ((colorStroke.BlendMode != BlendMode.Normal) ||
    (colorStroke.Opacity != 255) ||
    (colorStroke.IsVisible != true))
{
    throw new Exception("Color stroke effect was read wrong");
}
```

## ステップ3: ストローク設定を調整する

好みに応じてストローク設定を変更します。この例では、色を黄色に変更し、不透明度を 127 に設定し、カラーブレンド モードを使用します。

```csharp
var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

if ((fillSettings.Color != Color.Black) || (fillSettings.FillType != FillType.Color))
{
    throw new Exception("Color stroke effect settings were read wrong");
}

fillSettings.Color = Color.Yellow;
colorStroke.Opacity = 127;
colorStroke.BlendMode = BlendMode.Color;
```

## ステップ4: 編集した画像を保存する

ストローク レイヤーの変更を適用した後、画像を保存します。

```csharp
string exportPath = dataDir + "StrokeGradientChanged.psd";
im.Save(exportPath);
```

## ステップ5: 変更を確認する

編集した画像を読み込んで検査し、変更が正しく適用されていることを確認します。

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    //変更を確認するためのコードがここに追加されます
}
```

これらの手順を繰り返してさらに調整するか、さまざまなストローク効果を試して、目的の視覚効果を実現します。

## 結論

おめでとうございます! Aspose.PSD for .NET を使用して単色のストローク レイヤーを追加する方法を学習しました。この強力な機能により、.NET 環境で画像を強化するための可能性が広がります。

## よくある質問

### Q1: Aspose.PSD for .NET は最新の .NET Framework バージョンと互換性がありますか?

A1: はい、Aspose.PSD for .NET は、最新の .NET フレームワーク バージョンとの互換性を確保するために定期的に更新されます。

### Q2: Aspose.PSD for .NET を商用プロジェクトに使用できますか?

A2: もちろんです! Aspose.PSD for .NET は商用製品であり、ライセンスを購入することでプロジェクトで使用できます。

### Q3: Aspose.PSD for .NET のその他の例やドキュメントはどこで入手できますか?

 A3: 探索する[ドキュメント](https://reference.aspose.com/psd/net/)包括的な例とガイダンスについては、こちらをご覧ください。

### Q4: Aspose.PSD for .NET の無料試用版はありますか?

 A4: はい、無料トライアルをご利用いただけます。[リリースページ](https://releases.aspose.com/).

### Q5: Aspose.PSD for .NET のサポートを受けるにはどうすればよいですか?

 A5: 訪問[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)支援を求め、コミュニティとつながる。