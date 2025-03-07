---
title: Áp dụng Điều chỉnh Cân bằng Màu trong Aspose.PSD cho .NET
linktitle: Áp dụng điều chỉnh cân bằng màu
second_title: API Aspose.PSD .NET
description: Dễ dàng nâng cao màu sắc hình ảnh PSD với tính năng Điều chỉnh Cân bằng Màu của Aspose.PSD cho .NET. Hãy làm theo hướng dẫn từng bước của chúng tôi để có kết quả tuyệt vời.
weight: 14
url: /vi/net/image-adjustment/color-balance-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Áp dụng Điều chỉnh Cân bằng Màu trong Aspose.PSD cho .NET

## Giới thiệu

Chào mừng bạn đến với hướng dẫn toàn diện này về cách áp dụng Điều chỉnh Cân bằng Màu trong Aspose.PSD cho .NET! Aspose.PSD là một thư viện .NET mạnh mẽ cho phép các nhà phát triển làm việc với các tệp PSD một cách hiệu quả. Trong hướng dẫn này, chúng tôi sẽ tập trung vào tính năng Điều chỉnh Cân bằng Màu, cho phép bạn nâng cao độ cân bằng màu của hình ảnh PSD một cách dễ dàng.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.PSD for .NET Library: Tải xuống và cài đặt thư viện từ[Trang web Aspose.PSD](https://releases.aspose.com/psd/net/).
- Môi trường phát triển: Đảm bảo rằng bạn đã thiết lập môi trường phát triển .NET đang hoạt động trên máy của mình.
- Tệp PSD: Chuẩn bị sẵn tệp PSD mà bạn muốn áp dụng Điều chỉnh Cân bằng Màu sắc.

## Nhập không gian tên

Trong dự án .NET của bạn, hãy bao gồm các vùng tên cần thiết để sử dụng các tính năng Aspose.PSD. Thêm các dòng sau vào mã của bạn:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Bây giờ, hãy chia quá trình Điều chỉnh Cân bằng Màu thành nhiều bước:

## Bước 1: Tải tệp PSD

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // Mã cho Điều chỉnh Cân bằng Màu sẽ được thêm vào trong các bước sau.
}
```

## Bước 2: Truy cập và điều chỉnh cân bằng màu

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## Bước 3: Lưu hình ảnh đã điều chỉnh

```csharp
im.Save(outputPath);
```

Bây giờ, bạn đã áp dụng thành công Điều chỉnh cân bằng màu cho tệp PSD của mình bằng Aspose.PSD for .NET!

## Phần kết luận

Chúc mừng! Bạn đã học cách nâng cao sự cân bằng màu sắc của hình ảnh PSD bằng Aspose.PSD cho .NET. Thử nghiệm với các giá trị cân bằng khác nhau để đạt được hiệu ứng hình ảnh mong muốn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể áp dụng Điều chỉnh Cân bằng Màu cho nhiều lớp không?

Câu trả lời 1: Có, bạn có thể duyệt qua tất cả các lớp trong tệp PSD của mình và điều chỉnh độ cân bằng màu nếu cần.

### Câu hỏi 2: Aspose.PSD cho .NET có phù hợp để xử lý hàng loạt tệp PSD không?

A2: Chắc chắn rồi! Aspose.PSD cung cấp khả năng xử lý hàng loạt hiệu quả cho các tệp PSD.

### Câu hỏi 3: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.PSD cho .NET?

 A3: Tham quan[Giấy phép tạm thời Aspose.PSD](https://purchase.aspose.com/temporary-license/) để xin giấy phép tạm thời.

### Câu hỏi 4: Tôi có thể tìm thêm ví dụ và tài liệu ở đâu?

 A4: Khám phá[Tài liệu Aspose.PSD](https://reference.aspose.com/psd/net/) để biết ví dụ và hướng dẫn chi tiết.

### Câu hỏi 5: Aspose.PSD dành cho .NET có những tùy chọn hỗ trợ nào?

 A5: Tham quan[Diễn đàn Aspose.PSD](https://forum.aspose.com/c/psd/34) để được cộng đồng hỗ trợ và thảo luận.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
