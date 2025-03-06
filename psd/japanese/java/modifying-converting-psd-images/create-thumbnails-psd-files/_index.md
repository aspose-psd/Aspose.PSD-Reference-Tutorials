---
title: Java を使用して PSD ファイルからサムネイルを作成する
linktitle: Java を使用して PSD ファイルからサムネイルを作成する
second_title: Aspose.PSD Java API
description: Java と Aspose.PSD を使用して、PSD ファイルから簡単にサムネイルを作成する方法を学びます。シームレスな画像処理については、ステップバイステップのガイドに従ってください。
weight: 24
url: /ja/java/modifying-converting-psd-images/create-thumbnails-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java を使用して PSD ファイルからサムネイルを作成する

## 導入
グラフィック デザインの世界では、PSD (Photoshop Document) ファイルでの作業は一般的です。熟練した開発者、グラフィック デザイナー、または画像処理に取り組みたいだけの人でも、PSD ファイルからサムネイルを作成すると、時間を節約し、ワークフローを効率化できます。このチュートリアルでは、Aspose.PSD for Java を使用したプロセス全体をガイドします。Aspose.PSD は、Photoshop ファイルの管理に強力なライブラリであるだけでなく、手元のタスクを直感的で管理しやすいものにします。PSD ファイルからサムネイルを効率的に作成する方法を学ぶ準備はできていますか?
## 前提条件
サムネイル作成の詳細に入る前に、始めるために必要なものについて説明しましょう。
### Java開発環境
-  Java JDK: コンピュータにJava開発キット（JDK）がインストールされていることを確認してください。ダウンロードできます。[ここ](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- IDE: IntelliJ IDEA、Eclipse、NetBeans などの統合開発環境 (IDE) を使用すると、コーディングが容易になります。
### Aspose.PSD ライブラリ
- プロジェクトにAspose.PSDライブラリを含める必要があります。[最新バージョンはこちらからダウンロードしてください](https://releases.aspose.com/psd/java/).
### Javaの基礎知識
- Java の基礎知識があれば、サンプル コードをより効果的に理解できます。クラス、オブジェクト、ループなどの概念が頻繁に使用されます。
## パッケージのインポート
まず、Aspose.PSD ライブラリから必要なクラスをインポートします。この手順は、コード内でライブラリの機能を活用できるようになるため、非常に重要です。
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
前提条件が整ったので、メインイベントに進みましょう。PSD ファイルからサムネイルを作成するには、いくつかの簡単な手順が必要です。詳しく説明します。
## ステップ1: 環境を設定する
プロジェクトを開始し、サムネイル生成を準備する方法は次のとおりです。
1. Java プロジェクトを作成します。
   - IDE を開き、新しい Java プロジェクトを作成します。
   - 「PsdThumbnailGenerator」のような名前を付けます。
2. Aspose.PSD ライブラリを含める:
   -  Aspose.PSD JARファイルをプロジェクトのビルドパスに追加します。Mavenを使用している場合は、`pom.xml`:
     ```xml
     <dependency>
         <groupId>com.aspose</groupId>
         <artifactId>aspose-psd</artifactId>
         <version>your_version_here</version>
     </dependency>
     ```
## ステップ2: PSDファイルを読み込む
次に、サムネイルを作成する PSD ファイルを読み込む必要があります。 
1. ドキュメントディレクトリを指定します:
   PSD ファイルが配置されているディレクトリを定義します。
   ```java
   String dataDir = "Your Document Directory"; //あなたのパスに置き換えてください
   ```
2. PSD ファイルを読み込みます:
   使用`PsdImage` PSD ファイルを読み込むためのクラス。
   ```java
   PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
   ```
ここ、`sample.psd` PSD ファイルの名前です。ファイル名に応じて調整してください。
## ステップ3: PSDリソースを反復処理する
PSD イメージが読み込まれたので、次のステップではそのリソースを調べます。
1. リソース数を取得:
   PSD ファイル内のすべてのリソースをループします。
   ```java
   for (int i = 0; i < image.getImageResources().length; i++) {
       //処理リソース
   }
   ```
   
2. サムネイル リソースを識別します。
   ループ内で、リソースがサムネイルであるかどうかを確認します。
   ```java
   if (image.getImageResources()[i] instanceof ThumbnailResource) {
       //サムネイルを処理する
   }
   ```
## ステップ4: サムネイルを処理する
サムネイル リソースを識別したら、それに応じて処理する必要があります。
1. サムネイル形式の取得と確認:
   リソースが実際にサムネイルである場合は、それを取得してその形式を確認します。
   ```java
   ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
   if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
       //サムネイルを作成して保存する
   }
   ```
## ステップ5: サムネイルを作成して保存する
ここで魔法が起こります！サムネイル データから新しい画像を作成し、保存します。
1. 新しいイメージを作成する:
   サムネイル リソースの幅と高さを使用して、新しいビットマップ イメージを作成します。
   ```java
   PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
   ```
2. 新しい画像にピクセルを保存します。
   新しく作成した画像にサムネイルデータを転送します。
   ```java
   thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
   ```
3. サムネイル画像を保存します:
   最後に、サムネイル画像を一意の名前でドキュメント ディレクトリに保存します。
   ```java
   thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
   ```

## 結論
Java と Aspose.PSD を使用して PSD ファイルからサムネイルを作成するのは、扱いやすい手順に分解すれば簡単な作業になります。このチュートリアルでは、PSD ファイルからサムネイルを簡単に抽出できるようになり、ワークフローを強化する便利なツールが手に入ります。では、何があなたを妨げているのでしょうか? PSD ファイルを手に入れて、試してみましょう!
## よくある質問
### Aspose.PSD とは何ですか?
Aspose.PSD は、開発者が Photoshop ファイルを操作できるようにする Java ライブラリであり、PSD ファイルをプログラムで簡単に操作および管理できるようになります。
### Aspose.PSD を無料で使用できますか?
はい、Aspose では、ライセンスを購入する前にライブラリをテストできる無料トライアルを提供しています。
### サムネイルはどのような形式で保存できますか?
この例では、サムネイルを BMP 形式で保存しましたが、Aspose.PSD は他のさまざまな形式もサポートしています。
### Aspose.PSD を使用するには Photoshop をインストールする必要がありますか?
いいえ、Aspose.PSD は Photoshop とは独立して動作します。
### Aspose.PSD の詳細情報はどこで入手できますか?
ぜひチェックしてみてください[Aspose.PSD ドキュメント](https://reference.aspose.com/psd/java/)詳細、チュートリアル、リソースについてはこちらをご覧ください。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
