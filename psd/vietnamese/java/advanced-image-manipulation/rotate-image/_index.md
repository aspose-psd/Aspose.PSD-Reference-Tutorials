---
date: 2026-05-19
description: Tìm hiểu cách chuyển đổi PSD sang JPEG và xoay ảnh 270 độ bằng Aspose.PSD
  cho Java. Hướng dẫn này chỉ ra cách xoay tệp PSD, lật ảnh và chuyển đổi PSD sang
  JPEG.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: Xoay Ảnh 270 Độ
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Chuyển đổi PSD sang JPEG & Xoay 270° với Aspose.PSD cho Java
url: /vi/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi PSD sang JPEG & Xoay ảnh 270 độ bằng Aspose.PSD cho Java

## Giới thiệu

Trong **hướng dẫn xử lý ảnh Java** này, bạn sẽ học cách **chuyển đổi PSD sang JPEG** đồng thời xoay ảnh 270 độ bằng Aspose.PSD cho Java. Dù bạn đang xây dựng một pipeline xử lý hàng loạt, một trình chỉnh sửa trên web, hay một tiện ích desktop, thư viện cho phép bạn thao tác các lớp PSD mà không cần Photoshop. Chúng tôi cũng sẽ đề cập đến việc lật ảnh tùy chọn và trình bày quy trình toàn diện từ việc tải tệp PSD đến lưu thành JPEG.

## Câu trả lời nhanh
- **Thư viện nào thực hiện việc xoay?** Aspose.PSD for Java  
- **Góc xoay mà ví dụ sử dụng là gì?** 270 độ  
- **Tôi có thể lật ảnh không?** Có – sử dụng các tùy chọn `RotateFlipType` như `Rotate90FlipX`  
- **Làm sao để lưu kết quả?** Trong ví dụ chúng tôi lưu dưới dạng JPEG bằng `JpegOptions`  
- **Có cần giấy phép cho môi trường sản xuất không?** Cần một giấy phép Aspose.PSD hợp lệ cho việc sử dụng thương mại  

## “Xoay ảnh 270 độ” là gì?
Xoay một ảnh 270 độ có nghĩa là quay bức tranh ba phần tư vòng tròn đầy theo chiều kim đồng hồ (hoặc 90 độ ngược chiều kim đồng hồ). Vị trí này thường khôi phục lại bố cục dọc gốc sau các biến đổi trước đó, và thường được sử dụng khi ảnh được chụp ở chế độ ngang nhưng cần hiển thị ở chế độ dọc. Kết quả là một hình ảnh được định hướng đúng mà không mất chất lượng.

## Tại sao nên dùng Aspose.PSD cho nhiệm vụ này?
Aspose.PSD hỗ trợ **hơn 50 định dạng đầu vào và đầu ra** — bao gồm PSD, JPEG, PNG, BMP, GIF và TIFF — và có thể xử lý các tệp lên tới **2 GB** mà không cần tải toàn bộ tài liệu vào bộ nhớ. API hoạt động trên bất kỳ môi trường Java nào (JDK 8+), không yêu cầu cài đặt Photoshop gốc, và cung cấp một lệnh `rotateFlip` duy nhất để thực hiện cả việc xoay và lật trong một bước.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn có:

