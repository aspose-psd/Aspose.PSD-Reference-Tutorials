---
title: Aspose.PSD for Java で Resize Type Enumeration を使用してサイズを変更する
linktitle: サイズ変更型列挙によるサイズ変更
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用して Java で画像のサイズ変更をマスターします。Resize Type Enumeration を使用したステップバイステップ ガイド。
type: docs
weight: 18
url: /ja/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
---
## 導入

進化し続ける Java 開発の分野では、効率的な画像処理は開発者がしばしば取り組む重要な側面です。Aspose.PSD for Java は、Resize Type Enumeration の利点を追加して、シームレスな画像サイズ変更エクスペリエンスを提供する強力なソリューションとして登場しました。このチュートリアルでは、Aspose.PSD for Java を使用して画像サイズ変更を行う複雑な部分を詳しく調べ、各ステップを分解して包括的な理解を確実にします。

## 前提条件

このチュートリアルを始める前に、次の前提条件が満たされていることを確認してください。

1. Java 開発環境: マシンに Java 開発環境が設定されていることを確認します。

2. Aspose.PSDライブラリ: Aspose.PSDライブラリを以下のサイトからダウンロードしてインストールします。[Webサイト](https://releases.aspose.com/psd/java/).

3. サンプルPSDファイル: 実験用にサンプルPSDファイルを用意します。[このチュートリアルでは、[sample.psd](ドキュメント ディレクトリ/sample.psd) ファイルを使用します。

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## ステップ1: 画像を読み込む

まず、既存の画像を`RasterImage`クラス。次のコード スニペットを使用します。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//既存の画像をRasterImageクラスのインスタンスに読み込みます
Image image = Image.load(sourceFile);
```

## ステップ2: 画像のサイズを変更する

次に、Resize Type Enumeration を使用して、読み込まれた画像のサイズを変更します。この例では、Lanczos Resample メソッドを使用します。

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## ステップ3: サイズ変更した画像を保存する

サイズ変更後、指定した寸法と選択したサイズ変更タイプで画像を保存します。ここでは、JPEG ファイルとして保存します。

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

これで完了です。Aspose.PSD for Java の Resize Type Enumeration を使用して、画像のサイズを正常に変更できました。

結論として、Aspose.PSD for Java は画像操作のための堅牢なプラットフォームを提供し、Resize Type Enumeration はこのプロセスに柔軟性を追加します。小規模なプロジェクトでも大規模なアプリケーションでも、これらの手順をマスターすれば、画像のサイズ変更をシームレスに処理できるようになります。

## よくある質問

### Q1: Aspose.PSD for Java は小規模プロジェクトと大規模プロジェクトの両方に適していますか?

A1: もちろんです! Aspose.PSD for Java は、あらゆる規模のプロジェクトに対応できるように設計されており、スケーラビリティと効率性を提供します。

### Q2: Lanczos Resample 以外のサイズ変更タイプを使用できますか?

A2: はい、Aspose.PSD for Java では、Nearest Neighbour、Bicubic など、さまざまなサイズ変更タイプが提供されています。包括的なリストについては、ドキュメントを参照してください。

### Q3: Aspose.PSD for Java の追加サポートはどこで入手できますか?

 A3: ご質問やご不明な点がございましたら、[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34).

### Q4: Aspose.PSD for Java の無料試用版はありますか?

 A4: はい、無料試用版をご利用いただけます[ここ](https://releases.aspose.com/).

### Q5: Aspose.PSD for Java の一時ライセンスを取得するにはどうすればよいですか?

 A5: 一時ライセンスを取得するには、[このリンク](https://purchase.aspose.com/temporary-license/).