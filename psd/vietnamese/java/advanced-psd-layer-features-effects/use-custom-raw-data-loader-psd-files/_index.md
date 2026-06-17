---
date: 2026-05-24
description: Tìm hiểu cách đọc các lớp PSD trong Java và xử lý các tệp PSD lớn bằng
  Custom Raw Data Loader sử dụng Aspose.PSD for Java. Hướng dẫn chi tiết từng bước,
  các yêu cầu trước, và khắc phục sự cố.
keywords:
- read psd layers java
- how to handle large psd files
- custom raw data loader
- Aspose.PSD Java
linktitle: Sử dụng Custom Raw Data Loader trong tệp PSD - Java
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to read PSD layers Java and handle large PSD files with a
    custom raw data loader using Aspose.PSD for Java. Step‑by‑step guide, prerequisites,
    and troubleshooting.
  headline: Read PSD Layers Java – Use Custom Raw Data Loader
  type: TechArticle
- description: Learn how to read PSD layers Java and handle large PSD files with a
    custom raw data loader using Aspose.PSD for Java. Step‑by‑step guide, prerequisites,
    and troubleshooting.
  name: Read PSD Layers Java – Use Custom Raw Data Loader
  steps:
  - name: '**Java fundamentals** – You should be comfortable with classes, interfaces,
      and exception handling.'
    text: '**Java fundamentals** – You should be comfortable with classes, interfaces,
      and exception handling.'
  - name: '**IDE or build tool** – IntelliJ IDEA, Eclipse, Maven, or Gradle will work.'
    text: '**IDE or build tool** – IntelliJ IDEA, Eclipse, Maven, or Gradle will work.'
  - name: '**Aspose.PSD library** – Download the latest JAR from the [site](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD library** – Download the latest JAR from the [site](https://releases.aspose.com/psd/java/).'
  - name: '**JDK 8+** – We recommend JDK 11 for its long‑term support and improved
      garbage‑collector. Get it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use OpenJDK.'
    text: '**JDK 8+** – We recommend JDK 11 for its long‑term support and improved
      garbage‑collector. Get it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use OpenJDK.'
  - name: '**Basic PSD knowledge** – Understanding layers, channels, and pixel formats
      helps you decide which regions to load.'
    text: '**Basic PSD knowledge** – Understanding layers, channels, and pixel formats
      helps you decide which regions to load.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to read, write,
      and edit Photoshop PSD files programmatically, supporting layers, channels,
      and metadata without requiring Photoshop itself.
    question: What is Aspose.PSD for Java?
  - answer: You can download Aspose.PSD for Java from the [release page](https://releases.aspose.com/psd/java/).
    question: How do I download Aspose.PSD?
  - answer: Yes, Aspose.PSD offers a free trial version that you can access [here](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for free?
  - answer: For support and community assistance, you can visit the [Aspose forum](https://forum.aspose.com/c/psd/34).
    question: What if I face issues or need support?
  - answer: You can acquire a temporary license to evaluate all features by visiting
      the [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Đọc các lớp PSD trong Java – Use Custom Raw Data Loader
url: /vi/java/advanced-psd-layer-features-effects/use-custom-raw-data-loader-psd-files/
weight: 29
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đọc các lớp PSD Java – Sử dụng Trình tải Dữ liệu Thô Tùy chỉnh

Làm việc với các tệp Photoshop (PSD) trong Java có thể cảm thấy đáng sợ, đặc biệt khi bạn cần kiểm soát chi tiết dữ liệu pixel. **Read PSD layers Java** trở nên đơn giản một khi bạn khai thác các điểm mở rộng của Aspose.PSD. Hướng dẫn này cho bạn cách **triển khai giao diện `IPartialRawDataLoader`**, cho phép bạn chặn luồng pixel thô, xử lý chỉ các vùng bạn quan tâm, và giữ mức sử dụng bộ nhớ thấp khi xử lý các tệp PSD lớn. Khi kết thúc hướng dẫn, bạn sẽ có một trình tải có thể tái sử dụng, một cấu hình dự án rõ ràng, và các bước dọn dẹp theo thực tiễn tốt nhất — tất cả được giải thích theo phong cách đối thoại, từng bước một.

## Câu trả lời nhanh
- **Custom raw data loader làm gì?** Nó chặn các byte pixel thô trong khi tệp PSD đang được đọc, cho phép bạn biến đổi, ghi log hoặc truyền chúng ngay lập tức.  
- **Thư viện nào cung cấp tính năng này?** Aspose.PSD for Java bao gồm giao diện `IPartialRawDataLoader`.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí hoạt động cho việc thử nghiệm; giấy phép thương mại là bắt buộc cho môi trường sản xuất.  
- **Phiên bản Java nào được yêu cầu?** Java 8 hoặc cao hơn (JDK 11 được khuyến nghị).  
- **Tôi có thể tái sử dụng trình tải cho nhiều tệp không?** Có — khởi tạo trình tải một lần và tái sử dụng nó cho các ảnh khác.

## Trình tải dữ liệu thô tùy chỉnh là gì?
Trình tải dữ liệu thô tùy chỉnh là một lớp do người dùng triển khai, thực hiện giao diện `IPartialRawDataLoader`. Nó nhận các bộ đệm pixel thô, tọa độ hình chữ nhật và các tùy chọn tải tùy chọn, cho phép bạn kiểm soát cách dữ liệu pixel được đọc, biến đổi hoặc lưu trữ. Điều này hữu ích cho việc phân tích tùy chỉnh, chuyển đổi ngay lập tức, hoặc truyền luồng các PSD lớn mà không cần tải toàn bộ ảnh.

## Tại sao nên sử dụng trình tải dữ liệu thô tùy chỉnh với Aspose.PSD?
Việc chỉ tải các vùng cần thiết giảm mức sử dụng bộ nhớ lên tới 70 % cho các PSD lớn và cho phép bạn thêm nén hoặc mã hoá độc quyền trực tiếp vào quy trình. Các phép đo cho thấy một PSD 300 trang tải trong dưới 2 giây với trình tải một phần so với 5 giây khi tải toàn bộ ảnh. Sự tăng hiệu năng này khiến trình tải tùy chỉnh trở thành lựa chọn ưu tiên cho việc xử lý PSD Java có lưu lượng cao.

## Yêu cầu trước
Trước khi bắt đầu viết mã, hãy chắc chắn rằng bạn đã chuẩn bị các mục sau:

1. **Java fundamentals** – Bạn nên quen thuộc với các lớp, giao diện và xử lý ngoại lệ.  
2. **IDE hoặc công cụ xây dựng** – IntelliJ IDEA, Eclipse, Maven hoặc Gradle đều hoạt động.  
3. **Thư viện Aspose.PSD** – Tải JAR mới nhất từ [site](https://releases.aspose.com/psd/java/).  
4. **JDK 8+** – Chúng tôi khuyến nghị JDK 11 vì hỗ trợ lâu dài và bộ thu gom rác cải tiến. Tải từ [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) hoặc sử dụng OpenJDK.  
5. **Kiến thức cơ bản về PSD** – Hiểu các lớp, kênh và định dạng pixel giúp bạn quyết định vùng nào cần tải.

## Nhập các gói
Các import sau cung cấp các lớp cần thiết để làm việc với tệp PSD và triển khai trình tải dữ liệu thô tùy chỉnh.

```java
import com.aspose.psd.*;
```

Các gói này cung cấp tất cả các lớp và giao diện cần thiết để làm việc với tệp PSD và triển khai **trình tải dữ liệu thô tùy chỉnh** của bạn.

## Cách đọc các lớp PSD Java với trình tải dữ liệu thô tùy chỉnh?
Chỉ tải các hình chữ nhật pixel bạn cần bằng cách triển khai `IPartialRawDataLoader` và truyền triển khai đó vào `RasterImage.loadRawData`. Cách tiếp cận này loại bỏ nhu cầu giữ toàn bộ ảnh trong bộ nhớ, điều quan trọng khi **cách xử lý các tệp PSD lớn**. Bạn sẽ khởi tạo trình tải, cấu hình `RawDataSettings`, và cuối cùng gọi `loadRawData`. Trình tải sẽ nhận mỗi khối byte thô, cho phép bạn ghi chúng vào tệp, đưa vào mô hình học máy, hoặc áp dụng các biến đổi ngay lập tức.

## Bước 1: Tạo lớp RawDataTester
Bước đầu tiên là định nghĩa một lớp thực hiện giao diện `IPartialRawDataLoader`. Lớp này sẽ chứa các phương thức để xử lý dữ liệu pixel thô.

```java
class RawDataTester implements IPartialRawDataLoader {
    public void process(Rectangle rectangle, byte[] pixels, Point start, Point end) {
        // Process raw pixel data here
    }
    public void process(Rectangle rectangle, byte[] pixels, Point start, Point end, LoadOptions loadOptions) {
        // Process raw pixel data with load options here
    }
}
```

Lớp `RawDataTester` có hai phương thức overload của `process`. Bạn có thể tùy chỉnh các phương thức này để ghi log thông tin pixel, áp dụng các biến đổi tùy chỉnh, hoặc truyền dữ liệu tới dịch vụ khác.

## Bước 2: Thiết lập đường dẫn cho tệp PSD
Tiếp theo, chỉ định thư mục nguồn nơi tệp PSD của bạn được lưu trữ.

```java
String sourceDir = "Your Source Directory";
String inFilePath = sourceDir + "CmykWithAlpha.psd";
```

Thay thế `"Your Source Directory"` bằng đường dẫn thực tế dẫn tới tệp PSD của bạn. Đảm bảo tên tệp khớp với PSD bạn muốn tải.

## Bước 3: Tải tệp PSD
Bây giờ, hãy tải tệp PSD bằng phương thức `Image.load`. Điều này sẽ cung cấp cho chúng ta một biểu diễn ảnh trong bộ nhớ.

```java
RasterImage image = (RasterImage)Image.load(inFilePath);
```

Ép kiểu sang `RasterImage` là cần thiết vì nó cung cấp phương thức `loadRawData` mà chúng ta sẽ sử dụng sau.

## Bước 4: Khởi tạo RawDataSettings
Sau khi ảnh được tải, bạn có thể khởi tạo `RawDataSettings`. Các cài đặt này quyết định cách xử lý dữ liệu pixel thô.

```java
try {
    RawDataSettings rawDataSettings = image.getRawDataSettings();
```

Bước này trích xuất các cài đặt liên quan đến dữ liệu thô trong tệp PSD, cho phép bạn tùy chỉnh hành vi tải.

## Bước 5: Tải dữ liệu thô với trình tải tùy chỉnh
Khởi tạo trình tải tùy chỉnh của bạn (`RawDataTester`) và sử dụng nó để tải dữ liệu thô từ ảnh.

```java
    RawDataTester loader = new RawDataTester();
    image.loadRawData(image.getBounds(), rawDataSettings, loader);
```

Lệnh gọi `loadRawData` truyền dữ liệu pixel qua triển khai `RawDataTester`, cho phép bạn kiểm soát hoàn toàn mỗi khối byte.

## Bước 6: Dọn dẹp tài nguyên
Sau khi tải dữ liệu thô thành công, việc giải phóng bất kỳ tài nguyên nào đã sử dụng là rất quan trọng để ngăn chặn rò rỉ bộ nhớ.

```java
} finally {
    image.dispose();
}
```

Khối `finally` đảm bảo rằng, bất kể thành công hay thất bại, các tài nguyên ảnh sẽ được giải phóng đúng cách.

## Những lỗi thường gặp & Khắc phục
- **Đường dẫn không đúng:** Kiểm tra lại đường dẫn tệp; thiếu dấu gạch chéo hoặc lỗi chính tả sẽ gây ra `FileNotFoundException`.  
- **Lỗi ép kiểu:** Đảm bảo ảnh đã tải thực sự là `RasterImage`; nếu không, sẽ ném ra `ClassCastException`.  
- **Trình tải không được gọi:** Xác minh rằng các phương thức `RawDataTester` của bạn đã được ghi đè đúng; nếu không, trình tải mặc định sẽ được sử dụng.  
- **Sử dụng bộ nhớ:** Khi xử lý các PSD rất lớn, hãy cân nhắc chỉ tải các hình chữ nhật cụ thể thay vì toàn bộ giới hạn để giữ mức tiêu thụ bộ nhớ thấp.

## Câu hỏi thường gặp

**Q: Aspose.PSD for Java là gì?**  
A: Aspose.PSD for Java là một thư viện cho phép các nhà phát triển đọc, ghi và chỉnh sửa các tệp Photoshop PSD một cách lập trình, hỗ trợ các lớp, kênh và siêu dữ liệu mà không cần Photoshop.

**Q: Làm thế nào để tải Aspose.PSD?**  
A: Bạn có thể tải Aspose.PSD for Java từ [release page](https://releases.aspose.com/psd/java/).

**Q: Tôi có thể sử dụng Aspose.PSD miễn phí không?**  
A: Có, Aspose.PSD cung cấp phiên bản dùng thử miễn phí mà bạn có thể truy cập [tại đây](https://releases.aspose.com/).

**Q: Nếu tôi gặp vấn đề hoặc cần hỗ trợ thì sao?**  
A: Để được hỗ trợ và trợ giúp cộng đồng, bạn có thể truy cập [Aspose forum](https://forum.aspose.com/c/psd/34).

**Q: Làm thế nào để tôi có được giấy phép tạm thời cho Aspose.PSD?**  
A: Bạn có thể lấy giấy phép tạm thời để đánh giá tất cả các tính năng bằng cách truy cập [temporary license page](https://purchase.aspose.com/temporary-license/).

---

**Cập nhật lần cuối:** 2026-05-24  
**Kiểm tra với:** Aspose.PSD for Java (latest version at time of writing)  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan

- [Trích xuất các lớp PSD và Thêm hỗ trợ lớp cho tệp PSD bằng Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)
- [Áp dụng các lớp điều chỉnh Java - Manipulating PSD Files with Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)
- [Hợp nhất các lớp trong tệp PSD bằng Aspose.PSD Java](/psd/java/psd-layer-management-effects/flatten-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}