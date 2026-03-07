---
date: 2026-03-07
description: Aspose.PSD for Java を使用して PSD ファイルに画像ウォーターマークを作成する方法を学びましょう – PSD 画像処理とグラフィック保護のための簡単ガイドです。
linktitle: How to Create Image Watermark in PSD Files with Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して PSD ファイルに画像ウォーターマークを作成する方法
url: /ja/java/modifying-converting-psd-images/add-watermark-psd-files/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用して PSD ファイルに透かしを追加する

## Introduction
透かしは画像を保護し、所有権を示すさりげないが効果的な方法です。このチュートリアルでは、Aspose.PSD for Java を使用して PSD ファイルに **create image watermark** を作成する方法を学びます。ポートフォリオを披露する写真家や最新作品を提示するデザイナーにとって、透かしの追加はブランドアイデンティティを維持する上で重要です。さあ、コーヒーを一杯用意してリラックスし、始めましょう！

## Quick Answers
- **What is the primary goal?** プログラムで PSD ファイルに画像透かしを作成することです。  
- **Which library is used?** Aspose.PSD for Java。  
- **How long does implementation take?** 基本的な透かしでおおよそ 10‑15 分です。  
- **What are the main prerequisites?** Java JDK、Aspose.PSD ライブラリ、そしてソース PSD ファイル。  
- **Can I export the result as PNG?** はい – `save` メソッドに `PngOptions` を使用します。

## What is **create image watermark**?
画像透かしを作成することは、所有権情報を画像コンテンツに直接埋め込むために、半透明のテキストやグラフィックをプログラムでオーバーレイすることを指します。

## Why use Aspose.PSD for Java for psd image processing?
Aspose.PSD は **psd image processing** 用の豊富な API を提供し、レイヤー操作、エフェクト適用、最終画像のレンダリングを Photoshop がなくても実現できます。高忠実度のレンダリング、バッチ処理、主要な OS すべてで動作する点が特徴です。

## Prerequisites
コードに取り掛かる前に、以下を用意してください。

1. **Java Development Kit (JDK)** – 最近のバージョン (8 以上)。  
2. **Aspose.PSD for Java Library** – [Aspose website](https://releases.aspose.com/psd/java/) からダウンロード。  
3. **IDE** – Eclipse、IntelliJ IDEA、またはお好みのエディタ。  
4. **PSD File** – 作業ディレクトリに配置した `layers.psd` というサンプルファイル。  
5. **Basic Java knowledge** – クラス、オブジェクト、ファイル I/O の基本知識。

## Import Packages
環境が整ったので、必要なパッケージをインポートしましょう。Java のインポートは外部ライブラリのクラスや機能を利用できるようにするものです。以下が必要なインポートです。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## How to **create image watermark** – Step‑by‑Step Guide

### Step 1: Set Up Your Directory
まずは PSD ファイルが存在するパスを設定します。Java がファイルの場所を正しく認識するために重要です。

```java
String dataDir = "Your Document Directory";
```

`Your Document Directory` を `layers.psd` が格納されている実際のフォルダーに置き換えてください。

### Step 2: Load the PSD File
次に PSD ファイルを読み込み、`PsdImage` にキャストします。このステップでファイルを操作可能な形式に変換します。

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

本を開いてページに書き込むイメージです。

### Step 3: Create a Graphics Object
PSD ファイルがロードされたら、`Graphics` オブジェクトを作成します。これにより描画操作が可能になり、キャンバスにペイントブラシを持つような感覚です。

```java
Graphics graphics = new Graphics(psdImage);
```

### Step 4: Define the Font for Your Watermark
透かしの見た目を決めます。ここでは Arial、フォントサイズ 20 を使用します。フォント名やサイズはブランドに合わせて自由に変更してください。

```java
Font font = new Font("Arial", 20.0f);
```

### Step 5: Create a Solid Brush for Watermarking
ソリッドブラシは透かしの色と不透明度を決定します。ここではアルファ値を 50（255 中）に設定し、半透明のグレーにします。

```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```

ここで `Color.fromArgb(50, 128, 128, 128)` は 50% の不透明度を持つグレー色を生成します – 微妙な署名に最適です。

### Step 6: Set String Alignment for Your Watermark
透かしを画像の中心に配置するため、文字列の配置オプションを設定します。

```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
sf.setLineAlignment(StringAlignment.Center);
```

### Step 7: Draw the Watermark Using **java graphics drawstring**
いよいよ本番です。Graphics コンテキストが準備できたら、`java graphics drawstring` を使って透かしテキストを画像に描画します。

```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, 0, psdImage.getWidth(), psdImage.getHeight()), sf);
```

`"Some watermark text"` を実際に PSD に表示したいテキストに置き換えてください。

### Step 8: **Save PSD as PNG** – **export psd png**
透かしが配置されたら、**save psd png**（つまり PSD を PNG にエクスポート）して、任意のブラウザや画像ビューアで確認できるようにします。

```java
psdImage.save(dataDir + "AddWatermark_output.png", new PngOptions());
```

この行を実行すると、透かしが入った新しい PNG ファイルが作成されます。

## Common Issues and Solutions
- **Watermark not visible?** `Color.fromArgb()` のアルファ値を確認してください。値が低いほど透かしは透明になります。  
- **Incorrect dimensions?** 矩形のサイズに `psdImage.getWidth()` と `psdImage.getHeight()` を使用し、テキストが画像サイズに合わせてスケールするようにしてください。  
- **License exceptions?** 評価ライセンスはテストに使用できますが、本番環境では正式ライセンスが必要です。

## Frequently Asked Questions

**Q: Can I customize the watermark text?**  
A: もちろんです！`drawString` メソッド内の文字列を希望のテキストに置き換えるだけです。

**Q: What if I want a different font?**  
A: `Font` のインスタンス化を任意のインストール済みフォントに変更してください。例: `new Font("Times New Roman", 24.0f)`。

**Q: Is there a way to adjust opacity?**  
A: はい – `Color.fromArgb(alpha, r, g, b)` の最初のパラメータを変更します。`alpha` が低いほど透明度が高くなります。

**Q: Can I use other image formats besides PNG?**  
A: もちろんです。`new PngOptions()` を `new JpegOptions()` や `new BmpOptions()` に置き換えて、**save psd png** を別の形式で保存できます。

**Q: Where can I find more help?**  
A: 詳細な質問は [Aspose forums](https://forum.aspose.com/c/psd/34) または公式 [documentation](https://reference.aspose.com/psd/java/) をご覧ください。

## Conclusion
これで Aspose.PSD for Java を使用して PSD ファイルに **create image watermark** を作成する方法を習得しました。この手法はコンテンツを保護するだけでなく、すべてのビジュアル資産におけるブランドプレゼンスを強化します。フォント、色、不透明度を自由に組み合わせてスタイルに合わせ、**save psd png** や **export psd png** で必要な形式にエクスポートできることを覚えておいてください。

---

**Last Updated:** 2026-03-07  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}