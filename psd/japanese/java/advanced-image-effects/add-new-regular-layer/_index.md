---
title: Aspose.PSD for Java を使用して PSD に新しい通常レイヤーを追加する
linktitle: PSDに新しい通常レイヤーを追加する
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して PSD ファイルに新しい通常レイヤーを追加する方法を学びます。シームレスな PSD 操作については、ステップバイステップ ガイドに従ってください。
weight: 11
url: /ja/java/advanced-image-effects/add-new-regular-layer/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用して PSD に新しい通常レイヤーを追加する

## 導入

Aspose.PSD for Java を使用して PSD ファイルに新しい通常レイヤーを追加する方法を解説する包括的なチュートリアルへようこそ。Aspose.PSD は、開発者が PSD ファイルを効率的に操作および操作できるようにする強力な Java ライブラリです。このチュートリアルでは、詳細な手順とコード例を示しながら、PSD ファイルに新しい通常レイヤーを追加するプロセスを説明します。

## 前提条件

チュートリアルに進む前に、次の前提条件が満たされていることを確認してください。

- Java 開発環境: システムに Java 開発環境が設定されていることを確認します。
-  Aspose.PSDライブラリ: Aspose.PSD for Javaライブラリをダウンロードしてインストールします。ライブラリは次の場所にあります。[ここ](https://releases.aspose.com/psd/java/).

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。これらのパッケージは、Aspose.PSD 機能を使用するために不可欠です。Java ファイルの先頭に次の行を含めます。

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## ステップ1: PSDファイルを読み込む

次のコードを使用して、編集する PSD ファイルを読み込みます。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## ステップ2: データ配列と四角形を準備する

次のように 2 つの int 配列と 2 つの Rectangle オブジェクトを準備します。

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## ステップ3: レイヤーデータを初期化する

データ配列をデフォルト値で初期化します。

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## ステップ4: 通常のレイヤーを追加する

PSD 画像に 2 つの通常レイヤーを追加します。

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

## ステップ5: PSDとPNGを保存する

変更した PSD ファイルと追加の PNG ファイルを保存します。

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

おめでとうございます! Aspose.PSD for Java を使用して、PSD ファイルに新しい通常レイヤーを正常に追加しました。

## 結論

このチュートリアルでは、Aspose.PSD for Java を使用して PSD ファイルに新しい通常レイヤーを追加するプロセスを説明しました。この強力なライブラリは PSD 操作を簡素化し、Java 開発者が利用できるようにします。さまざまなパラメーターと機能を試して、Aspose.PSD の可能性を最大限に引き出してください。

## よくある質問

### Q1: Aspose.PSD は Java 8 と互換性がありますか?

A1: はい、Aspose.PSD は Java 8 以降のバージョンをサポートしています。

### Q2: 追加したレイヤーに変換を適用できますか?

A2: もちろんです! Aspose.PSD には、レイヤーのさまざまな変換オプションが用意されています。

### Q3: Aspose.PSD の追加ドキュメントはどこで入手できますか?

 A3: ドキュメントを参照してください[ここ](https://reference.aspose.com/psd/java/).

### Q4: Aspose.PSD の一時ライセンスを取得するにはどうすればよいですか?

 A4: 訪問[このリンク](https://purchase.aspose.com/temporary-license/)一時ライセンスのオプション。

### Q5: Aspose.PSD サポートのコミュニティ フォーラムはありますか?

 A5: はい、サポートやディスカッションは見つかります[ここ](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
