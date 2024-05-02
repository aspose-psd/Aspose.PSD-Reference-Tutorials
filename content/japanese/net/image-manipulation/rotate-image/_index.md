---
title: Aspose.PSD for .NET での画像の回転
linktitle: 画像を回転する
second_title: Aspose.PSD .NET API
description: Aspose.PSD を使用して、.NET で画像を簡単に回転する方法を学びます。ステップバイステップのチュートリアルに従ってください。
type: docs
weight: 15
url: /ja/net/image-manipulation/rotate-image/
---
## 導入

.NET を使用した画像操作の世界に飛び込む場合、Aspose.PSD はシームレスで効率的な画像処理のための頼りになるツールです。このチュートリアルでは、Aspose.PSD for .NET を使用して画像を回転するという基本的なタスクに焦点を当てます。プロセスをシンプルで実行可能なステップに分けて説明しますので、従ってください。

## 前提条件

始める前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for .NET ライブラリ: からライブラリをダウンロードしてインストールします。[Aspose.PSD .NET ドキュメント](https://reference.aspose.com/psd/net/).

- ドキュメント ディレクトリ: 画像を保存するディレクトリを設定します。コード スニペット内の「Your Document Directory」をこのディレクトリへのパスに置き換えます。

## 名前空間のインポート

Aspose.PSD 機能にアクセスするために必要な名前空間を必ず含めてください。 .NET プロジェクトの先頭に次の行を追加します。

```csharp
using Aspose.PSD.ImageOptions;
```

## ステップ 1: 画像をロードする

```csharp
string sourceFile = dataDir + @"sample.psd";

//既存の画像を RasterImage クラスのインスタンスにロードします
using (Image image = Image.Load(sourceFile))
{
```

## ステップ 2: 画像を回転する

```csharp
    //画像を時計回りに 270 度回転します
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## ステップ 3: 回転した画像を保存する

```csharp
    //回転した画像をJPEGファイルとして保存する
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

それでおしまい！わずか数行のコードで、Aspose.PSD for .NET を使用して画像を正常に回転できます。

## 結論

このチュートリアルでは、Aspose.PSD for .NET を使用して画像を回転する基本について説明しました。 Aspose.PSD は、画像操作のための堅牢なツール セットを提供し、.NET 開発者にとって不可欠なライブラリとなっています。さまざまな回転を試して、画像処理ワークフローを強化するさらなる機能を探索してください。

## よくある質問

### Q1: Aspose.PSD を使用して画像をカスタム角度で回転できますか?

はい、Aspose.PSD では回転のカスタム角度を指定できます。単に交換するだけです`RotateFlipType.Rotate270FlipNone`希望の回転角度の線に合わせます。

### Q2: Aspose.PSD はさまざまな画像形式と互換性がありますか?

絶対に。 Aspose.PSD は、PSD、JPEG、PNG などを含む幅広い画像形式をサポートしています。チェックしてください[ドキュメンテーション](https://reference.aspose.com/psd/net/)完全なリストについては、

### Q3: Aspose.PSD の一時ライセンスを取得するにはどうすればよいですか?

訪問[一時ライセンスのページ](https://purchase.aspose.com/temporary-license/) Aspose Web サイトにアクセスして、評価目的の一時ライセンスを取得します。

### Q4: Aspose.PSD のサポートはどこで見つけられますか?

ご質問やサポートが必要な場合は、次のサイトにアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)そしてコミュニティとつながりましょう。

### Q5: Aspose.PSD を商用目的で購入できますか?

確かに。を探索してください[購入ページ](https://purchase.aspose.com/buy)ニーズに合わせたライセンスを取得します。