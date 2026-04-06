---
date: 2025-12-27
description: Tìm hiểu cách vẽ hình chữ nhật màu đỏ và các hình dạng khác trong tệp
  PSD bằng Aspose.PSD cho Java. Hướng dẫn từng bước này bao gồm tạo tài liệu, thêm
  lớp và vẽ bằng các ví dụ mã.
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Vẽ hình chữ nhật màu đỏ bằng Aspose.PSD cho Java
url: /vi/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vẽ Hình Chữ Nhật Đỏ bằng Aspose.PSD cho Java

## Giới thiệu

Chào mừng bạn đến với hướng dẫn từng bước về cách **vẽ hình chữ nhật đỏ** bằng Aspose.PSD cho Java! Trong tutorial này, chúng ta sẽ tạo một tài liệu PSD mới, thêm một lớp, và vẽ các hình dạng với màu tùy chỉnh. Dù bạn đang tự động hoá tài sản đồ họa hay xây dựng backend cho công cụ thiết kế, tutorial này cung cấp những khối xây dựng cơ bản cần thiết.

## Câu trả lời nhanh
- **Lớp chính để tạo file PSD là gì?** `PsdImage`
- **Phương thức nào xóa màu nền của lớp?** `Graphics.clear(Color)`
- **Làm sao để vẽ một hình chữ nhật đỏ?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; giấy phép cần thiết cho môi trường sản xuất.
- **Có thể thao tác các file PSD hiện có bằng cùng API không?** Có, Aspose.PSD hỗ trợ chỉnh sửa PSD đầy đủ.

## Vẽ hình chữ nhật đỏ trong file PSD là gì?
Vẽ một hình chữ nhật đỏ có nghĩa là sử dụng đối tượng `Graphics` để render một hình chữ nhật được tô hoặc viền bằng màu đỏ lên một lớp cụ thể của ảnh PSD. Thao tác này thường dùng để làm nổi bật khu vực, tạo chỗ giữ chỗ, hoặc thêm đồ họa đơn giản một cách lập trình.

## Tại sao nên dùng Aspose.PSD cho Java để thao tác file PSD?
Aspose.PSD cung cấp API thuần Java cho phép bạn đọc, chỉnh sửa và ghi các file Photoshop PSD mà không cần cài đặt Photoshop. Nó hỗ trợ quản lý lớp, thao tác màu và vẽ vector, làm cho nó trở nên lý tưởng cho xử lý ảnh phía server, pipeline tài sản tự động và tạo đồ họa tùy chỉnh.

## Yêu cầu trước

- Java Development Kit (JDK) đã được cài đặt trên máy của bạn.  
- Thư viện Aspose.PSD cho Java. Bạn có thể tải về từ [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Nhập khẩu các gói

Để bắt đầu, nhập các lớp cần thiết vào dự án Java của bạn:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Bước 1: Tạo tài liệu mới

Đầu tiên, tạo một tài liệu PSD mới với kích thước canvas mong muốn. Tài liệu này sẽ chứa lớp mà chúng ta sẽ vẽ lên.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Bước 2: Thêm một lớp

Tiếp theo, thêm một lớp trống mới có kích thước đầy đủ chiều rộng và chiều cao của ảnh. Các lớp là cần thiết để tách biệt các thao tác vẽ.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Bước 3: Vẽ các hình dạng

Chúng ta sẽ sử dụng lớp `Graphics` để thao tác dữ liệu pixel của lớp. Dưới đây là ba ví dụ minh họa việc xóa nền và vẽ các hình chữ nhật với màu khác nhau.

### Xóa màu lớp (đặt nền thành màu vàng)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Vẽ một hình chữ nhật đỏ (trọng tâm chính)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Vẽ một hình chữ nhật xanh dương (ví dụ bổ sung)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Bước 4: Lưu các thay đổi

Cuối cùng, ghi ảnh PSD đã chỉnh sửa ra đĩa. File sẽ chứa lớp mới và các hình dạng đã vẽ.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Các vấn đề thường gặp và giải pháp

- **Lớp không hiển thị sau khi vẽ:** Đảm bảo lớp đã được thêm vào ảnh **trước** khi tạo đối tượng `Graphics`.
- **Màu sắc hiển thị không đúng:** Kiểm tra bạn đang sử dụng `Color.getRed()` (hoặc các phương thức tĩnh khác) thay vì giá trị RGB tùy chỉnh có thể vượt quá phạm vi.
- **File không được lưu:** Xác nhận đường dẫn `outputDir` tồn tại và ứng dụng có quyền ghi.

## Câu hỏi thường gặp

### Q1: Tôi có thể dùng Aspose.PSD cho Java để thao tác các file PSD hiện có không?

A1: Có, Aspose.PSD cho Java cung cấp chức năng phong phú để chỉnh sửa và thao tác các file PSD đã tồn tại.

### Q2: Tôi có thể tìm hỗ trợ cho Aspose.PSD cho Java ở đâu?

A2: Bạn có thể truy cập [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) để đặt câu hỏi liên quan đến hỗ trợ.

### Q3: Có bản dùng thử miễn phí cho Aspose.PSD cho Java không?

A3: Có, bạn có thể truy cập phiên bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

### Q4: Làm sao tôi mua giấy phép cho Aspose.PSD cho Java?

A4: Bạn có thể mua giấy phép từ [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy).

### Q5: Có giấy phép tạm thời cho Aspose.PSD cho Java không?

A5: Có, bạn có thể nhận giấy phép tạm thời từ [đây](https://purchase.aspose.com/temporary-license/).

## Các câu hỏi thường gặp bổ sung

**Q: Tôi có thể vẽ các hình dạng khác ngoài hình chữ nhật không?**  
A: Có, lớp `Graphics` cũng hỗ trợ vẽ ellipse, đường thẳng và các đường path tùy chỉnh.

**Q: Aspose.PSD có hỗ trợ độ trong suốt cho các hình dạng được vẽ không?**  
A: Hoàn toàn có; bạn có thể sử dụng `SolidBrush` với màu ARGB để bao gồm kênh alpha.

**Q: Có thể chỉnh sửa độ mờ của một lớp không?**  
A: Có, mỗi đối tượng `Layer` có phương thức `setOpacity` nhận giá trị từ 0 đến 255.

**Q: Làm sao tôi tải một file PSD hiện có thay vì tạo mới?**  
A: Sử dụng `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` trước khi thao tác các lớp.

## Kết luận

Bạn đã học cách **vẽ hình chữ nhật đỏ** và các hình dạng cơ bản khác trong file PSD bằng Aspose.PSD cho Java. Bằng cách tạo tài liệu, thêm lớp, xóa nền và vẽ bằng API `Graphics`, bạn có thể tự động hoá nhiều tác vụ thiết kế đồ họa. Hãy khám phá thêm bằng cách thử nghiệm các brush, hiệu ứng lớp và định dạng file khác nhau.

---

**Cập nhật lần cuối:** 2025-12-27  
**Đã kiểm tra với:** Aspose.PSD for Java 24.12 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}