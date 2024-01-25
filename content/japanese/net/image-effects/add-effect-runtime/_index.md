---
title: Aspose.PSD for .NET で実行時にエフェクトを追加する
linktitle: 実行時にエフェクトを追加する
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用した動的な画像の強化を検討します。実行時にエフェクトを簡単に追加できます。
type: docs
weight: 10
url: /ja/net/image-effects/add-effect-runtime/
---
## 導入

画像の視覚的な魅力を高めることは、グラフィック デザインや画像処理アプリケーションにおける一般的な要件です。このチュートリアルでは、Aspose.PSD for .NET を使用して実行時にエフェクトを追加する方法を検討します。 Aspose.PSD は、開発者が Adobe Photoshop ファイルをシームレスに操作できるようにする強力な API です。 

## 前提条件

ステップバイステップのガイドに入る前に、次のものが揃っていることを確認してください。

- C# と .NET Framework の基本的な知識。
-  Aspose.PSD for .NET がインストールされています。からダウンロードできます[ここ](https://releases.aspose.com/psd/net/).

## 名前空間のインポート

開始するには、C# プロジェクトに必要な名前空間が含まれていることを確認してください。これらの名前空間は、Aspose.PSD が提供する機能を利用するために不可欠です。

```csharp
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageLoadOptions;
```

## ステップ 1: ドキュメント ディレクトリを設定する

```csharp
string dataDir = "Your Document Directory";
```

「Your Document Directory」を PSD ファイルが存在する実際のパスに置き換えます。

## ステップ 2: エフェクトリソースを含む PSD 画像をロードする

```csharp
string sourceFileName = dataDir + "ThreeRegularLayers.psd";
string exportPath = dataDir + "ThreeRegularLayersChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
```

このステップでは PSD 画像がロードされ、エフェクト リソースのロードが可能になります。

## ステップ 3: カラーオーバーレイレイヤー効果を追加する

```csharp
var effect = im.Layers[1].BlendingOptions.AddColorOverlay();
effect.Color = Color.Green;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

ここでは、PSD 画像の 2 番目のレイヤーにカラー オーバーレイ効果を追加します。好みに応じて色、不透明度、ブレンド モードをカスタマイズできます。

## ステップ 4: 変更したイメージを保存する

```csharp
im.Save(exportPath);
```

最後に、エフェクトを適用した画像を指定したエクスポート パスに保存します。

## 結論

Aspose.PSD for .NET で実行時にエフェクトを追加するのは簡単なプロセスです。わずか数行のコードで、画像の視覚的な魅力を動的に強化できます。望ましい結果を得るために、さまざまなエフェクトとパラメータを試してください。

## よくある質問

### Q1: Aspose.PSD は最新の .NET Framework と互換性がありますか?

A1: はい、Aspose.PSD は、最新の .NET Framework バージョンとの互換性を確保するために定期的に更新されます。

### Q2: 1 つのレイヤーに複数のエフェクトを適用できますか?

A2：もちろんです！レイヤー上で複数のエフェクトを連鎖させて、複雑な視覚的拡張を作成できます。

### Q3: 追加できるエフェクトの種類に制限はありますか?

A3: Aspose.PSD は幅広いエフェクトを提供しますが、サポートされているエフェクトの詳細についてはドキュメントを確認することをお勧めします。

### Q4: テスト目的で一時ライセンスを取得するにはどうすればよいですか?

 A4: 仮免許は取得できます。[ここ](https://purchase.aspose.com/temporary-license/)テストと評価用。

### Q5: 追加のサポートやコミュニティのディスカッションはどこで見つけられますか?

 A5: にアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)サポートとディスカッションのため。