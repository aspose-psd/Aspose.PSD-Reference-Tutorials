---
date: 2026-03-15
description: Tìm hiểu cách tạo tệp PSD, tạo bảng màu PSD và thiết lập chế độ màu PSD
  bằng Aspose.PSD cho Java trong hướng dẫn từng bước này.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Cách tạo tệp PSD bằng Aspose.PSD cho Java
url: /vi/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Tạo Tệp PSD Sử Dụng Aspose.PSD cho Java

## Giới thiệu
Nếu bạn đã bao giờ tự hỏi **how to create PSD** một cách lập trình, thì bạn đang ở đúng chỗ. Aspose.PSD cho Java cung cấp cho bạn toàn quyền kiểm soát các tài liệu Photoshop, cho phép bạn tạo, chỉnh sửa và lưu tệp PSD mà không cần mở Photoshop. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn cách tạo một tệp **indexed PSD**, thiết lập chế độ màu PSD và tạo một bảng màu tùy chỉnh — tất cả đều bằng mã Java rõ ràng, từng bước. Dù bạn đang xây dựng một pipeline đồ họa, tự động tạo tài sản, hay chỉ thử nghiệm, các khái niệm ở đây sẽ giúp bạn hiện thực hóa ý tưởng hình ảnh của mình.

## Câu trả lời nhanh
- **Thư viện tôi cần là gì?** Aspose.PSD for Java
- **Tôi có thể tạo một indexed PSD không?** Yes, by setting the color mode to `Indexed`
- **Có cần cài Photoshop không?** No, Aspose.PSD works independently
- **Phiên bản Java nào được yêu cầu?** JDK 8 or later
- **Kích thước tối đa của canvas là bao nhiêu?** Any size; this example uses 500 × 500 px

## Tệp PSD Indexed là gì?
Một PSD Indexed lưu trữ màu trong một bảng màu thay vì giá trị màu đầy đủ cho mỗi pixel. Điều này giảm kích thước tệp và lý tưởng cho đồ họa với số màu hạn chế, chẳng hạn như biểu tượng hoặc tài sản UI. Bằng cách tạo một bảng màu tùy chỉnh, bạn kiểm soát chính xác các màu sẽ xuất hiện trong hình ảnh cuối cùng.

## Tại sao phải tạo bảng màu PSD?
- Giữ kích thước tệp nhỏ cho việc sử dụng trên web hoặc di động  
- Đảm bảo thương hiệu nhất quán bằng cách giới hạn màu sắc trong bảng màu công ty của bạn  
- Tăng tốc độ render trong các ứng dụng hỗ trợ hình ảnh indexed  

## Yêu cầu trước
Trước khi chúng ta bắt đầu với mã, hãy chắc chắn bạn có những thứ sau:

