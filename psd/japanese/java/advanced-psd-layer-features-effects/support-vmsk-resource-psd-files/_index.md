---
date: 2026-06-03
description: Aspose.PSD for Java を使用して PSD を PNG に変換し、Java でベクターマスクを作成する方法、ベクターマスク
  PSD の追加、そして Vmsk リソースをプログラムで操作する方法を学びます。
keywords:
- convert psd to png
- add vector mask psd
- psd vector mask tutorial
- aspose psd maven
linktitle: PSD を PNG に変換し、Java でベクターマスクを作成 – PSD ファイルの Vmsk リソース
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to convert PSD to PNG and create vector mask Java using Aspose.PSD
    for Java, add vector mask PSD, and manipulate Vmsk resources programmatically.
  headline: Convert PSD to PNG and Create Vector Mask Java – Vmsk Resource in PSD
    Files
  type: TechArticle
- questions:
  - answer: Create a `VmskResource`, populate it with the required path records (e.g.,
      `BezierKnotRecord`), and attach it to the layer’s resources collection.
    question: How do I add a new vector mask to an existing layer?
  - answer: Yes—after saving the PSD, load it again with `Image.load()` and call `im.save("output.png")`
      specifying the PNG format.
    question: Can I convert the edited PSD directly to PNG without opening Photoshop?
  - answer: Absolutely. Since the process is pure Java, you can embed it in Maven/Gradle
      builds, Docker containers, or any CI system that supports Java.
    question: Is there a way to automate this in a CI/CD pipeline?
  - answer: All recent releases (2024‑2025) support Java 8 and above, including Java
      11, 17, and newer LTS versions.
    question: What versions of Aspose.PSD are compatible with Java 11+?
  - answer: A free evaluation license works for development and testing. For production
      deployments, a commercial license is required.
    question: Do I need a license for development builds?
  type: FAQPage
second_title: Aspose.PSD Java API
title: PSD を PNG に変換し、Java でベクターマスクを作成 – PSD ファイルの Vmsk リソース
url: /ja/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD を PNG に変換し、ベクターマスク Java を作成 – PSD ファイル内の Vmsk リソース

## はじめに
PSD を **PNG に変換** しながら **ベクターマスク**（Vmsk）リソースを Photoshop ファイル内に作成する必要がある場合、Aspose.PSD for Java は両方をクリーンにプログラムで実行できる方法を提供します。デザイン自動化ツール、アセットを検証する CI パイプライン、またはカスタムマスクでグラフィックワークフローを拡張する場合でも、このチュートリアルでは PSD の読み込み、Vmsk リソースの取得、プロパティの調整、PNG へのエクスポート、変更後のファイルの保存という手順をすべて解説します。最後まで実施すれば、ベクターマスクの取り扱い、PSD → PNG の変換、追加のベクターデータでファイルを拡張する方法に慣れ、**convert PSD to PNG** のテクニックを習得できます。

## クイック回答
- **Vmsk リソースとは何ですか？** それは PSD ファイル内に保存されているベクターマスクデータで、レイヤーの複雑なベクトル形状を定義します。  
- **どのライブラリがサポートしていますか？** Aspose.PSD for Java が Vmsk リソースへの完全な読み書きアクセスを提供します。  
- **ライセンスは必要ですか？** 無料トライアルが利用可能です。商用利用には有償ライセンスが必要です。  
- **編集した PSD を PNG に変換できますか？** はい。保存後に PSD を読み込み、同じ API で PNG にエクスポートできます。  
- **Maven のサポートはありますか？** もちろんです。Aspose.PSD は Maven 依存関係として追加できます（「aspose psd maven」キーワード参照）。

## ベクターマスク（Vmsk リソース）とは？
ベクターマスク（Vmsk）は、ピクセルベースではなくベジェ曲線とパスレコードを使用してレイヤー上の透明領域と不透明領域を定義するマスクです。ベクターベースであるため、品質を損なうことなくスケーリングでき、高解像度グラフィックに最適です。複数のパスを含むことができ、各パスはベジェノットで構成され、透明度、塗りつぶし、レイヤーマスクへのリンクといった属性をサポートします。

