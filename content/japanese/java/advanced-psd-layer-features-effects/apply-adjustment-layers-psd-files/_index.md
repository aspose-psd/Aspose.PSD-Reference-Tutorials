---
title: Java を使用して PSD ファイルに調整レイヤーを適用する
linktitle: Java を使用して PSD ファイルに調整レイヤーを適用する
second_title: Aspose.PSD Java API
description: この開発者向けの完全なステップバイステップ ガイドでは、Aspose.PSD for Java を使用して PSD ファイルに調整レイヤーを適用する方法を学習します。
type: docs
weight: 15
url: /ja/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
---
## 導入
PSD ファイルに保存されている画像を強化したいと考えている Java 開発者ですか? そうであれば、この記事はまさにうってつけです。この記事では、Java 用の Aspose.PSD ライブラリを使用して PSD ファイルに調整レイヤーを適用する方法について説明します。個人プロジェクトで作業している場合でも、プロフェッショナル アプリケーションで作業している場合でも、PSD ファイルの操作方法を理解することで、ソフトウェアの機能を大幅に向上させることができます。 

## 前提条件
コードに進み、調整レイヤーの適用を開始する前に、必要な前提条件がいくつかあります。
1. Java開発キット（JDK）：マシンにJDKがインストールされていることを確認してください。ここからダウンロードできます。[Oracleのウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSDライブラリ:まだダウンロードしていない場合は、Java用のAspose.PSDライブラリをダウンロードする必要があります。[ここ](https://releases.aspose.com/psd/java/).
3. 開発環境: コードを記述して実行する IntelliJ IDEA や Eclipse などの Java 統合開発環境 (IDE) をセットアップします。
4. Java の基本的な知識: Java プログラミングの一般的な理解があれば、スムーズに理解できるようになります。
5. PSD ファイル: テスト用に PSD ファイルをいくつか用意しておきます。Adobe Photoshop を使用して作成するか、インターネットからサンプル ファイルをダウンロードすることができます。
## パッケージのインポート
コーディングを始める前に、どのパッケージをインポートする必要があるかを明確にしましょう。Aspose.PSD を使用すると、さまざまな方法で Photoshop ファイルを操作できるため、PSD 画像と調整レイヤーを処理するために必要なクラスを取得しましょう。
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```
パッケージの準備ができたので、例を段階的に説明していきましょう。
## ステップ1: PSDファイルを読み込む
最初のステップは、PSD ファイルを読み込むことです。これは、調整レイヤーを適用するために使用するファイルです。
```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```
このスニペットでは、PSDファイルが保存されているディレクトリを定義し、操作したい特定のファイルを読み込みます。`"Your Document Directory"`マシン上の PSD ファイルへの実際のパスを入力します。
## ステップ2: レイヤーを反復する
PSD ファイルを読み込んだので、そのレイヤーを反復処理して調整レイヤーを見つけます。
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) im.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(im.getLayers()[0]);
        }
    }
}
```
このステップでは、PSDファイルの各レイヤーをループして、`AdjustmentLayer`タイプ。見つかった場合は、通常最初のレイヤーであるベースレイヤーと結合します（`im.getLayers()[0]`）。この結合プロセスにより、画像に調整が効果的に適用されます。 
## ステップ3: 変更したPSDファイルを保存する
レイヤーを変更した後は、変更内容を保存することが重要です。次の手順でこれを実行しましょう。
```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```
ここでは、修正したPSDファイルのエクスポートパスを指定し、`save()`変更をディスクに書き込む方法。
## ステップ4: レベル調整レイヤー
別の種類の調整レイヤーであるレベル調整レイヤーに対してこのプロセスを繰り返してみましょう。 
### レベル調整レイヤーPSDを読み込む
```java
String sourceFileName2 = dataDir + "LevelsAdjustmentLayerRgb.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName2);
```
前と同様に、レベル調整レイヤーを含む PSD ファイルを読み込みます。 
### レベルレイヤーを反復処理する
次に、以前と同じようにレイヤーを再度ループしますが、今度は別の PSD ファイルで作業します。
```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) img.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(img.getLayers()[0]);
        }
    }
}
```
このコードは前の反復と同様に動作し、現在の PSD ファイル内の調整レイヤーを検索して、利用可能な調整を適用できるようにします。
## レベル調整レイヤーPSDを保存する
最後に、調整を適用した後、この新しいファイルを保存します。
```java
String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";
img.save(exportPath2);
```
これで、レベル調整レイヤーの処理が正常に完了しました。
## 結論
おめでとうございます。Java と Aspose.PSD ライブラリを使用して PSD ファイルに調整レイヤーを適用する方法を学習しました。色を微調整したり、レベルを調整したりする場合でも、PSD ファイルをプログラムで操作するための基礎スキルを習得できました。
Aspose.PSD を使用すると、画像編集のワークフローを大幅に効率化でき、従来のツールでは不可能だった自動化とカスタマイズが可能になります。ライブラリをさらに詳しく調べて、さまざまな種類のレイヤーを試し、どのようなクリエイティブな可能性があるのかを確認してください。
## よくある質問
### Aspose.PSD ライブラリとは何ですか?
Aspose.PSD は、開発者が Java アプリケーションで Photoshop PSD ファイルを読み込み、操作し、保存できるようにするライブラリです。
### Aspose.PSD を無料で使用できますか?
はい！Asposeでは、ライブラリを探索するための無料トライアルを提供しています。サインアップして[ここ](https://releases.aspose.com/).
### Aspose.PSD を使用するには Photoshop をインストールする必要がありますか?
いいえ、Photoshop は必要ありません。Aspose.PSD は独立して動作し、PSD ファイルをプログラムで操作します。
### Aspose.PSD のドキュメントはどこにありますか?
ドキュメントページをご覧ください[ここ](https://reference.aspose.com/psd/java/)機能、クラス、メソッドを調べます。
### Aspose 製品のサポートを受けるにはどうすればよいですか?
サポートは以下からアクセスできます。[Aspose フォーラム](https://forum.aspose.com/c/psd/34)質問したり解決策を見つけたりできる場所です。