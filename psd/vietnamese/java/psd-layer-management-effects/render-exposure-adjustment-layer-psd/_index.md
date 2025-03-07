---
title: Kết xuất lớp điều chỉnh phơi sáng trong tệp PSD - Java
linktitle: Kết xuất lớp điều chỉnh phơi sáng trong tệp PSD - Java
second_title: API Java Aspose.PSD
description: Tìm hiểu cách kết xuất và điều chỉnh các lớp phơi sáng trong tệp PSD bằng Aspose.PSD cho Java. Hướng dẫn từng bước với các ví dụ về mã để sửa đổi và thêm các lớp hiển thị.
weight: 15
url: /vi/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kết xuất lớp điều chỉnh phơi sáng trong tệp PSD - Java

## Giới thiệu

Bạn đang làm việc với các tệp PSD của Photoshop và cần điều chỉnh độ phơi sáng hoặc thêm lớp điều chỉnh độ phơi sáng theo chương trình? Cho dù bạn đang điều chỉnh các lớp hiện có hay thêm các lớp mới, Aspose.PSD cho Java đều cung cấp một cách mạnh mẽ và trực quan để xử lý các tác vụ này. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn cách sử dụng Aspose.PSD cho Java để hiển thị và sửa đổi các lớp điều chỉnh độ phơi sáng trong tệp PSD. Đến cuối hướng dẫn này, bạn sẽ biết cách điều chỉnh cài đặt độ phơi sáng trong các lớp hiện có và thêm các lớp điều chỉnh độ phơi sáng mới vào tệp PSD của mình. Hãy đi sâu vào!

## Điều kiện tiên quyết

Trước khi chúng ta bắt đầu hướng dẫn, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

1. Bộ công cụ phát triển Java (JDK): Bạn cần cài đặt JDK trên máy của mình. Hướng dẫn này giả sử bạn có ít nhất JDK 8.
2.  Aspose.PSD cho Java: Bạn cần thư viện Aspose.PSD để làm việc với các tệp PSD. Bạn có thể tải nó xuống từ[đây](https://releases.aspose.com/psd/java/).
3. Kiến thức cơ bản về Java: Làm quen với lập trình Java sẽ giúp bạn dễ dàng theo dõi.
4. IDE hoặc Trình soạn thảo văn bản: Sử dụng bất kỳ IDE nào như IntelliJ IDEA, Eclipse hoặc trình soạn thảo văn bản mà bạn chọn để viết và chạy mã Java.

## Gói nhập khẩu

Trước tiên, hãy nhập các gói cần thiết từ Aspose.PSD cho Java. Bước này đảm bảo rằng mã của chúng tôi có thể sử dụng các tính năng của thư viện để thao tác với tệp PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Bước 1: Tải tệp PSD

Để bắt đầu, bạn cần tải tệp PSD của mình vào ứng dụng. Đây là cách bạn có thể làm điều đó:

```java
String dataDir = "Your Document Directory";  // Xác định thư mục tài liệu của bạn
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Đường dẫn tệp PSD nguồn

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Tải tập tin PSD
```

 Trong đoạn mã này, thay thế`"Your Document Directory"` với đường dẫn chứa tệp PSD của bạn. các`Image.load()` phương thức tải tệp PSD vào một phiên bản của`PsdImage`, cho phép bạn thao tác các lớp của nó.

## Bước 2: Chỉnh sửa lớp điều chỉnh phơi sáng hiện có

Sau khi tải tệp PSD, bạn có thể truy cập và sửa đổi các lớp hiện có. Nếu tệp chứa lớp điều chỉnh độ phơi sáng, bạn có thể điều chỉnh các thuộc tính của nó:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Điều chỉnh mức độ phơi sáng
        expLayer.setOffset(-0.25f);  // Đặt phần bù
        expLayer.setGammaCorrection(0.5f);  // Điều chỉnh hiệu chỉnh gamma
    }
}
```

Trong vòng lặp này, chúng tôi lặp lại tất cả các lớp của tệp PSD. Nếu chúng ta tìm thấy một`ExposureLayer` , chúng tôi sửa đổi nó`Exposure`, `Offset` , Và`GammaCorrection` của cải. Điều này cho phép bạn tinh chỉnh đầu ra hình ảnh của lớp điều chỉnh độ phơi sáng.

## Bước 3: Lưu tệp PSD đã sửa đổi

Sau khi thực hiện thay đổi, bạn cần lưu file PSD đã cập nhật:

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Đường dẫn lưu file PSD đã sửa đổi

im.save(psdPathAfterChange);  // Lưu các thay đổi vào tệp PSD
```

