---
date: 2025-12-21
description: Aspose.PSD for Java（業界トップクラスのJava画像操作ライブラリ）を使用して画像のコントラスト調整方法を学び、PSDをTIFFに効率的に変換しましょう。
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用した画像のコントラスト調整方法
url: /ja/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 画像のコントラストを調整する方法（Aspose.PSD for Java）

## はじめに

Javaプロジェクトで **コントラストの調整方法** を探しているなら、ここが適切な場所です。Aspose.PSD for Java は強力な **java 画像操作ライブラリ** で、コントラスト、明るさなどの画像プロパティを細かく調整できます。このチュートリアルでは、PSD ファイルのコントラストを上げ、さらに **PSD を TIFF に変換** して下流のワークフローに利用する手順を詳しく解説します。

## クイック回答
- **“adjust contrast” とは何ですか？** 最も暗いピクセルと最も明るいピクセルの差を変えることで、ディテールが際立ちます。
- **どのライブラリがこれを処理しますか？** Aspose.PSD for Java – フル機能の画像処理ツールキットです。
- **ライセンスは必要ですか？** テスト用には一時ライセンスで動作しますが、本番環境ではフルライセンスが必要です。
- **結果を TIFF として保存できますか？** はい、`TiffOptions` を使用して処理した画像をエクスポートします。
- **コードの実行時間はどれくらいですか？** 標準サイズの PSD ファイルであれば、通常は1秒未満です。

## コントラスト調整とは？

コントラスト調整は画像のトーン範囲を変更し、明暗領域の差を強調します。スキャン後に画像が平坦に見える場合や、印刷用グラフィックを準備する際に特に有用です。

## なぜ Aspose.PSD for Java を使用するのか？

- **豊富なフォーマットサポート** – PSD、TIFF、PNG、JPEG など多数の形式を開く、編集する、保存することができます。
- **高性能** – キャッシュやラスタ画像の最適化によりメモリ使用量を削減します。
- **シンプルな API** – `adjustContrast` のような単一メソッド呼び出しでコードが読みやすくなります。

## 前提条件

本題に入る前に、以下が揃っていることを確認してください：

- Java プログラミングの基本知識。
- Aspose.PSD for Java ライブラリがインストールされていること。ダウンロードは [here](https://releases.aspose.com/psd/java/) から可能です。

## パッケージのインポート

Java クラスに必要なインポートを追加します：

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 手順 1: 画像の読み込み

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

ソース PSD ファイル（`sample.psd`）を `Image` オブジェクトに読み込みます。これが以降のすべての処理のエントリーポイントとなります。

## 手順 2: RasterImage へキャストしデータをキャッシュ

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

`RasterImage` へキャストすることでピクセルレベルの操作が可能になります。キャッシュは特に大きなファイルでパフォーマンスを向上させます。

## 画像のコントラストを調整する方法

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` メソッドは、変化率（パーセンテージ）を表す整数を受け取ります。この例ではコントラストを **50 %** 上げています。

## Aspose.PSD を使用して PSD を TIFF に変換

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

ここでは `TiffOptions`（サンプルあたりのビット数、フォトメトリック解釈）を設定し、コントラスト強化画像を TIFF ファイルとして書き出します。

## よくある問題と解決策
- **画像がキャッシュされていない:** 大きな PSD では必ず `cacheData()` を呼び出して `OutOfMemoryError` を防ぎます。
- **予期しない色シフト:** `setPhotometric` が目的のカラースペース（RGB と CMYK）と一致しているか確認してください。
- **ファイルが見つからない:** `dataDir` が正しいフォルダーを指しているか、ファイル名が正しく綴られているか確認してください。

## よくある質問

### Q1: Aspose.PSD はさまざまな画像フォーマットに対応していますか？

A1: はい、Aspose.PSD はさまざまな画像フォーマットをサポートしており、プロジェクトに柔軟性を提供します。

### Q2: Aspose.PSD の一時ライセンスはどう取得できますか？

A2: 一時ライセンスは [here](https://purchase.aspose.com/temporary-license/) から取得できます。

### Q3: Aspose.PSD のドキュメントはどこにありますか？

A3: ドキュメントは [here](https://reference.aspose.com/psd/java/) で入手できます。

### Q4: Aspose.PSD のサポートオプションは何がありますか？

A4: サポートは [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) をご利用ください。

### Q5: Aspose.PSD を購入できますか？

A5: はい、Aspose.PSD は [here](https://purchase.aspose.com/buy) から購入できます。

## 結論

これで、Aspose.PSD for Java を使用して PSD 画像の **コントラストを調整** する方法と、**PSD を TIFF に変換** してさらに処理する方法が分かりました。これらの手順により、画像品質を細かく制御しつつ、コードをクリーンで保守しやすく保てます。`adjustBrightness` や `adjustGamma` など、他の画像調整メソッドも自由に試して、特定のニーズに合わせてください。

---

**最終更新日:** 2025-12-21  
**テスト環境:** Aspose.PSD for Java 24.12  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}