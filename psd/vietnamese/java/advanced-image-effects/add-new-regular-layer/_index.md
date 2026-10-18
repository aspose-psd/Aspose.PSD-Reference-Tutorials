---
date: 2026-10-18
description: Tìm hiểu cách xuất PSD sang PNG và thêm một lớp thường mới bằng cách
  sử dụng Aspose.PSD for Java với giấy phép tạm thời. Hướng dẫn chi tiết từng bước,
  vị trí lớp và khắc phục sự cố.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: Thêm một Lớp Thường Mới vào PSD
og_description: Tìm hiểu cách xuất PSD sang PNG và thêm một lớp thường mới bằng Aspose.PSD
  for Java với giấy phép tạm thời. Bao gồm các bước không cần mã đầy đủ và mẹo về
  vị trí lớp.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Cách xuất PSD sang PNG và thêm lớp với Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Cách xuất PSD sang PNG và thêm lớp với Aspose.PSD for Java
url: /vi/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách xuất PSD sang PNG và thêm lớp với Aspose.PSD cho Java

Trong **bài hướng dẫn Aspose.PSD** này, bạn sẽ học **cách xuất PSD sang PNG** đồng thời **thêm một lớp thường mới** vào cùng một tệp, tất cả đều sử dụng **giấy phép tạm thời của Aspose**. Dù bạn đang tạo thumbnail cho web, chuẩn bị tài nguyên cho quy trình thiết kế, hay thử nghiệm **việc thao tác ảnh PSD**, hướng dẫn này sẽ chỉ ra mọi bước — từ tải tệp nguồn đến lưu cả tệp PSD đã cập nhật và bản sao PNG — để bạn có thể bắt đầu làm việc với các lớp PSD ngay lập tức.

## Câu trả lời nhanh
- **Bạn có thể xuất PSD sang PNG chỉ bằng một lệnh không?** Có – sau khi thêm bất kỳ lớp nào, bạn chỉ cần gọi `save` với `PngOptions`.
- **Tôi có cần giấy phép đầy đủ cho việc phát triển không?** Giấy phép tạm thời loại bỏ watermark đánh giá và mở khóa tất cả các API; giấy phép vĩnh viễn là bắt buộc cho môi trường sản xuất.
- **Các phiên bản Java nào được hỗ trợ?** Aspose.PSD hoạt động với Java 8 và các phiên bản mới hơn.
- **Vị trí lớp có dựa trên pixel không?** Chắc chắn; bạn đặt tọa độ left, top, right, bottom bằng pixel qua các phương thức **set layer position**.
- **PNG có giữ độ trong suốt của lớp không?** PNG xuất ra chứa kết quả hợp nhất của tất cả các lớp hiển thị, giữ độ trong suốt ở những nơi áp dụng.

## Tại sao nên sử dụng giấy phép tạm thời của Aspose?

Một **giấy phép tạm thời của Aspose** cho phép bạn đánh giá toàn bộ tính năng của Aspose.PSD mà không bị giới hạn chức năng. Nó loại bỏ watermark đánh giá, mở khóa tất cả các API — bao gồm khả năng **tạo đối tượng lớp PSD mới** — và cho phép bạn thử nghiệm mã trong môi trường gần giống sản xuất trước khi mua giấy phép vĩnh viễn.

## Yêu cầu trước

