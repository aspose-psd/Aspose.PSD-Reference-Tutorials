---
date: 2026-09-28
description: Hướng dẫn xử lý ảnh Java cho thấy cách điều chỉnh độ sáng của một hình
  ảnh bằng Aspose.PSD cho Java. Thực hiện theo mã từng bước để tải, chỉnh sửa và lưu
  các tệp PSD hoặc TIFF.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Điều chỉnh độ sáng của hình ảnh
og_description: Hướng dẫn xử lý ảnh Java cho thấy cách điều chỉnh độ sáng của một
  hình ảnh bằng Aspose.PSD cho Java. Thực hiện theo mã từng bước để tải, chỉnh sửa
  và lưu các tệp PSD hoặc TIFF.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Xử lý ảnh Java: điều chỉnh độ sáng với Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Xử lý ảnh Java: điều chỉnh độ sáng với Aspose.PSD'
url: /vi/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Điều chỉnh độ sáng của hình ảnh với Aspose.PSD cho Java

## Giới thiệu

Trong tutorial **java image processing** này, bạn sẽ học cách điều chỉnh độ sáng của một bức ảnh trực tiếp từ mã Java. Việc tinh chỉnh độ sáng là một nhiệm vụ thường gặp đối với các nhà thiết kế đồ họa, nhiếp ảnh gia và bất kỳ ai xây dựng các pipeline xử lý ảnh. Trong hướng dẫn **java image manipulation** này, chúng tôi sẽ hướng dẫn quy trình đầy đủ — tải PSD/TIFF, áp dụng độ lệch độ sáng và lưu kết quả — bằng thư viện Aspose.PSD cho Java.

## Câu trả lời nhanh
- **Thư viện nào xử lý độ sáng?** Aspose.PSD for Java.  
- **Phương thức nào thay đổi độ sáng?** `RasterImage.adjustBrightness()`.  
- **Tôi có thể làm việc với các tệp PSD và TIFF không?** Có, API hỗ trợ cả hai định dạng và hơn 10 loại ảnh bổ sung.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Cần giấy phép thương mại cho việc sử dụng không phải để đánh giá.  
- **Thời gian thực hiện khoảng bao lâu?** Thông thường dưới 10 phút cho một điều chỉnh cơ bản.

## Java image processing là gì?
`Java image processing` đề cập đến tập hợp các kỹ thuật cho phép bạn đọc, biến đổi và ghi dữ liệu ảnh một cách lập trình bằng Java. Điều chỉnh độ sáng là một trong những thao tác cốt lõi thay đổi độ sáng tổng thể của mỗi pixel, làm cho các vùng tối trở nên sáng hơn hoặc các vùng sáng trở nên tối hơn.

## Tại sao nên sử dụng Aspose.PSD cho Java?
Aspose.PSD cho Java cung cấp một giải pháp toàn diện, thuần Java, hỗ trợ đa dạng các định dạng raster và vector, loại bỏ các phụ thuộc native và cung cấp bộ nhớ đệm hiệu suất cao cho các tệp lớn. API phong phú của nó cho phép các nhà phát triển thực hiện các chỉnh sửa phức tạp về màu sắc và lớp với ít mã, làm cho nó trở nên lý tưởng cho cả các điều chỉnh đơn giản và các pipeline xử lý ảnh nâng cao.

- **Hỗ trợ hơn 10 định dạng raster và vector** – PSD, TIFF, JPEG, PNG, BMP, GIF, và hơn nữa.  
- **Triển khai thuần Java** – không có DLL native hay phụ thuộc bên ngoài, vì vậy nó hoạt động trên bất kỳ JVM nào.  
- **Bộ nhớ đệm hiệu suất cao** – dữ liệu raster có thể được lưu vào bộ nhớ đệm, cho phép chỉnh sửa lặp lại nhanh gấp tới 2× trên các tệp lớn.  
- **Giao diện API phong phú** – hơn 150 phương thức cho việc chỉnh màu, xử lý lớp, mặt nạ và ghép ảnh.

## Yêu cầu trước

Trước khi bắt đầu tutorial, hãy chắc chắn rằng bạn đã có các yêu cầu sau:

