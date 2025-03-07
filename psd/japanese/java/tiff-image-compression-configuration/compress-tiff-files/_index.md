---
title: Aspose.PSD for Java を使用して TIFF ファイルを圧縮する
linktitle: Aspose.PSD for Java を使用して TIFF ファイルを圧縮する
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して、品質を犠牲にすることなく TIFF ファイルを効率的に圧縮します。詳細なガイドに従ってワークフローを効率化します。
weight: 10
url: /ja/java/tiff-image-compression-configuration/compress-tiff-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用して TIFF ファイルを圧縮する

## 導入

大規模なグラフィック デザイン プロジェクトに取り組んでいて、PSD ファイルがシステムを圧迫しているとします。これらのファイルを共有するか、後で使用するために保存する必要がありますが、サイズが大きすぎて処理できません。そこで、PSD ファイルを TIFF 形式に圧縮すると便利です。TIFF ファイルは、品質とサイズのバランスが取れているため、保存と共有に最適です。このチュートリアルでは、Aspose.PSD for Java を使用して TIFF ファイルを圧縮するプロセスについて説明します。これにより、画像がコンパクトになりながらも品質が維持されます。

## 前提条件

コードに進む前に、準備を整えましょう。このチュートリアルに従うには、次のものが必要です。

1.  Aspose.PSD for Java: Aspose.PSD for Javaライブラリがあることを確認してください。[Webサイト](https://releases.aspose.com/psd/java/).
2. Java 開発環境: JDK がインストールされていることを確認してください。IntelliJ IDEA や Eclipse などの IDE も役立ちます。
3. サンプル PSD ファイル: 作業には PSD ファイルが必要です。 PSD ファイルがない場合、Adobe Photoshop などのグラフィック デザイン ソフトウェアを使用して、シンプルな PSD ファイルを作成できます。

すべての設定が完了したら、TIFF ファイルの圧縮を開始する準備が整います。

## パッケージのインポート

実際のコーディングを始める前に、必要なパッケージを Java プロジェクトにインポートする必要があります。これらのパッケージは、PSD ファイルと TIFF ファイルの操作に必要なクラスとメソッドを提供します。

```java
import com.aspose.psd.ColorPaletteHelper;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.tiff.enums.TiffCompressions;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

必要なパッケージをインポートしたので、PSD ファイルを TIFF 形式に圧縮するためのステップバイステップ ガイドに進みましょう。

## ステップ1: PSDファイルを読み込む

最初のステップは、圧縮する PSD ファイルを読み込むことです。Aspose.PSD for Java を使用すると、このプロセスが非常に簡単になります。
 PSDファイルを読み込むには、`Image.load()`メソッド。このメソッドは、指定されたディレクトリから PSD ファイルを読み取ります。どのように実行されるか見てみましょう。

```java
String dataDir = "Your Document Directory";
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

ここでは、PSDファイルを読み込みます。`layers.psd`指定されたディレクトリから`dataDir`。`Image.load()`メソッドはジェネリックを返す`Image`オブジェクトをキャストし、`PsdImage`オブジェクト。このキャストにより、PSD ファイルの特定の機能にアクセスできるようになります。

なぜこれが重要なのでしょうか? PSD ファイルの読み込みは、これから行うすべての作業の基礎となります。メイン イベントの前にステージを設定するようなものです。

## ステップ2: TIFFオプションを作成する

PSD ファイルが読み込まれたら、次のステップは、最終的な TIFF 画像の外観を決定する TIFF オプションを作成することです。このステップでは、圧縮、サンプルあたりのビット数、その他の重要な設定を行います。

画像を圧縮するには、`TiffOptions`クラス。このクラスを使用すると、TIFF ファイルのさまざまな設定を構成できます。

```java
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);
```

ここで初期化しました`TiffOptions`デフォルトの形式で設定します。しかし、これはほんの始まりに過ぎません。調整する必要がある設定を詳しく見ていきましょう。

## ステップ3: TIFF圧縮を設定する

TIFF オプションの設定が完了したので、次は圧縮に焦点を当てます。圧縮によりファイル サイズが縮小され、TIFF ファイルの管理が容易になります。

この例では、ロスレス圧縮方式である LZW 圧縮を使用します。つまり、ファイル サイズが縮小されても、画像の品質はそのまま維持されます。

```java
outputSettings.setCompression(TiffCompressions.Lzw);
```

圧縮を`Lzw`、画質を犠牲にすることなくファイル サイズを縮小します。ファイル サイズが小さく、画質が高品質という、両方の長所を兼ね備えた製品です。

LZW を選択する理由 LZW 圧縮は、グラフィックやデザイン ファイルによくある繰り返しパターンのある画像に特に効果的です。

## ステップ4: サンプルあたりのビット数と測光モードを調整する

圧縮は不可欠ですが、最終的な TIFF ファイルの品質とサイズに影響を与える他の要素もあります。最も重要な 2 つは、サンプルあたりのビット数と測光モードです。

### サンプルあたりのビット数の設定

サンプルあたりのビット数によって、画像の色深度が決まります。このチュートリアルでは、画像の品質とファイル サイズのバランスが取れた 4 ビットのグレースケール パレットを使用します。

```java
int[] ushort = {4};  
outputSettings.setBitsPerSample(ushort);
```

ここでは、サンプルあたりのビット数を 4 に設定しています。つまり、画像内の各ピクセルは 4 ビットで表され、16 種類のグレーの階調が可能になります。この設定は、フルレンジの色を必要としない画像に最適です。

### 測光モードの設定

フォトメトリック モードは、ピクセル データの解釈方法を決定します。この例では、色のない画像を圧縮するのに最適なグレースケール パレットを使用します。

```java
outputSettings.setPhotometric(TiffPhotometrics.Palette);
outputSettings.setPalette(ColorPaletteHelper.create4BitGrayscale(true));
```

測光モードを`Palette` ビットのグレースケール パレットを使用すると、プログラムを限られた数のシェードを持つグレースケール画像として扱うように指示します。これにより、視覚的な整合性を維持しながらファイル サイズがさらに削減されます。

## ステップ5: 圧縮されたTIFFファイルを保存する

すべての設定が完了したら、最後のステップとして PSD ファイルを圧縮された TIFF ファイルとして保存します。このステップは、これまでに行ったすべての作業の集大成です。

圧縮された TIFF ファイルを保存する方法は次のとおりです。

```java
psdImage.save(dataDir + "SampleTiff_out.tiff", outputSettings);
```

このコード行はPSDファイルをTIFFファイルとして指定されたディレクトリに保存します。`dataDir`。`outputSettings`以前に設定した内容に従ってファイルが圧縮されていることを確認してください。

これで完了です。PSD ファイルは、コンパクトで簡単に共有できる TIFF ファイルになりました。

## 結論

Aspose.PSD for Java を使用して TIFF ファイルを圧縮するのは簡単なプロセスであり、画像の品質を維持しながら大量のストレージ スペースを節約できます。このチュートリアルで説明されている手順に従うことで、PSD ファイルのサイズを効率的に縮小し、より管理しやすい TIFF 形式に変換できます。画像の保存、共有、アーカイブのいずれの場合でも、この方法を使用すると、品質やパフォーマンスを犠牲にする必要がありません。

## よくある質問

### 他の形式ではなく TIFF を使用する利点は何ですか?

TIFF ファイルはロスレス圧縮を提供するため、画像の品質を維持しながらファイル サイズを縮小できます。また、さまざまなプラットフォームやソフトウェアで広くサポートされています。

### この方法を使用してカラー画像を圧縮できますか?

はい、できます。ただし、このチュートリアルではグレースケール画像に焦点を当てています。カラー画像を扱うための設定を変更するには、`BitsPerSample`そして`Photometric`モード。

### LZW 圧縮はすべての画像にとって最適なオプションですか?

LZW 圧縮は、ロゴや単純なグラフィックなどの繰り返しパターンを持つ画像に最適です。ただし、写真の場合は、JPEG などの他の圧縮方法の方が適している場合があります。

### Aspose.PSD for Java を使用して他のファイル形式を圧縮できますか?

Aspose.PSD for Java は主に PSD ファイルを処理しますが、これらのファイルを TIFF、JPEG、PNG などのさまざまな形式に変換するための広範なサポートも提供します。

### グレースケール圧縮は画像の品質にどのような影響を与えますか?

グレースケール圧縮により、画像内の色の数が減り、視覚的な詳細が減少する可能性があります。ただし、特定の種類の画像では、このトレードオフは最小限であり、ファイル サイズが大幅に削減される可能性があります。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
