---
date: 2026-08-01
description: Tìm hiểu cách điều chỉnh gamma trong xử lý ảnh Java với Aspose.PSD, chuyển
  đổi PSD sang TIFF và khắc phục ảnh bị nhạt trong một hướng dẫn ngắn gọn.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Điều chỉnh gamma của ảnh
og_description: Tìm hiểu cách điều chỉnh gamma trong xử lý ảnh Java bằng Aspose.PSD
  – một thư viện nhanh, server‑side giúp sửa ảnh bị nhạt và chuyển đổi PSD sang TIFF
  chỉ trong vài dòng mã.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: cách điều chỉnh gamma – xử lý Java với Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Cách điều chỉnh gamma trong xử lý ảnh Java với Aspose.PSD
url: /vi/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Điều Chỉnh Gamma trong Xử Lý Ảnh Java với Aspose.PSD

## Giới thiệu

Nếu bạn đang làm việc với **java image processing**, việc học **cách điều chỉnh gamma** là một kỹ thuật cơ bản để cải thiện độ sáng và độ tương phản mà không mất chi tiết. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn cách sử dụng **Aspose.PSD for Java** để áp dụng gamma correction lên một tệp PSD, **convert PSD to TIFF**, và tránh **ảnh bị phai màu**. Bạn sẽ thấy tại sao cách tiếp cận này nhanh, đáng tin cậy, và hoàn hảo cho các pipeline **server‑side image processing**.

## Câu trả lời nhanh
- **Gamma correction làm gì?** Nó tái ánh xạ các giá trị độ sáng để làm cho các khu vực tối sáng hơn hoặc các khu vực sáng tối hơn trong khi vẫn giữ nguyên chi tiết tổng thể.  
- **Thư viện nào xử lý việc này?** Aspose.PSD for Java cung cấp một phương thức `adjustGamma` dành riêng cho hình ảnh raster.  
- **Tôi có thể chuyển đổi PSD sang TIFF trong cùng một quy trình không?** Có – sau khi điều chỉnh gamma, bạn có thể lưu ảnh trực tiếp sang TIFF bằng cách sử dụng `TiffOptions`.  
- **Tôi có cần giấy phép để phát triển không?** Bản dùng thử miễn phí hoạt động cho việc thử nghiệm; giấy phép thương mại là bắt buộc cho việc sử dụng trong môi trường sản xuất.  
- **Phiên bản Java nào được hỗ trợ?** Aspose.PSD hỗ trợ Java 8 trở lên.

## Gamma Correction trong Java là gì?

Gamma correction thay đổi mối quan hệ phi tuyến giữa các giá trị pixel đã được mã hoá và độ sáng hiển thị. Bằng cách điều chỉnh đường cong gamma, bạn có thể **khắc phục vấn đề ảnh bị phai màu** hoặc tăng cường chi tiết trong vùng bóng tối mà không làm quá sáng các vùng sáng. Nó hoạt động bằng cách áp dụng hàm luỹ thừa lên mỗi pixel, làm sáng các tông tối và nén các vùng sáng, tạo ra một hình ảnh tự nhiên hơn.

## Tại sao nên sử dụng Aspose.PSD cho Gamma Correction?

Aspose.PSD là một **java image processing library** giúp trừu tượng hoá các phức tạp của định dạng PSD. Nó hỗ trợ xử lý các tệp lên tới 2 GB, xử lý hơn 50 định dạng ảnh khác nhau, và cung cấp một lời gọi `adjustGamma` đơn giản, làm cho nó trở thành lựa chọn lý tưởng cho **java gamma correction** và **convert PSD to TIFF** trong quy trình làm việc.

## Yêu cầu trước

