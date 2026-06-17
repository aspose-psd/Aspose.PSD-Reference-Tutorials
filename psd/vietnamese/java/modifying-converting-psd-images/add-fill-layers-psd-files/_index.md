---
date: 2026-03-04
description: Tìm hiểu cách chỉnh sửa các lớp PSD một cách lập trình bằng cách thêm
  các lớp tô màu với Aspose.PSD cho Java. Hãy làm theo hướng dẫn từng bước này để
  nhanh chóng nâng cao thiết kế của bạn.
linktitle: Modify PSD Layers Programmatically – Add Fill Layers (Java)
second_title: Aspose.PSD Java API
title: Thay đổi các lớp PSD bằng lập trình – Thêm lớp tô màu (Java)
url: /vi/java/modifying-converting-psd-images/add-fill-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Sửa đổi các lớp PSD một cách lập trình – Thêm lớp Đổ màu (Java)

Nếu bạn đang muốn **sửa đổi các lớp PSD một cách lập trình**, việc thêm các lớp đổ màu là một trong những cách nhanh nhất để làm phong phú tài liệu Photoshop mà không cần mở Photoshop. Trong hướng dẫn này, chúng tôi sẽ đi qua các bước chính xác để tạo một PSD mới, chèn các lớp đổ màu, gradient và pattern, và sau đó lưu kết quả — tất cả đều sử dụng Aspose.PSD cho Java.

## Câu trả lời nhanh
- **Tôi có thể đạt được gì?** Thêm các lớp đổ màu, gradient và pattern vào tệp PSD một cách lập trình.  
- **Thư viện nào cần thiết?** Aspose.PSD cho Java (phiên bản mới nhất).  
- **Có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; giấy phép thương mại cần cho môi trường sản xuất.  
- **Thời gian triển khai khoảng bao lâu?** Khoảng 10‑15 phút cho một ví dụ cơ bản.  
- **Phiên bản Java nào được hỗ trợ?** JDK 11 hoặc mới hơn.

## “Sửa đổi các lớp PSD một cách lập trình” là gì?
Sửa đổi các lớp PSD một cách lập trình có nghĩa là sử dụng mã để tạo, chỉnh sửa hoặc xóa các lớp bên trong tài liệu Photoshop, cho phép bạn kiểm soát toàn bộ quy trình thiết kế mà không cần tương tác giao diện người dùng thủ công.

## Tại sao nên thêm lớp đổ màu với Aspose.PSD?
- **Tự động hoá** – Tạo hàng chục PSD trong một công việc batch.  
- **Nhất quán** – Áp dụng cùng một màu, gradient hoặc pattern cho nhiều tệp.  
- **Tốc độ** – Bỏ qua các bước thủ công tốn thời gian trong Photoshop.  
- **Đa nền tảng** – Hoạt động trên bất kỳ hệ điều hành nào hỗ trợ Java.

## Yêu cầu trước
Trước khi chúng ta bắt đầu với mã, hãy chắc chắn rằng bạn đã có:

