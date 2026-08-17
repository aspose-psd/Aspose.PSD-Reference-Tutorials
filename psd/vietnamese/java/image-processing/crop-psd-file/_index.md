---
date: 2026-08-17
description: Tìm hiểu cách cắt tệp PSD bằng Java với Aspose.PSD for Java – một phương
  pháp nhanh chóng, chính xác để cắt bớt tài liệu Photoshop trong các ứng dụng Java
  của bạn.
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: Cắt tệp PSD
og_description: Cắt tệp PSD bằng Java sử dụng Aspose.PSD for Java. Hướng dẫn này chỉ
  cho bạn từng bước cách cắt bớt tệp Photoshop một cách hiệu quả, kèm theo giải thích
  không cần mã và các mẹo thực hành tốt nhất.
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: Cắt tệp PSD bằng Java với Aspose.PSD – cắt ảnh nhanh
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: Cắt tệp PSD bằng Java sử dụng Aspose.PSD
url: /vi/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cắt tệp psd bằng Java sử dụng Aspose.PSD

## Giới thiệu

Nếu bạn cần cắt tài liệu Photoshop một cách lập trình, **crop psd file java** là một nhiệm vụ phổ biến cho các nhà phát triển Java làm việc với các pipeline đồ họa, pipeline tài sản, hoặc quy trình thiết kế tự động. Aspose.PSD for Java cung cấp một API chuyên dụng cho phép bạn xác định một hình chữ nhật và trích xuất vùng bạn cần chỉ trong vài dòng mã. Trong hướng dẫn này, bạn sẽ tìm hiểu tại sao thư viện được xây dựng để cắt ảnh hiệu suất cao, cách thiết lập môi trường, và các bước chính xác để tạo ra cả kết quả PSD và PNG.

## Câu trả lời nhanh
- **What library handles PSD cropping in Java?** Aspose.PSD for Java.
- **How many lines of code are required for a basic crop?** Hai lời gọi API sau khi tải ảnh.
- **Can I export the cropped area as PNG?** Có, sử dụng tùy chọn lưu PNG tích hợp.
- **Is a license required for production use?** Cần giấy phép thương mại sau thời gian dùng thử.
- **What Java versions are supported?** Java 8 trở lên, bao gồm Java 11, 17 và 21.

## Crop psd file java là gì?

Crop psd file java đề cập đến quá trình cắt một vùng hình chữ nhật ra khỏi tài liệu Photoshop (.psd) một cách lập trình bằng mã Java. Với Aspose.PSD, bạn có thể thực hiện thao tác này mà không cần khởi động Photoshop, làm cho nó trở nên lý tưởng cho các pipeline ảnh phía máy chủ.

## Tại sao nên sử dụng Aspose.PSD cho Java?

Aspose.PSD hỗ trợ **hơn 30 định dạng đầu vào và đầu ra** và có thể xử lý các tệp PSD lên tới **500 MB** mà không cần tải toàn bộ tài liệu vào bộ nhớ, nhờ kiến trúc streaming của nó. Thư viện bảo tồn các lớp, mặt nạ và hồ sơ màu, cung cấp kết quả cắt khớp với đầu ra gốc của Photoshop. Hiệu năng được định lượng này cho phép bạn xử lý các công việc batch trên phần cứng thông thường với mức sử dụng bộ nhớ dự đoán được.

## Yêu cầu trước

- **Java development environment** – JDK 8 hoặc mới hơn đã được cài đặt và cấu hình.
- **Aspose.PSD for Java** – tải JAR mới nhất và tài liệu [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).
- **Sample PSD file** – đặt một tệp .psd trong thư mục dự án của bạn để mã có thể tìm thấy nó.

## Cách cắt tệp PSD trong Java?

Tải tệp nguồn, xác định hình chữ nhật bạn muốn giữ, áp dụng việc cắt, và cuối cùng lưu kết quả ở các định dạng mong muốn. Toàn bộ quy trình chỉ cần năm bước đơn giản, mỗi bước được minh họa bằng một placeholder nơi bạn sẽ chèn mã của mình.

