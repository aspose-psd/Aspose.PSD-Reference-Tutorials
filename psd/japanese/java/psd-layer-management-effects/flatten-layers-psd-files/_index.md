---
title: Aspose.PSD Java を使用して PSD ファイルのレイヤーをフラット化する
linktitle: Aspose.PSD Java を使用して PSD ファイルのレイヤーをフラット化する
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用すると、PSD ファイル内のレイヤーを簡単にフラット化および結合できます。このステップ バイ ステップ ガイドに従って、PSD ファイルの管理を簡素化してください。
type: docs
weight: 13
url: /ja/java/psd-layer-management-effects/flatten-layers-psd-files/
---
## 導入

Photoshop ファイルで作業していて、複雑なレイヤーをもっと簡単に管理したいと思ったことはありませんか? いいえ、そんなことはありません! 今日は、プログラムで PSD ファイルを簡単に操作できる強力なツールである Aspose.PSD for Java の世界に飛び込みます。ここで取り上げる便利な機能の 1 つは、レイヤーのフラット化です。画像全体をフラット化する場合も、特定のレイヤーを選択的に結合する場合も、Aspose.PSD for Java が対応します。このチュートリアルでは、PSD ファイルに自信を持って取り組めるように、プロセスをステップごとに説明します。

## 前提条件

コードに進む前に、必要なものがすべて揃っていることを確認しましょう。

1. Java 開発キット (JDK): システムに JDK 8 以降がインストールされていることを確認してください。
2.  Aspose.PSD for Java: Aspose.PSDライブラリをダウンロードしてプロジェクトに追加します。[ここ](https://releases.aspose.com/psd/java/).
3. 統合開発環境 (IDE): IntelliJ IDEA や Eclipse などの IDE を使用すると、コーディング作業がよりスムーズになります。
4. Java の基本知識: このチュートリアルは初心者向けですが、Java の基本的な知識があれば、より簡単に理解できるようになります。
5. サンプル PSD ファイル: 実験用の PSD ファイルを用意します。複数のレイヤーを持つファイルを使用して、フラット化のプロセスを説明します。

基本的な部分は終わったので、楽しい部分、つまりコードの操作に取り掛かりましょう。

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートする必要があります。これらのパッケージを使用すると、Aspose.PSD for Java を使用して PSD ファイルを操作できるようになります。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

これらのインポートにより、PSD ファイルを読み込み、レイヤーを操作し、変更を保存できるようになります。次に、レイヤーをフラット化するプロセスを管理しやすいステップに分解してみましょう。

## ステップ1: PSD画像全体をフラット化する

最初のタスクは、PSD 画像全体をフラット化することです。これは、すべてのレイヤーを 1 つのレイヤーに結合して、画像の管理とエクスポートを容易にしたい場合に便利です。

### 1.1 PSDファイルを読み込む

まず、PSDファイルをプログラムに読み込みます。このファイルはプロジェクトディレクトリに配置する必要があります。`Your Document Directory`.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

このコードスニペットは、次の名前のPSDファイルを読み込みます。`ThreeRegularLayersSemiTransparent.psd`指定したディレクトリから。

### 1.2 画像を平坦化する

次に、画像全体をフラット化します。フラット化により、表示されているすべてのレイヤーが 1 つの背景レイヤーに結合されます。

```java
im.flattenImage();
```

このワンライナーを使用すると、PSD ファイル内のすべてのレイヤーが 1 つに結合されます。

### 1.3 フラット化された画像を保存する

最後に、フラット化された画像を新しいファイルに保存します。

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

これにより、フラット化されたPSDファイルが新しい名前で保存されます。`ThreeRegularLayersSemiTransparentFlattened.psd`おめでとうございます。Aspose.PSD for Java を使用して最初の PSD イメージをフラット化しました。

## ステップ2: 特定のレイヤーを結合する

場合によっては、画像全体をフラット化するのではなく、特定のレイヤーだけを結合したい場合があります。それを実現する方法を見てみましょう。

### 2.1 PSDファイルを再度読み込む

別の操作を実行するため、まず PSD ファイルを再度読み込みます。

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

これにより、同じ PSD ファイルが読み込まれ、レイヤー固有の操作の準備が整います。

### 2.2 レイヤーの識別と選択

特定のレイヤーを結合するには、まず結合するレイヤーを識別して選択します。

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

ここでは、PSD ファイルの 1 番目、2 番目、3 番目のレイヤーを選択しています。これらのレイヤーは配列に保存されており、インデックスでアクセスできます。

### 2.3 レイヤーを結合する

次に、選択したレイヤーを結合します。まず、下のレイヤーと中間のレイヤーを結合し、その結果を上のレイヤーと結合します。

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

このコードはレイヤーを順番にマージし、単一の結合されたレイヤーを生成します。

### 2.4 既存のレイヤーを結合したレイヤーに置き換える

結合後、画像内の既存のレイヤーを新しく結合したレイヤーに置き換える必要があります。

```java
img.setLayers(new Layer[]{layer2});
```

この手順により、画像には結合されたレイヤーのみが含まれるようになります。

### 2.5 更新されたPSDファイルを保存する

最後に、レイヤーを結合した更新された PSD ファイルを保存します。

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

これにより、結合されたレイヤーを含む PSD が新しい名前で保存され、元のファイルをそのまま保持できます。

## 結論

PSD ファイル内のレイヤーの操作は、迷路を進むような感じがすることがよくありますが、Aspose.PSD for Java を使用すると、地図を手に持っているような感覚になります。画像全体をフラット化する必要がある場合でも、選択したレイヤーを慎重に結合する必要がある場合でも、Aspose.PSD はプロセスを簡素化し、困難なタスクを簡単な操作に変えます。このチュートリアルに従うことで、Java を使用して PSD ファイル内のレイヤー操作を問題なく処理できるようになります。独自のプロジェクトで試してみて、どれだけの時間と労力を節約できるかを確認してください。

## よくある質問

### Aspose.PSD でレイヤーのフラット化を元に戻すことはできますか?  
いいえ、Aspose.PSD を使用してレイヤーをフラット化すると、その操作は元に戻せません。元のファイルのバックアップを常に保存しておくことをお勧めします。

### 表示されているレイヤーのみをフラット化することは可能ですか?  
はい、表示に基づいてどのレイヤーをフラット化するかを制御できます。フラット化したいレイヤーのみが表示されるようにしてから、`flattenImage`方法。

### レイヤーをフラット化するとファイルサイズは小さくなりますか?  
レイヤーをフラット化すると、特に複雑なレイヤーが多数ある場合にファイル サイズを削減できます。ただし、削減される正確な量はレイヤーの内容によって異なります。

### 異なるブレンドモードのレイヤーを結合できますか?  
はい、Aspose.PSD を使用して異なるブレンド モードのレイヤーを結合することができ、結果のレイヤーは結合されたレイヤーの外観を維持します。

### 隣接していないレイヤーを結合しようとするとどうなりますか?  
Aspose.PSD では、レイヤー スタック内の順序に関係なく、任意のレイヤーを結合できます。結合プロセスでは、選択したレイヤーが指定どおりに結合します。