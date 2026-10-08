---
date: 2026-10-08
description: Tìm hiểu cách đọc thẻ EXIF trong Java bằng Aspose.PSD for Java (asp)
  qua hướng dẫn từng bước, và nâng cao khả năng xử lý ảnh của bạn.
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: Đọc thông tin thẻ EXIF cụ thể trong Java
og_description: Đọc thẻ EXIF, các nhà phát triển Java có thể nhanh chóng trích xuất
  siêu dữ liệu hình ảnh bằng Aspose.PSD. Hướng dẫn này sẽ chỉ cho bạn cách tải một
  tệp PSD, tìm tài nguyên thu nhỏ, và in ra các trường EXIF quan trọng như WhiteBalance
  và ISO speed.
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: Cách đọc thẻ EXIF trong Java với Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  headline: How to read EXIF tags in Java with Aspose.PSD
  type: TechArticle
- description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  name: How to read EXIF tags in Java with Aspose.PSD
  steps:
  - name: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
    text: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
    text: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
  - name: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
    text: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
  type: HowTo
- questions:
  - answer: Aspose.PSD (asp)
    question: What library reads EXIF data from PSD in Java?
  - answer: WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength,
      and more.
    question: Which tags can be extracted?
  - answer: Yes, a commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: The same API supports PNG, JPEG, TIFF via Java image metadata extraction.
    question: Can I use this with other image formats?
  - answer: About 10‑15 minutes for a basic read‑only scenario.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- read exif tags java
- Aspose.PSD
- java image metadata extraction
- EXIF extraction
- PSD processing
title: Cách đọc thẻ EXIF trong Java với Aspose.PSD
url: /vi/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đọc thông tin thẻ EXIF cụ thể trong Java với Aspose (asp)

## Giới thiệu
Nếu bạn cần **đọc thẻ EXIF trong Java**, Aspose.PSD (asp) cung cấp một API sạch, thuần Java hoạt động mà không cần Photoshop. Trong hướng dẫn này, bạn sẽ học cách trích xuất dữ liệu EXIF từ ảnh PSD, chọn chỉ những thẻ bạn quan tâm và in chúng ra console. Chúng tôi sẽ bao phủ mọi thứ từ việc thiết lập môi trường phát triển đến việc lấy metadata như WhiteBalance, tốc độ ISO và tiêu cự. Hãy bắt đầu!

## Câu trả lời nhanh
- **Thư viện nào đọc dữ liệu EXIF từ PSD trong Java?** Aspose.PSD (asp)  
- **Những thẻ nào có thể được trích xuất?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength, và hơn nữa.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Có, cần giấy phép thương mại; bản dùng thử miễn phí có sẵn.  
- **Tôi có thể sử dụng điều này với các định dạng ảnh khác không?** API này hỗ trợ PNG, JPEG, TIFF thông qua việc trích xuất metadata ảnh bằng Java.  
- **Thời gian triển khai mất bao lâu?** Khoảng 10‑15 phút cho kịch bản chỉ đọc cơ bản.

## Asp là gì (Aspose.PSD cho Java)?
Aspose.PSD cho Java là một thư viện thuần Java cho phép các nhà phát triển làm việc với các tệp Adobe Photoshop (PSD, PSB) mà không cần cài đặt Photoshop. Nó cung cấp quyền truy cập lập trình vào các lớp, tài nguyên và metadata—bao gồm các thẻ EXIF—làm cho nó trở thành công cụ lý tưởng cho các nhiệm vụ **java image metadata extraction**.

## Tại sao nên sử dụng Aspose.PSD (asp) để trích xuất EXIF?
Bạn có thể trích xuất các thẻ EXIF trong Java chỉ với hai lời gọi phương thức, và thư viện xử lý các tệp lên tới 2 GB mà không cần tải toàn bộ tài liệu vào bộ nhớ. Nó hỗ trợ **30+ định dạng ảnh** và giữ nguyên các cài đặt máy ảnh, mang lại kết quả quyết định trên môi trường Windows, Linux và macOS.

## Yêu cầu trước
Trước khi chúng ta đi vào mã, có một vài thứ bạn cần chuẩn bị:

1. Java Development Kit (JDK): Đảm bảo bạn đã cài đặt JDK trên máy. Bạn có thể tải xuống từ [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. Aspose.PSD cho Java: Tải thư viện từ [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
3. Môi trường phát triển tích hợp (IDE): Một IDE như IntelliJ IDEA, Eclipse hoặc NetBeans sẽ giúp việc lập trình thuận tiện hơn.  
4. Tệp PSD: Một tệp PSD có dữ liệu EXIF. Bạn có thể sử dụng mẫu được cung cấp trong hướng dẫn này hoặc bất kỳ tệp PSD nào khác có thẻ EXIF.

## Nhập các gói
Nhập các lớp Aspose.PSD cần thiết như Image, PsdImage, ThumbnailResource và JpegExifData để làm việc với tệp PSD.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Bước 1: tải ảnh PSD
`Image.load()` tải một tệp và trả về một đối tượng Image đại diện cho dữ liệu ảnh.  
`PsdImage` là lớp Aspose.PSD cung cấp chức năng đặc thù cho PSD.  
Phương thức `Image.load()` tải bất kỳ tệp ảnh được hỗ trợ nào vào bộ nhớ, trả về một đối tượng `Image` chung mà bạn có thể ép kiểu sang loại đặc thù PSD.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

Trong bước này, chúng ta tải tệp PSD bằng phương thức `Image.load()`. Lớp `PsdImage` được sử dụng để đại diện cho ảnh PSD, và chúng ta ép kiểu ảnh đã tải sang lớp này để truy cập các chức năng đặc thù của PSD.

## Bước 2: lặp qua các tài nguyên ảnh
`PsdImage.getResources()` trả về một tập hợp các tài nguyên nhúng như thumbnail và dữ liệu EXIF.  
Lệnh `PsdImage.getResources()` trả về một tập hợp tất cả các tài nguyên nhúng. Bằng cách lặp qua tập hợp này, bạn có thể tìm các tài nguyên thumbnail chứa metadata EXIF.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

Chúng ta duyệt qua các tài nguyên ảnh bằng một vòng lặp `for`. Mục tiêu là xác định các tài nguyên là thể hiện của `ThumbnailResource` hoặc `Thumbnail4Resource`, vì đây là các loại chứa dữ liệu EXIF.

## Bước 3: trích xuất dữ liệu EXIF
`ThumbnailResource.getJpegOptions()` cung cấp quyền truy cập vào các tùy chọn JPEG bao gồm metadata EXIF.  
`JpegExifData` chứa các giá trị thẻ EXIF riêng lẻ.  
Phương thức `ThumbnailResource.getJpegOptions()` cung cấp quyền truy cập vào một đối tượng `JpegExifData`, chứa các thẻ EXIF riêng lẻ như WhiteBalance, ISOSpeed và FocalLength.  
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

Chúng ta sử dụng câu lệnh `if` để kiểm tra xem tài nguyên có phải là thể hiện của `ThumbnailResource` không. Nếu có, chúng ta ép kiểu và lấy `JpegOptions` để truy cập `ExifData`. Cuối cùng, chúng ta in ra các thẻ EXIF khác nhau như WhiteBalance, Pixel Dimensions, ISOSpeed và FocalLength.

## Các vấn đề thường gặp & mẹo
- **Dữ liệu EXIF null:** Một số tệp PSD có thể không chứa tài nguyên thumbnail có thông tin EXIF. Luôn kiểm tra `null` trước khi truy cập giá trị thẻ.  
- **Lỗi đường dẫn tệp:** Sử dụng đường dẫn tuyệt đối hoặc đảm bảo thư mục làm việc trỏ tới thư mục chứa tệp PSD của bạn.  
- **Hạn chế giấy phép:** Bản dùng thử giới hạn số trang bạn có thể xử lý; nâng cấp lên giấy phép đầy đủ để sử dụng không giới hạn.

## Câu hỏi thường gặp
### EXIF là gì?
EXIF (Exchangeable Image File Format) là metadata nhúng trong các tệp ảnh, chứa thông tin như cài đặt máy ảnh, ngày giờ và kích thước ảnh.

### Tôi có thể chỉnh sửa dữ liệu EXIF bằng Aspose.PSD không?
Có, Aspose.PSD cho phép bạn đọc và sửa đổi dữ liệu EXIF. Bạn có thể cập nhật các thẻ và lưu lại thay đổi vào tệp ảnh.

### Aspose.PSD cho Java có miễn phí không?
Aspose.PSD cung cấp phiên bản dùng thử miễn phí mà bạn có thể tải xuống từ [Aspose.PSD official releases page](https://releases.aspose.com/). Để sử dụng đầy đủ tính năng, bạn cần mua giấy phép.

### Aspose.PSD hỗ trợ những định dạng nào khác?
Aspose.PSD hỗ trợ nhiều định dạng Adobe Photoshop, bao gồm PSD, PSB và hơn thế nữa. Nó cũng cung cấp tùy chọn chuyển đổi các định dạng này sang PNG, JPEG, TIFF, v.v.

### Làm sao để nhận hỗ trợ cho Aspose.PSD?
Bạn có thể nhận hỗ trợ qua [forum](https://forum.aspose.com/c/psd/34) của Aspose.PSD.

### Điều này giúp gì cho **java image metadata extraction**?
Bằng cách sử dụng đối tượng `JpegExifData`, bạn có thể lập trình để lấy bất kỳ thẻ EXIF nào bạn cần, tạo nền tảng vững chắc cho các nhiệm vụ trích xuất metadata rộng hơn trên các định dạng ảnh.

---

**Last Updated:** 2026-10-08  
**Được kiểm tra với:** Aspose.PSD for Java 24.11 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Đọc và chỉnh sửa thẻ Jpeg Exif Java](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [Xử lý ảnh Jpeg Java](/psd/java/java-jpeg-image-processing/)
- [Cách xoay ảnh theo góc cụ thể với Aspose.PSD cho Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}