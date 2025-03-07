---
title: 控制 PSD 文件中的缓存重新分配
linktitle: 控制 PSD 文件中的缓存重新分配
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD for Java 管理 PSD 文件中的缓存重新分配。了解如何有效优化内存和文件处理 - 非常适合开发人员。
weight: 22
url: /zh/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 控制 PSD 文件中的缓存重新分配

## 介绍
当以编程方式处理图像和 Photoshop 文件时，效率是一个关键因素。Aspose.PSD for Java 提供强大的功能来无缝管理和操作 PSD 文件。优化性能的基本方面之一是控制缓存重新分配。缓存管理有助于保持内存和磁盘使用之间的平衡，确保您的应用程序运行顺畅，不会出现意外崩溃或减速。 
## 先决条件
在进入编码部分之前，需要确保以下几点以确保一切顺利进行：
1. Java 开发工具包 (JDK)：确保您的机器上安装了 JDK。您可以从以下网址下载[Oracle 网站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java：您需要下载 Aspose.PSD 库。您可以找到最新版本[这里](https://releases.aspose.com/psd/java/).
3. IDE 设置：像 IntelliJ IDEA 或 Eclipse 这样的集成开发环境 (IDE) 将使您更轻松地管理代码。
4. 对 Java 的基本了解：熟悉 Java 编程将帮助您更好地理解概念和代码片段。
5.  Aspose 许可证（可选）：如果您希望删除水印并获得完整功能，请考虑购买许可证[这里](https://purchase.aspose.com/buy)或尝试免费试用[这里](https://releases.aspose.com/).
## 导入包
在开始编写代码之前，让我们确保已经导入了必要的包。下面是 Java 文件开头应包含的内容的简要列表：
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
## 步骤 1：设置数据目录
首先，您需要设置一个用于存储缓存文件的目录。这对于有效管理缓存至关重要。
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- 字符串 dataDir：定义文档缓存的目录。
- Cache.setCacheFolder(dataDir)：此方法将缓存文件夹设置为指定目录。Aspose 创建的任何缓存现在都将存储在此处，而不是默认的临时目录。
## 步骤 2：配置缓存到磁盘
接下来，我们将指定希望缓存仅存储在磁盘上。如果您的应用程序使用大文件并且您想确保内存保持可用，这将特别有用。
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly)：此选项可确保缓存不保存在内存中，这有利于处理大型 PSD 文件而不会消耗太多 RAM。
## 步骤 3：设置最大磁盘和内存缓存大小
现在，让我们限制缓存大小。这很关键，因为无限缓存可能会导致性能问题。
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1千兆字节
Cache.setMaxMemoryForCache(1073741824); // 1千兆字节
```

- Cache.setMaxDiskSpaceForCache(1073741824)：这将磁盘上的缓存限制设置为 1 GB。您可以根据需要调整此大小。
- Cache.setMaxMemoryForCache(1073741824)：同样，这会限制内存中的缓存，确保您的应用程序不会使用过多的内存。
## 步骤 4：管理缓存重新分配策略
管理缓存的重新分配方式对于保持性能至关重要。以下是设置方法。
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false)：设置为 false 时，这允许 Aspose 更灵活地管理缓存重新分配，从而提高性能。
## 步骤 5：检查分配的缓存大小
此步骤用于监视内存或磁盘中当前为缓存分配了多少字节。让我们来实现它：
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1：存储磁盘上分配的字节数。
- long l2：存储在内存中分配的字节数。 
您可以随时检查这些值以确保您的应用程序按预期管理内存和磁盘使用情况。
## 步骤6：创建PSD图像
现在我们已经设置了缓存配置，让我们创建一个简单的 PSD 图像。
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- PsdOptions 选项：此对象允许您在创建 Photoshop 图像时指定选项。
- 颜色[color：包含图像调色板中将使用的颜色的数组。
## 步骤 7：将像素数据保存到图像
现在，让我们用像素数据填充图像并保存它。
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- 颜色[] 像素：这是一个颜色对象数组。在这里，我们用白色像素填充它。
- image.savePixels(image.getBounds(), pixels): 此方法将像素数据保存到图像。它使用我们定义的颜色更新图像。
## 步骤 8：创建映像后监控分配的缓存
创建图像后，最好再次检查为缓存分配了多少字节。
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes：捕获映像创建后磁盘上的当前分配。
- long memoryBytes：捕获内存中的当前分配。 
此步骤将帮助您确定操作后消耗了多少缓存。
## 步骤 9：检查是否正确处置
最后，确保所有 Aspose.PSD 对象都得到正确处理以避免内存泄漏至关重要。
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 和 l2：这些变量将帮助您检查最终分配。如果它们不为零，则表示某些对象尚未得到妥善处理。
## 结论
控制 Aspose.PSD for Java 中的缓存重新分配可以显著提高应用程序的性能。通过遵循上述步骤，您可以有效地管理缓存，最大限度地减少内存使用，并高效地创建漂亮的 PSD 文件。采用这些技术，您的应用程序将以最佳性能蓬勃发展！
## 常见问题解答
### 什么是 Aspose.PSD？
Aspose.PSD 是一个供.NET 和 Java 开发人员以编程方式创建、操作和转换 Photoshop (PSD) 文件的库。
### 如何检查分配的缓存大小？
使用类似方法`Cache.getAllocatedDiskBytesCount()`和`Cache.getAllocatedMemoryBytesCount()`监视当前缓存使用情况。
### 我可以为缓存设置自定义目录吗？
是的，你可以使用以下命令指定其他目录`Cache.setCacheFolder("Your Directory Path")`.
### Aspose.PSD 可以免费使用吗？
Aspose.PSD 是一个付费库，但你可以先从其网站上的免费试用版开始。[网站](https://releases.aspose.com/).
### 如果我不处理物体会发生什么情况？
不处置对象可能会导致内存泄漏，从而导致应用程序使用比必要更多的资源。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
