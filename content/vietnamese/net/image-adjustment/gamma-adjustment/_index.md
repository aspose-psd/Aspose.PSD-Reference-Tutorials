---
title: Triển khai Điều chỉnh Gamma trong Aspose.PSD cho .NET
linktitle: Thực hiện điều chỉnh Gamma
second_title: API Aspose.PSD .NET
description: Khám phá sức mạnh của Aspose.PSD cho .NET với hướng dẫn từng bước của chúng tôi về cách triển khai Điều chỉnh Gamma. Tinh chỉnh độ sáng và độ tương phản của hình ảnh một cách dễ dàng.
type: docs
weight: 12
url: /vi/net/image-adjustment/gamma-adjustment/
---
## Giới thiệu

Chào mừng bạn đến với hướng dẫn toàn diện về cách triển khai Điều chỉnh Gamma trong Aspose.PSD cho .NET! Điều chỉnh gamma là một kỹ thuật xử lý hình ảnh quan trọng cho phép bạn tinh chỉnh độ sáng và độ tương phản của hình ảnh. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình sử dụng thư viện Aspose.PSD mạnh mẽ cho .NET.

## Điều kiện tiên quyết

Trước khi đi sâu vào triển khai, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.PSD for .NET Library: Đảm bảo rằng bạn đã cài đặt thư viện Aspose.PSD cho .NET. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/psd/net/).

- .NET Framework: Hướng dẫn này giả sử bạn có hiểu biết cơ bản về phát triển .NET và đã cài đặt .NET Framework.

- Môi trường phát triển tích hợp (IDE): Chọn IDE ưa thích của bạn để phát triển .NET, chẳng hạn như Visual Studio.

## Nhập không gian tên

Trong dự án .NET của bạn, hãy bắt đầu bằng cách nhập các vùng tên cần thiết để làm việc với Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Bước 1: Thiết lập dự án của bạn

Tạo một dự án .NET mới trong IDE bạn đã chọn. Đảm bảo thêm tài liệu tham khảo vào thư viện Aspose.PSD.

## Bước 2: Xác định thư mục tài liệu

```csharp
string dataDir = "Your Document Directory";
```

## Bước 3: Tải hình ảnh

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // Các bước bổ sung sẽ được thực hiện bên trong khối sử dụng này.
}
```

## Bước 4: Truyền tới dữ liệu RasterImage và Cache

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## Bước 5: Điều chỉnh Gamma

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## Bước 6: Tạo TiffOptions và lưu

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## Phần kết luận

Chúc mừng! Bạn đã triển khai thành công Điều chỉnh Gamma bằng Aspose.PSD cho .NET. Thư viện mạnh mẽ này cung cấp các khả năng mạnh mẽ để xử lý hình ảnh, khiến nó trở thành một công cụ có giá trị cho các nhà phát triển .NET.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể tìm tài liệu Aspose.PSD ở đâu?

 A1: Bạn có thể tham khảo tài liệu[đây](https://reference.aspose.com/psd/net/).

### Câu hỏi 2: Làm cách nào để tải xuống Aspose.PSD cho .NET?

 A2: Bạn có thể tải xuống thư viện.[đây](https://releases.aspose.com/psd/net/).

### Câu 3: Có bản dùng thử miễn phí không?

 Trả lời 3: Có, bạn có thể dùng thử miễn phí.[đây](https://releases.aspose.com/).

### Câu hỏi 4: Tôi có thể nhận hỗ trợ cho Aspose.PSD ở đâu?

 A4: Bạn có thể truy cập diễn đàn hỗ trợ.[đây](https://forum.aspose.com/c/psd/34).

### Câu hỏi 5: Tôi có cần giấy phép tạm thời không?

 Câu trả lời 5: Nếu được yêu cầu, bạn có thể xin giấy phép tạm thời.[đây](https://purchase.aspose.com/temporary-license/).