1. **Kiến thức cơ bản về Java** – bạn nên quen thuộc với các lớp, phương thức và việc tạo đối tượng.  
2. **Java Development Kit (JDK) 8+** – đã được cài đặt và cấu hình trong IDE của bạn.  
3. **IDE (IntelliJ IDEA, Eclipse, v.v.)** – không bắt buộc nhưng rất được khuyến nghị để dễ dàng gỡ lỗi.  
4. **Thư viện Aspose.PSD cho Java** – tải xuống **[here](https://releases.aspose.com/psd/java/)** và thêm JAR vào classpath của dự án.  
5. **Các khái niệm cơ bản về thiết kế đồ họa** – hiểu biết về chế độ màu, bảng màu và các hình dạng cơ bản sẽ giúp bạn theo dõi.  

## Nhập các Gói
Trước khi tiếp tục với mã, hãy chắc chắn rằng chúng ta đã nhập tất cả các gói cần thiết vào ứng dụng Java của bạn. Đây là những gì bạn sẽ cần:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

Các import này sẽ cho phép bạn làm việc với các tùy chọn PSD, màu sắc và thao tác đồ họa thông qua Aspose.PSD.

Bây giờ, chúng ta sẽ phân tích mã từng bước để **how to create PSD** các tệp với chế độ màu indexed.

## Bước 1: Thiết lập Thư mục Tài liệu của Bạn
Đầu tiên, xác định nơi sẽ lưu PSD đã tạo.

```java
String dataDir = "Your Document Directory";
```

Thay thế `"Your Document Directory"` bằng đường dẫn tuyệt đối hoặc tương đối, ví dụ, `"/Users/YourName/Documents/"`.

## Bước 2: Tạo một Instance của PsdOptions
`PsdOptions` chứa tất cả các cài đặt cho tệp bạn sắp tạo.

```java
PsdOptions createOptions = new PsdOptions();
```

## Bước 3: Đặt các Thuộc tính Cốt lõi của PsdOptions
Ở đây chúng ta chỉ định vị trí xuất, **set psd color mode** thành `Indexed`, và phiên bản PSD.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – đường dẫn đầy đủ của tệp mới.  
- **Color Mode** – `Indexed` cho Aspose.PSD biết sử dụng hình ảnh dựa trên bảng màu.  
- **Version** – phiên bản định dạng PSD (5 hoạt động cho hầu hết các phiên bản Photoshop hiện đại).

## Bước 4: Tạo một Bảng màu (Generate PSD Color Palette)
Xác định các màu sẽ có trong hình ảnh indexed.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- Mảng `palette` chứa tối đa 256 đối tượng `Color`.  
- `CompressionMethod.RLE` cung cấp nén không mất dữ liệu hiệu quả cho các hình ảnh indexed.

## Bước 5: Tạo Canvas Hình ảnh PSD
Bây giờ chúng ta tạo một PSD trống với kích thước mong muốn.

```java
Image psd = Image.create(createOptions, 500, 500);
```

Điều này tạo ra một canvas 500 × 500 pixel sử dụng bảng màu đã định nghĩa ở trên.

## Bước 6: Vẽ Đồ họa trên PSD
Thêm nội dung hình ảnh—ở đây chúng ta vẽ một hình ellipse đỏ đơn giản trên nền trắng.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` lấp đầy nền bằng màu trắng.  
- `drawEllipse` vẽ một ellipse đỏ với đường viền 6 pixel.

## Bước 7: Lưu Tệp PSD
Cuối cùng, lưu hình ảnh vào đĩa.

```java
psd.save();
```

Tệp `Newsample_out.psd` sẽ xuất hiện trong thư mục bạn đã chỉ định ở trên.

## Các Vấn đề Thường gặp & Mẹo
- **Palette Size** – Nếu bạn cần hơn 4 màu, chỉ cần thêm chúng vào mảng `palette` (tối đa 256).  
- **File Permissions** – Đảm bảo quá trình Java có quyền ghi vào `dataDir`.  
- **Incorrect Color Mode** – Quên `createOptions.setColorMode(ColorModes.Indexed)` sẽ tạo ra một PSD RGB thay vì một PSD indexed.  

## Câu hỏi Thường gặp

**Q: Aspose.PSD cho Java là gì?**  
A: Aspose.PSD cho Java là một thư viện cho phép thao tác các tệp PSD (Photoshop) một cách lập trình bằng Java.

**Q: Tôi có thể sử dụng Aspose.PSD miễn phí không?**  
A: Có, bạn có thể truy cập phiên bản dùng thử miễn phí của Aspose.PSD **[here](https://releases.aspose.com/)**.

**Q: Tôi có cần cài Photoshop để làm việc với Aspose.PSD không?**  
A: Không, bạn có thể tạo và thao tác các tệp PSD mà không cần Photoshop, vì Aspose.PSD xử lý mọi thao tác một cách độc lập.

**Q: Làm thế nào để tôi lấy giấy phép tạm thời cho Aspose.PSD?**  
A: Bạn có thể yêu cầu giấy phép tạm thời **[here](https://purchase.aspose.com/temporary-license/)**.

**Q: Tôi có thể nhận hỗ trợ cho Aspose.PSD ở đâu?**  
A: Bạn có thể nhận hỗ trợ từ diễn đàn Aspose **[here](https://forum.aspose.com/c/psd/34)**.

## Kết luận
Bạn vừa học được cách **how to create PSD** các tệp với chế độ màu indexed, tạo một bảng màu tùy chỉnh và thêm các đồ họa đơn giản — tất cả đều sử dụng Aspose.PSD cho Java. Với những khối xây dựng này, bạn có thể mở rộng thành các bản vẽ phức tạp hơn, quản lý lớp và xử lý hàng loạt. Để khám phá sâu hơn, hãy xem tài liệu API chính thức **[here](https://reference.aspose.com/psd/java/)** và tiếp tục thử nghiệm với các bảng màu và các primitive vẽ khác nhau.

---

**Cập nhật lần cuối:** 2026-03-15  
**Được kiểm tra với:** Aspose.PSD for Java 24.12 (latest)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}