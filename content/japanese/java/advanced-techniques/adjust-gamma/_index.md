---
title: Aspose.PSD for Java を使用して画像のガンマを調整する
linktitle: 画像のガンマを調整する
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して画像のガンマを簡単に調整する方法を学びます。最適な結果を得るには、ステップバイステップのガイドに従ってください。
type: docs
weight: 23
url: /ja/java/advanced-techniques/adjust-gamma/
---
## 導入

画像処理の分野では、画像のガンマ調整は視覚的な魅力を高めるための重要なステップです。 Aspose.PSD for Java は、Java 開発者が画像ガンマを簡単に操作できる強力なソリューションを提供します。このチュートリアルでは、Aspose.PSD を使用してガンマを調整する方法を検討し、シームレスな実装を確実にするために各ステップを詳しく説明します。

## 前提条件

チュートリアルに入る前に、次の前提条件が設定されていることを確認してください。

1. Java 開発環境: システムに Java 開発環境がインストールされていることを確認します。
2.  Aspose.PSD ライブラリ: Aspose.PSD ライブラリをダウンロードして、Java プロジェクトに統合します。必要なリソースは次の場所にあります。[ドキュメンテーション](https://reference.aspose.com/psd/java/).
3. サンプル画像: ガンマ調整を適用するために使用するサンプル PSD 画像を準備します。

## パッケージのインポート

プロセスを開始するには、必要なパッケージを Java プロジェクトにインポートします。これにより、Aspose.PSD 機能をシームレスに利用するための準備が整います。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## ステップ 1: 画像をロードする

まず、サンプル PSD 画像をインスタンスにロードします。`RasterImage`クラス。これは、その後のガンマ調整の基礎となります。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//既存の画像を RasterImage クラスのインスタンスにロードします
Image image = Image.load(sourceFile);

// Image のオブジェクトを RasterImage にキャストします
RasterImage rasterImage = (RasterImage)image;

//パフォーマンスを向上させるために RasterImage がキャッシュされているかどうかを確認してください
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## ステップ 2: ガンマを調整する

ここで、ロードされた画像のガンマを調整します。`adjustGamma`方法。要件に応じてガンマ値を微調整します。

```java
//ガンマを調整する
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## ステップ 3: TiffOptions を作成する

のインスタンスを作成します`TiffOptions`結果の画像について。サンプルあたりのビット数や測光オプションなどのさまざまなプロパティを設定して、出力を仕様に合わせて調整します。

```java
//結果のイメージの TiffOptions のインスタンスを作成します。
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## ステップ 4: 結果のイメージを保存する

前に定義したファイルを使用して、操作した画像を TIFF 形式で保存します。`TiffOptions`.

```java
//結果の画像を TIFF 形式で保存します
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## 結論

おめでとう！ Aspose.PSD for Java を使用して画像のガンマを正常に調整しました。このプロセスにより、開発者は画質を簡単に向上させることができ、視覚的に魅力的なユーザー エクスペリエンスに貢献します。

## よくある質問

### Q1: Aspose.PSD ドキュメントはどこで見つけられますか?

 A1: ドキュメントには次の場所からアクセスできます。[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: Java 用の Aspose.PSD をダウンロードするにはどうすればよいですか?

 A2: からライブラリをダウンロードします。[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: Aspose.PSD はどこで購入できますか?

 A3: 訪問[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) Aspose.PSD を購入するには

### Q4: 無料トライアルはありますか?

A4: はい、次の場所で無料トライアルを試すことができます。[https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: Aspose.PSD のサポートはどこに問い合わせればよいですか?

 A5: サポートが必要な場合は、Aspose.PSD フォーラムにアクセスしてください。[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).