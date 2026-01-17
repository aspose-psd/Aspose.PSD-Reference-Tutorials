---
date: 2026-01-17
description: Tìm hiểu cách thêm mẫu nét vẽ trong Java với Aspose.PSD cho Java. Hãy
  làm theo hướng dẫn từng bước này để nhanh chóng cải thiện các hình ảnh PSD của bạn.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Cách Thêm Mẫu Đường Viền trong Java bằng Aspose.PSD
url: /vi/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Thêm Stroke Pattern Java Sử Dụng Aspose.PSD

## Giới thiệu
Nếu bạn cần **thêm stroke pattern java** vào một tệp Photoshop, Aspose.PSD for Java làm cho việc này trở nên vô cùng đơn giản. Dù bạn đang xây dựng một công cụ thiết kế đồ họa, tự động hoá các chỉnh sửa hàng loạt, hay chỉ thử nghiệm các hiệu ứng lớp, hướng dẫn này sẽ dẫn bạn qua từng bước — từ việc tải PSD đến việc xác nhận mẫu mới. Hãy cùng khám phá và xem bạn có thể nâng cấp hình ảnh của mình nhanh chóng như thế nào.

## Trả Lời Nhanh
- **Thư viện tôi cần gì?** Aspose.PSD for Java  
- **Phiên bản Java nào được hỗ trợ?** JDK 8 hoặc mới hơn  
- **Có cần giấy phép để thử nghiệm không?** Bản dùng thử miễn phí đủ cho việc phát triển; cần giấy phép cho môi trường sản xuất  
- **Thời gian triển khai khoảng bao lâu?** Khoảng 10‑15 phút cho một stroke pattern cơ bản  
- **Có thể tái sử dụng pattern trên nhiều lớp không?** Có, chỉ cần gán cùng một `PattResource` cho các lớp khác  

## Add stroke pattern java là gì?
Thêm một stroke pattern trong Java có nghĩa là áp dụng một fill tùy chỉnh (thường là một bitmap lặp lại) cho hiệu ứng stroke của một lớp. Kỹ thuật này cho phép bạn tạo các đường viền có kiểu dáng—ví dụ như đường gạch, họa tiết gạch, hoặc viền đồ họa tùy chỉnh—trực tiếp trong tệp PSD mà không cần mở Photoshop.

## Tại sao nên dùng Aspose.PSD cho add stroke pattern java?
- **Độ trung thực PSD đầy đủ** – Tất cả các hiệu ứng lớp, tài nguyên và chế độ hòa trộn được giữ nguyên.  
- **Không cần Photoshop gốc** – Hoạt động trên bất kỳ hệ điều hành nào có JDK.  
- **Kiểm soát bằng mã** – Tự động hoá xử lý hàng loạt hoặc tích hợp vào các dịch vụ phía server.  
- **API phong phú** – Truy cập tài nguyên toàn cục, pattern fill và blend mode trong một giao diện liền mạch.

## Yêu cầu trước
- **Java Development Kit (JDK)** – Đảm bảo đã cài đặt JDK 8 hoặc mới hơn.  
- **Aspose.PSD for Java** – Tải thư viện từ [here](https://releases.aspose.com/psd/java/) và thêm JAR vào classpath của dự án.  
- **IDE** – IntelliJ IDEA, Eclipse, hoặc bất kỳ trình soạn thảo nào bạn thích.

## Nhập Gói
Đầu tiên, nhập các lớp cần thiết để xử lý tệp PSD, màu sắc, hình chữ nhật và hiệu ứng stroke.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```

## Bước 1: Tải Tệp PSD
Tải tệp PSD nguồn để bạn có thể làm việc với các lớp và tài nguyên của nó.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Bước 2: Chuẩn Bị Dữ Liệu Pattern Mới
Tạo một pattern đơn giản kích thước 4 × 4 pixel sẽ được dùng cho stroke.

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

## Bước 3: Truy Cập Hiệu Ứng Stroke
Xác định hiệu ứng stroke trên lớp mục tiêu (trong ví dụ này là lớp thứ tư).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Bước 4: Sửa Đổi Hiệu Ứng Stroke
### Cập Nhật Thuộc Tính Stroke
Điều chỉnh độ trong suốt và chế độ hòa trộn để xem ảnh hưởng trực quan của pattern mới.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Cập Nhật Tài Nguyên Pattern
Thay thế tài nguyên pattern toàn cục hiện có bằng tài nguyên bạn vừa tạo.

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

## Bước 5: Áp Dụng Pattern Mới
Liên kết tài nguyên pattern đã cập nhật với hiệu ứng stroke và lưu lại tệp PSD.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Bước 6: Xác Minh Thay Đổi
Tải lại tệp và xác nhận rằng pattern mới, độ trong suốt và chế độ hòa trộn đã được áp dụng đúng.

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

## Các Vấn Đề Thường Gặp và Giải Pháp
| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|-----------|
| Pattern không hiển thị | Tham chiếu `PatternId` sai | Đảm bảo `PatternId` được đặt trên `PattResource` khớp với `PatternFillSettings`. |
| Stroke biến mất sau khi lưu | Độ trong suốt được đặt thành 0 hoặc hiệu ứng bị ẩn | Kiểm tra `setOpacity` nằm trong khoảng 0‑255 và `isVisible()` trả về `true`. |
| Màu sắc không như mong đợi | Chế độ hòa trộn không phù hợp | Sử dụng `BlendMode.Color` (hoặc chế độ khác) phù hợp với mục đích thiết kế. |

## Câu Hỏi Thường Gặp
### Aspose.PSD for Java là gì?
Aspose.PSD for Java là một thư viện cho phép các nhà phát triển tạo, chỉnh sửa và chuyển đổi tệp PSD (Photoshop Document) một cách lập trình.

### Tôi có thể sử dụng Aspose.PSD for Java trong dự án thương mại không?
Có, bạn có thể sử dụng nó trong các dự án thương mại. Bạn có thể mua giấy phép từ [here](https://purchase.aspose.com/buy).

### Có bản dùng thử miễn phí cho Aspose.PSD for Java không?
Có, bạn có thể tải phiên bản dùng thử miễn phí từ [here](https://releases.aspose.com/).

### Làm sao để nhận hỗ trợ cho Aspose.PSD for Java?
Bạn có thể nhận hỗ trợ từ diễn đàn cộng đồng Aspose [here](https://forum.aspose.com/c/psd/34).

### Yêu cầu hệ thống cho Aspose.PSD for Java là gì?
Bạn cần cài đặt JDK và một IDE để phát triển. Thư viện hỗ trợ nhiều hệ điều hành bao gồm Windows, Linux và macOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2026-01-17  
**Đã kiểm tra với:** Aspose.PSD for Java 24.12 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose