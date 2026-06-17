---
date: 2026-04-08
description: Học cách xuất tệp PSD sang PNG và tạo lớp PSD mới bằng Aspose.PSD cho
  Java sử dụng giấy phép tạm thời của Aspose. Hướng dẫn từng bước này bao gồm việc
  thao tác ảnh PSD và đặt vị trí lớp.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Thêm một lớp thường mới vào PSD
second_title: Aspose.PSD Java API
title: Xuất PSD sang PNG & Thêm lớp thường mới bằng Aspose.PSD cho Java – giấy phép
  tạm thời của Aspose
url: /vi/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất PSD sang PNG & Thêm Lớp Thường Mới bằng Aspose.PSD cho Java

## Giới thiệu

Trong **aspose psd tutorial** này, bạn sẽ khám phá cách **export PSD to PNG** đồng thời **creating a new regular layer** trong cùng một tệp, **using an aspose temporary license** cho việc phát triển. Cho dù bạn cần tạo các hình thu nhỏ sẵn sàng cho web, chuẩn bị tài nguyên cho quy trình thiết kế, hoặc chỉ đơn giản thử nghiệm với **psd image manipulation**, Aspose.PSD cho Java cung cấp cho bạn kiểm soát lập trình đầy đủ. Chúng tôi sẽ hướng dẫn từng bước—từ việc tải tệp nguồn đến lưu cả PSD đã cập nhật và bản sao PNG—để bạn có thể bắt đầu thao tác các lớp PSD ngay lập tức.

## Câu trả lời nhanh
- **Có thể xuất PSD sang PNG chỉ bằng một lệnh không?** Có, sau khi thêm các lớp, bạn có thể gọi `save` với `PngOptions`.
- **Tôi có cần giấy phép cho việc phát triển không?** Giấy phép tạm thời hoạt động cho việc thử nghiệm; giấy phép đầy đủ là bắt buộc cho môi trường sản xuất.
- **Phiên bản Java nào được hỗ trợ?** Aspose.PSD hoạt động với Java 8 và các phiên bản mới hơn.
- **Vị trí lớp có dựa trên pixel không?** Có, bạn thiết lập các tọa độ left, top, right, bottom bằng pixel bằng cách sử dụng các phương thức **set layer position**.
- **PNG có giữ được độ trong suốt của lớp không?** PNG sẽ chứa kết quả hợp nhất của tất cả các lớp có thể nhìn thấy.

## Tại sao nên sử dụng giấy phép tạm thời của Aspose?

Giấy phép tạm thời **aspose** cho phép bạn đánh giá toàn bộ tính năng của Aspose.PSD mà không có bất kỳ hạn chế chức năng nào. Nó loại bỏ watermark đánh giá, mở khóa tất cả các API—bao gồm khả năng **create new psd layer** objects—and lets you test your code in a production‑like environment before purchasing a permanent license.

## Yêu cầu trước

