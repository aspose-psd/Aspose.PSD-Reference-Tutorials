---
date: 2026-02-20
description: Aspose.PSD for Java を使用して、PSD のカラーモードを 16 ビットグレースケールに設定しながら PSD を PNG
  に変換する方法を学びましょう。コード例付きのステップバイステップガイドです。
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Javaで16ビットグレースケールカラー モードのPSDをPNGに変換する方法
url: /ja/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 16ビットグレースケール カラーモードで PSD を PNG に変換する（Java）

## はじめに
グラフィックデザインや画像操作の世界に飛び込むとき、**PSD を PNG に変換する方法** を知っていることは、まさに秘密兵器のようなものです。16ビットグレースケールモードを使用すると、驚異的な深みとトーンの豊かさが加わり、画像が際立ちます。このチュートリアルでは、**PSD のカラーモード**を 16ビットグレースケールに設定し、次に **Aspose.PSD for Java** を使って **PSD を PNG としてエクスポート**する手順を解説します。画像ワークフローをレベルアップする準備はできましたか？さっそく始めましょう。

## クイック回答
- **「PSD を PNG に変換する」には何が含まれますか？** PSD を読み込み、必要に応じてカラーモードを変更し、PNG ファイルとして保存します。  
- **変換を担当する Aspose のクラスはどれですか？** 読み込みに `PsdImage`、保存に `PngOptions` を使用します。  
- **特別なライセンスが必要ですか？** テスト用にはトライアルで動作しますが、本番環境では有料ライセンスが必要です。  
- **PNG でも 16 ビット深度を保持できますか？** はい、`PngColorType.GrayscaleWithAlpha` を使用すれば保持できます。  
- **サポートされている IDE はどれですか？** 任意の Java IDE – IntelliJ IDEA、Eclipse、VS Code などが使用可能です。

## なぜ 16ビットグレースケールで PSD を PNG に変換するのか？
* **トーンディテールを保持:** 16ビットグレースケールは 65 536 色階調を保存し、8ビット画像の 256 色階調よりはるかに多くの階調を提供します。  
* **広範な互換性:** PNG はブラウザ、モバイルアプリ、デスクトップツールで広くサポートされており、高品質データを保持したまま利用できます。  
* **ロスレスワークフロー:** Aspose.PSD で変換すれば不要な圧縮アーティファクトが発生せず、アーカイブやさらなる処理に最適です。

## 前提条件
チュートリアルを最大限に活用できるよう、事前に以下を準備してください。

1. **Java Development Kit (JDK)** – 最新バージョンがインストールされていることを確認してください。ダウンロードは [Oracle のサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) から行えます。  
2. **Aspose.PSD for Java Library** – PSD ファイルを操作するエンジンです。入手は [Aspose ダウンロードページ](https://releases.aspose.com/psd/java/) から。  
3. **IDE** – IntelliJ IDEA、Eclipse、または Visual Studio Code があれば問題ありません。  
4. **基本的な Java 知識** – Java の構文に慣れていると手順がスムーズに進みます。  
5. **サンプル PSD ファイル** – Adobe Photoshop で作成するか、無料のサンプルをオンラインで入手してください。

準備はできましたか？では、必要なパッケージをインポートしてコーディングを始めましょう。

## パッケージのインポート
まず、Java ファイルに必要な Aspose.PSD のインポートを追加します。

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

これらのインポートにより、PSD ファイルの操作、カラーモードの設定、PNG へのエクスポートに必要な機能が利用可能になります。

## 手順 1: ディレクトリの定義
最初に、ソースフォルダーと出力フォルダーを設定します。これにより、元の PSD を読む場所と変換後のファイルを書き込む場所をプログラムに指示できます。

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

プレースホルダー文字列を実際のマシン上のパスに置き換えてください。

## 手順 2: 画像処理を行うメソッドの作成
変換ロジックを再利用可能なメソッドにカプセル化します。このメソッドは、カラーモード、ビット深度、圧縮設定など、調整したいすべてのパラメータを受け取ります。

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

このメソッドにより、**PSD のカラーモードを設定**し、続いて **PSD を PNG としてエクスポート**する一連の流れが実現できます。

## 手順 3: ファイルパスの定義と PSD の読み込み
メソッド内で完全なファイルパスを構築し、元の 16ビットグレースケール PSD を読み込みます。

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` は、エクスポートした各ファイルに使用した設定を追跡するために役立ちます。

## 手順 4: レイヤーまたは全画像の処理
ここでは、特定のレイヤーまたは画像全体に描画を行います。この例では、結果をより見やすくするために控えめなグレーの枠線を追加します。

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

矩形は動的に計算されるため、画像サイズに関係なく中央に配置されます。

## 手順 5: 変更された PSD ファイルの保存
描画後、指定したカラーモードとビット深度で PSD を保存します。これが **変換前に PSD のカラーモードを設定**する核心部分です。

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## 手順 6: PSD を PNG に変換
最後に、保存した PSD を読み込み、PNG としてエクスポートします。`PngColorType.GrayscaleWithAlpha` を使用することで、PNG ファイルでも 16ビット深度を保持できます。

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

これで、**PSD を PNG に変換**しつつ、高品質な 16ビットグレースケールデータを保持できました。

## よくある問題と解決策
| 問題 | 発生原因 | 対策 |
|-------|----------------|-----|
| **“Unsupported color type” 例外** | サポートされていないチャンネル構成で PSD を保存しようとしたため。 | `channelBitsCount` が実際のビット深度 (16) と一致していること、`channelsCount` がグレースケール (1) に正しく設定されていることを確認してください。 |
| **ファイルが見つからない** | ソースディレクトリのパスが間違っているため。 | `sourceDir` 文字列を再確認し、PSD ファイルが存在することを確認してください。 |
| **出力 PNG が黒くなる** | アルファチャンネルの処理なしで PNG が保存されたため。 | 上記のように `PngColorType.GrayscaleWithAlpha` を使用してください。 |

## よくある質問

**Q: 16ビットグレースケール カラーモードとは何ですか？**  
A: 65 536 色階調を提供し、標準的な 8ビット（256 色階調）よりはるかに多くのトーンディテールを実現します。

**Q: Aspose.PSD をグレースケール以外の画像で使用できますか？**  
A: もちろんです！Aspose.PSD は RGB、CMYK、Lab など多数のカラーモードをサポートしています。

**Q: Aspose.PSD のトライアル版はありますか？**  
A: はい、無料のトライアル版を利用できます。まずは [Aspose ダウンロードページ](https://releases.aspose.com/) へアクセスしてください。

**Q: Aspose.PSD の使用例は他にどこで見られますか？**  
A: 詳細な例やチュートリアルは [ドキュメンテーション](https://reference.aspose.com/psd/java/) をご覧ください。

**Q: Aspose.PSD のライセンスはどうやって購入しますか？**  
A: [Aspose 購入ページ](https://purchase.aspose.com/buy) からライセンスをご購入いただけます。

---

**最終更新日:** 2026-02-20  
**テスト環境:** Aspose.PSD for Java 24.12（執筆時点での最新バージョン）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}