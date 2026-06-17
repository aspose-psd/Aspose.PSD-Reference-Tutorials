---
date: 2026-04-08
description: Aspose.PSD for Java の一時ライセンスを使用して、PSD を PNG にエクスポートし、新しい PSD レイヤーを作成する方法を学びます。このステップバイステップのチュートリアルでは、PSD
  画像の操作とレイヤー位置の設定について解説します。
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: PSDに新しい通常レイヤーを追加
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して PSD を PNG にエクスポートし、新しい通常レイヤーを追加 – Aspose の一時ライセンス
url: /ja/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用して PSD を PNG にエクスポートし、新しい通常レイヤーを追加する

## はじめに

この **aspose psd tutorial** では、開発用に **aspose temporary license** を使用して、同じファイル内に **新しい通常レイヤーを作成** しながら **PSD を PNG にエクスポート** する方法を紹介します。Web 用サムネイルを生成したり、デザインパイプライン用のアセットを準備したり、単に **psd image manipulation** を試したりする必要がある場合でも、Aspose.PSD for Java は完全なプログラム制御を提供します。ソースファイルの読み込みから、更新された PSD と PNG の両方の保存まで、すべての手順を順に説明するので、すぐに PSD レイヤーの操作を開始できます。

## クイック回答
- **PSD を PNG に一度の呼び出しでエクスポートできますか？** はい、レイヤーを追加した後、`save` を `PngOptions` と共に呼び出すことができます。
- **開発にライセンスは必要ですか？** テスト用には一時ライセンスで動作しますが、本番環境ではフルライセンスが必要です。
- **サポートされている Java バージョンはどれですか？** Aspose.PSD は Java 8 以降をサポートしています。
- **レイヤーの位置指定はピクセル単位ですか？** はい、**set layer position** メソッドを使用して左、上、右、下の座標をピクセルで設定します。
- **PNG はレイヤーの透明性を保持しますか？** PNG にはすべての可視レイヤーがマージされた結果が含まれます。

## なぜ Aspose の一時ライセンスを使用するのか？

**aspose temporary license** を使用すると、機能制限なしで Aspose.PSD のすべての機能を評価できます。評価用の透かしが除去され、すべての API がロック解除され、**create new psd layer** オブジェクトの作成も可能になります。永久ライセンスを購入する前に、実稼働に近い環境でコードをテストできます。

## 前提条件

開始する前に、以下を用意してください。

- **Java Development Environment** – JDK 8+ とビルドツール（Maven/Gradle）をインストール。
- **Aspose.PSD for Java** – 公式サイトから最新の JAR をダウンロード [here](https://releases.aspose.com/psd/java/)。
- **サンプル PSD ファイル** – 例では `OneLayer.psd` を使用します。

## パッケージのインポート

Java クラスに必要なインポートを追加します。これらのクラスは **psd image manipulation** とレイヤー処理のコア機能を提供します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 「set layer position」とは何か、そしてなぜ重要なのか

新しいレイヤーを追加する際、キャンバス上の表示位置を定義する必要があります。`setLeft`、`setTop`、`setRight`、`setBottom` メソッドはピクセル座標で **set layer position** を設定します。正確な位置合わせは、UI アセットの合成や印刷用ファイルの準備など、期待通りにグラフィックを配置するために不可欠です。

## ステップバイステップガイド

### ステップ 1: PSD ファイルをロードする

まず、変更したい既存の PSD をロードします。これにより操作可能な `PsdImage` オブジェクトが取得できます。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### ステップ 2: ピクセルデータと矩形を準備する

2 つのピクセルバッファ（`int[]`）を作成し、新しいレイヤーが描画される矩形領域を定義します。これは **creating a new psd layer** の基礎となります。

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### ステップ 3: レイヤーデータを初期化する

ピクセルバッファにデフォルトの ARGB 値を設定します。値 `-10000000` は半透明の暗い色に相当します。

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### ステップ 4: 通常レイヤーを追加する（PSD レイヤーを操作）

ここで **add regular layers** を PSD 画像に追加し、左・上・右・下のプロパティを使用して **set layer position** を設定します。これにより **manipulate PSD layers** をプログラムで行う方法が示されます。

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### ステップ 5: PSD を PNG にエクスポートし、更新された PSD を保存する

レイヤーが配置されたら、変更されたドキュメントを保存します。まず結果を PNG にエクスポート（**export psd to png** 手順）し、次に新しいレイヤーを含む PSD を永続化します。

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **プロのコツ：** PNG だけが必要な場合は、PSD の `save` 呼び出しを省略し、`PngOptions` で直接 `save` を呼び出すことができます。

## 一般的な問題とトラブルシューティング

| 症状 | 考えられる原因 | 対処法 |
|---------|--------------|-----|
| PNG が空白になる | レイヤーが非表示または完全に透明です | 非透明のピクセル値を設定するか、`layer.setVisible(true)` を呼び出してください。 |
| `ArrayIndexOutOfBoundsException` | 矩形サイズとピクセル配列の長さが一致しません | `rect.width * rect.height == dataArray.length` を確認してください。 |
| LicenseException at runtime | 有効なライセンスがロードされていません | 任意の API メソッドを呼び出す前に、一時または永久ライセンスをロードしてください。 |

## よくある質問

**Q: Aspose.PSD は Java 8 と互換性がありますか？**  
A: はい、Aspose.PSD は Java 8 以降をサポートしています。

**Q: 追加したレイヤーに変換（回転、スケール）を適用できますか？**  
A: もちろんです！`Layer` クラスは `rotate`、`scale`、`translate` などのメソッドを提供し、完全な変換制御が可能です。

**Q: 追加の Aspose.PSD ドキュメントはどこで見つけられますか？**  
A: 詳細な API ドキュメントは [here](https://reference.aspose.com/psd/java/) にあります。

**Q: Aspose.PSD の一時ライセンスはどう取得しますか？**  
A: 一時ライセンスの取得は [here](https://purchase.aspose.com/temporary-license/) から行えます。

**Q: Aspose.PSD のサポート用コミュニティフォーラムはありますか？**  
A: はい、Aspose フォーラムの [here](https://forum.aspose.com/c/psd/34) でディスカッションに参加できます。

## 結論

これで Aspose.PSD for Java を使用して **PSD を PNG にエクスポートしながら新しい通常レイヤーを追加** する方法と、**aspose temporary license** によって制限なしでこのワークフローを試す方法を学びました。このチュートリアルは、ファイルの読み込み、レイヤーの作成、ピクセルデータの設定、最終的な合成のエクスポートという **psd image manipulation** のコア機能を示しています。矩形サイズやピクセル色、レイヤー効果を自由に変更して、プロジェクトの要件に合わせた出力を作成してください。

---

**最終更新日:** 2026-04-08  
**テスト環境:** Aspose.PSD 24.11 for Java  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}