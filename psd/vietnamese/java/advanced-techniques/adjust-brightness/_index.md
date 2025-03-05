---
title: Điều chỉnh độ sáng của hình ảnh bằng Aspose.PSD cho Java
linktitle: Điều chỉnh độ sáng của hình ảnh
second_title: API Java Aspose.PSD
description: Tăng cường độ sáng hình ảnh trong Java với Aspose.PSD. Hướng dẫn từng bước để điều chỉnh độ sáng hình ảnh theo chương trình.
type: docs
weight: 21
url: /vi/java/advanced-techniques/adjust-brightness/
---
## Giới thiệu

Nâng cao hình ảnh là yêu cầu chung trong thiết kế đồ họa và nhiếp ảnh kỹ thuật số. Aspose.PSD cho Java cung cấp một giải pháp mạnh mẽ để điều chỉnh độ sáng hình ảnh theo chương trình. Trong hướng dẫn này, chúng ta sẽ khám phá cách sử dụng thư viện Aspose.PSD cho Java để điều chỉnh độ sáng của hình ảnh theo từng bước.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

-  Aspose.PSD for Java Library: Tải xuống và cài đặt thư viện từ[Aspose.PSD cho tài liệu Java](https://reference.aspose.com/psd/java/).

## Gói nhập khẩu

Để bắt đầu, hãy nhập các gói cần thiết vào dự án Java của bạn. Trong ví dụ này, chúng tôi sẽ sử dụng như sau:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Bây giờ, hãy chia quá trình điều chỉnh độ sáng của hình ảnh thành các bước đơn giản:

## Bước 1: Tải hình ảnh

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Tải hình ảnh hiện có vào một thể hiện của lớp RasterImage
Image image = Image.load(sourceFile);
// Truyền đối tượng của Hình ảnh sang RasterImage
RasterImage rasterImage = (RasterImage) image;

// Kiểm tra xem RasterImage có được lưu vào bộ nhớ đệm hay không và Cache RasterImage để có hiệu suất tốt hơn
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Trong bước này, chúng ta tải hình ảnh mục tiêu và chuyển nó sang một`RasterImage` để xử lý tiếp.

## Bước 2: Điều chỉnh độ sáng

```java
// Điều chỉnh độ sáng
rasterImage.adjustBrightness(-50);
```

 Ở đây, chúng tôi sử dụng`adjustBrightness`phương pháp sửa đổi độ sáng của hình ảnh. Trong ví dụ này, chúng tôi giảm độ sáng đi 50 đơn vị nhưng bạn có thể tùy chỉnh giá trị này dựa trên yêu cầu của mình.

## Bước 3: Đặt TiffOptions

```java
int[] ushort = {8, 8, 8};
// Tạo một phiên bản TiffOptions cho hình ảnh kết quả
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 Cấu hình`TiffOptions` để lưu hình ảnh đã điều chỉnh. Điều chỉnh`bitsPerSample` Và`photometric` tài sản dựa trên nhu cầu cụ thể của bạn.

## Bước 4: Lưu hình ảnh kết quả

```java
// Lưu hình ảnh kết quả
rasterImage.save(destName, tiffOptions);
```

 Cuối cùng, lưu hình ảnh đã sửa đổi bằng cách sử dụng`TiffOptions`.

## Phần kết luận

Việc điều chỉnh độ sáng của hình ảnh theo chương trình được thực hiện dễ dàng với Aspose.PSD cho Java. Hướng dẫn này đã cung cấp hướng dẫn toàn diện về cách triển khai chức năng này trong các ứng dụng Java của bạn.

## Câu hỏi thường gặp

### Q1: Tôi có thể điều chỉnh độ sáng ở các định dạng hình ảnh khác ngoài PSD không?

Câu trả lời 1: Có, Aspose.PSD cho Java hỗ trợ nhiều định dạng hình ảnh khác nhau như JPEG, PNG và TIFF.

### Q2: Làm cách nào để xử lý lỗi trong quá trình điều chỉnh hình ảnh?

Câu trả lời 2: Bạn có thể triển khai xử lý lỗi bằng cách sử dụng khối thử bắt để quản lý các trường hợp ngoại lệ có thể xảy ra.

### Câu 3: Có giới hạn về phạm vi điều chỉnh độ sáng không?

Câu trả lời 3: Phạm vi điều chỉnh tùy thuộc vào nội dung và định dạng hình ảnh, nhưng Aspose.PSD mang đến sự linh hoạt trong việc tùy chỉnh.

### Câu hỏi 4: Tôi có thể sử dụng Aspose.PSD cho Java trong các dự án thương mại không?

 Câu trả lời 4: Có, Aspose.PSD cho Java là một thư viện thương mại và bạn có thể lấy giấy phép từ[đây](https://purchase.aspose.com/buy).

### Câu hỏi 5: Có bản dùng thử miễn phí cho Aspose.PSD cho Java không?

 Câu trả lời 5: Có, bạn có thể khám phá thư viện với bản dùng thử miễn phí từ[đây](https://releases.aspose.com/).