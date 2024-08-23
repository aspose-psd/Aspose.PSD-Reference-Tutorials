---
title: Aspose.PSD for .NET でパターン付きのストローク レイヤーを追加する
linktitle: パターン付きストロークレイヤーの追加
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用して、ストローク レイヤーとパターンで PSD ファイルを強化します。シームレスな統合については、ステップ バイ ステップ ガイドに従ってください。
type: docs
weight: 13
url: /ja/net/layer-effects/adding-stroke-layer-pattern/
---
## 導入

PSD (Photoshop ドキュメント) ファイルをストローク レイヤーとパターンで強化すると、デザインにダイナミックなタッチを加えることができます。このチュートリアルでは、Aspose.PSD for .NET を活用して、PSD ファイルにパターン付きのストローク レイヤーを簡単に追加する方法を説明します。Aspose.PSD は、PSD ファイルの操作を包括的にサポートする強力な .NET ライブラリであり、開発者やデザイナーにとって非常に役立つツールです。

## 前提条件

チュートリアルに進む前に、次の前提条件が満たされていることを確認してください。

- C# プログラミング言語に関する基本的な知識。
- マシンに Visual Studio がインストールされています。
- ダウンロード可能なAspose.PSD for .NETライブラリ[ここ](https://releases.aspose.com/psd/net/).

## 名前空間のインポート

C# コードに必要な名前空間をインポートしていることを確認します。

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

## ステップ1: 環境を設定する

まず、C# コードでソース ディレクトリと出力ディレクトリを定義します。

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";
```

## ステップ2: PSDファイルを読み込む

Aspose.PSD の PsdImage クラスを使用して PSD ファイルを読み込みます。

```csharp
var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

string sourceFileName = Path.Combine(SourceDir, "Stroke.psd");
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // PSDファイルを処理するためのコードをここに記述します
}
```

## ステップ3: 新しいパターンデータを準備する

新しいパターンとその境界を定義します。

```csharp
var newPattern = new int[]
{
    //パターンの色はここに入力してください
};

var newPatternBounds = new Rectangle(0, 0, 4, 4);
var guid = Guid.NewGuid();
```

## ステップ4: ストロークレイヤーを変更する

ストローク レイヤーにアクセスし、そのプロパティを更新します。

```csharp
var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

//ストロークのプロパティを確認して更新する
//...

//不透明度とブレンドモードを更新する
patternStroke.Opacity = 127;
patternStroke.BlendMode = BlendMode.Color;
```

## ステップ5: パターン情報を更新する

PSD ファイル内のパターン情報を更新します。

```csharp
foreach (var globalLayerResource in im.GlobalLayerResources)
{
    if (globalLayerResource is PattResource)
    {
        //パターン情報を更新するためのコードをここに入力します
    }
}

//変更したPSDファイルを保存する
im.Save(exportPath);
```

## ステップ6: 変更を確認する

変更された PSD ファイルをロードし、変更を確認します。

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

    //変更を確認するためのコードをここに入力します
}
```

## 結論

おめでとうございます! Aspose.PSD for .NET でパターン付きのストローク レイヤーを追加する方法を学習しました。この多目的ライブラリにより、開発者は視覚的に魅力的なデザインを作成し、PSD ファイルの柔軟性を高めることができます。

## よくある質問

### Q1: Aspose.PSD for .NET はどのバージョンの Visual Studio でも使用できますか?

A1: はい、Aspose.PSD for .NET はさまざまなバージョンの Visual Studio と互換性があります。

### Q2: Aspose.PSD の一時ライセンスを取得するにはどうすればよいですか?

 A2: 訪問[ここ](https://purchase.aspose.com/temporary-license/)臨時免許を取得する。

### Q3: テストに使用できるサンプル PSD ファイルはありますか?

 A3: サンプルPSDファイルはドキュメントに記載されています。[ここ](https://reference.aspose.com/psd/net/).

### Q4: Aspose.PSD は PSD ファイルのバッチ処理に適していますか?

A4: もちろんです。Aspose.PSD for .NET はバッチ処理を強力にサポートします。

### Q5: サポートを求めたり、コミュニティのディスカッションに参加したりするにはどこに行けばよいですか?

 A5: 訪問[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)サポートとコミュニティの交流のため。