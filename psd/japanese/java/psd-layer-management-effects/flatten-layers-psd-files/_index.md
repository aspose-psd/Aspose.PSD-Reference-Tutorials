---
date: 2026-04-03
description: Aspose.PSD for Java を使用してレイヤーをフラット化し、PSD ファイルのサイズを削減する方法を学びましょう。このステップバイステップガイドでは、PSD
  ファイルを迅速にフラット化する手順を示します。
keywords:
- reduce psd file size
- how to flatten psd
- flatten visible layers psd
linktitle: レイヤーをフラット化してPSDファイルサイズを削減 – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: レイヤーをフラット化してPSDファイルサイズを削減 – Aspose.PSD Java
url: /ja/java/psd-layer-management-effects/flatten-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# レイヤーをフラット化してPSDファイルサイズを削減 – Aspose.PSD Java

## はじめに

Photoshop ドキュメントを開いたときに **PSDファイルサイズを削減** する方法を考えたことがあるなら、レイヤーのフラット化は最も効果的なテクニックのひとつです。Aspose.PSD for Java を使用すれば、プログラムで PSD 全体をフラット化したり、選択したレイヤーだけをマージしたりでき、視覚品質を犠牲にせずにファイルサイズを細かくコントロールできます。このチュートリアルでは、画像全体をフラット化する方法と特定のレイヤーだけをマージする方法の両方を解説し、PSD ファイルをすばやく縮小し、ワークフローをスムーズに保つ方法を紹介します。

## クイック回答
- **フラット化すると何が起きますか？** 可視レイヤーを単一の背景レイヤーに統合し、レイヤー情報を削除してファイルサイズを削減することが多いです。  
- **選択したレイヤーだけをフラット化できますか？** はい、特定のレイヤーだけをマージし、他はそのままにできます。  
- **ライセンスは必要ですか？** 開発用には無料トライアルで動作しますが、製品環境では商用ライセンスが必要です。  
- **必要なJavaバージョンは？** JDK 8 以上。  
- **フラット化は画像品質に影響しますか？** いいえ、視覚的な外観は変わらず、レイヤー構造だけが変わります。

## “PSDファイルサイズを削減” とは？

PSD ファイルサイズを削減するとは、不要なデータ（余分なレイヤー、非表示チャンネル、過剰なメタデータなど）を除去し、ファイルを軽くして読み込み・共有・処理を高速化することです。レイヤーをフラット化するのは、個別のレイヤーオブジェクトを破棄しつつ最終的な合成画像を保持できる一般的な手法です。

## なぜ Aspose.PSD for Java でレイヤーをフラット化するのか？

- **自動化:** Photoshop を手動で開く必要がなく、Java アプリケーションに直接組み込めます。  
- **精度:** ドキュメント全体をフラット化するか、表示中のレイヤーだけをフラット化（`flattenImage`）するか、選択レイヤーをマージ（`mergeLayers`）するか選べます。  
- **パフォーマンス:** ファイルが小さくなると読み込みが速くなり、下流プロセスでのメモリ使用量も減ります。  
- **クロスプラットフォーム:** Java が動作するすべての OS で利用可能です。

## 前提条件

1. **Java Development Kit (JDK):** JDK 8 以上がインストールされていること。  
2. **Aspose.PSD for Java:** ライブラリは [here](https://releases.aspose.com/psd/java/) からダウンロードしてください。  
3. **IDE:** IntelliJ IDEA、Eclipse、または任意の Java 対応 IDE。  
4. **基本的なJava知識:** 手順の理解に役立ちますが必須ではありません。  
5. **サンプルPSD:** 複数レイヤーを含むファイル（例: `ThreeRegularLayersSemiTransparent.psd`）。

これで準備が整ったので、コードに入りましょう。

## パッケージのインポート

まず、必要な Aspose.PSD クラスをインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

これらのインポートにより、PSDファイルの読み込み、レイヤーの操作、結果の保存が可能になります。

## 手順 1: PSD全体画像をフラット化

画像全体をフラット化することは、**PSDファイルサイズを削減**する最も手早い方法です。個々のレイヤーデータがすべて削除されます。

### 1.1 PSDファイルを読み込む

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 1.2 画像をフラット化

```java
im.flattenImage();
```

### 1.3 フラット化した画像を保存

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

新しいファイルは単一の背景レイヤーのみを含むため、通常はPSDサイズが小さくなります。

## 手順 2: 特定のレイヤーをマージ（PSDを選択的にフラット化する方法）

場合によっては、**表示中のレイヤーだけをフラット化**したり、他のレイヤーは編集可能なままサブセットを結合したいことがあります。

### 2.1 PSDファイルを再度読み込む

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 2.2 レイヤーを特定して選択

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

### 2.3 レイヤーをマージ

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

### 2.4 既存のレイヤーをマージしたレイヤーで置き換える

```java
img.setLayers(new Layer[]{layer2});
```

### 2.5 更新されたPSDファイルを保存

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

これでPSDはマージされたレイヤーだけを含み、保持したいレイヤーを残しつつファイルサイズを削減できます。

## よくある問題とヒント

- **フラット化前にバックアップ:** フラット化後は元に戻せません。必ず元の PSD のコピーを残しておきましょう。  
- **可視性が重要:** `flattenImage()` は *可視* レイヤーだけをマージします。フラット化したくないレイヤーは非表示にしてください。  
- **メモリ使用量:** 大きな PSD は大量の RAM を消費することがあります。十分なメモリを持つマシンで処理することを検討してください。  
- **ブレンドモード:** マージは各レイヤーのブレンドモードを考慮するため、Photoshop で見たときと同じ視覚結果になります。

## よくある質問

**Q: Aspose.PSDでレイヤーのフラット化を元に戻すことはできますか？**  
A: できません。フラット化は不可逆です。必ず元のファイルのバックアップを残してください。

**Q: 表示中のレイヤーだけをフラット化できますか？**  
A: はい。`flattenImage()` はレイヤーの可視性を尊重するので、フラット化したくないレイヤーは非表示にしておきます。

**Q: レイヤーをフラット化するとファイルサイズは減りますか？**  
A: 一般的に、レイヤー情報やメタデータが削除されるためサイズは小さくなりますが、削減率は内容次第です。

**Q: 異なるブレンドモードのレイヤーをマージできますか？**  
A: もちろんです。Aspose.PSDはブレンドモードを保持したままレイヤーをマージします。

**Q: 隣接していないレイヤーをマージしようとしたらどうなりますか？**  
A: Aspose.PSDはスタック順に関係なく任意のレイヤーをマージでき、結果は結合後の見た目になります。

---

**最終更新日:** 2026-04-03  
**テスト環境:** Aspose.PSD 24.11 for Java  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}