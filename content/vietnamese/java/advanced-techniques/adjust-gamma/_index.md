---
title: Điều chỉnh Gamma của hình ảnh bằng Aspose.PSD cho Java
linktitle: Điều chỉnh Gamma của hình ảnh
second_title: API Java Aspose.PSD
description: Tìm hiểu cách điều chỉnh gamma hình ảnh một cách dễ dàng bằng Aspose.PSD cho Java. Thực hiện theo hướng dẫn từng bước của chúng tôi để có kết quả tối ưu.
type: docs
weight: 23
url: /vi/java/advanced-techniques/adjust-gamma/
---
## Giới thiệu

Trong lĩnh vực xử lý hình ảnh, việc điều chỉnh gamma của hình ảnh là một bước quan trọng để nâng cao sức hấp dẫn trực quan của nó. Aspose.PSD cho Java cung cấp một giải pháp mạnh mẽ cho các nhà phát triển Java để dễ dàng thao tác gamma hình ảnh. Trong hướng dẫn này, chúng ta sẽ khám phá cách điều chỉnh gamma bằng Aspose.PSD, chia nhỏ từng bước để đảm bảo triển khai liền mạch.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn đã thiết lập các điều kiện tiên quyết sau:

1. Môi trường phát triển Java: Đảm bảo bạn đã cài đặt môi trường phát triển Java trên hệ thống của mình.
2.  Thư viện Aspose.PSD: Tải xuống và tích hợp thư viện Aspose.PSD vào dự án Java của bạn. Bạn có thể tìm thấy các tài nguyên cần thiết trong[tài liệu](https://reference.aspose.com/psd/java/).
3. Hình ảnh mẫu: Chuẩn bị hình ảnh PSD mẫu mà bạn sẽ sử dụng để áp dụng điều chỉnh gamma.

## Gói nhập khẩu

Để bắt đầu quá trình, hãy nhập các gói cần thiết vào dự án Java của bạn. Điều này tạo tiền đề cho việc sử dụng các chức năng của Aspose.PSD một cách liền mạch.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Bước 1: Tải hình ảnh

 Bắt đầu bằng cách tải hình ảnh PSD mẫu vào một phiên bản của`RasterImage` lớp học. Đây là nền tảng cho việc điều chỉnh gamma tiếp theo.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Tải hình ảnh hiện có vào một thể hiện của lớp RasterImage
Image image = Image.load(sourceFile);

// Truyền đối tượng của Hình ảnh sang RasterImage
RasterImage rasterImage = (RasterImage)image;

// Kiểm tra xem RasterImage có được lưu vào bộ nhớ đệm để có hiệu suất tốt hơn không
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Bước 2: Điều chỉnh Gamma

 Bây giờ, điều chỉnh gamma của hình ảnh được tải bằng cách sử dụng`adjustGamma` phương pháp. Tinh chỉnh các giá trị gamma theo yêu cầu của bạn.

```java
// Điều chỉnh gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Bước 3: Tạo TiffOptions

 Tạo một thể hiện của`TiffOptions` cho hình ảnh kết quả. Đặt các thuộc tính khác nhau, chẳng hạn như số bit trên mỗi mẫu và tùy chọn trắc quang, để điều chỉnh đầu ra theo thông số kỹ thuật của bạn.

```java
// Tạo một phiên bản TiffOptions cho hình ảnh kết quả
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Bước 4: Lưu hình ảnh kết quả

 Lưu hình ảnh đã chỉnh sửa sang định dạng TIFF bằng cách sử dụng định dạng đã xác định trước đó`TiffOptions`.

```java
// Lưu hình ảnh thu được sang định dạng TIFF
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Phần kết luận

Chúc mừng! Bạn đã điều chỉnh thành công gamma của hình ảnh bằng Aspose.PSD cho Java. Quá trình này cho phép các nhà phát triển nâng cao chất lượng hình ảnh một cách dễ dàng, góp phần mang lại trải nghiệm trực quan hấp dẫn cho người dùng.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể tìm tài liệu Aspose.PSD ở đâu?

 A1: Bạn có thể truy cập tài liệu tại[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Câu hỏi 2: Làm cách nào để tải xuống Aspose.PSD cho Java?

 A2: Tải xuống thư viện từ[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Câu 3: Tôi có thể mua Aspose.PSD ở đâu?

 A3: Tham quan[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) để mua Aspose.PSD.

### Q4: Có bản dùng thử miễn phí không?

 Đ4: Có, bạn có thể khám phá bản dùng thử miễn phí tại[https://releases.aspose.com/](https://releases.aspose.com/).

### Câu hỏi 5: Tôi có thể tìm kiếm sự hỗ trợ cho Aspose.PSD ở đâu?

 Câu trả lời 5: Để được hỗ trợ, hãy truy cập diễn đàn Aspose.PSD tại[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).