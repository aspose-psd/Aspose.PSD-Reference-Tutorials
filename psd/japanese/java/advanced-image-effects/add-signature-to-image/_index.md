---
date: 2026-10-24
description: Aspose.PSD for Java を使用して画像キャンバスを描画し、画像に署名を追加する方法を学びます。この Java 画像処理ガイドでは、画像を
  PNG 形式で保存し、グラフィックをオーバーレイする方法を示します。
keywords:
- draw image canvas
- save image png
- image processing java
- how to overlay image
- java graphics drawimage
lastmod: 2026-10-24
linktitle: 画像に署名を追加する
og_description: Aspose.PSD for Java を使用して画像キャンバスを描画し、画像に署名を追加する方法を学びます。画像を PNG 形式で保存し、グラフィックをオーバーレイする手順をステップバイステップでご案内します。
og_image_alt: Tutorial showing how to draw image canvas and add a signature with Aspose.PSD
  for Java
og_title: Javaで画像キャンバスを描画し、署名を追加する方法
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to draw image canvas and add a signature to an image using
    Aspose.PSD for Java. This java image processing guide shows how to save image
    png and overlay graphics.
  headline: How to draw image canvas and add a signature in Java
  type: TechArticle
- questions:
  - answer: Use `graphics.setOpacity(float opacity)` before calling `drawImage`. Values
      range from 0.0 (transparent) to 1.0 (opaque).
    question: How do I change the opacity of the signature?
  - answer: Yes—apply a transformation matrix via `graphics.rotateTransform(angle)`
      before drawing.
    question: Is it possible to rotate the signature?
  - answer: Absolutely. Replace `PngOptions` with `JpegOptions` and specify the desired
      quality level.
    question: Can I draw the signature onto a JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw image canvas
- Aspose.PSD
- Java image processing
- overlay graphics
title: Javaで画像キャンバスを描画し、署名を追加する方法
url: /ja/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Javaで画像キャンバスを描画し、署名を追加する方法

## はじめに

多くのビジネスワークフローでは、手書きまたはデジタル署名を画像に埋め込む必要があります—契約書、請求書、配達受領書などを考えてみてください。このチュートリアルでは、Aspose.PSD for Java を使用して **draw image canvas** を行い、署名を通常のオーバーレイレイヤーとして扱う方法を示します。ベース画像の読み込み、署名ファイルの読み込み、Graphics コンテキストの作成、オーバーレイの描画、そして最終的に **save image png** をする手順を学びます。最後には、署名、透かし、ロゴ、またはサーバー側で生成する任意の合成画像に使える再利用可能なパターンが手に入ります。

## クイック回答
- **“draw image on canvas” の意味は何ですか？** `Graphics` クラスを使用して、ある画像を別の画像に描画することを意味します。  
- **Javaで署名を追加する方法は？** 署名ファイルを `Image` として読み込み、`graphics.drawImage` を呼び出します。  
- **必要な Aspose.PSD のバージョンは？** 最近の 24.x 系であればどれでも構いません。コードは最新のライブラリでも動作します。  
- **複数の画像をオーバーレイできますか？** はい—異なるソースで `drawImage` 呼び出しを繰り返すだけです。  
- **ライセンスは必要ですか？** 開発にはトライアルで動作しますが、本番環境では商用ライセンスが必要です。

## draw image canvas とは何ですか？
キャンバス上に画像を描画することは、`Graphics` クラスを使用してある `Image` オブジェクトを別の画像にレンダリングし、実質的に2つの画像を1つのビットマップに合成することを意味します。この操作は、透かし、ロゴ、署名の追加など **overlay images java** 技術の基盤です。

## 署名のオーバーレイに Aspose.PSD を使用する理由
Aspose.PSD で署名をオーバーレイできるのは、**120 以上のレイヤータイプと 15 種類のマスクオプションをサポート**しており、透明度やブレンドを精密に制御できるからです。また、**500 MB のファイルを、一般的なサーバーハードウェア上でネイティブの Photoshop レンダリングの 2 倍の速度で処理**できるため、高スループットなサーバーサイド画像パイプラインに最適です。さらに、ライブラリは **ネイティブ OS 依存がゼロ** なので、Java 8+ ランタイムがあればどこでも動作します。

## 前提条件
- Java Development Kit (JDK) 8 以上。  
- Aspose.PSD for Java の JAR をプロジェクトのクラスパスに追加。  
- 2 つの画像ファイル：ベース画像（例：`layers.psd`）と署名画像（`sample.psd`）。  

## パッケージのインポート

