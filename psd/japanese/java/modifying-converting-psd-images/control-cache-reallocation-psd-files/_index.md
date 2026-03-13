---
date: 2026-03-13
description: Aspose.PSD for Java を使用してキャッシュ再割り当てを管理しながら、PSD 画像の Java プロジェクトの作成方法を学びましょう。メモリとディスクの使用量を効率的に最適化します。
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: JavaでPSD画像を作成 – キャッシュ再割り当ての制御
url: /ja/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

. We'll translate.

...

Continue.

We need to translate all bullet points and sentences.

Also note that there are placeholders like **??** but we will translate the original English.

Let's rewrite translation.

Make sure to keep markdown formatting.

Proceed.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD ファイルにおけるキャッシュ再割り当ての制御

## Introduction
**create PSD image java** プロジェクトを効率的に作成する必要がある場合、キャッシュ再割り当ての制御は不可欠です。画像や Photoshop ファイルをプログラムで扱う際、効率性は重要な要素です。Aspose.PSD for Java は、PSD ファイルをシームレスに管理・操作するための強力な機能を提供します。パフォーマンス最適化の基本的な側面のひとつがキャッシュ再割り当ての制御です。キャッシュ管理はメモリとディスク使用量のバランスを保ち、アプリケーションが予期せぬクラッシュや遅延なくスムーズに動作するよう支援します。 

## Quick Answers
- **What does cache reallocation do?** 大きな PSD ファイルを処理する際に、メモリとディスクの使用量のバランスを取ります。  
- **Which cache type is best for large images?** `CacheOnDiskOnly` はキャッシュをディスクに保存することでメモリを空けます。  
- **How much disk space can I allocate?** 最大 1 GB（または `setMaxDiskSpaceForCache` で設定した任意のサイズ）です。  
- **Do I need a license to use these features?** ライセンスを取得すると試用版の制限が解除されます。詳細は Aspose の購入ページをご覧ください。  
- **Can I monitor cache usage at runtime?** はい、`Cache.getAllocatedDiskBytesCount()` と `Cache.getAllocatedMemoryBytesCount()` を使用します。

## Why Control Cache Reallocation?
**create PSD image java** アプリケーションで高解像度やマルチレイヤーのファイルを扱う場合、キャッシュの管理は極めて重要です。適切なキャッシュ設定により、メモリ不足エラーを防止し、GC の一時停止を減らし、サーバーやデスクトップアプリで予測可能なパフォーマンスを実現できます。

