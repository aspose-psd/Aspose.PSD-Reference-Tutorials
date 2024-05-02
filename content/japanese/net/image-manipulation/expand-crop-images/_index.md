---
title: Aspose.PSD for .NET での画像の拡大とトリミング
linktitle: 画像の拡大とトリミング
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用して画像を動的に拡大およびトリミングする方法を学びます。シームレスな画像操作については、ステップバイステップのガイドに従ってください。
type: docs
weight: 13
url: /ja/net/image-manipulation/expand-crop-images/
---
## 導入

Aspose.PSD for .NET は、開発者が .NET アプリケーションでさまざまな画像形式を操作できるようにする包括的なイメージング ライブラリです。その際立った機能の 1 つは、画像を簡単に操作できることです。このチュートリアルでは、画像の拡大とトリミングに焦点を当て、Aspose.PSD を使用してこれらのタスクを実行するための実践的なガイドを提供します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for .NET ライブラリ: Aspose.PSD for .NET ライブラリがインストールされていることを確認します。からダウンロードできます。[Aspose.PSD for .NET ドキュメント](https://reference.aspose.com/psd/net/).

- サンプル画像: チュートリアルで使用するサンプル画像ファイル (例: 「example1.psd」) を準備します。

それでは、ステップバイステップのガイドを始めましょう。

## 名前空間のインポート

まず、Aspose.PSD for .NET が提供する機能を利用するために必要な名前空間をインポートします。次の名前空間をコードに追加します。

```csharp
using Aspose.PSD.ImageOptions;
```

## ステップ 1: プロジェクトをセットアップする

 Aspose.PSD for .NET が統合されたプロジェクトが設定されていることを確認してください。そうでない場合は、次に従ってください[ドキュメンテーション](https://reference.aspose.com/psd/net/)指導のために。

## ステップ 2: 画像をロードする

次のコードを使用してサンプル イメージを読み込みます。

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

//画像をロードする
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    //画像処理用の追加コードはここに配置されます
}
```

## ステップ 3: 画像データをキャッシュする

画像データをキャッシュしてパフォーマンスを最適化します。

```csharp
rasterImage.CacheData();
```

## ステップ 4: 宛先長方形を定義する

Rectangle クラスのインスタンスを作成し、長方形の X、Y、幅、高さを定義します。これは、画像が拡大またはトリミングされる領域になります。

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## ステップ 5: 出力画像を保存する

指定したオプションと保存先の四角形を使用して出力イメージを保存します。

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## 結論

おめでとう！ Aspose.PSD for .NET を使用して画像を拡大およびトリミングする方法を学習しました。この強力なライブラリは、.NET アプリケーション内で画像操作の可能性を広げます。

## よくある質問

### Q1: Aspose.PSD は PSD 以外の画像形式を処理できますか?

A1: はい、Aspose.PSD は、JPEG、PNG、GIF などを含む幅広い画像形式をサポートしています。

### Q2: Aspose.PSD のサポートはどこで見つけられますか?

 A2: 次の場所でサポートを見つけたり、コミュニティに参加したりできます。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34).

### Q3 Aspose.PSD for .NET の無料トライアルはありますか?

 A3: はい、次のサイトで利用できる無料トライアルで機能を試すことができます。[Aspose.PSD 無料トライアル](https://releases.aspose.com/).

### Q4: Aspose.PSD の一時ライセンスを取得するにはどうすればよいですか?

A4: 仮ライセンスは以下から取得できます。[Aspose.PSD 一時ライセンス](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose.PSD for .NET はどこで購入できますか?

 A5: ライブラリは次の場所で購入できます。[Aspose.PSD 購入ページ](https://purchase.aspose.com/buy).