## Aspose.PSD でベクターマスクを作成する理由
プログラムでベクターマスクを作成すると、手動で Photoshop を操作する必要がなくなり、膨大なファイル群での一貫性が保たれ、ビルドやデプロイパイプラインへの統合が可能になります。Aspose.PSD を使用すれば、正確なマスクジオメトリを生成し、任意のレイヤーに適用でき、完全な編集可能性を保持したまま動的グラフィック生成やレスポンシブデザインワークフローに活用できます。

- **自動化:** Photoshop を開かずにプログラムでマスクを追加・変更できます。  
- **一貫性:** 生成するすべての PSD が同じマスクルールに従うことを保証します。  
- **クロスプラットフォーム:** Java をサポートする任意の OS で動作します。  
- **統合:** 他の Aspose API（例: PSD → PNG 変換）と組み合わせてエンドツーエンドのワークフローを構築できます。  
- **スケーラビリティ:** ベクターマスクはサイズに関係なく鮮明で、レスポンシブデザインに最適です。

## Java 開発者にとっての重要性
**create vector mask java** のテクニックを使用すれば、バックエンドサービス、CI パイプライン、デスクトップユーティリティに高度なグラフィックロジックを直接組み込めます。デザイナーが手動でマスクを追加する必要がなくなり、コードだけでオンザフライに生成・調整できるため、時間とヒューマンエラーを大幅に削減できます。

## 前提条件
コードに入る前に、以下が揃っていることを確認してください。

