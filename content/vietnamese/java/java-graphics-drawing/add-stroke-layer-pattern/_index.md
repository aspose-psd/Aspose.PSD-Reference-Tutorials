---
title: Cách thêm mẫu lớp nét trong Java
linktitle: Cách thêm mẫu lớp nét trong Java
second_title: API Java Aspose.PSD
description: Tìm hiểu cách thêm mẫu lớp nét vào tệp PSD bằng Aspose.PSD cho Java. Hãy làm theo hướng dẫn từng bước này để cải thiện hình ảnh của bạn một cách dễ dàng.
type: docs
weight: 11
url: /vi/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## Giới thiệu
Việc thêm mẫu lớp nét vẽ vào hình ảnh trong Java nghe có vẻ là một nhiệm vụ khó khăn, nhưng với Aspose.PSD cho Java, điều đó dễ dàng hơn bạn nghĩ. Cho dù bạn đang thiết kế đồ họa hay làm việc trên các ứng dụng chỉnh sửa ảnh, hướng dẫn này sẽ hướng dẫn bạn thực hiện quy trình từng bước. Sẵn sàng để bắt đầu? Hãy đi sâu vào!
## Điều kiện tiên quyết
Trước khi bắt đầu, bạn sẽ cần một số thứ:
- Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt JDK trên hệ thống của mình.
-  Aspose.PSD cho Java: Tải xuống thư viện từ[đây](https://releases.aspose.com/psd/java/) và đưa nó vào dự án của bạn.
- IDE: Sử dụng Môi trường phát triển tích hợp (IDE) yêu thích của bạn như IntelliJ IDEA hoặc Eclipse.
## Gói nhập khẩu
Trước tiên, bạn cần nhập các gói cần thiết vào dự án Java của mình. Các gói này rất cần thiết để làm việc với Aspose.PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## Bước 1: Tải tệp PSD
Bước đầu tiên trong việc thêm mẫu lớp nét vẽ là tải tệp PSD mà bạn muốn chỉnh sửa.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
Bằng cách tải tệp PSD, giờ đây bạn có thể truy cập và thao tác các lớp và hiệu ứng của nó.
## Bước 2: Chuẩn bị dữ liệu mẫu mới
Tiếp theo, bạn cần chuẩn bị dữ liệu mẫu mới mà bạn sẽ áp dụng cho lớp nét vẽ.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
Dữ liệu mẫu này sẽ được sử dụng để tạo hiệu ứng nét mới.
## Bước 3: Truy cập hiệu ứng Stroke
Để sửa đổi hiệu ứng nét vẽ, bạn cần truy cập vào lớp cụ thể và các tùy chọn hòa trộn của nó.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Điều này đảm bảo bạn đang làm việc với lớp và hiệu ứng chính xác.
## Bước 4: Sửa đổi hiệu ứng Stroke
Bây giờ, hãy sửa đổi hiệu ứng nét vẽ với dữ liệu mẫu mới.
### Cập nhật thuộc tính hiệu ứng nét vẽ
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Cập nhật tài nguyên mẫu
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
Đoạn mã này cập nhật tài nguyên mẫu bằng dữ liệu mẫu mới.
## Bước 5: Áp dụng mẫu mới
Cuối cùng, áp dụng mẫu mới cho hiệu ứng nét vẽ và lưu các thay đổi.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Điều này đảm bảo mẫu mới được áp dụng chính xác và tệp được lưu cùng với các thay đổi.
## Bước 6: Xác minh các thay đổi
Để đảm bảo mọi thứ hoạt động chính xác, hãy tải lại tệp và xác minh các thay đổi.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
Bước này xác minh rằng dữ liệu mẫu đã được áp dụng chính xác cho hiệu ứng nét vẽ.
## Phần kết luận
Và bạn có nó rồi đấy! Bạn đã thêm thành công mẫu lớp nét vào tệp PSD bằng Aspose.PSD cho Java. Bằng cách làm theo các bước này, bạn có thể tùy chỉnh và nâng cao hình ảnh của mình một cách dễ dàng. Chúc mừng mã hóa!
## Câu hỏi thường gặp
### Aspose.PSD cho Java là gì?
Aspose.PSD cho Java là thư viện cho phép các nhà phát triển tạo, chỉnh sửa và chuyển đổi các tệp PSD (Tài liệu Photoshop) theo chương trình.
### Tôi có thể sử dụng Aspose.PSD cho Java trong một dự án thương mại không?
 Có, bạn có thể sử dụng nó trong các dự án thương mại. Bạn có thể mua giấy phép từ[đây](https://purchase.aspose.com/buy).
### Có bản dùng thử miễn phí dành cho Aspose.PSD cho Java không?
 Có, bạn có thể tải xuống phiên bản dùng thử miễn phí từ[đây](https://releases.aspose.com/).
### Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.PSD cho Java?
 Bạn có thể nhận được hỗ trợ từ diễn đàn cộng đồng Aspose[đây](https://forum.aspose.com/c/psd/34).
### Yêu cầu hệ thống đối với Aspose.PSD cho Java là gì?
Bạn cần cài đặt JDK và IDE để phát triển. Thư viện hỗ trợ nhiều hệ điều hành bao gồm Windows, Linux và macOS.