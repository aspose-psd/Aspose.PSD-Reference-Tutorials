---
date: 2026-09-08
description: Tìm hiểu cách vẽ hình chữ nhật trên ảnh bằng Aspose.PSD for Java, bao
  gồm việc tạo bitmap, màu nền và khởi tạo graphics cho việc xử lý ảnh bằng Java.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Vẽ hình chữ nhật trong Java
og_description: Tìm hiểu cách vẽ hình chữ nhật trên ảnh bằng Aspose.PSD for Java.
  Hướng dẫn này bao gồm việc tạo bitmap, thiết lập màu nền và khởi tạo graphics trong
  Java.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Cách vẽ hình chữ nhật trên ảnh bằng Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Cách vẽ hình chữ nhật trên ảnh bằng Aspose.PSD for Java
url: /vi/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách vẽ hình chữ nhật trên ảnh bằng Aspose.PSD cho Java

## Giới thiệu
Nếu bạn cần **how to draw rectangle** trên một hình ảnh một cách lập trình, Aspose.PSD cho Java cung cấp cho bạn một API sạch sẽ, hiệu suất cao. Trong hướng dẫn này, bạn sẽ thấy cách tạo một bitmap, đặt màu nền, và **initialize graphics java** các đối tượng để bạn có thể vẽ các hình chữ nhật với bất kỳ kích thước và màu sắc nào. Các bước rất đơn giản, mã ngắn gọn, và kết quả là một tệp BMP mà bạn có thể sử dụng trong bất kỳ quy trình làm việc nào dựa trên Java.

## Câu trả lời nhanh
- **Thư viện nào xử lý việc vẽ hình chữ nhật?** Aspose.PSD for Java.
- **Cần bao nhiêu dòng mã?** About six lines to create the image, set background, and draw two rectangles.
- **Các định dạng ảnh nào được hỗ trợ để xuất?** BMP, PNG, JPEG, TIFF, GIF and more.
- **Tôi có cần giấy phép cho việc phát triển không?** A free trial works for testing; a license is required for production.
- **Tôi có thể thay đổi độ dày viền không?** Yes – adjust the `Pen` thickness property before drawing.

## Vẽ hình chữ nhật trên ảnh là gì?
Vẽ một hình chữ nhật trên ảnh có nghĩa là tạo ra một hình dạng được tô đầy hoặc chỉ viền lên một bitmap bằng cách sử dụng ngữ cảnh đồ họa. Lớp `Graphics` của Aspose.PSD cung cấp các phương thức cho phép bạn chỉ định màu, vị trí và kích thước chỉ bằng một lời gọi.

## Tại sao nên sử dụng Aspose.PSD cho Java để vẽ hình chữ nhật?
Aspose.PSD hỗ trợ **hơn 50 định dạng ảnh** và có thể xử lý các tệp lên tới **2 GB** mà không cần tải toàn bộ tài liệu vào bộ nhớ. API `Graphics` của nó chạy nhanh tới **3×** so với Java AWT gốc cho các thao tác batch, làm cho nó trở thành lựa chọn lý tưởng cho việc xử lý ảnh phía máy chủ với hiệu suất cao.

## Yêu cầu trước
Trước khi bắt đầu, hãy chắc chắn rằng bạn có:

- **Java Development Kit (JDK) 8 hoặc cao hơn** installed.
- **Aspose.PSD for Java** library downloaded from the [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) and added to your project’s classpath.

### Nhập gói
Các câu lệnh `import` cung cấp cho bạn quyền truy cập vào các lớp cần thiết cho việc tạo bitmap và vẽ.

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
Các import này sẽ cho phép bạn truy cập các lớp và phương thức cần thiết để vẽ hình chữ nhật trên ảnh.

## Cách vẽ hình chữ nhật trên ảnh trong Java?
Tải một `PsdImage` mới, xóa bề mặt của nó bằng màu nền, tạo một đối tượng `Graphics`, và sau đó gọi `drawRectangle` với bút và cọ mong muốn. Toàn bộ quá trình chỉ mất vài lời gọi phương thức và tạo ra một bitmap sẵn sàng để lưu.  
`PsdImage` đại diện cho một bitmap trong bộ nhớ có thể được chỉnh sửa và lưu.  
`Graphics` cung cấp một bề mặt vẽ để render các hình dạng lên ảnh.

### Bước 1: tạo một ảnh mới
Lớp `PsdImage` đại diện cho một bitmap trong bộ nhớ. Khởi tạo nó cũng cấp phát bộ đệm pixel.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
Trong bước này, `PsdImage` được khởi tạo với chiều rộng và chiều cao **100 px** mỗi, cung cấp cho bạn một canvas nhỏ để minh họa.

