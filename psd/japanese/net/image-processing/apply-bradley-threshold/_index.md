---
title: Aspose.PSD for .NET で Bradley しきい値を適用する
linktitle: ブラッドリー閾値の適用
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET の Bradley Threshold を使用して画像のセグメンテーションを強化します。効果的な 2 値化のためのステップバイステップ ガイド。
weight: 15
url: /ja/net/image-processing/apply-bradley-threshold/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for .NET で Bradley しきい値を適用する

## 導入

Aspose.PSD for .NET で Bradley Threshold を適用する方法についての包括的なチュートリアルへようこそ。Aspose.PSD for .NET は、.NET アプリケーションで Photoshop ファイルを操作できる強力なライブラリです。Bradley Thresholding は、画像の 2 値化に使用される手法で、オブジェクトを背景から効果的に分離するのに役立ちます。

このチュートリアルでは、Aspose.PSD for .NET を使用して Bradley Threshold を適用するプロセスについて説明します。手順に進む前に、必要な前提条件が満たされていることを確認してください。

## 前提条件

始める前に、次の設定がされていることを確認してください。

-  Aspose.PSD for .NETライブラリ: ライブラリを以下のサイトからダウンロードしてインストールします。[Aspose.PSD for .NET ドキュメント](https://reference.aspose.com/psd/net/).
- ドキュメント ディレクトリ: ソース PSD ファイルと結果の 2 値化画像を保存するディレクトリを作成します。

前提条件が整いましたので、ステップバイステップのガイドに進みましょう。

## 名前空間のインポート

.NET プロジェクトでは、Aspose.PSD 機能にアクセスするために必要な名前空間を必ずインポートしてください。

```csharp
// Aspose.PSD 名前空間をインポートする
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

## ステップ1: ノイズの多い画像を読み込む

ソース PSD ファイルへのパスとバイナリ化された出力の保存先を定義します。

```csharp
//ドキュメント ディレクトリへのパス。
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"binarized_out.png";
```

## ステップ2: ブラッドリーしきい値を使用して画像を2値化する

PSD 画像を読み込み、しきい値を指定し、Bradley しきい値を適用して、出力を PNG 画像として保存します。

```csharp
//画像を読み込む
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    //閾値を定義する
    double threshold = 0.15;

    //BinarizeBradleyメソッドを呼び出し、しきい値をパラメータとして渡します。
    image.BinarizeBradley(threshold);

    //出力画像を保存する
    image.Save(destName, new PngOptions());
}
```

## 結論

おめでとうございます。Aspose.PSD for .NET に Bradley Threshold を正常に適用しました。この手法は、さまざまなアプリケーションで画像のセグメンテーションを強化するのに非常に役立ちます。

画像処理タスクを最適化するために、Aspose.PSD for .NET が提供するその他の機能や機能を自由に探索してください。

## よくある質問

### Q1: Bradley Threshold はどんな種類の画像にも適用できますか?

A1: はい、Bradley しきい値化は、さまざまな画像タイプに適した多目的な手法です。

### Q2: Aspose.PSD の追加ドキュメントはどこで入手できますか?

 A2: を参照してください[ドキュメント](https://reference.aspose.com/psd/net/) Aspose.PSD for .NET の詳細については、こちらをご覧ください。

### Q3: 無料トライアルはありますか？

 A3: はい、Aspose.PSD for .NETの無料トライアルをお試しください。[ここ](https://releases.aspose.com/).

### Q4: Aspose.PSD のサポートを受けるにはどうすればよいですか?

 A4: 訪問[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートとディスカッションのため。

### Q5: Aspose.PSD のライセンスはどこで購入できますか?

 A5: ライセンスを購入することができます[ここ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
