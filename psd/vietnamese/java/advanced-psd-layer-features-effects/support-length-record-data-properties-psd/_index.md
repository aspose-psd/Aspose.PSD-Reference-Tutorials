---
date: 2026-02-20
description: Tìm hiểu cách hỗ trợ các thuộc tính bản ghi độ dài và xử lý hàng loạt
  các tệp PSD bằng Aspose.PSD cho Java. Hướng dẫn từng bước kèm ví dụ mã.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Hỗ trợ các thuộc tính bản ghi độ dài – Chỉnh sửa các hình dạng vector PSD (Java)
url: /vi/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

 produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hỗ trợ Thuộc tính Bản ghi Độ dài – Chỉnh sửa Hình vector PSD (Java)

## Giới thiệu
Nếu bạn cần **modify PSD vector shapes** một cách lập trình, thư viện Aspose.PSD for Java cung cấp cho bạn toàn quyền kiểm soát các tệp Photoshop ngay từ mã Java của mình. Trong hướng dẫn này, chúng tôi sẽ đi qua mọi thứ bạn cần biết để **support length record properties**—một bước quan trọng khi bạn muốn chỉnh sửa các lớp hình vector. Khi kết thúc, bạn sẽ có thể mở một tệp PSD, điều chỉnh các thuộc tính hình vector của nó, và lưu tệp đã cập nhật mà không cần rời IDE. Hãy bắt đầu!

## Câu trả lời nhanh
- **What does “modify PSD vector shapes” mean?** Điều chỉnh hình học, các thao tác đường dẫn, hoặc các thuộc tính khác của các lớp dựa trên vector bên trong tệp PSD.  
- **Which library handles this?** Aspose.PSD for Java.  
- **Do I need a license?** Bản dùng thử miễn phí đủ cho việc đánh giá; cần giấy phép thương mại cho môi trường sản xuất.  
- **How long does the implementation take?** Khoảng 10‑15 phút cho một script chỉnh sửa hình cơ bản.  
- **What are the main prerequisites?** Java JDK, Aspose.PSD for Java, và một tệp PSD mẫu.

## “support length record properties” là gì?
Hỗ trợ length record properties có nghĩa là truy cập và cập nhật các đối tượng `LengthRecord` mô tả mỗi đường vector bên trong một PSD. Thay đổi các bản ghi này cho phép bạn kiểm soát cách các hình dạng kết hợp, giao nhau, hoặc trừ nhau.

## Tại sao nên sử dụng Aspose.PSD for Java để support length record properties?
- **No Photoshop required** – làm việc trực tiếp với các tệp PSD trên bất kỳ máy chủ nào.  
- **Rich API** – truy cập các lớp, tài nguyên và dữ liệu vector với các lớp được định kiểu chặt chẽ.  
- **Cross‑platform** – chạy trên Windows, Linux, hoặc macOS với bất kỳ JDK nào.  
- **Performance‑focused** – xử lý bộ nhớ hiệu quả và thao tác lưu nhanh.  

