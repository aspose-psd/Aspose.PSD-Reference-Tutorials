---
title: Triển khai Điều chỉnh độ sáng trong Aspose.PSD cho .NET
linktitle: Thực hiện điều chỉnh độ sáng
second_title: API Aspose.PSD .NET
description: Khám phá sức mạnh của Aspose.PSD cho .NET trong việc điều chỉnh độ sáng hình ảnh. Hãy làm theo hướng dẫn từng bước của chúng tôi để triển khai liền mạch.
type: docs
weight: 10
url: /vi/net/image-adjustment/brightness-adjustment/
---
## Giới thiệu

Nâng cao và điều chỉnh các thuộc tính hình ảnh là một yêu cầu phổ biến trong các ứng dụng khác nhau và Aspose.PSD cho .NET cung cấp một giải pháp mạnh mẽ để thao tác các tệp PSD một cách liền mạch. Một thao tác như vậy là điều chỉnh độ sáng, cho phép bạn sửa đổi độ sáng của hình ảnh một cách dễ dàng.

Trong hướng dẫn này, chúng ta sẽ tìm hiểu quy trình triển khai điều chỉnh độ sáng bằng Aspose.PSD cho .NET. Hãy làm theo các bước bên dưới để hiểu toàn diện về cách kết hợp các điều chỉnh độ sáng vào tệp PSD của bạn.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Thư viện Aspose.PSD cho .NET: Tải xuống và cài đặt thư viện Aspose.PSD cho .NET từ[Liên kết tải xuống](https://releases.aspose.com/psd/net/).

-  Thư mục Tài liệu: Thiết lập một thư mục để lưu trữ các tệp PSD của bạn và cập nhật`dataDir` biến trong đoạn mã được cung cấp kèm theo đường dẫn đến thư mục tài liệu của bạn.

## Nhập không gian tên

Trong dự án .NET của bạn, hãy bao gồm các vùng tên cần thiết để truy cập chức năng Aspose.PSD. Thêm các không gian tên sau vào mã của bạn:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

Bây giờ, hãy chia ví dụ thành nhiều bước:

## Bước 1: Tải tệp PSD

```csharp
// Đường dẫn đến thư mục tài liệu.
string dataDir = "Your Document Directory";
string sourceFile = dataDir + @"sample.psd";

// Tải tệp PSD bằng Aspose.PSD
using (var image = (PsdImage)Image.Load(sourceFile))
{
    // Mã của bạn cho các bước tiếp theo ở đây
}
```

## Bước 2: Lấy hình ảnh raster

```csharp
// Lấy hình ảnh raster từ tệp PSD đã tải
RasterCachedImage rasterImage = image;
```

## Bước 3: Điều chỉnh độ sáng

```csharp
// Đặt giá trị độ sáng. Các giá trị độ sáng được chấp nhận nằm trong khoảng [-255, 255].
rasterImage.AdjustBrightness(-50);
```

## Bước 4: Lưu hình ảnh đã sửa đổi

```csharp
// Lưu hình ảnh đã sửa đổi với độ sáng đã điều chỉnh
string destName = dataDir + @"AdjustBrightness_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
rasterImage.Save(destName, tiffOptions);
```

Bây giờ chúng tôi đã chia ví dụ thành các bước có thể quản lý được, bạn có thể tích hợp liền mạch khả năng điều chỉnh độ sáng vào dự án .NET của mình bằng Aspose.PSD.

## Phần kết luận

Aspose.PSD for .NET đơn giản hóa quá trình thực hiện điều chỉnh độ sáng trong tệp PSD. Bằng cách làm theo hướng dẫn từng bước được cung cấp ở trên, bạn có thể dễ dàng nâng cao sức hấp dẫn trực quan cho hình ảnh của mình. Thử nghiệm với các giá trị độ sáng khác nhau để đạt được kết quả mong muốn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể tìm tài liệu về Aspose.PSD cho .NET ở đâu?

 A1: Tài liệu có sẵn[đây](https://reference.aspose.com/psd/net/).

### Câu hỏi 2: Làm cách nào tôi có thể tải xuống thư viện Aspose.PSD cho .NET?

 A2: Bạn có thể tải xuống thư viện từ[trang phát hành](https://releases.aspose.com/psd/net/).

### Câu hỏi 3: Có bản dùng thử miễn phí dành cho Aspose.PSD cho .NET không?

 Câu trả lời 3: Có, bạn có thể truy cập bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 4: Tôi có thể nhận hỗ trợ cho Aspose.PSD cho .NET ở đâu?

 A4: Để được hỗ trợ, hãy truy cập[Diễn đàn Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Câu hỏi 5: Làm cách nào để có được giấy phép tạm thời cho Aspose.PSD cho .NET?

 Câu trả lời 5: Bạn có thể có được giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).