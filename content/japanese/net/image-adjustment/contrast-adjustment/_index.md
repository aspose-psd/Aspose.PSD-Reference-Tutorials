---
title: Aspose.PSD for .NET でのコントラスト調整の実装
linktitle: コントラスト調整を実施する
second_title: Aspose.PSD .NET API
description: このステップバイステップ ガイドを使用して、Aspose.PSD for .NET でコントラスト調整を実装する方法を学びます。
type: docs
weight: 11
url: /ja/net/image-adjustment/contrast-adjustment/
---
## 導入

Aspose.PSD for .NET でのコントラスト調整の実装に関するこの包括的なガイドへようこそ。このチュートリアルでは、強力な .NET イメージング ライブラリである Aspose.PSD を使用して画像のコントラストを強化するプロセスについて説明します。このガイドを終えると、画像にコントラスト調整をシームレスに適用する方法をしっかりと理解できるようになります。

## 前提条件

段階的なプロセスに入る前に、次の前提条件が満たされていることを確認してください。

1.  Aspose.PSD for .NET ライブラリ: Aspose.PSD for .NET ライブラリをダウンロードしてインストールします。ダウンロードリンクが見つかります[ここ](https://releases.aspose.com/psd/net/).

2. ドキュメント ディレクトリ: ソース ファイルと宛先ファイルが保存されるディレクトリを設定します。提供されたコード内の「Your Document Directory」をこのディレクトリへのパスに置き換えます。

前提条件が整ったので、実装に進みましょう。

## 名前空間のインポート

このステップでは、Aspose.PSD ライブラリが提供する機能にアクセスするために必要な名前空間をインポートします。

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## ステップ 1: 画像をロードする

ソースイメージをインスタンスにロードします。`RasterImage`クラス。

```csharp
//ExStart:画像の読み込み
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    RasterImage rasterImage = (RasterImage)image;
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    //次のステップに進みます...
}
//ExEnd:LoadImage
```

## ステップ 2: コントラストを調整する

このステップでは、読み込んだ画像のコントラストを調整します。

```csharp
//ExStart:コントラスト調整
rasterImage.AdjustContrast(50); //コントラストを 50% 調整します
//次のステップに進みます...
//ExEnd:コントラスト調整
```

## ステップ 3: TIFF オプションを作成する

のインスタンスを作成します`TiffOptions`結果の画像に対してさまざまなプロパティを設定し、画像を TIFF 形式で保存します。

```csharp
//ExStart:Tiff オプションの作成
string destName = dataDir + @"AdjustContrast_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
//ExEnd:CreateTiffOptions
```

おめでとう！ Aspose.PSD for .NET を使用してコントラスト調整を正常に実装しました。

## 結論

このチュートリアルでは、Aspose.PSD for .NET を使用して画像のコントラストを強化するプロセスを検討しました。このライブラリは、画像プロパティを操作する簡単な方法を提供し、開発者が視覚的に魅力的な画像を簡単に作成できるようにします。

## よくある質問

### Q1: Aspose.PSD for .NET は初心者に適していますか?

A1: Aspose.PSD for .NET は開発者にとって使いやすいように設計されており、初心者と経験豊富な開発者の両方に適しています。

### Q2: Aspose.PSD を商用プロジェクトに使用できますか?

 A2: はい、Aspose.PSD for .NET は商用プロジェクトで使用できます。ライセンスの詳細については、次のサイトを参照してください。[ここ](https://purchase.aspose.com/buy).

### Q3: 無料トライアルはありますか?

 A3: はい、Aspose.PSD for .NET の無料トライアルを試すことができます。[ここ](https://releases.aspose.com/).

### Q4: .NET 用の Aspose.PSD のサポートはどこで見つけられますか?

 A4: Aspose.PSD for .NET サポート フォーラムにアクセスしてください。[ここ](https://forum.aspose.com/c/psd/34)援助のために。

### Q5: 仮免許はどうやって取得できますか?

 A5: 必要に応じて、一時ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/).