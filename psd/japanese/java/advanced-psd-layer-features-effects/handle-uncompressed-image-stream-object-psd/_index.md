---
date: 2025-12-13
description: Aspose.PSD for Java を使用して、非圧縮画像ストリームを処理し、PSD グラフィックスオブジェクトの作成と PSD レイヤーの操作方法を学びましょう。
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: PSDグラフィックスオブジェクトの作成 – Javaでの非圧縮ストリーム
url: /ja/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD グラフィックスオブジェクトの作成 – Java の非圧縮ストリーム

## Introduction
Java における画像操作の世界へようこそ！このチュートリアルでは **PSD グラフィックスオブジェクトを作成**し、Aspose.PSD for Java を使用して非圧縮画像ストリームオブジェクトを扱います。ワークフローの自動化を目指すグラフィックデザイナーや、アプリケーションに強力な画像処理機能を組み込みたいソフトウェア開発者の皆様に最適なガイドです。前提条件から結論まで順を追って説明し、Aspose.PSD の始め方をしっかりと理解できるようにします。

## Quick Answers
- **“create PSD graphics object” とは何ですか？** PSD ファイル用のグラフィックコンテキストをインスタンス化し、その内容を描画または編集できるようにすることを指します。  
- **どのライブラリが非圧縮ストリームを扱いますか？** Aspose.PSD for Java が生（Raw）形式の非圧縮画像データをフルサポートしています。  
- **開発にライセンスは必要ですか？** テスト用の無料トライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **グラフィックスオブジェクト作成後に PSD レイヤーを操作できますか？** はい。Graphics インスタンスを使用すれば任意のレイヤーに描画できます。  

## Prerequisites
この旅を始める前に、必要なものがすべて揃っているか確認しましょう。以下が前提条件です。

### Java Development Kit (JDK)
マシンに JDK がインストールされていることを確認してください。Oracle のウェブサイトからダウンロードするか、OpenJDK を使用できます。

