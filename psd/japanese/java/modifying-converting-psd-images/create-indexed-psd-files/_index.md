---
date: 2026-03-15
description: このステップバイステップガイドで、Aspose.PSD for Java を使用して PSD ファイルの作成方法、PSD カラーパレットの生成方法、そして
  PSD カラーモードの設定方法を学びましょう。
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して PSD ファイルを作成する方法
url: /ja/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用して PSD ファイルを作成する方法

## Introduction
プログラムで **PSD を作成する方法** を知りたかったことはありませんか？Aspose.PSD for Java を使えば、Photoshop ドキュメントを完全に制御でき、Photoshop を開くことなく PSD ファイルの生成、編集、保存が可能です。このチュートリアルでは、**インデックス化された PSD** ファイルの作成、PSD カラーモードの設定、カスタムカラーパレットの生成を、分かりやすいステップバイステップの Java コードとともに解説します。グラフィックパイプラインの構築、アセット作成の自動化、あるいは単なる実験など、ここで紹介する概念はビジュアルアイデアを形にするのに役立ちます。

## Quick Answers
- **必要なライブラリは？** Aspose.PSD for Java  
- **インデックス化された PSD を作成できるか？** はい、カラーモードを `Indexed` に設定すれば可能です  
- **Photoshop のインストールは必要か？** いいえ、Aspose.PSD は単独で動作します  
- **必要な Java バージョンは？** JDK 8 以降  
- **キャンバスの最大サイズは？** 任意のサイズです。本例では 500 × 500 px を使用しています  

## What is an Indexed PSD File?
インデックス化された PSD は、各ピクセルのフルカラー値ではなくパレット内の色インデックスで色を表現します。これによりファイルサイズが削減され、アイコンや UI アセットなど色数が限られたグラフィックに最適です。カスタムパレットを生成することで、最終画像に使用される色を正確にコントロールできます。

## Why Generate a PSD Color Palette?
**PSD カラーパレット** を作成すると、次のようなメリットがあります。  
- ウェブやモバイル向けにファイルサイズを小さく保てる  
- 企業のブランドカラーに限定することで一貫性を確保できる  
- インデックス画像をサポートするアプリケーションでの描画速度が向上する  

## Prerequisites
コードに入る前に、以下の環境が整っていることを確認してください。

1. **Java の基本知識** – クラス、メソッド、オブジェクト生成に慣れていること。  
2. **Java Development Kit (JDK) 8 以上** – IDE に設定済みであること。  
3. **IDE (IntelliJ IDEA、Eclipse 等)** – 任意ですが、デバッグが楽になります。  
4. **Aspose.PSD for Java ライブラリ** – **[こちら](https://releases.aspose.com/psd/java/)** からダウンロードし、JAR をプロジェクトのクラスパスに追加してください。  
5. **基本的なグラフィックデザインの概念** – カラーモード、パレット、基本形状の理解があるとスムーズです。  

## Import Packages
コードを書く前に、必要なパッケージがすべてインポートされていることを確認しましょう。以下が必要なインポートです。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

これらのインポートにより、Aspose.PSD を通じて PSD オプション、カラー、グラフィック操作が可能になります。

それでは、**インデックスカラー モードで PSD を作成する方法** をステップバイステップで見ていきます。

## Step 1: Set Up Your Document Directory
まず、生成した PSD を保存する場所を定義します。

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` を絶対パスまたは相対パスに置き換えてください。例: `"/Users/YourName/Documents/"`  

## Step 2: Create an Instance of PsdOptions
`PsdOptions` は、これから作成するファイルの設定をすべて保持します。

```java
PsdOptions createOptions = new PsdOptions();
```

## Step 3: Set Core Properties of PsdOptions
ここでは出力先、**PSD カラーモード** を `Indexed` に設定し、PSD のバージョンを指定します。

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – 新規ファイルのフルパス。  
- **Color Mode** – `Indexed` を指定すると、Aspose.PSD がパレットベースの画像を生成します。  
- **Version** – PSD フォーマットのバージョン（5 がほとんどの最新 Photoshop で使用可能）。  

## Step 4: Create a Color Palette (Generate PSD Color Palette)
インデックス画像で使用できる色を定義します。

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- `palette` 配列は最大 256 個の `Color` オブジェクトを保持できます。  
- `CompressionMethod.RLE` はインデックス画像に対して効率的なロスレス圧縮を提供します。  

## Step 5: Create the PSD Image Canvas
次に、目的のサイズの空白 PSD キャンバスを作成します。

```java
Image psd = Image.create(createOptions, 500, 500);
```

これにより、先ほど定義したパレットを使用した 500 × 500 ピクセルのキャンバスが生成されます。

## Step 6: Draw Graphics on the PSD
ビジュアルコンテンツを追加します。ここでは白背景に赤い楕円を描画します。

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` で背景を白で塗りつぶします。  
- `drawEllipse` が 6 ピクセルのストローク幅で赤い楕円を描画します。  

## Step 7: Save the PSD File
最後に、画像をディスクに保存します。

```java
psd.save();
```

`Newsample_out.psd` というファイルが、先ほど指定したディレクトリに作成されます。

## Common Issues & Tips
- **パレットサイズ** – 4 色以上必要な場合は、`palette` 配列に色を追加してください（最大 256 色）。  
- **ファイル権限** – Java プロセスが `dataDir` に書き込み権限を持っていることを確認してください。  
- **カラーモードの指定忘れ** – `createOptions.setColorMode(ColorModes.Indexed)` を忘れると、RGB PSD が生成されてしまいます。  

## Frequently Asked Questions

**Q: Aspose.PSD for Java とは何ですか？**  
A: Aspose.PSD for Java は、Java から PSD（Photoshop）ファイルをプログラム的に操作できるライブラリです。

**Q: Aspose.PSD は無料で使えますか？**  
A: はい、**[こちら](https://releases.aspose.com/)** から無料トライアル版を入手できます。

**Q: Aspose.PSD を使用するのに Photoshop のインストールは必要ですか？**  
A: いいえ、Aspose.PSD は Photoshop に依存せず、単独で PSD の作成・操作が可能です。

**Q: Aspose.PSD の一時ライセンスはどこで取得できますか？**  
A: **[こちら](https://purchase.aspose.com/temporary-license/)** からリクエストできます。

**Q: Aspose.PSD のサポートはどこで受けられますか？**  
A: **[こちら](https://forum.aspose.com/c/psd/34)** の Aspose フォーラムでサポートを受けられます。

## Conclusion
インデックスカラー モードで **PSD を作成する方法** を学び、カスタムパレットを生成し、シンプルなグラフィックを描画する手順を習得しました。これらの基本ブロックを元に、より複雑な描画、レイヤー管理、バッチ処理へと拡張できます。さらに詳しくは公式 API リファレンス **[こちら](https://reference.aspose.com/psd/java/)** を参照し、さまざまなパレットや描画プリミティブで実験してみてください。

---

**Last Updated:** 2026-03-15  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}