---
title: Aspose.PSD for .NET で PSD ファイルを PNG に変換するときに切り取る
linktitle: PNG に変換するときに PSD ファイルをトリミングする
second_title: Aspose.PSD .NET API
description: Aspose.PSD for .NET を使用して PSD ファイルを簡単に切り抜く方法を学びます。PNG へのシームレスな変換については、ステップバイステップのガイドに従ってください。
type: docs
weight: 18
url: /ja/net/psd-file-manipulation/crop-psd-conversion-png/
---
## 導入
.NET 開発の分野では、画像の操作と変換は一般的なタスクです。Aspose.PSD for .NET は、このプロセスを効率化する強力なツール セットを提供します。よくある要件の 1 つは、PSD ファイルを PNG に変換する前にトリミングすることです。このステップ バイ ステップのチュートリアルでは、Aspose.PSD for .NET を使用してこのプロセスを詳しく説明します。
## 前提条件
この旅に出発する前に、以下のものを用意しておいてください。
-  Aspose.PSD for .NETライブラリ: ライブラリを以下のサイトからダウンロードしてインストールします。[Aspose.PSD for .NET ドキュメント](https://reference.aspose.com/psd/net/).
- サンプル PSD ファイル: 実験用に PSD ファイルを用意してください。 PSD ファイルがない場合、チュートリアルで提供されているサンプルを使用できます。
- .NET 環境: 動作する .NET 開発環境が設定されていることを確認します。
- ドキュメント ディレクトリ: コード内でドキュメント ディレクトリへのパスを指定します。
## 名前空間のインポート
.NET プロジェクトに、Aspose.PSD for .NET に必要な名前空間を含めます。
```csharp
using Aspose.PSD.ImageOptions;
```
## ステップ1: PSDイメージを読み込む
```csharp
//ドキュメント ディレクトリへのパス。
string dataDir = "Your Document Directory";
string srcPath = dataDir + @"sample.psd";
//既存のPSD画像を読み込む
using (RasterImage image = (RasterImage)Image.Load(srcPath))
{
    //次のステップのコードはここに記入します
}
```
## ステップ2: 切り抜き長方形を定義する
```csharp
//x、y、幅、高さを渡してRectangleクラスのインスタンスを作成します。
Rectangle cropRectangle = new Rectangle(0, 0, 350, 450);
```
## ステップ3: 画像をトリミングする
```csharp
//Imageクラスのcropメソッドを呼び出し、rectangleクラスのインスタンスを渡します。
image.Crop(cropRectangle);
```
## ステップ4: PNGオプションを指定する
```csharp
//PngOptionsクラスのインスタンスを作成する
PngOptions pngOptions = new PngOptions();
```
## ステップ5: 切り取った画像をPNGとして保存する
```csharp
//saveメソッドを呼び出し、出力パスとPngOptionsを指定してPSDファイルをPNGに変換し、出力を保存します。
string destName = dataDir + @"export.png";
image.Save(destName, pngOptions);
```
## 結論

おめでとうございます! Aspose.PSD for .NET を使用して PSD ファイルを PNG に変換するときにトリミングする方法を学習しました。この機能は、さまざまな画像処理シナリオで非常に役立ちます。

## よくある質問

### Q1: このライブラリを商用プロジェクトで使用できますか?

 A1: はい、Aspose.PSD for .NETは商用利用可能です。[Aspose.PSD ライセンス](https://purchase.aspose.com/buy)詳細については。

### Q2: 無料トライアルはありますか?

A2: もちろんです！無料試用版をお試しください[ここ](https://releases.aspose.com/).

### Q3: Aspose.PSD for .NET のサポートはどこで見つかりますか?

 A3: 訪問[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)ご不明な点やご質問がございましたら、お気軽にお問い合わせください。

### Q4: 一時ライセンスを取得するにはどうすればよいですか?

A4: 臨時免許証が必要な場合は取得できます[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: ドキュメントには例やチュートリアルはありますか?

 A5: はい、包括的なドキュメントと例を見つけることができます[ここ](https://reference.aspose.com/psd/net/).