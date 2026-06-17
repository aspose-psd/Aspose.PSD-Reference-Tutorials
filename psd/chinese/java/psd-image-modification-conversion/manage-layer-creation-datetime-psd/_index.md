---
date: 2026-03-28
description: 了解如何使用 Aspose.PSD for Java 创建新的 PSD 图层并管理其创建日期时间。本分步指南涵盖加载、读取、验证和添加图层。
linktitle: Create New PSD Layer and Manage Creation DateTime in Java
second_title: Aspose.PSD Java API
title: 在 Java 中创建新 PSD 图层并管理创建日期时间
url: /zh/java/psd-image-modification-conversion/manage-layer-creation-datetime-psd/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 创建新的 PSD 图层并在 Java 中管理创建日期时间

## 介绍
当您以编程方式处理 Photoshop (PSD) 文件时，能够 **create new PSD layer** 对象并跟踪它们的创建时间戳是一个真正的游戏改变者。无论您是为设计资产构建版本控制系统、自动化批量编辑，还是仅仅需要为协作项目提供审计追踪，了解如何读取和设置图层创建日期都能让您维护每一次更改的完整来源。在本教程中，我们将使用 Aspose.PSD for Java 完整演示整个过程——从加载 PSD、获取图层的创建日期、验证它，到最终添加全新的调整图层。

## 快速回答
- **什么库在 Java 中处理 PSD 文件？** Aspose.PSD for Java  
- **我可以读取图层的创建日期吗？** Yes, using `layer.getLayerCreationDateTime()`  
- **可以添加新的调整图层吗？** Absolutely – `im.addLevelsAdjustmentLayer()` creates one  
- **生产使用需要许可证吗？** A commercial license is required for non‑trial deployments  
- **支持哪个 Java 版本？** JDK 8 or later  

## 什么是“create new PSD layer”？
创建新的 PSD 图层意味着以编程方式向现有 PSD 文档中插入一个全新的图层对象——例如调整图层、文字图层或像素图层。此操作使您无需手动打开 Photoshop 即可扩展或修改图像。

## 为什么管理图层创建 DateTime？
跟踪每个图层的创建 DateTime 可帮助您：
- **审计修订** – 确切了解图层何时被添加。  
- **同步资产** – 通过比较时间戳在团队之间同步。  
- **自动化工作流** – 依赖基于时间的规则（例如，隐藏超过一个月的图层）。  

## 前置条件
在开始之前，请确保您已准备好以下内容：

1. **Java Development Kit (JDK)** – 版本 8 或更高。  
2. **IDE** – IntelliJ IDEA、Eclipse、NetBeans，或您喜欢的任何编辑器。  
3. **Aspose.PSD for Java** – 您可以在此[下载](https://releases.aspose.com/psd/java/)进行安装。  
4. **Basic Java knowledge** – 如果您是 Java 新手，也不用担心；代码都有完整注释。

一切就绪？太棒了！让我们跳进有趣的编码部分。

## 导入包
首先，导入您需要的 Aspose.PSD 类和 Java 实用工具。这些导入为您提供图像处理、图层操作和日期格式化的访问权限。

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

## 步骤 1：设置文档目录
指定包含您要处理的 PSD 的文件夹。将占位符替换为您机器上的绝对路径。

```java
String dataDir = "Your Document Directory";
```

## 步骤 2：加载 PSD 文件
通过加载目标文件创建 `PsdImage` 实例。此对象是所有图层操作的入口点。

```java
String sourceName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceName);
```

## 步骤 3：访问图层及其创建日期
获取第一个图层（索引 0）并检索其创建时间戳。这是您稍后将比较或记录的日期。

```java
Layer layer = im.getLayers()[0];
Date creationDateTime = layer.getLayerCreationDateTime();
```

## 步骤 4：格式化创建日期
将原始 `Date` 对象转换为人类可读的字符串。如果您喜欢不同的格式，可调整模式。

```java
DateFormat dateFormat = new SimpleDateFormat("yyyy/MM/dd HH:mm:ss");
```

## 步骤 5：验证创建日期
为了演示，我们将检索的日期与预期值进行比较。在实际项目中，您可能会将其与数据库记录或配置文件进行比较。

```java
Date expectedDateTime = new Date("2018/7/17 8:57:24");
Assert.areEqual(expectedDateTime, creationDateTime);
```

## 步骤 6：创建新图层
现在我们实际 **create new PSD layer** 对象。在这里我们添加一个 Levels 调整图层，它允许您在不更改原始像素的情况下微调色调范围。

```java
Date now = new Date();
Layer createdLayer = im.addLevelsAdjustmentLayer();
```

> **专业提示：** `now` 变量捕获您添加图层的瞬间，如果需要自定义时间戳，您可以稍后将其存储为元数据。

## 常见问题及解决方案
| 问题 | 原因 | 解决方案 |
|------|------|----------|
| `NullPointerException` on `layer.getLayerCreationDateTime()` | PSD 没有图层或图层索引超出范围。 | 在访问之前验证 `im.getLayers().length > 0`。 |
| Date mismatch in validation | `Date` 构造函数以区域设置相关的方式解析字符串。 | 使用 `SimpleDateFormat.parse("2018/07/17 08:57:24")` 进行可靠解析。 |
| New layer not visible in Photoshop | 调整图层默认可能是隐藏的。 | 创建后调用 `createdLayer.setVisible(true);`。 |

## 结论
您现在已经了解如何 **create new PSD layer** 对象、读取它们的创建时间戳、验证这些时间戳，并添加调整图层——全部使用 Aspose.PSD for Java。此功能为任何基于 Java 的图像处理流水线打开了高级自动化、审计追踪和协作工作流的大门。

如果您喜欢本教程，请探索其他 Aspose.PSD 功能，如合并图层、应用滤镜或导出为不同格式。可能性是无限的！

## 常见问答
### 什么是 Aspose.PSD？
Aspose.PSD 是一个强大的库，可用于以编程方式处理 Photoshop (PSD) 文件。

### 我可以免费使用 Aspose.PSD 吗？
是的！您可以在此[免费试用](https://releases.aspose.com/)开始使用。

### 长期使用需要购买许可证吗？
是的，一旦准备就绪，您可以在此[购买许可证](https://purchase.aspose.com/buy)。

### 在哪里可以找到关于 Aspose.PSD 的更多信息？
您可以查看[文档](https://reference.aspose.com/psd/java/)获取详细指南和 API 参考。

### 如果在使用 Aspose.PSD 时遇到问题，我该如何获取支持？
随时访问[支持论坛](https://forum.aspose.com/c/psd/34)获取社区帮助。

---

**Last Updated:** 2026-03-28  
**Tested With:** Aspose.PSD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}