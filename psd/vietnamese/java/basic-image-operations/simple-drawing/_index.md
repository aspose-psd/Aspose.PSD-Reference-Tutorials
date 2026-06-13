---
date: 2026-06-13
description: Tìm hiểu cách vẽ rectangle trong PSD files bằng Aspose.PSD for Java.
  Hướng dẫn này hiển thị step‑by‑step code, adding layers, server‑side image processing
  và shape drawing.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: Thực hiện Vẽ Đơn Giản
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Cách vẽ hình chữ nhật trong PSD bằng Aspose.PSD for Java
url: /vi/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Vẽ Hình Chữ Nhật trong PSD bằng Aspose.PSD cho Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá **cách vẽ hình chữ nhật** bên trong tệp Photoshop PSD bằng thư viện Aspose.PSD thuần Java. Dù bạn đang xây dựng một quy trình xử lý tài sản phía máy chủ, tự động tạo thumbnail, hay thêm đồ họa động vào các thiết kế hiện có, các bước dưới đây sẽ cung cấp một giải pháp hoàn chỉnh, sẵn sàng cho môi trường sản xuất. Chúng ta sẽ đề cập đến việc tạo tài liệu PSD mới, thêm lớp, xóa nền, và cuối cùng vẽ cả hình chữ nhật màu đỏ và màu xanh—tất cả mà không cần khởi động Photoshop.

## Câu trả lời nhanh
- **Lớp chính để tạo tệp PSD là gì?** `PsdImage`
- **Phương thức nào xóa màu nền của lớp?** `Graphics.clear(Color)`
- **Làm thế nào để vẽ một hình chữ nhật màu đỏ?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Tôi có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; giấy phép cần thiết cho môi trường sản xuất.
- **Tôi có thể thao tác các tệp PSD hiện có bằng cùng một API không?** Có, Aspose.PSD hỗ trợ chỉnh sửa PSD đầy đủ.

## Vẽ một hình chữ nhật màu đỏ trong tệp PSD là gì?

Vẽ một hình chữ nhật màu đỏ có nghĩa là sử dụng đối tượng `Graphics` để render một hình chữ nhật được tô hoặc viền bằng màu đỏ lên một lớp cụ thể của ảnh PSD. Thao tác này thường dùng để làm nổi bật khu vực, tạo chỗ giữ chỗ, hoặc thêm đồ họa đơn giản một cách lập trình.

## Tại sao nên dùng Aspose.PSD cho Java để thao tác tệp PSD?

Aspose.PSD cho Java hỗ trợ **hơn 50 định dạng đầu vào và đầu ra**, có thể xử lý các tệp PSD hàng trăm trang mà không cần tải toàn bộ tệp vào bộ nhớ, và chạy trên bất kỳ nền tảng nào hỗ trợ Java 8 trở lên. Động cơ xử lý ảnh phía máy chủ của nó loại bỏ nhu cầu sử dụng Photoshop, giảm chi phí giấy phép, và cho phép quy trình tự động xử lý tới **10 GB** dữ liệu ảnh mỗi giờ trên một máy ảo vừa phải.

## Yêu cầu trước

