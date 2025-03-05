---
title: Aspose.PSD for .NET で画像を比例的にサイズ変更する
linktitle: 画像を比例的にサイズ変更する
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET でシームレスな画像サイズ変更を体験してください。ライブラリをダウンロードし、チュートリアルに従って、画像処理機能を強化してください。
type: docs
weight: 14
url: /ja/net/image-manipulation/resize-images-proportionally/
---
画像操作の分野では、Aspose.PSD for .NET は強力なツールキットとして際立っており、開発者に画像の比率を維持したまま簡単にサイズを変更する機能を提供します。このステップ バイ ステップ ガイドでは、Aspose.PSD for .NET を使用して画像のサイズを変更するプロセスを順を追って説明し、画像の比率が完璧に維持されるようにします。

## 導入

画像を縦横比を維持したままサイズ変更することは、多くのアプリケーションでよく行われるタスクです。Aspose.PSD for .NET は、開発者にとってこのプロセスを簡素化します。Web アプリケーション、デスクトップ ソフトウェア、モバイル アプリのいずれを扱っている場合でも、画像の縦横比を維持しながらサイズを変更する方法を理解することは、視覚的な魅力と一貫性を維持するために重要です。

## 前提条件

Aspose.PSD for .NET を使用したサイズ変更の魔法に飛び込む前に、次の前提条件が満たされていることを確認してください。

1.  Aspose.PSD for .NETライブラリ: Aspose.PSD for .NETライブラリがインストールされていることを確認してください。[Aspose.PSD for .NET リリース](https://releases.aspose.com/psd/net/)ページ。

2. ドキュメント ディレクトリ: ドキュメントを保存するディレクトリを作成し、提供されたコード内の「Your Document Directory」をこのディレクトリへの実際のパスに置き換えます。

前提条件が整ったので、ステップバイステップのガイドに進みましょう。

## 名前空間のインポート

```csharp
using Aspose.PSD.ImageOptions;
```

必要なクラスとメソッドにアクセスするには、必要な名前空間をインポートします。

## ステップ1: 画像を読み込む

```csharp
//ドキュメント ディレクトリへのパス。
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

//既存の画像をRasterImageクラスのインスタンスに読み込みます
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	//残りの手順はここ
}
```

ソースイメージをロードするには、`Image.Load`方法。

## ステップ2: 幅と高さを指定する

```csharp
//幅と高さの指定
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

サイズ変更された画像の新しい幅と高さを決定します。この例では、幅と高さが半分になっていますが、必要に応じてこれらの値を調整できます。

## ステップ3: サイズ変更した画像を保存する

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

サイズ変更した画像を保存するには、`Save`指定されたオプションを持つメソッド。この場合は、PNG ファイルとして保存します。

## 結論

Aspose.PSD for .NET で画像を比例的にサイズ変更することは、画像処理ワークフローに価値を追加する簡単なプロセスです。このガイドでは、この機能をアプリケーションにシームレスに統合するための知識を身に付けることができます。

## よくある質問

### Q1: 画像のサイズを特定のサイズに変更できますか?

A1: はい、コード内の要件に応じて新しい幅と高さをカスタマイズできます。

### Q2: Aspose.PSD for .NET はバッチ画像サイズ変更に適していますか?

A2: もちろんです! これらの手順をループに組み込んで、複数の画像をバッチ処理することができます。

### Q3: Aspose.PSD for .NET には他の画像操作機能はありますか?

A3: はい、Aspose.PSD for .NET には、画像の切り取り、回転、フィルターの適用など、幅広い機能が備わっています。

### Q4: Aspose.PSD for .NET の無料試用版はありますか?

 A4: はい、無料トライアルでAspose.PSD for .NETの機能を試すことができます。[ここ](https://releases.aspose.com/)始めましょう。

### Q5: Aspose.PSD for .NET のサポートはどこで見つかりますか?

 A5: 訪問[Aspose.PSD for .NET フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートとディスカッションのため。