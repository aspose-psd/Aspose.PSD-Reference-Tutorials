---
title: Aspose.PSD for .NET にソリッドカラーのストロークレイヤーを追加する
linktitle: ソリッドカラーのストロークレイヤーを追加する
second_title: Aspose.PSD .NET API
description: Aspose.PSD を使用して .NET 画像操作スキルを強化します。単色のストロークレイヤーを段階的に追加する方法を学びましょう。
type: docs
weight: 11
url: /ja/net/layer-effects/adding-stroke-layer-solid-color/
---
## 導入

.NET 開発の分野では、視覚的に魅力的な画像を作成することが一般的な要件です。 Aspose.PSD for .NET は、画像をシームレスに操作および強化するための強力なツール セットを提供します。重要な機能の 1 つは、画像に鮮やかさと深みをもたらす単色のストローク レイヤーを追加することです。このチュートリアルでは、Aspose.PSD for .NET を使用してプロセスを段階的に説明します。

## 前提条件

チュートリアルに入る前に、次の前提条件を満たしていることを確認してください。

- .NET 開発の基本的な知識。
- Visual Studio がマシンにインストールされていること。
- .NET ライブラリ用の Aspose.PSD。からダウンロードできます。[Webサイト](https://releases.aspose.com/psd/net/).

## 名前空間のインポート

まず、Aspose.PSD for .NET の機能を利用するために必要な名前空間をインポートします。

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## ステップ 1: PSD ファイルをロードする

まず、ストローク レイヤーで強化したい PSD ファイルをロードします。ファイル パスが正しいことを確認してください。

```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "Stroke.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    //さらなるステップのコードがここに追加されます
}
```

## ステップ 2: ストローク エフェクトのプロパティにアクセスする

PSD ファイルからストローク エフェクトのプロパティを取得します。

```csharp
var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

if ((colorStroke.BlendMode != BlendMode.Normal) ||
    (colorStroke.Opacity != 255) ||
    (colorStroke.IsVisible != true))
{
    throw new Exception("Color stroke effect was read wrong");
}
```

## ステップ 3: ストローク設定を調整する

好みに応じてストローク設定を変更します。この例では、色を黄色に変更し、不透明度を 127 に設定し、カラー ブレンド モードを使用します。

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

## ステップ 4: 編集した画像を保存する

ストロークレイヤーの変更を適用した後、画像を保存します。

```csharp
string exportPath = dataDir + "StrokeGradientChanged.psd";
im.Save(exportPath);
```

## ステップ 5: 変更を確認する

編集したイメージをロードして検査することで、変更が正しく適用されていることを確認します。

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    //変更を確認するコードがここに追加されます
}
```

これらの手順を繰り返してさらに調整するか、さまざまなストローク効果を試して、目的の視覚的効果を実現します。

## 結論

おめでとう！ Aspose.PSD for .NET を使用して、単色のストローク レイヤーを追加する方法を学習しました。この強力な機能により、.NET 環境で画像を強化する可能性が広がります。

## よくある質問

### Q1: Aspose.PSD for .NET は、最新の .NET Framework バージョンと互換性がありますか?

A1: はい。Aspose.PSD for .NET は、最新の .NET Framework バージョンとの互換性を確保するために定期的に更新されます。

### Q2: Aspose.PSD for .NET を商用プロジェクトに使用できますか?

A2：もちろんです！ Aspose.PSD for .NET は商用製品であり、ライセンスを購入することでプロジェクトで使用できます。

### Q3: Aspose.PSD for .NET のその他の例やドキュメントはどこで入手できますか?

 A3: を探索してください。[ドキュメンテーション](https://reference.aspose.com/psd/net/)包括的な例とガイダンスについては、こちらをご覧ください。

### Q4: Aspose.PSD for .NET の無料トライアルはありますか?

 A4: はい、次のサイトから無料トライアルを利用できます。[リリースページ](https://releases.aspose.com/).

### Q5: Aspose.PSD for .NET のサポートを受けるにはどうすればよいですか?

 A5: にアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)支援を求め、コミュニティとつながるために。