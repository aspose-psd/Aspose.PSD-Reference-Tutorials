---
date: 2026-03-28
description: Aspose.PSD for Java を使用して新しい PSD レイヤーを作成し、その作成日時を管理する方法を学びます。このステップバイステップガイドでは、レイヤーの読み込み、読み取り、検証、追加について説明します。
linktitle: Create New PSD Layer and Manage Creation DateTime in Java
second_title: Aspose.PSD Java API
title: Javaで新しいPSDレイヤーを作成し、作成日時を管理する
url: /ja/java/psd-image-modification-conversion/manage-layer-creation-datetime-psd/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Javaで新しいPSDレイヤーを作成し、作成日時を管理する

## はじめに
プログラムでPhotoshop（PSD）ファイルを扱う際、**新しいPSDレイヤー**オブジェクトを作成し、その作成タイムスタンプを追跡できることは大きな変化をもたらします。デザイン資産のバージョン管理システムを構築したり、バッチ編集を自動化したり、共同プロジェクトの監査ログが必要だったりする場合でも、レイヤーの作成日を読み書きできれば、すべての変更の出所を完全に把握できます。このチュートリアルでは、Aspose.PSD for Java を使用して、PSD の読み込み、レイヤーの作成日時取得、検証、そして新しい調整レイヤーの追加までの一連の手順を解説します。

## クイック回答
- **JavaでPSDファイルを扱うライブラリは？** Aspose.PSD for Java  
- **レイヤーの作成日時を取得できるか？** はい、`layer.getLayerCreationDateTime()` を使用します  
- **新しい調整レイヤーを追加できるか？** もちろんです – `im.addLevelsAdjustmentLayer()` で作成できます  
- **本番環境でライセンスは必要か？** トライアル以外のデプロイには商用ライセンスが必要です  
- **対応しているJavaバージョンは？** JDK 8 以降  

## 「新しいPSDレイヤーを作成する」とは？
新しいPSDレイヤーを作成するとは、プログラム上で調整レイヤー、テキストレイヤー、ピクセルレイヤーなどの新規レイヤーオブジェクトを既存のPSDドキュメントに挿入することを指します。この操作により、Photoshop を手動で開かずに画像を拡張・変更できます。

## なぜレイヤー作成日時を管理するのか？
各レイヤーの作成日時を追跡することで、以下のような利点があります：
- **リビジョンの監査** – レイヤーが追加された正確な時刻を把握できます。  
- **チーム間での資産同期** – タイムスタンプを比較して整合性を保てます。  
- **時間ベースのルールに基づくワークフローの自動化**（例：1か月以上前に作成されたレイヤーを非表示にする）  

## 前提条件
作業を始める前に、以下を用意してください：

1. **Java Development Kit (JDK)** – バージョン 8 以上。  
2. **IDE** – IntelliJ IDEA、Eclipse、NetBeans、またはお好みのエディタ。  
3. **Aspose.PSD for Java** – インストール用に[こちらからダウンロード](https://releases.aspose.com/psd/java/)できます。  
4. **基本的なJava知識** – Java が初めてでも大丈夫です。コードはすべてコメント付きです。

すべて揃いましたか？素晴らしい！さっそくコーディングに入りましょう。

## パッケージのインポート
まず、必要な Aspose.PSD クラスと Java ユーティリティをインポートします。これらのインポートにより、画像処理、レイヤー操作、日付フォーマットが利用可能になります。

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

## 手順 1: ドキュメントディレクトリの設定
作業対象の PSD が格納されているフォルダを指定します。プレースホルダーはご自身の環境の絶対パスに置き換えてください。

```java
String dataDir = "Your Document Directory";
```

## 手順 2: PSD ファイルの読み込み
対象ファイルを読み込んで `PsdImage` インスタンスを作成します。このオブジェクトがすべてのレイヤー操作のエントリーポイントとなります。

```java
String sourceName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceName);
```

## 手順 3: レイヤーとその作成日時へのアクセス
最初のレイヤー（インデックス 0）を取得し、作成タイムスタンプを取得します。取得した日時は後で比較やログに使用します。

```java
Layer layer = im.getLayers()[0];
Date creationDateTime = layer.getLayerCreationDateTime();
```

## 手順 4: 作成日時のフォーマット
生の `Date` オブジェクトを人間が読みやすい文字列に変換します。別の形式が好みの場合はパターンを調整してください。

```java
DateFormat dateFormat = new SimpleDateFormat("yyyy/MM/dd HH:mm:ss");
```

## 手順 5: 作成日時の検証
デモンストレーションとして、取得した日時を期待値と比較します。実際のプロジェクトではデータベースや設定ファイルと照合することが考えられます。

```java
Date expectedDateTime = new Date("2018/7/17 8:57:24");
Assert.areEqual(expectedDateTime, creationDateTime);
```

## 手順 6: 新しいレイヤーの作成
ここで実際に **新しいPSDレイヤー** オブジェクトを作成します。例として Levels 調整レイヤーを追加し、元のピクセルを変更せずにトーン範囲を調整できるようにします。

```java
Date now = new Date();
Layer createdLayer = im.addLevelsAdjustmentLayer();
```

> **プロのコツ:** `now` 変数はレイヤーを追加した瞬間を保持します。必要に応じてメタデータとして保存すれば、カスタムタイムスタンプとして利用可能です。

## よくある問題と解決策
| 問題 | 発生原因 | 対策 |
|------|----------|------|
| `layer.getLayerCreationDateTime()` で `NullPointerException` が発生 | PSD にレイヤーが無い、またはインデックスが範囲外 | `im.getLayers().length > 0` を確認してからアクセス |
| 検証時に日付が一致しない | `Date` コンストラクタがロケール依存で文字列を解析 | 信頼性の高い `SimpleDateFormat.parse("2018/07/17 08:57:24")` を使用 |
| Photoshop で新しいレイヤーが表示されない | 調整レイヤーがデフォルトで非表示になる | 作成後に `createdLayer.setVisible(true);` を呼び出す |

## 結論
これで **新しいPSDレイヤー** オブジェクトの作成、作成日時の取得・検証、調整レイヤーの追加方法が分かりました。すべて Aspose.PSD for Java を使用しています。この機能により、Java ベースの画像処理パイプラインで高度な自動化、監査ログ、共同作業が可能になります。

本チュートリアルが役立ったなら、レイヤーの結合、フィルター適用、別フォーマットへのエクスポートなど、他の Aspose.PSD 機能もぜひ試してみてください。可能性は無限です！

## FAQ
### Aspose.PSD とは？
Aspose.PSD は、プログラムから Photoshop（PSD）ファイルを操作するための強力なライブラリです。

### Aspose.PSD は無料で使えるか？
はい！[こちら](https://releases.aspose.com/)から無料トライアルを開始できます。

### 長期利用にはライセンスが必要か？
はい、利用開始後は[こちら](https://purchase.aspose.com/buy)からライセンスを取得してください。

### Aspose.PSD の詳細情報はどこで得られるか？
詳しいガイドや API リファレンスは[ドキュメント](https://reference.aspose.com/psd/java/)をご覧ください。

### Aspose.PSD に関するサポートはどこで受けられるか？
コミュニティ支援は[サポートフォーラム](https://forum.aspose.com/c/psd/34)で受けられます。

---

**最終更新日:** 2026-03-28  
**テスト環境:** Aspose.PSD for Java 24.10  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}