---
title: Aspose.PSD for Java を使用して画像の明るさを調整する
linktitle: 画像の明るさを調整する
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用して Java で画像の明るさを強化します。画像の明るさをプログラムで調整するためのステップバイステップのガイド。
type: docs
weight: 21
url: /ja/java/advanced-techniques/adjust-brightness/
---
## 導入

画像を強化することは、グラフィック デザインやデジタル写真では一般的な要件です。 Aspose.PSD for Java は、画像の明るさをプログラムで調整するための強力なソリューションを提供します。このチュートリアルでは、Aspose.PSD for Java ライブラリを利用して画像の明るさを調整する方法を段階的に説明します。

## 前提条件

チュートリアルに進む前に、次の前提条件を満たしていることを確認してください。

-  Aspose.PSD for Java ライブラリ: からライブラリをダウンロードしてインストールします。[Java 用 Aspose.PSD ドキュメント](https://reference.aspose.com/psd/java/).

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。この例では、次のものを使用します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

ここで、画像の明るさを調整するプロセスを簡単な手順に分けてみましょう。

## ステップ 1: 画像をロードする

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

//既存の画像を RasterImage クラスのインスタンスにロードします
Image image = Image.load(sourceFile);
// Image のオブジェクトを RasterImage にキャストします
RasterImage rasterImage = (RasterImage) image;

//RasterImage がキャッシュされているかどうかを確認し、パフォーマンスを向上させるために RasterImage をキャッシュします
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

このステップでは、ターゲット画像をロードし、それを`RasterImage`さらなる処理のために。

## ステップ 2: 明るさを調整する

```java
//明るさを調整する
rasterImage.adjustBrightness(-50);
```

ここで使用するのは、`adjustBrightness`画像の明るさを変更する方法です。この例では、明るさを 50 単位減少させますが、要件に基づいてこの値をカスタマイズできます。

## ステップ 3: TiffOptions を設定する

```java
int[] ushort = {8, 8, 8};
//結果のイメージの TiffOptions のインスタンスを作成します。
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

を設定します。`TiffOptions`調整した画像を保存します。を調整します。`bitsPerSample`そして`photometric`特定のニーズに基づいたプロパティ。

## ステップ 4: 結果のイメージを保存する

```java
//結果の画像を保存します
rasterImage.save(destName, tiffOptions);
```

最後に、指定したファイルを使用して変更した画像を保存します。`TiffOptions`.

## 結論

Aspose.PSD for Java を使用すると、プログラムによる画像の明るさの調整が簡単になります。このチュートリアルでは、Java アプリケーションにこの機能を実装するための包括的なガイドを提供しました。

## よくある質問

### Q1: PSD 以外の画像フォーマットでも明るさを調整できますか?

A1: はい、Aspose.PSD for Java は、JPEG、PNG、TIFF などのさまざまな画像形式をサポートしています。

### Q2: 画像調整プロセス中にエラーが発生した場合はどうすればよいですか?

A2: try-catch ブロックを使用してエラー処理を実装し、発生する可能性のある例外を管理できます。

### Q3: 明るさの調整範囲に制限はありますか?

A3: 画像の内容や形式によって調整範囲は異なりますが、Aspose.PSD では柔軟にカスタマイズできます。

### Q4: Aspose.PSD for Java を商用プロジェクトで使用できますか?

 A4: はい、Aspose.PSD for Java は商用ライブラリであり、次からライセンスを取得できます。[ここ](https://purchase.aspose.com/buy).

### Q5: Aspose.PSD for Java の無料トライアルはありますか?

 A5: はい、無料トライアルでライブラリを探索できます。[ここ](https://releases.aspose.com/).