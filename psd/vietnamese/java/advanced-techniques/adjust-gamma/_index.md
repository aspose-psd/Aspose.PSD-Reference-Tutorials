---
date: 2026-02-27
description: Tìm hiểu cách điều chỉnh gamma trong xử lý ảnh Java với Aspose.PSD, chuyển
  đổi PSD sang TIFF và khắc phục hình ảnh bị phai màu trong một hướng dẫn ngắn gọn.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Cách điều chỉnh Gamma trong xử lý ảnh Java với Aspose.PSD
url: /vi/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Điều Chỉnh Gamma trong Xử Lý Hình Ảnh Java với Aspose.PSD

## Giới thiệu

Nếu bạn đang làm việc với **java image processing**, việc học **how to adjust gamma** là một kỹ thuật cơ bản để cải thiện độ sáng và độ tương phản mà không mất chi tiết. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn cách sử dụng **Aspose.PSD for Java** để áp dụng gamma correction cho tệp PSD, **convert PSD to TIFF**, và tránh **washed‑out image**. Bạn sẽ thấy tại sao cách tiếp cận này nhanh, đáng tin cậy và hoàn hảo cho các pipeline xử lý hình ảnh phía máy chủ.

## Câu trả lời nhanh
- **Gamma correction làm gì?** Nó tái ánh xạ các giá trị độ sáng để làm cho các khu vực tối sáng hơn hoặc các khu vực sáng tối hơn trong khi vẫn giữ chi tiết tổng thể.  
- **Thư viện nào xử lý việc này?** Aspose.PSD for Java cung cấp phương thức `adjustGamma` chuyên dụng cho hình ảnh raster.  
- **Tôi có thể convert PSD to TIFF trong cùng một quy trình không?** Có – sau khi điều chỉnh gamma, bạn có thể lưu trực tiếp hình ảnh sang TIFF bằng cách sử dụng `TiffOptions`.  
- **Tôi có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí hoạt động cho việc kiểm tra; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Phiên bản Java nào được hỗ trợ?** Aspose.PSD hỗ trợ Java 8 trở lên.

## Cách Điều Chỉnh Gamma trong Xử Lý Hình Ảnh Java
Điều chỉnh gamma là một phần cốt lõi của bất kỳ **java image processing tutorial** nào liên quan đến độ sáng hoặc độ tương phản. Dưới đây chúng tôi sẽ phân tích các bước, giải thích lý do mỗi dòng quan trọng, và cho bạn thấy cách tích hợp quy trình này vào codebase hiện có của bạn.

## Gamma Correction trong Java là gì?
Gamma correction thay đổi mối quan hệ phi tuyến giữa các giá trị pixel đã mã hoá và độ sáng hiển thị. Bằng cách tinh chỉnh đường cong gamma, bạn có thể **fix washed out image** hoặc tăng chi tiết trong vùng bóng mà không làm quá sáng các vùng sáng.

## Tại sao nên sử dụng Aspose.PSD cho Gamma Correction?
Aspose.PSD hoạt động như một **java image processing library** mạnh mẽ, trừu tượng hoá các phức tạp của định dạng PSD. Nó xử lý các hồ sơ màu, bộ nhớ đệm, và cung cấp một lời gọi `adjustGamma` đơn giản, khiến nó trở thành lựa chọn lý tưởng cho **java gamma correction** và **convert PSD to TIFF**.

## Yêu cầu trước

1. **Java Development Environment** – Cài đặt Java 8 hoặc mới hơn.  
2. **Aspose.PSD Library** – Tải xuống và thêm JAR vào dự án của bạn. Xem [documentation](https://reference.aspose.com/psd/java/) chính thức.  
3. **Sample Image** – Tệp PSD bạn muốn xử lý (ví dụ, `sample.psd`).  

## Nhập các gói

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

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

**Pro tip:** Caching dữ liệu raster một lần sẽ giảm tải bộ nhớ khi bạn áp dụng nhiều điều chỉnh liên tiếp.

## Bước 2: Điều chỉnh Gamma

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

Bạn có thể truyền các giá trị khác nhau cho các kênh đỏ, xanh lá và xanh dương nếu cần điều chỉnh riêng cho từng kênh.

## Bước 3: Tạo TiffOptions

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Thiết lập mẫu 8‑bit (`{8,8,8}`) giữ cho kích thước tệp TIFF ở mức hợp lý đồng thời bảo toàn độ chính xác màu.

## Bước 4: Lưu hình ảnh kết quả

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Sau khi lưu, bạn có thể đưa tệp TIFF vào các hệ thống downstream như dịch vụ in ấn hoặc API web.

## Các trường hợp sử dụng phổ biến

- **Automated graphics pipelines** – Điều chỉnh gamma ngay lập tức trước khi tạo thumbnail.  
- **Batch conversion tools** – Chuyển đổi các kho lưu trữ PSD lớn sang TIFF trong khi chuẩn hoá độ sáng.  
- **Web services** – Cung cấp một endpoint nhận PSD, áp dụng gamma correction và trả về TIFF cho client.

## Các vấn đề thường gặp và giải pháp

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Hình ảnh xuất hiện bị nhạt** | Giá trị gamma quá cao (ví dụ, > 2.5) | Giảm hệ số gamma xuống giá trị từ 1.8 đến 2.2. |
| **`rasterImage.isCached()` returns false** | Hình ảnh chưa được tải vào bộ nhớ | Gọi `rasterImage.cacheData()` trước khi điều chỉnh gamma. |
| **Kích thước tệp TIFF quá lớn** | Bits per sample được đặt thành 16‑bit | Sử dụng mẫu 8‑bit (`{8,8,8}`) như trong ví dụ. |

## Câu hỏi thường gặp

**Q: Tôi có thể áp dụng các giá trị gamma khác nhau cho từng kênh màu không?**  
A: Có – phương thức `adjustGamma` chấp nhận các giá trị float riêng biệt cho các kênh đỏ, xanh lá và xanh dương.

**Q: Có thể xâu chuỗi nhiều điều chỉnh hình ảnh trước khi lưu không?**  
A: Chắc chắn. Bạn có thể thực hiện thay đổi kích thước, cắt, hoặc chỉnh màu tuần tự trên cùng một đối tượng `RasterImage`.

**Q: Aspose.PSD có hỗ trợ tệp PSD đa trang không?**  
A: Có, mỗi layer có thể được truy cập và xử lý riêng lẻ.

**Q: Tôi có thể xuất ra định dạng nào ngoài TIFF?**  
A: Aspose.PSD hỗ trợ PNG, JPEG, BMP và nhiều định dạng khác thông qua các lớp options tương ứng.

**Q: Làm sao tránh hình ảnh bị nhạt sau khi áp dụng gamma correction?**  
A: Bắt đầu với gamma trung bình (khoảng 2.0) và xem trước kết quả; giảm gamma nếu hình ảnh trông quá sáng.

## Kết luận

Chúc mừng! Bạn đã thành công học **how to adjust gamma** trong một quy trình **java image processing**, chuyển đổi PSD sang TIFF, và tránh các lỗi thường gặp như **washed‑out image**. Mẫu này cung cấp cho bạn khả năng kiểm soát chi tiết độ sáng và độ tương phản, làm cho nó trở nên lý tưởng cho các pipeline đồ họa tự động, dịch vụ web, hoặc tiện ích desktop.

---

**Cập nhật lần cuối:** 2026-02-27  
**Kiểm tra với:** Aspose.PSD 24.11 for Java  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}