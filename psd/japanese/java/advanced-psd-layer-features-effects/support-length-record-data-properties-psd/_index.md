---
title: PSD で長さレコード データ プロパティをサポート - Java
linktitle: PSD で長さレコード データ プロパティをサポート - Java
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用して、Java で長さレコード データ プロパティを持つ PSD ファイルを操作する方法を学びます。詳細については、このステップ バイ ステップ ガイドに従ってください。
weight: 14
url: /ja/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD で長さレコード データ プロパティをサポート - Java

## 導入
Photoshop ファイルを操作していて、レイヤーや図形をプログラムで操作したいと思ったことはありませんか? もしそうなら、Aspose.PSD for Java ライブラリの素晴らしさに気付いたことでしょう。この強力なツールにより、開発者は Java コードを通じてシームレスに PSD ファイルを操作し、変更することができます。本日の記事では、このライブラリを使用して PSD ファイルの長さレコード データ プロパティをサポートする方法について詳しく説明します。 
熟練した Java 開発者でも、初心者でも、このガイドでは必要な知識をすべてステップごとに説明します。最後まで読めば、快適な Java 環境を離れることなく、PSD ファイルを開いてベクター シェイプのプロパティを変更し、変更を保存できるようになります。さあ、さっそく始めましょう!
## 前提条件
始める前に、準備しておくべきものがいくつかあります。すべてが整っていることを確かめておくと、プロセスがスムーズになります。土壇場で慌てるのは誰も望まないことです。必要なものは次のとおりです。
1.  Java開発キット（JDK）：マシンにJDKがインストールされていることを確認してください。ここからダウンロードできます。[Oracleのウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)またはパッケージ マネージャーを使用します。
2.  Aspose.PSD for Javaライブラリ: Aspose.PSD for Javaライブラリをダウンロードしてプロジェクトに含める必要があります。[Aspose リリース ページ](https://releases.aspose.com/psd/java/).
3. IDE: コードをより適切に処理するには、IntelliJ IDEA、Eclipse、または任意の Java IDE などの統合開発環境 (IDE) を使用します。
4. PSD ファイル: このチュートリアルでは、作業用の PSD ファイルが必要です。Adobe Photoshop で作成するか、サンプルの PSD をダウンロードしてください。
5. 基本的な Java の知識: Java 構文に精通していると、簡単に理解できるようになります。
## パッケージのインポート
これですべての前提条件が整いました。次のステップは必要なパッケージをインポートすることです。このステップは、これから使用するクラスとメソッドにアクセスするために重要です。以下は、Java プロジェクトに必要なパッケージをインポートする方法の例です。
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```
これらのインポートにより、PSD ファイルの操作に取り掛かる準備が整いました。

## ステップ1: ソースディレクトリと出力ディレクトリを設定する
ファイルをロードする前に、入力 PSD ファイルの取得元と変更したファイルの保存場所を指定しましょう。ローカル マシンに応じてディレクトリ パスを調整します。
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```
## ステップ2: PSDファイルを読み込む
 PSDファイルをロードしましょう！これには、`Image.load` Aspose.PSD ライブラリのメソッド。このメソッドを使用すると、PSD ファイルを開いて、そのレイヤーとリソースにアクセスできます。
```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```
本を開くのと同じように、ページ（レイヤーとリソース）を参照できます。
## ステップ3: レイヤー内のVsmsリソースを見つける
次に、PSD ファイル内の特定の VsmsResource を見つける必要があります。これらのリソースには、ベクター シェイプ レイヤーのデータが格納されています。ここで魔法が起こります。このスニペットでは、レイヤーのリソースをループしてこのリソースを見つけます。
```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```
宝探しのように、レイヤーを検索して貴重なベクター データを見つけます。
## ステップ4: 長さレコードにアクセスする
VsmsResource を取得したら、LengthRecord オブジェクトを抽出できます。各 LengthRecord はベクター シェイプ内のパスを表します。ここでは、3 つの LengthRecord にアクセスして、そのプロパティを操作します。
```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```
まるで絵画のどの部分を修正したいかを選択するようなものです。
## ステップ5: パス操作プロパティを変更する
次は楽しい部分、つまりパスのプロパティの変更です。ここでは、setPathOperations メソッドを使用して、図形同士の相互作用を変更できます。重なり合う領域を除外したり、前面の図形を背面から減算したりする操作を設定できます。
```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```
ケーキの層を調整するようなものだと想像してください。スライスの仕方によって、各層は異なる相互作用をします。
## ステップ6: 変更したPSDファイルを保存する
必要な変更を行った後、次のステップは変更した PSD ファイルを保存することです。ここで、これまでの努力が報われます。 
```java
psdImage.save(outPsdFilePath);
```
あなたの傑作が、世界に公開できるようきれいに梱包されました!
## ステップ7: リソースをクリーンアップする
最後に、メモリとリソースを解放するために使用したオブジェクトを破棄することが重要です。
```java
psdImage.dispose();
```
アートプロジェクトの後に作業スペースを掃除し、すべてがきちんと整頓されていることを確認するようなものだと考えてください。
## 結論
これで完了です。Aspose.PSD for Java を使用して PSD ファイルの長さレコード データ プロパティをサポートする包括的なチュートリアルが完了しました。ファイルの読み込みから図形プロパティの変更、最終製品の保存まで、各ステップでこのライブラリの威力が明らかになります。クリエイティブなプロジェクトに取り組んでいる場合でも、グラフィック アセットを自動化している場合でも、Aspose.PSD はまったく新しい可能性の世界を開きます。始める準備はできましたか? PSD ファイルに飛び込んで、創造性を解き放ちましょう。
## よくある質問
### Aspose.PSD for Java とは何ですか?
Aspose.PSD for Java は、開発者が Java を使用してプログラム的に Photoshop PSD ファイルを操作および操作できるようにするライブラリです。
### Aspose.PSD を無料プロジェクトで使用できますか?
はい、Aspose Web サイトで入手可能な試用版を使用して、ライブラリを無料で試すことができます。
### PSD ファイルにはどのような変更を加えることができますか?
PSD ファイル内で、レイヤー、シェイプ、テキスト、パス操作などを操作できます。
### Aspose.PSD は他のプログラミング言語と互換性がありますか?
はい、Aspose は .NET や Python など、さまざまなプログラミング言語用のさまざまなライブラリを提供しています。
### Aspose.PSD のドキュメントはどこにありますか?
完全なドキュメントにアクセスできます[ここ](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
