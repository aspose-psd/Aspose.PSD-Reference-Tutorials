---
title: Aspose.PSD for .NET でのシフトによる画像のトリミング
linktitle: シフトによる画像のトリミング
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用して画像を簡単にトリミングする方法を学びます。正確な画像調整については、ステップバイステップのガイドに従ってください。
type: docs
weight: 12
url: /ja/net/image-manipulation/crop-image-shifts/
---
## 導入

.NET 開発の分野では、Aspose.PSD は画像処理タスク用の強力なツールキットとして際立っています。その注目すべき機能の 1 つは、「シフトによるトリミング」機能のおかげで、画像を正確にトリミングできることです。このステップバイステップ ガイドでは、Aspose.PSD for .NET を使用して画像をシームレスにトリミングするプロセスを説明します。

## 前提条件

チュートリアルを詳しく進める前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for .NET Library: ライブラリがインストールされていることを確認してください。そうでない場合は、からダウンロードできます。[リリースページ](https://releases.aspose.com/psd/net/).

- .NET 環境: マシン上に .NET 開発環境がセットアップされていることを確認します。

- サンプル画像: 作業したいサンプル画像を PSD 形式で準備します。

## 名前空間のインポート

まず、必要な名前空間を .NET プロジェクトにインポートします。これらの名前空間は、画像のトリミングに必要な Aspose.PSD クラスとメソッドへのアクセスを提供します。

```csharp
using Aspose.PSD.ImageOptions;
```

## ステップ 1: ドキュメント ディレクトリを定義する

ソース ファイルと宛先ファイルが配置されるドキュメント ディレクトリへのパスを設定します。

```csharp
string dataDir = "Your Document Directory";
```

## ステップ 2: ソースイメージをロードする

切り抜きたいPSD画像を読み込みます。 「sample.psd」をソース ファイルの名前に置き換えてください。

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## ステップ 3: パフォーマンスを向上させるために画像データをキャッシュする

パフォーマンスを向上させるために、トリミングする前に画像データをキャッシュすることをお勧めします。

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## ステップ 4: クロップ用のシフト値を定義する

画像の左右上下のシフト値を指定します。トリミング要件に基づいてこれらの値を調整します。

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## ステップ 5: トリミングを適用して結果を保存する

を活用してください。`Crop`メソッドを使用して、指定されたシフトを適用し、トリミングされた画像を宛先ファイルに保存します。

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## 結論

おめでとう！ Aspose.PSD for .NET を使用して、シフトによって画像をトリミングする方法を学習しました。この強力な機能により、さまざまな画像処理タスクに必要な精度と制御が可能になります。

## よくある質問

### Q1: PSD だけでなく、さまざまな形式の画像をトリミングできますか?

A1: はい、Aspose.PSD はさまざまな画像形式をサポートしており、JPEG、PNG などの形式で画像をトリミングできます。

### Q2: Aspose.PSD for .NET を購入する前に利用できる試用版はありますか?

 A2：確かに！無料トライアルを利用してツールキットを探索できます[ここ](https://releases.aspose.com/).

### Q3: Aspose.PSD for .NET の一時ライセンスを取得するにはどうすればよいですか?

 A3: テスト目的で一時ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/).

### Q4: Aspose.PSD に関連する追加のサポートやディスカッションはどこで見つけられますか?

 A4: にアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)サポートと魅力的なディスカッションのために。

### Q5: Aspose.PSD for .NET を Web サイトから直接購入できますか?

 A5: はい、ライブラリは次のサイトから安全に購入できます。[購入ページ](https://purchase.aspose.com/buy).
