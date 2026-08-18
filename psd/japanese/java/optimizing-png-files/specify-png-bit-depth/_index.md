---
date: 2026-03-18
description: Aspose.PSD for Java を使用して、psd を png に変換しながら png のビット深度を変更する方法を学ぶ – コードサンプル付きのステップバイステップガイド
linktitle: Specify PNG Bit Depth in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して、指定したビット深度で PSD を PNG に変換する方法
url: /ja/java/optimizing-png-files/specify-png-bit-depth/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用した、指定ビット深度での PSD から PNG への変換

## Introduction
**psd を png に変換**し、正確な PNG ビット深度を制御したい場合は、ここが最適です。このチュートリアルでは、Aspose.PSD for Java を使用して PSD ファイルを PNG 画像として保存する際に、png のビット深度を変更する方法を解説します。バッチ処理ツール、Web サービス、デスクトップユーティリティのいずれを構築する場合でも、**grayscale カラータイプ**やカスタムビット深度などの **save png with options** が可能になり、画像品質とファイルサイズを細かくコントロールできます。

## Quick Answers
- **PNG のビット深度を変更できますか？** はい – `PngOptions.setBitDepth()` を使用して 1、2、4、8、または 16 ビットを指定できます。  
- **サポートされているカラータイプは？** Grayscale、TrueColor、Indexed など、`PngColorType` で指定可能です。  
- **Aspose.PSD のライセンスは必要ですか？** 開発目的であれば無料トライアルで動作します。商用環境では商用ライセンスが必要です。  
- **必要な Java バージョンは？** Java 8+（ライブラリは新しい JDK でも互換性があります）。  
- **コードはそのまま実行できますか？** はい – プレースホルダーのパスをご自身のフォルダーに置き換えるだけです。

## What is “convert psd to png” with custom bit depth?
Photoshop の PSD ファイルを PNG 画像に変換するのは、Web フレンドリーな形式が必要なときに一般的な作業です。**png quality を調整**するためにビット深度を設定できれば、視覚的忠実度とファイルサイズのバランスを取ることができ、サムネイルやアイコン、帯域幅が制限されている環境で特に有用です。

## Why use Aspose.PSD for Java?
Aspose.PSD for Java は、PSD フォーマットの複雑さを抽象化したハイレベル API を提供します。**create grayscale png**、**save png with options**、カラー プロファイルの処理を低レベルのバイト操作なしで実現できます。ライブラリは完全にマネージドでクロスプラットフォーム、定期的にアップデートが提供されます。

## Prerequisites
コードに入る前に、以下を用意してください。

1. **Java Development Kit (JDK)** – [Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) からダウンロード。  
2. **Aspose.PSD for Java** – [このリンク](https://releases.aspose.com/psd/java/) から最新の JAR を取得。  
3. **Basic Java knowledge** – クラス、メソッド、例外処理に慣れていること。  
4. **IDE** – IntelliJ IDEA や Eclipse など（任意ですが推奨）。  
5. **サンプル PSD ファイル** – コードで参照するフォルダーに配置。

すべて揃いましたか？では、必要なパッケージをインポートしましょう。

## Import Packages
前提条件が整ったので、Java アプリケーションで使用するパッケージをインポートして環境を整えます。Java ファイルの先頭に以下のインポート文を追加してください。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

これらのステートメントは、チュートリアル全体で使用するクラスをインポートし、PSD ファイルの読み込みや指定ビット深度での PNG 変換を可能にします。

## Step 1: Set Up Your Document Directory
画像を処理する前に、画像を保存するディレクトリを定義します。これは、工作プロジェクトで材料を入れる箱を用意するようなものです。

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load the PSD Image
次に、変換したい PSD 画像ファイルをロードします。これは、作業を始めるためにキャンバスを開くイメージです。

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

ここでは `Image.load()` メソッドを使用してサンプル PSD ファイルを読み込み、`PsdImage` にキャストして PSD 固有のプロパティにアクセスしています。

## Step 3: Create PNG Options
キャンバスが開いたら、画像を保存する際のオプションを設定します。これは、絵を描く前に色や筆のスタイルを選ぶようなものです。

```java
PngOptions options = new PngOptions();
```

このステップでは `PngOptions` のインスタンスを初期化し、PNG 出力のパラメータを指定できるようにします。

## Step 4: Set the Desired Color Type
最終的な PNG 画像で使用するカラータイプを決めます。カラフルなパレットにするか、モノクロにするかを選択します。

```java
options.setColorType(PngColorType.Grayscale);
```

この例ではカラータイプを grayscale に設定しています。フルカラー画像が必要な場合は `PngColorType.TrueColor` を選択できます。ここが **create grayscale png** のポイントです。

## Step 5: Specify the Bit Depth
次にビット深度を指定します。これは、プリンターに「どれだけ細かく印刷するか」を指示するようなものです – ビット数が多いほど細部が表現されます。

```java
options.setBitDepth((byte)1);
```

ここでは **1 bit** のビット深度を設定しています。シンプルなグレースケール画像に適しています。品質要件に応じて 2、4、8、または 16 に変更可能で、これが **change png bit depth** の典型的な使用例です。

## Step 6: Save the PNG Image
最後に作品を保存します！このステップで、編集キャンバスからギャラリーの壁へ作品を転送します。

```java
psdImage.save(dataDir + "SpecifyBitDepth_out.png", options);
```

`PsdImage` の `save()` メソッドを使用し、先ほど定義したオプションを適用して変換ファイルを保存します。これでカスタムビット深度の PNG が完成です。

## Common Issues and Solutions
- **`NullPointerException` が PSD のロード時に発生** – `dataDir` が正しいフォルダーを指しているか、`sample.psd` が存在するかを再確認してください。  
- **サポート外のビット深度** – Aspose.PSD は PNG に対して 1、2、4、8、16 ビットをサポートしています。それ以外の値を使用すると `IllegalArgumentException` がスローされます。  
- **カラータイプの不一致** – 選択した `PngColorType` と互換性のないビット深度を設定した場合、ライブラリは自動的に最も近いサポート設定に調整します。

## Frequently Asked Questions

**Q: Aspose.PSD for Java とは何ですか？**  
A: Aspose.PSD for Java は、Java アプリケーションで PSD ファイルを操作・変換できるライブラリです。

**Q: ビット深度はどのように指定しますか？**  
A: `options.setBitDepth((byte)n)` メソッドでビット深度を設定します。`n` には希望の深度を入力してください。

**Q: Aspose.PSD は無料で使えますか？**  
A: はい、無料トライアル版を利用できます。ダウンロードは [here](https://releases.aspose.com/) から。

**Q: Aspose のサポートライセンスはどこで取得できますか？**  
A: 一時ライセンスは [here](https://purchase.aspose.com/temporary-license/) から申し込めます。

**Q: どのような画像形式を変換できますか？**  
A: 主に PSD ファイルを扱いますが、PNG、JPEG、TIFF など多数の形式へ変換可能です。

## Conclusion
Aspose.PSD for Java を使用して、PNG のビット深度を制御しながら **psd を png に変換**する方法を学びました。`PngOptions` を調整すれば **adjust png quality**、**create grayscale png** が可能になり、あらゆるシナリオでファイルサイズと画質のバランスを最適化できます。さまざまなカラータイプとビット深度を試して、アプリケーションに最適な設定を見つけてください。

---

**Last Updated:** 2026-03-18  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}