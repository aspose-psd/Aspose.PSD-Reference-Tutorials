---
date: 2026-10-03
description: Tìm hiểu cách trích xuất thumbnail từ PSD trong Java bằng Aspose.PSD.
  Hướng dẫn từng bước này bao gồm cài đặt, các đoạn mã mẫu và lưu thumbnail dưới dạng
  ảnh JPEG.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: Trích xuất thumbnail từ PSD trong Java
og_description: Tìm hiểu cách trích xuất thumbnail từ PSD trong Java với Aspose.PSD.
  Hướng dẫn này sẽ đưa bạn qua các bước cài đặt, tải tệp, trích xuất thumbnail và
  lưu nó dưới dạng ảnh JPEG.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Trích xuất thumbnail từ PSD trong Java bằng Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: Trích xuất thumbnail từ PSD trong Java
url: /vi/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Trích xuất thumbnail từ PSD trong Java

## Giới thiệu
Việc trích xuất thumbnail từ tệp PSD cho phép bạn tạo các bản xem trước nhanh chóng mà không cần tải toàn bộ hình ảnh độ phân giải cao. Trong Java, Aspose.PSD làm cho quá trình này trở nên đơn giản và hiệu suất cao. Trong hướng dẫn này, bạn sẽ học cách thiết lập thư viện, xác định tài nguyên thumbnail, và lưu nó dưới dạng tệp JPEG — chỉ với vài dòng mã.

## Câu trả lời nhanh
- **Thư viện nào xử lý thumbnail PSD?** Aspose.PSD for Java.
- **Cần bao nhiêu dòng mã?** Khoảng năm dòng để tải, trích xuất và lưu.
- **Có thể trích xuất thumbnail từ các tệp PSD lớn không?** Có, Aspose.PSD xử lý các tệp lên tới 500 MB mà không cần tải toàn bộ bộ nhớ.
- **Có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí đủ cho việc đánh giá; giấy phép bắt buộc cho môi trường sản xuất.
- **Các định dạng đầu ra được hỗ trợ?** Thumbnail đã trích xuất có thể lưu dưới dạng JPEG, PNG hoặc BMP.

## Thumbnail PSD là gì?
Trích xuất thumbnail từ PSD là quá trình đọc hình ảnh xem trước nhỏ được nhúng bên trong tài liệu Photoshop (PSD). Bản xem trước này được lưu dưới dạng tài nguyên và có thể được lưu độc lập để lập danh mục hoặc hiển thị. Thumbnail thường là hình ảnh độ phân giải thấp, được các ứng dụng sử dụng để hiển thị nhanh một bản tóm tắt trực quan mà không cần tải toàn bộ hình ảnh gốc.

## Tại sao nên dùng Aspose.PSD cho nhiệm vụ này?
Aspose.PSD hỗ trợ **hơn 30 định dạng ảnh** và có thể xử lý các tệp PSD lên tới **500 MB** trong khi tiêu thụ bộ nhớ thấp vì nó chỉ đọc tài nguyên khi cần. API cũng cung cấp cơ chế xử lý lỗi mạnh mẽ, cho phép bạn trích xuất thumbnail một cách đáng tin cậy ngay cả khi tệp bị hỏng.

## Yêu cầu trước
Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:
- Java Development Kit (JDK) được cài đặt.
- Thư viện Aspose.PSD for Java tải về từ [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/).
- Kiến thức cơ bản về cú pháp Java và cách thiết lập dự án.

## Làm thế nào để trích xuất thumbnail từ tệp PSD trong Java?
Tải tệp PSD bằng `PsdImage`, xác định `ThumbnailResource`, và lưu dữ liệu ảnh của nó dưới dạng JPEG. Aspose.PSD ẩn đi việc phân tích cấp thấp, vì vậy bạn chỉ cần gọi `getResources()` rồi `save()` trên ảnh đã trích xuất. Cách tiếp cận này hoạt động với bất kỳ PSD nào có thumbnail, bất kể kích thước tệp.

## Nhập các gói
`Image` là lớp cơ sở để tải ảnh. `PsdImage` đại diện cho tài liệu PSD. `ThumbnailResource` và `Thumbnail4Resource` đại diện cho các tài nguyên thumbnail. `JpegOptions` chỉ định các tùy chọn lưu JPEG.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## Bước 1: tải tệp PSD
Đầu tiên, tạo một thể hiện `PsdImage` trỏ tới tệp PSD của bạn. Hàm khởi tạo chỉ đọc phần đầu và các tài nguyên cần thiết, giữ mức tiêu thụ bộ nhớ tối thiểu.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

