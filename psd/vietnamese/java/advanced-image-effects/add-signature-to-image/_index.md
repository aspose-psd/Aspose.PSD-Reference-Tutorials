---
date: 2025-12-02
description: Tìm hiểu cách vẽ hình ảnh trên canvas và chồng chữ ký trong Java bằng
  Aspose.PSD. Thực hiện theo hướng dẫn xử lý ảnh Java từng bước này và lưu kết quả
  dưới dạng PNG.
language: vi
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: Vẽ Hình ảnh trên Canvas – Thêm Chữ ký với Aspose.PSD cho Java
url: /java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vẽ Hình Ảnh trên Canvas – Thêm Chữ Ký với Aspose.PSD cho Java

## Giới thiệu

Thêm một chữ ký viết tay hoặc kỹ thuật số vào hình ảnh là một yêu cầu thường gặp cho hợp đồng, hoá đơn, hoặc bất kỳ tài liệu nào cần chứng minh tính xác thực. Với **Aspose.PSD for Java** bạn có thể **draw image on canvas** và xem chữ ký như một lớp phủ khác. Trong **java image processing tutorial** này chúng ta sẽ đi qua toàn bộ quy trình — từ tải ảnh gốc và file chữ ký, khởi tạo đồ họa, vẽ lớp phủ, và cuối cùng **save image png java**‑style.

## Câu trả lời nhanh
- **“draw image on canvas” có nghĩa là gì?** Nó đề cập đến việc render một hình ảnh lên một hình ảnh khác bằng lớp `Graphics`.  
- **Làm sao để thêm chữ ký trong Java?** Tải file chữ ký dưới dạng `Image` và sử dụng `Graphics.drawImage`.  
- **Phiên bản Aspose.PSD nào được yêu cầu?** Bất kỳ bản phát hành 24.x gần đây nào; mã hoạt động với thư viện mới nhất.  
- **Tôi có thể chồng nhiều hình ảnh không?** Có — lặp lại lời gọi `drawImage` với các nguồn khác nhau.  
- **Có cần giấy phép không?** Bản dùng thử hoạt động cho phát triển; cần giấy phép thương mại cho môi trường sản xuất.

## Draw Image on Canvas là gì?
Trong thuật ngữ của Aspose.PSD, vẽ một hình ảnh trên canvas có nghĩa là tô một đối tượng `Image` lên một đối tượng `Image` khác bằng ngữ cảnh `Graphics`. Hoạt động này là nền tảng của các kỹ thuật **overlay images java** như thêm watermark, logo, hoặc chữ ký.

## Tại sao nên sử dụng Aspose.PSD để chồng chữ ký?
- **Hỗ trợ PSD đầy đủ** – làm việc với các lớp, mặt nạ và độ trong suốt.  
- **Không phụ thuộc vào hệ điều hành** – thuần Java, lý tưởng cho xử lý phía máy chủ.  
- **Hiệu năng render cao** – tối ưu cho tệp lớn và bố cục phức tạp.  

## Yêu cầu trước
- Java Development Kit (JDK) 8 hoặc cao hơn.  
- Aspose.PSD for Java JAR đã được thêm vào classpath của dự án.  
- Hai tệp hình ảnh: một ảnh nền (ví dụ, `layers.psd`) và một đồ họa chữ ký (`sample.psd`).  

## Nhập các gói

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Bước 1: Tải hình ảnh chính và phụ

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Mẹo:** Giữ cả hai hình ảnh ở cùng chế độ màu (RGB) để tránh sự thay đổi màu không mong muốn khi vẽ.

## Bước 2: Khởi tạo Graphics (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

Đối tượng `Graphics` hoạt động như một cây cọ cho phép bạn **draw image on canvas**. Khởi tạo nó với `Image` chính sẽ liên kết tất cả các lệnh vẽ tiếp theo với canvas đó.

## Bước 3: Thêm chữ ký vào hình ảnh (how to add signature)

```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

Trong đoạn mã này chúng ta **overlay images java** bằng cách đặt chữ ký ở góc dưới‑phải. Điều chỉnh các giá trị `Point` nếu bạn cần vị trí khác.

## Vấn đề thường gặp & Giải pháp
| Symptom | Cause | Fix |
|---------|-------|-----|
| Chữ ký bị biến dạng | DPI không khớp giữa canvas và chữ ký | Sử dụng `signature.resize` trước khi vẽ hoặc đảm bảo cả hai tệp có cùng DPI. |
| File đầu ra quá lớn | Lưu mà không nén | Truyền một `PngOptions` được cấu hình với `CompressionLevel` đặt ở mức cao hơn. |
| Không có gì được vẽ | Graphics chưa được giải phóng | Gọi `graphics.dispose()` sau khi vẽ (tùy chọn, nhưng là thực hành tốt). |

## Kết luận

Bằng cách thực hiện các bước trên, bạn đã học được **cách draw image on canvas** và **thêm chữ ký** một cách liền mạch bằng Aspose.PSD cho Java. Kỹ thuật này có thể mở rộng để thêm watermark, logo, hoặc bất kỳ đồ họa phủ nào khác, mang lại cho ứng dụng Java của bạn khả năng **java image processing** mạnh mẽ.

## Câu hỏi thường gặp

### Q1: Tôi có thể thêm nhiều chữ ký vào một hình ảnh không?

A1: Có, bạn có thể thêm nhiều chữ ký bằng cách lặp lại các bước với các hình ảnh chữ ký khác nhau.

### Q2: Aspose.PSD có hỗ trợ các định dạng hình ảnh khác không?

A2: Có, Aspose.PSD hỗ trợ một loạt các định dạng hình ảnh, đảm bảo tính linh hoạt trong xử lý ảnh.

### Q3: Có cần giấy phép để sử dụng Aspose.PSD cho Java không?

A3: Có, bạn cần một giấy phép hợp lệ để sử dụng Aspose.PSD. Tham khảo [Purchase Aspose.PSD](https://purchase.aspose.com/buy) để biết chi tiết.

### Q4: Làm sao tôi có thể nhận hỗ trợ cho Aspose.PSD?

A4: Truy cập [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) để nhận hỗ trợ cộng đồng và thảo luận.

### Q5: Tôi có thể dùng thử Aspose.PSD cho Java trước khi mua không?

A5: Có, bạn có thể nhận một [free trial](https://releases.aspose.com/) để khám phá các tính năng trước khi quyết định mua.

## Các câu hỏi thường gặp bổ sung

**Q: Làm sao tôi thay đổi độ trong suốt của chữ ký?**  
A: Sử dụng `graphics.setOpacity(float opacity)` trước khi gọi `drawImage`. Giá trị nằm trong khoảng 0.0 (transparent) đến 1.0 (opaque).

**Q: Có thể xoay chữ ký không?**  
A: Có — áp dụng ma trận biến đổi bằng `graphics.rotateTransform(angle)` trước khi vẽ.

**Q: Tôi có thể vẽ chữ ký lên JPEG thay vì PNG không?**  
A: Hoàn toàn có thể. Thay `PngOptions` bằng `JpegOptions` và chỉ định mức chất lượng mong muốn.

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}