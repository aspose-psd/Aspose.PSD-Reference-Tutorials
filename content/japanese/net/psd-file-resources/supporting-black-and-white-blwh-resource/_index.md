---
title: Aspose.PSD for .NET での白黒リソースのサポート
linktitle: 白黒 (Blwh) リソースのサポート
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用した高度な画像編集を試してください。画像要素を正確に制御するために、白黒調整レイヤーをマスターする方法を学びます。
type: docs
weight: 13
url: /ja/net/psd-file-resources/supporting-black-and-white-blwh-resource/
---
## 導入
ダイナミックなデジタル メディアの世界では、画像編集は魅力的なビジュアルを作成する上で極めて重要な役割を果たします。 Aspose.PSD for .NET は、開発者が画像操作機能を次のレベルに引き上げられるようにします。このチュートリアルでは、画像を正確に微調整できるようにする、Aspose.PSD の白黒調整レイヤーのサポートについて説明します。
## 前提条件
チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。
- Aspose.PSD for .NET: からライブラリをダウンロードしてインストールします。[Aspose.PSD for .NET ドキュメント](https://reference.aspose.com/psd/net/).
- ドキュメント ディレクトリ: ドキュメント ディレクトリへのパスを指定します。
- 出力ディレクトリ: 編集した画像を保存するディレクトリを定義します。
## 名前空間のインポート
まず、必要な名前空間をプロジェクトにインポートします。
```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using System;
```
## ステップ 1: 画像をロードする
Aspose.PSD を使用してソース イメージを読み込みます。
```csharp
string sourceFileName = "YourImage.psd";
string destinationFileName = OutputDir + "Output_" + sourceFileName;
using (PsdImage image = (PsdImage)Image.Load(SourceDir + sourceFileName))
{
    //画像処理のコードはここに入れます
}
```
## ステップ 2: 白黒調整レイヤーを実装する
次に、Aspose.PSD での白黒調整レイヤーのサポートについて調べてみましょう。の`ExampleSupportOfBlwhResource`メソッドはこの機能を示します。
```csharp
void ExampleSupportOfBlwhResource(
    string sourceFileName,
    int reds,
    int yellows,
    int greens,
    int cyans,
    int blues,
    int magentas,
    bool useTint,
    int bwPresetKind,
    string bwPresetFileName,
    double tintColorRed,
    double tintColorGreen,
    double tintColorBlue,
    int tintColor,
    int newTintColor)
{
    //白黒調整レイヤーの実装はここにあります
}
```
## ステップ 3: 変更を検証して保存する
指定された白黒調整リソースが見つかったことを確認し、プロパティ値を検証して、編集した画像を保存します。
```csharp
ExampleSupportOfBlwhResource(
    "YourImage.psd",
    //必要に応じて他のパラメータを指定します
);
Console.WriteLine("SupportForBlwhResource executed successfully");
```
## 結論

Aspose.PSD for .NET は、画像編集機能を強化するための堅牢なプラットフォームを提供します。白黒調整レイヤーのサポートを活用することで、開発者は画像要素を正確に制御でき、創造的な表現の新たな可能性が広がります。

## よくある質問

### Q1: Aspose.PSD はさまざまな画像形式と互換性がありますか?

A1: はい、Aspose.PSD は幅広い画像形式をサポートしており、さまざまなファイル タイプを柔軟に処理できます。

### Q2: 1 つの画像に複数の調整レイヤーを適用できますか?

A2：もちろんです！ Aspose.PSD を使用すると、複数の調整レイヤーを積み重ねることができ、複雑な画像操作が可能になります。

### Q3: Aspose.PSD の一時ライセンスを取得するにはどうすればよいですか?

 A3: にアクセスしてください。[仮免許](https://purchase.aspose.com/temporary-license/) Aspose Web サイトのページにアクセスして、テスト用の一時ライセンスを取得します。

### Q4: Aspose.PSD のサポートはどこで見つけられますか?

 A4:[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)は、支援を求めたり、コミュニティと洞察を共有したりするための貴重なリソースです。

### Q5: 白黒調整をテストするために利用できるサンプル画像はありますか?

A5: はい、Aspose.PSD ドキュメントにサンプル イメージがあります。