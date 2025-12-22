---
date: 2025-12-19
description: Aspose.PSD for Java を使用して画像の明るさを調整する方法を学びましょう。この Java 画像操作チュートリアルは、ステップバイステップのガイドを提供します。
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して画像の明るさを調整する方法
url: /ja/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java で画像の明るさを調整する

## はじめに

Java のコードから直接画像の **明るさの調整方法を学びたい** 方は、ここが最適です。明るさの微調整は、グラフィックデザイナー、写真家、画像処理パイプラインを構築するすべての人に頻繁に求められる作業です。この **java 画像操作チュートリアル** では、PSD/TIFF の読み込み、明るさオフセットの適用、結果の保存という一連の流れを、Aspose.PSD for Java ライブラリを使って解説します。

## クイック回答
- **どのライブラリが明るさを扱うか？** Aspose.PSD for Java  
- **どのメソッドが明るさを変更するか？** `RasterImage.adjustBrightness()`  
- **PSD と TIFF ファイルを扱えるか？** はい、API は両方の形式をサポートしています。  
- **本番環境でライセンスは必要か？** 評価版以外の使用には商用ライセンスが必要です。  
- **実装にかかる時間は？** 基本的な調整であれば通常 10 分未満です。

## 画像の明るさ調整とは？

画像の明るさ調整は、画像内のすべてのピクセルの全体的な明るさを変更する操作です。明るさを上げると暗部が明るくなり、下げると全体が暗くなります。この操作は、露出不足の写真の補正、印刷用アセットの準備、アプリケーションでのビジュアルエフェクト作成などに有用です。

## Aspose.PSD for Java を選ぶ理由

- **フルフォーマットサポート** – PSD、TIFF、JPEG、PNG など多数。  
- **外部ネイティブ依存なし** – 純粋な Java で、統合が簡単。  
- **高性能キャッシュ** – ラスター データをキャッシュでき、繰り返し操作が高速。  
- **リッチ API** – カラー補正、レイヤー、マスク、その他高度な編集用メソッドを提供。

## 前提条件

チュートリアルに入る前に、以下の前提条件を満たしていることを確認してください。

- Aspose.PSD for Java ライブラリ: [Aspose.PSD for Java ドキュメント](https://reference.aspose.com/psd/java/) からダウンロードしてインストールしてください。

## パッケージのインポート

まず、Java プロジェクトに必要なパッケージをインポートします。この例では以下を使用します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

次に、画像の明るさ調整プロセスをシンプルな手順に分解していきます。

## Aspose.PSD を使った明るさ調整手順

### 手順 1: 画像を読み込む

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

このステップでは対象画像を読み込み、さらに処理するために `RasterImage` にキャストします。

### 手順 2: 明るさを調整する

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

ここで `adjustBrightness` メソッドを使って画像の明るさを変更します。この例では明るさを 50 ユニット減少させていますが、要件に合わせて値をカスタマイズできます。

### 手順 3: TiffOptions を設定する

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

調整後の画像を保存するための `TiffOptions` を構成します。`bitsPerSample` や `photometric` プロパティは、必要に応じて調整してください。

### 手順 4: 結果画像を保存する

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

最後に、指定した `TiffOptions` を使用して変更された画像を保存します。

## よくある問題と解決策

| 問題 | 原因 | 解決策 |
|------|------|--------|
| **`ClassCastException` が発生する** | ファイルがラスタ画像ではなくベクタ PSD などである | ソースファイル形式を確認するか、キャスト前に `image instanceof RasterImage` をチェックしてください。 |
| **明るさの変更が反映されない** | 調整前に画像がキャッシュされていない | 手順 1 のように `rasterImage.cacheData()` を呼び出してください。 |
| **保存したファイルが破損して見える** | `TiffOptions` の設定が誤っている | `bitsPerSample` が元画像の深度（通常はチャンネルあたり 8 ビット）と一致していることを確認してください。 |

## FAQ（よくある質問）

### Q1: PSD 以外の画像形式でも明るさを調整できますか？

A1: はい、Aspose.PSD for Java は JPEG、PNG、TIFF などさまざまな画像形式をサポートしています。

### Q2: 画像調整中にエラーが発生した場合、どう対処すればよいですか？

A2: try‑catch ブロックを使用して例外を捕捉し、適切に処理できます。

### Q3: 明るさ調整の範囲に制限はありますか？

A3: 調整範囲は画像の内容とフォーマットに依存しますが、Aspose.PSD は柔軟にカスタマイズ可能です。

### Q4: 商用プロジェクトで Aspose.PSD for Java を使用できますか？

A4: はい、商用ライセンスを取得すれば使用可能です。ライセンスは[こちら](https://purchase.aspose.com/buy)から入手できます。

### Q5: 無料トライアルはありますか？

A5: はい、[こちら](https://releases.aspose.com/)から無料トライアルをご利用いただけます。

### Q6: `adjustBrightness` メソッドはレイヤーの表示状態に影響しますか？

A6: このメソッドはラスタライズされた合成画像に対して動作するため、ラスタライズ時にレイヤーの可視性は考慮されます。

### Q7: 複数の調整（コントラスト、彩度など）を連続して適用できますか？

A7: もちろん可能です。明るさ調整後に同じ `RasterImage` インスタンスで `adjustContrast`、`adjustSaturation` などを呼び出せます。

---

**最終更新日:** 2025-12-19  
**テスト環境:** Aspose.PSD for Java 24.12（執筆時点での最新バージョン）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}