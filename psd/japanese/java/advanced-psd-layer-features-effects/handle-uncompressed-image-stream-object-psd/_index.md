---
date: 2026-02-17
description: Aspose.PSD for Java を使用して、PSD を PNG にエクスポートし、非圧縮画像ストリームを処理する方法を学びましょう。
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: PSD を PNG にエクスポート – PSD グラフィックスオブジェクトの作成 – Java の非圧縮ストリーム
url: /ja/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD を PNG にエクスポート – PSD Graphics オブジェクトの作成 – Java での非圧縮ストリーム

## Introduction
Java における画像操作の世界へようこそ！このチュートリアルでは **PSD graphics オブジェクトを作成** し、非圧縮画像ストリームオブジェクトを扱い、Aspose.PSD for Java を使用して **PSD を PNG にエクスポート** する方法を学びます。ワークフローを自動化したいグラフィックデザイナーでも、強力な画像処理機能をアプリケーションに統合したいソフトウェア開発者でも、このガイドはあなたのために作られています。前提条件から最終エクスポートまで、プロセス全体をしっかりと理解できるようにステップバイステップで解説します。

## Quick Answers
- **「PSD graphics オブジェクトを作成する」とは何ですか？** PSD ファイル用のグラフィックコンテキストをインスタンス化し、その内容を描画または編集できるようにすることを指します。  
- **どのライブラリが非圧縮ストリームを扱いますか？** Aspose.PSD for Java が生（非圧縮）画像データをフルサポートします。  
- **編集後に PSD を PNG にエクスポートできますか？** はい、`Graphics` オブジェクトがあれば PSD をレンダリングし PNG として保存できます。  
- **開発用にライセンスは必要ですか？** テスト用の無料トライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **エクスポートはロスレスですか？** PNG へのエクスポートは画像品質を保持します。ファイルサイズは JPEG より大きく、非圧縮 PSD よりは小さくなります。  

## How to export PSD to PNG using Aspose.PSD for Java
**PSD を PNG にエクスポート** する際の一般的なワークフローは次のとおりです。

1. PSD ファイルをロード（または作成）する。  
2. `Graphics` オブジェクトで描画やレイヤー操作を行う。  
3. `PngOptions` を使用して画像を保存する（同じ `Graphics` インスタンスを再利用可能）。  

このチュートリアルは非圧縮ストリームの取り扱いに焦点を当てていますが、作成した `Graphics` オブジェクトは後で PSD を PNG にレンダリングする際にも再利用できます。

## Prerequisites
コードに取り掛かる前に、必要なものがすべて揃っているか確認しましょう。以下が前提条件です。

### Java Development Kit (JDK)
マシンに JDK がインストールされていることを確認してください。Oracle のウェブサイトからダウンロードするか、OpenJDK を使用できます。

