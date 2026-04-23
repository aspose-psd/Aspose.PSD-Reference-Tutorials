---
date: 2026-02-25
description: Tìm hiểu cách chuyển đổi PSD sang TIFF và thực hiện điều chỉnh độ tương
  phản hình ảnh bằng Aspose.PSD cho Java, một thư viện xử lý ảnh Java hàng đầu.
linktitle: Convert PSD to TIFF and Adjust Contrast
second_title: Aspose.PSD Java API
title: Cách chuyển đổi PSD sang TIFF và điều chỉnh độ tương phản với Aspose.PSD cho
  Java
url: /vi/java/advanced-techniques/adjust-contrast/
weight: 22
---

.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Chuyển Đổi PSD sang TIFF và Điều Chỉnh Độ Tương Phản với Aspose.PSD cho Java

## Giới thiệu

Nếu bạn cần **convert PSD to TIFF** trong khi cũng tinh chỉnh chất lượng hình ảnh của đồ họa, bạn đang ở đúng nơi. Trong hướng dẫn này, chúng tôi sẽ đi qua quy trình hoàn chỉnh bằng cách sử dụng Aspose.PSD cho Java — một thư viện **java image manipulation** mạnh mẽ. Bạn sẽ học cách tăng **image contrast adjustment**, lưu trữ dữ liệu raster lớn để cải thiện hiệu năng, và cuối cùng **save image as TIFF** cho các bước xử lý tiếp theo. Hãy bắt đầu!

## Câu trả lời nhanh
- **What does “adjust contrast” mean?** Nó thay đổi sự chênh lệch giữa các pixel tối nhất và sáng nhất, làm nổi bật chi tiết.  
- **Which library handles this?** Aspose.PSD for Java – một bộ công cụ xử lý ảnh đầy đủ tính năng.  
- **Do I need a license?** Một **temporary aspose license** hoạt động cho việc thử nghiệm; cần giấy phép đầy đủ cho môi trường sản xuất.  
- **Tôi có thể **convert PSD to TIFF**?** Chắc chắn – chúng ta sẽ sử dụng `TiffOptions` để xuất ảnh đã xử lý.  
- **How long does the code take to run?** Thông thường dưới một giây cho các tệp PSD kích thước tiêu chuẩn trên phần cứng hiện đại.

## Điều chỉnh Độ Tương Phản của Hình Ảnh là gì?

Việc điều chỉnh độ tương phản thay đổi dải tông của một hình ảnh, tăng cường sự khác biệt giữa các vùng sáng và tối. Điều này đặc biệt hữu ích khi hình ảnh trông phẳng sau khi quét hoặc khi chuẩn bị đồ họa để in.

## Tại sao nên sử dụng Aspose.PSD cho Java?

- **Rich format support** – mở, chỉnh sửa và **save image as TIFF**, PNG, JPEG và nhiều định dạng khác.  
- **High performance** – caching và tối ưu hoá raster‑image giảm tải bộ nhớ, rất quan trọng đối với các tệp PSD lớn.  
- **Straight‑forward API** – các lời gọi phương thức đơn như `adjustContrast` làm cho mã dễ đọc và bảo trì.  
- **Comprehensive java image manipulation** capabilities phù hợp cho cả script đơn giản và ứng dụng cấp doanh nghiệp.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn bạn có:

- Kiến thức cơ bản về lập trình Java.  
- Thư viện Aspose.PSD cho Java đã được cài đặt. Bạn có thể tải xuống [here](https://releases.aspose.com/psd/java/).

## Nhập các Gói

Thêm các import cần thiết vào lớp Java của bạn:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Bước 1: Tải ảnh

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

Chúng ta tải tệp PSD nguồn (`sample.psd`) vào một đối tượng `Image`, đối tượng này là điểm khởi đầu cho mọi xử lý tiếp theo.

## Bước 2: Ép kiểu sang RasterImage và Lưu trữ Dữ liệu

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Ép kiểu sang `RasterImage` cho phép chúng ta truy cập các thao tác ở mức pixel. Caching cải thiện hiệu năng, đặc biệt với các tệp lớn.

## Cách Điều chỉnh Độ Tương Phản của Ảnh

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

Phương thức `adjustContrast` nhận một số nguyên đại diện cho phần trăm thay đổi. Trong ví dụ này chúng ta tăng độ tương phản lên **50 %**.

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

Ở đây chúng ta cấu hình `TiffOptions` (bits per sample, photometric interpretation) và **save image as TIFF**. Bước này hoàn thành quy trình **convert PSD to TIFF**.

## Các vấn đề thường gặp và giải pháp
- **Image not cached:** Luôn gọi `cacheData()` cho các PSD lớn để tránh `OutOfMemoryError`.  
- **Unexpected color shift:** Kiểm tra `setPhotometric` khớp với không gian màu mục tiêu của bạn (RGB vs. CMYK).  
- **File not found:** Đảm bảo `dataDir` trỏ tới thư mục đúng và tên tệp được viết chính xác.

## Câu hỏi thường gặp

### Q1: Aspose.PSD có tương thích với các định dạng ảnh khác nhau không?

A1: Có, Aspose.PSD hỗ trợ nhiều định dạng ảnh, cung cấp tính linh hoạt cho dự án của bạn.

### Q2: Làm thế nào để tôi có được giấy phép tạm thời cho Aspose.PSD?

A2: Bạn có thể nhận giấy phép tạm thời [here](https://purchase.aspose.com/temporary-license/).

### Q3: Tôi có thể tìm tài liệu Aspose.PSD ở đâu?

A3: Tài liệu có sẵn [here](https://reference.aspose.com/psd/java/).

### Q4: Các tùy chọn hỗ trợ nào có sẵn cho Aspose.PSD?

A4: Để được hỗ trợ, truy cập [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q5: Tôi có thể mua Aspose.PSD không?

A5: Có, bạn có thể mua Aspose.PSD [here](https://purchase.aspose.com/buy).

## Kết luận

Bây giờ bạn đã biết **how to convert PSD to TIFF** và thực hiện **image contrast adjustment** bằng Aspose.PSD cho Java. Các bước này cho phép bạn kiểm soát chi tiết chất lượng ảnh trong khi giữ mã nguồn sạch sẽ và dễ bảo trì. Hãy tự do thử nghiệm các phương pháp điều chỉnh khác như `adjustBrightness` hoặc `adjustGamma` để phù hợp với nhu cầu cụ thể của bạn.

---

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}