Thay thế `"Your_Document_Directory/"` bằng đường dẫn thư mục chứa tệp PSD của bạn, và `"your_file.psd"` bằng tên tệp PSD của bạn.

## Bước 2: lặp qua các tài nguyên ảnh
Aspose.PSD lưu thumbnail dưới dạng đối tượng `ThumbnailResource` trong bộ sưu tập tài nguyên của ảnh. Duyệt qua bộ sưu tập, kiểm tra kiểu tài nguyên, và lấy thumbnail đầu tiên bạn gặp.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Trích xuất dữ liệu thumbnail
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Tạo ảnh mới với dữ liệu thumbnail đã trích xuất
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Lưu thumbnail đã trích xuất thành tệp JPEG riêng biệt
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // In thông báo thành công
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Thoát vòng lặp sau khi tìm và xử lý thumbnail
    }
}
```
```

## Bước 3: lưu thumbnail đã trích xuất
Khi đã có ảnh thumbnail, gọi phương thức `save` của nó để ghi ra đĩa. Bạn có thể chọn JPEG, PNG hoặc BMP; JPEG là phổ biến nhất cho các bản xem trước trên web.

## Bước 4: xử lý các loại thumbnail khác nhau
Nếu một PSD chứa nhiều biến thể thumbnail, chẳng hạn `Thumbnail4Resource`, mở rộng logic lặp để kiểm tra từng loại. API cung cấp các lớp riêng cho mỗi tài nguyên, cho phép bạn chọn độ phân giải cần thiết.

## Các vấn đề thường gặp và giải pháp
- **Không tìm thấy thumbnail:** Không phải tất cả các tệp PSD đều nhúng bản xem trước. Kiểm tra tệp nguồn trong bảng “File → File Info” của Photoshop.
- **Lỗi định dạng không hỗ trợ:** Đảm bảo bạn đang dùng phiên bản Aspose.PSD mới nhất; các bản cũ có thể không nhận diện được các loại tài nguyên thumbnail mới.
- **Thiếu bộ nhớ khi xử lý tệp lớn:** Sử dụng `PsdImage.load(..., LoadOptions)` với `LoadOptions.setLoadResourcesOnly(true)` để tránh tải toàn bộ dữ liệu ảnh khi chỉ cần thumbnail.

## Câu hỏi thường gặp

**Q: Aspose.PSD là gì?**  
A: Aspose.PSD là một thư viện Java cho phép tạo, thao tác và chuyển đổi PSD cùng các định dạng ảnh raster khác một cách lập trình mà không cần Adobe Photoshop.

**Q: Tôi có thể tìm tài liệu chi tiết về Aspose.PSD for Java ở đâu?**  
A: Bạn có thể tham khảo [documentation](https://reference.aspose.com/psd/java/) để biết chi tiết API và các ví dụ.

**Q: Tôi có thể dùng thử Aspose.PSD miễn phí trước khi mua không?**  
A: Có, bạn có thể tải về một [free trial](https://releases.aspose.com/) để đánh giá khả năng của thư viện.

**Q: Làm sao để lấy giấy phép tạm thời cho Aspose.PSD?**  
A: Giấy phép tạm thời có sẵn tại trang [temporary license](https://purchase.aspose.com/temporary-license/).

**Q: Aspose.PSD có phù hợp cho mục đích thương mại không?**  
A: Có, Aspose.PSD có thể được sử dụng trong cả dự án cá nhân và thương mại theo các điều khoản cấp phép của nó.

---

**Cập nhật lần cuối:** 2026-10-03  
**Đã kiểm tra với:** Aspose.PSD for Java 24.12  
**Tác giả:** Aspose

## Các hướng dẫn liên quan

- [Cách chuyển đổi PSD sang các định dạng ảnh raster với Aspose.PSD cho Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Lưu PSD dưới dạng JPEG và hỗ trợ màu RGB với Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Thay đổi kích thước ảnh với Aspose.PSD cho Java – Vẽ hình và các thao tác ảnh cơ bản](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}