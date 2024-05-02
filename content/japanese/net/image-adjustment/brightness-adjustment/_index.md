---
title: Aspose.PSD for .NET での明るさ調整の実装
linktitle: 明るさ調整を実施する
second_title: Aspose.PSD .NET API
description: 画像の明るさを調整する際の Aspose.PSD for .NET の機能を試してください。シームレスな実装については、ステップバイステップのガイドに従ってください。
type: docs
weight: 10
url: /ja/net/image-adjustment/brightness-adjustment/
---
## 導入

画像属性の強化と調整はさまざまなアプリケーションで共通の要件であり、Aspose.PSD for .NET は PSD ファイルをシームレスに操作するための強力なソリューションを提供します。そのような操作の 1 つは明るさの調整で、これを使用すると画像の明るさを簡単に変更できます。

このチュートリアルでは、Aspose.PSD for .NET を使用して明るさ調整を実装するプロセスについて説明します。以下の手順に従って、PSD ファイルに明るさの調整を組み込む方法を包括的に理解してください。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for .NET ライブラリ: Aspose.PSD for .NET ライブラリを次の場所からダウンロードしてインストールします。[ダウンロードリンク](https://releases.aspose.com/psd/net/).

- ドキュメント ディレクトリ: PSD ファイルを保存し、ドキュメントを更新するためのディレクトリを設定します。`dataDir`提供されたコード スニペット内の変数をドキュメント ディレクトリへのパスに置き換えます。

## 名前空間のインポート

.NET プロジェクトに、Aspose.PSD 機能にアクセスするために必要な名前空間を含めます。次の名前空間をコードに追加します。

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

ここで、例を複数のステップに分けてみましょう。

## ステップ 1: PSD ファイルをロードする

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "Your Document Directory";
string sourceFile = dataDir + @"sample.psd";

//Aspose.PSD を使用して PSD ファイルをロードします
using (var image = (PsdImage)Image.Load(sourceFile))
{
    //さらなるステップのコードはここにあります
}
```

## ステップ 2: ラスター画像を取得する

```csharp
//読み込んだPSDファイルからラスター画像を取得します
RasterCachedImage rasterImage = image;
```

## ステップ 3: 明るさを調整する

```csharp
//明るさの値を設定します。許容される明るさの値は [-255, 255] の範囲内です。
rasterImage.AdjustBrightness(-50);
```

## ステップ 4: 変更したイメージを保存する

```csharp
//変更した画像を明るさを調整して保存します
string destName = dataDir + @"AdjustBrightness_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
rasterImage.Save(destName, tiffOptions);
```

例を管理しやすい手順に分割したので、Aspose.PSD を使用して輝度調整を .NET プロジェクトにシームレスに統合できます。

## 結論

Aspose.PSD for .NET は、PSD ファイルに明るさ調整を実装するプロセスを簡素化します。上記のステップバイステップのガイドに従うことで、画像の視覚的な魅力を簡単に高めることができます。望ましい結果を得るには、さまざまな明るさの値を試してください。

## よくある質問

### Q1: Aspose.PSD for .NET のドキュメントはどこで見つけられますか?

 A1: ドキュメントは入手可能です[ここ](https://reference.aspose.com/psd/net/).

### Q2: .NET ライブラリ用の Aspose.PSD をダウンロードするにはどうすればよいですか?

 A2: ライブラリは以下からダウンロードできます。[リリースページ](https://releases.aspose.com/psd/net/).

### Q3: Aspose.PSD for .NET の無料トライアルはありますか?

 A3: はい、無料トライアルにアクセスできます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.PSD for .NET のサポートはどこで入手できますか?

 A4: サポートについては、次のサイトにアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34).

### Q5: Aspose.PSD for .NET の一時ライセンスを取得するにはどうすればよいですか?

 A5: 仮免許を取得できます。[ここ](https://purchase.aspose.com/temporary-license/).