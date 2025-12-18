---
date: 2025-12-18
description: Aspose.PSD for Java を使用して PSD ファイルにベクターマスク（Vmsk リソース）を作成する方法を学びましょう。このステップバイステップのチュートリアルでは、ベクターマスクの追加、PSD
  から PNG への変換、その他の操作方法を示します。
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: JavaでPSDファイルにベクトルマスク（Vmskリソース）を作成する
url: /ja/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JavaでPSDファイルにベクトルマスク（Vmskリソース）を作成する

## Introduction
Photoshop（PSD）ファイル内に **ベクトルマスク**（Vmsk）リソースを **作成** したい場合、Aspose.PSD for Java を使用すると、クリーンでプログラム的な方法で実現できます。デザイン自動化ツールを構築する場合でも、既存のグラフィックパイプラインにカスタムマスク機能を追加する場合でも、このチュートリアルでは、PSD の読み込み、Vmsk リソースの取得、プロパティの調整、結果の保存までの手順をすべて解説します。最後まで読むと、ベクトルマスクの取り扱い、PSD から PNG への変換、追加のベクトルデータでファイルを拡張する方法が身につきます。

## Quick Answers
- **Vmsk リソースとは何ですか？** PSD ファイル内に保存されているベクトルマスクデータで、レイヤーの複雑なベクトル形状を定義します。  
- **どのライブラリがサポートしていますか？** Aspose.PSD for Java が Vmsk リソースの完全な読み書きを提供します。  
- **ライセンスは必要ですか？** 無料トライアルがあります。商用利用には製品ライセンスが必要です。  
- **編集した PSD を PNG に変換できますか？** はい。保存後に PSD を読み込み、同じ API で PNG にエクスポートできます。  
- **Maven のサポートはありますか？** もちろんです。Aspose.PSD は Maven 依存として追加できます（「aspose psd maven」キーワードを参照）。

## What is a Vector Mask (Vmsk Resource)?
ベクトルマスク（Vmsk）は、ピクセルベースではなくベジエ曲線とパスレコードを使用してレイヤー上の透明領域と不透明領域を定義するマスクです。ベクトルベースであるため、解像度を落とさずにスケーリングでき、高解像度グラフィックに最適です。

## Why Create a Vector Mask with Aspose.PSD?
- **Automation:** Photoshop を開かずにプログラムからマスクを追加・変更できます。  
- **Consistency:** 生成するすべての PSD が同じマスクルールに従うことを保証します。  
- **Cross‑platform:** Java が動作する OS ならどこでも利用可能です。  
- **Integration:** 他の Aspose API（例: PSD → PNG 変換）と組み合わせてエンドツーエンドのワークフローを構築できます。

## Prerequisites
コードに入る前に、以下の環境が整っていることを確認してください。

