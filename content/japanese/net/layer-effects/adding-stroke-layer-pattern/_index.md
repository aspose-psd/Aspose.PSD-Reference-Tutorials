---
title: Aspose.PSD for .NET にパターンを含むストローク レイヤーを追加する
linktitle: パターン付きストロークレイヤーを追加する
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用して、ストローク レイヤーとパターンで PSD ファイルを強化します。シームレスな統合については、ステップバイステップのガイドに従ってください。
type: docs
weight: 13
url: /ja/net/layer-effects/adding-stroke-layer-pattern/
---
## 導入

ストローク レイヤーとパターンを使用して PSD (Photoshop ドキュメント) ファイルを強化すると、デザインにダイナミックなタッチを加えることができます。このチュートリアルでは、Aspose.PSD for .NET を活用して、パターンを持つストローク レイヤーを PSD ファイルに簡単に追加する方法を説明します。 Aspose.PSD は、PSD ファイルの操作を包括的にサポートする強力な .NET ライブラリであり、開発者とデザイナーにとって同様に貴重なツールです。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

- C# プログラミング言語の基本的な知識。
- Visual Studio がマシンにインストールされていること。
- ダウンロードできる .NET ライブラリ用の Aspose.PSD[ここ](https://releases.aspose.com/psd/net/).

## 名前空間のインポート

必要な名前空間を C# コードにインポートしていることを確認してください。

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## ステップ 1: 環境をセットアップする

まず、C# コードでソース ディレクトリと出力ディレクトリを定義します。

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";
```

## ステップ 2: PSD ファイルをロードする

Aspose.PSD の PsdImage クラスを使用して PSD ファイルを読み込みます。

```csharp
var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

string sourceFileName = Path.Combine(SourceDir, "Stroke.psd");
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // PSD ファイルを処理するためのコードはここにあります
}
```

## ステップ 3: 新しいパターン データを準備する

新しいパターンとその境界を定義します。

```csharp
var newPattern = new int[]
{
    //パターンの色はここにあります
};

var newPatternBounds = new Rectangle(0, 0, 4, 4);
var guid = Guid.NewGuid();
```

## ステップ 4: ストロークレイヤーを変更する

ストローク レイヤーにアクセスし、そのプロパティを更新します。

```csharp
var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

//ストロークのプロパティを確認および更新する
//...

//不透明度とブレンドモードを更新します
patternStroke.Opacity = 127;
patternStroke.BlendMode = BlendMode.Color;
```

## ステップ 5: パターン情報を更新する

PSD ファイル内のパターン情報を更新します。

```csharp
foreach (var globalLayerResource in im.GlobalLayerResources)
{
    if (globalLayerResource is PattResource)
    {
        //パターン情報を更新するためのコードはここにあります
    }
}

//変更したPSDファイルを保存します
im.Save(exportPath);
```

## ステップ 6: 変更を確認する

変更した PSD ファイルをロードし、変更を確認します。

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

    //変更を確認するためのコードはここにあります
}
```

## 結論

おめでとう！ Aspose.PSD for .NET でパターンを含むストローク レイヤーを追加する方法を学習しました。この多用途ライブラリにより、開発者は視覚的に魅力的なデザインを作成し、PSD ファイルの柔軟性を高めることができます。

## よくある質問

### Q1: Aspose.PSD for .NET は Visual Studio のどのバージョンでも使用できますか?

A1: はい、Aspose.PSD for .NET は Visual Studio のさまざまなバージョンと互換性があります。

### Q2: Aspose.PSD の一時ライセンスを取得するにはどうすればよいですか?

 A2: 訪問[ここ](https://purchase.aspose.com/temporary-license/)仮免許を取得するためです。

### Q3: テストに利用できるサンプル PSD ファイルはありますか?

 A3: サンプル PSD ファイルはドキュメントにあります。[ここ](https://reference.aspose.com/psd/net/).

### Q4: Aspose.PSD は PSD ファイルのバッチ処理に適していますか?

A4: もちろん、Aspose.PSD for .NET はバッチ処理の強力なサポートを提供します。

### Q5: どこに支援を求めたり、コミュニティのディスカッションに参加したりできますか?

 A5: にアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)サポートとコミュニティの交流のために。