---
date: 2026-09-03
description: Tìm hiểu cách java graphics vẽ cung bằng Aspose.PSD for Java. Hướng dẫn
  từng bước kèm đoạn mã để tạo cung trong tệp PSD.
keywords:
- java graphics draw arc
- how to draw arcs java
- Aspose.PSD arc drawing
lastmod: 2026-09-03
linktitle: Vẽ cung trong Java
og_description: Tìm hiểu cách java graphics vẽ cung với Aspose.PSD for Java. Bài hướng
  dẫn này trình bày các yêu cầu trước, các bước mã, và mẹo để tạo cung trong tệp PSD.
og_image_alt: Screenshot of a Java program drawing an arc using Aspose.PSD
og_title: Cách java graphics vẽ cung trong Java – Hướng dẫn Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  headline: How to java graphics draw arc in Java
  type: TechArticle
- description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  name: How to java graphics draw arc in Java
  steps:
  - name: set up your Java project
    text: Create a new Java project in your favourite IDE and add the Aspose.PSD JAR
      to the build path. Ensure the JAR is referenced correctly so the compiler can
      locate the library classes.
  - name: import required packages
    text: 'To begin, import the necessary packages from Aspose.PSD for Java: The `Pen`
      class defines the colour, width, and style of the line used to draw the arc.
      These imports expose the `PsdImage`, `Graphics`, `Pen`, and colour classes needed
      for arc drawing.'
  - name: initialise image and graphics objects
    text: 'Create an instance of `PsdImage` and obtain a `Graphics` object to draw
      on: Replace `"Your Document Directory"` with the folder where you want the output
      files saved.'
  - name: define arc parameters
    text: 'Set the geometry and style of the arc—its bounding rectangle, start angle,
      sweep angle, colour, and thickness: Adjust the values to match the visual design
      you need; for example, a 200 px radius arc starting at 45° and sweeping 270°.'
  - name: draw the arc and save the image
    text: 'Invoke `drawArc` on the `Graphics` object and persist the PSD (or export
      to another format): The `drawArc` method of the `Graphics` class renders an
      arc defined by a bounding rectangle, start angle, and sweep angle using the
      specified `Pen`. The snippet draws the arc on the canvas and saves it as a '
  type: HowTo
- questions:
  - answer: Yes, the library can draw rectangles, ellipses, lines, polygons, and custom
      paths using the same `Graphics` API.
    question: Can Aspose.PSD for Java handle other shapes besides arcs?
  - answer: Create a `Pen` with the desired `Color` and width, then pass that `Pen`
      instance to `drawArc`.
    question: How do I change the arc colour and thickness?
  - answer: Absolutely. Aspose.PSD supports PNG, JPEG, TIFF, GIF and many more – just
      change the file extension in the `save` method.
    question: Is it possible to export the PSD to a format other than BMP?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for tutorials,
      code samples, and assistance from other developers.
    question: Where can I find more examples and community support?
  - answer: Yes, it can process files up to 2 GB and render arcs without loading the
      entire document into memory, thanks to its streaming architecture.
    question: Does the library work with large PSD files?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- arc drawing
- PSD manipulation
title: Cách java graphics vẽ cung trong Java
url: /vi/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách vẽ cung trong Java graphics bằng Java

## Giới thiệu
Trong hướng dẫn này, bạn sẽ khám phá cách **java graphics draw arc** bằng thư viện Aspose.PSD cho Java. Vẽ cung một cách lập trình là một yêu cầu phổ biến cho các thành phần UI tùy chỉnh, trực quan hoá dữ liệu và các báo cáo giàu đồ họa. Aspose.PSD cho Java cung cấp cho bạn toàn quyền kiểm soát các tệp PSD (Photoshop Document), cho phép tạo, chỉnh sửa và xuất ảnh mà không cần cài đặt Photoshop.

## Câu trả lời nhanh
- **Thư viện nào hỗ trợ vẽ cung trong Java?** Aspose.PSD for Java.  
- **Tôi có cần giấy phép cho việc sử dụng trong môi trường sản xuất không?** Có, cần giấy phép thương mại cho các triển khai không phải thử nghiệm.  
- **Các định dạng tệp nào tôi có thể xuất?** BMP, PNG, JPEG, TIFF, GIF và hơn nữa.  
- **Tôi có thể thay đổi độ dày và màu sắc của cung không?** Có, thông qua đối tượng `Pen` được truyền vào `drawArc`.  
- **API có tương thích với Java 8 và các phiên bản sau không?** Hoàn toàn tương thích với Java 8‑21.

## Java graphics draw arc là gì?
`java graphics draw arc` đề cập đến quá trình vẽ một đoạn đường cong—một cung—trên bề mặt đồ họa bằng các API vẽ của Java. Trong ngữ cảnh của Aspose.PSD, thao tác này được thực hiện trên một đối tượng `Graphics` đại diện cho một lớp trong tệp PSD.

## Tại sao nên dùng Aspose.PSD cho Java để vẽ cung?
Aspose.PSD hỗ trợ **hơn 50** định dạng hình ảnh và tài liệu, có thể xử lý các tệp PSD có **kích thước lên tới 2 GB**, và xử lý các tài liệu hàng trăm trang mà không cần tải toàn bộ tệp vào bộ nhớ. Hiệu năng được định lượng này làm cho nó trở thành lựa chọn lý tưởng cho việc tạo đồ họa phía máy chủ, nơi tốc độ và việc sử dụng bộ nhớ rất quan trọng.

