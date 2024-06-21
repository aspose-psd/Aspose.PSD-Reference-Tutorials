---
title: Aspose.PSD for .NET での画像の特定の角度の回転
linktitle: 画像を特定の角度で回転する
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET の威力を探ってください。特定の角度で画像を簡単に回転できます。ライブラリをダウンロードして、シームレスに画像の操作を始めてください。
type: docs
weight: 16
url: /ja/net/image-manipulation/rotate-image-specific-angle/
---
.NET を使用した画像操作の世界を詳しく調べている場合は、Aspose.PSD が強力なソリューションを提供します。このチュートリアルでは、Aspose.PSD を使用して画像を特定の角度で回転するプロセスを説明します。手順に入る前に、概要を説明して準備を整えましょう。

## 導入

Aspose.PSD for .NET は、開発者が PSD およびラスター イメージ形式をシームレスに操作できるようにする多用途ライブラリです。その重要な機能の 1 つは、画像を正確な角度で回転できることで、画像操作に柔軟性をもたらします。このチュートリアルでは、Aspose.PSD for .NET を使用して画像を特定の角度で回転する手順を説明します。

## 前提条件

この作業を開始する前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for .NET ライブラリ: からライブラリをダウンロードしてインストールします。[ダウンロードページ](https://releases.aspose.com/psd/net/).
- ドキュメント ディレクトリ: ソース ファイルと出力ファイルを保存するディレクトリを設定します。

## 名前空間のインポート

まず、必要な名前空間を .NET プロジェクトにインポートします。

```csharp
using Aspose.PSD.ImageOptions;
```

次に、この例をステップバイステップのガイド形式で複数のステップに分けてみましょう。

## ステップ 1: ドキュメント ディレクトリを設定する

```csharp
string dataDir = "Your Document Directory";
```

交換する`"Your Document Directory"`ソースファイルと出力ファイルを保存するディレクトリへのパスを置き換えます。

## ステップ 2: 画像をロードする

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    //追加の手順がここに挿入されます
}
```

回転したい画像をインスタンスにロードします。`RasterImage`.

## ステップ 3: 画像データをキャッシュする

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

回転時のパフォーマンスを向上させるために、画像データをキャッシュします。

## ステップ 4: 画像を回転する

```csharp
image.Rotate(20f, true, Color.Red);
```

比例したサイズを維持し、赤い背景を使用して、画像を 20 度回転します。

## ステップ 5: 結果を保存する

```csharp
image.Save(destName, new JpegOptions());
```

指定したオプションを使用して回転した画像を保存します (この場合は JPEG として)。

## 結論

おめでとう！ Aspose.PSD for .NET を使用して、画像を特定の角度で回転させることができました。このライブラリは、画像操作のための強力なツール セットを提供します。このチュートリアルは氷山の一角にすぎません。を探索してください[ドキュメンテーション](https://reference.aspose.com/psd/net/)さらに多くの機能とオプションについては、

## よくある質問

### Q1: 画像を 20 度以外の角度で回転できますか?

 A1: はい、角度パラメータはカスタマイズできます。`image.Rotate`メソッドを任意の値に変更します。

### Q2: Aspose.PSD は JPEG 以外の画像形式をサポートしていますか?

A2: もちろんです！ Aspose.PSD は、PNG、GIF、BMP、TIFF などの幅広い形式をサポートしています。

### Q3: 回転前に画像データのキャッシュは必要ですか?

A3: 必須ではありませんが、データをキャッシュすると、特に大きな画像の場合、パフォーマンスが大幅に向上します。

### Q4: Aspose.PSD 関連のクエリのサポートはどこで受けられますか?

 A4: にアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートとディスカッションのために。

### Q5: 購入する前に Aspose.PSD を試してみることはできますか?

 A5：確かに！あなたのものをつかんでください[無料トライアル](https://releases.aspose.com/)ライブラリの機能を探索します。