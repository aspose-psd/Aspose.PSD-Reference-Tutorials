---
title: Aspose.PSD for Java で画像の明るさを調整する
linktitle: 画像の明るさを調整する
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用して Java で画像の明るさを強化します。プログラムで画像の明るさを調整するためのステップバイステップ ガイド。
type: docs
weight: 21
url: /ja/java/advanced-techniques/adjust-brightness/
---
## 導入

画像の強調は、グラフィック デザインやデジタル写真では一般的な要件です。Aspose.PSD for Java は、プログラムで画像の明るさを調整するための強力なソリューションを提供します。このチュートリアルでは、Aspose.PSD for Java ライブラリを使用して画像の明るさを調整する方法を段階的に説明します。

## 前提条件

チュートリアルに進む前に、次の前提条件を満たしていることを確認してください。

-  Aspose.PSD for Javaライブラリ:ライブラリを以下のサイトからダウンロードしてインストールします。[Aspose.PSD for Java ドキュメント](https://reference.aspose.com/psd/java/).

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。この例では、次のものを使用します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

ここで、画像の明るさを調整するプロセスを簡単な手順に分解してみましょう。

## ステップ1: 画像を読み込む

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

//既存の画像をRasterImageクラスのインスタンスに読み込みます
Image image = Image.load(sourceFile);
// Image のオブジェクトを RasterImage にキャストする
RasterImage rasterImage = (RasterImage) image;

//RasterImage がキャッシュされているかどうかを確認し、パフォーマンスを向上させるために RasterImage をキャッシュします。
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

このステップでは、ターゲット画像をロードし、`RasterImage`さらに処理するため。

## ステップ2: 明るさを調整する

```java
//明るさを調整する
rasterImage.adjustBrightness(-50);
```

ここでは、`adjustBrightness`画像の明るさを変更する方法。この例では明るさを 50 単位下げていますが、この値は必要に応じてカスタマイズできます。

## ステップ3: TiffOptionsを設定する

```java
int[] ushort = {8, 8, 8};
//結果画像のTiffOptionsインスタンスを作成する
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

設定する`TiffOptions`調整した画像を保存するためのものです。`bitsPerSample`そして`photometric`特定のニーズに基づいたプロパティ。

## ステップ4: 結果画像を保存する

```java
//結果画像を保存する
rasterImage.save(destName, tiffOptions);
```

最後に、指定された方法で変更した画像を保存します。`TiffOptions`.

## 結論

Aspose.PSD for Java を使用すると、プログラムで画像の明るさを簡単に調整できます。このチュートリアルでは、Java アプリケーションでこの機能を実装するための包括的なガイドを提供します。

## よくある質問

### Q1: PSD以外の画像形式でも明るさを調整できますか？

A1: はい、Aspose.PSD for Java は JPEG、PNG、TIFF などのさまざまな画像形式をサポートしています。

### Q2: 画像調整プロセス中にエラーが発生した場合、どのように対処すればよいですか?

A2: 発生する可能性のある例外を管理するために、try-catch ブロックを使用してエラー処理を実装できます。

### Q3: 明るさ調整の範囲に制限はありますか？

A3: 調整範囲は画像の内容と形式によって異なりますが、Aspose.PSD では柔軟にカスタマイズできます。

### Q4: Aspose.PSD for Java を商用プロジェクトで使用できますか?

 A4: はい、Aspose.PSD for Javaは商用ライブラリであり、ライセンスは以下から取得できます。[ここ](https://purchase.aspose.com/buy).

### Q5: Aspose.PSD for Java の無料試用版はありますか?

 A5: はい、無料トライアルでライブラリを探索できます。[ここ](https://releases.aspose.com/).