- **Java Development Environment** – JDK 8+ và một công cụ xây dựng (Maven/Gradle) đã được cài đặt.
- **Aspose.PSD for Java** – Tải JAR mới nhất từ trang chính thức [here](https://releases.aspose.com/psd/java/).
- **A sample PSD file** – Chúng tôi sẽ sử dụng `OneLayer.psd` trong các ví dụ.

## Nhập các gói

Thêm các import cần thiết vào lớp Java của bạn. Các lớp này cung cấp chức năng cốt lõi cho **psd image manipulation** và việc xử lý lớp.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## “set layer position” là gì và tại sao nó quan trọng?

Khi bạn thêm một lớp mới, bạn cần xác định vị trí của nó trên canvas. Các phương thức `setLeft`, `setTop`, `setRight` và `setBottom` **set layer position** theo tọa độ pixel. Việc định vị chính xác đảm bảo đồ họa của bạn được sắp xếp đúng như mong đợi, điều này rất quan trọng cho các nhiệm vụ như ghép các tài sản UI hoặc chuẩn bị các tệp sẵn sàng in.

## Hướng dẫn từng bước

### Bước 1: Tải tệp PSD

Đầu tiên, tải PSD hiện có mà bạn muốn chỉnh sửa. Điều này sẽ cung cấp cho bạn một đối tượng `PsdImage` để làm việc.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Bước 2: Chuẩn bị dữ liệu pixel và các hình chữ nhật

Chúng ta sẽ tạo hai bộ đệm pixel (`int[]`) và xác định các vùng hình chữ nhật nơi các lớp mới sẽ được vẽ. Đây là nền tảng cho **creating a new psd layer**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Bước 3: Khởi tạo dữ liệu lớp

Điền các bộ đệm pixel bằng giá trị ARGB mặc định. Giá trị `-10000000` tương ứng với một màu tối bán trong suốt.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Bước 4: Thêm các lớp thường (Thao tác các lớp PSD)

Bây giờ chúng ta **add regular layers** vào hình ảnh PSD và **set layer position** bằng cách sử dụng các thuộc tính left, top, right và bottom. Điều này minh họa cách **manipulate PSD layers** một cách lập trình.

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

### Bước 5: Xuất PSD sang PNG và Lưu PSD đã cập nhật

Sau khi các lớp đã được đặt, lưu tài liệu đã chỉnh sửa. Đầu tiên chúng ta xuất kết quả sang PNG (bước **export psd to png**), sau đó chúng ta lưu PSD với các lớp mới.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Mẹo chuyên nghiệp:** Nếu bạn chỉ cần PNG, bạn có thể bỏ qua lệnh `save` của PSD và trực tiếp gọi `save` với `PngOptions`.

## Các vấn đề thường gặp & Khắc phục

| Triệu chứng | Nguyên nhân có thể | Cách khắc phục |
|------------|--------------------|----------------|
| PNG xuất hiện trống | Các lớp không hiển thị hoặc hoàn toàn trong suốt | Đảm bảo bạn đặt giá trị pixel không trong suốt hoặc gọi `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Kích thước hình chữ nhật không khớp với độ dài mảng pixel | Xác minh rằng `rect.width * rect.height == dataArray.length`. |
| LicenseException khi chạy | Không có giấy phép hợp lệ được tải | Tải một giấy phép tạm thời hoặc vĩnh viễn trước khi gọi bất kỳ phương thức API nào. |

## Câu hỏi thường gặp

**Q: Aspose.PSD có tương thích với Java 8 không?**  
A: Có, Aspose.PSD hỗ trợ Java 8 và các phiên bản sau.

**Q: Tôi có thể áp dụng các biến đổi (xoay, thu phóng) cho các lớp đã thêm không?**  
A: Chắc chắn! Lớp `Layer` cung cấp các phương thức như `rotate`, `scale`, và `translate` để kiểm soát đầy đủ các biến đổi.

**Q: Tôi có thể tìm tài liệu Aspose.PSD bổ sung ở đâu?**  
A: Tài liệu API chi tiết có sẵn [here](https://reference.aspose.com/psd/java/).

**Q: Làm thế nào để tôi có được giấy phép tạm thời cho Aspose.PSD?**  
A: Truy cập trang giấy phép tạm thời [here](https://purchase.aspose.com/temporary-license/).

**Q: Có diễn đàn cộng đồng nào hỗ trợ Aspose.PSD không?**  
A: Có, tham gia thảo luận trên diễn đàn Aspose [here](https://forum.aspose.com/c/psd/34).

## Kết luận

Bạn đã học cách **export PSD to PNG** đồng thời **adding new regular layers** bằng Aspose.PSD cho Java, và bạn đã thấy cách **aspose temporary license** cho phép bạn thử quy trình này mà không có hạn chế. Bài hướng dẫn này trình bày các khả năng cốt lõi của **psd image manipulation**: tải tệp, tạo lớp, điền dữ liệu pixel và xuất bản phối hợp cuối cùng. Hãy tự do thử nghiệm với các kích thước hình chữ nhật, màu pixel hoặc hiệu ứng lớp khác nhau để điều chỉnh đầu ra phù hợp với nhu cầu dự án của bạn.

---

**Cập nhật lần cuối:** 2026-04-08  
**Kiểm tra với:** Aspose.PSD 24.11 for Java  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}