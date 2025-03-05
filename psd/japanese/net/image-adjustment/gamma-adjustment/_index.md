---
title: Aspose.PSD for .NET でガンマ調整を実装する
linktitle: ガンマ調整の実装
second_title: Aspose.PSD .NET API
description: ガンマ調整の実装に関するステップバイステップ ガイドを使用して、Aspose.PSD for .NET のパワーを体験してください。画像の明るさとコントラストを簡単に微調整できます。
type: docs
weight: 12
url: /ja/net/image-adjustment/gamma-adjustment/
---
## 導入

Aspose.PSD for .NET でガンマ調整を実装するための包括的なガイドへようこそ。ガンマ調整は、画像の明るさとコントラストを微調整できる重要な画像処理技術です。このチュートリアルでは、強力な .NET 用の Aspose.PSD ライブラリを使用して、そのプロセスを順を追って説明します。

## 前提条件

実装に進む前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for .NETライブラリ: Aspose.PSDライブラリがインストールされていることを確認してください。ダウンロードできます。[ここ](https://releases.aspose.com/psd/net/).

- .NET Framework: このチュートリアルでは、.NET 開発の基本を理解しており、.NET Framework がインストールされていることを前提としています。

- 統合開発環境 (IDE): Visual Studio など、.NET 開発に適した IDE を選択します。

## 名前空間のインポート

.NET プロジェクトでは、まず Aspose.PSD を操作するために必要な名前空間をインポートします。

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## ステップ1: プロジェクトを設定する

選択した IDE で新しい .NET プロジェクトを作成します。Aspose.PSD ライブラリへの参照を必ず追加してください。

## ステップ2: ドキュメントディレクトリを定義する

```csharp
string dataDir = "Your Document Directory";
```

## ステップ3: 画像を読み込む

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    //この using ブロック内で追加の手順が実行されます。
}
```

## ステップ4: RasterImageにキャストしてデータをキャッシュする

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## ステップ5: ガンマを調整する

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## ステップ6: TiffOptionsを作成して保存する

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## 結論

おめでとうございます。Aspose.PSD for .NET を使用してガンマ調整を正常に実装できました。この強力なライブラリは、画像処理のための堅牢な機能を提供するため、.NET 開発者にとって貴重なツールとなります。

## よくある質問

### Q1: Aspose.PSD のドキュメントはどこにありますか?

 A1: ドキュメントを参照してください[ここ](https://reference.aspose.com/psd/net/).

### Q2: Aspose.PSD for .NET をダウンロードするにはどうすればよいですか?

 A2: ライブラリをダウンロードできます[ここ](https://releases.aspose.com/psd/net/).

### Q3: 無料トライアルはありますか？

 A3: はい、無料トライアルをご利用いただけます[ここ](https://releases.aspose.com/).

### Q4: Aspose.PSD のサポートはどこで受けられますか?

 A4: サポートフォーラムをご覧ください[ここ](https://forum.aspose.com/c/psd/34).

### Q5: 一時ライセンスは必要ですか?

 A5: 必要に応じて臨時免許を取得できます[ここ](https://purchase.aspose.com/temporary-license/).