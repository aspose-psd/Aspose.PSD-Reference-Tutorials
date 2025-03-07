---
title: PSDにレベル調整レイヤーを追加する
linktitle: PSDにレベル調整レイヤーを追加する
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して PSD ファイルにレベル調整レイヤーを効果的に追加する方法を学習します。画像編集スキルを向上させます。
weight: 16
url: /ja/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSDにレベル調整レイヤーを追加する

## 導入
画像編集では、レベルを管理すると、写真の鮮やかさと鮮明さに大きく影響します。Photoshop の便利なツールの 1 つに「レベル調整レイヤー」があります。これを使用すると、画像の色調範囲と色バランスを微調整できます。このガイドでは、Aspose.PSD for Java を使用して PSD ファイルにレベル調整レイヤーを実装する方法を説明します。それでは、Java IDE を入手してください。
## 前提条件
レベル調整の世界に飛び込む前に、スムーズな走行を確保するためにいくつかの設定を行う必要があります。
1.  Java開発キット（JDK）：マシンにJDKがインストールされていることを確認してください。インストールされていない場合は、[Oracleのウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)または OpenJDK を使用します。
2.  Aspose.PSD for Javaライブラリ: PSDファイルを操作するには、Aspose.PSDライブラリをダウンロードする必要があります。最新バージョンはここから入手できます。[ダウンロードリンク](https://releases.aspose.com/psd/java/)プロジェクトのライブラリに JAR が含まれていることを確認します。
3. Java の基礎知識: このチュートリアルではコード スニペットを詳しく説明するため、Java プログラミングの基礎を理解しておくと役立ちます。
4. IDE のセットアップ: IntelliJ IDEA、Eclipse、NetBeans など、任意の Java IDE を使用してコードを記述および実行できます。Java プロジェクトをセットアップし、Aspose.PSD ライブラリを追加したことを確認してください。

## パッケージのインポート
コードの記述を始める前に、Aspose.PSD ライブラリから必要なパッケージをインポートする必要があります。手順は次のとおりです。
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
これらのパッケージをインポートすることで、PSD ファイルの読み込み、変更、保存に必要なクラスにアクセスできるようになります。

それでは、プロセスをわかりやすいステップに分解してみましょう。PSD ファイルの読み込み、レベルの調整、変更の保存の手順を順を追って説明します。 
## ステップ1: ファイルパスを設定する
最初のステップは、PSD ファイルの場所と、変更した出力を保存する場所を定義することです。ディレクトリ パスは、ニーズに合わせてカスタマイズできます。
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
ここで、`"Your Document Directory"`PSD ファイルが保存されているシステム上の実際のパスを入力します。これで、次に行うすべての作業の準備が整います。
## ステップ2: PSDファイルを読み込む
さて、PSDファイルを読み込みましょう。`PsdImage`クラス。このステップは、レイヤーにアクセスして操作できるようにするため不可欠です。
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
電話すると`Image.load()`PSDファイルを読み込み、インスタンスを作成します。`PsdImage`一緒に働くことができるもの。
## ステップ3: レイヤーを反復する
レベル調整レイヤーを調整したいので、PSD ファイル内の各レイヤーをループする必要があります。これにより、変更する特定のレイヤーを見つけることができます。
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        //さらなる操作はここで行われます...
    }
}
```
このループでは、`instanceof LevelsLayer`現在のレイヤーがレベル調整レイヤーであるかどうかを確認します。そうである場合は、そのプロパティの調整に進むことができます。
## ステップ4: レベルチャンネル設定を調整する
正しいレイヤーを特定したら、その入力レベルと出力レベルを変更できます。ここで魔法が起こります。さまざまなパラメータを調整して、画像にどのような影響を与えるかを確認します。
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
各パラメータの機能は次のとおりです。
- 入力中間トーンレベル: 中間トーンを調整します。
- 入力シャドウ レベル: 画像の暗い領域を微調整します。
- 入力ハイライト レベル: 画像の明るい領域を変更します。
- 出力シャドウ レベル: 暗いシャドウの表示方法を設定します。
- 出力ハイライト レベル: ライトのハイライトの表示方法を設定します。
さまざまな値を自由に試してみてください。
## ステップ5: 変更したPSDファイルを保存する
調整が完了したら、変更した PSD ファイルを保存します。この手順は、変更が適用され、保存されることを確認するために重要です。
```java
im.save(psdPathAfterChange);
```
調整されたPSDファイルは、指定された場所にあります。`psdPathAfterChange`. 
## 結論
Aspose.PSD for Java を使用して PSD ファイルにレベル調整レイヤーを追加する方法を学習しました。このガイドに従うことで、画像の色調品質を簡単に調整し、より鮮やかで視覚的に魅力的な出力を実現できます。練習を重ねれば完璧になります。自由に調整を微調整し、さまざまな PSD ファイルを調べて変更の効果を確認してください。
## よくある質問
### レベル調整レイヤーとは何ですか?
レベル調整レイヤーを使用すると、画像の色調範囲を修正し、シャドウ、中間調、ハイライトのバランスをとることができます。
### Aspose.PSD を購入せずに使用できますか?
はい！Aspose では、購入前にライブラリをテストできる無料トライアルを提供しています。
### Aspose.PSD のドキュメントはどこにありますか?
ドキュメントは以下からご覧いただけます[ここ](https://reference.aspose.com/psd/java/).
### Aspose 製品に対するコミュニティ サポートはありますか?
もちろんです！質問やサポートは[Aspose フォーラム](https://forum.aspose.com/c/psd/34).
### Aspose.PSD の一時ライセンスを取得するにはどうすればよいですか?
一時免許を申請することができます[ここ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