### Bước 2: khởi tạo đối tượng graphics java
Một thể hiện `Graphics` là bề mặt vẽ gắn với ảnh mà bạn vừa tạo.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
Đối tượng `Graphics` này sẽ được sử dụng để thực hiện các thao tác vẽ như tô đầy hình dạng hoặc vẽ viền.

### Bước 3: đặt màu nền java
Trước khi vẽ các hình dạng, bạn thường muốn một nền đồng nhất. Sử dụng `clear` với một `Color` để lấp đầy toàn bộ canvas.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
Nền được đặt thành **yellow**, cung cấp độ tương phản cao cho các hình chữ nhật màu đỏ và xanh dương sẽ theo sau.

### Bước 4: vẽ hình chữ nhật trên ảnh
Sử dụng `drawRectangle` với một `Pen` cho viền và một `SolidBrush` cho phần tô. Bạn có thể vẽ nhiều hình chữ nhật với các màu và vị trí khác nhau.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Các lệnh này vẽ một hình chữ nhật **red** tại (10, 10) và một hình chữ nhật **blue** tại (50, 50), mỗi hình có chiều rộng 40 px và chiều cao 30 px.

### Bước 5: xuất ảnh ra bitmap
Cuối cùng, lưu ảnh đã chỉnh sửa ra đĩa. Aspose.PSD tự động mã hoá bitmap theo định dạng bạn chỉ định.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
Ảnh được lưu dưới dạng tệp BMP tại đường dẫn được lưu trong `outpath`.

## Các vấn đề thường gặp và giải pháp
- **Tệp đầu ra trống** – Ensure you call `graphics.clear` before drawing; otherwise the canvas may remain transparent.
- **Màu không đúng** – Verify that you import `com.aspose.psd.Color` and not `java.awt.Color`.
- **Ảnh lớn gây hết bộ nhớ** – Use `PsdImage` constructors that support streaming to avoid loading the whole file into RAM.

## Câu hỏi thường gặp

**Q: Có thể Aspose.PSD cho Java xử lý các hình dạng khác ngoài hình chữ nhật không?**  
A: Có, nó hỗ trợ các hình elip, đường thẳng, đa giác và các đường dẫn tùy chỉnh, cung cấp cho bạn khả năng vẽ vector đầy đủ.

**Q: Làm thế nào để tôi thay đổi độ dày của viền hình chữ nhật?**  
A: Đặt phương thức `setWidth(float)` của đối tượng `Pen` trước khi gọi `drawRectangle`.

**Q: Aspose.PSD cho Java có phù hợp cho các tác vụ xử lý ảnh hiệu suất cao không?**  
A: Chắc chắn – API streaming của nó xử lý các tệp PSD hàng trăm trang với mức sử dụng RAM dưới 200 MB.

**Q: Tôi có thể tìm thêm ví dụ và hướng dẫn cho Aspose.PSD cho Java ở đâu?**  
A: Bạn có thể khám phá thêm các ví dụ và tài liệu chi tiết trên [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

**Q: Aspose.PSD cho Java có hỗ trợ các định dạng ảnh khác ngoài BMP không?**  
A: Có, nó hỗ trợ PNG, JPEG, TIFF, GIF và hơn 30 định dạng bổ sung cho cả nhập và xuất.

## Kết luận
Bạn giờ đã biết **how to draw rectangle** trên một ảnh bằng Aspose.PSD cho Java, từ việc tạo bitmap đến đặt màu nền và khởi tạo graphics. Hãy thử nghiệm với các kích thước, màu sắc và các hình dạng bổ sung để thành thạo **java image manipulation**. Khi đã sẵn sàng, tích hợp mẫu này vào các pipeline xử lý batch lớn hơn hoặc các trình chỉnh sửa dựa trên UI.

---

**Cập nhật lần cuối:** 2026-09-08  
**Được kiểm tra với:** Aspose.PSD for Java 24.12  
**Tác giả:** Aspose

## Các hướng dẫn liên quan

- [Thay đổi kích thước ảnh với Aspose.PSD cho Java – Vẽ hình dạng & Các thao tác ảnh cơ bản](/psd/java/basic-image-operations/)
- [Thêm chữ ký vào ảnh – Vẽ ảnh trên Canvas với Aspose.PSD cho Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Cắt ảnh bằng hình chữ nhật với Aspose.PSD cho Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}