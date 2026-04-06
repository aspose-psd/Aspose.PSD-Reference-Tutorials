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

# Cách tạo gradient viền lớp trong Java

## Giới thiệu
Bạn đã bao giờ tự hỏi làm thế nào để **tạo lớp viền gradient** trong các tệp PSD của mình bằng Java? Bạn đang ở đúng nơi! Hôm nay chúng tôi sẽ khám phá Aspose.PSD cho Java — một thư mạnh mẽ cho phép bạn vận hành các tệp PSD một cách dễ dàng. Dù bạn mới bắt đầu cài đặt đồ họa hay muốn điều chỉnh các thiết kế hiện có, hướng dẫn này sẽ hướng dẫn bạn từng bước bổ sung và tùy chỉnh đường viền gradient.

## Trả lời nhanh
- **Mục tiêu chính là gì?** Mục tiêu chính là gì? Tạo một gradient viền lớp trên tệp PSD.
- **Cần có thư viện nào?** Thư viện nào cần thiết? Aspose.PSD cho Java.
- **Tôi có cần giấy phép không?** Tôi có cần giấy phép không? Có, cần có hợp lệ giấy phép (hoặc tạm thời) cho môi trường sản xuất.
- **Phiên bản Java nào hoạt động?** Phiên bản Java nào đang hoạt động? Java8hoặc cao hơn.
- **Thời gian thực hiện mất bao lâu?** Thời gian thực hiện khoảng bao lâu? Khoảng 10‑15 phút cho một cơ sở gradient biên giới.

## Lớp nét chuyển màu là gì?
Lớp border gradient là một đường viền vector bao quanh một dạng hoặc văn bản, chuyển đổi mượt mà giữa các màu. Sử dụng Aspose.PSD, bạn có thể định nghĩa chương trình các màu, độ trong suốt, góc và loại (tuyến tính, bán kính, v.v.) của đường viền.

## Tại sao nên sử dụng Aspose.PSD cho Java?
- **Hỗ trợ đầy đủ PSD** – Hỗ trợ đầy đủ PSD – đọc, chỉnh sửa và ghi các tệp PSD mà không cần Photoshop.
- **API hiệu ứng phong phú** – API hiệu ứng phong phú – truy cập viền, bóng, phát sáng và nhiều lớp ứng dụng hiệu ứng khác.
- **Đa nền tảng** – Nền tảng – hoạt động trên bất kỳ hệ điều hành nào hỗ trợ Java.
- **Không có phụ thuộc gốc** – Không phụ thuộc gốc – thuần Java, dễ tích hợp vào CI đường ống.

## Điều kiện tiên quyết
1. **Bộ công cụ phát triển Java (JDK)** – Bộ công cụ phát triển Java (JDK) – Cài đặt JDK mới nhất từ ​​[trang web của Oracle](https://www.oracle.com/java/technologists/javase-downloads.html).
2. **Aspose.PSD for Java** – Aspose.PSD cho Java – Tải thư viện từ [trang tải xuống Aspose.PSD](https://releases.aspose.com/psd/java/).
3. **IDE** – IntelliJ IDEA, Eclipse hoặc NetBeans.
4. **Giấy phép** – Giấy phép – Nhận một [giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) nếu bạn chưa có giấy phép đầy đủ.

## Nhập gói
Trước tiên, hãy nhập các lớp mà chúng ta cần để tải PSD, truy cập các hiệu ứng và định cấu hình tô màu chuyển màu.

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

Bây giờ hãy chia quá trình thành các bước rõ ràng.

## Bước 1: Tải tập tin PSD
Chúng ta tải tập tin PSD nguồn và kích hoạt các tài nguyên hiệu ứng để hiệu ứng đường viền có thể sử dụng được.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Bước 2: Truy cập hiệu ứng nét vẽ
Giả sử nét vẽ chúng ta muốn chỉnh sửa thuộc về lớp thứ ba (index2), chúng ta truy xuất thuộc tính `StrokeEffect` của nó.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## Bước 3: Kiểm tra thuộc tính hiệu ứng nét vẽ
Trước khi thực hiện thay đổi, chúng ta xác nhận các cài đặt hiện có để biết chính xác những gì chúng ta đang cập nhật.

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

## Bước 4: Chỉnh sửa cài đặt tô màu chuyển sắc
Tại đây, chúng ta thay đổi màu sắc, độ mờ, chế độ hòa trộn và các thuộc tính khác để đạt được giao diện mong muốn.

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

## Bước 5: Thêm và chỉnh sửa điểm màu và độ trong suốt
Chúng ta thêm các điểm màu và độ trong suốt mới, sau đó điều chỉnh các điểm hiện có để tạo hình chuyển sắc.

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

## Bước 6: Lưu tệp PSD đã chỉnh sửa
Sau khi thực hiện tất cả các điều chỉnh, chúng ta ghi tệp đã cập nhật trở lại ổ đĩa.

```java
im.save(exportPath);
```

## Bước 7: Kiểm tra các chỉnh sửa
Tải tệp đã lưu và xác nhận rằng mọi thuộc tính đều phản ánh các thay đổi chúng ta đã áp dụng.

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

## Phần kết luận
Bây giờ bạn đã biết cách **tạo hiệu ứng lớp nét chuyển màu** trong tệp PSD bằng Aspose.PSD cho Java. Bằng cách tải PSD, truy cập hiệu ứng nét vẽ, điều chỉnh cài đặt tô màu chuyển màu và lưu kết quả, bạn có thể tạo đồ họa cấp chuyên nghiệp theo chương trình mà không cần mở Photoshop.

## Câu hỏi thường gặp
### Aspose.PSD cho Java là gì?
Aspose.PSD for Java là một thư viện cho phép các nhà phát triển làm việc với các tệp PSD trong các ứng dụng Java, cung cấp các tính năng để tạo, thao tác và chuyển đổi tệp PSD.

### Tôi có cần giấy phép để sử dụng Aspose.PSD cho Java không?
Có, bạn cần có giấy phép hợp lệ để sử dụng Aspose.PSD cho Java. Bạn có thể nhận được [giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) để đánh giá.

### Tôi có thể sử dụng Aspose.PSD cho Java để tạo tệp PSD từ đầu không?
Chắc chắn! Aspose.PSD cho Java cung cấp các API toàn diện để tạo và vận hành các tệp PSD theo cách thiết lập.

### Có thể áp dụng các hiệu ứng khác bằng Aspose.PSD cho Java không?
Có, bạn có thể áp dụng các ứng dụng khác như bóng, phát sáng và nhiều thứ khác bằng Aspose.PSD cho Java.

### Tôi có thể tìm tài liệu về Aspose.PSD cho Java ở đâu?
Bạn có thể tìm tài liệu [tại đây](https://reference.aspose.com/psd/java/).

---

**Cập nhật lần cuối:** 2026-01-14
**Đã thử nghiệm với:** Aspose.PSD cho Java 24.11
**Tác giả:** Giả định

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
