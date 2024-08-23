---
title: Aspose.PSD for Java で画像のガンマを調整する
linktitle: 画像のガンマを調整する
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して、画像のガンマを簡単に調整する方法を学びます。最適な結果を得るには、ステップバイステップのガイドに従ってください。
type: docs
weight: 23
url: /ja/java/advanced-techniques/adjust-gamma/
---
## 導入

画像処理の分野では、画像のガンマを調整することは、その見た目の魅力を高めるための重要なステップです。Aspose.PSD for Java は、Java 開発者が画像のガンマを簡単に操作できる強力なソリューションを提供します。このチュートリアルでは、Aspose.PSD を使用してガンマを調整する方法を、各ステップを詳しく説明して、シームレスな実装を実現します。

## 前提条件

チュートリアルに進む前に、次の前提条件が設定されていることを確認してください。

1. Java 開発環境: システムに Java 開発環境がインストールされていることを確認します。
2.  Aspose.PSDライブラリ: Aspose.PSDライブラリをダウンロードしてJavaプロジェクトに統合します。必要なリソースは以下にあります。[ドキュメント](https://reference.aspose.com/psd/java/).
3. サンプル画像: ガンマ調整を適用するために使用するサンプル PSD 画像を準備します。

## パッケージのインポート

プロセスを開始するには、Java プロジェクトに必要なパッケージをインポートします。これにより、Aspose.PSD 機能をシームレスに利用するための準備が整います。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## ステップ1: 画像を読み込む

まず、サンプルPSD画像を`RasterImage`クラス。これが後続のガンマ調整の基礎となります。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//既存の画像をRasterImageクラスのインスタンスに読み込みます
Image image = Image.load(sourceFile);

// Image のオブジェクトを RasterImage にキャストする
RasterImage rasterImage = (RasterImage)image;

//パフォーマンス向上のため、RasterImage がキャッシュされているかどうかを確認します。
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## ステップ2: ガンマを調整する

次に、読み込んだ画像のガンマを調整します。`adjustGamma`方法。要件に応じてガンマ値を微調整します。

```java
//ガンマを調整する
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## ステップ3: TiffOptionsを作成する

インスタンスを作成する`TiffOptions`結果の画像に対して、サンプルあたりのビット数や測光オプションなどのさまざまなプロパティを設定して、出力を仕様に合わせて調整します。

```java
//結果画像のTiffOptionsインスタンスを作成する
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## ステップ4: 結果画像を保存する

以前に定義したTIFF形式で操作した画像を保存します。`TiffOptions`.

```java
//結果の画像をTIFF形式で保存します
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## 結論

おめでとうございます! Aspose.PSD for Java を使用して画像のガンマを正常に調整できました。このプロセスにより、開発者は画像の品質を簡単に向上させることができ、視覚的に魅力的なユーザー エクスペリエンスに貢献できます。

## よくある質問

### Q1: Aspose.PSD のドキュメントはどこにありますか?

 A1: ドキュメントは次の場所からアクセスできます。[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: Aspose.PSD for Java をダウンロードするにはどうすればいいですか?

 A2: ライブラリをダウンロードするには[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: Aspose.PSD はどこで購入できますか?

 A3: 訪問[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) Aspose.PSD を購入します。

### Q4: 無料トライアルはありますか?

 A4: はい、無料トライアルをお試しください。[詳細はこちら](https://releases.aspose.com/).

### Q5: Aspose.PSD のサポートはどこで受けられますか?

 A5: サポートについては、Aspose.PSDフォーラムをご覧ください。[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).