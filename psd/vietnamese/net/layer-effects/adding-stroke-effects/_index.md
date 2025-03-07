---
title: Thêm hiệu ứng nét vẽ vào các lớp trong Aspose.PSD cho .NET
linktitle: Thêm hiệu ứng đột quỵ vào các lớp
second_title: API Aspose.PSD .NET
description: Nâng cao tính thẩm mỹ của hình ảnh với Aspose.PSD cho .NET. Tìm hiểu cách thêm hiệu ứng nét theo từng bước. Tải xuống, mua hoặc dùng thử bản dùng thử miễn phí ngay bây giờ.
weight: 10
url: /vi/net/layer-effects/adding-stroke-effects/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thêm hiệu ứng nét vẽ vào các lớp trong Aspose.PSD cho .NET

## Giới thiệu

Chào mừng bạn đến với hướng dẫn từng bước này về cách thêm hiệu ứng nét vẽ vào các lớp trong Aspose.PSD cho .NET. Việc nâng cao sự hấp dẫn trực quan cho hình ảnh của bạn thật dễ dàng với hiệu ứng nét vẽ và Aspose.PSD làm cho việc này trở nên liền mạch đối với các nhà phát triển .NET. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn thực hiện quy trình, cung cấp các bước và ví dụ rõ ràng để giúp bạn nắm vững tính năng mạnh mẽ này.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

- Aspose.PSD for .NET: Tải xuống và cài đặt thư viện Aspose.PSD từ[trang web](https://releases.aspose.com/psd/net/).

- Thư mục tài liệu: Chuẩn bị một thư mục chứa tài liệu PSD mà bạn muốn áp dụng hiệu ứng đột quỵ.

- Thư mục đầu ra: Có một thư mục riêng để lưu trữ hình ảnh đầu ra với các hiệu ứng nét.

- Visual Studio: Đảm bảo bạn đã thiết lập Visual Studio hoặc bất kỳ môi trường phát triển .NET ưa thích nào khác.

## Nhập không gian tên

Trong dự án .NET của bạn, hãy bao gồm các vùng tên cần thiết để tận dụng chức năng Aspose.PSD:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## Bước 1: Tải tài liệu PSD

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Mã của bạn để tải tài liệu PSD có ở đây
}
```

## Bước 2: Thêm hiệu ứng nét màu

```csharp
// Thêm màu tô, tại vị trí Bên trong
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Bước 3: Vị trí bên ngoài

```csharp
// Thêm màu tô, ở vị trí Bên ngoài
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Bước 4: Vị trí trung tâm

```csharp
// Thêm màu tô vào vị trí Center
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Lặp lại các bước tương tự cho các màu tô Chuyển màu và Mẫu, điều chỉnh cài đặt cho phù hợp.

## Phần kết luận

Chúc mừng! Bạn đã học thành công cách thêm hiệu ứng nét vẽ vào các lớp bằng Aspose.PSD cho .NET. Thử nghiệm với các cài đặt khác nhau để đạt được tác động trực quan mong muốn trong hình ảnh của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể chỉ áp dụng hiệu ứng nét vẽ cho các lớp cụ thể không?

Câu trả lời 1: Có, bạn có thể nhắm mục tiêu các lớp cụ thể bằng cách điều chỉnh chỉ mục lớp trong mã.

### Câu hỏi 2: Aspose.PSD có tương thích với .NET framework mới nhất không?

A2: Chắc chắn rồi! Aspose.PSD được thiết kế để tích hợp liền mạch với các khung .NET mới nhất.

### Câu hỏi 3: Làm cách nào để tùy chỉnh màu nét?

 A3: Đơn giản chỉ cần sửa đổi`Color` thuộc tính trong mã để đạt được màu nét mong muốn.

### Câu hỏi 4: Aspose.PSD có hỗ trợ xử lý hàng loạt cho nhiều tệp PSD không?

Câu trả lời 4: Có, bạn có thể lặp qua nhiều tệp PSD và áp dụng hiệu ứng nét vẽ bằng cách sử dụng phương pháp tương tự.

### Câu hỏi 5: Tôi có thể sử dụng phiên bản dùng thử trước khi mua Aspose.PSD không?

 A5: Chắc chắn rồi! Lấy[dùng thử miễn phí](https://releases.aspose.com/) để khám phá các khả năng của Aspose.PSD trước khi mua hàng.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
