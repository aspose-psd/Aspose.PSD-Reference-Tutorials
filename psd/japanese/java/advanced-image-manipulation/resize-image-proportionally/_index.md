---
date: 2025-12-08
description: Aspose.PSD を使用して Java で PSD を PNG に変換し、画像を比例的にリサイズする方法を学びます。このステップバイステップのチュートリアルでは、画像のキャッシュ、リサイズ、PNG
  への保存について説明します。
language: ja
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して PSD を PNG に変換し、比例的にリサイズする方法
url: /java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用した PSD から PNG への変換と比例リサイズの方法

## はじめに

**PSD を PNG に変換**し、元のアスペクト比を保ちたい場合は、ここが最適です。このチュートリアルでは、**Aspose.PSD のチュートリアル**として、Java で画像ファイルを比例的にリサイズし、パフォーマンス向上のために画像をキャッシュし、最終的に PNG として保存する手順を解説します。最後まで読めば、このワークフローを任意の Java ベースの画像処理パイプラインに組み込むことができます。

## クイック回答
- **Aspose.PSD は PSD を PNG に変換できますか？** はい – PSD を読み込み、`PngOptions` で保存すれば完了です。
- **ライブラリは比例リサイズをサポートしていますか？** もちろんです。`resizeWidthProportionally` と `resizeHeightProportionally` を使用します。
- **まず画像をキャッシュする必要がありますか？** 大きな PSD ファイルの場合、`image.cacheData()` によるキャッシュでパフォーマンスが向上します。
- **必要な Java のバージョンは？** Java 8 以降が完全にサポートされています。
- **本番環境でライセンスは必要ですか？** はい、商用ライセンスを取得すると評価版の透かしが除去されます。

## 「PSD を PNG に変換する」とは何か、なぜ重要なのか

Photoshop ドキュメント（PSD）をポータブルネットワークグラフィックス（PNG）ファイルに変換すると、レイヤー構造を軽量でウェブフレンドリーな形式で共有できます。PNG は透過性とロスレス品質を保持するため、UI アセットやサムネイル、画像の忠実度が重要なシーンに最適です。

## なぜ Java で画像を比例リサイズするのか？

**画像を比例的にリサイズ**することで、アスペクト比が歪むことなく、さまざまな画面で自然に見えるようになります。`Aspose.PSD` API には比例スケーリング用の専用メソッドが用意されており、手動で計算ミスをする心配がありません。

## 前提条件

コードに入る前に、以下を用意してください。

1. **Java Development Kit (JDK)** – Java 8 以上がインストールされていること。
2. **Aspose.PSD for Java** – 公式サイトから最新の JAR を[こちら](https://releases.aspose.com/psd/java/)でダウンロード。
3. プロジェクトから参照できるディレクトリに配置したサンプル PSD ファイル（`sample.psd`）。

## パッケージのインポート

Java クラスに必要なインポートを追加します。これらのクラスで画像の読み込み、キャッシュ、リサイズ、PNG 出力オプションが利用可能になります。

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## 手順 1: PSD 画像の読み込み

まず、ソース PSD ファイルを読み込みます。ファイルが大きい場合は、画像データをキャッシュすることで、後続の操作時のメモリ使用量を抑えられます。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## 手順 2: 画像を比例的にリサイズ (Java)

次に新しいサイズを決めます。この例では、元のサイズの **半分** に縮小し、アスペクト比を保持します。必要に応じて幅または高さを調整してください。

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **プロのコツ:** `resizeWidthProportionally` *または* `resizeHeightProportionally` のどちらか一方を使用すれば、ライブラリが自動的にもう一方の寸法を計算し、画像を比例的に保ちます。

## 手順 3: リサイズした画像を PNG として保存

最後に、リサイズした画像を PNG 形式でエクスポートします。これで **PSD から PNG への変換**ワークフローが完了です。

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

コードを実行すると、元の PSD の半分のサイズで、同等の画質・歪みなしの PNG ファイルが生成されます。

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|------|------|------|
| **OutOfMemoryError** | 大きな PSD がキャッシュされていない | リサイズ前に `image.cacheData()` を呼び出す |
| **Blank PNG output** | ファイルパスが誤っている | `dataDir` と書き込み権限を確認 |
| **Aspect ratio looks off** | 幅と高さを手動で両方設定した | Aspose.PSD が提供する比例メソッドを使用 |

## FAQ

**Q: Aspose.PSD はすべての画像形式に対応していますか？**  
A: Aspose.PSD は PSD、PNG、JPEG、BMP、GIF など多数の形式をサポートしています。詳細は[ドキュメント](https://reference.aspose.com/psd/java/)をご覧ください。

**Q: 商用プロジェクトで Aspose.PSD を使用できますか？**  
A: はい。商用ライセンスは[Aspose ストア](https://purchase.aspose.com/buy)で購入できます。

**Q: テスト用の一時ライセンスはありますか？**  
A: あります。評価目的で[こちら](https://purchase.aspose.com/temporary-license/)から一時ライセンスをリクエストしてください。

**Q: コミュニティサポートはどこで受けられますか？**  
A: [Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)で質問や情報共有が可能です。

**Q: 完全な API リファレンスはどこで確認できますか？**  
A: 詳細な API ドキュメントは[こちら](https://reference.aspose.com/psd/java/)にあります。

## 結論

これで **PSD を PNG に変換**し、画像を比例的にリサイズし、キャッシュを活用する方法が分かりました。Aspose.PSD for Java を使って、ネイティブの Photoshop を必要とせずに高速で高品質な画像処理を実装してください。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2025-12-08  
**テスト環境:** Aspose.PSD 24.12 for Java  
**作者:** Aspose