---
title: Aspose.PSD for Java で画像を比例的にサイズ変更する
linktitle: 画像を比例的にサイズ変更
second_title: Aspose.PSD Java API
description: Aspose.PSD を使用して Java アプリケーションを強化します。ガイドに従って、簡単に画像を比例的にサイズ変更します。今すぐ画像処理機能を強化しましょう。
type: docs
weight: 17
url: /ja/java/advanced-image-manipulation/resize-image-proportionally/
---
## 導入

Aspose.PSD for Java を使用して画像を比例的にサイズ変更する手順を説明したガイドへようこそ。効率的な画像サイズ変更機能を使用して Java アプリケーションを強化したい場合は、ここが最適な場所です。このチュートリアルでは、明確で簡潔な手順を使用してプロセスを順を追って説明します。

## 前提条件

チュートリアルに進む前に、次の前提条件が満たされていることを確認してください。

1. Java 環境: システムに Java がインストールされていることを確認してください。
2.  Aspose.PSDライブラリ: Aspose.PSDライブラリをダウンロードしてインストールします。必要なリソースは以下にあります。[ここ](https://releases.aspose.com/psd/java/).

## パッケージのインポート

前提条件を整理したら、必要なパッケージを Java プロジェクトにインポートします。Aspose.PSD ライブラリがプロジェクトで正しく参照されていることを確認します。

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## ステップ1: 画像を読み込む

まず、サイズを変更する画像を Java アプリケーションに読み込みます。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## ステップ2: 幅と高さを指定する

サイズ変更した画像の新しい幅と高さを決定します。この例では、画像のサイズを元のサイズの半分に変更します。

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## ステップ3: サイズ変更した画像を保存する

形式オプション (この場合は PNG) を指定して、サイズ変更した画像を目的の場所に保存します。

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

これで完了です。Aspose.PSD for Java を使用して、画像を比例的にサイズ変更できました。

## 結論

このチュートリアルでは、Java 用の Aspose.PSD ライブラリを使用して画像を比例的にサイズ変更するための基本的な手順について説明しました。これで、この機能を Java アプリケーションに簡単に統合して、画像処理を改善できます。

## よくある質問

### Q1: Aspose.PSD はすべての画像形式と互換性がありますか?

 A1: Aspose.PSDはPSD、PNG、JPEGなど、さまざまな画像形式をサポートしています。[ドキュメント](https://reference.aspose.com/psd/java/)包括的なリストについては、こちらをご覧ください。

### Q2: Aspose.PSD を商用プロジェクトに使用できますか?

 A2: はい、できます。[購入ページ](https://purchase.aspose.com/buy)ライセンスの詳細については、こちらをご覧ください。

### Q3: テスト目的で一時ライセンスを利用できますか?

 A3: はい、一時免許証を取得することができます[ここ](https://purchase.aspose.com/temporary-license/)評価のため。

### Q4: Aspose.PSD のサポートはどこで見つかりますか?

 A4: 訪問[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートと支援のため。

### Q5: Aspose.PSD ドキュメントにアクセスするにはどうすればいいですか?

 A5: 詳細なドキュメントを参照してください[ここ](https://reference.aspose.com/psd/java/).
`