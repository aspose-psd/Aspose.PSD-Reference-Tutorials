---
title: JavaでAIをPSDに変換
linktitle: JavaでAIをPSDに変換
second_title: Aspose.PSD Java API
description: 簡単なステップバイステップガイドを使用して、Aspose.PSD を使用して Java で AI を PSD に変換します。迅速かつシームレスなファイル変換を必要とする開発者に最適です。
type: docs
weight: 14
url: /ja/java/java-ai-to-image-format-conversion/convert-ai-to-psd/
---
## 導入
Java を使用して AI (Adobe Illustrator) ファイルを PSD (Adobe Photoshop) ファイルに変換したいと考えていますか?そうですね、あなたは正しい場所にいます！今日は、Java ライブラリ用の強力な Aspose.PSD を使用してこのタスクを実行する方法を検討します。このガイドでは、前提条件から詳細なステップバイステップの手順まで、知っておくべきことをすべて説明します。デザイン ファイルをシームレスに変換してみましょう。
## 前提条件
始める前に、いくつかの準備をしておく必要があります。
1. Java Development Kit (JDK): システムに JDK 8 以降がインストールされていることを確認してください。
2.  Aspose.PSD for Java: 次の場所から Aspose.PSD for Java ライブラリをダウンロードします。[ダウンロードページ](https://releases.aspose.com/psd/java/).
3. 統合開発環境 (IDE): Java コードを作成して実行するための IntelliJ IDEA や Eclipse などの IDE。
4. AI ファイル: 変換する Adobe Illustrator ファイル。
5. Aspose 一時ライセンス (オプション): 制限なしで全機能を使用するには、[仮免許](https://purchase.aspose.com/temporary-license/).
## パッケージのインポート
まず、必要なパッケージをインポートしてプロジェクトをセットアップしましょう。 Aspose.PSD for Java をプロジェクトのクラスパスに含める必要があります。その方法は次のとおりです。
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.imageoptions.PsdOptions;
```
または、次の場所から JAR ファイルをダウンロードすることもできます。[Java 用 Aspose.PSD ダウンロード ページ](https://releases.aspose.com/psd/java/)それをプロジェクトに手動で追加します。
プロセスをシンプルで管理しやすいステップに分割してみましょう。
## ステップ 1: プロジェクトのセットアップ
まず、好みの IDE でプロジェクトをセットアップします。
### 新しいプロジェクトを作成する
1. IDE を開き、新しい Java プロジェクトを作成します。
2. プロジェクトに「AItoPSDConverter」などの意味のある名前を付けます。
### Aspose.PSD ライブラリを追加
1. JAR ファイルをダウンロードした場合は、それをプロジェクトのビルド パスに追加します。
2.  Maven を使用している場合は、依存関係が正しく追加されていることを確認してください。`pom.xml`.
## ステップ 2: AI ファイルをロードする
プロジェクトが設定されたので、変換したい AI ファイルをロードしましょう。
```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "34992OStroke.ai";       
AiImage image = (AiImage) Image.load(sourceFileName);
```
## ステップ 3: PSD オプションの設定
次に、PSD 出力のオプションを設定する必要があります。
```java
PsdOptions options = new PsdOptions();
```
## ステップ 4: AI ファイルを PSD として保存する
AI ファイルがロードされ、オプションが設定されたら、PSD ファイルとして保存できるようになります。
```java
String outFileName = dataDir + "34992OStroke.psd";
image.save(outFileName, options);
```
## 結論
そして、それができました！ Aspose.PSD for Java を使用して AI ファイルを PSD ファイルに正常に変換しました。この強力なライブラリにより、Java アプリケーションでの複雑なファイル変換を簡単に処理できるようになります。経験豊富な開発者でも、初心者でも、このガイドは AI から PSD への変換機能をプロジェクトに簡単に統合するのに役立ちます。
## よくある質問
### Java 用 Aspose.PSD とは何ですか?
Aspose.PSD for Java は、開発者が Adobe Photoshop を必要とせずに、Java アプリケーション内で Photoshop ファイル (PSD および PSB) を作成、編集、変換できる堅牢なライブラリです。
### Aspose.PSD for Java を無料で使用できますか?
 Aspose.PSD for Java は無料トライアルを提供しており、以下からダウンロードできます。[無料お試しページ](https://releases.aspose.com/)。完全な機能については、[ライセンス](https://purchase.aspose.com/buy)が必要です。
### Aspose.PSD for Java の一時ライセンスを取得するにはどうすればよいですか?
一時ライセンスは以下から取得できます。[一時ライセンスのページ](https://purchase.aspose.com/temporary-license/).
### PSDファイルをAIファイルに戻すことは可能ですか?
現在、Aspose.PSD for Java は、PSD ファイルを AI ファイルに戻すことをサポートしていません。 PSD および PSB ファイルの処理に重点を置いています。
### 他の例やドキュメントはどこで入手できますか?
包括的なドキュメントと例は、[Aspose.PSD for Java ドキュメント ページ](https://reference.aspose.com/psd/java/).