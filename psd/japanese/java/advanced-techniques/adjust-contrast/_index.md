---
date: 2026-02-25
description: Aspose.PSD for Java（業界トップクラスのJava画像操作ライブラリ）を使用して、PSD を TIFF に変換し、画像のコントラスト調整を行う方法を学びましょう。
linktitle: Convert PSD to TIFF and Adjust Contrast
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して PSD を TIFF に変換し、コントラストを調整する方法
url: /ja/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD を TIFF に変換し、Aspose.PSD for Java でコントラストを調整する方法

## はじめに

**PSD を TIFF に変換**しながら、グラフィックの視覚品質を微調整したい場合は、ここが最適です。このチュートリアルでは、堅牢な **java image manipulation** ライブラリである Aspose.PSD for Java を使用した完全なワークフローを解説します。**画像コントラスト調整**の方法、パフォーマンス向上のための大規模ラスターデータのキャッシュ、そして最終的に **TIFF として画像を保存**して下流処理に渡す手順を学びます。さっそく始めましょう！

## クイック回答
- **“adjust contrast” とは何ですか？** 最も暗いピクセルと最も明るいピクセルの差を変えることで、ディテールが際立ちます。  
- **どのライブラリがこれを扱いますか？** Aspose.PSD for Java – フル機能の画像処理ツールキット。  
- **ライセンスは必要ですか？** **temporary aspose license** はテストに使用できます。製品版ではフルライセンスが必要です。  
- **“convert PSD to TIFF” を変換できますか？** もちろんです – `TiffOptions` を使用して処理済み画像をエクスポートします。  
- **コードの実行時間はどれくらいですか？** 標準サイズの PSD ファイルであれば、最新ハードウェア上で概ね 1 秒未満です。

## 画像コントラスト調整とは？

コントラスト調整は画像のトーンレンジを変更し、明暗領域の区別を強調します。スキャン後に画像が平坦に見える場合や、印刷用グラフィックを準備する際に特に有用です。

## なぜ Aspose.PSD for Java を使用するのか？

- **豊富なフォーマットサポート** – TIFF、PNG、JPEG など多数の形式で **画像を保存** できます。  
- **高性能** – キャッシュとラスタ画像の最適化によりメモリ使用量を削減し、大容量 PSD ファイルでも快適に処理できます。  
- **シンプルな API** – `adjustContrast` のような単一メソッド呼び出しでコードが読みやすく、保守性が向上します。  
- **包括的な java image manipulation** 機能を備えており、簡易スクリプトからエンタープライズ規模のアプリケーションまで対応可能です。

## 前提条件

始める前に以下を確認してください：

- Java プログラミングの基本知識。  
- Aspose.PSD for Java ライブラリがインストール済み。ダウンロードは [here](https://releases.aspose.com/psd/java/) から。

## パッケージのインポート

Java クラスに必要なインポートを追加します：

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

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

ソース PSD ファイル（`sample.psd`）を `Image` オブジェクトに読み込みます。これが以降のすべての処理のエントリーポイントとなります。

## ステップ 2: RasterImage にキャストしてデータをキャッシュする

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

`RasterImage` にキャストすることでピクセルレベルの操作が可能になります。キャッシュを行うことで、特に大容量ファイルの処理速度が向上します。

## 画像のコントラストを調整する方法

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` メソッドは、変化率（パーセンテージ）を表す整数を受け取ります。この例ではコントラストを **50 %** 上げています。

## Aspose.PSD を使用して PSD を TIFF に変換する

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

ここでは `TiffOptions`（サンプルあたりのビット数、フォトメトリック解釈）を設定し、**画像を TIFF として保存**します。この手順で **convert PSD to TIFF** のワークフローが完了します。

## 一般的な問題と解決策
- **画像がキャッシュされていない:** 大きな PSD では必ず `cacheData()` を呼び出し、`OutOfMemoryError` を回避してください。  
- **予期しない色シフト:** `setPhotometric` が目的のカラースペース（RGB と CMYK）と一致しているか確認してください。  
- **ファイルが見つからない:** `dataDir` が正しいフォルダーを指しているか、ファイル名が正しく綴られているか確認してください。

## よくある質問

### Q1: Aspose.PSD はさまざまな画像フォーマットに対応していますか？

A1: はい、Aspose.PSD は多数の画像フォーマットをサポートしており、プロジェクトで柔軟に利用できます。

### Q2: Aspose.PSD の一時ライセンスはどこで取得できますか？

A2: 一時ライセンスは [here](https://purchase.aspose.com/temporary-license/) から取得できます。

### Q3: Aspose.PSD のドキュメントはどこにありますか？

A3: ドキュメントは [here](https://reference.aspose.com/psd/java/) にあります。

### Q4: Aspose.PSD のサポートオプションは何がありますか？

A4: サポートについては [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) をご覧ください。

### Q5: Aspose.PSD を購入できますか？

A5: はい、購入は [here](https://purchase.aspose.com/buy) から可能です。

## 結論

これで **PSD を TIFF に変換**し、Aspose.PSD for Java を使って **画像コントラスト調整**を行う方法が分かりました。これらの手順により、画像品質を細かく制御しつつ、コードをシンプルで保守しやすく保てます。`adjustBrightness` や `adjustGamma` など、他の調整メソッドも試してみて、ニーズに合わせた最適な画像処理を実現してください。

---

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}