---
date: 2026-01-14
description: Tìm hiểu cách tạo lớp nét viền gradient và tùy chỉnh gradient cho nét
  viền trong các tệp PSD bằng Aspose.PSD cho Java qua hướng dẫn từng bước này.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: Cách tạo lớp viền gradient trong Java
url: /vi/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách tạo lớp viền gradient trong Java

## Introduction
Bạn đã bao giờ tự hỏi làm thế nào để **tạo lớp viền gradient** trong các tệp PSD của mình bằng Java? Bạn đang ở đúng nơi! Hôm nay chúng ta sẽ khám phá Aspose.PSD cho Java — một thư viện mạnh mẽ cho phép bạn thao tác các tệp PSD một cách dễ dàng. Dù bạn mới bắt đầu lập trình đồ họa hay muốn tinh chỉnh các thiết kế hiện có, hướng dẫn này sẽ hướng dẫn bạn từng bước thêm và tùy chỉnh gradient cho viền.

## Quick Answers
- **What is the primary goal?** Mục tiêu chính là gì? Tạo một lớp viền gradient trên tệp PSD.  
- **Which library is required?** Thư viện nào cần thiết? Aspose.PSD for Java.  
- **Do I need a license?** Tôi có cần giấy phép không? Có, cần một giấy phép hợp lệ (hoặc tạm thời) cho môi trường sản xuất.  
- **What Java version works?** Phiên bản Java nào hoạt động? Java 8 hoặc cao hơn.  
- **How long does implementation take?** Thời gian thực hiện khoảng bao lâu? Khoảng 10‑15 phút cho một viền gradient cơ bản.

## What is a Gradient Stroke Layer?
Lớp viền gradient là một đường viền vector bao quanh một hình dạng hoặc văn bản, chuyển đổi mượt mà giữa các màu. Sử dụng Aspose.PSD, bạn có thể định nghĩa chương trình các màu, độ trong suốt, góc và loại (tuyến tính, bán kính, v.v.) của viền.

## Why use Aspose.PSD for Java?
- **Full PSD support** – Hỗ trợ đầy đủ PSD – đọc, chỉnh sửa và ghi các tệp PSD mà không cần Photoshop.  
- **Rich effect API** – API hiệu ứng phong phú – truy cập viền, bóng, phát sáng và nhiều hiệu ứng lớp khác.  
- **Cross‑platform** – Đa nền tảng – hoạt động trên bất kỳ hệ điều hành nào hỗ trợ Java.  
- **No native dependencies** – Không phụ thuộc gốc – thuần Java, dễ tích hợp vào các pipeline CI.

## Prerequisites
1. **Java Development Kit (JDK)** – Bộ công cụ phát triển Java (JDK) – Cài đặt JDK mới nhất từ [trang web của Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java** – Aspose.PSD cho Java – Tải thư viện từ [trang tải xuống Aspose.PSD](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse hoặc NetBeans.  
4. **License** – Giấy phép – Nhận một [giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) nếu bạn chưa có giấy phép đầy đủ.

## Import Packages
First, import the classes we’ll need for loading the PSD, accessing effects, and configuring gradient fills.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

Now let’s break the process into clear steps.

## Step 1: Load the PSD File
We load the source PSD and enable effect resources so the stroke effect is available.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Step 2: Access the Stroke Effect
Assuming the stroke we want to modify belongs to the third layer (index 2), we retrieve its `StrokeEffect`.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## Step 3: Verify Stroke Effect Properties
Before making changes, we confirm the existing settings so we know exactly what we’re updating.

```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```

## Step 4: Modify the Gradient Fill Settings
Here we change the color, opacity, blend mode, and other properties to achieve the desired look.

```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```

## Step 5: Add and Modify Color and Transparency Points
We add new color and transparency points, then adjust the existing ones to shape the gradient.

```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```

## Step 6: Save the Modified PSD File
After all adjustments, we write the updated file back to disk.

```java
im.save(exportPath);
```

## Step 7: Verify the Modifications
Load the saved file and assert that every property reflects the changes we applied.

```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## Conclusion
You now know how to **create gradient stroke layer** effects in PSD files using Aspose.PSD for Java. By loading a PSD, accessing the stroke effect, tweaking gradient fill settings, and saving the result, you can programmatically produce professional‑grade graphics without ever opening Photoshop.

## FAQ's
### What is Aspose.PSD for Java?
Aspose.PSD for Java là một thư viện cho phép các nhà phát triển làm việc với các tệp PSD trong các ứng dụng Java, cung cấp các tính năng để tạo, thao tác và chuyển đổi tệp PSD.

### Do I need a license to use Aspose.PSD for Java?
Có, bạn cần một giấy phép hợp lệ để sử dụng Aspose.PSD cho Java. Bạn có thể nhận một [giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) để đánh giá.

### Can I use Aspose.PSD for Java to create PSD files from scratch?
Chắc chắn! Aspose.PSD cho Java cung cấp các API toàn diện để tạo và thao tác các tệp PSD một cách lập trình.

### Is it possible to apply other effects using Aspose.PSD for Java?
Có, bạn có thể áp dụng các hiệu ứng khác như bóng, phát sáng và nhiều hơn nữa bằng Aspose.PSD cho Java.

### Where can I find the documentation for Aspose.PSD for Java?
Bạn có thể tìm tài liệu [tại đây](https://reference.aspose.com/psd/java/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-14  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose