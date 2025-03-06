---
title: Aspose.PSD for .NET でカラーバランス調整を適用する
linktitle: カラーバランス調整の適用
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET のカラーバランス調整機能を使用すると、PSD 画像の色を簡単に強化できます。ステップバイステップのガイドに従って、すばらしい結果を得てください。
weight: 14
url: /ja/net/image-adjustment/color-balance-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for .NET でカラーバランス調整を適用する

## 導入

Aspose.PSD for .NET でカラー バランス調整を適用する方法についての包括的なガイドへようこそ。Aspose.PSD は、開発者が PSD ファイルを効率的に操作できるようにする強力な .NET ライブラリです。このチュートリアルでは、PSD イメージのカラー バランスを簡単に強化できるカラー バランス調整機能に焦点を当てます。

## 前提条件

チュートリアルに進む前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for .NETライブラリ: ライブラリを以下のサイトからダウンロードしてインストールします。[Aspose.PSD ウェブサイト](https://releases.aspose.com/psd/net/).
- 開発環境: マシンに動作する .NET 開発環境が設定されていることを確認します。
- PSD ファイル: カラーバランス調整を適用する PSD ファイルを用意します。

## 名前空間のインポート

.NET プロジェクトに、Aspose.PSD 機能を使用するために必要な名前空間を含めます。コードに次の行を追加します。

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

ここで、カラーバランス調整プロセスを複数のステップに分解してみましょう。

## ステップ1: PSDファイルを読み込む

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    //カラーバランス調整のコードは次の手順で追加されます。
}
```

## ステップ2: カラーバランスにアクセスして調整する

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

## ステップ3: 調整した画像を保存する

```csharp
im.Save(outputPath);
```

これで、Aspose.PSD for .NET を使用して PSD ファイルにカラー バランス調整を正常に適用できました。

## 結論

おめでとうございます! Aspose.PSD for .NET を使用して PSD イメージのカラー バランスを強化する方法を学習しました。さまざまなバランス値を試して、希望する視覚効果を実現してください。

## よくある質問

### Q1: カラーバランス調整を複数のレイヤーに適用できますか?

A1: はい、PSD ファイル内のすべてのレイヤーを反復処理し、必要に応じてカラーバランスを調整できます。

### Q2: Aspose.PSD for .NET は PSD ファイルのバッチ処理に適していますか?

A2: もちろんです! Aspose.PSD は PSD ファイルに対して効率的なバッチ処理機能を提供します。

### Q3: Aspose.PSD for .NET の一時ライセンスを取得するにはどうすればよいですか?

 A3: 訪問[Aspose.PSD 一時ライセンス](https://purchase.aspose.com/temporary-license/)一時ライセンスの場合。

### Q4: その他の例やドキュメントはどこで見つかりますか?

 A4: 探索する[Aspose.PSD ドキュメント](https://reference.aspose.com/psd/net/)詳細な例とガイドについては、こちらをご覧ください。

### Q5: Aspose.PSD for .NET にはどのようなサポート オプションがありますか?

 A5: 訪問[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートとディスカッションのため。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
