---
title: Aspose.PSD for Java で画像のコントラストを調整する
linktitle: 画像のコントラストを調整する
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用して、Java での画像コントラスト調整の世界を探索します。シームレスな画像操作については、ステップバイステップのガイドに従ってください。
type: docs
weight: 22
url: /ja/java/advanced-techniques/adjust-contrast/
---
## 導入

Java による画像処理の分野では、Aspose.PSD は強力なツールとして際立っています。その数多くの機能の中でも、画像のコントラストを調整することは一般的な要件です。このチュートリアルでは、Aspose.PSD for Java を使用して画像のコントラストを調整するプロセスについて説明します。熟練した開発者でも、初心者でも、このガイドは画像操作のこの重要な側面を習得するのに役立ちます。

## 前提条件

チュートリアルに進む前に、次の前提条件が満たされていることを確認してください。

- Java プログラミングの基本的な理解。
-  Aspose.PSD for Javaライブラリがインストールされています。ダウンロードできます[ここ](https://releases.aspose.com/psd/java/).

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートする必要があります。コードに次の行を追加します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## ステップ1: 画像を読み込む

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//既存の画像をRasterImageクラスのインスタンスに読み込みます
Image image = Image.load(sourceFile);
```

このステップでは、サンプル画像（「sample.psd」）を`Image.load`方法。

## ステップ2: RasterImageにキャストしてデータをキャッシュする

```java
// Image のオブジェクトを RasterImage にキャストする
RasterImage rasterImage = (RasterImage)image;

//RasterImage がキャッシュされているかどうかを確認し、パフォーマンスを向上させるために RasterImage をキャッシュします。
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

ここでは、ジェネリック`Image`異議を唱える`RasterImage`特定の処理用。画像データをキャッシュするとパフォーマンスが向上します。

## ステップ3: コントラストを調整する

```java
//コントラストを調整する
rasterImage.adjustContrast(50);
```

の`adjustContrast`この方法は、画像のコントラストを変更するために使用されます。この例では、コントラストが 50% 増加します。

## ステップ4: TiffOptionsを作成して保存する

```java
//結果画像のTiffOptionsインスタンスを作成する
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

//結果の画像をTIFF形式で保存します
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

ここでは、`TiffOptions`出力イメージの形式やその他のプロパティを指定します。最終的なイメージは TIFF ファイルに保存されます。

## 結論

おめでとうございます! Aspose.PSD for Java を使用して画像のコントラストを正常に調整できました。このチュートリアルでは、パッケージのインポートから処理済みの画像の保存までの重要な手順について説明しました。

## よくある質問

### Q1: Aspose.PSD はさまざまな画像形式と互換性がありますか?

A1: はい、Aspose.PSD はさまざまな画像形式をサポートしており、プロジェクトに柔軟性をもたらします。

### Q2: Aspose.PSD の一時ライセンスを取得するにはどうすればよいですか?

 A2: 臨時免許証を取得できます[ここ](https://purchase.aspose.com/temporary-license/).

### Q3: Aspose.PSD のドキュメントはどこにありますか?

A3: ドキュメントは入手可能です[ここ](https://reference.aspose.com/psd/java/).

### Q4: Aspose.PSD にはどのようなサポート オプションがありますか?

 A4: サポートについては、[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34).

### Q5: Aspose.PSD を購入できますか?

 A5: はい、Aspose.PSDを購入できます。[ここ](https://purchase.aspose.com/buy).