### 必要なもの
- **Java Development Kit (JDK):** JDK 8 以上をインストールしてください。ダウンロードは [Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-downloads.html) から。  
- **Aspose.PSD for Java ライブラリ:** PSD ファイルを操作する強力なライブラリです。ダウンロードは [Aspose のリリースページ](https://releases.aspose.com/psd/java/) から。クイックスタート用に同ページまたは [free trial](https://releases.aspose.com/) から無料トライアルを取得してください。  
- **IDE:** 任意の Java IDE（IntelliJ IDEA、Eclipse、NetBeans）で構いません。

### ワークスペースの設定手順
1. **新規 Java プロジェクトを作成** – 好みの IDE で新しいプロジェクトを開始します。  
2. **Aspose ライブラリを追加** – ダウンロードした Aspose JAR をプロジェクトのビルドパスに追加し、PSD 関連クラスにアクセスできるようにします。

環境が整ったら、実装手順に進みます。

## Aspose.PSD for Java を使用して PSD を PNG に変換する方法
`PsdImage.load()` でソース PSD を読み込み、必要に応じてベクターマスクを編集し、`save()` に `ExportFormat.Png` を指定して保存します。Aspose.PSD はカラープロファイル、レイヤー、マスクデータを自動的に処理し、元のビジュアルと一致するピクセルパーフェクトな PNG を生成します。この 2 段階のフローはサイズに関係なくすべての PSD で機能し、Java 対応プラットフォーム上で動作します。

## パッケージのインポート
`com.aspose.psd` パッケージは、画像の読み込み、リソース操作、エクスポート機能など、PSD ファイル処理に必要なコアクラスを提供します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

準備ができたら、各操作を順に見ていきましょう。

## 手順 1: PSD ファイルの読み込み
ファイルを読み込むと、メモリ上にドキュメント全体を表す `PsdImage` オブジェクトが取得できます。

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` に PSD ファイルがあるディレクトリを設定します。  
- `sourceFileName` 文字列を作成し、ディレクトリと PSD ファイル名を結合します。  
- 最後に `Image.load()` を使って PSD を `PsdImage` オブジェクトにロードします。

## 手順 2: Vmsk リソースの取得
`VmskResource` クラスは PSD レイヤー内に保存されたベクターマスクデータをカプセル化します。取得することでマスクパスを検査・変更できます。

```java
VmskResource resource = getVmskResource(im);
```

- 画像から Vmsk リソースを検索・取得する `getVmskResource()` メソッドを呼び出します。

## 手順 3: Vmsk リソースプロパティの検証
変更を加える前に、マスクが有効で正しい向きか、期待通りのパス数があるかを確認します。

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- ここでは Vmsk リソースの各種プロパティをチェックしています。無効化、反転、リンク解除されていないか、パス数が正しいかを確認します。

## 手順 4: 各パスへのアクセスと検証
各パスレコードはベクトル形状の一部を記述します。検証することで正しいジオメトリを扱っていることを確認できます。

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- 3 つの特定パスレコードを抽出し、タイプとプロパティを検証して基準を満たすか確認しています。

## 手順 5: Vmsk リソースの編集
ここからが実際の変更パートです。ワークフローに合わせてマスクの動作フラグを切り替えられます。

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- このブロックでは Vmsk リソースのさまざまなプロパティを `true` に設定し、マスクの振る舞いを制御しています。

## 手順 6: ベジェノットポイントの変更
ベジェノットは各ベクトルセグメントの曲率を定義します。ポイントを調整することでラスタライズせずにマスクの形状を変形できます。

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- 特定の `BezierKnotRecord` パスにアクセスし、ポイントを変更してベクターマスクを再形成しています。

## 手順 7: 変更済み PSD の保存
すべての編集が完了したら、変更を新しい PSD ファイルに永続化します。

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- エクスポート先の PSD パスを設定し、`im.save()` を呼び出して新ファイルに書き出します。

## 手順 8: PSD を PNG にエクスポート
更新されたマスクを含む PSD を直接 PNG にエクスポートします。これが **convert PSD to PNG** ワークフローの実演です。

```java
im.dispose();
```

- `im.save("output.png", ExportFormat.Png)` を使用して、編集済みベクターマスクを反映した高品質 PNG を生成します。

## リソースのクリーンアップ
最後に、画像オブジェクトを適切に破棄してリソースを解放する必要があります。

CODE_BLOCK_PLACEHOLDER_9_END

- 長時間実行するプロセスでは、使用後に必ずリソースを破棄することがベストプラクティスです。メモリリーク防止につながります。

## よくある問題と解決策
| 問題 | 発生理由 | 解決方法 |
|------|----------|----------|
| **`VmskResource` が見つかりません** | PSD にベクターマスクレイヤーが含まれていない | ソース PSD にベクターマスクがあるか確認するか、Photoshop で手動で追加してください。 |
| **パスアクセス時の `ArrayIndexOutOfBoundsException`** | 期待したパスレコード数が異なる | `resource.getPaths().length` を確認し、インデックス使用を調整してください。 |
| **ライセンス例外** | 有効な Aspose.PSD ライセンスなしで実行 | `License license = new License(); license.setLicense("Aspose.PSD.lic");` でトライアルまたは購入ライセンスを適用してください。 |
| **メモリリーク** | 長時間実行プロセスで画像が破棄されていない | `finally` ブロックで必ず `im.dispose()` を呼び出すか、サポートされていれば try‑with‑resources を使用してください。 |

## FAQ

**Q: 既存レイヤーに新しいベクターマスクを追加するには？**  
A: `VmskResource` を作成し、必要なパスレコード（例: `BezierKnotRecord`）を設定して、レイヤーのリソースコレクションに添付します。

**Q: Photoshop を開かずに編集済み PSD を直接 PNG に変換できますか？**  
A: はい。PSD を保存した後、再度 `Image.load()` で読み込み、`im.save("output.png")` と PNG フォーマットを指定すれば可能です。

**Q: CI/CD パイプラインで自動化できますか？**  
A: もちろんです。純粋な Java プロセスなので、Maven/Gradle ビルド、Docker コンテナ、または Java をサポートする任意の CI システムに組み込めます。

**Q: Java 11 以降で互換性のある Aspose.PSD バージョンは？**  
A: 最近のリリース（2024‑2025）はすべて Java 8 以上、特に Java 11、17、その他の LTS バージョンをサポートしています。

**Q: 開発ビルドでもライセンスは必要ですか？**  
A: 開発・テスト用には無料評価ライセンスで動作します。商用デプロイには有償ライセンスが必要です。

---

**最終更新日:** 2026-06-03  
**テスト環境:** Aspose.PSD 24.11 for Java  
**作者:** Aspose

## 関連チュートリアル

- [Export PSD to PNG with Layer Mask Support in Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [Convert PSD to PNG with Color Overlay – Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}