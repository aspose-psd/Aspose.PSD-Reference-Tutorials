---
date: 2026-07-22
description: Aspose.PSD for Java を使用して PSD レイヤーを抽出し、PNG に変換する方法を学びます。堅牢なグラフィック操作が必要な開発者に最適です。
keywords:
- extract psd layers
- how to extract psd
- convert psd to png
lastmod: 2026-07-22
linktitle: Aspose.PSD Java を使用して PSD レイヤーを抽出し、PSD ファイルのレイヤーサポートを追加する
og_description: Aspose.PSD for Java で PSD レイヤーを抽出し、PNG に変換します。ステップバイステップのガイドに従って、レイヤー抽出と画像変換を自動化しましょう。
og_image_alt: Developer guide showing Java code to extract PSD layers and save as
  PNG using Aspose.PSD
og_title: PSD レイヤーの抽出 – Aspose.PSD Java を使用した PSD ファイルのレイヤーサポート追加
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  headline: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
    Java
  type: TechArticle
- description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  name: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD Java
  steps:
  - name: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
  - name: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
    text: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
    text: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that allows you to manipulate PSD files
      without having Photoshop installed.
    question: What is Aspose.PSD for Java?
  - answer: Yes! While primarily for PSD files, Aspose offers libraries for a wide
      range of formats, including AI, PDF, and SVG.
    question: Can I use Aspose.PSD for other file formats?
  - answer: Absolutely! You can download a free trial version [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: Access the Aspose forum for PSD‑related questions [here](https://forum.aspose.com/c/psd/34).
    question: Where can I get support if I run into problems?
  - answer: Iterate over `image.getLayers()`, create a new `Bitmap` for each layer,
      and save it with its own `PngOptions`. This yields individual PNG files per
      layer.
    question: Can I convert each layer to a separate PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- extract psd
- Aspose.PSD
- Java image processing
title: Aspose.PSD Java を使用して PSD レイヤーを抽出し、PSD ファイルのレイヤーサポートを追加する
url: /ja/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Java を使用して PSD レイヤーを抽出し、PSD ファイルのレイヤーサポートを追加する

## はじめに
Photoshop Document（PSD）ファイルの取り扱いは、グラフィックデザイナーや開発者にとって日常的な作業であり、**extract psd layers** は資産の再利用や画像パイプラインの自動化への最初のステップになることが多いです。このチュートリアルでは、PSD から個々のレイヤーを抽出し、フルレイヤーサポートを有効にし、Aspose.PSD for Java を使用して **convert PSD layers to PNG** を行う方法を学びます。環境設定からベストプラクティスのヒントまで網羅し、数分で任意の Java アプリケーションにこのワークフローを統合できるようにします。

## クイック回答
- **What does “extract PSD layers” mean?** PSD ファイルを読み込み、個々のレイヤーにアクセスして操作またはエクスポートできることを意味します。  
- **Which library handles this in Java?** Java でこれを処理するライブラリはどれですか？ Aspose.PSD for Java は Photoshop が不要なフル機能の PSD 処理を提供します。  
- **Can I convert PSD layers to PNG in one go?** PSD レイヤーを一度に PNG に変換できますか？ はい、適切なオプションでファイルを読み込み、透明度を保持する PNG オプションで保存することで可能です。  
- **Do I need a license for production use?** 本番環境で使用するにはライセンスが必要ですか？ 本番環境では商用ライセンスが必要です。評価用に無料トライアルが利用可能です。  
- **What Java version is required?** 必要な Java バージョンは何ですか？ JDK 8 以上（このチュートリアルでは例として JDK 11 を使用）。

## Aspose.PSD for Java を使用して PSD レイヤーを抽出する方法は？
PSD をロードし、レイヤー効果を有効にして、数行の Java コードで結果を PNG として保存します。この直接的なアプローチにより、サーバー上で Photoshop が不要になり、Java 8+ をサポートする任意のプラットフォームで動作します。  
まず、`setLoadEffectsResource(true)` と `setUseDiskForLoadEffectsResource(true)` を設定した `PsdLoadOptions` オブジェクトを作成し、`PsdImage.load(path, options)` でファイルをロードします。ロード後は、`image.save(outputPath, new PngOptions())` を使用してレイヤーをマージするか、`image.getLayers()` を反復処理して各レイヤーを個別にエクスポートできます。これにより、すべての効果が保持され、メモリ使用量を抑えることができます。

## なぜ PSD レイヤーを抽出して PNG に変換するのか？
レイヤーを抽出することで、**reuse assets**、**automate thumbnail generation**、そしてウェブ対応グラフィックの **preserve transparency** が可能になります。Aspose.PSD は **50+ input and output formats** をサポートし、ディスクベースのリソース処理により、ファイル全体をメモリに読み込むことなく数百ページに及ぶ PSD ファイルを処理できます。

## 前提条件
本格的に始める前に、以下が揃っていることを確認してください。

1. **Java Development Environment** – JDK がインストールされています。[Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) からダウンロードできます。  
2. **Aspose.PSD for Java** – 公式ダウンロードページ [here](https://releases.aspose.com/psd/java/) から最新のライブラリを取得してください。  
3. **Basic Java knowledge** – Java プログラムのコンパイルと実行に慣れていること。  
4. **IDE** – IntelliJ IDEA、Eclipse、またはお好みのエディタ。  
5. **A PSD file** – 任意の PSD を使用するか、テスト用にサンプル PSD をダウンロードしてください。

これらが揃ったら、PSD レイヤーの抽出を開始する準備が整います。

## パッケージのインポート
`PsdImage`、`PsdLoadOptions`、`PngOptions` クラスはワークフローの中心です。  

`PsdImage` は、メモリ内で単一の PSD ファイルを表す Aspose.PSD のトップレベルオブジェクトです。  

`PsdLoadOptions` は、レイヤー効果などのリソースのロード方法を制御できます。  

`PngOptions` は PNG ファイルの出力形式と透明度の取り扱いを定義します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## ステップ 1: ディレクトリの定義
ソース PSD と出力 PNG のパスを設定します。`dataDir` をファイルが存在するフォルダを指すように調整してください。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – `"Your Document Directory"` を実際のフォルダパスに置き換えてください。  
- `sourceFileName` – 処理したい PSD のフルパス。  
- `output` – 抽出されたレイヤーを含む PNG の出力先パス。

## ステップ 2: ロードオプションの設定
`PsdLoadOptions` を設定することで、すべてのレイヤー効果とリソースが正しくロードされ、**extract PSD layers** を行う際に重要です。

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – レイヤーに付随する追加効果（ドロップシャドウなど）をロードします。  
- `setUseDiskForLoadEffectsResource(true)` – 重いリソースをディスクにオフロードし、メモリ負荷を軽減します。

## ステップ 3: PSD ファイルのロード
ここでは、上記で定義したオプションを使用して PSD を `PsdImage` オブジェクトにロードします。

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

この時点で、`image` はすべてのレイヤー、マスク、効果を保持しており、抽出の準備ができています。

## ステップ 4: 保存オプションの設定
PNG の保存方法を設定します。`TruecolorWithAlpha` を使用すると、元のレイヤーの透明度が保持されます。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## ステップ 5: 画像の保存（Convert PSD Layers to PNG）
ロードした PSD（すべてのレイヤーを含む）を単一の PNG ファイルにエクスポートします。このステップは実質的に **convert psd layers png** を一度の操作で行います。

```java
image.save(output, saveOptions);
```

各レイヤーを個別の PNG にしたい場合は `image.getLayers()` を反復処理できますが、多くのユースケースではマージされた PNG で十分です。

## ステップ 6: まとめ
処理が成功したことを示すフレンドリーなコンソールメッセージを追加します。

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## 一般的な問題とヒント
- **Out‑of‑Memory Errors:** 非常に大きな PSD を処理する場合は、`setUseDiskForLoadEffectsResource(true)` を有効にして一時データをオフロードしてください。  
- **Missing Effects:** `setLoadEffectsResource(true)` が設定されていることを確認してください。設定されていないと、一部のレイヤー効果が無視される可能性があります。  
- **Path Problems:** プラットフォームに依存しないパス処理のために、`java.nio.file` の `Paths.get(...)` を使用してください。

## よくある質問

**Q: Aspose.PSD for Java とは何ですか？**  
A: Aspose.PSD for Java は、Photoshop をインストールせずに PSD ファイルを操作できるライブラリです。

**Q: Aspose.PSD を他のファイル形式でも使用できますか？**  
A: はい！主に PSD 用ですが、Aspose は AI、PDF、SVG など幅広いフォーマット向けのライブラリも提供しています。

**Q: 無料トライアル版はありますか？**  
A: もちろんです！無料トライアル版は [here](https://releases.aspose.com/) からダウンロードできます。

**Q: 問題が発生した場合、どこでサポートを受けられますか？**  
A: PSD 関連の質問は Aspose フォーラム [here](https://forum.aspose.com/c/psd/34) で取得できます。

**Q: 各レイヤーを個別の PNG に変換できますか？**  
A: `image.getLayers()` を反復処理し、各レイヤーごとに新しい `Bitmap` を作成して、個別の `PngOptions` で保存します。これにより、レイヤーごとに個別の PNG ファイルが生成されます。

## 結論
これで、Aspose.PSD for Java を使用して **extract PSD layers**、フルレイヤーサポートの有効化、そして **convert PSD layers to PNG** の方法を学びました。自動化されたアセットパイプラインを構築する場合でも、デスクトップアプリにグラフィック機能を追加する場合でも、Photoshop 自体が不要で Photoshop ファイルを細かく制御できます。フィルタの適用、プログラムによるレイヤーのマージ、またはワークフローに合わせて各レイヤーを個別にエクスポートするなど、さらに探求してみてください。

---

**最終更新日:** 2026-07-22  
**テスト環境:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.PSD for Java を使用して PSD を PNG にエクスポートし、新しいレギュラーレイヤーを追加する](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Java でレイヤーマスクサポート付き PSD を PNG にエクスポート](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Java で PSD を画像に変換 – Aspose.PSD で調整レイヤーを適用](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}