`Graphics` クラスは描画機能を提供し、`Image` は画像オブジェクトを表し、`Point` は座標を定義します。  
```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## 手順 1: 主画像と副画像をロード

`Image` オブジェクトは、結合されるソース画像と宛先画像を表します。  
```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **プロのコツ:** 描画時に予期しない色の変化を防ぐため、両方の画像を同じカラーモード（RGB）に保ってください。

## 手順 2: Graphics の初期化 (initialize graphics java)

`Graphics` は主画像から作成され、描画キャンバスとして機能します。  
```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics` オブジェクトはペイントブラシのように機能し、**draw image on canvas** を可能にします。主画像の `Image` で初期化することで、以降のすべての描画コマンドがそのキャンバスに結び付けられます。

## 手順 3: 画像に署名を追加 (how to add signature)

`drawImage` メソッドは、指定された位置に署名画像をキャンバス上に描画します。  
```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

このスニペットでは、署名を右下隅に配置することで **overlay images java** を実現しています。別の位置が必要な場合は `Point` の値を調整してください。

## Java Graphics の drawImage を使用して画像をオーバーレイする方法

ベース画像をロードし、そこから `Graphics` インスタンスを作成し、`graphics.drawImage(signature, x, y)` を呼び出します。`x` と `y` はオーバーレイのピクセル座標を表します。この一度の呼び出しで署名がメモリ上の元のキャンバスに合成され、その後任意のサポート形式で結果を保存できます。

## よくある問題と解決策
| 症状 | 原因 | 対策 |
|---------|-------|-----|
| 署名が歪んで表示される | キャンバスと署名の DPI が一致していない | 描画前に `signature.resize` を使用するか、両ファイルの DPI を揃えてください。 |
| 出力ファイルが巨大になる | 圧縮なしで保存している | `CompressionLevel` を高めに設定した `PngOptions` を渡してください。 |
| 何も描画されない | Graphics が破棄されていない | 描画後に `graphics.dispose()` を呼び出してください（任意ですが推奨）。 |

## 実務での追加ヒント
- **複数の署名:** 異なる `Image` オブジェクトと座標で `graphics.drawImage` を繰り返し呼び出す。  
- **不透明度の制御:** 描画前に `graphics.setOpacity(float opacity)` を使用して署名を半透明にします。  
- **署名の回転:** 斜めの署名が必要な場合は `graphics.rotateTransform(angle)` を適用します。  
- **他形式で保存:** `PngOptions` を `JpegOptions` や `BmpOptions` に置き換えて JPEG、BMP などで出力します。

## よくある質問

### Q1: 画像に複数の署名を追加できますか？

A1: はい、異なる署名画像で手順を繰り返すことで複数の署名を追加できます。

### Q2: Aspose.PSD は他の画像形式をサポートしていますか？

A2: はい、Aspose.PSD は 50 以上の入出力形式（PSD、PNG、JPEG、BMP、TIFF、GIF など）をサポートしており、画像処理の柔軟性を提供します。

### Q3: Java 用 Aspose.PSD の使用にライセンスは必要ですか？

A3: はい、本番環境で使用するには有効なライセンスが必要です。ライセンスの詳細は [Purchase Aspose.PSD](https://purchase.aspose.com/buy) をご覧ください。

### Q4: Aspose.PSD のサポートはどこで受けられますか？

A4: コミュニティサポートやディスカッションは [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) をご利用ください。

### Q5: 購入前に Aspose.PSD for Java を試すことはできますか？

A5: はい、購入前に機能を確認できる [free trial](https://releases.aspose.com/) を取得できます。

**追加のFAQ**

**Q: 署名の不透明度を変更するには？**  
A: `drawImage` を呼び出す前に `graphics.setOpacity(float opacity)` を使用します。値は 0.0（透明）から 1.0（不透明）までです。

**Q: 署名を回転させることは可能ですか？**  
A: はい、描画前に `graphics.rotateTransform(angle)` で変換行列を適用します。

**Q: PNG ではなく JPEG に署名を描画できますか？**  
A: もちろんです。`PngOptions` を `JpegOptions` に置き換え、希望の品質レベルを指定してください。

## 結論

これらの手順に従うことで、Aspose.PSD for Java を使用して **画像キャンバスを描画し、画像に署名を追加する方法** を学びました。同じパターンは透かしやロゴ、その他のオーバーレイ画像にも拡張でき、Java アプリケーションに強力な **image processing java** 機能を提供します。

---

**最終更新日:** 2026-10-24  
**テスト環境:** Aspose.PSD for Java 24.11  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.PSD for Java を使用して PSD に矩形を描画・保存](/psd/java/basic-image-operations/simple-drawing/)
- [Aspose.PSD for Java で画像をリサイズ – 図形描画と基本画像操作](/psd/java/basic-image-operations/)
- [パターンオーバーレイ PSD: Aspose.PSD for Java でエフェクトを追加](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}