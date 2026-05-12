---
date: 2026-02-22
description: Aspose.PSD for Java を使用してベクターマスクを作成し、ベクターマスク PSD を追加し、Vmsk リソースをプログラムで操作する方法を学びましょう。
linktitle: Create Vector Mask Java – Vmsk Resource in PSD Files
second_title: Aspose.PSD Java API
title: Javaでベクターマスクを作成 – PSDファイルのVmskリソース
url: /ja/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Create Vector Mask Java – Vmsk Resource in PSD Files

## Introduction
Photoshop（PSD）ファイル内に **ベクターマスク**（Vmsk）リソースを作成する必要がある場合、Aspose.PSD for Java を使えば、クリーンでプログラム的な方法で実現できます。デザイン自動化ツールを構築する場合でも、既存のグラフィックパイプラインにカスタムマスク機能を追加する場合でも、このチュートリアルでは、PSD の読み込み、Vmsk リソースの取得、プロパティの調整、結果の保存までの手順をすべて解説します。最後まで読めば、ベクターマスクの取り扱い、PSD から PNG への変換、追加のベクターデータでファイルを拡張する方法を **create vector mask java** のテクニックで習得できます。

## Quick Answers
- **Vmsk リソースとは何ですか？** PSD ファイル内に保存されているベクターマスクデータで、レイヤーの複雑なベクトル形状を定義します。  
- **どのライブラリがサポートしていますか？** Aspose.PSD for Java が Vmsk リソースのフル読み書きを提供します。  
- **ライセンスは必要ですか？** 無料トライアルがありますが、商用利用には有償ライセンスが必要です。  
- **編集した PSD を PNG に変換できますか？** はい。保存後に PSD を読み込み、同じ API で PNG にエクスポートできます。  
- **Maven のサポートはありますか？** もちろんです。Aspose.PSD は Maven 依存として追加できます（「aspose psd maven」キーワード参照）。

## What is a Vector Mask (Vmsk Resource)?
ベクターマスク（Vmsk）は、ピクセルベースではなくベジエ曲線とパスレコードを使用してレイヤー上の透明領域と不透明領域を定義するマスクです。ベクターベースなので、解像度を落とさずにスケーリングでき、高解像度グラフィックに最適です。

## Why Create a Vector Mask with Aspose.PSD?
- **Automation:** Photoshop を開かずにプログラムからマスクを追加・変更できます。  
- **Consistency:** 生成するすべての PSD が同じマスクルールに従うことを保証します。  
- **Cross‑platform:** Java が動作する OS ならどこでも利用可能です。  
- **Integration:** 他の Aspose API（例: PSD → PNG 変換）と組み合わせてエンドツーエンドのワークフローが構築できます。  
- **Scalability:** ベクターマスクはサイズに関係なく鮮明なままで、レスポンシブデザインに最適です。

## Why This Matters for Java Developers
**create vector mask java** のテクニックを使うことで、バックエンドサービス、CI パイプライン、デスクトップユーティリティに高度なグラフィックロジックを直接組み込めます。デザイナーが手作業でマスクを追加する必要がなくなり、コードだけでオンザフライに生成・調整できるため、時間短縮とヒューマンエラーの削減が実現します。

## Prerequisites
コードに入る前に、以下の環境が整っていることを確認してください。