### What You Need
- Java Development Kit (JDK): マシンに JDK がインストールされていることを確認してください。未インストールの場合は、[Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html) からダウンロードできます。  
- Aspose.PSD for Java Library: PSD ファイル管理用の強力なライブラリです。[Aspose release page](https://releases.aspose.com/psd/java/) からダウンロードできます。購入前に試したい方は、[free trial](https://releases.aspose.com/) も利用可能です。  
- An IDE: IntelliJ IDEA、Eclipse など、任意の Java IDE が使用できます。

### Setting Up Your Workspace
1. **Create a New Java Project** – お好みの IDE で新規プロジェクトを作成します。  
2. **Add the Aspose Library** – ダウンロードした Aspose JAR をプロジェクトのビルドパスに追加し、PSD 関連クラスにアクセスできるようにします。

環境が整ったら、実装に進みましょう。

## How to create vector mask in PSD files with Java
以下はステップバイステップのガイドです。コードブロックは元のチュートリアルと同一で、各ステップを分かりやすく説明するテキストを追加しています。

## Import Packages
PSD ファイルを操作する前に、Aspose.PSD ライブラリから必要なクラスをインポートします。

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

これで準備完了です。各操作を順に見ていきます。

## Step 1: Load Your PSD File
最初に行うべきことは PSD ファイルの読み込みです。ここからすべてが始まります。

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` に PSD ファイルが格納されているディレクトリを設定します。  
- `sourceFileName` にはディレクトリと PSD ファイル名を結合した文字列を作成します。  
- 最後に `Image.load()` を使って PSD を `PsdImage` オブジェクトにロードします。

## Step 2: Retrieve the Vmsk Resource
PSD 画像がロードできたら、Vmsk リソースを取得します。

```java
VmskResource resource = getVmskResource(im);
```

- `getVmskResource()` メソッドを呼び出すことで、画像内から Vmsk リソースを検索・取得します。

## Step 3: Validate Vmsk Resource Properties
変更を加える前に、Vmsk リソースが期待通りの状態か検証することが重要です。

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- ここでは Vmsk リソースの各種プロパティをチェックしています。無効化、反転、リンク状態でないこと、パス数が正しいことを確認します。

## Step 4: Access Each Path and Validate
さらに深く掘り下げて、Vmsk リソース内のパスを検証します。

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

- 3 つの特定パスレコードを抽出し、タイプやプロパティが基準を満たしているか検証します。

## Step 5: Edit the Vmsk Resource
いよいよ変更フェーズです。必要に応じて Vmsk リソースのプロパティを調整できます。

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- このブロックでは Vmsk の各種フラグを `true` に設定し、マスクの動作を制御しています。

## Step 6: Modify the Bezier Knot Points
ベジエノットはベクトルパスの要です。ここでいくつかの値を変更します。

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- 特定の `BezierKnotRecord` パスにアクセスし、ポイントを変更してベクトルマスクの形状を再構成します。

## Step 7: Save the Modified PSD File
すべての編集が完了したら、変更後の PSD を保存します。

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- エクスポート先の PSD パスを設定し、`im.save()` を呼び出して新しいファイルに書き込みます。

## Step 8: Clean Up Resources
最後に、画像リソースを適切に破棄してリソースを解放します。

```java
im.dispose();
```

- 使用後は必ずリソースを破棄する習慣をつけましょう。メモリリーク防止につながります。

## Conclusion
おめでとうございます！Aspose.PSD for Java を使用して PSD ファイル内に **ベクトルマスク**（Vmsk）リソースを作成する一連の手順を完了しました。画像のロード、Vmsk の取得と検証、プロパティの編集、そして修正後の PSD の保存まで、ベクトルマスクワークフローを自動化するための基礎が身についたはずです。これらのテクニックを活用してデザインパイプラインを強化したり、他の Aspose API（例: PSD → PNG 変換）と統合したり、カスタムグラフィックツールを構築したりしてください。

## FAQ's
### What is a Vmsk resource?
Vmsk リソースは PSD ファイル内のベクトルマスクで、複雑なベクトル形状と編集機能を提供します。

### Can I use Aspose.PSD in a Maven project?
はい。リポジトリの座標を使用して、Maven プロジェクトの依存として Aspose.PSD を追加できます。

### What format can I save my modified PSD files in?
修正後のファイルは PSD のまま保存することも、PNG、JPEG など他の形式にエクスポートすることも可能です。

### Is there a free trial available for Aspose.PSD?
はい、Aspose.PSD の無料トライアルで機能をテストできます。詳しくは [free trial link](https://releases.aspose.com/) をご覧ください。

### How can I get support for Aspose.PSD?
サポートやトラブルシューティングは [Aspose forum](https://forum.aspose.com/c/psd/34) で受けられます。

## Frequently Asked Questions
**Q: How do I add a new vector mask to an existing layer?**  
A: `VmskResource` を作成し、必要なパスレコード（例: `BezierKnotRecord`）を設定して、レイヤーのリソースコレクションに添付します。

**Q: Can I convert the edited PSD directly to PNG without opening Photoshop?**  
A: はい。PSD を保存した後、`Image.load()` で再度読み込み、`im.save("output.png")` と PNG フォーマットを指定すれば変換できます。

**Q: Is there a way to automate this in a CI/CD pipeline?**  
A: もちろんです。純粋な Java プロセスなので、Maven/Gradle ビルド、Docker コンテナ、または Java をサポートする任意の CI システムに組み込めます。

**Q: What versions of Aspose.PSD are compatible with Java 11+?**  
A: 最近のリリース（2024‑2025）すべてが Java 8 以上、特に Java 11、17、その他の LTS バージョンをサポートしています。

**Q: Do I need a license for development builds?**  
A: 開発・テスト用途には無料評価ライセンスで十分です。商用デプロイには製品ライセンスが必要です。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

---