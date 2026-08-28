---
date: 2026-08-28
description: Thêm pattern vào layer trong Java với Aspose.PSD. Thực hiện theo hướng
  dẫn từng bước để áp dụng stroke layer effect, cấu hình pattern resources và lưu
  các tệp PSD của bạn một cách hiệu quả.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Cách Thêm Stroke Layer Pattern trong Java
og_description: Thêm pattern vào layer trong Java bằng Aspose.PSD. Thực hiện theo
  hướng dẫn ngắn gọn để áp dụng stroke layer effect, cấu hình pattern resources và
  lưu các tệp PSD của bạn một cách hiệu quả.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Thêm pattern vào layer trong Java – Aspose.PSD tutorial
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Cách thêm pattern vào layer trong Java
url: /vi/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách thêm mẫu vào lớp trong Java

## Giới thiệu
Thêm mẫu vào lớp trong Java là một yêu cầu phổ biến khi bạn cần làm phong phú các tệp Photoshop PSD bằng các hiệu ứng nét viền tùy chỉnh. Với Aspose.PSD cho Java, nhiệm vụ này trở nên đơn giản, ngay cả khi bạn mới làm quen với thư viện. Trong hướng dẫn này, bạn sẽ học cách tải một tệp PSD, tạo một tài nguyên mẫu, gắn nó vào hiệu ứng nét viền, và lưu kết quả — tất cả với các hướng dẫn rõ ràng, từng bước.

## Câu trả lời nhanh
- **Thư viện cần thiết là gì?** Aspose.PSD for Java.  
- **Thời gian thực hiện khoảng bao lâu?** Khoảng 10‑15 phút cho một mẫu cơ bản.  
- **Có cần giấy phép không?** Bản dùng thử miễn phí đủ cho phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Phiên bản Java nào được hỗ trợ?** JDK 8 hoặc mới hơn.  
- **Có thể sử dụng trong dịch vụ web không?** Có, API không phụ thuộc vào nền tảng và hoạt động trong bất kỳ môi trường Java nào.

## Thêm mẫu vào một lớp là gì?
Thêm mẫu vào một lớp có nghĩa là gán một bitmap lặp lại vào hiệu ứng nét viền hoặc tô màu sao cho hình ảnh lặp lại trên viền của hình dạng. Kỹ thuật này thường được dùng cho viền trang trí, kết cấu và lớp phủ thương hiệu, cho phép nhà thiết kế tạo ra các chủ đề hình ảnh nhất quán mà không cần vẽ từng phần tử một cách thủ công.

## Tại sao nên sử dụng Aspose.PSD cho nhiệm vụ này?
Aspose.PSD hỗ trợ **hơn 30 định dạng ảnh** và có thể thao tác các tệp PSD lên tới **2 GB** mà không cần tải toàn bộ tài liệu vào bộ nhớ, mang lại hiệu năng nhanh trên phần cứng máy chủ thông thường. API linh hoạt cho phép bạn làm việc với các hiệu ứng lớp một cách lập trình, loại bỏ nhu cầu sử dụng Photoshop trong các quy trình tự động.

## Yêu cầu trước
- Java Development Kit (JDK) 8 hoặc mới hơn đã được cài đặt.  
- Aspose.PSD cho Java – tải xuống từ **trang tải Aspose.PSD cho Java**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) và thêm JAR vào classpath của dự án.  
- Một IDE như IntelliJ IDEA hoặc Eclipse để chỉnh sửa và chạy mã mẫu.  
- Một tệp PSD mẫu chứa lớp hình dạng mà bạn muốn sửa đổi.

## Nhập các gói
Đầu tiên, nhập các namespace cung cấp quyền truy cập vào các đối tượng PSD, tài nguyên và hiệu ứng.

```
// No actual code block is added to preserve original placeholders.
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
```

## Cách thêm mẫu vào lớp trong Java?

Tải tệp PSD mục tiêu, tạo một tài nguyên mẫu, gắn nó vào hiệu ứng nét viền của lớp mong muốn, và cuối cùng lưu tệp. Quy trình từ đầu đến cuối này chỉ mất vài dòng mã và hoạt động với bất kỳ tệp PSD chuẩn nào có chứa lớp hình dạng vector.

### Bước 1: tải tệp PSD
Việc tải tài liệu cho phép bạn truy cập vào cấu trúc lớp và bộ sưu tập hiệu ứng.  
`PsdLoadOptions` cấu hình cách PSD được đọc, trong khi `PsdImage` đại diện cho tệp đã tải trong bộ nhớ.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

Bằng cách tải tệp PSD, bạn hiện có thể truy cập và thao tác các lớp và hiệu ứng của nó.