## Yêu cầu trước
1. **Java Development Kit (JDK)** – tải xuống từ [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) hoặc sử dụng trình quản lý gói ưa thích của bạn.  
2. **Aspose.PSD for Java** – lấy JAR mới nhất từ [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, hoặc bất kỳ trình chỉnh sửa nào tương thích với Java.  
4. **A PSD file** – tạo một tệp trong Photoshop hoặc lấy một PSD mẫu để thử nghiệm.  
5. **Basic Java knowledge** – quen thuộc với các lớp, đối tượng và xử lý ngoại lệ.

## Nhập các gói
Đầu tiên, nhập các lớp bạn sẽ cần để làm việc với tệp PSD và tài nguyên hình vector.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Bước 1: Thiết lập Thư mục Nguồn và Đầu ra
Xác định vị trí tệp PSD gốc và nơi bạn muốn lưu tệp đã chỉnh sửa.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Bước 2: Tải tệp PSD
Sử dụng `Image.load` để mở tệp và ép kiểu thành `PsdImage` để truy cập các tính năng đặc thù của PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Bước 3: Tìm tài nguyên Vsms trong Lớp
Dữ liệu hình vector nằm trong một `VsmsResource`. Duyệt qua các tài nguyên của lớp thứ hai để tìm nó.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Bước 4: Truy cập Length Records
Mỗi `LengthRecord` đại diện cho một đường vector riêng biệt. Lấy những bản ghi bạn dự định chỉnh sửa.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Bước 5: Chỉnh sửa Thuộc tính Thao tác Đường dẫn
Bây giờ bạn có thể **modify PSD vector shapes** bằng cách thay đổi `PathOperations` của chúng. Điều này xác định cách các hình dạng tương tác (ví dụ: loại trừ, giao nhau, trừ).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Bước 6: Lưu tệp PSD đã chỉnh sửa
Lưu các thay đổi của bạn vào một tệp mới.

```java
psdImage.save(outPsdFilePath);
```

## Bước 7: Dọn dẹp Tài nguyên
Giải phóng `PsdImage` để giải phóng bộ nhớ.

```java
psdImage.dispose();
```

## Cách xử lý hàng loạt các tệp PSD với support length record properties
Nếu bạn cần áp dụng cùng một điều chỉnh hình vector cho nhiều PSD, hãy bao quanh đoạn mã trên trong một vòng lặp duyệt qua một thư mục các tệp. Cập nhật `inPsdFilePath` và `outPsdFilePath` cho mỗi vòng lặp, và bạn sẽ có thể **batch process PSD files** một cách hiệu quả.

## Những Cạm Bẫy Thường Gặp & Mẹo
- **Null checks** – luôn kiểm tra `resource` không phải `null` trước khi truy cập các đường dẫn.  
- **Path index bounds** – đảm bảo các chỉ số bạn dùng (`[2]`, `[7]`, `[11]`) tồn tại trong PSD cụ thể bạn đang chỉnh sửa.  
- **License** – chạy mà không có giấy phép hợp lệ sẽ chèn watermark vào PSD đã lưu.  

## Kết luận
Bây giờ bạn đã có một ví dụ hoàn chỉnh, từ đầu đến cuối về cách **modify PSD vector shapes** bằng cách support length record properties với Aspose.PSD for Java. Dù bạn đang tự động hoá quy trình tài sản hay xây dựng công cụ thiết kế tùy chỉnh, các API này cung cấp cho bạn khả năng linh hoạt thao tác các lớp vector mà không cần công việc thủ công trong Photoshop. Hãy khám phá thêm bằng cách thử nghiệm các `PathOperations` khác hoặc kết hợp nhiều chỉnh sửa `LengthRecord` cho các hình dạng phức tạp.

## Câu hỏi Thường gặp

**Q: Làm thế nào để xử lý một PSD không chứa lớp hình vector?**  
A: `VsmsResource` sẽ không tồn tại, vì vậy `resource` sẽ vẫn là `null`. Thêm kiểm tra và bỏ qua bước chỉnh sửa hoặc thông báo cho người dùng.

**Q: Tôi có thể thay đổi các thuộc tính khác như màu nền hoặc độ rộng nét viền không?**  
A: Có, `LengthRecord` cung cấp các setter bổ sung cho fill, stroke và opacity. Tham khảo tài liệu API để biết chi tiết.

**Q: Có thể batch‑process nhiều tệp PSD không?**  
A: Chắc chắn. Bao quanh đoạn mã trong một vòng lặp duyệt qua thư mục các tệp PSD, điều chỉnh các đường dẫn đầu vào và đầu ra mỗi lần.

**Q: Tôi có cần đóng các stream thủ công khi tải từ đường dẫn tệp không?**  
A: Phương thức `Image.load` xử lý các stream tệp nội bộ, nhưng nếu bạn tải từ một `InputStream`, hãy nhớ đóng nó sau khi sử dụng.

**Q: Phiên bản Aspose.PSD nào cần thiết cho các API này?**  
A: Các lớp `LengthRecord` và `PathOperations` đã có từ Aspose.PSD 20.10. Khuyến nghị sử dụng phiên bản mới nhất.

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}