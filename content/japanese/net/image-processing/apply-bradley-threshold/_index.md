---
title: Aspose.PSD for .NET での Bradley しきい値の適用
linktitle: ブラッドリーしきい値の適用
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET の Bradley Threshold を使用して画像のセグメンテーションを強化します。効果的な二値化のためのステップバイステップのガイド。
type: docs
weight: 15
url: /ja/net/image-processing/apply-bradley-threshold/
---
## 導入

Aspose.PSD for .NET での Bradley Threshold の適用に関する包括的なチュートリアルへようこそ。 Aspose.PSD for .NET は、.NET アプリケーションで Photoshop ファイルを操作できるようにする強力なライブラリです。 Bradley Thresholding は画像の 2 値化に使用される技術で、オブジェクトを背景から効果的に分離するのに役立ちます。

このチュートリアルでは、Aspose.PSD for .NET を使用して Bradley Threshold を適用するプロセスを説明します。手順に入る前に、必要な前提条件が整っていることを確認してください。

## 前提条件

始める前に、次の設定がされていることを確認してください。

-  Aspose.PSD for .NET ライブラリ: からライブラリをダウンロードしてインストールします。[Aspose.PSD for .NET ドキュメント](https://reference.aspose.com/psd/net/).
- ドキュメント ディレクトリ: ソース PSD ファイルと結果のバイナリ化された画像を保存するディレクトリを作成します。

前提条件が整ったので、ステップバイステップのガイドに進みましょう。

## 名前空間のインポート

.NET プロジェクトで、Aspose.PSD 機能にアクセスするために必要な名前空間をインポートしてください。

```csharp
// Aspose.PSD 名前空間をインポートする
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

## ステップ 1: ノイズのある画像をロードする

ソース PSD ファイルへのパスとバイナリ化された出力の宛先を定義します。

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"binarized_out.png";
```

## ステップ 2: Bradley しきい値を使用して画像を 2 値化する

PSD イメージをロードし、しきい値を指定し、Bradley しきい値を適用して、出力を PNG イメージとして保存します。

```csharp
//画像をロードする
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    //しきい値を定義する
    double threshold = 0.15;

    //BinarizeBradley メソッドを呼び出し、しきい値をパラメータとして渡します
    image.BinarizeBradley(threshold);

    //出力画像を保存する
    image.Save(destName, new PngOptions());
}
```

## 結論

おめでとう！ Aspose.PSD for .NET で Bradley Threshold が正常に適用されました。この技術は、さまざまなアプリケーションで画像のセグメンテーションを強化するのに非常に役立ちます。

画像処理タスクを最適化するために、Aspose.PSD for .NET が提供するその他の機能を自由に探索してください。

## よくある質問

### Q1: Bradley Threshold はどのタイプの画像にも適用できますか?

A1: はい、Bradley Thresholding は、さまざまな種類の画像に適した汎用性の高い技術です。

### Q2: 追加の Aspose.PSD ドキュメントはどこで見つけられますか?

 A2: を参照してください。[ドキュメンテーション](https://reference.aspose.com/psd/net/) Aspose.PSD for .NET の詳細については、「Aspose.PSD for .NET」を参照してください。

### Q3: 無料トライアルはありますか?

 A3: はい、Aspose.PSD for .NET の無料トライアルを試すことができます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.PSD のサポートを受けるにはどうすればよいですか?

 A4: にアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートとディスカッションのために。

### Q5: Aspose.PSD のライセンスはどこで購入できますか?

 A5: ライセンスを購入できます。[ここ](https://purchase.aspose.com/buy).