Dòng này lưu tệp PSD đã sửa đổi vào đường dẫn đã chỉ định, duy trì các điều chỉnh độ phơi sáng của bạn.

## Bước 4: Xuất dưới dạng PNG

Để xuất tệp PSD đã cập nhật dưới dạng PNG, hãy làm theo các bước sau:

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Đường dẫn lưu file PNG

PngOptions saveOptions = new PngOptions();  // Tạo tùy chọn PNG
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Đặt loại màu thành Truecolor với Alpha

im.save(pngExportPath, saveOptions);  // Lưu dưới dạng PNG
```

 Đây,`PngOptions` được sử dụng để định cấu hình cài đặt xuất PNG.`PngColorType.TruecolorWithAlpha` đảm bảo rằng tệp PNG giữ được độ sâu màu và độ trong suốt.

## Bước 5: Thêm lớp điều chỉnh phơi sáng mới

Nếu bạn muốn thêm lớp điều chỉnh độ phơi sáng mới vào tệp PSD hiện có, bạn có thể thực hiện bằng đoạn mã sau:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Đường dẫn tệp PSD nguồn

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Tải tập tin PSD

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Thêm lớp điều chỉnh độ phơi sáng mới

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Đường dẫn lưu file PSD đã sửa đổi
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Đường dẫn lưu file PNG

img.save(psdPathAfterChange);  // Lưu các thay đổi vào tệp PSD

PngOptions options = new PngOptions();  // Tạo tùy chọn PNG
options.setColorType(PngColorType.TruecolorWithAlpha);  // Đặt loại màu thành Truecolor với Alpha

img.save(pngExportPath, options);  // Lưu dưới dạng PNG
```

Trong bước này, một lớp điều chỉnh độ phơi sáng mới sẽ được thêm vào tệp PSD với các giá trị hiệu chỉnh độ phơi sáng, độ lệch và gamma được chỉ định. Sau đó, các tệp PSD và PNG được cập nhật sẽ được lưu.

## Phần kết luận

Và bạn có nó! Bạn đã học cách kết xuất và điều chỉnh các lớp hiển thị trong tệp PSD bằng Aspose.PSD cho Java. Chúng tôi đã đề cập đến cách sửa đổi các lớp phơi sáng hiện có, thêm các lớp mới và xuất tác phẩm của bạn dưới dạng tệp PNG. Cho dù bạn đang chỉnh sửa ảnh hay chuẩn bị nội dung thiết kế, những kỹ năng này sẽ nâng cao khả năng quản lý tệp PSD của bạn theo chương trình. Chúc mừng mã hóa!

## Câu hỏi thường gặp

### Aspose.PSD cho Java là gì?

Aspose.PSD for Java là thư viện cho phép bạn tạo, chỉnh sửa và chuyển đổi các tệp PSD theo chương trình bằng Java. Nó cung cấp chức năng toàn diện để làm việc với các tài liệu Photoshop.

### Tôi có thể sử dụng Aspose.PSD cho Java để thao tác với các loại lớp khác không?

Có, Aspose.PSD cho Java hỗ trợ nhiều loại lớp khác nhau, bao gồm lớp văn bản, lớp điều chỉnh và lớp hình ảnh, cho phép thao tác rộng rãi trên các tệp PSD.

### Làm cách nào để bắt đầu với Aspose.PSD cho Java?

 Bạn có thể bắt đầu bằng cách tải xuống thư viện từ[trang web](https://releases.aspose.com/psd/java/) và đề cập đến[tài liệu](https://reference.aspose.com/psd/java/) để biết hướng dẫn chi tiết và ví dụ.

### Có bản dùng thử miễn phí dành cho Aspose.PSD cho Java không?

 Có, bản dùng thử miễn phí có sẵn. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/).

### Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.PSD cho Java?

 Để được hỗ trợ, bạn có thể truy cập[Diễn đàn hỗ trợ Aspose](https://forum.aspose.com/c/psd/34) nơi bạn có thể đặt câu hỏi và nhận trợ giúp từ cộng đồng.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
