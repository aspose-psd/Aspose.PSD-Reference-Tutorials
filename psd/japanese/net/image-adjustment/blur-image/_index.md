---
title: Aspose.PSD for .NET で画像をぼかす
linktitle: 画像をぼかす
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用して画像を簡単にぼかす方法を学びます。C# プロジェクトでシームレスな画像操作を行うためのステップバイステップ ガイドです。
weight: 13
url: /ja/net/image-adjustment/blur-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for .NET で画像をぼかす

## 導入

.NET 開発の分野では、Aspose.PSD は画像操作の強力な味方であることが証明されています。このチュートリアルでは、Aspose.PSD for .NET を使用して画像をぼかすという特定のタスクに焦点を当てています。画像処理スキルを向上させたい場合や、プログラムで画像をぼかす効率的な方法を探している場合は、このチュートリアルが役に立ちます。

## 前提条件

チュートリアルに進む前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for .NET: Aspose.PSDライブラリがインストールされていることを確認してください。ダウンロードはここから行えます。[ここ](https://releases.aspose.com/psd/net/).

- 開発環境: .NET 開発環境をセットアップし、C# の基本を理解している必要があります。

- サンプル画像: PSD 形式のサンプル画像を用意します。独自の画像を使用することも、テスト用にダウンロードすることもできます。

## 名前空間のインポート

まず、C# コードに必要な名前空間をインポートします。

```csharp
using Aspose.PSD.ImageFilters.FilterOptions;
using Aspose.PSD.ImageOptions;
```

## ステップ1: ドキュメントディレクトリを定義する

```csharp
//ドキュメント ディレクトリへのパス。
string dataDir = "Your Document Directory";
```

## ステップ2: 画像を読み込む

```csharp
//ExStart:BluranImage

string sourceFile = dataDir + @"sample.psd";

//既存の画像をRasterImageクラスのインスタンスに読み込みます
using (var image = Image.Load(sourceFile))
{
    //このブロックを使用して次の手順に進みます
}
```

## ステップ3: 画像をラスターイメージに変換する

```csharp
RasterImage rasterImage = (RasterImage)image;
```

## ステップ4: ガウスぼかしフィルターを適用する

```csharp
rasterImage.Filter(rasterImage.Bounds, new GaussianBlurFilterOptions(15, 15));
```

ここでは、`GaussianBlurFilterOptions`クラスは、水平方向と垂直方向の両方のぼかしに指定された半径 15 で使用されます。

## ステップ5: ぼかした画像を保存する

```csharp
string destName = dataDir + @"BlurAnImage_out.gif";
rasterImage.Save(destName, new GifOptions());
```

## 結論

おめでとうございます。Aspose.PSD for .NET を使用して画像をぼかすことができました。このチュートリアルでは、Aspose.PSD の機能について簡単に紹介し、.NET アプリケーションで画像を操作する無数の可能性への扉を開きます。

## よくある質問

### Q1: 画像のさまざまな部分に異なるぼかしの強度を適用できますか?

A1: はい、Aspose.PSD を使用すると、さまざまなパラメータを持つフィルターを画像の特定の領域に適用して、ぼかし処理を細かく制御できます。

### Q2: Aspose.PSD はすべての画像形式と互換性がありますか?

A2: Aspose.PSD は幅広い画像形式をサポートしていますが、完全なリストと形式固有の考慮事項についてはドキュメントを確認することをお勧めします。

### Q3: Aspose.PSD の一時ライセンスを取得するにはどうすればよいですか?

 A3: 臨時免許証は以下から取得できます。[ここ](https://purchase.aspose.com/temporary-license/)テストおよび評価の目的で。

### Q4: Aspose.PSD には他の画像操作機能はありますか?

A4: もちろんです! Aspose.PSD は、サイズ変更、切り取り、色調整など、包括的な機能セットを提供します。完全なリストについては、ドキュメントを参照してください。

### Q5: Aspose.PSD コミュニティでサポートを受けたり、コミュニティとつながったりするには、どこで連絡すればよいですか?

 A5: ご質問やご相談は、[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