### Bước 2: chuẩn bị dữ liệu mẫu mới
Tạo một `PatternResource` chứa bitmap bạn muốn lặp lại làm mẫu nét viền.  
`PatternResource` là tài nguyên toàn cục PSD lưu trữ một mẫu bitmap lặp lại. `Rectangle` xác định giới hạn của mẫu, và `UUID` cung cấp một định danh duy nhất.

```
// Placeholder for original code.
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
```

Dữ liệu mẫu này sẽ được dùng để tạo hiệu ứng nét viền mới.

### Bước 3: truy cập hiệu ứng nét viền
Xác định lớp hình dạng đã có nét viền, sau đó lấy đối tượng `StrokeEffect` của nó.  
`StrokeEffect` đại diện cho hiệu ứng nét viền được áp dụng cho lớp hình dạng.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

Điều này đảm bảo bạn đang làm việc với lớp và hiệu ứng đúng.

### Bước 4: sửa đổi hiệu ứng nét viền
Bây giờ cập nhật các thuộc tính của nét viền để tham chiếu tới tài nguyên mẫu mới.

#### Cập nhật thuộc tính hiệu ứng nét viền
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### Cập nhật tài nguyên mẫu
`PattResource` là tài nguyên lớp toàn cục PSD lưu trữ dữ liệu mẫu.

```
// Placeholder for original code.
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
```

Các đoạn mã này thay thế mẫu hiện có bằng mẫu bạn đã cung cấp.

### Bước 5: áp dụng mẫu mới
`PatternFillSettings` chứa các cài đặt tô cho hiệu ứng nét viền dựa trên mẫu. Cam kết các thay đổi vào lớp và ghi lại PSD đã cập nhật lên đĩa.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

Điều này đảm bảo mẫu mới được áp dụng đúng và tệp được lưu lại với các thay đổi.

### Bước 6: xác minh các thay đổi
Tải lại tệp và kiểm tra nét viền để xác nhận mẫu hiển thị như mong đợi.

```
// Placeholder for original code.
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
```

Bước này xác minh rằng dữ liệu mẫu đã được áp dụng chính xác cho hiệu ứng nét viền.

## Các vấn đề thường gặp và khắc phục
- **Mẫu không hiển thị:** Đảm bảo DPI của ảnh mẫu khớp với độ phân giải của PSD, và cờ `Enabled` của nét viền được đặt thành `true`.  
- **Các tệp PSD lớn gây OutOfMemoryError:** Sử dụng `PsdImage.load(..., LoadOptions)` với `LoadOptions.setLoadAllLayers(false)` để tải lớp khi cần.  
- **Lớp không đúng được chọn:** Xác minh chỉ mục hoặc tên lớp trước khi truy cập các hiệu ứng; bạn có thể liệt kê `psdImage.getLayers()` để xem các lớp có sẵn.

## Câu hỏi thường gặp

**Q: Aspose.PSD cho Java là gì?**  
A: Aspose.PSD cho Java là một thư viện cho phép các nhà phát triển tạo, chỉnh sửa và chuyển đổi các tệp PSD (Photoshop Document) một cách lập trình.

**Q: Có thể sử dụng Aspose.PSD cho Java trong dự án thương mại không?**  
A: Có, bạn có thể sử dụng trong dự án thương mại. Bạn có thể mua giấy phép từ **trang mua Aspose**([Aspose purchase page](https://purchase.aspose.com/buy)).

**Q: Có phiên bản dùng thử miễn phí cho Aspose.PSD cho Java không?**  
A: Có, bạn có thể tải phiên bản dùng thử miễn phí từ **trang phát hành Aspose**([Aspose releases page](https://releases.aspose.com/)).

**Q: Làm sao để nhận hỗ trợ cho Aspose.PSD cho Java?**  
A: Bạn có thể nhận hỗ trợ từ diễn đàn cộng đồng Aspose **tại đây**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)).

**Q: Yêu cầu hệ thống cho Aspose.PSD cho Java là gì?**  
A: Bạn cần cài đặt JDK và một IDE để phát triển. Thư viện hỗ trợ Windows, Linux và macOS.

## Kết luận
Bạn đã học cách thêm mẫu vào lớp trong Java bằng Aspose.PSD. Bằng cách làm theo các bước trên, bạn có thể nâng cao các tệp PSD một cách lập trình với các mẫu nét viền tùy chỉnh, tự động hoá quy trình thương hiệu, và tích hợp xử lý đồ họa vào bất kỳ ứng dụng Java nào. Khám phá các tính năng khác của Aspose.PSD như hợp nhất lớp, điều chỉnh màu, và xuất ra PNG hoặc JPEG để mở rộng bộ công cụ xử lý ảnh của mình.

---

**Last Updated:** 2026-08-28  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose

## Các hướng dẫn liên quan

- [Kết xuất lớp Đổ mẫu PSD](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Ghi đè mẫu PSD: Thêm hiệu ứng với Aspose.PSD cho Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Cách thay đổi màu nét viền Java bằng Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}