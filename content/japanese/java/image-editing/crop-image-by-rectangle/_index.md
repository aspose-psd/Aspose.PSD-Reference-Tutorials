---
title: Java 用 Aspose.PSD で画像を四角形で切り抜く
linktitle: 画像を長方形で切り抜く
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用して Java のシームレスな画像トリミング機能を試してください。ステップバイステップのガイドに従って、Aspose.PSD for Java を使用して画像を簡単に切り抜きます。
type: docs
weight: 15
url: /ja/java/image-editing/crop-image-by-rectangle/
---
## 導入

Java 開発の世界では、画像の操作は一般的なタスクであり、Aspose.PSD for Java は画像処理のための強力なソリューションを提供します。このチュートリアルでは、Aspose.PSD for Java を使用して画像を四角形で切り取るプロセスを説明します。これを簡単に達成するには、以下の手順に従ってください。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

- Java Development Kit (JDK) がマシンにインストールされています。
-  Java ライブラリの Aspose.PSD。からダウンロードできます。[Webサイト](https://releases.aspose.com/psd/java/).

## パッケージのインポート

Aspose.PSD for Java の機能を活用するには、Java プロジェクトに必要なパッケージを必ず含めてください。 Java ファイルの先頭に次の import ステートメントを追加します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

ここで、プロセスを複数のステップに分けて、Aspose.PSD for Java を使用して画像を四角形で切り抜く方法を説明します。

## ステップ 1: ドキュメント ディレクトリを設定する

```java
String dataDir = "Your Document Directory";
```

交換する`"Your Document Directory"`PSD ファイルが配置されている実際のパスに置き換えます。

## ステップ 2: ソース ファイルと宛先ファイルを指定する

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

ソース PSD ファイルと宛先 JPEG ファイルのパスを定義します。

## ステップ 3: イメージをロードしてキャッシュする

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

PSD 画像を`RasterImage`インスタンスを作成し、そのデータをキャッシュします。

## ステップ 4: 切り抜き四角形を作成および定義する

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

のインスタンスを作成します。`Rectangle`トリミングに必要なサイズのクラス。

## ステップ 5: 画像を切り取って保存する

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

指定した四角形を使用して切り抜き操作を実行し、結果を JPEG ファイルとして保存します。

必要に応じてこれらの手順を繰り返し、特定の要件に応じてパラメータを調整します。

## 結論

このチュートリアルでは、Aspose.PSD for Java を使用して画像を四角形で切り取るプロセスを説明しました。これらの手順に従うことで、強力な画像操作機能を Java アプリケーションに簡単に統合できます。

## よくある質問

### Q1: Aspose.PSD for Java を他の Java フレームワークと一緒に使用できますか?

A1: はい、Aspose.PSD for Java はさまざまな Java フレームワークと統合でき、開発プロジェクトに柔軟性をもたらします。

### Q2: Aspose.PSD for Java の無料トライアルはありますか?

 A2: はい、無料試用版にアクセスできます。[ここ](https://releases.aspose.com/).

### Q3: 追加のサポートや支援はどこで入手できますか?

 A3: にアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートとディスカッションのために。

### Q4: Aspose.PSD for Java の一時ライセンスを取得するにはどうすればよいですか?

 A4: 仮免許を取得することができます。[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose.PSD for Java でのトリミングでサポートされている画像形式は何ですか?

A5: Aspose.PSD for Java は、PSD、PNG、JPEG などを含むさまざまな画像形式をサポートしています。