---
title: Aspose.PSD for .NET で画像を特定の角度に回転する
linktitle: 特定の角度で画像を回転する
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET のパワーを体験してください。特定の角度で画像を簡単に回転できます。ライブラリをダウンロードして、シームレスな画像操作を開始してください。
type: docs
weight: 16
url: /ja/net/image-manipulation/rotate-image-specific-angle/
---
.NET で画像操作の世界に足を踏み入れようとしている場合、Aspose.PSD は強力なソリューションを提供します。このチュートリアルでは、Aspose.PSD を使用して特定の角度で画像を回転するプロセスについて説明します。手順に進む前に、概要を説明して準備を整えましょう。

## 導入

Aspose.PSD for .NET は、開発者が PSD およびラスター画像形式をシームレスに操作できるようにする多機能ライブラリです。その主な機能の 1 つは、画像を正確な角度で回転できることで、これにより画像操作の柔軟性が向上します。このチュートリアルでは、Aspose.PSD for .NET を使用して特定の角度で画像を回転する手順について説明します。

## 前提条件

この旅を始める前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for .NETライブラリ: ライブラリを以下のサイトからダウンロードしてインストールします。[ダウンロードページ](https://releases.aspose.com/psd/net/).
- ドキュメント ディレクトリ: ソース ファイルと出力ファイルを保存するディレクトリを設定します。

## 名前空間のインポート

まず、.NET プロジェクトに必要な名前空間をインポートします。

```csharp
using Aspose.PSD.ImageOptions;
```

ここで、ステップバイステップのガイド形式で例を複数のステップに分解してみましょう。

## ステップ1: ドキュメントディレクトリを設定する

```csharp
string dataDir = "Your Document Directory";
```

交換する`"Your Document Directory"`ソースファイルと出力ファイルを保存するディレクトリへのパスを指定します。

## ステップ2: 画像を読み込む

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    //追加の手順はここに挿入されます
}
```

回転したい画像をインスタンスに読み込みます`RasterImage`.

## ステップ3: 画像データをキャッシュする

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

回転時のパフォーマンスを向上させるために画像データをキャッシュします。

## ステップ4: 画像を回転する

```csharp
image.Rotate(20f, true, Color.Red);
```

比例サイズを維持し、赤い背景を使用して、画像を 20 度回転します。

## ステップ5: 結果を保存する

```csharp
image.Save(destName, new JpegOptions());
```

回転した画像を指定されたオプションで保存します (この場合は JPEG として)。

## 結論

おめでとうございます！Aspose.PSD for .NETを使用して、特定の角度で画像を回転させることができました。このライブラリは画像操作のための強力なツールセットを提供しており、このチュートリアルはほんの一部にすぎません。[ドキュメント](https://reference.aspose.com/psd/net/)その他の機能とオプションについてはこちらをご覧ください。

## よくある質問

### Q1: 画像を20度以外の角度で回転できますか？

 A1: はい、角度パラメータをカスタマイズできます。`image.Rotate`メソッドを任意の値に設定します。

### Q2: Aspose.PSD は JPEG 以外の画像形式もサポートしていますか?

A2: もちろんです! Aspose.PSD は、PNG、GIF、BMP、TIFF など、幅広い形式をサポートしています。

### Q3: 回転前に画像データをキャッシュする必要はありますか?

A3: 必須ではありませんが、データをキャッシュすると、特に大きな画像の場合、パフォーマンスが大幅に向上します。

### Q4: Aspose.PSD 関連のクエリのサポートはどこで受けられますか?

 A4: 訪問[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートとディスカッションのため。

### Q5: 購入前に Aspose.PSD を試すことはできますか?

 A5: もちろんです！[無料トライアル](https://releases.aspose.com/)ライブラリの機能を調べます。