- Java Development Kit (JDK) 8 hoặc mới hơn đã được cài đặt trên máy của bạn.  
- Thư viện Aspose.PSD cho Java. Bạn có thể tải xuống từ [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Nhập khẩu các gói

Các câu lệnh `import` đưa các lớp cần thiết vào phạm vi để bạn có thể làm việc với ảnh PSD, lớp, màu và đồ họa.

Lớp `PsdImage` là đối tượng cấp cao nhất của Aspose.PSD, đại diện cho một tệp PSD duy nhất trong bộ nhớ.  
`Graphics` cung cấp các primitive vẽ như đường thẳng, hình chữ nhật và hình elip.  
`Color` và `Pen` cho phép bạn chỉ định màu nét và độ dày.  
Lớp `Layer` đại diện cho một lớp ảnh riêng lẻ trong tài liệu PSD.  
Lớp `Rectangle` xác định vị trí và kích thước của khu vực hình chữ nhật được dùng cho các thao tác vẽ.  
Lớp `SolidBrush` dùng để tô các hình dạng bằng màu đồng nhất.

## Bước đầu tiên để tạo tài liệu PSD là gì?

Bạn khởi tạo `PsdImage` bằng cách cung cấp độ rộng và chiều cao của canvas tính bằng pixel, tạo ra một cấu trúc tệp PSD trống. Sau khi thiết lập bất kỳ lớp nền hoặc lớp khởi tạo nào, gọi phương thức `save` với đường dẫn tệp để ghi tài liệu ra đĩa. Điều này chuẩn bị ảnh cho các thao tác chỉnh sửa tiếp theo.

## Bước 1: Tạo Tài liệu Mới

Đầu tiên, tạo một tài liệu PSD mới với kích thước canvas mong muốn. Tài liệu này sẽ chứa lớp mà chúng ta sẽ vẽ lên.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Làm thế nào để thêm một lớp trống mới vào ảnh PSD?

Đầu tiên, tạo một thể hiện `Layer` mới với cùng độ rộng và chiều cao như `PsdImage` cha. Sau đó, thêm lớp này vào bộ sưu tập `Layers` của ảnh bằng phương thức `add`. Khi lớp đã là một phần của ảnh, lấy đối tượng `Graphics` của nó để thực hiện các thao tác vẽ; nếu không thực hiện bước này, các hình vẽ sẽ không hiển thị.

## Bước 2: Thêm Lớp

Tiếp theo, thêm một lớp trống mới phủ toàn bộ chiều rộng và chiều cao của ảnh. Các lớp là cần thiết để tách biệt các thao tác vẽ.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Mục đích của việc xóa màu nền của lớp là gì?

Gọi `Graphics.clear` với một `Color` cụ thể sẽ lấp đầy toàn bộ lớp bằng màu đó, thực chất đặt lại toàn bộ dữ liệu pixel. Điều này đảm bảo mọi nội dung trước đó bị xóa và lớp bắt đầu từ một nền đã biết, tránh hiện tượng trong suốt hoặc pha màu không mong muốn khi PSD được mở hoặc chỉnh sửa trong Photoshop.

## Bước 3: Vẽ Các Hình Dạng

Chúng ta sẽ sử dụng lớp `Graphics` để thao tác dữ liệu pixel của lớp. Dưới đây là ba ví dụ minh họa việc xóa nền và vẽ các hình chữ nhật với các màu khác nhau.

### Xóa Màu Lớp (đặt nền thành màu vàng)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### Vẽ Hình Chữ Nhật Đỏ (trọng tâm chính)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Vẽ Hình Chữ Nhật Xanh (ví dụ bổ sung)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## Làm thế nào để lưu tệp PSD đã chỉnh sửa vào đĩa?

Sử dụng phương thức `save` trên đối tượng `PsdImage`, truyền đường dẫn tệp đầy đủ và tùy chọn chỉ định định dạng ảnh mong muốn (mặc định là PSD). Điều này ghi tất cả các lớp, mặt nạ và lệnh vẽ vào một tệp PSD duy nhất tuân thủ chuẩn Photoshop, cho phép mở mà không có cảnh báo.

## Bước 4: Lưu Các Thay Đổi

Cuối cùng, ghi ảnh PSD đã chỉnh sửa ra đĩa. Tệp sẽ chứa lớp mới và các hình đã vẽ.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Các vấn đề thường gặp và giải pháp

- **Lớp không hiển thị sau khi vẽ:** Đảm bảo lớp đã được thêm vào ảnh **trước** khi tạo đối tượng `Graphics`. Bề mặt vẽ phải được gắn vào một lớp hợp lệ.
- **Màu sắc hiển thị không đúng:** Kiểm tra bạn đang sử dụng `Color.getRed()` (hoặc `Color.getBlue()`) thay vì tự tạo giá trị RGB vượt quá phạm vi 0‑255.
- **Tệp không được lưu:** Xác nhận đường dẫn `outputDir` tồn tại và ứng dụng có quyền ghi. Trên Linux, bạn có thể cần điều chỉnh quyền sở hữu thư mục hoặc dùng `Files.createDirectories`.
- **Hiệu năng chậm khi xử lý tệp lớn:** Sử dụng `setLoadOptions` của `PsdImage` để chỉ tải các kênh cần thiết, giảm tiêu thụ bộ nhớ cho các PSD lớn hơn 200 MB.

## Câu hỏi thường gặp

**Q1: Tôi có thể dùng Aspose.PSD cho Java để thao tác các tệp PSD hiện có không?**  
A1: Có, Aspose.PSD cho Java cung cấp chức năng phong phú để chỉnh sửa và thao tác các tệp PSD hiện có, bao gồm sắp xếp lại lớp, điều chỉnh mặt nạ và vẽ vector.

**Q2: Tôi có thể tìm hỗ trợ cho Aspose.PSD cho Java ở đâu?**  
A2: Bạn có thể truy cập [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) để nhận hỗ trợ từ cộng đồng và các phản hồi chính thức của Aspose.

**Q3: Có bản dùng thử miễn phí cho Aspose.PSD cho Java không?**  
A3: Có, bạn có thể truy cập bản dùng thử miễn phí [tại đây](https://releases.aspose.com/). Bản dùng thử bao gồm tất cả tính năng nhưng sẽ thêm watermark vào các tệp đã lưu.

**Q4: Làm sao để mua giấy phép cho Aspose.PSD cho Java?**  
A4: Bạn có thể mua giấy phép từ [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy). Các tùy chọn giấy phép bao gồm vĩnh viễn, thuê bao và giấy phép site.

**Q5: Có giấy phép tạm thời cho Aspose.PSD cho Java không?**  
A5: Có, bạn có thể nhận giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

## Các câu hỏi thường gặp bổ sung

**Q: Tôi có thể vẽ các hình dạng khác ngoài hình chữ nhật không?**  
A: Có, lớp `Graphics` cũng hỗ trợ vẽ elip, đường thẳng và các đường dẫn tùy chỉnh qua phương thức `drawPath`.

**Q: Aspose.PSD có hỗ trợ độ trong suốt cho các hình đã vẽ không?**  
A: Hoàn toàn có; bạn có thể dùng `SolidBrush` với màu ARGB để bao gồm độ trong suốt alpha, cho phép tạo lớp phủ bán trong suốt.

**Q: Có thể chỉnh sửa độ mờ của một lớp không?**  
A: Có, mỗi đối tượng `Layer` có phương thức `setOpacity` nhận giá trị từ 0 đến 255, cho phép kiểm soát độ trong suốt của lớp một cách chi tiết.

**Q: Làm sao để tải một tệp PSD hiện có thay vì tạo mới?**  
A: Dùng `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` trước khi thao tác các lớp. Ảnh đã tải sẽ giữ nguyên tất cả các lớp và mặt nạ gốc.

## Kết luận

Bạn đã nắm vững **cách vẽ hình chữ nhật** và thao tác các lớp bên trong tệp PSD bằng Aspose.PSD cho Java. Bằng cách tạo tài liệu, thêm lớp, xóa nền và vẽ bằng API `Graphics`, bạn có thể tự động hoá vô số nhiệm vụ thiết kế đồ họa phía máy chủ. Hãy thử nghiệm với các loại bút, cọ và hiệu ứng lớp khác nhau để mở rộng nền tảng này thành các pipeline tạo ảnh đầy đủ tính năng.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## Các hướng dẫn liên quan

- [How to Draw Shapes Java – Basic Image Operations](/psd/java/basic-image-operations/)
- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [Crop Image by Rectangle in Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**Last Updated:** 2026-06-13  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose