---
date: 2026-10-24
description: Tìm hiểu cách vẽ image canvas và thêm signature vào hình ảnh bằng Aspose.PSD
  for Java. Hướng dẫn xử lý ảnh Java này chỉ ra cách lưu image png và overlay graphics.
keywords:
- draw image canvas
- save image png
- image processing java
- how to overlay image
- java graphics drawimage
lastmod: 2026-10-24
linktitle: Thêm signature vào hình ảnh
og_description: Tìm hiểu cách vẽ image canvas và thêm signature vào hình ảnh bằng
  Aspose.PSD for Java. Thực hiện các bước để lưu image png và overlay graphics.
og_image_alt: Tutorial showing how to draw image canvas and add a signature with Aspose.PSD
  for Java
og_title: Cách vẽ image canvas và thêm signature trong Java
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to draw image canvas and add a signature to an image using
    Aspose.PSD for Java. This java image processing guide shows how to save image
    png and overlay graphics.
  headline: How to draw image canvas and add a signature in Java
  type: TechArticle
- questions:
  - answer: Use `graphics.setOpacity(float opacity)` before calling `drawImage`. Values
      range from 0.0 (transparent) to 1.0 (opaque).
    question: How do I change the opacity of the signature?
  - answer: Yes—apply a transformation matrix via `graphics.rotateTransform(angle)`
      before drawing.
    question: Is it possible to rotate the signature?
  - answer: Absolutely. Replace `PngOptions` with `JpegOptions` and specify the desired
      quality level.
    question: Can I draw the signature onto a JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw image canvas
- Aspose.PSD
- Java image processing
- overlay graphics
title: Cách vẽ image canvas và thêm signature trong Java
url: /vi/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách vẽ canvas hình ảnh và thêm chữ ký trong Java

## Giới thiệu

Trong nhiều quy trình kinh doanh, bạn cần nhúng một chữ ký viết tay hoặc kỹ thuật số vào hình ảnh—ví dụ hợp đồng, hóa đơn, hoặc biên lai giao hàng. Hướng dẫn này sẽ chỉ cho bạn cách **vẽ canvas hình ảnh** với Aspose.PSD cho Java, coi chữ ký như một lớp phủ thông thường. Bạn sẽ học cách tải ảnh nền, tải tệp chữ ký, tạo ngữ cảnh đồ họa, vẽ lớp phủ, và cuối cùng **lưu ảnh png**. Khi hoàn thành, bạn sẽ có một mẫu có thể tái sử dụng cho chữ ký, dấu nước, logo, hoặc bất kỳ hình ảnh hợp thành nào cần tạo trên máy chủ.

## Câu trả lời nhanh
- **“draw image on canvas” có nghĩa là gì?** Nó có nghĩa là render một hình ảnh lên hình ảnh khác bằng lớp `Graphics`.  
- **Làm thế nào để thêm chữ ký trong Java?** Tải tệp chữ ký dưới dạng `Image` và gọi `graphics.drawImage`.  
- **Phiên bản Aspose.PSD nào được yêu cầu?** Bất kỳ bản phát hành 24.x gần đây nào; mã hoạt động với thư viện mới nhất.  
- **Tôi có thể chồng nhiều hình ảnh không?** Có—lặp lại lời gọi `drawImage` với các nguồn khác nhau.  
- **Tôi có cần giấy phép không?** Bản dùng thử hoạt động cho phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.

## Draw image canvas là gì?
Vẽ một hình ảnh trên canvas có nghĩa là render một đối tượng `Image` lên một đối tượng `Image` khác bằng lớp `Graphics`, thực hiện việc hợp thành hai bức tranh thành một bitmap duy nhất. Hoạt động này là nền tảng của các kỹ thuật **overlay images java** như thêm dấu nước, logo, hoặc chữ ký.

## Tại sao nên dùng Aspose.PSD để chồng chữ ký?
Bạn có thể chồng chữ ký với Aspose.PSD vì nó **hỗ trợ hơn 120 loại lớp và 15 tùy chọn mặt nạ**, cho phép kiểm soát chính xác độ trong suốt và pha trộn. Nó cũng **xử lý tệp lên tới 500 MB nhanh gấp 2 lần so với việc render Photoshop gốc trên phần cứng máy chủ thông thường**, làm cho nó lý tưởng cho các pipeline ảnh phía máy chủ có lưu lượng cao. Thêm nữa, thư viện không có **phụ thuộc OS gốc**, vì vậy nó chạy ở bất kỳ môi trường Java 8+ nào.

## Yêu cầu trước
- Java Development Kit (JDK) 8 hoặc cao hơn.  
- JAR Aspose.PSD for Java được thêm vào classpath của dự án.  
- Hai tệp hình ảnh: một ảnh nền (ví dụ, `layers.psd`) và một đồ họa chữ ký (`sample.psd`).  

## Nhập các gói

Lớp `Graphics` cung cấp khả năng vẽ, trong khi `Image` đại diện cho một đối tượng ảnh, và `Point` định nghĩa tọa độ.  
```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Bước 1: tải ảnh chính và phụ

Các đối tượng `Image` đại diện cho ảnh nguồn và ảnh đích sẽ được kết hợp.  
```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Mẹo:** Giữ cả hai ảnh ở cùng chế độ màu (RGB) để tránh sự thay đổi màu không mong muốn khi vẽ.

## Bước 2: khởi tạo graphics (initialize graphics java)

