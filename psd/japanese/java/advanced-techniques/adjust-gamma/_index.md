---
date: 2026-02-27
description: Aspose.PSD を使用した Java 画像処理でガンマを調整し、PSD を TIFF に変換し、色あせた画像を修正する方法を簡潔なチュートリアルで学びましょう。
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Aspose.PSD を使用した Java 画像処理でガンマを調整する方法
url: /ja/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD を使用した Java 画像処理でガンマを調整する方法

## はじめに

**java image processing** に取り組んでいる方にとって、**ガンマの調整方法** を学ぶことは、ディテールを失わずに明るさとコントラストを向上させる基本的なテクニックです。このチュートリアルでは、**Aspose.PSD for Java** を使って PSD ファイルにガンマ補正を適用し、**PSD を TIFF に変換** し、**色あせた画像** を防ぐ方法を解説します。このアプローチが高速で信頼性が高く、サーバーサイドの画像パイプラインに最適である理由もご紹介します。

## クイック回答
- **ガンマ補正は何をするのですか？**  
  輝度値を再マッピングし、暗部を明るくしたり明部を暗くしたりしながら、全体のディテールを保持します。  
- **どのライブラリが処理を担当しますか？**  
  Aspose.PSD for Java がラスタ画像用の専用 `adjustGamma` メソッドを提供します。  
- **同じフローで PSD を TIFF に変換できますか？**  
  はい。ガンマ調整後に `TiffOptions` を使用して画像を直接 TIFF として保存できます。  
- **開発にライセンスは必要ですか？**  
  無料トライアルでテストは可能ですが、本番環境では商用ライセンスが必要です。  
- **サポートされている Java バージョンは？**  
  Aspose.PSD は Java 8 以降をサポートしています。

## Java 画像処理でガンマを調整する方法
ガンマ調整は、明るさやコントラストを扱う **java image processing tutorial** の核心です。以下では手順を分解し、各行の意味を解説し、既存のコードベースに統合する方法を示します。

## Java のガンマ補正とは？
ガンマ補正は、エンコードされたピクセル値と表示される明るさとの非線形関係を変更します。ガンマ曲線を調整することで、**色あせた画像** の問題を解消したり、ハイライトを過剰に露出させずにシャドウのディテールを強調したりできます。

## なぜ Aspose.PSD をガンマ補正に使うのか？
Aspose.PSD は **java image processing library** として、PSD フォーマットの複雑さを抽象化します。カラープロファイルやキャッシュ処理を自動で行い、シンプルな `adjustGamma` 呼び出しだけで **java gamma correction** や **convert PSD to TIFF** のワークフローを実現できるため、非常に便利です。

## 前提条件

1. **Java 開発環境** – Java 8 以降がインストールされていること。  
2. **Aspose.PSD ライブラリ** – JAR をダウンロードし、プロジェクトに追加します。公式の [documentation](https://reference.aspose.com/psd/java/) を参照してください。  
3. **サンプル画像** – 処理対象の PSD ファイル（例: `sample.psd`）。

## パッケージのインポート

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 手順 1: 画像を読み込む

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

**プロのコツ:** ラスタデータを一度キャッシュしておくと、連続して複数の調整を行う際のメモリ使用量が抑えられます。

## 手順 2: ガンマを調整する

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

赤・緑・青チャンネルごとに異なる値を渡すことで、チャンネル単位の微調整も可能です。

## 手順 3: TiffOptions を作成する

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

8 ビットサンプル (`{8,8,8}`) を指定すると、TIFF のファイルサイズを抑えつつ色忠実度を保てます。

## 手順 4: 結果画像を保存する

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

保存後は、印刷サービスや Web API などの下流システムへ TIFF を渡すことができます。

## 主な利用ケース

- **自動化されたグラフィックパイプライン** – サムネイル生成前にリアルタイムでガンマを調整。  
- **バッチ変換ツール** – 大量の PSD アーカイブを明るさを正規化しながら TIFF に変換。  
- **Web サービス** – PSD を受け取りガンマ補正を適用し、クライアントに TIFF を返すエンドポイントを提供。

## よくある問題と対策

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **画像が色あせて見える** | ガンマ値が高すぎる（例: > 2.5） | ガンマ係数を 1.8〜2.2 の範囲に下げる |
| **`rasterImage.isCached()` が false を返す** | 画像がまだメモリにロードされていない | ガンマ調整前に `rasterImage.cacheData()` を呼び出す |
| **TIFF ファイルサイズが大きい** | サンプルビット数が 16 ビットに設定されている | 例に示したように 8 ビットサンプル (`{8,8,8}`) を使用する |

## FAQ

**Q: 各色チャンネルに異なるガンマ値を適用できますか？**  
A: はい。`adjustGamma` メソッドは赤・緑・青それぞれに個別の float 値を受け取ります。

**Q: 保存前に複数の画像調整を連鎖させることは可能ですか？**  
A: もちろんです。同じ `RasterImage` インスタンスでリサイズ、クロップ、カラー補正などを順に実行できます。

**Q: Aspose.PSD はマルチページ PSD ファイルをサポートしていますか？**  
A: はい。各レイヤーに個別にアクセスして処理できます。

**Q: TIFF 以外にエクスポートできる形式は？**  
A: Aspose.PSD は PNG、JPEG、BMP など多数の形式を、対応するオプションクラスを使ってエクスポート可能です。

**Q: ガンマ補正後に色あせた画像にならないようにするには？**  
A: まずは中程度のガンマ（約 2.0）から始め、プレビューで確認しながら明るすぎる場合は下げて調整してください。

## 結論

おめでとうございます！**java image processing** のワークフローで **ガンマを調整** し、PSD を TIFF に変換し、**色あせた画像** といった一般的な落とし穴を回避する方法を習得しました。このパターンは明るさとコントラストを細かく制御できるため、自動化されたグラフィックパイプライン、Web サービス、デスクトップユーティリティなどに最適です。

---

**最終更新日:** 2026-02-27  
**テスト環境:** Aspose.PSD 24.11 for Java  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}