---
title: PSD ファイル内のキャッシュの再割り当てを制御する
linktitle: PSD ファイル内のキャッシュの再割り当てを制御する
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して PSD ファイル内のキャッシュの再割り当てを管理します。メモリとファイル処理を効率的に最適化する方法を学習します。開発者に最適です。
weight: 22
url: /ja/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD ファイル内のキャッシュの再割り当てを制御する

## 導入
画像や Photoshop ファイルをプログラムで操作する場合、効率は重要な要素です。Aspose.PSD for Java は、PSD ファイルをシームレスに管理および操作するための強力な機能を提供します。パフォーマンスを最適化する基本的な側面の 1 つは、キャッシュの再割り当てを制御することです。キャッシュ管理は、メモリとディスクの使用量のバランスを維持し、予期しないクラッシュや速度低下を起こさずにアプリケーションがスムーズに実行されるようにするのに役立ちます。 
## 前提条件
コーディング部分に進む前に、すべてがスムーズに実行されるように確認する必要があることがいくつかあります。
1. Java開発キット（JDK）：マシンにJDKがインストールされていることを確認してください。ここからダウンロードできます。[Oracleのウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Aspose.PSDライブラリをダウンロードする必要があります。最新リリースは[ここ](https://releases.aspose.com/psd/java/).
3. IDE セットアップ: IntelliJ IDEA や Eclipse などの統合開発環境 (IDE) を使用すると、コードの管理が容易になります。
4. Java の基本的な理解: Java プログラミングに精通していると、概念やコード スニペットをより深く理解できるようになります。
5.  Asposeライセンス（オプション）：透かしを削除して完全な機能を利用したい場合は、ライセンスの購入を検討してください。[ここ](https://purchase.aspose.com/buy)または無料トライアルをお試しください[ここ](https://releases.aspose.com/).
## パッケージのインポート
コードを書き始める前に、必要なパッケージがインポートされていることを確認しましょう。以下は、Java ファイルの先頭に含める内容の簡単なリストです。
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```
## ステップ1: データディレクトリの設定
まず最初に、キャッシュ ファイルを保存するディレクトリを設定する必要があります。これは、キャッシュを効果的に管理するために不可欠です。
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- 文字列 dataDir: ドキュメント キャッシュのディレクトリを定義します。
- Cache.setCacheFolder(dataDir): このメソッドは、キャッシュ フォルダーを指定されたディレクトリに設定します。Aspose によって作成されたキャッシュは、デフォルトの一時ディレクトリではなく、ここに保存されるようになります。
## ステップ2: ディスクへのキャッシュの設定
次に、キャッシュをディスクにのみ保存することを指定します。これは、アプリケーションで大きなファイルを使用し、メモリを空けておきたい場合に特に便利です。
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): このオプションは、キャッシュがメモリに保持されないようにし、RAM をあまり消費せずに大きな PSD ファイルを処理するのに役立ちます。
## ステップ3: ディスクとメモリの最大キャッシュサイズの設定
次に、キャッシュ サイズを制限しましょう。無制限のキャッシュはパフォーマンスの問題を引き起こす可能性があるため、これは非常に重要です。
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1ギガバイト
Cache.setMaxMemoryForCache(1073741824); // 1ギガバイト
```

- Cache.setMaxDiskSpaceForCache(1073741824): ディスク上のキャッシュの制限を 1 GB に設定します。このサイズは必要に応じて調整できます。
- Cache.setMaxMemoryForCache(1073741824): 同様に、メモリ内キャッシュを制限し、アプリケーションが過剰なメモリを使用しないようにします。
## ステップ4: キャッシュ再割り当て戦略を管理する
キャッシュの再割り当て方法を管理することは、パフォーマンスを維持するために不可欠です。設定方法は次のとおりです。
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): false に設定すると、Aspose はキャッシュの再割り当てをより柔軟に管理できるようになり、パフォーマンスが向上します。
## ステップ5: 割り当てられたキャッシュサイズを確認する
このステップでは、メモリまたはディスク上のキャッシュに現在割り当てられているバイト数を監視します。これを実装してみましょう。
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: ディスクに割り当てられたバイト数を格納します。
- long l2: メモリに割り当てられたバイト数を格納します。 
これらの値をいつでも確認して、アプリケーションがメモリとディスクの使用量を期待どおりに管理していることを確認できます。
## ステップ6: PSDイメージの作成
キャッシュ構成が設定されたので、簡単な PSD イメージを作成しましょう。
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- PsdOptions オプション: このオブジェクトを使用すると、Photoshop 画像を作成するときにオプションを指定できます。
- 色[color: 画像パレットで使用される色を含む配列。
## ステップ7: ピクセルデータを画像に保存する
それでは、画像にピクセルデータを入力して保存しましょう。
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- 色[] ピクセル: これはカラー オブジェクトの配列です。ここでは、白いピクセルで塗りつぶしています。
- image.savePixels(image.getBounds(), Pixels): このメソッドは、ピクセル データを画像に保存します。定義した色で画像を更新します。
## ステップ8: イメージ作成後に割り当てられたキャッシュを監視する
イメージを作成した後、キャッシュに割り当てられているバイト数を再度確認することをお勧めします。
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes: イメージ作成後のディスク上の現在の割り当てをキャプチャします。
- long memoryBytes: メモリ内の現在の割り当てをキャプチャします。 
この手順は、操作後に消費されるキャッシュの量を判断するのに役立ちます。
## ステップ9: 適切な廃棄方法を確認する
最後に、メモリ リークを回避するために、すべての Aspose.PSD オブジェクトが適切に破棄されていることを確認することが重要です。
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 と l2: これらの変数は、最終的な割り当てを確認するのに役立ちます。ゼロでない場合は、一部のオブジェクトが適切に破棄されていないことを示します。
## 結論
Aspose.PSD for Java でキャッシュの再割り当てを制御すると、アプリケーションのパフォーマンスに大きな違いが生まれます。上記の手順に従うことで、キャッシュを効果的に管理し、メモリ使用量を最小限に抑え、美しい PSD ファイルを効率的に作成できます。これらのテクニックを活用して、アプリケーションが最適なパフォーマンスで成長するのを見てください。
## よくある質問
### Aspose.PSD とは何ですか?
Aspose.PSD は、.NET および Java 開発者が Photoshop (PSD) ファイルをプログラムで作成、操作、変換するためのライブラリです。
### 割り当てられたキャッシュ サイズを確認するにはどうすればよいですか?
次のような方法を使用する`Cache.getAllocatedDiskBytesCount()`そして`Cache.getAllocatedMemoryBytesCount()`現在のキャッシュの使用状況を監視します。
### キャッシュ用のカスタムディレクトリを設定できますか?
はい、別のディレクトリを指定するには、`Cache.setCacheFolder("Your Directory Path")`.
### Aspose.PSD は無料で使用できますか?
Aspose.PSDは有料のライブラリですが、無料トライアルで始めることもできます。[Webサイト](https://releases.aspose.com/).
### 物を処分しないとどうなりますか?
オブジェクトを破棄しないとメモリ リークが発生し、アプリケーションが必要以上に多くのリソースを使用する可能性があります。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
