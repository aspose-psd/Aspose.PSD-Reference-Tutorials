---
title: Điều chỉnh độ tương phản của hình ảnh bằng Aspose.PSD cho Java
linktitle: Điều chỉnh độ tương phản của hình ảnh
second_title: API Java Aspose.PSD
description: Khám phá thế giới điều chỉnh độ tương phản hình ảnh trong Java với Aspose.PSD. Hãy làm theo hướng dẫn từng bước của chúng tôi để thao tác hình ảnh liền mạch.
type: docs
weight: 22
url: /vi/java/advanced-techniques/adjust-contrast/
---
## Giới thiệu

Trong lĩnh vực xử lý hình ảnh bằng Java, Aspose.PSD nổi bật như một công cụ mạnh mẽ. Trong số vô số tính năng của nó, điều chỉnh độ tương phản hình ảnh là một yêu cầu phổ biến. Hướng dẫn này sẽ hướng dẫn bạn quy trình điều chỉnh độ tương phản hình ảnh bằng Aspose.PSD cho Java. Cho dù bạn là nhà phát triển dày dạn kinh nghiệm hay mới bắt đầu, hướng dẫn này sẽ giúp bạn nắm vững khía cạnh thiết yếu này của thao tác hình ảnh.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

- Hiểu biết cơ bản về lập trình Java.
-  Đã cài đặt thư viện Aspose.PSD cho Java. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/psd/java/).

## Gói nhập khẩu

Để bắt đầu, bạn cần nhập các gói cần thiết vào dự án Java của mình. Thêm các dòng sau vào mã của bạn:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Bước 1: Tải hình ảnh

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Tải hình ảnh hiện có vào một thể hiện của lớp RasterImage
Image image = Image.load(sourceFile);
```

 Trong bước này, chúng ta tải hình ảnh mẫu ("sample.psd") bằng cách sử dụng`Image.load` phương pháp.

## Bước 2: Truyền tới dữ liệu RasterImage và Cache

```java
// Truyền đối tượng của Hình ảnh sang RasterImage
RasterImage rasterImage = (RasterImage)image;

// Kiểm tra xem RasterImage có được lưu vào bộ nhớ đệm hay không và Cache RasterImage để có hiệu suất tốt hơn
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Ở đây, chúng tôi sử dụng chung`Image` phản đối một`RasterImage` để xử lý cụ thể. Bộ nhớ đệm dữ liệu hình ảnh cải thiện hiệu suất.

## Bước 3: Điều chỉnh độ tương phản

```java
// Điều chỉnh độ tương phản
rasterImage.adjustContrast(50);
```

 các`adjustContrast`phương pháp được sử dụng để sửa đổi độ tương phản của hình ảnh. Trong ví dụ này, độ tương phản được tăng thêm 50%.

## Bước 4: Tạo TiffOptions và lưu

```java
// Tạo một phiên bản TiffOptions cho hình ảnh kết quả
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Lưu hình ảnh thu được sang định dạng TIFF
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Ở đây, chúng tôi thiết lập`TiffOptions` cho hình ảnh đầu ra, chỉ định định dạng và các thuộc tính khác. Hình ảnh cuối cùng sau đó được lưu vào tệp TIFF.

## Phần kết luận

Chúc mừng! Bạn đã điều chỉnh thành công độ tương phản của hình ảnh bằng Aspose.PSD cho Java. Hướng dẫn này bao gồm các bước cần thiết, từ nhập gói đến lưu hình ảnh đã xử lý.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.PSD có tương thích với các định dạng hình ảnh khác nhau không?

Câu trả lời 1: Có, Aspose.PSD hỗ trợ nhiều định dạng hình ảnh khác nhau, mang lại sự linh hoạt cho các dự án của bạn.

### Câu hỏi 2: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.PSD?

 A2: Bạn có thể nhận được giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).

### Câu 3: Tôi có thể tìm tài liệu Aspose.PSD ở đâu?

A3: Tài liệu có sẵn[đây](https://reference.aspose.com/psd/java/).

### Câu hỏi 4: Aspose.PSD có những tùy chọn hỗ trợ nào?

 A4: Để được hỗ trợ, hãy truy cập[Diễn đàn Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Câu 5: Tôi có thể mua Aspose.PSD không?

 Câu trả lời 5: Có, bạn có thể mua Aspose.PSD[đây](https://purchase.aspose.com/buy).