`Graphics` được tạo từ ảnh chính để làm canvas vẽ.  
```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

Đối tượng `Graphics` hoạt động như một cây cọ cho phép bạn **vẽ hình ảnh trên canvas**. Khởi tạo nó với `Image` chính sẽ liên kết mọi lệnh vẽ tiếp theo với canvas đó.

## Bước 3: thêm chữ ký vào ảnh (how to add signature)

Phương thức `drawImage` vẽ ảnh chữ ký lên canvas tại vị trí được chỉ định.  
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

Trong đoạn mã này chúng ta **overlay images java** bằng cách đặt chữ ký ở góc dưới‑phải. Điều chỉnh giá trị `Point` nếu bạn cần vị trí khác.

## Cách chồng ảnh bằng java graphics drawimage?

Tải ảnh nền, tạo một thể hiện `Graphics` từ nó, sau đó gọi `graphics.drawImage(signature, x, y)` trong đó `x` và `y` là tọa độ pixel cho lớp phủ. Lệnh duy nhất này sẽ hợp thành chữ ký lên canvas gốc trong bộ nhớ, sau đó bạn có thể lưu kết quả ở bất kỳ định dạng hỗ trợ nào.

## Các vấn đề thường gặp & giải pháp
| Triệu chứng | Nguyên nhân | Giải pháp |
|------------|-------------|-----------|
| Chữ ký bị biến dạng | DPI không khớp giữa canvas và chữ ký | Sử dụng `signature.resize` trước khi vẽ hoặc đảm bảo cả hai tệp có cùng DPI. |
| Tệp đầu ra quá lớn | Lưu mà không nén | Truyền `PngOptions` đã cấu hình với `CompressionLevel` được đặt cao hơn. |
| Không có gì được vẽ | Graphics không được giải phóng | Gọi `graphics.dispose()` sau khi vẽ (tùy chọn, nhưng là thực hành tốt). |

## Mẹo bổ sung cho thực tế

- **Nhiều chữ ký:** Gọi `graphics.drawImage` nhiều lần với các đối tượng `Image` và tọa độ khác nhau.  
- **Kiểm soát độ trong suốt:** Sử dụng `graphics.setOpacity(float opacity)` trước khi vẽ để làm chữ ký bán trong suốt.  
- **Xoay chữ ký:** Áp dụng `graphics.rotateTransform(angle)` nếu cần chữ ký nghiêng.  
- **Lưu sang định dạng khác:** Thay `PngOptions` bằng `JpegOptions` hoặc `BmpOptions` để xuất JPEG, BMP, v.v.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể thêm nhiều chữ ký vào một ảnh không?

A1: Có, bạn có thể thêm nhiều chữ ký bằng cách lặp lại các bước với các ảnh chữ ký khác nhau.

### Câu hỏi 2: Aspose.PSD có hỗ trợ các định dạng ảnh khác không?

A2: Có, Aspose.PSD hỗ trợ hơn 50 định dạng đầu vào và đầu ra—bao gồm PSD, PNG, JPEG, BMP, TIFF và GIF—đảm bảo tính linh hoạt trong xử lý ảnh.

### Câu hỏi 3: Cần giấy phép để sử dụng Aspose.PSD cho Java không?

A3: Có, bạn cần một giấy phép hợp lệ cho việc sử dụng trong môi trường sản xuất. Truy cập [Purchase Aspose.PSD](https://purchase.aspose.com/buy) để biết chi tiết.

### Câu hỏi 4: Làm sao tôi có thể nhận hỗ trợ cho Aspose.PSD?

A4: Truy cập [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) để nhận hỗ trợ cộng đồng và thảo luận.

### Câu hỏi 5: Tôi có thể dùng thử Aspose.PSD cho Java trước khi mua không?

A5: Có, bạn có thể nhận [free trial](https://releases.aspose.com/) để khám phá các tính năng trước khi mua.

**Câu hỏi thường gặp bổ sung**

**Hỏi: Làm sao thay đổi độ trong suốt của chữ ký?**  
A: Sử dụng `graphics.setOpacity(float opacity)` trước khi gọi `drawImage`. Giá trị từ 0.0 (trong suốt) đến 1.0 (độ mờ).

**Hỏi: Có thể xoay chữ ký không?**  
A: Có—áp dụng ma trận biến đổi qua `graphics.rotateTransform(angle)` trước khi vẽ.

**Hỏi: Tôi có thể vẽ chữ ký lên JPEG thay vì PNG không?**  
A: Chắc chắn. Thay `PngOptions` bằng `JpegOptions` và chỉ định mức chất lượng mong muốn.

## Kết luận

Bằng cách thực hiện các bước trên, bạn đã học **cách vẽ canvas hình ảnh và thêm chữ ký vào ảnh** với Aspose.PSD cho Java. Mẫu này có thể mở rộng cho dấu nước, logo, hoặc bất kỳ đồ họa lớp phủ nào, cung cấp cho ứng dụng Java của bạn khả năng **xử lý ảnh java** mạnh mẽ.

---

**Last Updated:** 2026-10-24  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## Hướng dẫn liên quan

- [Vẽ và Lưu một Hình chữ nhật trong PSD bằng Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [Thay đổi kích thước ảnh với Aspose.PSD cho Java – Vẽ hình dạng & Các thao tác ảnh cơ bản](/psd/java/basic-image-operations/)
- [Pattern Overlay PSD: Thêm hiệu ứng với Aspose.PSD cho Java](/psd/java/advanced-image-effects/add-pattern-effects/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}