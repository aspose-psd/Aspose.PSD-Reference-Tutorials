---
date: 2026-04-28
description: Aspose.PSD for Java を使用してキャンバス上に画像を描画し、画像に署名を追加する方法を学びます。この Java 画像処理チュートリアルでは、画像を
  PNG として保存し、グラフィックをオーバーレイする方法を示します。
keywords:
- add signature to image
- draw image on canvas
- save image as png
- java image processing
- add watermark java
linktitle: 画像に署名を追加する
second_title: Aspose.PSD Java API
title: 画像に署名を追加 – Aspose.PSD for Javaでキャンバスに画像を描画
url: /ja/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 画像に署名を追加 – Aspose.PSD for Javaでキャンバスに画像を描画

## はじめに

手書きまたはデジタルの **add signature to image** を追加することは、契約書、請求書、または真正性の証明が必要なあらゆる文書で一般的な要件です。このチュートリアルでは、Aspose.PSD for Java が **draw image on canvas** を可能にし、署名を別のオーバーレイレイヤーとして扱う方法を示します。ベース画像の読み込み、署名ファイルの読み込み、Graphics コンテキストの初期化、オーバーレイの描画、そして最終的に **save image as PNG** までの手順を解説します。最後には、**java image processing** のシナリオ全般（署名、透かし、ロゴなど）で再利用できるパターンが手に入ります。

## クイック回答
- **draw image on canvas とは何ですか？** `Graphics` クラスを使用して、ある画像を別の画像にレンダリングすることを指します。  
- **Java で署名を追加する方法は？** 署名ファイルを `Image` としてロードし、`Graphics.drawImage` を使用します。  
- **必要な Aspose.PSD のバージョンは？** 最近の 24.x リリースであればどれでも構いません。コードは最新のライブラリでも動作します。  
- **複数の画像をオーバーレイできますか？** はい—異なるソースで `drawImage` 呼び出しを繰り返すだけです。  
- **ライセンスは必要ですか？** 開発にはトライアルで動作しますが、本番環境では商用ライセンスが必要です。

## “draw image on canvas” とは何か？
Aspose.PSD の用語では、キャンバスに画像を描画することは、`Graphics` コンテキストを使用してある `Image` オブジェクトを別の `Image` にペイントすることを意味します。この操作は、**overlay images java** のような透かし、ロゴ、署名の追加技術の基盤です。

## 署名のオーバーレイに Aspose.PSD を使用する理由
- **Full PSD support** – レイヤー、マスク、透過性を扱えます。  
- **No native OS dependencies** – 純粋な Java で、サーバーサイド処理に最適です。  
- **High‑performance rendering** – 大容量ファイルや複雑な構成に最適化されています。  

## 前提条件
- Java Development Kit (JDK) 8 以上。  
- プロジェクトのクラスパスに Aspose.PSD for Java の JAR を追加します。  
- 2 つの画像ファイル：ベース画像（例: `layers.psd`）と署名画像（`sample.psd`）。  

## パッケージのインポート

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## 手順 1: 主画像と副画像の読み込み

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **プロのコツ:** 描画時の予期せぬ色変化を防ぐため、両方の画像を同じカラーモード（RGB）に保ってください。

## 手順 2: Graphics の初期化 (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics` オブジェクトは、**draw image on canvas** を可能にするペイントブラシのようなものです。これを主 `Image` で初期化することで、以降のすべての描画コマンドがそのキャンバスに結び付けられます。

## 手順 3: 画像に署名を追加 (how to add signature)

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

このスニペットでは、署名を右下隅に配置して **overlay images java** を実行しています。別の位置が必要な場合は `Point` の値を調整してください。

## よくある問題と解決策

| 症状 | 原因 | 対策 |
|------|------|------|
| 署名が歪んで表示される | キャンバスと署名の DPI が一致していない | 描画前に `signature.resize` を使用するか、両ファイルが同じ DPI であることを確認してください。 |
| 出力ファイルが巨大になる | 圧縮なしで保存している | `CompressionLevel` を高めに設定した `PngOptions` を渡してください。 |
| 描画されない | Graphics が破棄されていない | 描画後に `graphics.dispose()` を呼び出してください（任意ですが推奨）。 |

## 実務での追加ヒント

- **Multiple signatures:** 異なる `Image` オブジェクトと座標で `graphics.drawImage` を繰り返し呼び出します。  
- **Opacity control:** 描画前に `graphics.setOpacity(float opacity)` を使用して署名を半透明にします。  
- **Rotating the signature:** 斜めの署名が必要な場合は `graphics.rotateTransform(angle)` を適用します。  
- **Saving to other formats:** `PngOptions` を `JpegOptions` や `BmpOptions` に置き換えて JPEG、BMP などで出力します。

## よくある質問

### Q1: 画像に複数の署名を追加できますか？

A1: はい、異なる署名画像で手順を繰り返すことで複数の署名を追加できます。

### Q2: Aspose.PSD は他の画像形式をサポートしていますか？

A2: はい、Aspose.PSD は幅広い画像形式をサポートしており、画像処理の柔軟性を確保します。

### Q3: Java 用 Aspose.PSD の使用にライセンスは必要ですか？

A3: はい、Aspose.PSD を使用するには有効なライセンスが必要です。ライセンスの詳細は [Purchase Aspose.PSD](https://purchase.aspose.com/buy) をご覧ください。

### Q4: Aspose.PSD のサポートはどのように受けられますか？

A4: コミュニティサポートやディスカッションは [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) をご利用ください。

### Q5: 購入前に Aspose.PSD for Java を試せますか？

A5: はい、購入前に機能を確認できる [free trial](https://releases.aspose.com/) を取得できます。

**追加の FAQ**

**Q: 署名の不透明度を変更するには？**  
A: `drawImage` を呼び出す前に `graphics.setOpacity(float opacity)` を使用します。値は 0.0（透明）から 1.0（不透明）までです。

**Q: 署名を回転させることは可能ですか？**  
A: はい—描画前に `graphics.rotateTransform(angle)` で変換行列を適用します。

**Q: PNG ではなく JPEG に署名を描画できますか？**  
A: もちろんです。`PngOptions` を `JpegOptions` に置き換え、希望の品質レベルを指定してください。

## 結論

これらの手順に従うことで、Aspose.PSD for Java を使用して **draw image on canvas** により **add signature to image** を行う方法を習得しました。同じパターンは透かし、ロゴ、その他のオーバーレイ画像にも拡張でき、Java アプリケーションに強力な **java image processing** 機能を提供します。

---

**最終更新日:** 2026-04-28  
**テスト環境:** Aspose.PSD for Java 24.11  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}