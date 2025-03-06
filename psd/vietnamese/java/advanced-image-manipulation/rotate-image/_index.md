---
title: Xoay một hình ảnh trong Aspose.PSD cho Java
linktitle: Xoay một hình ảnh
second_title: API Java Aspose.PSD
description: Khám phá xoay hình ảnh trong Java một cách dễ dàng với Aspose.PSD. Xoay, lật và lưu tệp PSD dễ dàng.
weight: 19
url: /vi/java/advanced-image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xoay một hình ảnh trong Aspose.PSD cho Java

## Giới thiệu

Aspose.PSD cho Java cung cấp một bộ tính năng mạnh mẽ để làm việc với hình ảnh, cho phép các nhà phát triển thao tác và xử lý các tệp PSD một cách hiệu quả. Trong hướng dẫn này, chúng ta sẽ tập trung vào một nhiệm vụ cụ thể: xoay hình ảnh. Cho dù bạn đang xây dựng một ứng dụng chỉnh sửa ảnh hay chỉ cần điều chỉnh hướng của hình ảnh, Aspose.PSD đều giúp quá trình này trở nên đơn giản.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.PSD for Java Library: Đảm bảo bạn đã tải xuống và cài đặt thư viện Aspose.PSD cho Java. Bạn có thể tìm thấy thư viện và tài liệu chi tiết[đây](https://reference.aspose.com/psd/java/).

- Môi trường phát triển Java: Đảm bảo bạn đã thiết lập môi trường phát triển Java trên máy của mình.

-  Tệp PSD mẫu: Chuẩn bị tệp PSD mẫu mà bạn muốn xoay. Điều chỉnh`sourceFile` biến trong mã ví dụ với đường dẫn đến tệp PSD của bạn.

## Gói nhập khẩu

Bắt đầu bằng cách nhập các gói cần thiết để tận dụng khả năng của Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Bước 1: Tải hình ảnh

 Tải hình ảnh hiện có vào một phiên bản của`Image` lớp học:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Bước 2: Xoay hình ảnh

 Xoay hình ảnh bằng cách sử dụng`rotateFlip` phương pháp. Trong ví dụ này, chúng tôi xoay hình ảnh 270 độ:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Bước 3: Lưu hình ảnh đã xoay

 Lưu hình ảnh đã xoay bằng cách sử dụng`save` phương thức và chỉ định định dạng đầu ra (JPEG, trong trường hợp này):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Phần kết luận

Chúc mừng! Bạn đã xoay hình ảnh thành công bằng Aspose.PSD cho Java. Thư viện đơn giản nhưng mạnh mẽ này mở ra một thế giới khả năng xử lý hình ảnh trong các ứng dụng Java của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.PSD có tương thích với các định dạng hình ảnh khác nhau không?

Câu trả lời 1: Có, Aspose.PSD hỗ trợ nhiều định dạng hình ảnh khác nhau, bao gồm PSD, JPEG, PNG, v.v.

### Câu hỏi 2: Tôi có thể áp dụng các thao tác xoay tùy chỉnh, không chỉ các thao tác lật được xác định trước không?

A2: Chắc chắn rồi! Aspose.PSD cung cấp tính linh hoạt trong việc áp dụng các phép xoay tùy chỉnh để đáp ứng các yêu cầu cụ thể của bạn.

### Câu hỏi 3: Tôi có thể tìm thêm hỗ trợ hoặc hỗ trợ ở đâu?

 A3: Đối với bất kỳ thắc mắc hoặc vấn đề nào, hãy truy cập[Diễn đàn Aspose.PSD](https://forum.aspose.com/c/psd/34) để hỗ trợ cộng đồng.

### Q4: Có bản dùng thử miễn phí không?

 Câu trả lời 4: Có, bạn có thể khám phá Aspose.PSD bằng[dùng thử miễn phí](https://releases.aspose.com/).

### Câu hỏi 5: Làm cách nào để có được giấy phép tạm thời?

 Câu trả lời 5: Nếu bạn cần giấy phép tạm thời, bạn có thể lấy một giấy phép[đây](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
