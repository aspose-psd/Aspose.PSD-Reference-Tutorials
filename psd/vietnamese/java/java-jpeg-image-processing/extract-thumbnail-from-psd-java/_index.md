---
title: Trích xuất hình thu nhỏ từ PSD trong Java
linktitle: Trích xuất hình thu nhỏ từ PSD trong Java
second_title: API Java Aspose.PSD
description: Tìm hiểu cách trích xuất hình thu nhỏ từ tệp PSD bằng Aspose.PSD cho Java. Hướng dẫn từng bước này bao gồm mọi thứ từ thiết lập đến lưu hình ảnh được trích xuất.
weight: 15
url: /vi/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Trích xuất hình thu nhỏ từ PSD trong Java

## Giới thiệu
Trong hướng dẫn này, chúng ta sẽ khám phá cách trích xuất hình thu nhỏ từ tệp PSD bằng Aspose.PSD cho Java. Hình thu nhỏ có thể hữu ích để xem trước nhanh hoặc tạo các phiên bản hình ảnh nhỏ hơn được nhúng trong tài liệu PSD. Hãy đi sâu vào các bước cần thiết để đạt được điều này bằng Aspose.PSD.
## Điều kiện tiên quyết
Trước khi chúng tôi bắt đầu, hãy đảm bảo bạn đã thiết lập sau:
- Bộ công cụ phát triển Java (JDK) được cài đặt trên hệ thống của bạn.
-  Aspose.PSD cho thư viện Java. Bạn có thể tải nó xuống từ[đây](https://releases.aspose.com/psd/java/).
- Kiến thức cơ bản về lập trình Java.
## Gói nhập khẩu
Để bắt đầu, hãy đưa gói Aspose.PSD cần thiết vào lớp Java của bạn:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Bước 1: Tải tệp PSD
Đầu tiên, tải tệp PSD chứa hình thu nhỏ bạn muốn trích xuất.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Thay thế`"Your_Document_Directory/"` với đường dẫn thư mục chứa tệp PSD của bạn và`"your_file.psd"` với tên tệp PSD của bạn.
## Bước 2: Lặp lại tài nguyên hình ảnh
Lặp lại các tài nguyên hình ảnh để tìm tài nguyên hình thu nhỏ.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Trích xuất dữ liệu hình thu nhỏ
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Tạo một hình ảnh mới với dữ liệu hình thu nhỏ được trích xuất
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Lưu hình thu nhỏ được trích xuất dưới dạng tệp JPEG riêng
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Xuất thông báo thành công
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Thoát khỏi vòng lặp sau khi tìm thấy và xử lý hình thu nhỏ
    }
}
```
## Bước 3: Lưu hình thu nhỏ được trích xuất
Lưu hình thu nhỏ được trích xuất dưới dạng tệp hình ảnh riêng biệt (trong trường hợp này là tệp JPEG).
## Bước 4: Xử lý các loại hình thu nhỏ khác nhau
 Nếu tệp PSD của bạn có thể chứa nhiều loại hình thu nhỏ, chẳng hạn như`Thumbnail4Resource`, bạn có thể mở rộng logic để xử lý các trường hợp đó một cách tương tự.

## Phần kết luận
Trong hướng dẫn này, chúng tôi đã khám phá cách trích xuất hình thu nhỏ từ tệp PSD bằng Aspose.PSD cho Java. Bằng cách làm theo các bước được nêu ở trên, bạn có thể truy xuất và lưu hình thu nhỏ được nhúng trong tài liệu PSD của mình một cách hiệu quả.

## Câu hỏi thường gặp
### Aspose.PSD là gì?
Aspose.PSD là thư viện Java cho phép các nhà phát triển làm việc với PSD và các định dạng tệp hình ảnh khác theo chương trình.
### Tôi có thể tìm thêm tài liệu về Aspose.PSD cho Java ở đâu?
 Bạn có thể tham khảo các[tài liệu](https://reference.aspose.com/psd/java/) để biết các ví dụ và tài liệu tham khảo API chi tiết.
### Tôi có thể dùng thử Aspose.PSD miễn phí trước khi mua không?
 Có, bạn có thể tải xuống một[dùng thử miễn phí](https://releases.aspose.com/) để đánh giá năng lực của thư viện.
### Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.PSD?
 Giấy phép tạm thời có thể được lấy từ[đây](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD có phù hợp cho mục đích thương mại không?
Có, Aspose.PSD có thể được sử dụng cho cả dự án cá nhân và thương mại theo điều khoản cấp phép.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
