---
date: 2025-12-21
description: Tìm hiểu cách điều chỉnh độ tương phản của hình ảnh bằng Aspose.PSD cho
  Java, một thư viện xử lý ảnh Java hàng đầu, và chuyển đổi PSD sang TIFF một cách
  hiệu quả.
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: Cách điều chỉnh độ tương phản của hình ảnh bằng Aspose.PSD cho Java
url: /vi/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Điều Chỉnh Độ Tương Phản của Hình Ảnh với Aspose.PSD cho Java

## Giới thiệu

Nếu bạn đang tìm kiếm **cách điều chỉnh độ tương phản** trong các dự án Java của mình, bạn đã đến đúng nơi. Aspose.PSD cho Java là một **thư viện xử lý ảnh java** mạnh mẽ cho phép bạn tinh chỉnh các thuộc tính của hình ảnh như độ tương phản, độ sáng và nhiều hơn nữa. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn chi tiết các bước để tăng độ tương phản của tệp PSD và sau đó **chuyển đổi PSD sang TIFF** cho các quy trình downstream.

## Câu trả lời nhanh
- **“adjust contrast” có nghĩa là gì?** Nó thay đổi sự chênh lệch giữa các pixel tối nhất và sáng nhất, làm nổi bật chi tiết.
- **Thư viện nào thực hiện việc này?** Aspose.PSD cho Java – một bộ công cụ xử lý ảnh đầy đủ tính năng.
- **Tôi có cần giấy phép không?** Giấy phép tạm thời hoạt động cho việc thử nghiệm; giấy phép đầy đủ cần thiết cho môi trường sản xuất.
- **Tôi có thể lưu kết quả dưới dạng TIFF không?** Có, chúng ta sẽ sử dụng `TiffOptions` để xuất hình ảnh đã xử lý.
- **Mã chạy mất bao lâu?** Thông thường dưới một giây cho các tệp PSD kích thước tiêu chuẩn.

## Điều chỉnh độ tương phản là gì?

Điều chỉnh độ tương phản thay đổi dải tông của một hình ảnh, tăng cường sự khác biệt giữa các vùng sáng và tối. Điều này đặc biệt hữu ích khi hình ảnh trông phẳng sau khi quét hoặc khi chuẩn bị đồ họa để in.

## Tại sao nên sử dụng Aspose.PSD cho Java?

- **Hỗ trợ định dạng phong phú** – mở, chỉnh sửa và lưu PSD, TIFF, PNG, JPEG và nhiều định dạng khác.
- **Hiệu năng cao** – bộ nhớ đệm và tối ưu hoá raster‑image giảm tải bộ nhớ.
- **API đơn giản** – các lời gọi phương thức đơn như `adjustContrast` giúp mã dễ đọc.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn có:

- Kiến thức cơ bản về lập trình Java.
- Thư viện Aspose.PSD cho Java đã được cài đặt. Bạn có thể tải xuống [tại đây](https://releases.aspose.com/psd/java/).

## Nhập các gói

Add the required imports to your Java class:

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

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

Chúng ta tải tệp PSD nguồn (`sample.psd`) vào một đối tượng `Image`, đây là điểm khởi đầu cho mọi xử lý tiếp theo.

## Bước 2: Ép kiểu sang RasterImage và lưu vào bộ nhớ đệm

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Ép kiểu sang `RasterImage` cho phép chúng ta truy cập các thao tác ở mức độ pixel. Việc lưu vào bộ nhớ đệm cải thiện hiệu năng, đặc biệt với các tệp lớn.

## Cách điều chỉnh độ tương phản của hình ảnh

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

Phương thức `adjustContrast` nhận một số nguyên đại diện cho phần trăm thay đổi. Trong ví dụ này, chúng ta tăng độ tương phản lên **50 %**.

## Chuyển đổi PSD sang TIFF bằng Aspose.PSD

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Ở đây chúng ta cấu hình `TiffOptions` (số bit mỗi mẫu, cách diễn giải quang học) và ghi hình ảnh đã tăng độ tương phản ra tệp TIFF.

## Các vấn đề thường gặp và giải pháp
- **Hình ảnh chưa được lưu vào bộ nhớ đệm:** Luôn gọi `cacheData()` cho các PSD lớn để tránh `OutOfMemoryError`.
- **Màu sắc bị dịch chuyển không mong muốn:** Kiểm tra `setPhotometric` có khớp với không gian màu mục tiêu của bạn (RGB vs. CMYK).
- **Không tìm thấy tệp:** Đảm bảo `dataDir` trỏ tới thư mục đúng và tên tệp được viết chính xác.

## Câu hỏi thường gặp

### Q1: Aspose.PSD có tương thích với các định dạng ảnh khác nhau không?

A1: Có, Aspose.PSD hỗ trợ nhiều định dạng ảnh, mang lại tính linh hoạt cho các dự án của bạn.

### Q2: Làm thế nào để tôi có được giấy phép tạm thời cho Aspose.PSD?

A2: Bạn có thể nhận giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

### Q3: Tôi có thể tìm tài liệu Aspose.PSD ở đâu?

A3: Tài liệu có sẵn [tại đây](https://reference.aspose.com/psd/java/).

### Q4: Các tùy chọn hỗ trợ nào có sẵn cho Aspose.PSD?

A4: Để được hỗ trợ, hãy truy cập [diễn đàn Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Tôi có thể mua Aspose.PSD không?

A5: Có, bạn có thể mua Aspose.PSD [tại đây](https://purchase.aspose.com/buy).

## Kết luận

Bây giờ bạn đã biết **cách điều chỉnh độ tương phản** của hình ảnh PSD bằng Aspose.PSD cho Java và cách **chuyển đổi PSD sang TIFF** để xử lý tiếp theo. Các bước này cho phép bạn kiểm soát chi tiết chất lượng ảnh trong khi giữ mã nguồn sạch sẽ và dễ bảo trì. Hãy tự do thử nghiệm các phương pháp điều chỉnh ảnh khác như `adjustBrightness` hoặc `adjustGamma` để phù hợp với nhu cầu cụ thể của bạn.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}