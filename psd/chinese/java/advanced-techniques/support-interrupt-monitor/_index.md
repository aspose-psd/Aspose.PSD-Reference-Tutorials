---
date: 2026-06-08
description: 了解如何使用 Aspose.PSD for Java 将 PSD 保存为 PNG，并在需要时中断转换。高效管理图像工作流。
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: 中断监视器支持
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 如何在 Aspose.PSD for Java 中使用 Interrupt Monitor 将 PSD 保存为 PNG
url: /zh/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 的中断监视器将 PSD 保存为 PNG

## 介绍

如果您需要在保持对长时间运行的转换过程完全控制的同时 **将 PSD 保存为 PNG**，Aspose.PSD for Java 的中断监视器正好满足此需求。在本教程中，我们将演示如何设置监视器、将 PSD 文件转换为 PNG，以及在需要时安全地中止操作。您还将了解此功能在典型图像处理工作流中的位置以及为何它是构建稳健应用程序的必备工具。

## 快速答案
- **我可以中断 PSD 到 PNG 的转换吗？** 可以，使用 `InterruptMonitor` 可随时停止该过程。  
- **哪个方法用于将 PSD 保存为 PNG？** 调用 `save(outputPath, new PngOptions())`。  
- **生产环境需要许可证吗？** 需要商业许可证；提供免费试用版。  
- **支持哪些 Java 版本？** 完全支持 Java 8 及更高版本。  
- **库是线程安全的吗？** 转换可以在独立线程中运行；监视器能够安全地处理中断。

## 前置条件

在深入了解中断监视器的使用细节之前，请确保已具备以下前置条件：

- **Java 开发环境：** 在您的系统上搭建好 Java 开发环境。  
- **Aspose.PSD 库：** 获取 Aspose.PSD for Java 库。您可以在[此处](https://releases.aspose.com/psd/java/)下载。也可以访问 Aspose 主站[此处](https://releases.aspose.com/)。  
- **文档目录：** 为您的 PSD 文档准备一个指定目录。

## 导入包

在 Java 项目中导入必要的包，以确保能够使用 Aspose.PSD 的功能。

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

现在，让我们将示例代码拆解为一步步的指南，以在您的 Aspose.PSD for Java 项目中集成中断监视器。

## 如何使用中断监视器将 PSD 保存为 PNG？

`PsdImage` 表示已加载到内存中的 PSD 文档。  
`SaveImageWorker` 在单独的线程中执行图像转换。

使用 `new PsdImage("source.psd")` 加载 PSD 文件，将 `InterruptMonitor` 附加到 `SaveImageWorker`，然后调用 `save("output.png", new PngOptions())`。监视器会监控取消请求，并在毫秒级别内干净地中止转换，将控制权返回给您的应用程序。

### 步骤 1：设置文档目录

```java
String dataDir = "Your Document Directory";
```

请将 “Your Document Directory” 替换为实际存放 PSD 文档的路径。

### 步骤 2：定义图像选项和输出路径

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

指定图像选项、源 PSD 文件以及转换后图像的目标输出路径。

### 步骤 3：初始化中断监视器和 SaveImageWorker

`InterruptMonitor` 类监视正在运行的转换，并在调用 `requestInterrupt()` 时中断它。

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

创建 `InterruptMonitor` 和 `SaveImageWorker` 的实例，并将监视器链接到图像转换工作器。

### 步骤 4：启动图像转换线程

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

为图像转换过程启动新线程，并设置超时时间以预期可能的中断。

### 步骤 5：中断进程

调用 `monitor.requestInterrupt()` 即可向监视器发送中止正在进行的转换的信号。

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

使用 `InterruptMonitor` 中断图像转换过程并等待中断完成。最后，删除输出文件以进行清理。

## 为什么在 PSD 到 PNG 转换中使用中断监视器？

Aspose.PSD 支持 **30 多种输出格式**，包括 PNG、JPEG、BMP 和 TIFF，并且能够在不将整个文档加载到内存的情况下处理高达 **500 MB** 的文件。通过添加中断监视器，您可以减少 CPU 浪费，提高批处理流水线的响应速度，尤其是在转换超出预期时间限制时。

## 常见问题与解决方案

- **转换无限挂起：** 确保在调用 `save` 之前已 **附加** 监视器。  
- **中断后输出文件损坏：** 监视器会干净地中止；但在使用文件前请始终检查文件是否存在。  
- **线程安全问题：** 为每个转换启动独立线程；监视器仅影响其关联的工作器。

## 常见问答

**问 1：什么是 Aspose.PSD for Java 中的中断监视器？**  
答：中断监视器让开发者能够暂停或取消长时间运行的图像转换，从而实时控制资源使用。

**问 2：如何获取 Aspose.PSD for Java 库？**  
答：您可以在[此处](https://releases.aspose.com/psd/java/)下载 Aspose.PSD for Java 库。

**问 3：是否提供 Aspose.PSD for Java 的免费试用？**  
答：是的，您可以在[此处](https://releases.aspose.com/)体验免费试用。

**问 4：在哪里可以找到 Aspose.PSD for Java 的支持？**  
答：访问 Aspose.PSD for Java 支持论坛[此处](https://forum.aspose.com/c/psd/34)。

**问 5：如何购买 Aspose.PSD for Java 的许可证？**  
答：您可以在[此处](https://purchase.aspose.com/buy)购买 Aspose.PSD for Java 许可证。

**问 6：我可以并行将多个 PSD 文件转换为 PNG 吗？**  
答：可以，为每个文件启动单独线程，并为每个转换工作器附加独立的 `InterruptMonitor`。

**问 7：库在 PSD 到 PNG 转换过程中是否处理颜色配置文件？**  
答：当然；Aspose.PSD 会保留嵌入的 ICC 配置文件，并自动将其应用到输出的 PNG。

---

**最后更新：** 2026-06-08  
**测试环境：** Aspose.PSD 23.12 for Java  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相关教程

- [在 Aspose.PSD for Java 中将 PSD 保存为 PNG 并应用渲染投影阴影](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [使用 Aspose.PSD for Java 将 PSD 导出为 PNG 并添加新常规图层](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Java 中 PSD 文件的中断监视器支持](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}