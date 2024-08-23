---
title: Cách thêm gradient lớp nét trong Java
linktitle: Cách thêm gradient lớp nét trong Java
second_title: API Java Aspose.PSD
description: Tìm hiểu cách thêm và tùy chỉnh độ dốc của lớp nét trong tệp PSD bằng Aspose.PSD cho Java với hướng dẫn từng bước toàn diện này.
type: docs
weight: 10
url: /vi/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## Giới thiệu
Bạn đã bao giờ tự hỏi làm cách nào để thêm gradient lớp nét vào hình ảnh của mình bằng Java chưa? Vâng, bạn đang ở đúng nơi! Hôm nay, chúng ta sẽ đi sâu vào thế giới Aspose.PSD cho Java, một thư viện mạnh mẽ giúp bạn thao tác các tệp PSD một cách dễ dàng. Cho dù bạn là người mới bắt đầu hay một nhà phát triển dày dạn kinh nghiệm, hướng dẫn từng bước này sẽ hướng dẫn bạn qua quá trình thêm gradient lớp nét vào các tệp PSD của bạn. Vì vậy, hãy thắt dây an toàn và sẵn sàng nâng cao kỹ năng chỉnh sửa đồ họa của bạn!
## Điều kiện tiên quyết
Trước khi chúng ta bắt đầu, có một số thứ bạn cần chuẩn bị sẵn. Hãy chắc chắn rằng bạn có những điều sau đây:
1.  Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt JDK trên hệ thống của mình. Bạn có thể tải nó xuống từ[trang web của Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD cho Thư viện Java: Bạn có thể tải xuống từ[Trang tải xuống Aspose.PSD](https://releases.aspose.com/psd/java/).
3. Môi trường phát triển tích hợp (IDE): Bất kỳ IDE nào như IntelliJ IDEA, Eclipse hoặc NetBeans đều sẽ hoạt động.
4.  Giấy phép hợp lệ: Bạn có thể nhận được một[giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) nếu bạn không có đầy đủ.
## Gói nhập khẩu
Trước tiên, hãy nhập các gói cần thiết. Những điều này sẽ cho phép chúng ta sử dụng các lớp và phương thức cần thiết để thao tác với tệp PSD.
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
Bây giờ, hãy chia ví dụ thành nhiều bước để hiểu rõ hơn.
## Bước 1: Tải tệp PSD
 Đầu tiên, chúng ta cần tải tệp PSD mà chúng ta muốn sửa đổi. Chúng tôi sẽ sử dụng`PsdLoadOptions` để xác định rằng chúng tôi muốn tải các tài nguyên hiệu ứng.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Bước 2: Truy cập hiệu ứng Stroke
Tiếp theo, chúng ta cần truy cập vào hiệu ứng nét vẽ của lớp mà chúng ta quan tâm. Ở đây, chúng ta giả sử đó là lớp thứ ba (chỉ mục 2) trong tệp PSD.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Bước 3: Xác minh thuộc tính hiệu ứng Stroke
Trước khi thực hiện bất kỳ thay đổi nào, hãy xác minh các thuộc tính của hiệu ứng nét vẽ để đảm bảo chúng tôi đang sửa đổi cài đặt chính xác.
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
## Bước 4: Sửa đổi cài đặt tô màu chuyển màu
Bây giờ là lúc sửa đổi cài đặt tô màu gradient theo yêu cầu của chúng tôi. Chúng tôi sẽ thay đổi màu sắc, độ mờ, chế độ hòa trộn và các thuộc tính khác.
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
## Bước 5: Thêm và sửa đổi các điểm màu và độ trong suốt
Hãy thêm các điểm màu và độ trong suốt mới cũng như sửa đổi những điểm hiện có để đạt được hiệu ứng chuyển màu mong muốn.
```java
// Thêm điểm màu mới
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Thay đổi vị trí của điểm trước đó
fillSettings.getColorPoints()[1].setLocation(1899);
// Thêm điểm trong suốt mới
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Thay đổi vị trí của điểm trong suốt trước đó
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Bước 6: Lưu tệp PSD đã sửa đổi
Sau khi thực hiện tất cả các sửa đổi cần thiết, chúng ta cần lưu tệp PSD.
```java
im.save(exportPath);
```
## Bước 7: Xác minh sửa đổi
Cuối cùng, hãy tải tệp PSD đã lưu và xác minh rằng các thay đổi của chúng tôi đã được áp dụng chính xác.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Kiểm tra điểm màu
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
// Kiểm tra điểm trong suốt
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
Và bạn có nó! Bây giờ bạn đã biết cách thêm và thao tác chuyển màu gradient của lớp nét trong tệp PSD bằng Aspose.PSD cho Java. Hướng dẫn này đề cập đến việc tải tệp PSD, truy cập và sửa đổi các hiệu ứng nét vẽ cũng như lưu các thay đổi. Với những kỹ năng này, bạn có thể tạo các gradient hấp dẫn về mặt hình ảnh và tùy chỉnh các tệp PSD cho phù hợp với nhu cầu của mình.
## Câu hỏi thường gặp
### Aspose.PSD cho Java là gì?
Aspose.PSD for Java là thư viện cho phép các nhà phát triển làm việc với các tệp PSD trong các ứng dụng Java, cung cấp các tính năng để tạo, thao tác và chuyển đổi các tệp PSD.
### Tôi có cần giấy phép để sử dụng Aspose.PSD cho Java không?
 Có, bạn cần có giấy phép hợp lệ để sử dụng Aspose.PSD cho Java. Bạn có thể nhận được một[giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) cho mục đích đánh giá.
### Tôi có thể sử dụng Aspose.PSD cho Java để tạo tệp PSD từ đầu không?
Tuyệt đối! Aspose.PSD cho Java cung cấp các API toàn diện để tạo và thao tác các tệp PSD theo chương trình.
### Có thể áp dụng các hiệu ứng khác bằng Aspose.PSD cho Java không?
Có, bạn có thể áp dụng nhiều hiệu ứng khác nhau như bóng, ánh sáng, v.v. bằng cách sử dụng Aspose.PSD cho Java.
### Tôi có thể tìm tài liệu về Aspose.PSD cho Java ở đâu?
 Bạn có thể tìm thấy tài liệu[đây](https://reference.aspose.com/psd/java/).