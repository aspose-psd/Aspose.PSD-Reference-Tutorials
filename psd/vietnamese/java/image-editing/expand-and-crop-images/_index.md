---
date: 2026-07-08
description: 'Hướng dẫn thư viện chỉnh sửa ảnh Java: học cách cắt ảnh bằng Aspose.PSD
  cho Java, thay đổi kích thước, mở rộng canvas và chuyển đổi PSD sang JPEG.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: Mở rộng và Cắt ảnh
og_description: Hướng dẫn thư viện chỉnh sửa ảnh Java cho thấy cách cắt, mở rộng canvas
  và chuyển đổi PSD sang JPEG bằng Aspose.PSD cho Java trong vài phút.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Thư viện chỉnh sửa ảnh Java – Cắt ảnh với Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Thư viện chỉnh sửa ảnh Java – Cắt ảnh với Aspose.PSD
url: /vi/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thư viện chỉnh sửa ảnh Java: Cắt ảnh Java với Aspose.PSD

## Giới thiệu

## Câu trả lời nhanh
- **Thư viện nào xử lý cắt ảnh java?** Aspose.PSD for Java.  
- **Tôi có cần giấy phép để phát triển không?** Bản dùng thử miễn phí hoạt động cho việc kiểm tra; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Tôi có thể chuyển đổi PSD sang JPEG trong khi cắt không?** Có, sử dụng `JpegOptions` cùng với một hình chữ nhật cắt.  
- **Java 8 có được hỗ trợ không?** Aspose.PSD hỗ trợ Java 8 và các phiên bản mới hơn.  
- **Thời gian thực hiện khoảng bao lâu?** Thông thường dưới 10 phút cho một thao tác cắt cơ bản.

## “crop image java” là gì?

Cắt ảnh java có nghĩa là chọn một vùng hình chữ nhật của ảnh nguồn và loại bỏ mọi thứ nằm ngoài vùng đó. Với Aspose.PSD, bạn tạo một `Rectangle` xác định khu vực, áp dụng nó cho một `RasterImage`, và sau đó lưu kết quả ở bất kỳ định dạng được hỗ trợ nào như JPEG.

## Tại sao nên sử dụng Aspose.PSD cho việc cắt ảnh Java?

Aspose.PSD cung cấp một **java image editing library** xử lý các tệp PSD một cách nguyên bản, hỗ trợ hơn 100 tính năng lớp, và có thể xử lý ảnh lên tới 10 000 × 10 000 pixel trong khi giữ mức sử dụng bộ nhớ dưới 500 MB. Nó cũng cung cấp khả năng chuyển đổi tích hợp sang JPEG, PNG, BMP và nhiều định dạng khác, mà không cần công cụ bên ngoài. Điều này làm cho các pipeline xử lý hàng loạt nhanh, đáng tin cậy và dễ bảo trì.

## Yêu cầu trước

