---
title: JavaでPSDからサムネイルを抽出する
linktitle: JavaでPSDからサムネイルを抽出する
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して PSD ファイルからサムネイルを抽出する方法を学びます。このステップバイステップ ガイドでは、セットアップから抽出した画像の保存まですべてをカバーしています。
type: docs
weight: 15
url: /ja/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## 導入
このチュートリアルでは、Aspose.PSD for Java を使用して PSD ファイルからサムネイルを抽出する方法について説明します。サムネイルは、簡単なプレビューや、PSD ドキュメントに埋め込まれた画像の小さいバージョンを作成する場合に便利です。Aspose.PSD を使用してこれを実現するために必要な手順について詳しく見ていきましょう。
## 前提条件
始める前に、次の設定がされていることを確認してください。
- Java Development Kit (JDK) がシステムにインストールされています。
-  Aspose.PSD for Javaライブラリ。ここからダウンロードできます。[ここ](https://releases.aspose.com/psd/java/).
- Java プログラミングの基礎知識。
## パッケージのインポート
開始するには、Java クラスに必要な Aspose.PSD パッケージを含めます。
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## ステップ1: PSDファイルを読み込む
まず、抽出したいサムネイルが含まれる PSD ファイルを読み込みます。
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
交換する`"Your_Document_Directory/"` PSDファイルが保存されているディレクトリパスと`"your_file.psd"`PSD ファイルの名前を入力します。
## ステップ2: 画像リソースを反復処理する
画像リソースを反復処理してサムネイル リソースを見つけます。
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        //サムネイルデータを抽出する
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        //抽出したサムネイルデータを使用して新しい画像を作成します
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        //抽出したサムネイルを別のJPEGファイルとして保存します。
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        //成功メッセージの出力
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; //サムネイルが見つかり処理されたらループを終了します
    }
}
```
## ステップ3: 抽出したサムネイルを保存する
抽出したサムネイルを別の画像ファイル（この場合は JPEG ファイル）として保存します。
## ステップ4: さまざまなサムネイルタイプの処理
PSDファイルに複数の種類のサムネイルが含まれている場合、例えば`Thumbnail4Resource`、ロジックを拡張して、同様にそれらのケースを処理することができます。

## 結論
このチュートリアルでは、Aspose.PSD for Java を使用して PSD ファイルからサムネイルを抽出する方法について説明しました。上記の手順に従うことで、PSD ドキュメント内に埋め込まれたサムネイルを効率的に取得して保存できます。

## よくある質問
### Aspose.PSD とは何ですか?
Aspose.PSD は、開発者が PSD やその他の画像ファイル形式をプログラムで操作できるようにする Java ライブラリです。
### Aspose.PSD for Java に関する詳細なドキュメントはどこで入手できますか?
参照するには[ドキュメント](https://reference.aspose.com/psd/java/)詳細な API リファレンスと例については、こちらをご覧ください。
### 購入前に Aspose.PSD を無料で試すことはできますか?
はい、ダウンロードできます[無料トライアル](https://releases.aspose.com/)ライブラリの機能を評価するため。
### Aspose.PSD の一時ライセンスを取得するにはどうすればよいですか?
一時ライセンスは以下から取得できます。[ここ](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD は商用利用に適していますか?
はい、Aspose.PSD はライセンス条件に従って個人プロジェクトと商用プロジェクトの両方に使用できます。