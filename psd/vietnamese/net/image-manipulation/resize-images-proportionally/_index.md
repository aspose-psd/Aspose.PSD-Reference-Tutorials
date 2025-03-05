---
title: Thay đổi kích thước hình ảnh theo tỷ lệ trong Aspose.PSD cho .NET
linktitle: Thay đổi kích thước hình ảnh theo tỷ lệ
second_title: API Aspose.PSD .NET
description: Khám phá khả năng thay đổi kích thước hình ảnh liền mạch với Aspose.PSD cho .NET. Tải xuống thư viện, làm theo hướng dẫn của chúng tôi và nâng cao khả năng xử lý hình ảnh của bạn.
type: docs
weight: 14
url: /vi/net/image-manipulation/resize-images-proportionally/
---
Trong lĩnh vực xử lý hình ảnh, Aspose.PSD cho .NET nổi bật như một bộ công cụ mạnh mẽ, cung cấp cho các nhà phát triển khả năng thay đổi kích thước hình ảnh theo tỷ lệ một cách dễ dàng. Trong hướng dẫn từng bước này, chúng tôi sẽ hướng dẫn bạn quy trình thay đổi kích thước hình ảnh bằng Aspose.PSD cho .NET, đảm bảo rằng hình ảnh của bạn duy trì tỷ lệ hoàn hảo.

## Giới thiệu

Thay đổi kích thước hình ảnh theo tỷ lệ là một nhiệm vụ phổ biến trong nhiều ứng dụng và Aspose.PSD cho .NET đơn giản hóa quy trình này cho các nhà phát triển. Cho dù bạn đang làm việc trên ứng dụng web, phần mềm máy tính để bàn hay ứng dụng di động, việc hiểu cách thay đổi kích thước hình ảnh trong khi vẫn duy trì tỷ lệ khung hình của chúng là rất quan trọng để duy trì sự hấp dẫn và nhất quán về mặt hình ảnh.

## Điều kiện tiên quyết

Trước khi đi sâu vào phép thuật thay đổi kích thước bằng Aspose.PSD cho .NET, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

1.  Aspose.PSD for .NET Library: Đảm bảo rằng bạn đã cài đặt thư viện Aspose.PSD cho .NET. Bạn có thể tải nó xuống từ[Aspose.PSD cho các bản phát hành .NET](https://releases.aspose.com/psd/net/) trang.

2. Thư mục Tài liệu: Tạo một thư mục để lưu trữ tài liệu của bạn và thay thế "Thư mục Tài liệu của Bạn" trong mã được cung cấp bằng đường dẫn thực tế đến thư mục này.

Bây giờ bạn đã thiết lập các điều kiện tiên quyết, hãy chuyển sang hướng dẫn từng bước.

## Nhập không gian tên

```csharp
using Aspose.PSD.ImageOptions;
```

Nhập các không gian tên cần thiết để truy cập các lớp và phương thức được yêu cầu.

## Bước 1: Tải hình ảnh

```csharp
// Đường dẫn đến thư mục tài liệu.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Tải hình ảnh hiện có vào một thể hiện của lớp RasterImage
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// Các bước còn lại hãy thực hiện tại đây
}
```

 Tải hình ảnh nguồn bằng cách sử dụng`Image.Load` phương pháp.

## Bước 2: Chỉ định chiều rộng và chiều cao

```csharp
// Chỉ định chiều rộng và chiều cao
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Xác định chiều rộng và chiều cao mới cho hình ảnh đã thay đổi kích thước. Trong ví dụ này, chiều rộng và chiều cao giảm một nửa nhưng bạn có thể điều chỉnh các giá trị này dựa trên yêu cầu của mình.

## Bước 3: Lưu hình ảnh đã thay đổi kích thước

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Lưu hình ảnh đã thay đổi kích thước bằng cách sử dụng`Save` phương pháp với các tùy chọn được chỉ định. Trong trường hợp này, chúng tôi lưu nó dưới dạng tệp PNG.

## Phần kết luận

Thay đổi kích thước hình ảnh theo tỷ lệ trong Aspose.PSD cho .NET là một quá trình đơn giản giúp tăng thêm giá trị cho quy trình xử lý hình ảnh của bạn. Hướng dẫn này đã trang bị cho bạn kiến thức để tích hợp liền mạch chức năng này vào các ứng dụng của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể thay đổi kích thước hình ảnh theo kích thước cụ thể không?

Trả lời 1: Có, bạn có thể tùy chỉnh chiều rộng và chiều cao mới theo yêu cầu của bạn trong mã.

### Câu hỏi 2: Aspose.PSD cho .NET có phù hợp để thay đổi kích thước hình ảnh hàng loạt không?

A2: Chắc chắn rồi! Bạn có thể kết hợp các bước này thành một vòng lặp để xử lý hàng loạt nhiều hình ảnh.

### Câu hỏi 3: Có các tính năng xử lý hình ảnh khác trong Aspose.PSD cho .NET không?

Câu trả lời 3: Có, Aspose.PSD cho .NET cung cấp nhiều tính năng, bao gồm cắt xén, xoay và áp dụng các bộ lọc cho hình ảnh.

### Câu hỏi 4: Có bản dùng thử miễn phí dành cho Aspose.PSD cho .NET không?

 Câu trả lời 4: Có, bạn có thể khám phá các khả năng của Aspose.PSD dành cho .NET bằng bản dùng thử miễn phí. Thăm nom[đây](https://releases.aspose.com/) để bắt đầu.

### Câu hỏi 5: Tôi có thể tìm hỗ trợ cho Aspose.PSD cho .NET ở đâu?

 A5: Tham quan[Aspose.PSD cho diễn đàn .NET](https://forum.aspose.com/c/psd/34) để được cộng đồng hỗ trợ và thảo luận.