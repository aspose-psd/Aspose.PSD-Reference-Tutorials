---
date: 2025-12-25
description: 了解如何使用 Aspose.PSD for Java 在支持中断监控的情况下将 PSD 转换为 PNG，包括 Java 线程中断示例以及保存
  PSD 为 PNG 的技巧。
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: 如何在 Aspose.PSD for Java 中使用中断监视器将 PSD 转换为 PNG
url: /zh/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 的中断监视器将 PSD 转换为 PNG

## 介绍

如果您需要在保持对长时间运行的图像转换的完整控制的同时**convert PSD to PNG**，Aspose.PSD for Java 的 Interrupt Monitor 正是您一直在寻找的工具。在本教程中，我们将演示一个真实的**java thread interrupt example**，让您能够在转换过程中途停止它，从而灵活地管理资源、强制超时或响应用户取消。

## 快速回答
- **What does the Interrupt Monitor do?** 它允许您安全地发出信号以停止正在进行的图像转换。  
- **Can I convert PSD to PNG with it?** 是的——该监视器适用于任何保存操作，包括 PNG。  
- **Is a separate thread required?** 通常您会在单独的线程中运行转换，以便能够中断它。  
- **Which Aspose.PSD version is needed?** 任何包含 `com.aspose.psd.multithreading.InterruptMonitor` 的近期版本。  
- **Do I need a license for production?** 是的，非试用使用需要有效的 Aspose.PSD 许可证。

## 什么是使用中断监视器的“convert PSD to PNG”？

将大型 Photoshop 文档（PSD/PSB）转换为 PNG 图像可能会占用大量 CPU。通过将 **Interrupt Monitor** 附加到转换工作线程，您可以编程方式中止该过程——这对于 Web 服务、批处理作业或用户可能取消操作的 UI 应用程序非常适用。

## 为什么使用中断监视器？

- **Responsive UI:** 防止在处理大文件时应用程序冻结。  
- **Resource Management:** 停止超出时间或内存预算的转换。  
- **Error Handling:** 当中断发生时，优雅地清理部分输出文件。

## 前提条件

- Java 开发环境（JDK 8 或更高）。  
- Aspose.PSD for Java 库 – 在 **[here](https://releases.aspose.com/psd/java/)** 下载。  
- 包含您要处理的 PSD/PSB 文件的文件夹。

## 导入包

首先导入所需的类。这将为您提供图像选项、中断监视器和线程工具的访问权限。

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## 步骤指南

### 步骤 1：设置文档目录

```java
String dataDir = "Your Document Directory";
```

将 `"Your Document Directory"` 替换为 PSD 文件所在的绝对路径。

### 步骤 2：定义图像选项和输出路径

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

这里我们使用 `PngOptions` **save PSD as PNG**。根据需要调整文件名。

### 步骤 3：初始化 Interrupt Monitor 和 SaveImageWorker

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

`InterruptMonitor` 实例稍后将用于停止转换。`SaveImageWorker` 将监视器与转换任务关联。

### 步骤 4：在单独线程中启动图像转换

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

我们在后台线程上启动转换，以便主线程保持响应。`Thread.sleep(3000)` 调用模拟超时情景。

### 步骤 5：中断进程（Java 线程中断示例）

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

调用 `monitor.interrupt()` 会触发 **how to interrupt monitor** 逻辑。中断后我们会清理任何部分写入的 PNG 文件。

## 常见问题及解决方案

| Issue | Reason | Fix |
|-------|--------|-----|
| 转换永不停止 | 监视器未链接到工作线程 | 确保 `SaveImageWorker` 接收相同的 `InterruptMonitor` 实例。 |
| 中断后输出文件仍然存在 | 清理代码未执行 | 验证 `finally` 块已运行且文件路径正确。 |
| `OutOfMemoryError` on large PSB files | 未使用流式选项 | 使用带有启用内存高效加载的 `LoadOptions` 的 `PsdImage`。 |

## 常见问题解答

### Q1：Aspose.PSD for Java 中的 Interrupt Monitor 是什么？

A1：Interrupt Monitor 让开发者 **manage and interrupt image conversion processes**，为您提供对长时间运行任务的细粒度控制。

### Q2：如何获取 Aspose.PSD for Java 库？

A2：您可以在 **[here](https://releases.aspose.com/psd/java/)** 下载 Aspose.PSD for Java 库。

### Q3：Aspose.PSD for Java 是否提供免费试用？

A3：是的，您可以在 **[here](https://releases.aspose.com/)** 试用 Aspose.PSD 的免费版。

### Q4：在哪里可以找到 Aspose.PSD for Java 的支持？

A4：请访问 Aspose.PSD for Java 支持论坛 **[here](https://forum.aspose.com/c/psd/34)**。

### Q5：如何购买 Aspose.PSD for Java 的许可证？

A5：您可以在 **[here](https://purchase.aspose.com/buy)** 购买 Aspose.PSD for Java 的许可证。

**最后更新：** 2025-12-25  
**测试环境：** Aspose.PSD 24.11 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}