1. **Môi trường phát triển Java** – Đã cài đặt Java 8 hoặc phiên bản mới hơn.  
2. **Thư viện Aspose.PSD** – Tải xuống và thêm JAR vào dự án của bạn. Xem [documentation](https://reference.aspose.com/psd/java/) chính thức.  
3. **Hình ảnh mẫu** – Một tệp PSD bạn muốn xử lý (ví dụ, `sample.psd`).  

## Nhập các gói

Trước khi bắt đầu, hãy nhập các namespace cần thiết để bạn có thể truy cập vào việc xử lý raster và các tùy chọn định dạng tệp.

## Bước 1: Tải ảnh

Lớp `RasterImage` đại diện cho dữ liệu pixel raster hoá của một lớp PSD trong bộ nhớ. Việc tải ảnh một lần và lưu vào bộ nhớ đệm giảm thiểu việc tiêu tốn bộ nhớ cho các điều chỉnh tiếp theo.

## Bước 2: Điều chỉnh Gamma

Tải PSD của bạn bằng `new RasterImage("sample.psd")` và gọi `rasterImage.adjustGamma(2.0f)` — dòng lệnh duy nhất này áp dụng gamma 2.0 cho tất cả các kênh màu, làm sáng các vùng bóng tối trong khi giữ nguyên các vùng sáng. Bạn có thể truyền các giá trị riêng cho đỏ, xanh lá và xanh dương nếu cần điều chỉnh riêng cho từng kênh.

## Bước 3: Tạo TiffOptions

`TiffOptions` cho phép bạn kiểm soát nén, số bit mỗi mẫu, và các cài đặt đặc thù của TIFF. Đặt mẫu 8‑bit (`{8,8,8}`) giữ kích thước tệp TIFF ở mức hợp lý trong khi vẫn bảo toàn độ trung thực màu.

## Bước 4: Lưu ảnh đã xử lý

Gọi `rasterImage.save("output.tif", tiffOptions)` để ghi ảnh đã xử lý ra đĩa. Sau khi lưu, bạn có thể đưa tệp TIFF vào các hệ thống downstream như dịch vụ in ấn hoặc API web.

## Các trường hợp sử dụng phổ biến

- **Các pipeline đồ họa tự động** – Điều chỉnh gamma ngay lập tức trước khi tạo thumbnail.  
- **Công cụ chuyển đổi hàng loạt** – Chuyển đổi các kho lưu trữ PSD lớn sang TIFF trong khi chuẩn hoá độ sáng.  
- **Dịch vụ web** – Cung cấp một endpoint nhận PSD, áp dụng gamma correction, và trả về TIFF cho khách hàng sử dụng.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| **Ảnh bị phai màu** | Giá trị gamma quá cao (ví dụ, > 2.5) | Giảm hệ số gamma xuống một giá trị giữa 1.8 và 2.2. |
| **`rasterImage.isCached()` returns false** | Ảnh chưa được tải vào bộ nhớ | Gọi `rasterImage.cacheData()` trước khi điều chỉnh gamma. |
| **Kích thước tệp TIFF lớn** | Bits mỗi mẫu được đặt thành 16‑bit | Sử dụng mẫu 8‑bit (`{8,8,8}`) như trong ví dụ. |

## Câu hỏi thường gặp

**Q: Có thể áp dụng các giá trị gamma khác nhau cho từng kênh màu không?**  
A: Có – phương thức `adjustGamma` chấp nhận các giá trị float riêng cho các kênh đỏ, xanh lá và xanh dương.

**Q: Có thể xâu chuỗi nhiều điều chỉnh ảnh trước khi lưu không?**  
A: Chắc chắn. Bạn có thể thực hiện thay đổi kích thước, cắt, hoặc chỉnh màu một cách tuần tự trên cùng một đối tượng `RasterImage`.

**Q: Aspose.PSD có hỗ trợ tệp PSD đa trang không?**  
A: Có, mỗi lớp có thể được truy cập và xử lý riêng biệt.

**Q: Tôi có thể xuất ra định dạng nào ngoài TIFF?**  
A: Aspose.PSD hỗ trợ PNG, JPEG, BMP và nhiều định dạng khác thông qua các lớp tùy chọn tương ứng.

**Q: Làm sao để tránh ảnh bị phai màu sau khi điều chỉnh gamma?**  
A: Bắt đầu với gamma ở mức trung bình (khoảng 2.0) và xem trước kết quả; giảm gamma nếu ảnh quá sáng.

## Kết luận

Chúc mừng! Bạn đã thành công học **cách điều chỉnh gamma** trong quy trình **java image processing**, chuyển đổi PSD sang TIFF, và tránh được các lỗi thường gặp như **ảnh bị phai màu**. Mẫu này cung cấp cho bạn khả năng kiểm soát chi tiết độ sáng và độ tương phản, làm cho nó trở thành lựa chọn lý tưởng cho các pipeline đồ họa tự động, dịch vụ web, hoặc tiện ích desktop.

---

**Cập nhật lần cuối:** 2026-08-01  
**Kiểm tra với:** Aspose.PSD 24.11 for Java  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan

- [Hướng dẫn Xử lý Ảnh Java - Điều chỉnh Độ sáng của Ảnh với Aspose.PSD cho Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Cách Chuyển đổi PSD sang TIFF và Điều chỉnh Độ tương phản với Aspose.PSD cho Java](/psd/java/advanced-techniques/adjust-contrast/)
- [Chuyển đổi PSD sang Ảnh trong Java – Áp dụng Các lớp Điều chỉnh với Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

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

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```