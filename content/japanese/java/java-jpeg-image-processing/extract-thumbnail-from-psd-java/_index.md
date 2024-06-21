---
title: JavaでPSDからサムネイルを抽出する
linktitle: JavaでPSDからサムネイルを抽出する
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して PSD ファイルからサムネイルを抽出する方法を学びます。このステップバイステップのガイドでは、セットアップから抽出した画像の保存までのすべてを説明します。
type: docs
weight: 15
url: /ja/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## 導入
このチュートリアルでは、Aspose.PSD for Java を使用して PSD ファイルからサムネイルを抽出する方法を説明します。サムネイルは、素早いプレビューや、PSD ドキュメント内に埋め込まれた画像の小さいバージョンを作成する場合に役立ちます。 Aspose.PSD を使用してこれを実現するために必要な手順を詳しく見てみましょう。
## 前提条件
始める前に、次の設定がされていることを確認してください。
- Java Development Kit (JDK) がシステムにインストールされています。
-  Java ライブラリの Aspose.PSD。からダウンロードできます[ここ](https://releases.aspose.com/psd/java/).
- Java プログラミングの基本的な知識。
## パッケージのインポート
まず、必要な Aspose.PSD パッケージを Java クラスに含めます。
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## ステップ 1: PSD ファイルをロードする
まず、抽出したいサムネイルを含む PSD ファイルを読み込みます。
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
交換する`"Your_Document_Directory/"` PSD ファイルが配置されているディレクトリ パスを使用して、`"your_file.psd"` PSD ファイルの名前を付けます。
## ステップ 2: 画像リソースを反復処理する
画像リソースを繰り返し処理して、サムネイル リソースを見つけます。
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        //サムネイルデータの抽出
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        //抽出したサムネイルデータを使用して新しい画像を作成します
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        //抽出したサムネイルを別の JPEG ファイルとして保存します
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        //成功メッセージを出力する
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; //サムネイルが見つかって処理されたら、ループを終了します。
    }
}
```
## ステップ 3: 抽出したサムネイルを保存する
抽出したサムネイルを別の画像ファイル（今回はJPEGファイル）として保存します。
## ステップ 4: さまざまなサムネイル タイプの処理
PSD ファイルに複数のタイプのサムネイルが含まれる場合があります。`Thumbnail4Resource`、ロジックを拡張して、これらのケースを同様に処理することができます。

## 結論
このチュートリアルでは、Aspose.PSD for Java を使用して PSD ファイルからサムネイルを抽出する方法を検討しました。上記の手順に従うことで、PSD ドキュメント内に埋め込まれたサムネイルを効率的に取得して保存できます。

## よくある質問
### Aspose.PSDとは何ですか?
Aspose.PSD は、開発者が PSD およびその他の画像ファイル形式をプログラムで操作できるようにする Java ライブラリです。
### Aspose.PSD for Java に関するその他のドキュメントはどこで見つけられますか?
を参照できます。[ドキュメンテーション](https://reference.aspose.com/psd/java/)詳細な API リファレンスと例については、
### 購入する前に、Aspose.PSD を無料で試用できますか?
はい、ダウンロードできます[無料トライアル](https://releases.aspose.com/)ライブラリの機能を評価します。
### Aspose.PSD の一時ライセンスを取得するにはどうすればよいですか?
一時ライセンスは以下から取得できます。[ここ](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD は商用利用に適していますか?
はい、Aspose.PSD は、ライセンス条項に基づいて個人プロジェクトと商用プロジェクトの両方に使用できます。