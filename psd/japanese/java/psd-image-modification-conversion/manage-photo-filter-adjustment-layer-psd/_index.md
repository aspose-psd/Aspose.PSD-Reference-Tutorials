---
date: 2026-03-28
description: Aspose.PSD for Java を使用して、写真フィルターレイヤーの作成方法と調整レイヤーを含む PSD ファイルの追加方法を学びましょう。このガイドに従って、フィルターの編集と追加を簡単に行えます。
linktitle: How to Create Photo Filter Layer in PSD Using Java
second_title: Aspose.PSD Java API
title: JavaでPSDに写真フィルター レイヤーを作成する方法
url: /ja/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD のフォトフィルター調整レイヤーの管理 - Java

## はじめに
Java 開発者で、PSD ファイル内に **create photo filter layer** オブジェクトを作成したい方は、正しい場所に来ました。このチュートリアルでは、Aspose.PSD for Java を使用して既存の Photo Filter Adjustment Layer を編集し、新しいレイヤーを追加する方法を解説します。最後まで読むと、**create photo filter layer** の作成方法、プロパティの調整方法、さらには **add adjustment layer PSD** ファイルをプログラムで追加する方法が正確に分かり、グラフィックデザインのワークフローが高速化されます。

## クイック回答
- **Java で PSD レイヤーを扱うライブラリはどれですか？** Aspose.PSD for Java  
- **既存の Photo Filter レイヤーを編集できますか？** Yes – PSD をロードし、`PhotoFilterLayer` を見つけて、プロパティを変更します。  
- **新しいフィルター レイヤーを追加するには？** `PsdImage` インスタンスに対して `addPhotoFilterLayer(Color)` を使用します。  
- **本番環境でライセンスが必要ですか？** 商用ライセンスが必要です。無料トライアルが利用可能です。  
- **サポートされている Java バージョンは何ですか？** JDK 8 以上 (JDK 11 推奨)。  

## Photo Filter Adjustment Layer とは何ですか？
Photo Filter Adjustment Layer は、選択した色で画像全体に色調を付ける非破壊的エフェクトで、写真フィルターを適用するのと似ています。レイヤーとして独立して存在し、元のピクセルを変更せずに色、密度、明度を調整できます。

## なぜ Aspose.PSD を使ってフォトフィルター レイヤーを作成するのか？
- **フルコントロール**: Adobe Photoshop なしで PSD 構造を完全に制御できます。  
- **クロスプラットフォーム** Java API は Windows、Linux、macOS で動作します。  
- **COM インターロップなし** – 純粋な Java で、サーバーサイド処理に最適です。  
- **PSD バージョン 1‑8 をサポート**し、レイヤー効果とマスクを保持します。  

## 前提条件
### 必須ソフトウェア
1. Java Development Kit (JDK): マシンに互換性のある JDK がインストールされていることを確認してください。[Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) からダウンロードできます。  
2. Aspose.PSD for Java: PSD ファイルを操作するには Aspose.PSD ライブラリが必要です。[Aspose のリリースページ](https://releases.aspose.com/psd/java/) からダウンロードできます。[Aspose のドキュメント](https://reference.aspose.com/psd/java/) も確認してください。  
3. IDE（統合開発環境）：IntelliJ IDEA や Eclipse などの優れた IDE を使用すると、コーディングがスムーズになります。  

### 基本の理解
Java プログラミングに慣れており、PSD ファイルの基本的な仕組みを理解していると役立ちます。Java でライブラリを使用するのが初めての場合は、インポートやフレームワークの利用方法に慣れることをお勧めします。

## パッケージのインポート
始めるには、Aspose.PSD ライブラリから必要なクラスをインポートする必要があります。以下は Java ファイルの冒頭で必要となるシンプルなインポート文です：
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
このコードを Java ファイルの先頭に貼り付ければ、PSD 画像の操作を開始できるようになります！

## 既存の Photo Filter レイヤーの編集
### ステップ 1: データディレクトリの設定
まず、PSD ファイルが保存されているディレクトリを定義する必要があります。`"Your Document Directory"` を実際のパスに置き換えてください。以下のように整理します：
```java
String dataDir = "Your Document Directory";
```

### ステップ 2: PSD ファイルのロード
次に、編集したい PSD ファイルをロードします。指定したディレクトリに `PhotoFilterAdjustmentLayer.psd` が存在することを確認してください。
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```

### ステップ 3: 画像オブジェクトの初期化
Aspose の組み込み機能を使用して、画像をプロジェクトにロードします：
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### ステップ 4: レイヤーの反復処理
次に、PSD ファイル内のレイヤーを調べます。目的は `PhotoFilterLayer` を見つけることです：
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // Make changes to the layer
    }
}
```

### ステップ 5: Photo Filter レイヤーのカスタマイズ
ここが本番です！`Color` と `Density` を変更できます。例えば、鮮やかな赤色に設定し、密度を調整することができます：
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```

### ステップ 6: 編集した PSD ファイルの保存
最後に、変更を保存して調整済みの新しい PSD ファイルを作成します：
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
これで PSD ファイル内の Photo Filter Adjustment Layer を編集しました。

## 新しい Photo Filter レイヤーの追加
### ステップ 1: ディレクトリパスの設定
前と同様に、データディレクトリを定義します：
```java
String dataDir = "Your Document Directory";
```

### ステップ 2: ソースファイルのロード
この例では、**add adjustment layer PSD** を追加したい別の PSD ファイルをロードします：
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```

### ステップ 3: 画像オブジェクトの再初期化
新しい `PsdImage` インスタンスを作成する必要があるので、ファイルをロードします：
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### ステップ 4: Photo Filter レイヤーの追加
これで、カスタマイズした色で新しい Photo Filter レイヤーを追加できます。手順は以下の通りです：
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```

### ステップ 5: 新しい PSD ファイルの保存
再び、変更を保存する時です。以下の行で実行できます：
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
これで PSD ファイルに新しいフォトフィルター レイヤーを正常に追加しました。

## 一般的な問題と解決策
- **画像をロードするときの `ClassCastException`** – ロードするファイルが PSD であることを確認してください。他の形式は別のクラスが必要です。  
- **カラー値が正しく表示されない** – 各コンポーネントが 0‑255 の `Color.fromArgb(alpha, red, green, blue)` を使用してください。  
- **レイヤーが見つからない** – ソース PSD に実際に `PhotoFilterLayer` が含まれているか確認してください。デバッグには `im.getLayers().length` を使用します。  

## よくある質問
### Aspose.PSD とは何ですか？
Aspose.PSD は、PSD ファイルの作成、編集、変換を行う .NET および Java 用ライブラリです。

### Aspose.PSD を無料で試せますか？
はい、Aspose は無料トライアル版を提供しています。[こちら](https://releases.aspose.com/) で確認してください。

### ドキュメントはどこで見つけられますか？
完全なドキュメントは [Aspose のリファレンスページ](https://reference.aspose.com/psd/java/) にあります。

### Aspose.PSD の購入方法は？
ソフトウェアは [このリンク](https://purchase.aspose.com/buy) から購入できます。

### Aspose.PSD のサポートはありますか？
もちろんです！Aspose のサポートフォーラム [こちら](https://forum.aspose.com/c/psd/34) でサポートを受けられます。

---

**最終更新日:** 2026-03-28  
**テスト環境:** Aspose.PSD for Java 24.11 (2026 年時点の最新)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}