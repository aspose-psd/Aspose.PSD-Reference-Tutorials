---
title: Aspose.PSD for Java の Resize Type Enumeration を使用したサイズ変更
linktitle: サイズ変更タイプ列挙型を使用したサイズ変更
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用した Java でのマスター イメージのサイズ変更。サイズ変更タイプ列挙を使用するステップバイステップのガイド。
type: docs
weight: 18
url: /ja/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
---
## 導入

進化し続ける Java 開発環境において、効率的な画像処理は、開発者がしばしば取り組む重要な側面です。 Aspose.PSD for Java は強力なソリューションとして登場し、Resize Type Enumeration の利点を加えて画像のサイズを変更するためのシームレスなエクスペリエンスを提供します。このチュートリアルでは、Aspose.PSD for Java を使用した画像のサイズ変更の複雑さを詳しく掘り下げ、包括的な理解を確実にするために各ステップに分けて説明します。

## 前提条件

このチュートリアルを開始する前に、次の前提条件が満たされていることを確認してください。

1. Java 開発環境: マシン上に Java 開発環境がセットアップされていることを確認します。

2. Aspose.PSD ライブラリ: Aspose.PSD ライブラリを次の場所からダウンロードしてインストールします。[Webサイト](https://releases.aspose.com/psd/java/).

3. サンプル PSD ファイル: 実験用にサンプル PSD ファイルを用意します。使用できます[このチュートリアルのサンプル.psd](ドキュメント ディレクトリ/sample.psd) ファイル。

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## ステップ 1: 画像をロードする

まず、既存のイメージをインスタンスにロードします。`RasterImage`クラス。次のコード スニペットを使用します。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//既存の画像を RasterImage クラスのインスタンスにロードします
Image image = Image.load(sourceFile);
```

## ステップ 2: 画像のサイズを変更する

ここで、Resize Type Enumeration を使用して、ロードされた画像のサイズを変更します。この例では、Lanczos Resample メソッドを使用します。

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## ステップ 3: サイズ変更した画像を保存する

サイズ変更後、指定した寸法と選択したサイズ変更タイプで画像を保存します。ここでは、JPEG ファイルとして保存します。

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

そして、それができました！ Aspose.PSD for Java の Resize Type Enumeration を使用して画像のサイズを正常に変更しました。

結論として、Aspose.PSD for Java は画像操作のための堅牢なプラットフォームを提供し、Resize Type Enumeration はこのプロセスに柔軟性のレイヤーを追加します。小規模なプロジェクトで作業している場合でも、大規模なアプリケーションで作業している場合でも、これらの手順をマスターすると、画像のサイズ変更をシームレスに処理できるようになります。

## よくある質問

### Q1: Aspose.PSD for Java は小規模プロジェクトと大規模プロジェクトの両方に適していますか?

A1: もちろんです！ Aspose.PSD for Java は、あらゆる規模のプロジェクトに対応できるように設計されており、スケーラビリティと効率性を提供します。

### Q2: Lanczos Resample 以外の別のサイズ変更タイプを使用できますか?

A2: はい、Aspose.PSD for Java では、最近傍、バイキュービックなど、さまざまなサイズ変更タイプが提供されています。包括的なリストについてはドキュメントを参照してください。

### Q3: Java 用 Aspose.PSD の追加サポートはどこで見つけられますか?

 A3: ご質問やサポートが必要な場合は、次のサイトにアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34).

### Q4: Aspose.PSD for Java の無料トライアルはありますか?

 A4: はい、無料試用版にアクセスできます。[ここ](https://releases.aspose.com/).

### Q5: Aspose.PSD for Java の一時ライセンスを取得するにはどうすればよいですか?

 A5: 一時ライセンスを取得するには、次のサイトにアクセスしてください。[このリンク](https://purchase.aspose.com/temporary-license/).