---
title: Thực hiện vẽ đơn giản với Aspose.PSD cho Java
linktitle: Thực hiện vẽ đơn giản
second_title: API Java Aspose.PSD
description: Tìm hiểu cách vẽ hình trong tệp PSD bằng Aspose.PSD cho Java. Hướng dẫn từng bước này bao gồm việc tạo, thêm lớp và vẽ bằng các ví dụ về mã.
type: docs
weight: 10
url: /vi/java/basic-image-operations/simple-drawing/
---
## Giới thiệu

Chào mừng bạn đến với hướng dẫn từng bước này về cách thực hiện vẽ đơn giản bằng Aspose.PSD cho Java! Trong hướng dẫn này, chúng ta sẽ khám phá những điều cơ bản về tạo tài liệu PSD mới, thêm các lớp và vẽ các hình dạng với các màu sắc khác nhau. Aspose.PSD cho Java là một thư viện mạnh mẽ cho phép bạn thao tác với các tệp PSD theo chương trình, cung cấp chức năng mở rộng cho các tác vụ thiết kế đồ họa.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

- Bộ công cụ phát triển Java (JDK) được cài đặt trên máy của bạn.
- Aspose.PSD cho thư viện Java. Bạn có thể tải nó xuống từ[Aspose.PSD cho Tài liệu Java](https://reference.aspose.com/psd/java/).

## Gói nhập khẩu

Để bắt đầu, hãy nhập các gói cần thiết vào dự án Java của bạn. Bao gồm mã sau vào đầu tệp Java của bạn:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Bước 1: Tạo một tài liệu mới

Hãy bắt đầu bằng cách tạo một tài liệu PSD mới với chiều rộng và chiều cao được chỉ định:

```java
//ExStart:Tạo tài liệu
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:Tạo tài liệu
```

## Bước 2: Thêm một lớp

Bây giờ, hãy thêm một lớp vào tài liệu bằng cách sử dụng hàm tạo không có đối số:

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Bước 3: Vẽ hình

Ở bước này, chúng ta sẽ sử dụng lớp Graphics để vẽ các hình trên lớp đã tạo:

### Vẽ một hình chữ nhật có màu vàng

```java
//ExStart:VẽHình chữ nhậtVàng
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:VẽHình chữ nhậtVàng
```

### Vẽ một hình chữ nhật màu đỏ

```java
//ExStart:VẽHình chữ nhật màu đỏ
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedHình chữ nhật
```

### Vẽ một hình chữ nhật màu xanh

```java
//ExStart:DrawBlueHình chữ nhật
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueHình chữ nhật
```

## Bước 4: Lưu thay đổi

Cuối cùng, lưu một bản sao của tệp PSD đã tải bao gồm các thay đổi:

```java
//ExStart:Lưu Thay đổi
image.save(outPsdFilePath);
//ExEnd:Lưu Thay đổi
```

## Phần kết luận

Chúc mừng! Bạn đã thực hiện thành công việc vẽ đơn giản bằng Aspose.PSD cho Java. Hướng dẫn này bao gồm việc tạo một tài liệu mới, thêm các lớp và vẽ hình chữ nhật với các màu khác nhau. Hãy thoải mái khám phá các tính năng nâng cao hơn do thư viện cung cấp cho nhu cầu thiết kế đồ họa của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.PSD cho Java để thao tác với các tệp PSD hiện có không?

Câu trả lời 1: Có, Aspose.PSD cho Java cung cấp chức năng mở rộng để chỉnh sửa và thao tác với các tệp PSD hiện có.

### Câu hỏi 2: Tôi có thể tìm hỗ trợ cho Aspose.PSD cho Java ở đâu?

 A2: Bạn có thể ghé thăm[Aspose.PSD cho Diễn đàn Java](https://forum.aspose.com/c/psd/34) cho bất kỳ truy vấn liên quan đến hỗ trợ.

### Câu hỏi 3: Có bản dùng thử miễn phí cho Aspose.PSD cho Java không?

 A3: Có, bạn có thể truy cập phiên bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 4: Làm cách nào tôi có thể mua giấy phép Aspose.PSD cho Java?

 A4: Bạn có thể mua giấy phép từ[Trang mua Aspose.PSD](https://purchase.aspose.com/buy).

### Câu hỏi 5: Có giấy phép tạm thời cho Aspose.PSD dành cho Java không?

 Câu trả lời 5: Có, bạn có thể xin giấy phép tạm thời từ[đây](https://purchase.aspose.com/temporary-license/).