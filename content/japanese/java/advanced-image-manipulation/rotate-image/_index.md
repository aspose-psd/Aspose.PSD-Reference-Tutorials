---
title: Aspose.PSD for Java で画像を回転する
linktitle: 画像を回転する
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用して、Java で画像の回転を簡単に試してみましょう。 PSD ファイルを簡単に回転、反転、保存できます。
type: docs
weight: 19
url: /ja/java/advanced-image-manipulation/rotate-image/
---
## 導入

Aspose.PSD for Java は、画像を操作するための強力な機能セットを提供し、開発者が PSD ファイルを効率的に操作および処理できるようにします。このチュートリアルでは、画像の回転という 1 つの特定のタスクに焦点を当てます。写真編集アプリケーションを構築している場合でも、単に画像の向きを調整する必要がある場合でも、Aspose.PSD を使用するとプロセスが簡単になります。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for Java ライブラリ: Aspose.PSD for Java ライブラリをダウンロードしてインストールしていることを確認します。ライブラリと詳細なドキュメントを見つけることができます[ここ](https://reference.aspose.com/psd/java/).

- Java 開発環境: マシン上に Java 開発環境がセットアップされていることを確認してください。

- サンプル PSD ファイル: 回転させたいサンプル PSD ファイルを用意します。を調整します。`sourceFile`サンプル コード内の変数を PSD ファイルへのパスに置き換えます。

## パッケージのインポート

まず、Aspose.PSD の機能を活用するために必要なパッケージをインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## ステップ 1: 画像をロードする

既存のイメージをインスタンスにロードします。`Image`クラス：

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## ステップ 2: 画像を回転する

を使用して画像を回転します。`rotateFlip`方法。この例では、画像を 270 度回転します。

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## ステップ 3: 回転した画像を保存する

回転した画像を保存するには、`save`方法と出力形式 (この場合は JPEG) を指定します。

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## 結論

おめでとう！ Aspose.PSD for Java を使用して画像を正常に回転できました。このシンプルかつ強力なライブラリは、Java アプリケーションでの画像操作の可能性を広げます。

## よくある質問

### Q1: Aspose.PSD はさまざまな画像形式と互換性がありますか?

A1: はい、Aspose.PSD は PSD、JPEG、PNG などを含むさまざまな画像形式をサポートしています。

### Q2: 定義済みの反転だけでなく、カスタムの回転を適用できますか?

A2: もちろんです！ Aspose.PSD は、特定の要件を満たすためにカスタム回転を適用するための柔軟性を提供します。

### Q3: 追加のサポートや支援はどこで入手できますか?

 A3: 質問や問題がある場合は、次のサイトにアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティサポートのために。

### Q4: 無料トライアルはありますか?

 A4: はい、Aspose.PSD を使用して探索できます。[無料トライアル](https://releases.aspose.com/).

### Q5: 仮ライセンスを取得するにはどうすればよいですか?

 A5: 仮免許が必要な場合は取得できます。[ここ](https://purchase.aspose.com/temporary-license/).