### Aspose.PSD for Java
Aspose.PSD ライブラリをダウンロードしてインストールする必要があります。この強力なライブラリを使えば PSD ファイルを簡単に操作できます。最新バージョンは [this link](https://releases.aspose.com/psd/java/) から入手してください。

### Integrated Development Environment (IDE)
Java コードの作成とテストには IDE の使用をおすすめします。IntelliJ IDEA、Eclipse、またはお好みの IDE を利用してください。

### Basic Understanding of Java
Java の基本的な知識（クラス、メソッド、例外処理など）があると作業がスムーズです。

すべて準備できたら、袖をまくって本題のコーディングに入りましょう！

## Import Packages
まずは Aspose.PSD を操作するために必要なパッケージをインポートします。以下は PSD ファイルを扱う際に一般的に使用するインポート例です。

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

コードを段階的に分解して説明しますので、安心して進めてください。セットアップ、PSD のロード、操作、出力までを順に行います。

## Step 1: Define Your Document Directory
コーディングを始める前に、PSD ファイルが置かれているディレクトリを定義します。これはプロジェクトの土台を作る作業です。

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` を実際のパス（例: `layers.psd` がある場所）に置き換えてください。これでファイルの所在が明確になります。

## Step 2: Create a Byte Array Output Stream
変更した画像を保存する場所が必要です。`ByteArrayOutputStream` を使えば画像データを簡単に取得できます。

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

この行は `ByteArrayOutputStream` オブジェクト `ms` を新規作成しています。非圧縮画像を保存するためにこのオブジェクトを使用します。

## Step 3: Load the PSD File
いよいよ実際の PSD ファイルをロードします。ここからが本番です！

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

この行は PSD ファイルを `PsdImage` オブジェクトに読み込みます。パスが正しいことを確認してください。間違えるとエラーが発生します。

## Step 4: Set Up the PsdOptions for Saving
画像を保存する際の設定を行います——もちろん非圧縮です！

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

ここで `PsdOptions` オブジェクトを作成し、圧縮方法を `Raw` に設定しています。この設定により画像はフルクオリティで圧縮なしで保存されます。

## Step 5: Save the Image to the Output Stream
```java
psdImage.save(ms, saveOptions);
```

この行はステップ 2 で作成した `ByteArrayOutputStream` に、ステップ 4 で定義したオプションを使って画像を保存します。`save` メソッドが設定に基づき適切にエンコードを行います。

## Step 6: Reset the Output Stream
保存後、出力ストリームは末尾に位置しています。最初から読み取れるようにリセットが必要です。

```java
ms.reset();
```

`reset` メソッドは `ByteArrayOutputStream` を先頭に戻します。テープを巻き戻すイメージです。

## Step 7: Load the Newly Created Image
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

ここでは `ByteArrayOutputStream` から新しい `PsdImage` オブジェクトに画像を再度ロードします。先ほどの作業結果を確認できる段階です。

## Step 8: Create Graphics Object
画像をさらに加工したりレンダリングしたりするために、Graphics オブジェクトを作成します。

```java
Graphics graphics = new Graphics(psdImage);
```

この行は `psdImage` を元に `Graphics` オブジェクトを初期化しています。これでペイントブラシを手に入れたように描画や操作が可能になります。

## Manipulate PSD Layers with Graphics Object
`Graphics` インスタンスが手に入ったので、**PSD レイヤーを操作** できます。たとえばシェイプの描画、テキストの追加、特定レイヤーへのフィルタ適用などです。グラフィックコンテキストはピクセルデータに直接作用するため、各レイヤーの外観を細かく制御できます。

## Common Issues and Solutions
- **NullPointerException が発生した場合** – `dataDir` のパスとファイル名が正しいか再確認してください。  
- **Raw を指定しているのに圧縮された出力になる** – `save` メソッド呼び出し前に `saveOptions.setCompressionMethod(CompressionMethod.Raw);` が実行されているか確認してください。  
- **Graphics オブジェクトが空白になる** – 正しい `PsdImage` インスタンス（ロードしたもの）を使用しているか確認してください。意図しない新規作成オブジェクトを使っていませんか。

## FAQ's
### What is Aspose.PSD?
Aspose.PSD は、開発者がプログラムから Photoshop PSD ファイルおよび関連画像形式を作成、編集、操作できるようにする .NET ライブラリです。

### How can I download Aspose.PSD for Java?
[release page](https://releases.aspose.com/psd/java/) からダウンロードできます。

### Is there a free trial for Aspose.PSD?
はい、[here](https://releases.aspose.com/) から無料トライアル版を取得できます。

### Can I get support for Aspose.PSD?
もちろんです！[Aspose support forum](https://forum.aspose.com/c/psd/34) で質問できます。

### How can I obtain a temporary license for Aspose.PSD?
[temporary license page](https://purchase.aspose.com/temporary-license/) へアクセスして取得してください。

## Frequently Asked Questions

**Q: Can I use the graphics object to edit only one specific layer?**  
A: Yes. After loading the PSD, select the desired layer via `psdImage.getLayers().get_Item(index)` and pass it to the `Graphics` constructor.

**Q: Does the Raw compression method affect file size?**  
A: Raw stores pixel data without compression, so the file size will be larger than compressed PSDs, but image quality remains untouched.

**Q: Is it possible to export the edited PSD to another format (e.g., PNG)?**  
A: Absolutely. Use the appropriate `Image.save` overload with `PngOptions` after editing—this is the standard way to **export PSD to PNG**.

**Q: What Java version is required?**  
A: Aspose.PSD for Java supports JDK 8 and later.

**Q: How do I release resources after processing?**  
A: Call `psdImage.dispose()` and close any streams to free native resources.

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}