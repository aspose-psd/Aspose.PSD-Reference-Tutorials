---
date: 2025-12-17
description: Aspose.PSD for Java を使用して、PSD のカラーモードを 16 ビットグレースケールに設定しながら PSD を PNG
  に変換する方法を学びましょう。コード例付きのステップバイステップガイド。
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Javaで16ビットグレースケールカラーモードのPSDをPNGに変換する方法
url: /ja/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Javaで16ビットグレースケール カラーモードを使用してPSDをPNGに変換する

## はじめに
グラフィックデザインや画像操作の世界に足を踏み入れるとき、**convert PSD to PNG** の方法を理解することは、まさに秘密兵器を手に入れたようなものです。特に、16ビットグレースケールモードを使用すると、画像に驚くほどの深みとディテールが加わり、真に際立ちます。このチュートリアルでは、Aspose.PSD for Java を使用して **set PSD color mode** を 16ビットグレースケールに設定し、続いて **export PSD as PNG** する手順を解説します。画像ワークフローを次のレベルへ引き上げる準備はできましたか？さっそく始めましょう。

## クイック回答
- **“convert PSD to PNG” が何を行うか？** PSD をロードし、必要に応じてカラーモードを変更し、PNG ファイルとして保存します。  
- **変換を担当する Aspose クラスはどれか？** ロード用に `PsdImage`、保存用に `PngOptions`。  
- **特別なライセンスが必要か？** テスト用にはトライアルで動作しますが、本番環境では有料ライセンスが必要です。  
- **PNG で 16 ビット深度を保持できるか？** はい、`PngColorType.GrayscaleWithAlpha` を使用すれば保持できます。  
- **対応 IDE は？** 任意の Java IDE – IntelliJ IDEA、Eclipse、VS Code など。

## 前提条件
始める前に、このチュートリアルを最大限に活用できるよう、環境が整っていることを確認しましょう。必要なものは以下の通りです：

1. **Java Development Kit (JDK)** – 最新バージョンがインストールされていることを確認してください。[Oracle のサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)からダウンロードできます。  
2. **Aspose.PSD for Java Library** – PSD ファイルを操作できるエンジンです。[Aspose ダウンロードページ](https://releases.aspose.com/psd/java/)から取得してください。  
3. **IDE** – IntelliJ IDEA、Eclipse、または Visual Studio Code が使用できます。  
4. **Basic Java knowledge** – Java の構文に慣れていると手順がスムーズに進みます。  
5. **サンプル PSD ファイル** – Adobe Photoshop で作成するか、オンラインで無料サンプルをダウンロードしてください。

準備はできましたか？それでは、必要なパッケージをインポートしてコーディングを始めましょう。

## パッケージのインポート
まずは、必要な Aspose.PSD のインポート文を Java ファイルに追加します：

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

これらのインポートにより、PSD ファイルの操作、カラーモードの設定、結果の PNG へのエクスポートに必要な機能が利用できるようになります。

## 手順 1: ディレクトリの定義
まず、ソースフォルダーと出力フォルダーを設定します。これにより、プログラムは元の PSD を読み込む場所と変換後のファイルを書き込む場所を認識します。

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

プレースホルダー文字列を、実際のマシン上のパスに置き換えてください。

## 手順 2: 画像処理を行うメソッドの作成
変換ロジックを再利用可能なメソッドにカプセル化します。このメソッドは、カラーモード、ビット深度、圧縮など、調整したいすべてのパラメータを受け取ります。

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

このメソッドを使用すると、**set PSD color mode** してから **export PSD as PNG** までを一連の流れで実行できます。

## 手順 3: ファイルパスの定義と PSD のロード
メソッド内で完全なファイルパスを構築し、元の 16 ビットグレースケール PSD をロードします：

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` は、各エクスポートファイルに使用した設定を追跡するのに役立ちます。

## 手順 4: レイヤーまたは全画像の処理
ここでは、特定のレイヤーまたは画像全体に描画します。この例では、結果をより見やすくするために控えめなグレーの枠線を追加します。

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
描画後、指定したカラーモードとビット深度で PSD を保存します。これが変換前に **setting PSD color mode** を行う核心部分です。

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
最後に、先ほど保存した PSD をロードし、PNG としてエクスポートします。`PngColorType.GrayscaleWithAlpha` を使用することで、PNG ファイルに 16 ビット深度を保持します。

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

これで、**converted PSD to PNG** に成功し、高品質な 16 ビットグレースケールデータを保持したまま完了です。

## よくある問題と解決策
| Issue | Why It Happens | Fix |
|-------|----------------|-----|
| **“Unsupported color type” exception** | サポートされていないチャンネル構成で PSD を保存しようとしたために発生します。 | `channelBitsCount` が実際のビット深度 (16) と一致し、グレースケールの場合は `channelsCount` が正しく (1) 設定されていることを確認してください。 |
| **File not found** | ソースディレクトリのパスが間違っているためです。 | `sourceDir` 文字列を再確認し、PSD ファイルが存在することを確認してください。 |
| **Output PNG appears black** | アルファチャンネルの処理なしで PNG が保存されたためです。 | 上記のように `PngColorType.GrayscaleWithAlpha` を使用してください。 |

## よくある質問
**Q: 16 ビットグレースケール カラーモードとは何ですか？**  
A: 65 536 色階調のグレーを提供し、標準の 8 ビット（256 色）よりはるかに多くのトーンディテールを実現します。

**Q: Aspose.PSD をグレースケール以外の画像で使用できますか？**  
A: もちろんです！Aspose.PSD は RGB、CMYK、Lab など多数のカラーモードをサポートしています。

**Q: Aspose.PSD のトライアル版はありますか？**  
A: はい、Aspose.PSD の無料トライアル版を試すことができます。[Aspose ダウンロードページ](https://releases.aspose.com/)へアクセスしてください。

**Q: Aspose.PSD の使用例をもっと見つけるには？**  
A: 詳細な例やチュートリアルは[ドキュメンテーション](https://reference.aspose.com/psd/java/)をご覧ください。

**Q: Aspose.PSD のライセンスはどうやって購入しますか？**  
A: [Aspose 購入ページ](https://purchase.aspose.com/buy)からライセンスを購入できます。

---

**最終更新日:** 2025-12-17  
**テスト環境:** Aspose.PSD for Java 24.12 (執筆時点での最新バージョン)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}