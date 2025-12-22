---
date: 2025-12-18
description: Tìm hiểu cách tạo mặt nạ vector (tài nguyên Vmsk) trong các tệp PSD bằng
  Aspose.PSD cho Java. Hướng dẫn từng bước này cho bạn biết cách thêm mặt nạ vector,
  chuyển đổi PSD sang PNG và nhiều hơn nữa.
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: Tạo Mặt nạ Vector (Tài nguyên Vmsk) trong các tệp PSD bằng Java
url: /vi/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo Vector Mask (Tài nguyên Vmsk) trong tệp PSD bằng Java

## Giới thiệu
Nếu bạn cần **tạo vector mask** (Vmsk) trong các tệp Photoshop (PSD), Aspose.PSD for Java cung cấp cho bạn một cách tiếp cận sạch sẽ và lập trình để thực hiện. Dù bạn đang xây dựng một công cụ tự động hoá thiết kế hay thêm hỗ trợ mask tùy chỉnh vào quy trình đồ họa hiện có, hướng dẫn này sẽ dẫn bạn qua từng bước—tải PSD, đọc tài nguyên Vmsk, chỉnh sửa các thuộc tính của nó, và lưu kết quả. Khi hoàn thành, bạn sẽ tự tin xử lý vector mask, chuyển đổi PSD sang PNG, và mở rộng tệp với dữ liệu vector bổ sung.

## Câu trả lời nhanh
- **Vmsk resource là gì?** Đó là dữ liệu vector mask được lưu trong tệp PSD, định nghĩa các hình dạng vector phức tạp cho một lớp.  
- **Thư viện nào hỗ trợ?** Aspose.PSD for Java cung cấp quyền đọc/ghi đầy đủ cho tài nguyên Vmsk.  
- **Có cần giấy phép không?** Có bản dùng thử miễn phí; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Có thể chuyển đổi PSD đã chỉnh sửa sang PNG không?** Có—sau khi lưu, bạn có thể tải lại PSD và xuất ra PNG bằng cùng API.  
- **Có hỗ trợ Maven không?** Chắc chắn; Aspose.PSD có thể được thêm dưới dạng phụ thuộc Maven (xem từ khóa “aspose psd maven”).

## Vmsk Resource là gì?
Vmsk (Vector Mask) là một mask không dựa trên pixel, sử dụng các đường cong Bézier và bản ghi đường dẫn để xác định các vùng trong suốt và không trong suốt trên một lớp. Vì nó dựa trên vector, nó có thể phóng to mà không mất chất lượng—lý tưởng cho đồ họa độ phân giải cao.

## Tại sao tạo Vector Mask với Aspose.PSD?
- **Tự động hoá:** Thêm hoặc sửa đổi mask một cách lập trình mà không cần mở Photoshop.  
- **Nhất quán:** Đảm bảo mọi PSD bạn tạo ra đều tuân theo cùng một quy tắc mask.  
- **Đa nền tảng:** Hoạt động trên bất kỳ hệ điều hành nào hỗ trợ Java.  
- **Tích hợp:** Kết hợp với các API Aspose khác (ví dụ, chuyển PSD → PNG) để xây dựng quy trình làm việc đầu‑tới‑đầu.

## Yêu cầu trước
Trước khi chúng ta bắt đầu với mã, hãy chắc chắn bạn đã chuẩn bị các thứ sau:

### Những gì bạn cần
- **Java Development Kit (JDK):** Đảm bảo máy của bạn đã cài đặt JDK. Nếu chưa, bạn có thể tải về từ [trang web Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
- **Thư viện Aspose.PSD for Java:** Đây là thư viện mạnh mẽ để quản lý tệp PSD. Bạn có thể tải về từ [trang phát hành Aspose](https://releases.aspose.com/psd/java/). Đối với những ai muốn thử trước khi mua, cũng có thể bắt đầu với [bản dùng thử miễn phí](https://releases.aspose.com/).
- **IDE:** Bất kỳ IDE nào cho Java (như IntelliJ IDEA, Eclipse, …) đều phù hợp cho dự án này.

### Cài đặt môi trường làm việc
1. **Tạo một dự án Java mới** – Mở IDE ưa thích và khởi tạo một dự án trống.  
2. **Thêm thư viện Aspose** – Sau khi tải về file JAR của Aspose, thêm nó vào đường dẫn biên dịch của dự án để bạn có thể truy cập các lớp liên quan tới PSD.

Với môi trường đã sẵn sàng, chúng ta sẽ chuyển sang phần thực thi.

## Cách tạo vector mask trong tệp PSD bằng Java
Dưới đây là hướng dẫn chi tiết từng bước. Các khối mã được giữ nguyên như trong tutorial gốc; chúng tôi chỉ thêm phần giải thích để mỗi bước trở nên rõ ràng hơn.

## Nhập khẩu các gói
Trước khi làm việc với tệp PSD, chúng ta cần nhập các lớp cần thiết từ thư viện Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

Sau khi đã chuẩn bị xong, hãy đi qua từng thao tác.

## Bước 1: Tải tệp PSD của bạn
Điều đầu tiên cần làm là tải tệp PSD. Đây là nơi mọi thứ bắt đầu.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Chúng ta đặt `dataDir` tới thư mục chứa tệp PSD.  
- Tạo chuỗi `sourceFileName` bằng cách kết hợp thư mục với tên tệp PSD.  
- Cuối cùng, tải tệp PSD vào đối tượng `PsdImage` bằng `Image.load()`.

## Bước 2: Lấy tài nguyên Vmsk
Sau khi đã tải ảnh PSD, chúng ta sẽ truy xuất tài nguyên Vmsk.

```java
VmskResource resource = getVmskResource(im);
```

- Gọi phương thức `getVmskResource()` để tìm và lấy tài nguyên Vmsk từ ảnh.

## Bước 3: Xác thực các thuộc tính của tài nguyên Vmsk
Trước khi thực hiện sửa đổi, cần xác thực rằng tài nguyên Vmsk ở trạng thái mong đợi.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Ở đây chúng ta kiểm tra các thuộc tính khác nhau của tài nguyên Vmsk, đảm bảo nó không bị tắt, không bị đảo ngược, không bị tách rời và có số lượng đường dẫn đúng.

## Bước 4: Truy cập từng đường dẫn và xác thực
Hãy đi sâu hơn và kiểm tra các đường dẫn bên trong tài nguyên Vmsk.

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- Chúng ta trích xuất ba bản ghi đường dẫn cụ thể và xác thực kiểu cũng như các thuộc tính của chúng để chắc chắn đáp ứng tiêu chí.

## Bước 5: Chỉnh sửa tài nguyên Vmsk
Bây giờ chúng ta bắt đầu phần sửa đổi! Bạn có thể tùy chỉnh các thuộc tính của tài nguyên Vmsk theo nhu cầu.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- Trong khối này, chúng ta bật/tắt các thuộc tính khác nhau của tài nguyên Vmsk. Bằng cách đặt chúng thành `true`, chúng ta kiểm soát cách mask hoạt động trong tệp PSD.

## Bước 6: Thay đổi các điểm nút Bézier
Các nút Bézier là yếu tố quan trọng của các đường vector. Hãy thay đổi một số giá trị ở đây.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Chúng ta truy cập các đường `BezierKnotRecord` cụ thể và thay đổi các điểm của chúng để có thể thay đổi hình dạng của vector mask.

## Bước 7: Lưu tệp PSD đã chỉnh sửa
Khi mọi chỉnh sửa đã hoàn tất, chúng ta sẽ lưu tệp PSD đã thay đổi.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Đặt đường dẫn cho tệp PSD xuất ra và gọi `im.save()` để ghi các thay đổi vào tệp mới này.

## Bước 8: Dọn dẹp tài nguyên
Cuối cùng, chúng ta cần giải phóng tài nguyên ảnh để tránh rò rỉ bộ nhớ.

```java
im.dispose();
```

- Luôn luôn giải phóng bất kỳ tài nguyên nào sau khi sử dụng. Điều này giúp ngăn ngừa rò rỉ bộ nhớ trong ứng dụng của bạn.

## Kết luận
Chúc mừng! Bạn vừa hoàn thành quy trình chi tiết **tạo vector mask** (Vmsk) trong tệp PSD bằng Aspose.PSD for Java. Từ việc tải ảnh, lấy và xác thực tài nguyên Vmsk, chỉnh sửa các thuộc tính, đến lưu PSD đã thay đổi, bạn đã có nền tảng vững chắc để tự động hoá quy trình vector mask. Hãy áp dụng các kỹ thuật này để nâng cao quy trình thiết kế, tích hợp với các API Aspose khác (như chuyển PSD sang PNG), hoặc xây dựng công cụ đồ họa tùy chỉnh.

## Câu hỏi thường gặp
**Q: Làm thế nào để thêm một vector mask mới vào một lớp hiện có?**  
A: Tạo một `VmskResource`, điền các bản ghi đường dẫn cần thiết (ví dụ, `BezierKnotRecord`), và gắn nó vào bộ sưu tập tài nguyên của lớp.

**Q: Tôi có thể chuyển đổi PSD đã chỉnh sửa trực tiếp sang PNG mà không mở Photoshop không?**  
A: Có—sau khi lưu PSD, tải lại bằng `Image.load()` và gọi `im.save("output.png")` với định dạng PNG.

**Q: Có cách nào tự động hoá quy trình này trong pipeline CI/CD không?**  
A: Chắc chắn. Vì quy trình hoàn toàn bằng Java, bạn có thể nhúng nó vào các build Maven/Gradle, container Docker, hoặc bất kỳ hệ thống CI nào hỗ trợ Java.

**Q: Các phiên bản Aspose.PSD nào tương thích với Java 11+?**  
A: Tất cả các bản phát hành gần đây (2024‑2025) hỗ trợ Java 8 trở lên, bao gồm Java 11, 17 và các phiên bản LTS mới hơn.

**Q: Tôi có cần giấy phép cho các bản build phát triển không?**  
A: Giấy phép đánh giá miễn phí đủ cho phát triển và thử nghiệm. Đối với triển khai sản xuất, cần mua giấy phép thương mại.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