- Thư viện **Aspose.PSD for Java** đã được cài đặt. Bạn có thể tải xuống và xem tài liệu tham khảo API đầy đủ [tại đây](https://reference.aspose.com/psd/java/).  
- Môi trường phát triển Java (JDK 8 trở lên).  
- Một tệp PSD mẫu mà bạn muốn xoay. Cập nhật biến `sourceFile` trong mã với đường dẫn đúng tới tệp của bạn.

## Nhập gói

Các lớp `Image`, `RotateFlipType` và `JpegOptions` cần thiết để tải, biến đổi và lưu tệp.  
`Image` là lớp cốt lõi đại diện cho tài liệu PSD trong bộ nhớ.  
`RotateFlipType` liệt kê các thao tác xoay và lật được hỗ trợ.  
`JpegOptions` cấu hình các thiết lập đầu ra JPEG như chất lượng.  

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Cách chuyển đổi PSD sang JPEG sau khi xoay?

Tải PSD nguồn, áp dụng xoay 270 độ, và ngay lập tức lưu nó dưới dạng JPEG. Quy trình ba bước này chạy dưới một giây cho các ảnh 10 MP điển hình trên CPU hiện đại, rất phù hợp cho các công việc batch có khối lượng lớn. Bằng cách chỉ xử lý dữ liệu ảnh cần thiết, mức tiêu thụ bộ nhớ giữ thấp, và JPEG kết quả vẫn giữ được độ trung thực hình ảnh trong khi giảm kích thước tệp.

### Bước 1: Tải tệp PSD

`Image` là lớp cốt lõi của Aspose.PSD đại diện cho một tài liệu PSD duy nhất trong bộ nhớ. Khi khởi tạo, nó chỉ đọc thông tin tiêu đề, giúp giảm mức sử dụng bộ nhớ.  

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Bước 2: Xoay ảnh 270 độ

`rotateFlip` thực hiện việc xoay đã chỉ định và tùy chọn lật trên ảnh. `RotateFlipType.Rotate270FlipNone` quay canvas 270 độ theo chiều kim đồng hồ trong khi giữ nguyên hướng ảnh.  

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Mẹo chuyên nghiệp:** Nếu bạn cũng cần lật ảnh theo chiều ngang hoặc chiều dọc, hãy chọn một `RotateFlipType` khác như `Rotate90FlipX` hoặc `Rotate180FlipY`.

### Bước 3: Chuyển đổi PSD sang JPEG và Lưu

`JpegOptions` định nghĩa các tham số đặc thù cho JPEG như chất lượng nén. Phương thức `save` ghi ảnh đã biến đổi ra đĩa ở định dạng mong muốn.  

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Tệp `RotatedImage_out.jpg` hiện chứa nội dung PSD gốc đã được xoay 270 độ và lưu dưới dạng JPEG.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **Ảnh hiển thị ngược** | Kiểm tra bạn đã sử dụng `Rotate270FlipNone`. Đối với xoay 90 độ theo chiều kim đồng hồ, hãy dùng `Rotate90FlipNone`. |
| **Tệp đầu ra bị hỏng** | Đảm bảo thư mục đích tồn tại và bạn có quyền ghi. |
| **Lỗi giấy phép** | Cài đặt giấy phép Aspose.PSD tạm thời hoặc vĩnh viễn trước khi tải ảnh trong môi trường sản xuất. |

## Câu hỏi thường gặp

**Q: Aspose.PSD có tương thích với các định dạng ảnh khác nhau không?**  
A: Có, Aspose.PSD hỗ trợ PSD, JPEG, PNG, BMP, GIF, TIFF và nhiều định dạng raster khác.

**Q: Tôi có thể áp dụng các góc xoay tùy chỉnh, không chỉ các lật đã định sẵn không?**  
A: Chắc chắn! Mặc dù `RotateFlipType` cung cấp các góc phổ biến, bạn có thể nối nhiều lời gọi hoặc sử dụng ma trận biến đổi cho các góc tùy ý.

**Q: Làm sao để chuyển đổi PSD đã xoay sang định dạng khác, chẳng hạn PNG?**  
A: Thay thế `JpegOptions` bằng `PngOptions` (hoặc lớp tùy chọn phù hợp) trong phương thức `save`.

**Q: Tôi có thể tìm hỗ trợ hoặc trợ giúp bổ sung ở đâu?**  
A: Để nhận trợ giúp cộng đồng, hãy truy cập [Diễn đàn Aspose.PSD](https://forum.aspose.com/c/psd/34).

**Q: Có bản dùng thử miễn phí không?**  
A: Có, bạn có thể khám phá Aspose.PSD với một [bản dùng thử miễn phí](https://releases.aspose.com/).

**Q: Làm sao để lấy giấy phép tạm thời?**  
A: Nếu bạn cần giấy phép tạm thời, bạn có thể lấy một [tại đây](https://purchase.aspose.com/temporary-license/).

**Cập nhật lần cuối:** 2026-05-19  
**Kiểm tra với:** Aspose.PSD for Java 24.12  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan

- [Chuyển đổi PSD sang các định dạng ảnh raster với Aspose.PSD cho Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Chuyển đổi PSD sang PNG và Xoay các lớp trong tệp PSD bằng Java](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Cách xoay ảnh trong Java với Aspose.PSD](/psd/java/advanced-image-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}