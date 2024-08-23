---
title: Aspose.PSD for Java で画像を回転する
linktitle: 画像を回転する
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用すると、Java で画像の回転を簡単に実行できます。PSD ファイルを簡単に回転、反転、保存できます。
type: docs
weight: 19
url: /ja/java/advanced-image-manipulation/rotate-image/
---
## 導入

Aspose.PSD for Java は、画像を操作する強力な機能セットを提供し、開発者が PSD ファイルを効率的に操作および処理できるようにします。このチュートリアルでは、画像の回転という特定のタスクに焦点を当てます。写真編集アプリケーションを構築する場合でも、単に画像の方向を調整する必要がある場合でも、Aspose.PSD を使用するとプロセスが簡単になります。

## 前提条件

チュートリアルに進む前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for Javaライブラリ: Aspose.PSD for Javaライブラリをダウンロードしてインストールしたことを確認してください。ライブラリと詳細なドキュメントは以下から入手できます。[ここ](https://reference.aspose.com/psd/java/).

- Java 開発環境: マシンに Java 開発環境が設定されていることを確認します。

- サンプルPSDファイル：回転したいサンプルPSDファイルを準備します。`sourceFile`サンプルコード内の変数に PSD ファイルへのパスを指定します。

## パッケージのインポート

まず、Aspose.PSD の機能を活用するために必要なパッケージをインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## ステップ1: 画像を読み込む

既存の画像をインスタンスにロードします`Image`クラス：

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## ステップ2: 画像を回転する

画像を回転するには、`rotateFlip`方法。この例では、画像を 270 度回転します。

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## ステップ3: 回転した画像を保存する

回転した画像を保存するには、`save`メソッドと出力形式（この場合は JPEG）を指定します。

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## 結論

おめでとうございます! Aspose.PSD for Java を使用して画像を正常に回転できました。このシンプルでありながら強力なライブラリにより、Java アプリケーションでの画像操作の可能性が広がります。

## よくある質問

### Q1: Aspose.PSD はさまざまな画像形式と互換性がありますか?

A1: はい、Aspose.PSD は PSD、JPEG、PNG など、さまざまな画像形式をサポートしています。

### Q2: 定義済みの反転だけでなく、カスタム回転を適用できますか?

A2: もちろんです! Aspose.PSD は、特定の要件を満たすためにカスタム回転を適用する柔軟性を提供します。

### Q3: 追加のサポートや支援はどこで受けられますか?

 A3: ご質問やご不明な点がございましたら、[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティサポートのため。

### Q4: 無料トライアルはありますか?

 A4: はい、Aspose.PSDを[無料トライアル](https://releases.aspose.com/).

### Q5: 一時ライセンスを取得するにはどうすればよいですか?

 A5: 臨時免許証が必要な場合は取得できます[ここ](https://purchase.aspose.com/temporary-license/).