## Prerequisites
コーディングに入る前に、スムーズに実行できるよう以下の項目を確認してください：
1. Java Development Kit (JDK): マシンに JDK がインストールされていることを確認してください。ダウンロードは [Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) から可能です。  
2. Aspose.PSD for Java: Aspose.PSD ライブラリをダウンロードしてください。最新リリースは [こちら](https://releases.aspose.com/psd/java/) にあります。  
3. IDE Setup: IntelliJ IDEA や Eclipse などの統合開発環境 (IDE) を使用すると、コード管理が容易になります。  
4. Basic Understanding of Java: Java プログラミングの基礎知識があると、概念やコードスニペットが理解しやすくなります。  
5. Aspose License (Optional): ウォーターマークを除去し、フル機能を利用したい場合は、[こちら](https://purchase.aspose.com/buy) でライセンス購入、または無料トライアルを [こちら](https://releases.aspose.com/) でお試しください。

## Import Packages
コードを書き始める前に、必要なパッケージがインポートされていることを確認しましょう。以下は Java ファイルの冒頭でインクルードすべき項目の簡易リストです：
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

## How to Create PSD Image Java with Cache Control
以下は、キャッシュ設定を直接 PSD 画像作成プロセスに結び付けるステップバイステップの手順です。

### Step 1: Setting Up Your Data Directory
まず最初に、キャッシュファイルを保存したいディレクトリを設定する必要があります。キャッシュを効果的に管理するために必須です。
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: ドキュメントキャッシュ用ディレクトリを定義します。  
- `Cache.setCacheFolder(dataDir)`: このメソッドはキャッシュフォルダーを指定したディレクトリに設定します。Aspose が作成するすべてのキャッシュは、デフォルトの一時ディレクトリではなくここに保存されます。

### Step 2: Configuring Cache To Disk
次に、キャッシュをディスクのみに保存するよう指定します。大容量ファイルを扱うアプリケーションで、メモリを確保したい場合に特に有用です。
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: このオプションによりキャッシュがメモリに保持されず、ディスクのみで管理されます。大きな PSD ファイルを扱う際に RAM の消費を抑えるのに役立ちます。

### Step 3: Setting Maximum Disk and Memory Cache Size
続いてキャッシュサイズに上限を設定します。無制限のキャッシュはパフォーマンス問題を引き起こす可能性があるため、重要なステップです。
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: ディスク上のキャッシュ上限を 1 GB に設定します。必要に応じてサイズは調整可能です。  
- `Cache.setMaxMemoryForCache(1073741824)`: 同様に、メモリ上のキャッシュ上限を設定し、過剰なメモリ使用を防ぎます。

### Step 4: Manage Cache Reallocation Strategy
キャッシュの再割り当て方法を管理することは、パフォーマンス維持に不可欠です。設定方法は以下の通りです。
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: `false` に設定すると、Aspose がキャッシュ再割り当てをより柔軟に管理でき、パフォーマンス向上につながります。

### Step 5: Check Allocated Cache Size
現在メモリまたはディスクに割り当てられているバイト数を監視します。以下のコードで実装してください：
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: ディスク上に割り当てられたバイト数を格納します。  
- `long l2`: メモリ上に割り当てられたバイト数を格納します。  
これらの値は随時確認でき、アプリケーションが期待通りにメモリとディスクを管理しているかを判断できます。

### Step 6: Creating a PSD Image
キャッシュ設定が完了したので、シンプルな PSD 画像を作成します。
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Photoshop 画像作成時のオプションを指定できるオブジェクトです。  
- `Color[] color`: 画像パレットで使用するカラーを格納する配列です。

### Step 7: Saving Pixel Data to the Image
画像にピクセルデータを設定し、保存します。
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: カラーオブジェクトの配列です。ここでは白色ピクセルで埋めています。  
- `image.savePixels(image.getBounds(), pixels)`: ピクセルデータを画像に保存するメソッドです。定義したカラーで画像が更新されます。

### Step 8: Monitoring Allocated Cache After Image Creation
画像作成後、再度キャッシュの割り当てバイト数を確認することが推奨されます。
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: 画像作成後のディスク上の現在の割り当て量を取得します。  
- `long memoryBytes`: メモリ上の現在の割り当て量を取得します。  
このステップにより、操作後にどれだけキャッシュが消費されたかを把握できます。

### Step 9: Check for Proper Disposal
最後に、すべての Aspose.PSD オブジェクトが適切に破棄されているか確認し、メモリリークを防止します。
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` と `l2`: 最終的な割り当て量をチェックするための変数です。ゼロでない場合は、いくつかのオブジェクトが正しく破棄されていないことを示します。

## Common Issues and Solutions
- **Cache folder not created** – `Cache.setCacheFolder` に渡したパスに対して、アプリケーションが書き込み権限を持っているか確認してください。  
- **Out‑of‑memory errors** – 大きな PSD ファイルを読み込む前に、`Cache.setCacheType(CacheType.CacheOnDiskOnly)` が適用されていることを再確認してください。  
- **Unexpected cache size** – 各主要操作の後に `Cache.getAllocated*BytesCount()` メソッドを使用して、キャッシュの増減を追跡してください。

## Frequently Asked Questions

**Q: What is Aspose.PSD?**  
A: Aspose.PSD は、.NET および Java 開発者が Photoshop (PSD) ファイルをプログラムで作成、操作、変換できるライブラリです。

**Q: How do I check allocated cache size?**  
A: `Cache.getAllocatedDiskBytesCount()` と `Cache.getAllocatedMemoryBytesCount()` などのメソッドを使用して、現在のキャッシュ使用量を監視します。

**Q: Can I set a custom directory for cache?**  
A: はい、`Cache.setCacheFolder("Your Directory Path")` を使用して別のディレクトリを指定できます。

**Q: Is Aspose.PSD free to use?**  
A: Aspose.PSD は有料ライブラリですが、[website](https://releases.aspose.com/) で提供されている無料トライアルから始めることができます。

**Q: What happens if I don’t dispose of objects?**  
A: オブジェクトを破棄しないとメモリリークが発生し、アプリケーションが不要なリソースを消費し続けます。

## Conclusion
**create PSD image java** アプリケーションでキャッシュ再割り当てを制御することは、パフォーマンスに大きな差をもたらします。上記の手順に従うことで、キャッシュを効率的に管理し、メモリ消費を最小限に抑えつつ、Aspose.PSD for Java で高品質な PSD ファイルを生成できます。これらのテクニックを活用すれば、プロジェクトはよりスムーズに動作し、スケーラビリティも向上します。

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}