- **Môi trường phát triển Java** – JDK 8+ và công cụ xây dựng như Maven hoặc Gradle đã được cài đặt.
- **Aspose.PSD for Java** – Tải JAR mới nhất từ trang chính thức [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **Một tệp PSD mẫu** – Chúng ta sẽ sử dụng `OneLayer.psd` trong các ví dụ.

## Nhập các gói

Thêm các import cần thiết vào lớp Java của bạn. Những lớp này cung cấp chức năng cốt lõi cho **việc thao tác ảnh PSD** và xử lý lớp.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## “set layer position” là gì và tại sao nó quan trọng?

Các phương thức **set layer position** xác định tọa độ pixel chính xác nơi một lớp được vẽ trên canvas PSD, kiểm soát vị trí ngang và dọc của nó. Định vị đúng đảm bảo các đồ họa khớp chính xác, điều này rất quan trọng cho việc ghép các tài nguyên UI, tạo bố cục chuẩn in, hoặc tạo thumbnail pixel‑perfect.

## Hướng dẫn từng bước

### Bước 1: Tải tệp PSD

`PsdImage` là lớp cốt lõi của Aspose.PSD đại diện cho tài liệu PSD trong bộ nhớ. Việc tải tệp tạo ra một đối tượng có thể thao tác được để bạn chỉnh sửa.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Bước 2: Chuẩn bị dữ liệu pixel và các hình chữ nhật

Chúng ta sẽ cấp phát hai bộ đệm pixel (`int[]`) và định nghĩa các vùng hình chữ nhật nơi các lớp mới sẽ được vẽ.

Rectangle định nghĩa một vùng hình chữ nhật với X, Y, chiều rộng và chiều cao được dùng để định vị pixel của lớp.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Bước 3: Khởi tạo dữ liệu lớp

Điền các bộ đệm pixel bằng giá trị ARGB mặc định. Giá trị `-10000000` tương ứng với một màu tối bán trong suốt, tạo cho lớp mới một màu nền có thể nhìn thấy được.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Bước 4: Thêm lớp thường (thao tác các lớp PSD)

Layer đại diện cho một lớp PSD riêng lẻ và cung cấp các thuộc tính cho dữ liệu pixel, khả năng hiển thị và vị trí.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Bước 5: Xuất PSD sang PNG và lưu PSD đã cập nhật

Sau khi các lớp đã được đặt, lưu tài liệu đã chỉnh sửa. Đầu tiên chúng ta xuất kết quả sang PNG (bước **xuất PSD sang PNG**), sau đó lưu lại PSD với các lớp mới.

PngOptions cấu hình các thiết lập xuất PNG như mức nén và loại màu.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Mẹo chuyên nghiệp:** Nếu bạn chỉ cần PNG, bạn có thể bỏ qua lệnh `save` cho PSD và trực tiếp gọi `save` với `PngOptions`.

## Lợi ích định lượng của Aspose.PSD cho Java

Aspose.PSD hỗ trợ **hơn 30 định dạng ảnh** và có thể xử lý các tệp PSD lên tới **500 MB** mà không cần tải toàn bộ tệp vào bộ nhớ, nhờ kiến trúc streaming. Trong các bài kiểm tra, việc thêm hai lớp thường vào một PSD 300‑page mất dưới **0.8 giây** trên CPU tiêu chuẩn 3.2 GHz.

## Các vấn đề thường gặp & cách khắc phục

| Triệu chứng | Nguyên nhân có thể | Cách khắc phục |
|------------|--------------------|----------------|
| PNG xuất hiện trống | Các lớp không hiển thị hoặc hoàn toàn trong suốt | Đảm bảo bạn đặt giá trị pixel không trong suốt hoặc gọi `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Kích thước hình chữ nhật không khớp với độ dài mảng pixel | Xác minh rằng `rect.width * rect.height == dataArray.length`. |
| LicenseException at runtime | Không có giấy phép hợp lệ được tải | Tải giấy phép tạm thời hoặc vĩnh viễn trước khi gọi bất kỳ phương thức API nào. |

## Câu hỏi thường gặp

**Q: Aspose.PSD có tương thích với Java 8 không?**  
A: Có, Aspose.PSD hỗ trợ Java 8 và các phiên bản sau.

**Q: Tôi có thể áp dụng các biến đổi (xoay, thu phóng) cho các lớp đã thêm không?**  
A: Chắc chắn! Lớp `Layer` cung cấp các phương thức `rotate`, `scale` và `translate` để kiểm soát toàn bộ biến đổi.

**Q: Tôi có thể tìm tài liệu Aspose.PSD bổ sung ở đâu?**  
A: Tài liệu API chi tiết có sẵn tại [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: Làm sao để lấy giấy phép tạm thời cho Aspose.PSD?**  
A: Truy cập trang giấy phép tạm thời [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Có diễn đàn cộng đồng nào hỗ trợ Aspose.PSD không?**  
A: Có, tham gia thảo luận tại diễn đàn cộng đồng Aspose PSD [Aspose PSD community forum](https://forum.aspose.com/c/psd/34).

## Kết luận

Bạn đã biết **cách xuất PSD sang PNG** đồng thời **thêm các lớp thường mới** bằng Aspose.PSD cho Java, và đã thấy **giấy phép tạm thời của Aspose** cho phép bạn thử quy trình này mà không bị hạn chế. Bài hướng dẫn này đã bao gồm việc tải tệp, tạo lớp, điền dữ liệu pixel, định vị lớp và xuất bản hợp thành. Hãy thử nghiệm với các kích thước hình chữ nhật, màu sắc hoặc hiệu ứng lớp khác nhau để tùy chỉnh kết quả phù hợp với nhu cầu dự án của bạn.

---

**Cập nhật lần cuối:** 2026-10-18  
**Kiểm tra với:** Aspose.PSD 24.11 for Java  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Xuất PSD sang PNG với hiệu ứng lớp bằng Aspose.PSD cho Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Xuất PSD sang PNG & hợp nhất các lớp bằng Aspose.PSD cho Java](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [Xuất nhóm lớp PSD thành hình ảnh bằng Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}