1. **Java Development Kit (JDK)** – Java 8 hoặc phiên bản mới hơn đã được cài đặt.  
2. **Aspose.PSD for Java** – tải thư viện từ trang chính thức **[here](https://releases.aspose.com/psd/java/)**.  

> **Mẹo chuyên nghiệp:** Thêm file JAR Aspose.PSD vào classpath của dự án hoặc các phụ thuộc Maven/Gradle để tránh `ClassNotFoundException`.

## Nhập gói

Thêm các import cần thiết vào file nguồn Java của bạn. Các lớp này cho phép bạn truy cập vào việc tải ảnh, thao tác raster, định nghĩa hình chữ nhật và các tùy chọn xuất JPEG.

## Cách cắt ảnh Java bằng Aspose.PSD?

Tải PSD nguồn bằng `RasterImage`, xác định một `Rectangle` mô tả khu vực cắt (tọa độ âm có thể mở rộng canvas), và cuối cùng lưu kết quả bằng `JpegOptions`. Quy trình ba bước này xử lý cả việc cắt và chuyển đổi định dạng trong một lần, loại bỏ nhu cầu tạo file trung gian.

## Bước 1: Đặt thư mục tài liệu của bạn

Xác định thư mục chứa tệp PSD nguồn. Thay thế placeholder bằng đường dẫn thực tế trên máy của bạn.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Bước 2: Xác định đường dẫn nguồn và đích

Xác định nơi đọc PSD và nơi ghi JPEG đã cắt.

```java
String dataDir = "Your Document Directory";
```

## Bước 3: Tải và lưu bộ nhớ đệm ảnh

`RasterImage` đại diện cho phiên bản raster của tệp PSD trong bộ nhớ.  
Tải PSD vào một đối tượng `RasterImage`. Lưu vào bộ nhớ đệm cải thiện hiệu suất cho các thao tác tiếp theo như cắt.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Bước 4: Tạo Rectangle để cắt

`Rectangle` xác định tọa độ X, Y và chiều rộng/chiều cao của vùng cắt.  
Tạo một `Rectangle` mô tả khu vực bạn muốn giữ lại. Các tọa độ có thể là âm để **mở rộng** canvas trước khi cắt, điều này hữu ích để thêm viền quanh ảnh gốc.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **Tại sao sử dụng tọa độ âm?**  
> Giá trị X/Y âm dịch vùng cắt sang trái/lên trên, thực tế thêm không gian trống (mở rộng) quanh nội dung gốc trước khi cắt cuối cùng.

## Bước 5: Lưu ảnh đã cắt

`JpegOptions` chỉ định các cài đặt cho đầu ra JPEG, như chất lượng và nén.  
Cuối cùng, lưu ảnh kết quả bằng `JpegOptions`. Bước này cũng minh họa **convert psd jpeg** trong khi áp dụng hình chữ nhật cắt.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Kết quả:** `jpeg_out.jpg` hiện chứa một ảnh 300 × 300 pixel đã được mở rộng 200 px ở mỗi phía và sau đó được cắt theo hình chữ nhật đã định nghĩa.

Chúc mừng! Bạn đã thực hiện thành công **java image cropping**, mở rộng canvas, và chuyển đổi tệp PSD sang JPEG—tất cả trong vài dòng mã ngắn gọn.

## Các trường hợp sử dụng phổ biến

- **Chuẩn bị tài nguyên cho web** – cắt và thay đổi kích thước ảnh chụp màn hình hoặc thiết kế trước khi tải lên.  
- **Tạo thumbnail** – trích xuất một vùng cụ thể từ PSD lớn để hiển thị trước.  
- **Xử lý hàng loạt tự động** – lặp qua thư mục chứa các tệp PSD, áp dụng cùng một hình chữ nhật cắt cho mỗi tệp.

## Khắc phục sự cố & Mẹo

| Vấn đề | Giải pháp đề xuất |
|-------|-------------------|
| `OutOfMemoryError` khi tải PSD lớn | Gọi `rasterImage.cacheData()` sớm và cân nhắc tăng kích thước heap JVM (`-Xmx`). |
| Vùng cắt lệch trung tâm | Kiểm tra các offset X/Y của rectangle; nhớ rằng giá trị âm mở rộng canvas. |
| JPEG đầu ra bị mờ | Điều chỉnh cài đặt chất lượng của `JpegOptions` (ví dụ, `new JpegOptions { Quality = 90 }`). |

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.PSD có tương thích với các phiên bản Java khác nhau không?

A1: Có, Aspose.PSD hỗ trợ Java 8, 11, 17 và các phiên bản mới hơn, đảm bảo tính tương thích rộng rãi trên các môi trường phát triển.

### Câu hỏi 2: Tôi có thể sử dụng Aspose.PSD cho dự án thương mại không?

A2: Chắc chắn, Aspose.PSD cung cấp giấy phép thương mại cho các nhà phát triển, cho phép sử dụng trong cả ứng dụng cá nhân và thương mại.

### Câu hỏi 3: Có bất kỳ hạn chế nào về các định dạng tệp ảnh được hỗ trợ không?

A3: Aspose.PSD hỗ trợ hơn 30 định dạng ảnh, bao gồm PSD, JPEG, PNG, BMP, TIFF và nhiều hơn nữa. Tham khảo [documentation](https://reference.aspose.com/psd/java/) để xem danh sách đầy đủ.

### Câu hỏi 4: Làm sao tôi có thể nhận hỗ trợ cho các câu hỏi liên quan đến Aspose.PSD?

A4: Truy cập [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) để tìm sự trợ giúp từ cộng đồng hoặc đội ngũ hỗ trợ của Aspose.

### Câu hỏi 5: Có bản dùng thử miễn phí không?

A5: Có, bạn có thể khám phá Aspose.PSD với bản dùng thử miễn phí. Tải về [here](https://releases.aspose.com/).

---

**Cập nhật lần cuối:** 2026-07-08  
**Được kiểm tra với:** Aspose.PSD for Java 24.12  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## Hướng dẫn liên quan

- [Thay đổi kích thước đơn giản với Aspose.PSD – Thư viện xử lý ảnh Java](/psd/java/basic-image-operations/simple-resizing/)
- [Cách xoay ảnh 270 độ với Aspose.PSD cho Java](/psd/java/advanced-image-manipulation/rotate-image/)
- [Cách điều chỉnh Gamma trong xử lý ảnh Java với Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}