- Thư viện Aspose.PSD cho Java: Tải xuống và cài đặt thư viện từ [tài liệu Aspose.PSD cho Java](https://reference.aspose.com/psd/java/).  
- Bộ công cụ phát triển Java (JDK) 8 hoặc cao hơn đã được cài đặt trên máy của bạn.  
- Môi trường phát triển (IDE) như IntelliJ IDEA, Eclipse hoặc VS Code.

## Nhập các gói

Để bắt đầu, nhập các gói cần thiết vào dự án Java của bạn. Trong ví dụ này, chúng ta sẽ sử dụng các gói sau:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Bây giờ, hãy chia quy trình điều chỉnh độ sáng của một hình ảnh thành các bước đơn giản:

## Cách điều chỉnh độ sáng bằng Aspose.PSD?

Tải hình ảnh nguồn, áp dụng độ lệch độ sáng, cấu hình tùy chọn lưu và ghi kết quả ra đĩa — tất cả trong bốn bước ngắn gọn. Các phần sau cung cấp hướng dẫn chi tiết, từng bước mà bạn có thể sao chép vào dự án của mình. Cách tiếp cận này đảm bảo mỗi thao tác được thực hiện hiệu quả và hình ảnh cuối cùng giữ nguyên chất lượng gốc đồng thời phản ánh sự thay đổi độ sáng mong muốn.

### Bước 1: Tải hình ảnh

Lớp `RasterImage` đại diện cho phiên bản raster hoá của tệp PSD hoặc TIFF trong bộ nhớ. Nó cung cấp truy cập trực tiếp vào pixel cho các thao tác chỉnh màu.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Trong bước này, chúng ta tải hình ảnh mục tiêu và ép kiểu nó thành `RasterImage` để tiếp tục xử lý.

### Bước 2: Điều chỉnh độ sáng

`adjustBrightness(int value)` thay đổi độ sáng của mỗi pixel theo giá trị nguyên được chỉ định. Số dương làm sáng ảnh; số âm làm tối ảnh. Phương thức xử lý ảnh ngay tại chỗ, không cần tạo đối tượng mới.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Ở đây, chúng ta sử dụng phương thức `adjustBrightness` để thay đổi độ sáng của hình ảnh. Trong ví dụ này, chúng ta giảm độ sáng xuống 50 đơn vị, nhưng bạn có thể tùy chỉnh giá trị này tùy theo yêu cầu.

### Bước 3: Đặt TiffOptions

`TiffOptions` chỉ định các tham số mã hoá cho đầu ra TIFF, chẳng hạn như bits per sample và photometric interpretation. Nó cho phép bạn kiểm soát cách tệp kết quả được mã hoá.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Cấu hình `TiffOptions` để lưu hình ảnh đã điều chỉnh. Điều chỉnh các thuộc tính `bitsPerSample` và `photometric` dựa trên nhu cầu cụ thể của bạn.

### Bước 4: Lưu hình ảnh kết quả

Gọi `save` sẽ ghi dữ liệu raster đã xử lý vào một tệp sử dụng các tùy chọn đã định nghĩa trước. Thao tác này nguyên tử và đảm bảo tệp đầu ra là một ảnh TIFF hợp lệ.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Cuối cùng, lưu hình ảnh đã chỉnh sửa bằng `TiffOptions` đã chỉ định.

## Các vấn đề thường gặp và giải pháp

| Issue | Reason | Solution |
|-------|--------|----------|
| **`ClassCastException` when casting Image** | Tệp không phải là ảnh raster (ví dụ, PSD vector). | Xác minh định dạng tệp nguồn hoặc sử dụng `image instanceof RasterImage` trước khi ép kiểu. |
| **Brightness change has no effect** | Ảnh chưa được lưu vào bộ nhớ đệm trước khi điều chỉnh. | Gọi `rasterImage.cacheData()` như đã minh họa trong Bước 1. |
| **Saved file appears corrupted** | Cấu hình `TiffOptions` không đúng. | Đảm bảo `bitsPerSample` khớp với độ sâu ảnh nguồn (thông thường 8‑bit mỗi kênh). |

## Câu hỏi thường gặp

**H: Tôi có thể điều chỉnh độ sáng trong các định dạng ảnh khác ngoài PSD không?**  
Đ: Có, Aspose.PSD cho Java hỗ trợ JPEG, PNG, BMP, GIF và nhiều định dạng raster khác ngoài PSD và TIFF.

**H: Làm thế nào để xử lý lỗi trong quá trình điều chỉnh ảnh?**  
Đ: Bao quanh mã xử lý bằng khối try‑catch và bắt `IOException` hoặc `ImageProcessingException` để quản lý lỗi truy cập tệp và thao tác raster.

**H: Có giới hạn nào cho phạm vi điều chỉnh độ sáng không?**  
Đ: Phương thức chấp nhận các giá trị nguyên từ –255 đến +255; các giá trị ngoài phạm vi này sẽ bị giới hạn tới giá trị gần nhất.

**H: Tôi có thể sử dụng Aspose.PSD cho Java trong các dự án thương mại không?**  
Đ: Có, cần giấy phép thương mại cho việc sử dụng trong môi trường sản xuất. Mua giấy phép [tại đây](https://purchase.aspose.com/buy).

**H: Có bản dùng thử miễn phí không?**  
Đ: Có, bạn có thể khám phá thư viện với bản dùng thử miễn phí từ [đây](https://releases.aspose.com/).

**H: Phương thức `adjustBrightness` có ảnh hưởng đến độ hiển thị của lớp không?**  
Đ: Phương thức hoạt động trên ảnh composite đã raster hóa, vì vậy các lớp ẩn sẽ bị bỏ qua trong quá trình raster hóa, giữ nguyên kết quả hình ảnh mong muốn.

**H: Tôi có thể chuỗi nhiều điều chỉnh (ví dụ, độ tương phản, độ bão hòa) liên tiếp không?**  
Đ: Chắc chắn. Sau khi điều chỉnh độ sáng, bạn có thể gọi `adjustContrast`, `adjustSaturation`, hoặc các phương thức chỉnh màu khác trên cùng một đối tượng `RasterImage`.

**Last Updated:** 2026-09-28  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose

## Hướng dẫn liên quan

- [Thư viện Xử lý Ảnh Java: Đảo ngược Lớp bằng Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Chuyển ảnh sang Đen trắng bằng Aspose.PSD cho Java](/psd/java/advanced-techniques/grayscale-image/)
- [Cách Xoay ảnh ở góc cụ thể với Aspose.PSD cho Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}