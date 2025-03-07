---
title: Aspose.PSD for .NET で画像を回転する
linktitle: 画像を回転する
second_title: Aspose.PSD .NET API
description: Aspose.PSD を使用して .NET で画像を簡単に回転する方法を学びます。ステップバイステップのチュートリアルに従ってください。
weight: 15
url: /ja/net/image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for .NET で画像を回転する

## 導入

.NET を使用して画像操作の世界に飛び込む場合、Aspose.PSD はシームレスで効率的な画像処理に最適なツールです。このチュートリアルでは、基本的なタスクである Aspose.PSD for .NET を使用して画像を回転することに焦点を当てます。プロセスをシンプルで実用的な手順に分解しながら進めていきます。

## 前提条件

始める前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD for .NETライブラリ: ライブラリを以下のサイトからダウンロードしてインストールします。[Aspose.PSD .NET ドキュメント](https://reference.aspose.com/psd/net/).

- ドキュメント ディレクトリ: 画像を保存するディレクトリを設定します。コード スニペットの「ドキュメント ディレクトリ」をこのディレクトリへのパスに置き換えます。

## 名前空間のインポート

Aspose.PSD 機能にアクセスするために必要な名前空間を必ず含めてください。.NET プロジェクトの先頭に次の行を追加します。

```csharp
using Aspose.PSD.ImageOptions;
```

## ステップ1: 画像を読み込む

```csharp
string sourceFile = dataDir + @"sample.psd";

//既存の画像をRasterImageクラスのインスタンスに読み込みます
using (Image image = Image.Load(sourceFile))
{
```

## ステップ2: 画像を回転する

```csharp
    //画像を時計回りに270度回転します
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## ステップ3: 回転した画像を保存する

```csharp
    //回転した画像をJPEGファイルとして保存する
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

これで完了です。わずか数行のコードで、Aspose.PSD for .NET を使用して画像を回転できました。

## 結論

このチュートリアルでは、Aspose.PSD for .NET を使用して画像を回転する基本について説明しました。Aspose.PSD は、画像操作用の強力なツール セットを提供するため、.NET 開発者にとって不可欠なライブラリとなっています。さまざまな回転を試し、画像処理ワークフローを強化するさらなる機能を探ってみましょう。

## よくある質問

### Q1: Aspose.PSD を使用して、カスタム角度で画像を回転できますか?

はい、Aspose.PSDでは回転のカスタム角度を指定できます。`RotateFlipType.Rotate270FlipNone`希望の回転角度に合わせて線を引きます。

### Q2: Aspose.PSD はさまざまな画像形式と互換性がありますか?

もちろんです。Aspose.PSDはPSD、JPEG、PNGなど、幅広い画像形式をサポートしています。[ドキュメント](https://reference.aspose.com/psd/net/)完全なリストについては、こちらをご覧ください。

### Q3: Aspose.PSD の一時ライセンスを取得するにはどうすればよいですか?

訪問する[一時ライセンスページ](https://purchase.aspose.com/temporary-license/)評価目的で一時ライセンスを取得するには、Aspose Web サイトにアクセスしてください。

### Q4: Aspose.PSD のサポートはどこで見つかりますか?

ご質問やサポートについては、[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティとつながりましょう。

### Q5: Aspose.PSD を商用目的で購入できますか?

もちろんです。[購入ページ](https://purchase.aspose.com/buy)ニーズに合わせたライセンスを取得します。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
