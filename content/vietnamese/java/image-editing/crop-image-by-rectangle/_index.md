---
title: Cắt hình ảnh bằng hình chữ nhật trong Aspose.PSD cho Java
linktitle: Cắt ảnh theo hình chữ nhật
second_title: API Java Aspose.PSD
description: Khám phá khả năng cắt ảnh liền mạch trong Java với Aspose.PSD. Làm theo hướng dẫn từng bước của chúng tôi để cắt ảnh dễ dàng bằng Aspose.PSD cho Java.
type: docs
weight: 15
url: /vi/java/image-editing/crop-image-by-rectangle/
---
## Giới thiệu

Trong thế giới phát triển Java, thao tác với hình ảnh là một nhiệm vụ phổ biến và Aspose.PSD cho Java cung cấp một giải pháp mạnh mẽ để xử lý hình ảnh. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình cắt ảnh theo hình chữ nhật bằng Aspose.PSD cho Java. Hãy làm theo các bước dưới đây để đạt được điều này một cách dễ dàng.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo rằng bạn có sẵn các điều kiện tiên quyết sau:

- Bộ công cụ phát triển Java (JDK) được cài đặt trên máy của bạn.
-  Aspose.PSD cho thư viện Java. Bạn có thể tải nó xuống từ[trang mạng](https://releases.aspose.com/psd/java/).

## Gói nhập khẩu

Đảm bảo bao gồm các gói cần thiết trong dự án Java của bạn để tận dụng các khả năng của Aspose.PSD cho Java. Thêm các câu lệnh nhập sau vào đầu tệp Java của bạn:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Bây giờ, hãy chia quy trình thành nhiều bước để hướng dẫn bạn cắt hình ảnh theo hình chữ nhật bằng Aspose.PSD cho Java.

## Bước 1: Thiết lập thư mục tài liệu của bạn

```java
String dataDir = "Your Document Directory";
```

 Thay thế`"Your Document Directory"` với đường dẫn thực tế nơi chứa tệp PSD của bạn.

## Bước 2: Chỉ định tệp nguồn và đích

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Xác định đường dẫn cho tệp PSD nguồn và tệp JPEG đích.

## Bước 3: Tải và lưu trữ hình ảnh

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Tải hình ảnh PSD vào một`RasterImage` instance và lưu trữ dữ liệu của nó.

## Bước 4: Tạo và xác định hình chữ nhật cắt

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

 Tạo một thể hiện của`Rectangle` lớp với kích thước mong muốn để cắt xén.

## Bước 5: Cắt và lưu hình ảnh

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Thực hiện thao tác cắt bằng cách sử dụng hình chữ nhật đã chỉ định và lưu kết quả dưới dạng tệp JPEG.

Lặp lại các bước này nếu cần, điều chỉnh các thông số theo yêu cầu cụ thể của bạn.

## Phần kết luận

Trong hướng dẫn này, chúng ta đã tìm hiểu quy trình cắt xén hình ảnh theo hình chữ nhật bằng Aspose.PSD cho Java. Bằng cách làm theo các bước này, bạn có thể dễ dàng tích hợp các khả năng xử lý hình ảnh mạnh mẽ vào các ứng dụng Java của mình.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.PSD cho Java với các khung công tác Java khác không?

Câu trả lời 1: Có, Aspose.PSD cho Java có thể được tích hợp với nhiều khung công tác Java khác nhau, mang lại sự linh hoạt trong các dự án phát triển của bạn.

### Câu hỏi 2: Có bản dùng thử miễn phí cho Aspose.PSD cho Java không?

 A2: Có, bạn có thể truy cập phiên bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 3: Tôi có thể tìm thêm hỗ trợ hoặc hỗ trợ ở đâu?

 A3: Tham quan[Diễn đàn Aspose.PSD](https://forum.aspose.com/c/psd/34) để được cộng đồng hỗ trợ và thảo luận.

### Câu hỏi 4: Làm cách nào để có được giấy phép tạm thời cho Aspose.PSD cho Java?

 A4: Bạn có thể có được giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).

### Câu hỏi 5: Các định dạng hình ảnh được hỗ trợ để cắt xén trong Aspose.PSD cho Java là gì?

Câu trả lời 5: Aspose.PSD cho Java hỗ trợ nhiều định dạng hình ảnh khác nhau, bao gồm PSD, PNG, JPEG, v.v.