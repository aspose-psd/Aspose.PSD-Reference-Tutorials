---
date: 2026-01-17
description: Tìm hiểu cách vẽ cung trong đồ họa Java bằng Aspose.PSD cho Java. Hướng
  dẫn từng bước kèm ví dụ mã cho các ứng dụng đồ họa.
linktitle: Java Graphics Draw Arc with Aspose.PSD
second_title: Aspose.PSD Java API
title: Java Graphics Vẽ Cung với Aspose.PSD – Hướng Dẫn Từng Bước
url: /vi/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Graphics Draw Arc với Aspose.PSD

## Giới thiệu
Trong hướng dẫn này, bạn sẽ khám phá cách **java graphics draw arc** bằng thư viện Aspose.PSD for Java. Vẽ cung bằng mã lập trình rất hữu ích cho các thành phần UI tùy chỉnh, trực quan hoá dữ liệu, hoặc bất kỳ đồ họa nào cần kiểm soát độ cong chính xác. Chúng tôi sẽ hướng dẫn từng bước — từ thiết lập dự án đến render cung và lưu kết quả — để bạn có thể thêm tính năng này vào các ứng dụng Java của mình ngay lập tức.

## Câu trả lời nhanh
- **Thư viện nào cho phép Java vẽ cung một cách dễ dàng?** Aspose.PSD for Java.  
- **Tôi có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; cần giấy phép cho môi trường sản xuất.  
- **Các định dạng đầu ra nào được hỗ trợ?** BMP, PNG, JPEG, TIFF, GIF, và nhiều hơn nữa.  
- **Tôi có thể thay đổi độ dày hoặc màu của cung không?** Có — điều chỉnh các thuộc tính của đối tượng `Pen`.  
- **Mã có tương thích với Java 8+ không?** Chắc chắn, API được thiết kế cho Java 8 và các phiên bản mới hơn.

## “java graphics draw arc” là gì?
Cụm từ này đề cập đến việc sử dụng mã Java để vẽ một đoạn cong (cung) lên một canvas đồ họa. Với Aspose.PSD, bạn sẽ có lớp `Graphics` cấp cao giúp đơn giản hoá các thao tác vẽ, quản lý màu sắc, khử răng cưa và xuất file một cách tự động.

## Tại sao nên dùng Aspose.PSD để vẽ cung?
- **Hỗ trợ PSD đầy đủ** – Tạo hoặc chỉnh sửa file Photoshop mà không cần cài Photoshop.  
- **API vẽ phong phú** – Các phương thức như `drawArc` cho phép bạn chỉ định kích thước, góc và kiểu dáng trong một lời gọi duy nhất.  
- **Xuất đa định dạng** – Lưu cung của bạn thành BMP, PNG, JPEG, v.v., chỉ với vài dòng mã.  
- **Tối ưu hiệu năng** – Thiết kế cho hình ảnh lớn và xử lý batch.

## Yêu cầu trước
1. **Môi trường phát triển Java** – Cài đặt Java (JDK 8 trở lên). Tải về từ [trang web của Oracle](https://www.oracle.com/java/).  
2. **Aspose.PSD for Java** – Nhận thư viện từ [trang tải xuống](https://releases.aspose.com/psd/java/) và thêm JAR vào classpath của dự án.

## Nhập khẩu các gói
Đầu tiên, đưa các lớp Aspose.PSD cần thiết vào phạm vi sử dụng:

```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

Các import này cung cấp quyền truy cập vào định nghĩa màu, công cụ vẽ, container ảnh và các tùy chọn lưu file.

## Hướng dẫn từng bước

### Bước 1: Thiết lập dự án Java của bạn
Tạo một dự án Maven hoặc Gradle mới, thêm JAR Aspose.PSD và xác nhận IDE không báo lỗi import.

### Bước 2: Khởi tạo đối tượng Image và Graphics
Tạo một canvas `PsdImage` trống và một thể hiện `Graphics` để vẽ:

```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```

Thay thế `"Your Document Directory"` bằng thư mục nơi bạn muốn lưu file kết quả.

### Bước 3: Định nghĩa tham số cho cung
Xác định kích thước và góc tạo nên cung:

```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```

Bạn có thể điều chỉnh các số này để phù hợp với phong cách hình ảnh mong muốn.

### Bước 4: Vẽ và lưu cung
Sử dụng phương thức `drawArc`, sau đó xuất ảnh:

```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

Mã sẽ vẽ một cung màu đen trên nền vàng và ghi kết quả vào `Arc.bmp`. Thay đổi `outputPath` và `BmpOptions` nếu muốn xuất sang định dạng hoặc chất lượng khác.

## Các vấn đề thường gặp & Giải pháp
- **Lỗi file không tồn tại** – Đảm bảo `dataDir` kết thúc bằng dấu phân cách đường dẫn (`/` hoặc `\\`) và thư mục đã tồn tại.  
- **Cung chỉ hiển thị dưới dạng đường thẳng** – Kiểm tra `width` và `height` có lớn hơn 0 và `sweepAngle` không phải là bội số của 360° (trường hợp này sẽ vẽ một hình ellipse đầy đủ).  
- **Màu không áp dụng** – Sử dụng `new Pen(Color.getRed())` hoặc đặt `pen.setWidth(2)` để thấy hiệu ứng rõ ràng hơn.

## Câu hỏi thường gặp

**Q: Aspose.PSD for Java có thể xử lý các hình dạng khác ngoài cung không?**  
A: Có, nó hỗ trợ hình chữ nhật, ellipse, đường thẳng và các đường path tùy chỉnh qua cùng API `Graphics`.

**Q: Làm sao để thay đổi độ dày hoặc màu của cung?**  
A: Tạo một `Pen` với `Color` và `Width` mong muốn (ví dụ: `new Pen(Color.getBlue(), 3)`) và truyền vào `drawArc`.

**Q: Có thể xuất cung sang các định dạng khác ngoài BMP không?**  
A: Chắc chắn. Sử dụng `PngOptions`, `JpegOptions`, `TiffOptions`, v.v., thay cho `BmpOptions`.

**Q: Tôi có thể tìm thêm ví dụ và hỗ trợ ở đâu?**  
A: Tham khảo [diễn đàn Aspose.PSD](https://forum.aspose.com/c/psd/34) để nhận trợ giúp cộng đồng, tài liệu chính thức và các mẫu mã.

## Kết luận
Bạn đã có một ví dụ hoàn chỉnh, sẵn sàng cho môi trường sản xuất về cách **java graphics draw arc** bằng Aspose.PSD for Java. Bằng cách điều chỉnh các tham số, cài đặt pen và tùy chọn xuất, bạn có thể tích hợp các cung tùy chỉnh vào bất kỳ quy trình đồ họa Java nào.

---

**Cập nhật lần cuối:** 2026-01-17  
**Đã kiểm tra với:** Aspose.PSD for Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}