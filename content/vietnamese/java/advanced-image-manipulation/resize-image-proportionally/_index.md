---
title: Thay đổi kích thước hình ảnh theo tỷ lệ với Aspose.PSD cho Java
linktitle: Thay đổi kích thước hình ảnh theo tỷ lệ
second_title: API Java Aspose.PSD
description: Nâng cao các ứng dụng Java của bạn với Aspose.PSD. Làm theo hướng dẫn của chúng tôi để thay đổi kích thước hình ảnh một cách dễ dàng. Hãy nâng cao khả năng xử lý hình ảnh của bạn ngay hôm nay.
type: docs
weight: 17
url: /vi/java/advanced-image-manipulation/resize-image-proportionally/
---
## Giới thiệu

Chào mừng bạn đến với hướng dẫn từng bước của chúng tôi về cách thay đổi kích thước hình ảnh theo tỷ lệ bằng Aspose.PSD cho Java. Nếu bạn đang tìm cách nâng cao các ứng dụng Java của mình bằng khả năng thay đổi kích thước hình ảnh hiệu quả thì bạn đã đến đúng nơi. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn thực hiện quy trình bằng các bước rõ ràng và ngắn gọn.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

1. Môi trường Java: Đảm bảo bạn đã cài đặt Java trên hệ thống của mình.
2.  Thư viện Aspose.PSD: Tải xuống và cài đặt thư viện Aspose.PSD. Bạn có thể tìm thấy các tài nguyên cần thiết[đây](https://releases.aspose.com/psd/java/).

## Gói nhập khẩu

Khi bạn đã sắp xếp các điều kiện tiên quyết, hãy nhập các gói cần thiết vào dự án Java của bạn. Đảm bảo rằng thư viện Aspose.PSD được tham chiếu chính xác trong dự án của bạn.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Bước 1: Tải hình ảnh

Bắt đầu bằng cách tải hình ảnh bạn muốn thay đổi kích thước vào ứng dụng Java của mình.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Bước 2: Chỉ định chiều rộng và chiều cao

Xác định chiều rộng và chiều cao mới cho hình ảnh đã thay đổi kích thước của bạn. Trong ví dụ này, chúng tôi sẽ thay đổi kích thước hình ảnh thành một nửa kích thước ban đầu.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Bước 3: Lưu hình ảnh đã thay đổi kích thước

Lưu hình ảnh đã thay đổi kích thước vào vị trí mong muốn của bạn, chỉ định các tùy chọn định dạng (PNG, trong trường hợp này).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Và bạn có nó rồi đấy! Bạn đã thay đổi kích thước hình ảnh theo tỷ lệ thành công bằng Aspose.PSD cho Java.

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã trình bày các bước cần thiết để thay đổi kích thước hình ảnh theo tỷ lệ bằng cách sử dụng thư viện Aspose.PSD cho Java. Giờ đây, bạn có thể dễ dàng tích hợp chức năng này vào các ứng dụng Java của mình để cải thiện khả năng xử lý hình ảnh.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.PSD có tương thích với tất cả các định dạng hình ảnh không?

 Câu trả lời 1: Aspose.PSD hỗ trợ nhiều định dạng hình ảnh khác nhau, bao gồm PSD, PNG, JPEG, v.v. Kiểm tra[tài liệu](https://reference.aspose.com/psd/java/) để có danh sách đầy đủ.

### Câu hỏi 2: Tôi có thể sử dụng Aspose.PSD cho các dự án thương mại không?

 A2: Có, bạn có thể. Tham quan[trang mua hàng](https://purchase.aspose.com/buy) để biết chi tiết cấp phép.

### Câu hỏi 3: Giấy phép tạm thời có sẵn cho mục đích thử nghiệm không?

 A3: Có, bạn có thể xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/) để đánh giá.

### Câu hỏi 4: Tôi có thể tìm hỗ trợ cho Aspose.PSD ở đâu?

 A4: Tham quan[Diễn đàn Aspose.PSD](https://forum.aspose.com/c/psd/34) để được cộng đồng hỗ trợ và giúp đỡ.

### Câu hỏi 5: Làm cách nào tôi có thể truy cập tài liệu Aspose.PSD?

 A5: Tham khảo tài liệu chi tiết[đây](https://reference.aspose.com/psd/java/).
`