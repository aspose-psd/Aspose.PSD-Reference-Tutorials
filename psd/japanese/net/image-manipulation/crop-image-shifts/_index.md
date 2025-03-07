---
title: Aspose.PSD for .NET でシフトによる画像の切り抜き
linktitle: シフトによる画像の切り抜き
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用して画像を簡単にトリミングする方法を学びます。正確な画像調整については、ステップバイステップのガイドに従ってください。
weight: 12
url: /ja/net/image-manipulation/crop-image-shifts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for .NET でシフトによる画像の切り抜き

## 導入

.NET 開発の分野では、Aspose.PSD は画像処理タスク用の強力なツールキットとして際立っています。その注目すべき機能の 1 つは、「シフトによるトリミング」機能により、画像を正確にトリミングできることです。このステップ バイ ステップ ガイドでは、Aspose.PSD for .NET を使用して画像をシームレスにトリミングするプロセスについて説明します。

## 前提条件

チュートリアルに進む前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for .NETライブラリ: ライブラリがインストールされていることを確認してください。インストールされていない場合は、[リリースページ](https://releases.aspose.com/psd/net/).

- .NET 環境: マシンに .NET 開発環境が設定されていることを確認します。

- サンプル画像: 作業に使用するサンプル画像を PSD 形式で準備します。

## 名前空間のインポート

まず、必要な名前空間を .NET プロジェクトにインポートします。これらの名前空間は、画像の切り抜きに必要な Aspose.PSD クラスとメソッドへのアクセスを提供します。

```csharp
using Aspose.PSD.ImageOptions;
```

## ステップ1: ドキュメントディレクトリを定義する

ソース ファイルと宛先ファイルが配置されるドキュメント ディレクトリへのパスを設定します。

```csharp
string dataDir = "Your Document Directory";
```

## ステップ2: ソースイメージを読み込む

切り抜きたい PSD 画像をロードします。「sample.psd」をソース ファイルの名前に置き換えてください。

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## ステップ3: パフォーマンス向上のために画像データをキャッシュする

パフォーマンスを向上させるために、トリミングする前に画像データをキャッシュすることをお勧めします。

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## ステップ4: 切り抜きのシフト値を定義する

画像の左、右、上、下のシフト値を指定します。切り抜きの要件に基づいてこれらの値を調整します。

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## ステップ5: トリミングを適用して結果を保存する

活用する`Crop`指定されたシフトを適用し、トリミングされた画像を宛先ファイルに保存するメソッド。

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## 結論

おめでとうございます! Aspose.PSD for .NET を使用してシフトによって画像をトリミングする方法を学習しました。この強力な機能により、さまざまな画像処理タスクに必要な精度と制御が実現します。

## よくある質問

### Q1: PSD だけでなく、さまざまな形式の画像をトリミングできますか?

A1: はい、Aspose.PSD はさまざまな画像形式をサポートしており、JPEG、PNG などの形式で画像をトリミングできます。

### Q2: Aspose.PSD for .NET を購入する前に試用版はありますか?

 A2: もちろんです！無料トライアルでツールキットを試すことができます[ここ](https://releases.aspose.com/).

### Q3: Aspose.PSD for .NET の一時ライセンスを取得するにはどうすればよいですか?

 A3: テスト目的で臨時ライセンスを取得することができます[ここ](https://purchase.aspose.com/temporary-license/).

### Q4: Aspose.PSD に関する追加のサポートやディスカッションはどこで見つかりますか?

 A4: 訪問[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)サポートと魅力的な議論のため。

### Q5: Aspose.PSD for .NET を Web サイトから直接購入できますか?

 A5: はい、ライブラリは安全に購入できます。[購入ページ](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