### Aspose.PSD for Java
Aspose.PSD ライブラリをダウンロードしてインストールする必要があります。この強力なライブラリを使えば PSD ファイルを簡単に操作できます。最新バージョンは [this link](https://releases.aspose.com/psd/java/) から取得できます。

### Integrated Development Environment (IDE)
Java コードの記述とテストには IDE の使用をおすすめします。IntelliJ IDEA、Eclipse、またはお好みの IDE を使用してください。

### Basic Understanding of Java
Java プログラミングの基礎（クラス、メソッド、例外処理など）に慣れていると作業がスムーズです。

すべて準備できたら、袖をまくってワクワクするコーディングパートへ進みましょう！

## Import Packages
作業を開始するには、Aspose.PSD 用に必要なパッケージをインポートする必要があります。以下に PSD ファイルを扱う際に通常使用するインポート文を示します。

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

次に、コードを段階的に分解して説明します。セットアップ、PSD の読み込み、操作、保存の順に進めます。

## Step 1: Define Your Document Directory
コードを書く前に、PSD ファイルが置かれているディレクトリを定義します。これはプロジェクトの土台を設定することに相当します。

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` を、実際に PSD ファイル（例: layers.psd）が存在するパスに置き換えてください。これによりファイルの場所を手間なく特定できます。

## Step 2: Create a Byte Array Output Stream
変更後の画像を保存する場所が必要です。`ByteArrayOutputStream` を使用すれば画像データを簡単にキャプチャできます。

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

この行は `ms` という名前の新しい `ByteArrayOutputStream` オブジェクトを初期化します。非圧縮画像の保存にこのオブジェクトを使用します。

## Step 3: Load the PSD File
いよいよ実際の PSD ファイルを読み込みます。ここからがマジックの始まりです！

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

この行は PSD ファイルを `PsdImage` オブジェクトにロードします。パスが正しくないと、チェックされていないクイズのようにエラーが発生しますので注意してください。

## Step 4: Set Up the PsdOptions for Saving
画像を保存する方法（もちろん非圧縮）を指定する必要があります。

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

ここでは `PsdOptions` オブジェクトを作成し、圧縮方式を `Raw` に設定しています。この方式により画像はフルクオリティを保ち、圧縮なしで保存されます。

## Step 5: Save the Image to the Output Stream
```java
psdImage.save(ms, saveOptions);
```

この行は Step 2 で作成した `ByteArrayOutputStream` に、Step 4 で定義したオプションを使用して変更後の画像を保存します。`save` メソッドが設定に基づき画像を適切にエンコードします。

## Step 6: Reset the Output Stream
保存後、出力ストリームは末尾に位置しています。先頭から読み取れるようにリセットが必要です。

```java
ms.reset();
```

この `reset` メソッドは `ByteArrayOutputStream` を再び先頭から読み取れる状態に準備します。好きな曲を聴く前にテープを巻き戻すイメージです！

## Step 7: Load the Newly Created Image
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

ここでは `ByteArrayOutputStream` から画像を再度読み込み、新しい `PsdImage` オブジェクトに格納します。これで先ほどの作業結果を確認できます。

## Step 8: Create Graphics Object
画像をさらに修正または描画するには、グラフィックスオブジェクトを作成する必要があります。

```java
Graphics graphics = new Graphics(psdImage);
```

この行は `psdImage` を使用して `Graphics` オブジェクトを初期化します。これでペイントブラシを手に入れたように、画像を自由に描画・操作できます。

## Manipulate PSD Layers with Graphics Object
**Graphics** インスタンスを取得したので、**PSD レイヤーを操作**できます。たとえばシェイプの描画、テキストの追加、特定レイヤーへのフィルタ適用などが可能です。グラフィックコンテキストはピクセルデータに直接作用するため、各レイヤーの外観を細かく制御できます。

## Common Issues and Solutions
- **NullPointerException がファイル読み込み時に発生** – `dataDir` のパスとファイル名が正しいか再確認してください。  
- **Raw を使用しているのに出力が圧縮される** – `save` メソッド呼び出し前に `saveOptions.setCompressionMethod(CompressionMethod.Raw);` が実行されているか確認してください。  
- **Graphics オブジェクトが空白になる** – 正しい `PsdImage` インスタンス（ロードしたもの）に対して描画しているか確認してください。新しく作成したインスタンスで意図せず描画していないか注意が必要です。

## FAQ's
### What is Aspose.PSD?
Aspose.PSD は .NET ライブラリで、開発者がプログラムから Photoshop PSD ファイルおよび関連画像フォーマットを作成、編集、操作できるようにします。

### How can I download Aspose.PSD for Java?
[release page](https://releases.aspose.com/psd/java/) からダウンロードできます。

### Is there a free trial for Aspose.PSD?
はい、[here](https://releases.aspose.com/) から無料トライアル版を入手できます。

### Can I get support for Aspose.PSD?
もちろんです！[Aspose support forum](https://forum.aspose.com/c/psd/34) でサポートを受けられます。

### How can I obtain a temporary license for Aspose.PSD?
[temporary license page](https://purchase.aspose.com/temporary-license/) にアクセスして取得してください。

## Frequently Asked Questions

**Q: Can I use the graphics object to edit only one specific layer?**  
A: Yes. After loading the PSD, select the desired layer via `psdImage.getLayers().get_Item(index)` and pass it to the `Graphics` constructor.

**Q: Does the Raw compression method affect file size?**  
A: Raw stores pixel data without compression, so the file size will be larger than compressed PSDs, but image quality remains untouched.

**Q: Is it possible to export the edited PSD to another format (e.g., PNG)?**  
A: Absolutely. Use the appropriate `Image.save` overload with `PngOptions` after editing.

**Q: What Java version is required?**  
A: Aspose.PSD for Java supports JDK 8 and later.

**Q: How do I release resources after processing?**  
A: Call `psdImage.dispose()` and close any streams to free native resources.

---  

**Last Updated:** 2025-12-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}