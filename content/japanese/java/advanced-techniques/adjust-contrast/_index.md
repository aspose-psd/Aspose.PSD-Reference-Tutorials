---
title: Aspose.PSD for Java を使用して画像のコントラストを調整する
linktitle: 画像のコントラストを調整する
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用して、Java での画像コントラスト調整の世界を探索してください。シームレスな画像操作については、ステップバイステップのガイドに従ってください。
type: docs
weight: 22
url: /ja/java/advanced-techniques/adjust-contrast/
---
## 導入

Java を使用した画像処理の分野では、Aspose.PSD は強力なツールとして際立っています。その無数の機能の中で、画像のコントラストの調整は一般的な要件です。このチュートリアルでは、Aspose.PSD for Java を使用して画像のコントラストを調整するプロセスを説明します。経験豊富な開発者でも、初心者でも、このガイドは画像操作のこの重要な側面を習得するのに役立ちます。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

- Java プログラミングの基本的な理解。
-  Java ライブラリ用の Aspose.PSD がインストールされています。ダウンロードできます[ここ](https://releases.aspose.com/psd/java/).

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートする必要があります。コードに次の行を追加します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## ステップ 1: 画像をロードする

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//既存の画像を RasterImage クラスのインスタンスにロードします
Image image = Image.load(sourceFile);
```

このステップでは、`Image.load`方法。

## ステップ 2: RasterImage にキャストしてデータをキャッシュする

```java
// Image のオブジェクトを RasterImage にキャストします
RasterImage rasterImage = (RasterImage)image;

//RasterImage がキャッシュされているかどうかを確認し、パフォーマンスを向上させるために RasterImage をキャッシュします
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

ここでは、ジェネリックをキャストします`Image`に反対する`RasterImage`特定の処理のために。画像データをキャッシュするとパフォーマンスが向上します。

## ステップ 3: コントラストを調整する

```java
//コントラストを調整する
rasterImage.adjustContrast(50);
```

の`adjustContrast`画像のコントラストを変更するために使用されるメソッドです。この例では、コントラストが 50% 増加します。

## ステップ 4: TiffOptions を作成して保存する

```java
//結果のイメージの TiffOptions のインスタンスを作成します。
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

//結果の画像を TIFF 形式で保存します
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

ここで設定するのは、`TiffOptions`出力イメージの形式とその他のプロパティを指定します。最終的な画像は TIFF ファイルに保存されます。

## 結論

おめでとう！ Aspose.PSD for Java を使用して画像のコントラストを正常に調整しました。このチュートリアルでは、パッケージのインポートから処理されたイメージの保存までの重要な手順を説明しました。

## よくある質問

### Q1: Aspose.PSD はさまざまな画像形式と互換性がありますか?

A1: はい、Aspose.PSD はさまざまな画像形式をサポートしており、プロジェクトに柔軟性をもたらします。

### Q2: Aspose.PSD の一時ライセンスを取得するにはどうすればよいですか?

 A2: 仮免許は取得できます。[ここ](https://purchase.aspose.com/temporary-license/).

### Q3: Aspose.PSD ドキュメントはどこで見つけられますか?

A3: ドキュメントは入手可能です[ここ](https://reference.aspose.com/psd/java/).

### Q4: Aspose.PSD ではどのようなサポート オプションが利用できますか?

 A4: サポートについては、次のサイトにアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34).

### Q5: Aspose.PSD を購入できますか?

 A5: はい、Aspose.PSD を購入できます。[ここ](https://purchase.aspose.com/buy).