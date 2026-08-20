---
date: 2026-05-29
description: Aspose.PSD for Java を使用して、カラー文字付きの PSD を PNG に保存する方法を学びます。このステップバイステップガイドでは、PSD
  を PNG に効率的に変換する方法を示します。
keywords:
- save psd as png
- convert psd to png
- Aspose.PSD Java
linktitle: テキストレイヤーで異なる色の文字を描画する
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PSD as PNG with colored text using Aspose.PSD for
    Java. This step‑by‑step guide shows how to convert PSD to PNG efficiently.
  headline: Save PSD as PNG with Colored Text using Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is primarily designed for Java, but Aspose provides similar
      libraries for various programming languages.
    question: Can I use Aspose.PSD for Java with other programming languages?
  - answer: Yes, you can obtain a free trial version from [Aspose.PSD](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: Where can I find additional support or assistance?
  - answer: You can request a temporary license from [Aspose.PSD](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Yes, explore the [Aspose.PSD documentation](https://reference.aspose.com/psd/java/)
      for more tutorials and examples.
    question: Are there other tutorials available for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して、カラー文字付きの PSD を PNG に保存
url: /ja/java/advanced-techniques/render-text-different-colors/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用して、カラー文字付きで PSD を PNG に保存する

Welcome to our step‑by‑step guide on how to **save PSD as PNG** with different colored text using Aspose.PSD for Java. Aspose.PSD is a powerful Java library that allows you to manipulate Photoshop files programmatically, providing you with extensive capabilities to work with PSD and PSB file formats.

In this tutorial, we'll walk you through the process of rendering text with various colors in a text layer using Aspose.PSD. By the end of this guide, you'll have a clear understanding of how to achieve this task seamlessly.

## クイック回答
- **PSD を PNG として保存する方法は？** Aspose.PSD の `PsdImage` クラスを使用して PSD をロードし、`PngOptions` を指定して `save` を呼び出します。  
- **1 つのテキストレイヤーで複数の色をレンダリングできますか？** はい、テキストの各 `Portion` に異なる `Color` オブジェクトを割り当てます。  
- **必要な Java バージョンは？** Java 8 以上がサポートされています。  
- **本番環境でライセンスは必要ですか？** 商用ライセンスが必要です。無料トライアルも利用可能です。  
- **大容量ファイルでもメモリ効率は良いですか？** フルメモリロードなしで最大 2 GB のファイルを処理できます。

## カラー文字付きで PSD を PNG に保存する方法

Load your PSD file, modify the text layer’s portions to assign distinct colors, and then save the image as PNG—this whole workflow is performed in just a few lines of Java code. Aspose.PSD automatically rasterizes the edited layer, preserving transparency and color fidelity, so the resulting PNG matches the original design.

## Aspose.PSD for Java とは？

Aspose.PSD for Java is a library that enables programmatic creation, editing, and conversion of Photoshop (PSD/PSB) files. It supports **50+ image formats** and can process multi‑hundred‑page documents without loading the entire file into memory, delivering high performance for server‑side automation.

## 前提条件

- Java プログラミングの基本的な知識。  
- Aspose.PSD for Java ライブラリがインストール済みです。ダウンロードは [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) から行えます。

## パッケージのインポート

`Image` is the base class for loading and saving image files. `PsdImage` represents a Photoshop document, while `TextLayer` provides access to text layer properties. `PngOptions` defines settings for PNG export.  
```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## 手順 1: プロジェクトのセットアップ

Create a new Java project and include the Aspose.PSD library. Make sure you have the necessary permissions to access and modify files in your project directory.

## 手順 2: ソースおよび出力ディレクトリの定義

Specify the source and output directories where your PSD files are located and where the resulting images will be saved. Update the `sourceDir` and `outputDir` variables accordingly.  
```java
String sourceDir = "Your Document Directory";
String outputDir = "Your Document Directory";
```

## 手順 3: PSD ファイルのロードとテキストレイヤーへのアクセス

`PsdImage` loads a PSD file into memory, and `TextLayer` allows manipulation of the text content within that layer.  
```java
String targetFilePath = sourceDir + "text_ethalon_different_colors.psd";
String resultFilePath = outputDir + "RenderTextWithDifferentColorsInTextLayer_out.png";

PsdImage psdImage = null;
try
{
    psdImage = (PsdImage) Image.load(targetFilePath);
    TextLayer txtLayer = (TextLayer)psdImage.getLayers()[1];
    txtLayer.getTextData().updateLayerData();
```

## 手順 4: PNG オプションの設定と画像の保存

`PngOptions` configures the PNG output parameters such as color type and compression.  
```java
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
    psdImage.save(resultFilePath, pngOptions);
}
finally
{
    if (psdImage != null) psdImage.dispose();
}
```

## よくある問題と解決策

- **Missing license exception:** Ensure you have applied a valid license file before calling any save operation.  
- **Color not applied:** Verify that each `Portion` in the text layer has its `Color` property set correctly.  
- **Large file memory usage:** Use `PsdImage`'s `load` overload with `loadOptions` to stream large files.

## よくある質問

**Q: Aspose.PSD for Java を他のプログラミング言語と併用できますか？**  
A: Aspose.PSD は主に Java 用に設計されていますが、Aspose はさまざまなプログラミング言語向けに同様のライブラリを提供しています。

**Q: Aspose.PSD for Java のトライアル版はありますか？**  
A: はい、無料トライアル版は [Aspose.PSD](https://releases.aspose.com/) から入手できます。

**Q: 追加のサポートや支援はどこで得られますか？**  
A: コミュニティサポートやディスカッションは [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) をご覧ください。

**Q: Aspose.PSD for Java の一時ライセンスはどう取得できますか？**  
A: 一時ライセンスは [Aspose.PSD](https://purchase.aspose.com/temporary-license/) からリクエストできます。

**Q: 他に Aspose.PSD のチュートリアルはありますか？**  
A: はい、[Aspose.PSD documentation](https://reference.aspose.com/psd/java/) でさらに多くのチュートリアルやサンプルをご確認ください。

**Q: 複数の PSD ファイルをバッチで PNG に変換することは可能ですか？**  
A: はい、フォルダー内の PSD ファイルをループで処理し、同じテキストカラーのロジックを適用して PNG として保存できます。

**Q: 出力される PNG はロスレスですか？**  
A: Aspose.PSD で保存された PNG は完全なロスレス品質を保持し、すべての色と透過情報を保持します。

---

**最終更新日:** 2026-05-29  
**テスト環境:** Aspose.PSD 24.12 for Java  
**作者:** Aspose

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [Aspose.PSD for Java を使用して PSD を PNG にエクスポートし、新しいレギュラーレイヤーを追加する](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Aspose.PSD for Java で PSD を PNG に保存し、レンダリングドロップシャドウを適用する](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Aspose.PSD for Java でカラーオーバーレイ付きで PSD を PNG に変換する](/psd/java/advanced-image-manipulation/rendering-color-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}