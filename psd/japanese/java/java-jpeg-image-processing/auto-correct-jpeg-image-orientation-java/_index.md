---
title: Java で JPEG 画像の向きを自動修正する
linktitle: Java で JPEG 画像の向きを自動修正する
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用して Java で JPEG 画像の向きを自動的に修正する方法を学びます。画像処理スキルを簡単に向上できます。
type: docs
weight: 12
url: /ja/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---
## 導入
今日のデジタル時代では、プログラムによる画像の操作と最適化は、さまざまな分野の開発者にとって重要なタスクになっています。Aspose.PSD for Java は、PSD、JPEG、およびその他の画像形式を効率的に処理するための強力なツールを開発者に提供します。このチュートリアルでは、Aspose.PSD for Java を使用して JPEG 画像の向きを自動的に修正するという特定のタスクについて詳しく説明します。写真編集アプリを構築する場合でも、コンテンツ管理システムで画像リソースを管理する場合でも、画像処理ワークフローを自動化する場合でも、このガイドを読めば、この機能を Java アプリケーションにシームレスに統合するために必要な知識が得られます。
## 前提条件
このチュートリアルに進む前に、次の前提条件が設定されていることを確認してください。
- Java 開発環境: システムに Java 開発キット (JDK) がインストールされていることを確認してください。
-  Aspose.PSD for Java JAR: Aspose.PSD for Javaライブラリを以下からダウンロードします。[ここ](https://releases.aspose.com/psd/java/).
- 統合開発環境 (IDE): Java 開発には、IntelliJ IDEA、Eclipse、または任意の IDE を使用します。
- Java と画像処理の基本的な理解: Java プログラミングと画像処理の基本的な概念を理解していると役立ちます。

## パッケージのインポート
例を始める前に、Aspose.PSD for Java から必要なパッケージをインポートしてください。
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## ステップ1: PSDイメージを読み込む
まず、向きを修正する必要がある JPEG サムネイルを含む PSD イメージを読み込みます。
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
交換する`"Your Document Directory"` PSD ファイルが配置されている実際のディレクトリ パスを入力します。
## ステップ2: 画像リソースを反復処理する
次に、画像リソースを反復処理して、JPEG サムネイル リソースを見つけます。
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    //サムネイル リソースを検索します。通常、サムネイルは Jpeg ファイル形式です。
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        //サムネイルデータを調整します。
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            //サムネイルが保存されている場合は、自動的に回転します。
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```
## ステップ3: 画像を保存する
最後に、自動回転を適用した後、修正した画像を保存します。
```java
image.save();
```
この手順により、イメージに加えられた変更が保持されます。

## 結論
結論として、Aspose.PSD for Java を使用すると、PSD ファイル内の JPEG 画像の向きを自動的に修正する強力なソリューションが提供されます。このチュートリアルで説明されている手順に従うことで、開発者は画像処理ワークフローを強化し、さまざまなプラットフォームやデバイスで画像が正しく表示されるようにすることができます。
## よくある質問
### Aspose.PSD for Java とは何ですか?
Aspose.PSD for Java は、Java 開発者が PSD、JPEG、およびその他の画像形式をプログラムで操作できるようにする強力なライブラリです。
### Aspose.PSD for Java をダウンロードするにはどうすればいいですか?
ライブラリは以下からダウンロードできます。[ここ](https://releases.aspose.com/psd/java/).
### Aspose.PSD for Java は画像操作をサポートしていますか?
はい、サイズ変更、切り抜き、向きの調整など、さまざまな画像操作タスクをサポートしています。
### Aspose.PSD for Java のドキュメントはどこにありますか?
包括的なドキュメントが利用可能[ここ](https://reference.aspose.com/psd/java/).
### Aspose.PSD for Java を無料で試すことはできますか?
はい、無料トライアルをご利用いただけます[ここ](https://releases.aspose.com/).