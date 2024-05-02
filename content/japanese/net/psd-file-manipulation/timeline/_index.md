---
title: Aspose.PSD for .NET でのタイムラインの操作
linktitle: タイムラインの操作
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET Timeline クラスを使用して PSD 画像の操作を強化します。フレームのプロパティ、レイヤーの状態を制御し、クリエイティブな可能性を簡単に解き放ちます。
type: docs
weight: 16
url: /ja/net/psd-file-manipulation/timeline/
---
## 導入
グラフィック デザインと画像操作の動的な世界では、画像のタイムラインを制御および操作する機能が非常に重要です。 Aspose.PSD for .NET は、Timeline クラスを使用した強力なソリューションを提供します。この高度な機能を使用すると、フレーム遅延の変更、特定のフレームのレイヤー状態の編集など、PsdImage のタイムラインに変更を加えることができます。
## 前提条件
Timeline クラスが提供するエキサイティングな可能性を検討する前に、次の前提条件が満たされていることを確認してください。
-  Aspose.PSD for .NET ライブラリ: Aspose.PSD for .NET ライブラリがインストールされていることを確認します。からダウンロードできます。[Aspose.PSD for .NET ドキュメント](https://reference.aspose.com/psd/net/).
- ドキュメント ディレクトリと出力ディレクトリ: コード内でドキュメントと出力ディレクトリのパスを定義します。を調整します。`baseDir`そして`outputDir`プロジェクトの構造に応じて変数を変更します。
ここで、Timeline クラスを利用する方法を段階的に見てみましょう。
## 名前空間のインポート
Timeline クラスの操作を開始するには、コードに必要な名前空間をインポートします。
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## ステップ 1: PSD 画像をロードする
まず、指定したソース ファイルから PSD 画像をロードします。ソース ファイルのパスが正しく設定されていることを確認します。
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //さらなる操作のためのコードはここにあります
}
```
## ステップ 2: タイムラインにアクセスする
PSD 画像がロードされたら、次のコードを使用してタイムラインにアクセスします。
```csharp
Timeline timeline = psdImage.Timeline;
```
## ステップ 3: 破棄方法を変更する
特定のフレームの破棄メソッドを操作します。この例では、フレーム 1 の破棄方法を変更します。
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## ステップ 4: フレーム遅延を調整する
特定のフレームの遅延を変更します。ここでは、フレーム 2 の遅延を 15 に変更します。
```csharp
timeline.Frames[1].Delay = 15;
```
## ステップ 5: レイヤ状態を編集する
特定のフレームの「レイヤー1」の不透明度を変更します。この例では、フレーム 2 の不透明度を 50 に設定します。
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## ステップ 6: レイヤーを移動する
「レイヤー 1」を特定のフレーム (この例ではフレーム 3) の左下隅に移動します。
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## ステップ 7: 新しいフレームを追加する
新しいフレームをタイムラインに追加します。
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## ステップ 8: ブレンド モードを変更する
特定のフレーム (この場合はフレーム 4) の「レイヤー 1」のブレンド モードを変更します。
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## ステップ 9: 変更を保存する
変更を PsdImage インスタンスに適用し、変更した PSD イメージを保存します。
```csharp
psdImage.Save(outputPsd);
```
## ステップ 10: クリーンアップ
最後に、一時出力ファイルを削除してクリーンアップします。
```csharp
File.Delete(outputPsd);
```
## 結論

結論として、Aspose.PSD for .NET の Timeline クラスを使用すると、開発者は PSD 画像のタイムラインをきめ細かく制御できるようになります。一連の簡単な手順を通じて、フレームのプロパティやレイヤーの状態などを操作し、創造的な可能性の領域を開くことができます。

## よくある質問

### Q1: Aspose.PSD for .NET は初心者に適していますか?

A1: もちろんです！ Aspose.PSD for .NET は、ユーザーフレンドリーなインターフェイスと包括的なドキュメントを提供し、初心者と熟練した開発者の両方がアクセスできるようにします。

### Q2: GIF 画像にタイムラインの変更を適用できますか?

A2: Timeline クラスは、PSD 画像専用に設計されています。 GIF の操作については、Aspose.GIF for .NET を参照してください。

### Q3: 追加のサポートを見つけたり、問題について話し合ったりできる場所はどこですか?

 A3: にアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートと問題の議論のために。

### Q4: Aspose.PSD for .NET の一時ライセンスを取得するにはどうすればよいですか?

 A4: 仮免許を取得する[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose.PSD for .NET を使用する主な利点は何ですか?

A5: Aspose.PSD for .NET は、高度な画像処理機能、PSD ファイル操作、および高性能レンダリングを提供します。