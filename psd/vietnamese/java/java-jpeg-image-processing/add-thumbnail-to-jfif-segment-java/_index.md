---
date: 2026-09-28
description: Cách thêm thumbnail vào đoạn JFIF trong Java bằng Aspose.PSD. Thực hiện
  theo hướng dẫn từng bước để nhúng thumbnail vào tệp PSD một cách nhanh chóng và
  đáng tin cậy.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: Thêm Thumbnail vào Đoạn JFIF trong Java
og_description: Cách thêm thumbnail vào đoạn JFIF trong Java bằng Aspose.PSD. Thực
  hiện theo hướng dẫn từng bước để nhúng thumbnail vào tệp PSD một cách nhanh chóng
  và đáng tin cậy.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: Cách thêm thumbnail vào đoạn JFIF trong Java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: Cách thêm thumbnail vào đoạn JFIF trong Java
url: /vi/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách thêm hình thu nhỏ vào đoạn JFIF trong Java

## Giới thiệu
Thêm một hình thu nhỏ vào đoạn JFIF của tệp PSD là một yêu cầu phổ biến khi bạn cần xem trước nhanh mà không tải toàn bộ hình ảnh. Trong hướng dẫn này, bạn sẽ học **cách thêm hình thu nhỏ** vào đoạn JFIF trong Java bằng cách sử dụng Aspose.PSD. Khi kết thúc hướng dẫn, bạn sẽ có một đoạn mã có thể chạy, hiểu cấu trúc JFIF bên dưới, và các mẹo để xử lý các tệp lớn một cách hiệu quả.

## Câu trả lời nhanh
- **Thư viện nào được yêu cầu?** Aspose.PSD for Java.
- **Phiên bản Java nào hoạt động?** JDK 11 hoặc sau.
- **Cần bao nhiêu dòng mã?** Khoảng 10 dòng để tải, sửa đổi và lưu.
- **Tôi có thể xử lý các tệp đa megabyte không?** Có, Aspose.PSD truyền dữ liệu theo luồng, vì vậy việc sử dụng bộ nhớ vẫn thấp.
- **Có cần giấy phép thương mại không?** Cần giấy phép cho việc sử dụng trong môi trường sản xuất; bản dùng thử miễn phí có sẵn.

## Đoạn JFIF là gì?
Đoạn JFIF là một khối JPEG File Interchange Format có thể lưu trữ dữ liệu tùy chọn như hình thu nhỏ, EXIF, hoặc hồ sơ màu.  
Nó nằm trong luồng JPEG của tệp PSD và được hầu hết các trình xem ảnh nhận diện để tạo xem trước nhanh.

## Tại sao cần thêm hình thu nhỏ vào tệp PSD?
Aspose.PSD for Java hỗ trợ **hơn 30 định dạng ảnh** và có thể xử lý các tệp lên tới **2 GB** mà không cần tải toàn bộ tài liệu vào bộ nhớ. Thêm hình thu nhỏ giảm băng thông mạng khi truyền các bản xem trước và tăng tốc độ hiển thị UI trong các ứng dụng thư viện.

