---
title: Tạo hình thu nhỏ từ tệp PSD bằng Java
linktitle: Tạo hình thu nhỏ từ tệp PSD bằng Java
second_title: API Java Aspose.PSD
description: Tìm hiểu cách dễ dàng tạo hình thu nhỏ từ tệp PSD bằng Java và Aspose.PSD. Hãy làm theo hướng dẫn từng bước của chúng tôi để xử lý hình ảnh liền mạch.
weight: 24
url: /vi/java/modifying-converting-psd-images/create-thumbnails-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo hình thu nhỏ từ tệp PSD bằng Java

## Giới thiệu
Trong thế giới thiết kế đồ họa, việc làm việc với các tệp PSD (Tài liệu Photoshop) là điều bình thường. Cho dù bạn là nhà phát triển dày dạn kinh nghiệm, nhà thiết kế đồ họa hay chỉ là người muốn tìm hiểu sâu về xử lý hình ảnh, việc tạo hình thu nhỏ từ tệp PSD có thể giúp bạn tiết kiệm thời gian và hợp lý hóa quy trình làm việc của mình. Hướng dẫn này sẽ hướng dẫn bạn trong toàn bộ quá trình sử dụng Aspose.PSD cho Java. Aspose.PSD không chỉ là một thư viện mạnh mẽ để quản lý các tệp Photoshop mà còn giúp công việc này trở nên trực quan và dễ quản lý. Bạn đã sẵn sàng tìm hiểu cách tạo hình thu nhỏ từ tệp PSD một cách hiệu quả chưa?
## Điều kiện tiên quyết
Trước khi đi sâu vào nội dung cơ bản của việc tạo hình thu nhỏ, hãy cùng tìm hiểu những gì bạn cần để bắt đầu.
### Môi trường phát triển Java
-  Java JDK: Đảm bảo bạn đã cài đặt Bộ công cụ phát triển Java (JDK) trên máy tính của mình. Bạn có thể tải nó xuống[đây](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- IDE: Môi trường phát triển tích hợp (IDE) như IntelliJ IDEA, Eclipse hoặc NetBeans sẽ giúp việc viết mã dễ dàng hơn.
### Thư viện Aspose.PSD
- Bạn cần đưa thư viện Aspose.PSD vào dự án của mình. bạn có thể[tải phiên bản mới nhất tại đây](https://releases.aspose.com/psd/java/).
### Kiến thức cơ bản về Java
- Việc làm quen với các khái niệm cơ bản về Java sẽ giúp bạn điều hướng qua mã ví dụ hiệu quả hơn. Các khái niệm như lớp, đối tượng và vòng lặp sẽ được sử dụng thường xuyên.
## Gói nhập khẩu
Bắt đầu bằng cách nhập các lớp cần thiết từ thư viện Aspose.PSD. Bước này rất quan trọng vì nó cho phép bạn tận dụng các chức năng của thư viện trong mã của mình.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
Với những điều kiện tiên quyết đã sẵn sàng, hãy bắt đầu sự kiện chính! Tạo hình thu nhỏ từ tệp PSD bao gồm một số bước đơn giản và tôi sẽ chia nhỏ cho bạn.
## Bước 1: Thiết lập môi trường của bạn
Đây là cách bắt đầu dự án của bạn và chuẩn bị cho việc tạo hình thu nhỏ.
1. Tạo một dự án Java:
   - Mở IDE của bạn và tạo một dự án Java mới.
   - Đặt tên nó là "PsdThumbnailGenerator".
2. Bao gồm Thư viện Aspose.PSD:
   -  Thêm tệp JAR Aspose.PSD vào đường dẫn xây dựng dự án của bạn. Nếu bạn đang sử dụng Maven, hãy đưa nó vào`pom.xml`:
     ```xml
     <dependency>
         <groupId>com.aspose</groupId>
         <artifactId>aspose-psd</artifactId>
         <version>your_version_here</version>
     </dependency>
     ```
## Bước 2: Tải tệp PSD
Tiếp theo, chúng ta cần tải tệp PSD mà chúng ta muốn tạo hình thu nhỏ. 
1. Chỉ định thư mục tài liệu của bạn:
   Xác định thư mục chứa tệp PSD của bạn.
   ```java
   String dataDir = "Your Document Directory"; // Thay thế bằng đường dẫn của bạn
   ```
2. Tải tệp PSD:
    Sử dụng`PsdImage` class để tải tệp PSD của bạn.
   ```java
   PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
   ```
 Đây,`sample.psd` là tên tệp PSD của bạn. Điều chỉnh điều này theo tên tập tin của bạn.
## Bước 3: Lặp lại tài nguyên PSD
Bây giờ chúng ta đã tải xong hình ảnh PSD, bước tiếp theo là kiểm tra tài nguyên của nó.
1. Nhận số lượng tài nguyên:
   Chúng tôi sẽ lặp qua tất cả các tài nguyên trong tệp PSD.
   ```java
   for (int i = 0; i < image.getImageResources().length; i++) {
       // Xử lý tài nguyên
   }
   ```
   
2. Xác định tài nguyên hình thu nhỏ:
   Bên trong vòng lặp, kiểm tra xem tài nguyên có phải là hình thu nhỏ hay không.
   ```java
   if (image.getImageResources()[i] instanceof ThumbnailResource) {
       // Xử lý hình thu nhỏ
   }
   ```
## Bước 4: Xử lý hình thu nhỏ
Sau khi xác định được tài nguyên hình thu nhỏ, chúng tôi sẽ cần xử lý tài nguyên đó cho phù hợp.
1. Truy xuất và kiểm tra định dạng hình thu nhỏ:
   Nếu tài nguyên thực sự là hình thu nhỏ, hãy truy xuất nó và kiểm tra định dạng của nó.
   ```java
   ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
   if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
       // Tạo và lưu hình thu nhỏ
   }
   ```
## Bước 5: Tạo và lưu hình thu nhỏ
Đây là nơi phép thuật xảy ra! Chúng tôi sẽ tạo một hình ảnh mới từ dữ liệu hình thu nhỏ và lưu nó.
1. Tạo một hình ảnh mới:
   Chúng tôi sẽ sử dụng chiều rộng và chiều cao của tài nguyên hình thu nhỏ để tạo hình ảnh bitmap mới.
   ```java
   PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
   ```
2. Lưu trữ pixel trong hình ảnh mới:
   Chuyển dữ liệu hình thu nhỏ sang hình ảnh mới tạo.
   ```java
   thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
   ```
3. Lưu hình ảnh thu nhỏ:
   Cuối cùng, lưu hình ảnh thu nhỏ vào thư mục tài liệu của bạn với một tên duy nhất.
   ```java
   thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
   ```

## Phần kết luận
Tạo hình thu nhỏ từ các tệp PSD bằng Java và Aspose.PSD có thể là một nhiệm vụ đơn giản khi bạn chia nó thành các bước có thể quản lý được. Với hướng dẫn này, giờ đây bạn có khả năng trích xuất hình thu nhỏ từ các tệp PSD một cách dễ dàng, cung cấp cho bạn một công cụ tiện lợi để nâng cao quy trình làm việc của bạn. Vậy điều gì đang ngăn cản bạn? Hãy nhanh tay sở hữu một số tệp PSD và dùng thử!
## Câu hỏi thường gặp
### Aspose.PSD là gì?
Aspose.PSD là một thư viện Java cho phép các nhà phát triển làm việc với các tệp Photoshop, giúp thao tác và quản lý các tệp PSD theo chương trình dễ dàng hơn.
### Tôi có thể sử dụng Aspose.PSD miễn phí không?
Có, Aspose cung cấp bản dùng thử miễn phí mà bạn có thể sử dụng để kiểm tra thư viện trước khi mua giấy phép.
### Tôi có thể lưu hình thu nhỏ ở định dạng nào?
Trong ví dụ này, chúng tôi đã lưu hình thu nhỏ ở định dạng BMP, nhưng Aspose.PSD cũng hỗ trợ nhiều định dạng khác.
### Tôi có cần cài đặt Photoshop để sử dụng Aspose.PSD không?
Không, Aspose.PSD hoạt động độc lập với Photoshop.
### Tôi có thể tìm thêm thông tin về Aspose.PSD ở đâu?
 Bạn có thể kiểm tra[Tài liệu Aspose.PSD](https://reference.aspose.com/psd/java/) để biết thêm chi tiết, hướng dẫn và tài nguyên.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