1. **Java Development Kit (JDK)** – Cài đặt JDK 11 hoặc mới hơn. Bạn có thể tải về từ [trang web Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD cho Java** – Tải thư viện mới nhất từ trang tải chính thức [tại đây](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, hoặc bất kỳ trình soạn thảo nào bạn thích.  
4. **Kiến thức cơ bản về Java** – Hiểu biết về lớp và phương thức sẽ hữu ích, nhưng hướng dẫn sẽ giải thích từng bước.

## Nhập khẩu các gói
Để bắt đầu làm việc với tệp PSD, bạn cần nhập các lớp Aspose.PSD liên quan:

```java
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
```

Các import này cho phép bạn truy cập vào đối tượng `PsdImage` (tài liệu) và các loại `FillLayer` mà chúng ta sẽ sử dụng.

## Cách sửa đổi các lớp PSD một cách lập trình – Hướng dẫn từng bước

### Bước 1: Thiết lập thư mục đầu ra
Xác định nơi sẽ lưu PSD kết quả để bạn có thể tìm lại sau.

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
```

Thay thế `"Your Document Directory"` bằng đường dẫn tuyệt đối hoặc tương đối trên máy của bạn.

### Bước 2: Tạo một tài liệu Photoshop mới
Khởi tạo một canvas trống sẽ chứa các lớp đổ màu.

```java
PsdImage psdImage = new PsdImage(100, 100);
```

Các tham số `100, 100` đại diện cho chiều rộng và chiều cao tính bằng pixel. Điều chỉnh chúng cho phù hợp với yêu cầu thiết kế của bạn.

### Bước 3: Thêm lớp Đổ màu Đơn sắc
Tạo một lớp đổ màu đơn sắc và đặt cho nó một tên dễ nhận biết.

```java
FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);
colorFillLayer.setDisplayName("Color Fill Layer");
psdImage.addLayer(colorFillLayer);
```

Bạn có thể thay đổi màu thực tế sau này bằng cách truy cập vào cài đặt đổ màu của lớp (không được hiển thị ở đây để ngắn gọn).

### Bước 4: Thêm lớp Đổ Gradient
Các lớp đổ gradient giúp tạo độ sâu và sự thu hút trực quan.

```java
FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);
gradientFillLayer.setDisplayName("Gradient Fill Layer");
psdImage.addLayer(gradientFillLayer);
```

Tự do thử nghiệm các gradient tuyến tính hoặc radial thông qua cài đặt của lớp.

### Bước 5: Thêm lớp Đổ Pattern
Các lớp đổ pattern cho phép bạn lặp lại hình ảnh hoặc texture trên một lớp.

```java
FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);
patternFillLayer.setDisplayName("Pattern Fill Layer");
patternFillLayer.setOpacity((byte)50);
psdImage.addLayer(patternFillLayer);
```

Đặt độ trong suốt thành 50 % giúp pattern hòa quyện tốt với các lớp bên dưới.

### Bước 6: Lưu tệp PSD của bạn
Ghi lại các thay đổi vào đĩa.

```java
psdImage.save(outPsdFilePath);
```

Mở tệp đã lưu trong Photoshop hoặc bất kỳ trình xem PSD nào để xem ba lớp đổ màu mới.

### Bước 7: Dọn dẹp tài nguyên
Luôn luôn giải phóng đối tượng `PsdImage` để giải bộ nhớ gốc.

```java
psdImage.dispose();
```

## Các vấn đề thường gặp & Mẹo
- **Đường dẫn đầu ra không hợp lệ** – Đảm bảo thư mục tồn tại và bạn có quyền ghi.  
- **Tiêu thụ bộ nhớ** – Đối với canvas rất lớn, gọi `psdImage.dispose()` ngay khi bạn hoàn thành công việc với ảnh.  
- **Thứ tự lớp** – Các lớp được thêm vào đỉnh stack theo mặc định; sử dụng `psdImage.insertLayer(layer, index)` nếu bạn cần một thứ tự cụ thể.

## Câu hỏi thường gặp

**H: Tôi có thể thêm những loại lớp đổ màu nào bằng Aspose.PSD cho Java?**  
Đ: Bạn có thể thêm lớp đổ màu đơn sắc, gradient và pattern.

**H: Aspose.PSD có hỗ trợ các định dạng ảnh khác không?**  
Đ: Có, nó hoạt động với BMP, JPEG, PNG và nhiều định dạng khác.

**H: Tôi có thể sử dụng Aspose.PSD miễn phí không?**  
Đ: Bạn có thể khám phá bản dùng thử miễn phí của Aspose.PSD cho Java [tại đây](https://releases.aspose.com/).

**H: Tôi có thể tìm tài liệu chi tiết về Aspose.PSD ở đâu?**  
Đ: Bạn có thể truy cập tài liệu đầy đủ [tại đây](https://reference.aspose.com/psd/java/).

**H: Có cộng đồng hỗ trợ cho Aspose.PSD không?**  
Đ: Có, bạn có thể nhận trợ giúp từ cộng đồng trên diễn đàn Aspose [tại đây](https://forum.aspose.com/c/psd/34).

## Kết luận
Bạn đã học cách **sửa đổi các lớp PSD một cách lập trình** bằng cách thêm các lớp đổ màu khác nhau sử dụng Aspose.PSD cho Java. Cách tiếp cận này giúp tiết kiệm thời gian, đảm bảo tính nhất quán trong các dự án và mở ra các kịch bản xử lý batch mạnh mẽ. Hãy thử nghiệm với các màu, gradient và pattern khác nhau để xem bạn có thể đẩy mạnh việc tạo thiết kế tự động đến mức nào.

---

**Cập nhật lần cuối:** 2026-03-04  
**Đã kiểm tra với:** Aspose.PSD cho Java (phiên bản mới nhất)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}