---
date: 2025-12-21
description: Aspose.PSD を使用して画像のガンマを調整し、Java で画像処理を行う方法を学びましょう。PSD を TIFF に変換し、ガンマ補正を適用するステップバイステップガイド。
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Java画像処理 – Aspose.PSDでガンマを調整
url: /ja/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Image Processing – Adjust Gamma with Aspose.PSD

## はじめに

**Java 画像処理** に取り組む際、画像のガンマを調整することは、ディテールを失わずに明るさとコントラストを向上させる基本的なテクニックです。このチュートリアルでは、**Aspose.PSD for Java** を使用して PSD ファイルにガンマ補正を適用し、結果を TIFF 画像としてエクスポートする方法を順を追って解説します。このアプローチが高速で信頼性が高く、サーバーサイドの画像パイプラインに最適である理由もご紹介します。

## クイックアンサー
- **ガンマ補正とはどのようなものですか？** 輝度値を再マッピングすることで、全体的なディテールを維持しながら、暗い部分を明るくしたり、明るい部分を暗くしたりします。
- **どのライブラリが処理を担当していますか？** Aspose.PSD for Java は、ラスター画像専用の `adjustGamma` メソッドを提供しています。
- **同じフローで PSD を TIFF に変換できますか？** はい。ガンマ調整後、`TiffOptions` を使用して画像を直接 TIFF に保存できます。
- **開発にはライセンスが必要ですか？** 無料トライアルはテスト用として使用できますが、本番環境での使用には商用ライセンスが必要です。
- **どのバージョンの Java がサポートされていますか？** Aspose.PSD は Java8 以降をサポートしています。

## Java 画像処理とは何ですか？

Java image processing とは、Java ライブラリを使用して視覚データの操作、分析、変換を行うことを指します。リサイズ、フィルタリング、カラー補正、フォーマット変換などのタスクを、デスクトップアプリや Web アプリケーションで自動化できます。

## ガンマ補正に Aspose.PSD を使用する理由

Aspose.PSD は PSD フォーマットの複雑さを抽象化したハイレベル API を提供し、実際の画像調整に集中できるようにします。キャッシュ処理やカラープロファイルの管理を行い、シンプルな `adjustGamma` 呼び出しだけで **image gamma correction** や **convert psd to tiff** のワークフローを実現できるため、最適です。

## 前提条件

チュートリアルに入る前に、以下の前提条件が整っていることを確認してください。

1. **Java 開発環境**– システムに Java 開発環境がインストールされていること。  
2. **Aspose.PSD ライブラリ** – Aspose.PSD ライブラリをダウンロードし、Java プロジェクトに組み込むこと。必要なリソースは [documentation](https://reference.aspose.com/psd/java/) にあります。  
3. **サンプル画像** – ガンマ調整に使用するサンプル PSD 画像を用意すること。

## パッケージのインポート

プロセスを開始するために、Java プロジェクトで必要なパッケージをインポートします。これにより Aspose.PSD の機能をシームレスに利用できるようになります。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## ステップ1: イメージを読み込む

サンプル PSD 画像を `RasterImage` クラスのインスタンスに読み込みます。これが以降のガンマ調整の基盤となります。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## ステップ2: ガンマを調整する

読み込んだ画像に対して `adjustGamma` メソッドを使用し、ガンマを調整します。必要に応じてガンマ値を微調整してください。

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## ステップ3: TiffOptionsを作成する

結果画像用に `TiffOptions` のインスタンスを作成します。ビット深度やフォトメトリックオプションなど、出力を希望通りに設定します。

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## ステップ4: 結果画像を保存する

先ほど定義した `TiffOptions` を使用して、操作した画像を TIFF 形式で保存します。

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## よくある問題と解決策

| 問題 | 発生原因 | 解決方法 |
|-------|----------------|------------|
| **画像が色褪せて見える** | ガンマ値が高すぎる (例: 2.5 より大きい) | ガンマ係数を 1.8 ～ 2.2 に下げてください。 |
| **`rasterImage.isCached()` が false を返す** | 画像がまだメモリに読み込まれていない | ガンマを調整する前に `rasterImage.cacheData()` を呼び出してください。 |
| **TIFF ファイルのサイズが大きい** | サンプルあたりのビット数が 16 ビットに設定されています | 例に示すように、8 ビットサンプル (`{8,8,8}`) を使用してください。 |

## よくある質問

**Q: 各カラーチャンネルに異なるガンマ値を適用できますか？**
A: はい。`adjustGamma` メソッドは、赤、緑、青の各チャンネルに別々の float 値を受け入れます。

**Q: 保存前に複数の画像調整を連続して実行できますか？**
A: もちろんです。同じ `RasterImage` インスタンスに対して、サイズ変更、切り抜き、または色補正を連続して実行できます。

**Q: Aspose.PSD は複数ページの PSD ファイルをサポートしていますか？**
A: はい、各レイヤーに個別にアクセスして処理できます。

**Q: TIFF 以外にどのような形式でエクスポートできますか？**
A: Aspose.PSD は、それぞれのオプションクラスを介して PNG、JPEG、BMP など、その他多くの形式をサポートしています。

## まとめ

おめでとうございます！Aspose.PSD for Java を使用して PSD ファイルのガンマを調整し、TIFF 画像としてエクスポートすることで、**Java 画像処理** を実行できました。このワークフローでは、画像の明るさとコントラストを細かく制御できるため、自動化されたグラフィックパイプライン、Webサービス、デスクトップユーティリティに最適です。

---

**最終更新日:** 2025年12月21日
**テスト環境:** Aspose.PSD 24.11 for Java
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
