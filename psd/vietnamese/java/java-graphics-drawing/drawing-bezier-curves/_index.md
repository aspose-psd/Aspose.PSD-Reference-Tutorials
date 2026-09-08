---
date: 2026-09-08
description: Tìm hiểu cách vẽ đường cong Bezier trong Java bằng Aspose.PSD cho Java.
  Thực hiện các hướng dẫn step‑by‑step, prerequisites, và code‑free examples.
keywords:
- how to draw bezier
- how to use pen
- bezier curve example java
- java graphics draw curve
lastmod: 2026-09-08
linktitle: Vẽ Đường Cong Bezier trong Java
og_description: Cách vẽ đường cong Bezier trong Java bằng Aspose.PSD. Hướng dẫn này
  bao gồm prerequisites, step‑by‑step drawing, và các mẹo cho high‑resolution images.
og_image_alt: Screenshot of a Java application rendering a Bezier curve with Aspose.PSD
og_title: Cách vẽ đường cong Bezier trong Java bằng thư viện Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  headline: How to draw bezier curves in Java with Aspose.PSD library
  type: TechArticle
- description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  name: How to draw bezier curves in Java with Aspose.PSD library
  steps:
  - name: create an image instance
    text: 'The `PsdImage` class is Aspose.PSD''s top‑level object that represents
      a single PSD file in memory. First, you need to create an instance of the `PsdImage`
      class, which represents a PSD image in memory. Explanation: - `PsdImage` is
      instantiated with width and height parameters (100 × 100 pixels in th'
  - name: initialize graphics context
    text: 'The `Graphics` class provides drawing capabilities on a `PsdImage`. Next,
      initialize an instance of the `Graphics` class to perform drawing operations
      on the image. Explanation: - `Graphics` object is initialized with the `image`
      instance, allowing drawing operations.'
  - name: clear the graphics surface
    text: 'The `clear()` method sets the background colour of the graphics surface.
      Clear the graphics surface using a specific background colour, here `Color.getYellow()`.
      Explanation: - `clear()` method sets the background colour of the graphics surface.'
  - name: initialize pen for drawing
    text: 'The `Pen` object defines stroke attributes such as colour and width. Set
      up a `Pen` object with properties like colour and width to define how the curve
      will be drawn. Explanation: - `Pen` is initialized with black colour and 3‑pixel
      width.'
  - name: define bezier curve parameters
    text: 'Control points determine the curvature. Specify the control points and
      end points for the Bezier curve. Explanation: - `startX`, `startY`: Starting
      point of the curve. - `controlX1`, `controlY1`: First control point. - `controlX2`,
      `controlY2`: Second control point. - `endX`, `endY`: Ending point of'
  - name: draw the bezier curve
    text: 'The `drawBezier()` method renders the curve using the supplied `Pen` and
      points. Use the `drawBezier()` method to draw the Bezier curve onto the image
      using the previously defined `Pen` and control points. Explanation: - `drawBezier()`
      method draws the curve with specified parameters using the `blac'
  - name: save the image
    text: Saving the image persists the drawing to disk. Save the drawn image to a
      BMP file format.
  type: HowTo
- questions:
  - answer: Yes, repeat the `drawBezier()` call inside a loop, updating the control
      points for each curve.
    question: Can I draw multiple Bezier curves in the same image?
  - answer: Modify the `Pen` object's colour property (`Color.getBlack()` in the example)
      before invoking `drawBezier()`.
    question: How can I change the colour of the Bezier curve?
  - answer: Yes, Aspose.PSD for Java supports high‑resolution images with efficient
      memory management, handling files larger than 500 MB without loading the entire
      file into memory.
    question: Is Aspose.PSD for Java suitable for high‑resolution images?
  - answer: Yes, Aspose.PSD for Java supports exporting to PNG, JPEG, TIFF, and many
      other raster formats.
    question: Can I export the image to formats other than BMP?
  - answer: Visit the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and code samples.
    question: Where can I find more examples and documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- drawing bezier
- Aspose.PSD
- Java graphics
- curve drawing
title: Cách vẽ đường cong Bezier trong Java bằng thư viện Aspose.PSD
url: /vi/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách vẽ đường cong Bezier trong Java với thư viện Aspose.PSD

## Giới thiệu
Nếu bạn cần biết **cách vẽ bezier** shapes trong một ứng dụng Java desktop hoặc server, Aspose.PSD for Java cung cấp cho bạn một API sạch sẽ, tiết kiệm bộ nhớ. Trong hướng dẫn này, bạn sẽ thấy các bước chính xác để tạo một canvas PSD, cấu hình bút vẽ, xác định các điểm điều khiển và vẽ một đường cong Bezier mượt—tất cả mà không cần viết bất kỳ mã thao tác pixel cấp thấp nào.

## Câu trả lời nhanh
- **Thư viện nào xử lý việc vẽ?** Aspose.PSD for Java.  
- **Cần bao nhiêu dòng mã?** Khoảng mười câu lệnh ngắn gọn.  
- **Tôi có thể thay đổi màu đường cong không?** Có, bằng cách điều chỉnh thuộc tính màu của `Pen`.  
- **Có hỗ trợ xuất ảnh độ phân giải cao không?** Có, lên tới các tệp 500 MB mà không cần tải toàn bộ vào bộ nhớ.  
- **Tôi có cần giấy phép thương mại không?** Bản dùng thử miễn phí hoạt động cho phát triển; cần giấy phép cho môi trường sản xuất.

## Đường cong Bezier là gì?
Đường cong Bezier là một đường mượt được định nghĩa toán học, được điều khiển bởi hai hoặc nhiều điểm. Nó được sử dụng rộng rãi trong đồ họa vector, hoạt ảnh và thiết kế giao diện người dùng để tạo các hình dạng tinh tế, có thể mở rộng. Hình dạng của đường cong được xác định bởi điểm bắt đầu, điểm kết thúc và một hoặc nhiều điểm điều khiển ảnh hưởng đến độ cong, cho phép các nhà thiết kế mô hình các đường phức tạp chỉ với các tham số đơn giản.

## Tại sao nên sử dụng Aspose.PSD để vẽ đường cong Bezier?
Aspose.PSD hỗ trợ **hơn 30 định dạng ảnh** và có thể xử lý **các tệp PSD hàng trăm trang** mà không cần tải toàn bộ tài liệu vào RAM. Phương thức `drawBezier()` của thư viện tự động xử lý khử răng cưa và quản lý màu sắc, mang lại kết quả pixel‑perfect trong vòng chưa đầy một giây cho các canvas thường kích thước 100 × 100.

## Yêu cầu trước
1. **Java Development Kit (JDK)** – bất kỳ phiên bản mới nào (8 trở lên) đã được cài đặt và cấu hình.  
2. **Aspose.PSD for Java JAR** – tải xuống thư viện Aspose.PSD for Java từ [Tải xuống Aspose.PSD Java](https://releases.aspose.com/psd/java/) và thêm vào classpath của dự án.  
3. **Integrated Development Environment (IDE)** – chẳng hạn như Eclipse, IntelliJ IDEA hoặc NetBeans, đã được thiết lập với JDK.

## Nhập các gói
Những import sau đây đưa vào các lớp Aspose.PSD cần thiết cho việc tạo ảnh và vẽ.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Cách vẽ đường cong bezier trong Java?
Tải một `PsdImage` trống, tạo một đối tượng `Graphics`, cấu hình một `Pen`, xác định các điểm bắt đầu, điều khiển và kết thúc, gọi `drawBezier()`, và cuối cùng lưu ảnh. Trình tự này tạo ra một đường cong mượt mà chỉ với một lời gọi phương thức và không yêu cầu tính toán pixel thủ công.

### Bước 1: tạo một thể hiện ảnh
`Lớp `PsdImage` là đối tượng cấp cao nhất của Aspose.PSD đại diện cho một tệp PSD duy nhất trong bộ nhớ. Đầu tiên, bạn cần tạo một thể hiện của lớp `PsdImage`, đại diện cho một ảnh PSD trong bộ nhớ.
```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```
Explanation:
- `PsdImage` được khởi tạo với các tham số chiều rộng và chiều cao (100 × 100 pixel trong ví dụ này).

### Bước 2: khởi tạo ngữ cảnh đồ họa
`Lớp `Graphics` cung cấp khả năng vẽ trên một `PsdImage`. Tiếp theo, khởi tạo một thể hiện của lớp `Graphics` để thực hiện các thao tác vẽ trên ảnh.
```java
Graphics graphics = new Graphics(image);
```
Explanation:
- `Đối tượng `Graphics` được khởi tạo với thể hiện `image`, cho phép thực hiện các thao tác vẽ.`

### Bước 3: xóa bề mặt đồ họa
Phương thức `clear()` đặt màu nền cho bề mặt đồ họa. Xóa bề mặt đồ họa bằng một màu nền cụ thể, ở đây là `Color.getYellow()`.
```java
graphics.clear(Color.getYellow());
```
Explanation:
- `Phương thức `clear()` đặt màu nền cho bề mặt đồ họa.`

### Bước 4: khởi tạo bút vẽ
Đối tượng `Pen` xác định các thuộc tính nét vẽ như màu và độ rộng. Thiết lập một đối tượng `Pen` với các thuộc tính như màu và độ rộng để xác định cách vẽ đường cong.
```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```
Explanation:
- `Pen` được khởi tạo với màu đen và độ rộng 3 pixel.

### Bước 5: xác định các tham số đường cong bezier
Các điểm điều khiển xác định độ cong. Xác định các điểm điều khiển và điểm cuối cho đường cong Bezier.
```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```
Explanation:
- `startX`, `startY`: Điểm bắt đầu của đường cong.  
- `controlX1`, `controlY1`: Điểm điều khiển thứ nhất.  
- `controlX2`, `controlY2`: Điểm điều khiển thứ hai.  
- `endX`, `endY`: Điểm kết thúc của đường cong.

### Bước 6: vẽ đường cong bezier
Phương thức `drawBezier()` vẽ đường cong bằng cách sử dụng `Pen` và các điểm đã cung cấp. Sử dụng phương thức `drawBezier()` để vẽ đường cong Bezier lên ảnh bằng `Pen` và các điểm điều khiển đã định nghĩa trước.
```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```
Explanation:
- `Phương thức `drawBezier()` vẽ đường cong với các tham số đã chỉ định bằng `blackPen`.`

### Bước 7: lưu ảnh
Lưu ảnh sẽ ghi lại bản vẽ lên đĩa. Lưu ảnh đã vẽ dưới định dạng tệp BMP.
```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

## Các vấn đề thường gặp và giải pháp
- **Đường cong xuất hiện phẳng** – Kiểm tra xem các điểm điều khiển có thẳng hàng với điểm bắt đầu và kết thúc không. Hãy dịch chuyển chúng một chút để tạo độ cong.  
- **Màu không thay đổi** – Đảm bảo bạn đã thay đổi màu của `Pen` trước khi gọi `drawBezier()`.  
- **Lỗi thiếu bộ nhớ trên canvas lớn** – Sử dụng các hàm khởi tạo `PsdImage` cho phép streaming, hoặc chia vẽ thành các ô.

## Câu hỏi thường gặp

**Q: Tôi có thể vẽ nhiều đường Bezier trong cùng một ảnh không?**  
A: Có, lặp lại lời gọi `drawBezier()` trong một vòng lặp, cập nhật các điểm điều khiển cho mỗi đường cong.

**Q: Làm sao tôi có thể thay đổi màu của đường Bezier?**  
A: Thay đổi thuộc tính màu của đối tượng `Pen` (`Color.getBlack()` trong ví dụ) trước khi gọi `drawBezier()`.

**Q: Aspose.PSD for Java có phù hợp cho ảnh độ phân giải cao không?**  
A: Có, Aspose.PSD for Java hỗ trợ ảnh độ phân giải cao với quản lý bộ nhớ hiệu quả, xử lý các tệp lớn hơn 500 MB mà không tải toàn bộ tệp vào bộ nhớ.

**Q: Tôi có thể xuất ảnh sang các định dạng khác ngoài BMP không?**  
A: Có, Aspose.PSD for Java hỗ trợ xuất ra PNG, JPEG, TIFF và nhiều định dạng raster khác.

**Q: Tôi có thể tìm thêm ví dụ và tài liệu ở đâu?**  
A: Tham khảo [tài liệu Aspose.PSD cho Java](https://reference.aspose.com/psd/java/) để có các hướng dẫn chi tiết và mẫu mã.

---

**Last Updated:** 2026-09-08  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## Hướng dẫn liên quan

- [Thay đổi kích thước ảnh với Aspose.PSD cho Java – Vẽ hình dạng & Các thao tác ảnh cơ bản](/psd/java/basic-image-operations/)
- [Vẽ và lưu một hình chữ nhật trong PSD bằng Aspose.PSD cho Java](/psd/java/basic-image-operations/simple-drawing/)
- [Cách thay đổi màu nét vẽ Java bằng Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}