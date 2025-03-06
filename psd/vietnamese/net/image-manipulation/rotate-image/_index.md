---
title: Xoay hình ảnh trong Aspose.PSD cho .NET
linktitle: Xoay một hình ảnh
second_title: API Aspose.PSD .NET
description: Tìm hiểu cách xoay hình ảnh dễ dàng trong .NET với Aspose.PSD. Thực hiện theo hướng dẫn từng bước của chúng tôi.
weight: 15
url: /vi/net/image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xoay hình ảnh trong Aspose.PSD cho .NET

## Giới thiệu

Nếu bạn đang đi sâu vào thế giới xử lý hình ảnh bằng .NET, Aspose.PSD là công cụ phù hợp để xử lý hình ảnh liền mạch và hiệu quả. Trong hướng dẫn này, chúng ta sẽ tập trung vào một nhiệm vụ cơ bản – xoay hình ảnh bằng Aspose.PSD cho .NET. Hãy làm theo khi chúng tôi chia quy trình thành các bước đơn giản, có thể thực hiện được.

## Điều kiện tiên quyết

Trước khi chúng ta bắt đầu, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.PSD for .NET Library: Tải xuống và cài đặt thư viện từ[Tài liệu Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- Thư mục tài liệu của bạn: Thiết lập thư mục lưu trữ hình ảnh của bạn. Thay thế "Thư mục tài liệu của bạn" trong đoạn mã bằng đường dẫn đến thư mục này.

## Nhập không gian tên

Đảm bảo bao gồm các không gian tên cần thiết để truy cập chức năng Aspose.PSD. Thêm các dòng sau vào đầu dự án .NET của bạn:

```csharp
using Aspose.PSD.ImageOptions;
```

## Bước 1: Tải hình ảnh

```csharp
string sourceFile = dataDir + @"sample.psd";

// Tải hình ảnh hiện có vào một thể hiện của lớp RasterImage
using (Image image = Image.Load(sourceFile))
{
```

## Bước 2: Xoay hình ảnh

```csharp
    // Xoay hình ảnh 270 độ theo chiều kim đồng hồ
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Bước 3: Lưu hình ảnh đã xoay

```csharp
    // Lưu hình ảnh đã xoay dưới dạng tệp JPEG
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

Thế thôi! Chỉ với vài dòng mã, bạn đã xoay hình ảnh thành công bằng Aspose.PSD cho .NET.

## Phần kết luận

Trong hướng dẫn này, chúng ta đã khám phá những kiến thức cơ bản về xoay hình ảnh bằng Aspose.PSD cho .NET. Aspose.PSD cung cấp một bộ công cụ mạnh mẽ để xử lý hình ảnh, khiến nó trở thành một thư viện cần thiết cho các nhà phát triển .NET. Thử nghiệm với các góc quay khác nhau và khám phá các khả năng khác để nâng cao quy trình xử lý hình ảnh của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể xoay hình ảnh theo một góc tùy chỉnh bằng Aspose.PSD không?

 Có, Aspose.PSD cho phép bạn chỉ định góc xoay tùy chỉnh. Đơn giản chỉ cần thay thế`RotateFlipType.Rotate270FlipNone` phù hợp với góc xoay mong muốn của bạn.

### Câu hỏi 2: Aspose.PSD có tương thích với nhiều định dạng hình ảnh khác nhau không?

 Tuyệt đối. Aspose.PSD hỗ trợ nhiều định dạng hình ảnh, bao gồm PSD, JPEG, PNG, v.v. Kiểm tra[tài liệu](https://reference.aspose.com/psd/net/) để có danh sách đầy đủ.

### Câu hỏi 3: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.PSD?

 Ghé thăm[trang giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) trên trang web Aspose để lấy giấy phép tạm thời cho mục đích đánh giá.

### Câu hỏi 4: Tôi có thể tìm hỗ trợ cho Aspose.PSD ở đâu?

 Nếu có bất kỳ thắc mắc hoặc trợ giúp nào, hãy truy cập[Diễn đàn Aspose.PSD](https://forum.aspose.com/c/psd/34) và kết nối với cộng đồng.

### Câu hỏi 5: Tôi có thể mua Aspose.PSD cho mục đích thương mại không?

 Chắc chắn. Khám phá[trang mua hàng](https://purchase.aspose.com/buy) để có được giấy phép phù hợp với nhu cầu của bạn.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