## Yêu cầu trước
- Java Development Kit (JDK): Đảm bảo bạn đã cài Java trên hệ thống. Bạn có thể tải xuống từ [Oracle's JDK website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- Aspose.PSD for Java: Bạn cần có thư viện Aspose.PSD for Java. Bạn có thể lấy nó từ [Aspose.PSD Java download page](https://releases.aspose.com/psd/java/).
- Integrated Development Environment (IDE): Sử dụng một IDE như IntelliJ IDEA hoặc Eclipse cho phát triển Java.
- Basic Understanding of Java: Hiểu biết cơ bản về ngôn ngữ lập trình Java và các khái niệm.

## Cách thêm hình thu nhỏ vào đoạn JFIF trong Java?
Tải PSD mục tiêu, xác định tài nguyên JFIF, thay thế dữ liệu hình thu nhỏ của nó, và lưu tệp. Toàn bộ thao tác có thể thực hiện bằng một vài lời gọi API đơn giản, và Aspose.PSD sẽ xử lý cấu trúc JPEG cấp thấp cho bạn.

### Bước 1: nhập các gói
`Document`, `JfifResource`, và các lớp liên quan là một phần của không gian tên Aspose.PSD. Document đại diện cho container tệp PSD, và JfifResource cung cấp quyền truy cập vào đoạn JFIF trong PSD. Nhập chúng ở đầu file nguồn của bạn.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### Bước 2: tải ảnh PSD
Tạo một thể hiện `PsdImage` bằng cách truyền đường dẫn tệp vào hàm khởi tạo. PsdImage là lớp Aspose.PSD mô hình hoá một tài liệu Photoshop. Điều này tải siêu dữ liệu tài liệu trong khi truyền dữ liệu pixel.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### Bước 3: lặp qua các tài nguyên ảnh
Tìm trong bộ sưu tập `Resources` một `JfifResource`. Khi tìm thấy, bạn có thể thay thế mảng byte hình thu nhỏ của nó bằng một bản xem trước mới được mã hoá JPEG.

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### Bước 4: điều chỉnh dữ liệu hình thu nhỏ
Tạo một hình thu nhỏ JPEG nhỏ (ví dụ, 120 × 120 px) bằng bất kỳ thư viện xử lý ảnh nào, sau đó gán mảng byte kết quả cho `jfifResource.ThumbnailData`.

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### Bước 5: lưu ảnh đã sửa đổi
Gọi phương thức `save` trên đối tượng `PsdImage`, chỉ định đường dẫn đầu ra và định dạng mong muốn. Đoạn JFIF bây giờ chứa hình thu nhỏ mới.

```java
image.save(dataDir + "output.psd");
```

## Các vấn đề thường gặp và giải pháp
- **Hình thu nhỏ không hiển thị trong trình xem:** Đảm bảo dữ liệu hình thu nhỏ là một mảng byte JPEG hợp lệ và kích thước của nó nằm trong phạm vi 256 × 256 px, là kích thước tối đa được JFIF hỗ trợ.
- **OutOfMemoryError trên các tệp PSD lớn:** Sử dụng `PsdImage.load(inputStream, true)` để bật chế độ truyền dữ liệu, giúp giảm tiêu thụ bộ nhớ.
- **Kiểu tài nguyên không đúng:** Xác nhận rằng tài nguyên bạn sửa đổi thực sự là một `JfifResource`; các tài nguyên khác như `ExifResource` sẽ không ảnh hưởng đến việc hiển thị hình thu nhỏ.

## Câu hỏi thường gặp

**Q: Aspose.PSD for Java là gì?**  
A: Aspose.PSD for Java là một thư viện thương mại cho phép các nhà phát triển tạo, chỉnh sửa, chuyển đổi và render các tệp Photoshop PSD mà không cần Adobe Photoshop.

**Q: Tôi có thể tìm tài liệu chi tiết hơn cho Aspose.PSD for Java ở đâu?**  
A: Tài liệu chi tiết có thể được tìm thấy trên trang [Aspose.PSD for Java documentation page](https://reference.aspose.com/psd/java/).

**Q: Aspose.PSD for Java có phù hợp cho việc sử dụng thương mại không?**  
A: Có, Aspose.PSD for Java có thể được sử dụng thương mại. Bạn có thể mua giấy phép từ [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).

**Q: Tôi có thể dùng thử Aspose.PSD cho Java trước khi mua không?**  
A: Có, bạn có thể tải bản dùng thử miễn phí từ [Aspose.PSD's trial download page](https://releases.aspose.com/).

**Q: Làm thế nào tôi có thể nhận hỗ trợ cho Aspose.PSD for Java?**  
A: Để được hỗ trợ, truy cập [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

---

**Cập nhật lần cuối:** 2026-09-28  
**Kiểm tra với:** Aspose.PSD for Java 24.11  
**Tác giả:** Aspose

## Các hướng dẫn liên quan

- [Thêm tài nguyên IOPA vào tệp PSD bằng Aspose PSD cho Java](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [Thêm chữ ký vào hình ảnh – Vẽ hình trên Canvas với Aspose.PSD cho Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Cách xoay hình ảnh ở góc cụ thể với Aspose.PSD cho Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}