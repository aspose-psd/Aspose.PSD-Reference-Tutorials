---
title: Aspose.PSD for Java で画像を四角形に切り取る
linktitle: 画像を長方形で切り取る
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用して、Java でのシームレスな画像切り抜き機能を試してみましょう。Aspose.PSD for Java を使用して画像を簡単に切り抜くには、ステップ バイ ステップ ガイドに従ってください。
type: docs
weight: 15
url: /ja/java/image-editing/crop-image-by-rectangle/
---
## 導入

Java 開発の世界では、画像の操作は一般的なタスクであり、Aspose.PSD for Java は画像処理のための強力なソリューションを提供します。このチュートリアルでは、Aspose.PSD for Java を使用して画像を四角形で切り取るプロセスについて説明します。これを簡単に実現するには、以下の手順に従ってください。

## 前提条件

チュートリアルに進む前に、次の前提条件が満たされていることを確認してください。

- マシンに Java 開発キット (JDK) がインストールされています。
- Aspose.PSD for Javaライブラリ。ダウンロードは以下から行えます。[Webサイト](https://releases.aspose.com/psd/java/).

## パッケージのインポート

Aspose.PSD for Java の機能を活用するには、Java プロジェクトに必要なパッケージが含まれていることを確認してください。Java ファイルの先頭に次のインポート ステートメントを追加します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

ここで、Aspose.PSD for Java を使用して画像を四角形で切り抜く手順を複数のステップに分解して説明します。

## ステップ1: ドキュメントディレクトリを設定する

```java
String dataDir = "Your Document Directory";
```

交換する`"Your Document Directory"`PSD ファイルが配置されている実際のパスを入力します。

## ステップ2: ソースファイルと宛先ファイルを指定する

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

ソース PSD ファイルと宛先 JPEG ファイルのパスを定義します。

## ステップ3: イメージをロードしてキャッシュする

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

PSD画像を`RasterImage`インスタンスを作成し、そのデータをキャッシュします。

## ステップ4: 切り抜き長方形を作成して定義する

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

インスタンスを作成する`Rectangle`切り抜きたいサイズのクラス。

## ステップ5: 画像を切り抜いて保存する

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

指定された四角形を使用して切り抜き操作を実行し、結果を JPEG ファイルとして保存します。

必要に応じてこれらの手順を繰り返し、特定の要件に応じてパラメータを調整します。

## 結論

このチュートリアルでは、Aspose.PSD for Java を使用して画像を四角形で切り取るプロセスを説明しました。これらの手順に従うことで、強力な画像操作機能を Java アプリケーションに簡単に統合できます。

## よくある質問

### Q1: Aspose.PSD for Java を他の Java フレームワークと一緒に使用できますか?

A1: はい、Aspose.PSD for Java はさまざまな Java フレームワークと統合できるため、開発プロジェクトに柔軟性がもたらされます。

### Q2: Aspose.PSD for Java の無料試用版はありますか?

 A2: はい、無料試用版をご利用いただけます[ここ](https://releases.aspose.com/).

### Q3: 追加のサポートや支援はどこで受けられますか?

 A3: 訪問[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートとディスカッションのため。

### Q4: Aspose.PSD for Java の一時ライセンスを取得するにはどうすればよいですか?

 A4: 臨時免許証を取得することができます[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose.PSD for Java でトリミングできる画像形式は何ですか?

A5: Aspose.PSD for Java は、PSD、PNG、JPEG など、さまざまな画像形式をサポートしています。