---
date: 2026-03-21
description: Aspose.PSD for Java を使用して PSD を PNG に変換し、PSD ファイルをトリミングする方法を学びましょう。このガイドでは、Java
  アプリケーションでのステップバイステップの画像処理を示します。
linktitle: Cropping PSD when Converting to PNG
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して PSD を PNG に変換しながらトリミングする方法
url: /ja/java/psd-conversion/cropping-psd-converting-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用して PSD を PNG に変換しながらトリミングする方法

## はじめに
Java 開発の動的な世界では、効率的な画像処理を習得することが重要です。このチュートリアルでは、強力な Aspose.PSD for Java ライブラリを使用して **psd を png に変換** し、画像を単一のワークフローでトリミングする方法を学びます。ステップバイステップのガイドを終える頃には、PNG エクスポートに正確なトリミングを追加でき、Java アプリケーションで PSD アセットを自信を持って扱えるようになります。

## クイック回答
- **コードは何をしますか？** PSD を読み込み、矩形をトリミングし、PNG として保存します。  
- **必要なライブラリは？** Aspose.PSD for Java（最新バージョン）。  
- **ライセンスは必要ですか？** はい、商用利用には商用ライセンスが必要です。  
- **任意のトリミング領域を定義できますか？** もちろんです。必要な X、Y、幅、高さを設定します。  
- **大きなファイルでも高速ですか？** はい、Aspose.PSD は高性能処理向けに最適化されています。

## convert psd to png とは何ですか？
PSD を PNG に変換するとは、レイヤー構造を持つ Photoshop ドキュメントを、ロスレスの PNG 画像にフラット化することです。この形式はウェブ配信、サムネイル、またはレイヤーが不要なラスタ画像が必要なあらゆるシナリオに最適です。

## PNG に変換する前に PSD をトリミングする理由
トリミングにより、デザインの必要な部分だけを抽出でき、ファイルサイズを削減し、視覚的に重要なコンテンツに焦点を当てられます。サムネイル作成、UI アセット、レスポンシブレイアウト用画像の準備に特に有用です。

## 前提条件
チュートリアルに入る前に、以下の前提条件を満たしていることを確認してください。
- Java プログラミングの基本的な知識。  
- システムに Java Development Kit (JDK) がインストールされていること。  
- Aspose.PSD for Java ライブラリをダウンロードし、プロジェクトに追加していること。  
- 実験用のサンプル PSD ファイル。

## パッケージのインポート
Java プロジェクトで Aspose.PSD の機能を使用するために、必要なパッケージをインポートしてください:
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```

## ステップ 1: プロジェクトの設定
Java プロジェクトを作成し、Aspose.PSD for Java ライブラリをプロジェクトのクラスパスに追加します。これにより、必要なすべての画像処理クラスにアクセスできるようになります。

## ステップ 2: PSD 画像の読み込み
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// Load an existing PSD image
RasterImage image = (RasterImage)Image.load(srcPath);
```
*ここでは、ソース PSD ファイルを `RasterImage` オブジェクトに読み込みます。このオブジェクトはトリミングなどのラスタベース操作を提供します。*

## ステップ 3: トリミング領域の定義
```java
// Create an instance of Rectangle class by passing x, y, width, and height
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
*`Rectangle` は保持したい領域を定義します。デザインに合わせて `x`、`y`、`width`、`height` の値を調整してください。このステップは「トリミング領域を定義する」キーワードに直接対応しています。*

## ステップ 4: PSD 画像のトリミング
```java
// Call the crop method of Image class and pass the Rectangle instance
image.crop(cropRegion);
```
*`crop` を呼び出すことで、指定した矩形外のすべてを除外し、メモリ上の画像が変更されます。*

## ステップ 5: PNG エクスポートオプションの設定
```java
// Create an instance of PngOptions class
PngOptions pngOptions = new PngOptions();
```
*`PngOptions` を使用すると、圧縮レベルやカラーモードなど、PNG 固有の設定を制御できます。*

## ステップ 6: トリミングした画像を PNG として保存
```java
// Provide output path and PngOptions to convert the PSD file to PNG and save the output
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
*`save` メソッドは、定義したトリミングを保持しながら **psd を png に変換** する操作を実行します。*

## よくある落とし穴とヒント
- **矩形サイズが不正:** 幅と高さが元画像サイズを超えないようにしてください。超えると例外がスローされます。  
- **大きな PSD のメモリ使用量:** 保存後に `RasterImage` オブジェクト (`image.dispose()`) を破棄して、ネイティブリソースを解放します。  
- **ライセンス未設定:** 有効なライセンスなしでコードを実行すると、出力 PNG に透かしが表示されます。

## よくある質問
### Aspose.PSD for Java を使用して不規則な形状の PSD ファイルをトリミングできますか？
はい、Aspose.PSD for Java ではカスタムのトリミング領域を定義でき、さまざまな形状に画像をトリミングできます。

### Aspose.PSD for Java は大規模な画像処理タスクに適していますか？
もちろんです！ Aspose.PSD は大きな画像を効率的に処理できるよう設計されており、広範な画像処理要件を持つプロジェクトに最適です。

### Aspose.PSD for Java のライセンスは必要ですか？
はい、商用利用には有効なライセンスが必要です。ライセンスは [Aspose Purchase](https://purchase.aspose.com/buy) から取得できます。

### Aspose.PSD for Java のサポートを受けたり、問題を報告したりするには？
サポートや質問は [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) で受け付けています。経験を共有したり、問題を報告したりしてください。

### 購入前に Aspose.PSD for Java を試すことはできますか？
もちろんです！ 無料トライアルは [here](https://releases.aspose.com/) から利用できます。

---

**最終更新日:** 2026-03-21  
**テスト環境:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**著者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}