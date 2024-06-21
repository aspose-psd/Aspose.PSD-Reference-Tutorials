---
title: Aspose.PSD for .NET で PNG に変換するときに PSD ファイルをトリミングする
linktitle: PNG への変換時に PSD ファイルをトリミングする
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用して PSD ファイルを簡単にトリミングする方法を学びます。 PNG へのシームレスな変換については、ステップバイステップのガイドに従ってください。
type: docs
weight: 18
url: /ja/net/psd-file-manipulation/crop-psd-conversion-png/
---
## 導入
.NET 開発の分野では、イメージの操作と変換は一般的なタスクです。 Aspose.PSD for .NET は、このプロセスを効率化するための強力なツール セットを提供します。よくある要件の 1 つは、PSD ファイルを PNG に変換する前にトリミングすることです。このステップバイステップのチュートリアルでは、Aspose.PSD for .NET を使用するプロセスを詳しく説明します。
## 前提条件
この旅を始める前に、以下のものがあることを確認してください。
-  Aspose.PSD for .NET ライブラリ: からライブラリをダウンロードしてインストールします。[Aspose.PSD for .NET ドキュメント](https://reference.aspose.com/psd/net/).
- サンプル PSD ファイル: 実験用に PSD ファイルを用意します。お持ちでない場合は、チュートリアルで提供されているサンプルを使用できます。
- .NET 環境: 動作する .NET 開発環境がセットアップされていることを確認してください。
- ドキュメント ディレクトリ: コード内でドキュメント ディレクトリへのパスを指定します。
## 名前空間のインポート
.NET プロジェクトに、Aspose.PSD for .NET に必要な名前空間を含めます。
```csharp
using Aspose.PSD.ImageOptions;
```
## ステップ 1: PSD 画像をロードする
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "Your Document Directory";
string srcPath = dataDir + @"sample.psd";
//既存の PSD 画像をロードする
using (RasterImage image = (RasterImage)Image.Load(srcPath))
{
    //さらなるステップのコードはここにあります
}
```
## ステップ 2: 切り抜き四角形を定義する
```csharp
//x、y、幅、高さを渡して Rectangle クラスのインスタンスを作成します
Rectangle cropRectangle = new Rectangle(0, 0, 350, 450);
```
## ステップ 3: 画像をトリミングする
```csharp
//Imageクラスのcropメソッドを呼び出し、rectangleクラスのインスタンスを渡す
image.Crop(cropRectangle);
```
## ステップ 4: PNG オプションを指定する
```csharp
//PngOptions クラスのインスタンスを作成する
PngOptions pngOptions = new PngOptions();
```
## ステップ 5: 切り取った画像を PNG として保存します。
```csharp
// save メソッドを呼び出し、出力パスを指定し、PSD ファイルを PNG に変換して出力を保存する PngOptions を指定します。
string destName = dataDir + @"export.png";
image.Save(destName, pngOptions);
```
## 結論

おめでとう！ Aspose.PSD for .NET を使用して PSD ファイルを PNG に変換するときにトリミングする方法を学習しました。この機能は、さまざまな画像処理シナリオで非常に役立ちます。

## よくある質問

### Q1: このライブラリを商用プロジェクトで使用できますか?

 A1: はい、Aspose.PSD for .NET は商用利用できます。参照する[Aspose.PSD ライセンス](https://purchase.aspose.com/buy)詳細については。

### Q2: 無料トライアルはありますか?

 A2: もちろんです！無料の試用版を試すことができます[ここ](https://releases.aspose.com/).

### Q3: Aspose.PSD for .NET のサポートはどこで見つけられますか?

 A3: にアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)サポートやご質問がございましたら。

### Q4: 仮免許はどのように取得すればよいですか?

A4: 仮免許が必要な場合は取得できます。[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: ドキュメントに利用可能な例やチュートリアルはありますか?

 A5: はい、包括的なドキュメントと例を見つけることができます。[ここ](https://reference.aspose.com/psd/net/).