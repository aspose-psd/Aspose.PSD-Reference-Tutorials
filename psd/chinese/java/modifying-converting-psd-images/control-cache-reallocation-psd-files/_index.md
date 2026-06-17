---
date: 2026-03-13
description: 学习如何使用 Aspose.PSD for Java 创建 PSD 图像 Java 项目，同时管理缓存重新分配。高效优化内存和磁盘使用。
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: 创建 PSD 图像 Java – 控制缓存重新分配
url: /zh/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

 as is.

Also ensure markdown formatting preserved.

Let's craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 PSD 文件中控制缓存重新分配

## Introduction
如果您需要高效地 **create PSD image java** 项目，控制缓存重新分配是必不可少的。在以编程方式处理图像和 Photoshop 文件时，效率是关键因素。Aspose.PSD for Java 提供了强大的功能，能够无缝管理和操作 PSD 文件。优化性能的基本方面之一就是控制缓存重新分配。缓存管理有助于在内存和磁盘使用之间保持平衡，确保您的应用程序平稳运行，不会出现意外崩溃或减速。

## Quick Answers
- **缓存重新分配的作用是什么？** 它在处理大型 PSD 文件时平衡内存和磁盘使用。  
- **哪种缓存类型最适合大图像？** `CacheOnDiskOnly` 通过将缓存存储在磁盘上来保持内存空闲。  
- **我可以分配多少磁盘空间？** 最多 1 GB（或使用 `setMaxDiskSpaceForCache` 设置的任何大小）。  
- **使用这些功能是否需要许可证？** 许可证可移除试用限制；请参阅 Aspose 购买页面。  
- **我可以在运行时监控缓存使用情况吗？** 可以，使用 `Cache.getAllocatedDiskBytesCount()` 和 `Cache.getAllocatedMemoryBytesCount()`。

## Why Control Cache Reallocation?
在处理高分辨率或多图层文件的 **create PSD image java** 应用程序中，管理缓存至关重要。适当的缓存设置可以防止内存不足错误，减少 GC 暂停，并为服务器或桌面应用程序提供可预测的性能。