### What You Need
- Java Development Kit (JDK): お使いのマシンに JDK がインストールされていることを確認してください。未インストールの場合は、[Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-downloads.html)からダウンロードできます。  
- Aspose.PSD for Java Library: PSD ファイル管理用の強力なライブラリです。[Aspose のリリースページ](https://releases.aspose.com/psd/java/)からダウンロードできます。購入前に試したい方は、[無料トライアル](https://releases.aspose.com/)も利用可能です。  
- An IDE: IntelliJ IDEA、Eclipse など、任意の Java IDE があれば本プロジェクトは実行できます。

### Setting Up Your Workspace
1. **Create a New Java Project** – お好みの IDE で新規プロジェクトを作成します。  
2. **Add the Aspose Library** – ダウンロードした Aspose JAR をプロジェクトのビルドパスに追加し、PSD 関連クラスにアクセスできるようにします。

環境が整ったら、実装に進みましょう。

## How to create vector mask in PSD files with Java
以下はステップバイステップのガイドです。コードブロックは元のチュートリアルと同一で、各ステップを分かりやすく説明するテキストを追加しています。

### Import Packages
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

これで準備完了です。次に各操作を順に見ていきます。

### Step 1: Load Your PSD File
最初に行うべきことは PSD ファイルのロードです。ここからマジックが始まります。

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` に PSD ファイルが格納されているディレクトリを設定します。  
- `sourceFileName` にはディレクトリと PSD ファイル名を結合した文字列を作成します。  
- 最後に `Image.load()` を使って PSD を `PsdImage` オブジェクトに読み込みます。

### Step 2: Retrieve the Vmsk Resource
PSD 画像をロードしたら、Vmsk リソースを取得します。

```java
VmskResource resource = getVmskResource(im);
```

- `getVmskResource()` メソッドを呼び出すことで、画像内の Vmsk リソースを検索・取得します。

### Step 3: Validate Vmsk Resource Properties
変更を加える前に、Vmsk リソースが期待通りの状態か検証することが重要です。

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- ここでは Vmsk リソースの各種プロパティをチェックしています。無効化、反転、リンク状態が正しく、パス数が期待通りであることを確認します。

### Step 4: Access Each Path and Validate
さらに深掘りして、Vmsk リソース内のパスを検証します。

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

### Step 5: Edit the Vmsk Resource
いよいよ変更パートです。必要に応じて Vmsk リソースのプロパティを調整できます。

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- このブロックでは Vmsk の各種フラグを `true` に設定し、マスクの挙動を制御しています。

### Step 6: Modify the Bezier Knot Points
ベジエノットはベクターパスの要です。ここでいくつかの値を変更します。

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- 特定の `BezierKnotRecord` パスにアクセスし、ポイントを変更してベクターマスクの形状を再構成します。

### Step 7: Save the Modified PSD File
すべての編集が完了したら、変更後の PSD を保存します。

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- エクスポート先の PSD パスを設定し、`im.save()` を呼び出して新しいファイルに書き込みます。

### Step 8: Clean Up Resources
最後に、リソースを適切に解放してメモリリークを防止します。

```java
im.dispose();
```

- 使用が終わったら必ずリソースを破棄する習慣をつけましょう。これによりアプリケーションのメモリ使用量を抑えられます。

## Common Issues and Solutions
| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **`VmskResource` not found** | PSD にベクターマスクレイヤーが含まれていません。 | ソース PSD にベクターマスクがあるか確認するか、Photoshop で手動で追加してください。 |
| **`ArrayIndexOutOfBoundsException` on path access** | 期待したパスレコード数と実際が異なるためです。 | `resource.getPaths().length` を確認し、インデックスの使用を調整してください。 |
| **License exception** | 有効な Aspose.PSD ライセンスなしで実行しています。 | `License license = new License(); license.setLicense("Aspose.PSD.lic");` でトライアルまたは購入済みライセンスを適用してください。 |
| **Memory leak** | 長時間実行するプロセスで画像が破棄されていません。 | `finally` ブロックで必ず `im.dispose()` を呼ぶか、サポートされていれば try‑with‑resources を使用してください。 |

## Frequently Asked Questions

**Q: How do I add a new vector mask to an existing layer?**  
A: `VmskResource` を作成し、必要なパスレコード（例: `BezierKnotRecord`）を設定して、レイヤーのリソースコレクションに追加します。

**Q: Can I convert the edited PSD directly to PNG without opening Photoshop?**  
A: はい。PSD を保存した後、`Image.load()` で再度読み込み、`im.save("output.png")` と PNG フォーマットを指定すれば変換できます。

**Q: Is there a way to automate this in a CI/CD pipeline?**  
A: もちろんです。純粋な Java プロセスなので、Maven/Gradle ビルド、Docker コンテナ、または Java をサポートする任意の CI システムに組み込めます。

**Q: What versions of Aspose.PSD are compatible with Java 11+?**  
A: 最近のリリース（2024‑2025 系）すべてが Java 8 以上、特に Java 11、17、その他の LTS バージョンをサポートしています。

**Q: Do I need a license for development builds?**  
A: 開発・テスト用には無料の評価ライセンスで問題ありません。商用デプロイ時は有償ライセンスが必要です。

---

**Last Updated:** 2026-02-22  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}