## Yêu cầu trước
1. **Môi trường phát triển Java** – Cài đặt Java từ [trang web của Oracle](https://www.oracle.com/java/).  
2. **Thư viện Aspose.PSD cho Java** – Tải JAR mới nhất từ [trang tải xuống](https://releases.aspose.com/psd/java/). Thực hiện các hướng dẫn để thêm JAR vào classpath của dự án.

## Cách vẽ cung trong Java graphics bằng Java?
Tải một `PsdImage` mới, lấy bề mặt `Graphics` của nó, cấu hình một `Pen` với màu và độ dày mong muốn, và gọi `drawArc`. Chuỗi lệnh ngắn gọn này tạo ra cung và lưu kết quả trong một chuỗi phương thức duy nhất. Bằng cách điều chỉnh hình chữ nhật bao quanh và các tham số góc, bạn có thể kiểm soát kích thước, vị trí và góc quét của cung để đáp ứng yêu cầu thiết kế.

### Bước 1: thiết lập dự án Java của bạn
Tạo một dự án Java mới trong IDE yêu thích của bạn và thêm JAR Aspose.PSD vào đường dẫn biên dịch. Đảm bảo JAR được tham chiếu đúng để trình biên dịch có thể tìm thấy các lớp thư viện.

### Bước 2: nhập các gói cần thiết
To begin, import the necessary packages from Aspose.PSD for Java:
The `Pen` class defines the colour, width, and style of the line used to draw the arc.
```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```  
Các import này cung cấp các lớp `PsdImage`, `Graphics`, `Pen`, và các lớp màu cần thiết cho việc vẽ cung.

### Bước 3: khởi tạo đối tượng hình ảnh và đồ họa
Create an instance of `PsdImage` and obtain a `Graphics` object to draw on:
```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```  
Thay thế `"Your Document Directory"` bằng thư mục nơi bạn muốn lưu các tệp đầu ra.

### Bước 4: định nghĩa các tham số của cung
Set the geometry and style of the arc—its bounding rectangle, start angle, sweep angle, colour, and thickness:
```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```  
Điều chỉnh các giá trị để phù hợp với thiết kế hình ảnh bạn cần; ví dụ, một cung bán kính 200 px bắt đầu ở 45° và quét 270°.

### Bước 5: vẽ cung và lưu hình ảnh
Invoke `drawArc` on the `Graphics` object and persist the PSD (or export to another format):
The `drawArc` method of the `Graphics` class renders an arc defined by a bounding rectangle, start angle, and sweep angle using the specified `Pen`.
```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```  
Đoạn mã vẽ cung trên canvas và lưu nó dưới dạng tệp BMP. Thay đổi phần mở rộng tệp trong `outputPath` để xuất ra PNG, JPEG hoặc TIFF.

## Những lỗi thường gặp và cách khắc phục
- **Đơn vị góc không đúng** – Aspose.PSD yêu cầu góc tính bằng độ, không phải radian. Cung cấp radian sẽ gây ra kết quả không mong muốn.  
- **Độ dày Pen quá lớn** – Pen quá dày có thể khiến cung vượt ra ngoài giới hạn hình ảnh; giảm độ dày hoặc mở rộng canvas.  
- **Vấn đề đường dẫn tệp** – Sử dụng đường dẫn tuyệt đối hoặc đảm bảo thư mục làm việc có quyền ghi để tránh `IOException`.

## Câu hỏi thường gặp

**Q: Aspose.PSD cho Java có thể xử lý các hình dạng khác ngoài cung không?**  
A: Có, thư viện có thể vẽ hình chữ nhật, hình elip, đường thẳng, đa giác và các đường dẫn tùy chỉnh bằng cùng một API `Graphics`.

**Q: Làm thế nào để thay đổi màu và độ dày của cung?**  
A: Tạo một `Pen` với `Color` và độ rộng mong muốn, sau đó truyền đối tượng `Pen` đó vào `drawArc`.

**Q: Có thể xuất PSD sang định dạng khác ngoài BMP không?**  
A: Chắc chắn. Aspose.PSD hỗ trợ PNG, JPEG, TIFF, GIF và nhiều định dạng khác – chỉ cần thay đổi phần mở rộng tệp trong phương thức `save`.

**Q: Tôi có thể tìm thêm ví dụ và hỗ trợ cộng đồng ở đâu?**  
A: Truy cập [diễn đàn Aspose.PSD](https://forum.aspose.com/c/psd/34) để xem các hướng dẫn, mẫu mã và nhận trợ giúp từ các nhà phát triển khác.

**Q: Thư viện có hoạt động với các tệp PSD lớn không?**  
A: Có, nó có thể xử lý các tệp lên tới 2 GB và vẽ cung mà không cần tải toàn bộ tài liệu vào bộ nhớ, nhờ kiến trúc streaming.

---

**Cập nhật lần cuối:** 2026-09-03  
**Kiểm tra với:** Aspose.PSD for Java 24.11  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Vẽ và Lưu một Hình Chữ Nhật trong PSD bằng Aspose.PSD cho Java](/psd/java/basic-image-operations/simple-drawing/)
- [Thay đổi kích thước ảnh với Aspose.PSD cho Java – Vẽ hình dạng & Các thao tác ảnh cơ bản](/psd/java/basic-image-operations/)
- [Cách thay đổi màu viền trong Java bằng Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}