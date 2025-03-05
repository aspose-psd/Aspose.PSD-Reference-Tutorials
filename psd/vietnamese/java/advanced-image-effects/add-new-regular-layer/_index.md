---
title: Thêm một lớp thông thường mới vào PSD bằng Aspose.PSD cho Java
linktitle: Thêm một lớp thông thường mới vào PSD
second_title: API Java Aspose.PSD
description: Tìm hiểu cách thêm lớp thông thường mới vào tệp PSD bằng Aspose.PSD cho Java. Làm theo hướng dẫn từng bước của chúng tôi để thao tác PSD liền mạch.
type: docs
weight: 11
url: /vi/java/advanced-image-effects/add-new-regular-layer/
---
## Giới thiệu

Chào mừng bạn đến với hướng dẫn toàn diện này về cách sử dụng Aspose.PSD cho Java để thêm lớp thông thường mới vào tệp PSD. Aspose.PSD là một thư viện Java mạnh mẽ cho phép các nhà phát triển thao tác và làm việc với các tệp PSD một cách hiệu quả. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình thêm lớp thông thường mới vào tệp PSD, cung cấp các bước chi tiết và ví dụ về mã.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

- Môi trường phát triển Java: Đảm bảo rằng bạn đã thiết lập môi trường phát triển Java trên hệ thống của mình.
-  Thư viện Aspose.PSD: Tải xuống và cài đặt thư viện Aspose.PSD cho Java. Bạn có thể tìm thấy thư viện[đây](https://releases.aspose.com/psd/java/).

## Gói nhập khẩu

Để bắt đầu, hãy nhập các gói cần thiết vào dự án Java của bạn. Các gói này rất cần thiết để làm việc với các chức năng của Aspose.PSD. Bao gồm các dòng sau vào đầu tệp Java của bạn:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Bước 1: Tải tệp PSD

Tải tệp PSD bạn muốn chỉnh sửa bằng mã sau:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Bước 2: Chuẩn bị mảng dữ liệu và hình chữ nhật

Chuẩn bị hai mảng int và hai đối tượng Rectangle như sau:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Bước 3: Khởi tạo dữ liệu lớp

Khởi tạo mảng dữ liệu với giá trị mặc định:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Bước 4: Thêm các lớp thông thường

Thêm hai lớp thông thường vào hình ảnh PSD:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## Bước 5: Lưu PSD và PNG

Lưu PSD đã sửa đổi và tệp PNG bổ sung:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Chúc mừng! Bạn đã thêm thành công một lớp thông thường mới vào tệp PSD bằng Aspose.PSD cho Java.

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã đề cập đến quá trình thêm một lớp thông thường mới vào tệp PSD bằng Aspose.PSD cho Java. Thư viện mạnh mẽ này đơn giản hóa thao tác PSD, giúp các nhà phát triển Java có thể truy cập được. Thử nghiệm với các thông số và chức năng khác nhau để khám phá toàn bộ tiềm năng của Aspose.PSD.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.PSD có tương thích với Java 8 không?

Câu trả lời 1: Có, Aspose.PSD hỗ trợ Java 8 và các phiên bản mới hơn.

### Câu hỏi 2: Tôi có thể áp dụng các phép biến đổi cho các lớp được thêm vào không?

A2: Chắc chắn rồi! Aspose.PSD cung cấp một loạt các tùy chọn chuyển đổi cho các lớp.

### Câu hỏi 3: Tôi có thể tìm thêm tài liệu Aspose.PSD ở đâu?

 A3: Bạn có thể tham khảo tài liệu[đây](https://reference.aspose.com/psd/java/).

### Câu hỏi 4: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.PSD?

 A4: Thăm quan[liên kết này](https://purchase.aspose.com/temporary-license/) cho các tùy chọn giấy phép tạm thời.

### Câu hỏi 5: Có diễn đàn cộng đồng nào hỗ trợ Aspose.PSD không?

 Câu trả lời 5: Có, bạn có thể tìm thấy sự hỗ trợ và thảo luận[đây](https://forum.aspose.com/c/psd/34).