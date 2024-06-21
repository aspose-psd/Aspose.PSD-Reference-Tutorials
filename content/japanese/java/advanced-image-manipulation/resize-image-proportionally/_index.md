---
title: Aspose.PSD for Java を使用して画像のサイズを比例的に変更する
linktitle: 画像のサイズを比例的に変更する
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用して Java アプリケーションを強化します。ガイドに従って、画像のサイズを比例的に簡単に変更してください。今すぐ画像処理能力を強化しましょう。
type: docs
weight: 17
url: /ja/java/advanced-image-manipulation/resize-image-proportionally/
---
## 導入

Aspose.PSD for Java を使用して画像のサイズを比例的に変更するためのステップバイステップ ガイドへようこそ。効率的な画像サイズ変更機能を使用して Java アプリケーションを強化したい場合は、ここが適切な場所です。このチュートリアルでは、明確かつ簡潔な手順を使用してプロセスを説明します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

1. Java 環境: システムに Java がインストールされていることを確認してください。
2.  Aspose.PSD ライブラリ: Aspose.PSD ライブラリをダウンロードしてインストールします。必要なリソースを見つけることができます[ここ](https://releases.aspose.com/psd/java/).

## パッケージのインポート

前提条件を整理したら、必要なパッケージを Java プロジェクトにインポートします。 Aspose.PSD ライブラリがプロジェクト内で正しく参照されていることを確認してください。

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## ステップ 1: 画像をロードする

まず、サイズを変更する画像を Java アプリケーションにロードします。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## ステップ 2: 幅と高さを指定する

サイズ変更した画像の新しい幅と高さを決定します。この例では、画像のサイズを元の半分のサイズに変更します。

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## ステップ 3: サイズ変更した画像を保存する

形式オプション (この場合は PNG) を指定して、サイズ変更した画像を目的の場所に保存します。

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

そして、それができました！ Aspose.PSD for Java を使用して画像のサイズを比例的に変更することに成功しました。

## 結論

このチュートリアルでは、Java 用 Aspose.PSD ライブラリを使用して画像のサイズを比例的に変更するための重要な手順について説明しました。この機能を Java アプリケーションに簡単に統合して、画像処理を改善できるようになりました。

## よくある質問

### Q1: Aspose.PSD はすべての画像形式と互換性がありますか?

 A1: Aspose.PSD は、PSD、PNG、JPEG などを含むさまざまな画像形式をサポートしています。チェックしてください[ドキュメンテーション](https://reference.aspose.com/psd/java/)包括的なリストについては、

### Q2: Aspose.PSD を商用プロジェクトに使用できますか?

 A2: はい、可能です。訪問[購入ページ](https://purchase.aspose.com/buy)ライセンスの詳細については、

### Q3: 一時ライセンスはテスト目的で利用できますか?

 A3: はい、仮ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/)評価用に。

### Q4: Aspose.PSD のサポートはどこで見つけられますか?

 A4: にアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートと支援のために。

### Q5: Aspose.PSD ドキュメントにアクセスするにはどうすればよいですか?

 A5: 詳細ドキュメントを参照してください。[ここ](https://reference.aspose.com/psd/java/).
`