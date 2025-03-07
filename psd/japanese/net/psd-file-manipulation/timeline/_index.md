---
title: Aspose.PSD for .NET でタイムラインを操作する
linktitle: タイムラインの操作
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET Timeline クラスを使用して PSD 画像の操作を強化します。フレームのプロパティやレイヤーの状態を制御し、クリエイティブな可能性を簡単に発揮します。
weight: 16
url: /ja/net/psd-file-manipulation/timeline/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for .NET でタイムラインを操作する

## 導入
グラフィック デザインや画像操作の動的な世界では、画像のタイムラインを制御および操作する機能が重要です。Aspose.PSD for .NET は、Timeline クラスで強力なソリューションを提供します。この高度な機能により、ユーザーは PsdImage のタイムラインを変更して、フレーム遅延を変更したり、特定のフレームのレイヤー状態を編集したりすることができます。
## 前提条件
Timeline クラスが提供するエキサイティングな可能性に飛び込む前に、次の前提条件が満たされていることを確認してください。
-  Aspose.PSD for .NETライブラリ: Aspose.PSD for .NETライブラリがインストールされていることを確認してください。[Aspose.PSD for .NET ドキュメント](https://reference.aspose.com/psd/net/).
- ドキュメントと出力ディレクトリ: コード内のドキュメントと出力ディレクトリのパスを定義します。`baseDir`そして`outputDir`プロジェクト構造に応じて変数を設定します。
それでは、Timeline クラスを活用する方法を段階的に見ていきましょう。
## 名前空間のインポート
Timeline クラスの使用を開始するには、コードに必要な名前空間をインポートします。
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## ステップ1: PSDイメージを読み込む
まず、指定されたソース ファイルから PSD イメージを読み込みます。ソース ファイルのパスが正しく設定されていることを確認します。
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //以降の操作のためのコードをここに入力します
}
```
## ステップ2: タイムラインにアクセスする
PSD 画像が読み込まれたら、次のコードを使用してタイムラインにアクセスします。
```csharp
Timeline timeline = psdImage.Timeline;
```
## ステップ3: 破棄方法を変更する
特定のフレームの dispose メソッドを操作します。この例では、フレーム 1 の dispose メソッドを変更します。
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## ステップ4: フレーム遅延を調整する
特定のフレームの遅延を変更します。ここでは、フレーム 2 の遅延を 15 に変更します。
```csharp
timeline.Frames[1].Delay = 15;
```
## ステップ5: レイヤー状態を編集する
特定のフレームの「レイヤー 1」の不透明度を変更します。この例では、フレーム 2 の不透明度を 50 に設定します。
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## ステップ6: レイヤーを移動する
「レイヤー 1」を特定のフレーム（この例ではフレーム 3）の左下隅に移動します。
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## ステップ7: 新しいフレームを追加する
タイムラインに新しいフレームを追加します。
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## ステップ8: ブレンドモードを変更する
特定のフレーム（この場合はフレーム 4）の「レイヤー 1」のブレンド モードを変更します。
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## ステップ9: 変更を保存する
変更を PsdImage インスタンスに適用し、変更された PSD 画像を保存します。
```csharp
psdImage.Save(outputPsd);
```
## ステップ10: クリーンアップ
最後に、一時出力ファイルを削除してクリーンアップします。
```csharp
File.Delete(outputPsd);
```
## 結論

結論として、Aspose.PSD for .NET の Timeline クラスにより、開発者は PSD 画像のタイムラインを細かく制御できるようになります。一連の簡単な手順で、フレームのプロパティやレイヤーの状態などを操作でき、クリエイティブな可能性が広がります。

## よくある質問

### Q1: Aspose.PSD for .NET は初心者に適していますか?

A1: もちろんです! Aspose.PSD for .NET は、ユーザーフレンドリーなインターフェイスと包括的なドキュメントを提供しているため、初心者から熟練した開発者まで誰でも利用できます。

### Q2: GIF 画像にタイムラインの変更を適用できますか?

A2: Timeline クラスは PSD 画像専用に設計されています。GIF の操作については、Aspose.GIF for .NET を参照してください。

### Q3: 追加のサポートを見つけたり、問題について相談したりできる場所はどこですか?

 A3: 訪問[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティのサポートと問題に関する議論のため。

### Q4: Aspose.PSD for .NET の一時ライセンスを取得するにはどうすればよいですか?

 A4: 臨時免許を取得する[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose.PSD for .NET を使用する主な利点は何ですか?

A5: Aspose.PSD for .NET は、高度な画像処理機能、PSD ファイル操作、および高性能レンダリングを提供します。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
