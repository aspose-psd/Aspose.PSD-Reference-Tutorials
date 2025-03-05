---
title: Thêm màu lớp nét trong Aspose.PSD cho Java
linktitle: Thêm màu lớp nét
second_title: API Java Aspose.PSD
description: Khám phá sức mạnh của Aspose.PSD cho Java với hướng dẫn từng bước của chúng tôi về cách thêm màu lớp nét vẽ. Nâng cao thiết kế đồ họa của bạn một cách dễ dàng.
type: docs
weight: 14
url: /vi/java/advanced-image-effects/add-stroke-layer-color/
---
## Giới thiệu

Khai phá tiềm năng thiết kế đồ họa của ứng dụng Java của bạn với Aspose.PSD. Trong hướng dẫn này, chúng ta sẽ đi sâu vào thế giới hấp dẫn của việc thêm màu lớp nét vẽ bằng Aspose.PSD cho Java. Nâng cao đồ họa của bạn bằng những nét vẽ nổi bật, dễ dàng tạo ra các thiết kế hấp dẫn về mặt hình ảnh.

## Điều kiện tiên quyết

Trước khi bắt đầu hành trình sáng tạo này, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Thư viện Aspose.PSD: Tải xuống và thiết lập thư viện Aspose.PSD bằng cách làm theo hướng dẫn[tài liệu](https://reference.aspose.com/psd/java/).

- Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt Java trên hệ thống của mình.

- Môi trường phát triển tích hợp (IDE): Chọn một IDE theo sở thích của bạn; Eclipse hoặc IntelliJ là những lựa chọn phổ biến.

## Gói nhập khẩu

Hãy bắt đầu bằng cách nhập các gói cần thiết để biến phép thuật Aspose.PSD thành hiện thực.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Bước 1: Thiết lập dự án của bạn

Bắt đầu bằng cách tạo một dự án Java mới trong IDE ưa thích của bạn. Đảm bảo rằng thư viện Aspose.PSD được thêm vào dự án của bạn.

## Bước 2: Tải tệp PSD

Tải tệp PSD bằng Aspose.PSD, cho phép tải tài nguyên hiệu ứng.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Bước 3: Truy cập lớp Stroke

Truy cập lớp hiệu ứng đột quỵ trong tệp PSD.

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Bước 4: Xác thực thuộc tính nét vẽ

Đảm bảo các thuộc tính đột quỵ như mong đợi.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Bước 5: Đặt màu và độ mờ

Sửa đổi màu sắc và độ mờ của lớp nét vẽ.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Bước 6: Lưu PSD đã sửa đổi

Lưu tệp PSD đã sửa đổi với màu lớp nét vẽ mới được thêm vào.

```java
im.save(exportPath);
```

## Phần kết luận

Chúc mừng! Bạn đã thêm thành công màu lớp nét vào tệp PSD của mình bằng Aspose.PSD cho Java. Thử nghiệm với các màu sắc và cài đặt khác nhau để làm cho thiết kế đồ họa của bạn trở nên sống động.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.PSD với các thư viện đồ họa Java khác không?

Câu trả lời 1: Có, Aspose.PSD có thể được tích hợp với các thư viện đồ họa Java khác để nâng cao chức năng.

### Câu hỏi 2: Aspose.PSD có tương thích với định dạng tệp PSD mới nhất không?

A2: Chắc chắn rồi! Aspose.PSD theo kịp các thông số kỹ thuật định dạng tệp PSD mới nhất, đảm bảo khả năng tương thích.

### Câu hỏi 3: Làm cách nào để xử lý các trường hợp ngoại lệ khi sử dụng Aspose.PSD?

 A3: Hãy tham khảo[diễn đàn hỗ trợ](https://forum.aspose.com/c/psd/34) để được hỗ trợ trong việc xử lý các trường hợp ngoại lệ và khắc phục sự cố.

### Câu hỏi 4: Tôi có thể dùng thử Aspose.PSD trước khi mua không?

 A4: Chắc chắn rồi! Lấy một[dùng thử miễn phí](https://releases.aspose.com/) để khám phá các tính năng của Aspose.PSD trước khi đưa ra cam kết.

### Câu hỏi 5: Tôi có thể lấy giấy phép tạm thời cho Aspose.PSD ở đâu?

 A5: Có được một[giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) để Aspose.PSD đánh giá khả năng của nó trong các dự án của bạn.