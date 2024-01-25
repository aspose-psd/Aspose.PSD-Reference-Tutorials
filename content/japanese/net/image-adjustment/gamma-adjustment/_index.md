---
title: Aspose.PSD for .NET でのガンマ調整の実装
linktitle: ガンマ調整の実施
second_title: Aspose.PSD .NET API
description: ガンマ調整の実装に関するステップバイステップ ガイドを使用して、Aspose.PSD for .NET の威力を体験してください。画像の明るさとコントラストを簡単に微調整できます。
type: docs
weight: 12
url: /ja/net/image-adjustment/gamma-adjustment/
---
## 導入

Aspose.PSD for .NET でのガンマ調整の実装に関するこの包括的なガイドへようこそ。ガンマ調整は、画像の明るさとコントラストを微調整できる重要な画像処理技術です。このチュートリアルでは、.NET 用の強力な Aspose.PSD ライブラリを使用するプロセスを説明します。

## 前提条件

実装に入る前に、次の前提条件が満たされていることを確認してください。

-  .NET ライブラリ用の Aspose.PSD: .NET 用の Aspose.PSD ライブラリがインストールされていることを確認します。ダウンロードできます[ここ](https://releases.aspose.com/psd/net/).

- .NET Framework: このチュートリアルは、.NET 開発の基本を理解しており、.NET Framework がインストールされていることを前提としています。

- 統合開発環境 (IDE): Visual Studio などの .NET 開発用の優先 IDE を選択します。

## 名前空間のインポート

.NET プロジェクトで、Aspose.PSD を操作するために必要な名前空間をインポートすることから始めます。

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## ステップ 1: プロジェクトをセットアップする

選択した IDE で新しい .NET プロジェクトを作成します。 Aspose.PSD ライブラリへの参照を必ず追加してください。

## ステップ 2: ドキュメント ディレクトリを定義する

```csharp
string dataDir = "Your Document Directory";
```

## ステップ 3: 画像をロードする

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    //追加の手順は、この using ブロック内で実行されます。
}
```

## ステップ 4: RasterImage にキャストしてデータをキャッシュする

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## ステップ 5: ガンマを調整する

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## ステップ 6: TiffOptions を作成して保存する

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## 結論

おめでとう！ Aspose.PSD for .NET を使用してガンマ調整を正常に実装しました。この強力なライブラリは、画像処理のための堅牢な機能を提供し、.NET 開発者にとって貴重なツールになります。

## よくある質問

### Q1: Aspose.PSD ドキュメントはどこで見つけられますか?

 A1: ドキュメントを参照してください。[ここ](https://reference.aspose.com/psd/net/).

### Q2: .NET 用の Aspose.PSD をダウンロードするにはどうすればよいですか?

 A2: ライブラリをダウンロードできます。[ここ](https://releases.aspose.com/psd/net/).

### Q3: 無料トライアルはありますか?

 A3: はい、無料トライアルを利用できます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.PSD のサポートはどこで入手できますか?

 A4: サポート フォーラムにアクセスしてください。[ここ](https://forum.aspose.com/c/psd/34).

### Q5: 仮免許は必要ですか?

 A5: 必要に応じて、一時ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/).