### Bước 1: đặt thư mục tài liệu

Thay thế “Your Document Directory” bằng đường dẫn tuyệt đối hoặc tương đối chứa tệp PSD bạn muốn xử lý.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### Bước 2: tải tệp PSD

Lớp `RasterImage` là điểm vào của Aspose.PSD cho các thao tác dựa trên raster trên tệp PSD. Khi tải tệp, nó tạo ra một biểu diễn trong bộ nhớ mà bạn có thể thao tác.

```java
String dataDir = "Your Document Directory";
```

### Bước 3: xác định vùng cắt

`Rectangle` xác định tọa độ X và Y cùng với chiều rộng và chiều cao của vùng cần giữ. Lớp này là một phần của gói Java AWT chuẩn và được Aspose.PSD sử dụng để chỉ định giới hạn cắt.

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### Bước 4: lưu PSD đã cắt

Sau khi áp dụng việc cắt, bạn có thể lưu kết quả lại dưới dạng PSD. Thư viện chỉ ghi các pixel đã cắt, giữ nguyên chế độ màu và độ sâu bit gốc.

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### Bước 5: lưu ảnh đã cắt dưới dạng PNG

Nếu bạn cần một phiên bản thân thiện với web, xuất raster đã cắt sang PNG. Aspose.PSD cung cấp các tùy chọn lưu PNG cho phép bạn kiểm soát mức nén và interlacing.

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## Các vấn đề thường gặp và giải pháp

- **Incorrect rectangle coordinates** – Đảm bảo các giá trị X/Y bắt đầu từ 0 cho góc trên‑trái; giá trị âm sẽ gây ra `ArgumentException`.
- **Memory spikes on large files** – Sử dụng tùy chọn `loadOptions.setLoadOnlyVisibleLayers(true)` để giảm bộ nhớ khi bạn không cần các lớp ẩn.
- **Color profile loss** – Bảo tồn hồ sơ ICC gốc bằng cách gọi `image.getColorProfile()` trước khi cắt và gán lại sau khi thực hiện.

## Câu hỏi thường gặp

### Q1: tôi có thể sử dụng Aspose.PSD cho Java để cắt ảnh ở các định dạng khác không?

A1: Aspose.PSD chủ yếu hướng tới các tệp PSD, nhưng nó cũng hỗ trợ BMP, GIF, JPEG, PNG, TIFF và một số định dạng raster khác cho cả đầu vào và đầu ra.

### Q2: Aspose.PSD cho Java có phù hợp cho xử lý ảnh quy mô lớn không?

A2: Có. Kiến trúc streaming của thư viện xử lý các tệp PSD hàng trăm trang với dung lượng bộ nhớ dưới 100 MB, làm cho nó lý tưởng cho các công việc batch.

### Q3: có những cân nhắc về giấy phép nào khi sử dụng Aspose.PSD cho Java không?

A3: Cần giấy phép thương mại cho các triển khai trong môi trường sản xuất. Chi tiết có trên [Aspose.PSD for Java purchase page](https://purchase.aspose.com/buy).

### Q4: làm thế nào tôi có thể nhận hỗ trợ cho các vấn đề liên quan đến Aspose.PSD cho Java?

A4: Truy cập [Aspose.PSD for Java forum](https://forum.aspose.com/c/psd/34) để đặt câu hỏi, chia sẻ đoạn mã, và nhận trợ giúp từ cộng đồng và các kỹ sư sản phẩm.

### Q5: tôi có thể dùng thử Aspose.PSD cho Java trước khi mua không?

A5: Có, bạn có thể tải bản dùng thử miễn phí đầy đủ chức năng [Aspose.PSD free trial download](https://releases.aspose.com/).

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## Các hướng dẫn liên quan

- [Cắt ảnh bằng hình chữ nhật trong Aspose.PSD cho Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Cắt ảnh bằng dịch chuyển trong Aspose.PSD cho Java](/psd/java/image-editing/crop-image-by-shifts/)
- [Cách xoay ảnh trong Java với Aspose.PSD](/psd/java/advanced-image-manipulation/rotate-image/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}