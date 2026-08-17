---
date: 2026-03-07
description: Aspose.PSD for Java を使用して PSD ファイルにレベル調整レイヤーを追加し、レベルの調整方法を学びましょう。トーンの微調整をすばやくマスターできます。
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: レベルの調整方法 – PSDでレベル調整レイヤーを追加
url: /ja/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD にレベル調整レイヤーを追加する

## はじめに
Photoshop ドキュメントで **レベルの調整方法** を探しているなら、Level Adjustment Layer が最適なツールです。元のピクセルを永久に変更することなく、シャドウ、ミッドトーン、ハイライトを微調整できます。このチュートリアルでは、Aspose.PSD for Java を使用して PSD ファイルに Level Adjustment Layer を追加する手順を解説し、数ステップでプロフェッショナルなトーンコントロールを実現します。

## クイック回答
- **Level Adjustment Layer は何をしますか？** 画像のトーン範囲を非破壊的に変更します。  
- **使用されているライブラリは？** Aspose.PSD for Java。  
- **ライセンスは必要ですか？** 開発には無料トライアルで動作しますが、製品版ではライセンスが必要です。  
- **実装にどれくらい時間がかかりますか？** 基本的な調整で約10〜15分です。  
- **複数のチャンネルを調整できますか？** はい、各カラーチャンネルごとに入力/出力レベルを個別に設定できます。

## Level Adjustment Layer とは？
Level Adjustment Layer は、入力シャドウ、ミッドトーン、ハイライト、および出力レベルを調整することで画像のトーンバランスを補正できます。独立したレイヤーとして存在するため、可視性を切り替えたり削除したりしても、下のアートワークに影響を与えません。

## Aspose.PSD で Level Adjustment Layer を追加する理由
- **Automation（自動化）:** バッチ処理パイプラインにレベル調整を組み込めます。  
- **Cross‑platform（クロスプラットフォーム）:** Java をサポートするすべての OS で動作します。  
- **Precision（精度）:** 各チャンネルの設定にプログラムからアクセスでき、正確な結果が得られます。  

## 前提条件
1. Java Development Kit (JDK)。まだ持っていない場合は、[Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)からダウンロードするか、OpenJDK を使用してください。  
2. Aspose.PSD for Java ライブラリ – 最新の JAR はこの[ダウンロードリンク](https://releases.aspose.com/psd/java/)から取得してください。  
3. Java プログラミングの基本知識。  
4. IntelliJ IDEA、Eclipse、NetBeans などの IDE に Aspose.PSD JAR をクラスパスに追加した環境。  

## パッケージのインポート
コードを書き始める前に、Aspose.PSD ライブラリから必要なパッケージをインポートする必要があります。以下のように行います:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
これらのインポートにより、PSD ファイルの読み込み、Level Adjustment Layer の操作、個々のチャンネル設定の操作に必要なクラスが利用可能になります。

## PSD ファイルでレベルを調整する方法
以下は、プログラムで **レベルを調整する方法** をステップバイステップで示すガイドです。

### 手順 1: ファイルパスの設定
元の PSD がある場所と、編集後のファイルを保存する場所を定義します。
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
`"Your Document Directory"` を実際のフォルダパスに置き換えてください。

### 手順 2: PSD ファイルの読み込み
ソースファイルから `PsdImage` インスタンスを作成します。
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
これで PSD 内のすべてのレイヤーにフルアクセスできます。

### 手順 3: レイヤーの反復処理
変更したい Level Adjustment Layer を見つけます。
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
`instanceof LevelsLayer` のチェックにより、レベル調整レイヤーのみを対象にしていることが保証されます。

### 手順 4: レベルチャンネル設定の調整
選択したチャンネルの入力および出力値を調整します。
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Input Midtone Level（入力ミッドトーンレベル）:** ミッドトーンの範囲をシフトします。  
- **Input Shadow Level（入力シャドウレベル）:** シャドウを暗くしたり明るくしたりします。  
- **Input Highlight Level（入力ハイライトレベル）:** 最も明るい部分を制御します。  
- **Output Shadow/Highlight Levels（出力シャドウ/ハイライトレベル）:** 最終的な出力範囲を定義します。  

さまざまな値を試して、画像にどのように影響するか確認してください。

### 手順 5: 変更済み PSD ファイルの保存
変更を新しいファイルに保存します。
```java
im.save(psdPathAfterChange);
```
`psdPathAfterChange` で指定した場所に更新された PSD が保存されています。

## よくある問題と解決策
- **File not found（ファイルが見つかりません）:** `dataDir` が正しいフォルダを指しているか、元の PSD が存在するか確認してください。  
- **ClassCastException:** 読み込んでいるファイルが PSD であることを確認してください。他の形式は別のクラスが必要です。  
- **License errors（ライセンスエラー）:** 本番ビルドでは有効な Aspose.PSD ライセンスを使用してください。開発にはトライアルで動作します。

## 結論
これで、Aspose.PSD for Java を使用して PSD ファイルに Level Adjustment Layer を追加・設定し、**レベルを調整する方法** が分かりました。この手法により、トーンバランスを正確にコントロールしつつ、ワークフローを完全に自動化できます。さまざまなチャンネル値を試し、バッチ処理を活用して複数の画像に同じ調整を適用してみてください。

## よくある質問

**Q: Level Adjustment Layer とは何ですか？**  
A: 画像のトーン範囲（シャドウ、ミッドトーン、ハイライト）を変更できる非破壊的なレイヤーです。

**Q: ライセンスを購入せずに Aspose.PSD を使用できますか？**  
A: はい、無料トライアルでライブラリを評価できますが、商用展開にはライセンスが必要です。

**Q: Aspose.PSD のドキュメントはどこで見つけられますか？**  
A: ドキュメントは[こちら](https://reference.aspose.com/psd/java/)にあります。

**Q: Aspose 製品のコミュニティサポートはありますか？**  
A: もちろんです！質問やサポートは[Aspose フォーラム](https://forum.aspose.com/c/psd/34)で受けられます。

**Q: Aspose.PSD の一時ライセンスはどのように取得できますか？**  
A: [こちら](https://purchase.aspose.com/temporary-license/)から一時ライセンスを申請できます。

---

**最終更新日:** 2026-03-07  
**テスト環境:** Aspose.PSD latest version (Java)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}