---
title: Aspose.PSD for .NET でのカラー バランス調整の適用
linktitle: カラーバランス調整を適用する
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET のカラー バランス調整機能を使用して、PSD 画像の色を簡単に強化します。素晴らしい結果を得るには、ステップバイステップのガイドに従ってください。
type: docs
weight: 14
url: /ja/net/image-adjustment/color-balance-adjustment/
---
## 導入

Aspose.PSD for .NET でのカラー バランス調整の適用に関するこの包括的なガイドへようこそ。 Aspose.PSD は、開発者が PSD ファイルを効率的に操作できるようにする強力な .NET ライブラリです。このチュートリアルでは、PSD 画像のカラー バランスを簡単に向上できるカラー バランス調整機能に焦点を当てます。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for .NET ライブラリ: からライブラリをダウンロードしてインストールします。[Aspose.PSD Web サイト](https://releases.aspose.com/psd/net/).
- 開発環境: マシン上に動作する .NET 開発環境がセットアップされていることを確認します。
- PSD ファイル: カラーバランス調整を適用する PSD ファイルを用意します。

## 名前空間のインポート

.NET プロジェクトに、Aspose.PSD 機能を使用するために必要な名前空間を含めます。コードに次の行を追加します。

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

ここで、カラー バランス調整プロセスを複数のステップに分けてみましょう。

## ステップ 1: PSD ファイルをロードする

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    //カラーバランス調整のコードは次の手順で追加します。
}
```

## ステップ 2: カラーバランスにアクセスして調整する

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## ステップ 3: 調整した画像を保存する

```csharp
im.Save(outputPath);
```

これで、Aspose.PSD for .NET を使用して PSD ファイルにカラー バランス調整が正常に適用されました。

## 結論

おめでとう！ Aspose.PSD for .NET を使用して PSD 画像のカラー バランスを向上させる方法を学習しました。望ましい視覚効果を実現するために、さまざまなバランス値を試してください。

## よくある質問

### Q1: カラーバランス調整を複数のレイヤーに適用できますか?

A1: はい、PSD ファイル内のすべてのレイヤーを繰り返し処理し、必要に応じてカラー バランスを調整できます。

### Q2: Aspose.PSD for .NET は PSD ファイルのバッチ処理に適していますか?

A2：もちろんです！ Aspose.PSD は、PSD ファイルの効率的なバッチ処理機能を提供します。

### Q3: Aspose.PSD for .NET の一時ライセンスを取得するにはどうすればよいですか?

 A3: 訪問[Aspose.PSD 一時ライセンス](https://purchase.aspose.com/temporary-license/)仮免許の場合。

### Q4: 他の例やドキュメントはどこで入手できますか?

 A4: を探索してください。[Aspose.PSD ドキュメント](https://reference.aspose.com/psd/net/)詳細な例とガイドについては、

### Q5: Aspose.PSD for .NET ではどのようなサポート オプションが利用できますか?

 A5: にアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートとディスカッションのために。
