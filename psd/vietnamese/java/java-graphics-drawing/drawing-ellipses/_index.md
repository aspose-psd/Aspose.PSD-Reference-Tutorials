---
date: 2026-01-19
description: Học cách vẽ hình elip trong Java bằng Aspose.PSD để thiết kế đồ họa chính
  xác và xử lý ảnh. Thành thạo các hướng dẫn từng bước.
linktitle: Drawing Ellipses in Java
second_title: Aspose.PSD Java API
title: Cách vẽ hình elip trong Java với Aspose.PSD
url: /vi/java/java-graphics-drawing/drawing-ellipses/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Vẽ Ellipse trong Java

## Introduction
Trong hướng dẫn này, bạn sẽ học **cách vẽ ellipse** bằng Aspose.PSD cho Java. Aspose.PSD là một thư viện mạnh mẽ cho phép các nhà với các tệp PSD và thao tác hình ảnh một cách dễ dàng. Vẽ các hình dạng như ellipse là một nhiệm vụ cơ bản trong xử lý ảnh và thiết kế đồ họa. Bằng cách làm theo hướng dẫn này, bạn sẽ có kinh nghiệm thực tế tạo ellipse bằng lậpSD.

## Quick Answers
- **What library is best for drawing the example?  
- **Can I change the ellipse style?** Yes – use different `Pen` settings or brushes.  
- **Which image formats are supported for saving?** BMP, PNG, JPEG, PSD, and more.

## What is “how to draw ellipse” in Java?
Vẽ một ellipse có nghĩa là render một hình oval mượt trên bitmap hoặc canvas PSD. Trong Java, việc này được thực hiện bằng cách tạo một ngữ cảnh đồ họa, cấu hình một `Pen` (hoặc brush), và gọi phương thức `draw vẽ sắc, và chuyển đổi định dạng tệp. Nó hoạt động nhất quán trên mà không cần thư viện bổ sung.

## Prerequisites
- Kiến thức cơ bản về lập trình Java.  
- JDK (Java Development Kit) đã được cài đặt trên hệ thống của bạn.  
- Môi trường phát triển tích IntelliJ IDEA hoặc Eclipse.  
- Thư viện Aspose.PSD cho Java. Bạn có thể tải xuống từ [here](https://releases.aspose.com/psd/java/).

## Import Packages
First, you need to import the necessary packages from Aspose.PSD:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Step 1: Set up your Java project
Trước khi bắt đầu viết mã, hãy chắc chắn dự án Java của bạn đã được cấu hình đúng với Aspose.PSD được bao gồm như một phụ thuộc.

## Step 2: Create an instance of PsdImage
Khởi tạo một thể hiện mới của `PsdImage` với độ rộng và chiều cao mong muốn.

```java
Image image = new PsdImage(100, 100);
```

## Step 3: Initialize Graphics object
Tạo và khởi tạo một thể hiện của `Graphics` để làm việc với hình ảnh.

```java
Graphics graphics = new Graphics(image);
```

## Step 4: Clear the Graphics surface
Trước khi vẽ, xóa bề mặt đồ họa bằng một màu cụ thể (tùy chọn).

```java
graphics.clear(Color.getYellow());
```

## Step 5: Draw a dotted ellipse
Sử dụng một đối tượng `Pen` màu đỏ và vẽ một ellipse dạng chấm trong một `Rectangle` được chỉ định.

```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```

## Step 6: Draw a continuous ellipse
Tạo một đối tượng `Pen` với brush xanh đậm đặc và vẽ một ellipse liên tục trong một `Rectangle` khác.

```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```

## Step 7: Save the image
Cuối cùng, lưu hình ảnh đã tạo ở định dạng BMP tới đường dẫn đã chỉ định.

```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

## Common Issues and Solutions
- **Image appears blank:** Ensure you called `graphics.clear` before drawing or set a background color.  
  -> Hình ảnh xuất hiện trống: Đảm bảo bạn đã gọi ` vẽ hoặc đặt màu nền.  
- **Ellipse size looks wrong:** Verify the `Rectangle` parameters (x, y, width, height) match your intended dimensions.  
  -> Kích thước ellipse không đúng: Kiểm tra các tham số của `Rectangle` (x, y, width, height) có khớp với kích thước mong muốn không.  
- **License exception:** If you see a licensing error, apply -> Lỗi giấy gặp lỗi giấy phép thử miễn phí, cho phép bạn đánh giá các tính năng trước khi mua.

### Where can I find more examples and documentation?
Truy cập [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) để xem các hướng dẫn và ví dụ chi tiết.

### How can I get temporary licenses for Aspose.PSD?
Giấy phép tạm thời có thể được lấy từ [Aspose.PSD Temporary License](https://purchase.aspose.com/temporary-license/).

### What formats can Aspose.PSD save images to?
Aspose.PSD hỗ trợ lưu ảnh sang nhiều định dạng bao gồm BMP, PNG, JPEG và PSD.

### Is Aspose.PSD suitable for enterprise use?
Có, Aspose.PSD được thiết kế cho các nhiệm vụ xử lý ảnh chuyên nghiệp và cấp doanh nghiệp.

## Conclusion
Chúc mừng! Bạn đã học thành công **cách vẽ ellipse** bằng lập trình sử dụng Aspose.PSD cho Java. Hướng dẫn này đã bao gồm việc thiết lập dự án, khởi tạo đồ họa, vẽ ellipse dạng chấm và liên tục, và lưu hình ảnh kết quả. Bây giờ bạn có thể tích hợp các kỹ thuật này vào các ứng dụng Java của mình cho nhiều kịch bản thiết kế đồ họa và xử lý ảnh.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-19  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose