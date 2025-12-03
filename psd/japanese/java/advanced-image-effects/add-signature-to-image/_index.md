---
date: 2025-12-02
description: Aspose.PSD を使用して Java でキャンバスに画像を描画し、署名をオーバーレイする方法を学びましょう。このステップバイステップの
  Java 画像処理チュートリアルに従い、結果を PNG として保存します。
language: ja
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: キャンバス上に画像を描く – Aspose.PSD for Javaで署名を追加
url: /java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Canvasに画像を描画 – Aspose.PSD for Javaで署名を追加

## Introduction

手書きまたはデジタル署名を画像に追加することは、契約書、請求書、または真正性の証明が必要なあらゆる文書で頻繁に求められます。**Aspose.PSD for Java** を使用すれば **draw image on canvas** が可能になり、署名を単なるオーバーレイレイヤーとして扱うことができます。この **java image processing tutorial** では、ベース画像と署名ファイルの読み込み、Graphics の初期化、オーバーレイの描画、そして最終的に **save image png java** 形式で保存するまでの全工程を解説します。

## Quick Answers
- **“draw image on canvas” とは何ですか？** `Graphics` クラスを使用して、ある画像を別の画像上に描画することを指します。  
- **Java で署名を追加する方法は？** 署名ファイルを `Image` として読み込み、`Graphics.drawImage` を使用します。  
- **必要な Aspose.PSD のバージョンは？** 最新の 24.x 系リリースであれば問題なく動作します。  
- **複数の画像をオーバーレイできますか？** はい、異なるソースで `drawImage` を繰り返し呼び出すだけです。  
- **ライセンスは必要ですか？** 開発段階ではトライアルで動作しますが、本番環境では商用ライセンスが必要です。

## What Is “Draw Image on Canvas”?
Aspose.PSD の用語では、画像をキャンバスに描画することは、`Graphics` コンテキストを介してある `Image` オブジェクトを別の `Image` にペイントすることを意味します。この操作は、ウォーターマーク、ロゴ、署名などの **overlay images java** 技術の基盤となります。

## Why Use Aspose.PSD for Overlaying a Signature?
- **Full PSD support** – レイヤー、マスク、透過性をフルに扱えます。  
- **No native OS dependencies** – 純粋な Java 実装で、サーバーサイド処理に最適です。  
- **High‑performance rendering** – 大容量ファイルや複雑な構成でも高速にレンダリングできます。  

## Prerequisites
- Java Development Kit (JDK) 8 以上。  
- プロジェクトのクラスパスに Aspose.PSD for Java の JAR を追加。  
- 2 つの画像ファイル：ベース画像（例: `layers.psd`）と署名画像（`sample.psd`）。  

## Import Packages

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Load Primary and Secondary Images

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** 描画時の予期せぬ色変化を防ぐため、両方の画像を同じカラーモード (RGB) に統一してください。

## Step 2: Initialize Graphics (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics` オブジェクトは、**draw image on canvas** を実現するためのペイントブラシのようなものです。プライマリ `Image` に対して初期化することで、以降のすべての描画コマンドがそのキャンバスに対して行われます。

## Step 3: Add Signature to Image (how to add signature)

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

このコードスニペットでは、署名を画像の右下隅に配置して **overlay images java** を実現しています。別の位置にしたい場合は `Point` の値を調整してください。

## Common Issues & Solutions
| Symptom | Cause | Fix |
|---------|-------|-----|
| 署名が歪んで表示される | キャンバスと署名の DPI が一致していない | 描画前に `signature.resize` を使用するか、両ファイルの DPI を統一してください。 |
| 出力ファイルが巨大になる | 圧縮なしで保存している | `CompressionLevel` を高めた `PngOptions` を設定して保存してください。 |
| 描画が全く行われない | Graphics が破棄されていない | 描画後に `graphics.dispose()` を呼び出してください（省略可能ですが推奨）。 |

## Conclusion

本手順に従うことで、**draw image on canvas** の方法と Aspose.PSD for Java を用いた **署名の追加** 方法を習得できました。このテクニックはウォーターマークやロゴなど、任意のオーバーレイ画像にも応用でき、Java アプリケーションに強力な **java image processing** 機能を提供します。

## FAQ's

### Q1: 画像に複数の署名を追加できますか？

A1: はい、異なる署名画像を使用して手順を繰り返すことで複数の署名を追加できます。

### Q2: Aspose.PSD は他の画像形式もサポートしていますか？

A2: はい、Aspose.PSD は幅広い画像形式に対応しており、柔軟な画像処理が可能です。

### Q3: Aspose.PSD for Java の使用にライセンスは必要ですか？

A3: はい、Aspose.PSD の使用には有効なライセンスが必要です。ライセンスの詳細は [Purchase Aspose.PSD](https://purchase.aspose.com/buy) をご覧ください。

### Q4: Aspose.PSD のサポートはどこで受けられますか？

A4: コミュニティサポートやディスカッションは [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) で提供されています。

### Q5: 購入前に Aspose.PSD for Java を試すことはできますか？

A5: はい、[free trial](https://releases.aspose.com/) で機能を確認した上で購入をご検討いただけます。

## Additional Frequently Asked Questions

**Q: 署名の不透明度を変更するには？**  
A: `drawImage` を呼び出す前に `graphics.setOpacity(float opacity)` を使用します。値は 0.0（完全に透明）から 1.0（完全に不透明）までです。

**Q: 署名を回転させることは可能ですか？**  
A: はい、描画前に `graphics.rotateTransform(angle)` で変換行列を適用してください。

**Q: PNG ではなく JPEG に署名を描画できますか？**  
A: もちろん可能です。`PngOptions` を `JpegOptions` に置き換え、希望の品質レベルを指定してください。

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}