## Prerequisites
在进入编码部分之前，您需要确保以下几点，以便一切顺利运行：
1. **Java Development Kit (JDK)**：确保您的机器上已安装 JDK。您可以从 [Oracle 的网站](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) 下载。  
2. **Aspose.PSD for Java**：您需要下载 Aspose.PSD 库。您可以在 [此处](https://releases.aspose.com/psd/java/) 找到最新版本。  
3. **IDE Setup**：使用 IntelliJ IDEA 或 Eclipse 等集成开发环境（IDE）可以更轻松地管理代码。  
4. **Java 基础**：熟悉 Java 编程有助于更好地理解概念和代码片段。  
5. **Aspose 许可证（可选）**：如果您希望移除水印并获得完整功能，请考虑在 [此处](https://purchase.aspose.com/buy) 购买许可证，或在 [此处](https://releases.aspose.com/) 试用免费版。

## Import Packages
在开始编写代码之前，让我们确保已导入必要的包。下面是您在 Java 文件开头需要包含的简要列表：
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
下面是一个逐步演练，将缓存配置直接关联到 Java 中创建 PSD 图像的过程。

### Step 1: Setting Up Your Data Directory
首先，您需要设置一个目录，用于存放缓存文件。这对于有效管理缓存至关重要。
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`：定义文档缓存的目录。  
- `Cache.setCacheFolder(dataDir)`：此方法将缓存文件夹设置为指定目录。Aspose 创建的任何缓存现在都会存储在此处，而不是默认的临时目录。

### Step 2: Configuring Cache To Disk
接下来，我们将指定仅在磁盘上存储缓存。如果您的应用程序使用大文件并希望确保内存保持空闲，这尤其有用。
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`：此选项确保缓存不保存在内存中，有助于在处理大型 PSD 文件时避免占用过多 RAM。

### Step 3: Setting Maximum Disk and Memory Cache Size
现在，让我们限制缓存大小。无限制的缓存可能导致性能问题，这一点至关重要。
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`：为磁盘缓存设置 1 GB 的上限。您可以根据需要调整此大小。  
- `Cache.setMaxMemoryForCache(1073741824)`：同样，这限制了内存缓存，确保您的应用程序不会使用过多内存。

### Step 4: Manage Cache Reallocation Strategy
管理缓存重新分配方式对于保持性能至关重要。以下是设置方法。
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`：设置为 `false` 时，允许 Aspose 更灵活地管理缓存重新分配，从而提升性能。

### Step 5: Check Allocated Cache Size
此步骤用于监控当前在内存或磁盘上为缓存分配的字节数。让我们实现它：
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`：存储磁盘上已分配的字节数。  
- `long l2`：存储内存中已分配的字节数。  

您可以随时检查这些值，以确保应用程序按预期管理内存和磁盘使用。

### Step 6: Creating a PSD Image
现在缓存配置已就绪，让我们创建一个简单的 PSD 图像。
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`：此对象允许您在创建 Photoshop 图像时指定选项。  
- `Color[] color`：包含将在图像调色板中使用的颜色的数组。

### Step 7: Saving Pixel Data to the Image
现在，让我们为图像填充像素数据并保存。
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`：这是一个颜色对象数组，此处我们用白色像素填充。  
- `image.savePixels(image.getBounds(), pixels)`：此方法将像素数据保存到图像中，并使用我们定义的颜色更新图像。

### Step 8: Monitoring Allocated Cache After Image Creation
创建图像后，最好再次检查为缓存分配的字节数。
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`：捕获图像创建后磁盘上的当前分配。  
- `long memoryBytes`：捕获内存中的当前分配。  

此步骤将帮助您了解操作后缓存的消耗情况。

### Step 9: Check for Proper Disposal
最后，确保所有 Aspose.PSD 对象已正确释放，以避免内存泄漏，这一点至关重要。
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` 和 `l2`：这些变量可帮助您检查最终分配情况。如果它们不为零，说明有对象未被正确释放。

## Common Issues and Solutions
- **未创建缓存文件夹** – 确认应用程序对您传递给 `Cache.setCacheFolder` 的路径具有写入权限。  
- **内存不足错误** – 再次确认在加载大型 PSD 文件之前已应用 `Cache.setCacheType(CacheType.CacheOnDiskOnly)`。  
- **意外的缓存大小** – 在每个主要操作后使用 `Cache.getAllocated*BytesCount()` 方法来跟踪增长。

## Frequently Asked Questions

**Q: 什么是 Aspose.PSD？**  
A: Aspose.PSD 是面向 .NET 和 Java 开发者的库，可编程地创建、操作和转换 Photoshop（PSD）文件。

**Q: 如何检查已分配的缓存大小？**  
A: 使用 `Cache.getAllocatedDiskBytesCount()` 和 `Cache.getAllocatedMemoryBytesCount()` 等方法来监控当前缓存使用情况。

**Q: 我可以为缓存设置自定义目录吗？**  
A: 可以，使用 `Cache.setCacheFolder("Your Directory Path")` 可以指定不同的目录。

**Q: Aspose.PSD 免费使用吗？**  
A: Aspose.PSD 是付费库，但您可以在其 [website](https://releases.aspose.com/) 上获取免费试用版。

**Q: 如果我不释放对象会怎样？**  
A: 未释放对象会导致内存泄漏，使您的应用程序使用的资源超出必要范围。

## Conclusion
在 **create PSD image java** 应用程序中控制缓存重新分配可以显著提升性能。按照上述步骤操作，您将能够高效管理缓存，降低内存消耗，并使用 Aspose.PSD for Java 生成高质量的 PSD 文件。运用这些技术，您的项目将运行得更顺畅、可扩展性更好。

---

**最后更新：** 2026-03-13  
**测试环境：** Aspose.PSD for Java (latest release)  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}