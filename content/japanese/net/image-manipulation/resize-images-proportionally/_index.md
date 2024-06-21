---
title: Aspose.PSD for .NET での画像のサイズを比例的に変更する
linktitle: 画像のサイズを比例的に変更する
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用してシームレスな画像サイズ変更を試してください。ライブラリをダウンロードしてチュートリアルに従い、画像処理機能を強化してください。
type: docs
weight: 14
url: /ja/net/image-manipulation/resize-images-proportionally/
---
画像操作の分野では、Aspose.PSD for .NET は強力なツールキットとして際立っており、開発者に画像のサイズを比例的に簡単に変更できる機能を提供します。このステップバイステップのガイドでは、Aspose.PSD for .NET を使用して画像のサイズを変更し、画像の比率を完璧に維持するプロセスを説明します。

## 導入

画像のサイズを比例的に変更することは、多くのアプリケーションで一般的なタスクであり、Aspose.PSD for .NET は開発者にとってこのプロセスを簡素化します。 Web アプリケーション、デスクトップ ソフトウェア、モバイル アプリのいずれで作業している場合でも、視覚的な魅力と一貫性を維持するには、アスペクト比を維持しながら画像のサイズを変更する方法を理解することが重要です。

## 前提条件

Aspose.PSD for .NET を使用したサイズ変更の魔法に入る前に、次の前提条件が満たされていることを確認してください。

1.  Aspose.PSD for .NET ライブラリ: Aspose.PSD for .NET ライブラリがインストールされていることを確認します。からダウンロードできます。[.NET リリース用の Aspose.PSD](https://releases.aspose.com/psd/net/)ページ。

2. ドキュメント ディレクトリ: ドキュメントを保存するディレクトリを作成し、提供されたコード内の「ドキュメント ディレクトリ」をこのディレクトリへの実際のパスに置き換えます。

前提条件を設定したので、ステップバイステップのガイドに進みましょう。

## 名前空間のインポート

```csharp
using Aspose.PSD.ImageOptions;
```

必要なクラスとメソッドにアクセスするために必要な名前空間をインポートします。

## ステップ 1: 画像をロードする

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

//既存の画像を RasterImage クラスのインスタンスにロードします
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	//残りの手順はここに進みます
}
```

を使用してソース画像をロードします。`Image.Load`方法。

## ステップ 2: 幅と高さを指定する

```csharp
//幅と高さの指定
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

サイズ変更された画像の新しい幅と高さを決定します。この例では、幅と高さは半分ですが、要件に基づいてこれらの値を調整できます。

## ステップ 3: サイズ変更した画像を保存する

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

サイズ変更した画像を保存するには、`Save`オプションを指定したメソッド。この場合、PNG ファイルとして保存します。

## 結論

Aspose.PSD for .NET で画像のサイズを比例的に変更することは、画像処理ワークフローに価値を加える簡単なプロセスです。このガイドでは、この機能をアプリケーションにシームレスに統合するための知識を提供します。

## よくある質問

### Q1: 画像のサイズを特定のサイズに変更できますか?

A1: はい、コード内の要件に応じて新しい幅と高さをカスタマイズできます。

### Q2: Aspose.PSD for .NET は画像のバッチ サイズ変更に適していますか?

A2: もちろんです！これらのステップをループに組み込んで、複数の画像をバッチ処理できます。

### Q3: Aspose.PSD for .NET には他の画像操作機能はありますか?

A3: はい。Aspose.PSD for .NET は、画像のトリミング、回転、フィルターの適用など、幅広い機能を提供します。

### Q4: Aspose.PSD for .NET の無料トライアルはありますか?

 A4: はい、無料トライアルで Aspose.PSD for .NET の機能を試すことができます。訪問[ここ](https://releases.aspose.com/)始めるために。

### Q5: Aspose.PSD for .NET のサポートはどこで見つけられますか?

 A5: にアクセスしてください。[Aspose.PSD for .NET フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートとディスカッションのために。