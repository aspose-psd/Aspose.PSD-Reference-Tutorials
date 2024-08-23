---
title: Aspose.PSD for .NET で実行時に効果を追加する
linktitle: 実行時にエフェクトを追加する
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用して動的な画像強化を試してみましょう。実行時に簡単に効果を追加できます。
type: docs
weight: 10
url: /ja/net/image-effects/add-effect-runtime/
---
## 導入

画像の視覚的な魅力を高めることは、グラフィック デザインや画像処理アプリケーションでよく求められる要件です。このチュートリアルでは、Aspose.PSD for .NET を使用して実行時に効果を追加する方法について説明します。Aspose.PSD は、開発者が Adobe Photoshop ファイルをシームレスに操作できるようにする強力な API です。 

## 前提条件

ステップバイステップガイドに進む前に、次のものを用意してください。

- C# および .NET フレームワークに関する基本的な知識。
-  Aspose.PSD for .NETがインストールされています。こちらからダウンロードできます。[ここ](https://releases.aspose.com/psd/net/).

## 名前空間のインポート

まず、C# プロジェクトに必要な名前空間が含まれていることを確認してください。これらの名前空間は、Aspose.PSD が提供する機能を利用するために不可欠です。

```csharp
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageLoadOptions;
```

## ステップ1: ドキュメントディレクトリを設定する

```csharp
string dataDir = "Your Document Directory";
```

「Your Document Directory」を、PSD ファイルが配置されている実際のパスに置き換えます。

## ステップ2: エフェクトリソース付きのPSDイメージを読み込む

```csharp
string sourceFileName = dataDir + "ThreeRegularLayers.psd";
string exportPath = dataDir + "ThreeRegularLayersChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
```

このステップでは、PSD イメージが読み込まれ、エフェクト リソースの読み込みが可能になります。

## ステップ3: カラーオーバーレイレイヤー効果を追加する

```csharp
var effect = im.Layers[1].BlendingOptions.AddColorOverlay();
effect.Color = Color.Green;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

ここでは、PSD 画像の 2 番目のレイヤーにカラーオーバーレイ効果を追加します。好みに応じて、色、不透明度、ブレンドモードをカスタマイズできます。

## ステップ4: 変更した画像を保存する

```csharp
im.Save(exportPath);
```

最後に、効果を適用した画像を指定したエクスポート パスに保存します。

## 結論

Aspose.PSD for .NET で実行時に効果を追加するのは簡単なプロセスです。わずか数行のコードで、画像の視覚的な魅力を動的に高めることができます。さまざまな効果とパラメーターを試して、希望する結果を達成してください。

## よくある質問

### Q1: Aspose.PSD は最新の .NET フレームワークと互換性がありますか?

A1: はい、Aspose.PSD は、最新の .NET Framework バージョンとの互換性を確保するために定期的に更新されます。

### Q2: 1 つのレイヤーに複数のエフェクトを適用できますか?

A2: もちろんです! レイヤー上で複数のエフェクトを連鎖させて、複雑な視覚効果を作成できます。

### Q3: 追加できるエフェクトの種類に制限はありますか?

A3: Aspose.PSD は幅広いエフェクトを提供していますが、サポートされているエフェクトの詳細についてはドキュメントを確認することをお勧めします。

### Q4: テスト目的で一時ライセンスを取得するにはどうすればよいですか?

 A4: 臨時免許証を取得できます[ここ](https://purchase.aspose.com/temporary-license/)テストと評価のため。

### Q5: 追加のサポートやコミュニティのディスカッションはどこで見つかりますか?

 A5: 訪問[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)サポートとディスカッションのため。