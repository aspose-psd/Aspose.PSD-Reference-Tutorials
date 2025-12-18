---
date: 2025-12-17
description: Tìm hiểu cách chỉnh sửa các hình vector PSD bằng cách hỗ trợ các thuộc
  tính dữ liệu bản ghi độ dài sử dụng Aspose.PSD cho Java. Hướng dẫn từng bước kèm
  ví dụ mã.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Cách chỉnh sửa các hình vector PSD – Hỗ trợ các thuộc tính dữ liệu bản ghi
  độ dài trong Java
url: /vi/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hỗ trợ Thuộc tính Dữ liệu Bản ghi Độ dài trong PSD - Java

## Giới thiệu
Nếu bạn cần **sửa đổi các hình vector trong PSD** một cách lập trình, thư viện Aspose.PSD for Java cung cấp cho bạn toàn quyền kiểm soát các tệp Photoshop ngay từ mã Java của mình. Trong hướng dẫn này, chúng ta sẽ đi qua mọi thứ bạn cần biết để hỗ trợ các thuộc tính dữ liệu bản ghi độ dài — một bước thiết yếu khi bạn muốn chỉnh sửa các lớp hình vector. Khi hoàn thành, bạn sẽ có thể mở một tệp PSD, điều chỉnh các thuộc tính hình vector, và lưu tệp đã cập nhật mà không rời khỏi IDE. Hãy cùng bắt đầu!

## Câu trả lời nhanh
- **“Sửa đổi các hình vector trong PSD” có nghĩa là gì?** Điều chỉnh hình học, các thao tác đường dẫn, hoặc các thuộc tính khác của các lớp dựa trên vector bên trong tệp PSD.  
- **Thư viện nào thực hiện việc này?** Aspose.PSD for Java.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc đánh giá; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Thời gian triển khai khoảng bao lâu?** Khoảng 10‑15 phút cho một script sửa đổi hình cơ bản.  
- **Các yêu cầu chính là gì?** Java JDK, Aspose.PSD for Java, và một tệp PSD mẫu.

## “Sửa đổi các hình vector trong PSD” là gì?
Việc sửa đổi các hình vector trong PSD liên quan đến việc thay đổi dữ liệu đường dẫn vector nền tảng — chẳng hạn như các bản ghi độ dài và các thao tác đường dẫn — để giao diện hình dạng được cập nhật tương ứng. Điều này đặc biệt hữu ích cho các quy trình đồ họa tự động, xử lý hàng loạt, hoặc công cụ thiết kế tùy chỉnh.

## Tại sao nên dùng Aspose.PSD for Java để sửa đổi các hình vector trong PSD?
- **Không cần Photoshop** – làm việc trực tiếp với tệp PSD trên bất kỳ máy chủ nào.  
- **API phong phú** – truy cập các lớp, tài nguyên và dữ liệu vector bằng các lớp được định kiểu mạnh.  
- **Đa nền tảng** – chạy trên Windows, Linux hoặc macOS với bất kỳ JDK nào.  
- **Tối ưu hiệu năng** – quản lý bộ nhớ hiệu quả và thao tác lưu nhanh chóng.

## Các yêu cầu trước
1. **Java Development Kit (JDK)** – tải về từ [trang web của Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) hoặc dùng trình quản lý gói ưa thích.  
2. **Aspose.PSD for Java** – lấy JAR mới nhất từ [trang phát hành của Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, hoặc bất kỳ trình soạn thảo Java nào tương thích.  
4. **Một tệp PSD** – tạo trong Photoshop hoặc lấy một tệp PSD mẫu để thử nghiệm.  
5. **Kiến thức cơ bản về Java** – quen thuộc với lớp, đối tượng và xử lý ngoại lệ.

## Nhập các gói
Đầu tiên, nhập các lớp cần thiết để làm việc với tệp PSD và tài nguyên hình vector.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Bước 1: Thiết lập Thư mục Nguồn và Thư mục Đầu ra
Xác định vị trí tệp PSD gốc và nơi bạn muốn lưu tệp đã sửa đổi.

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

## Bước 3: Xác định tài nguyên Vsms trong Lớp
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

## Bước 4: Truy cập các Bản ghi Độ dài
Mỗi `LengthRecord` đại diện cho một đường dẫn vector riêng biệt. Lấy những bản ghi bạn dự định sửa đổi.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Bước 5: Sửa đổi Thuộc tính Thao tác Đường dẫn
Bây giờ bạn có thể **sửa đổi các hình vector trong PSD** bằng cách thay đổi `PathOperations` của chúng. Điều này quyết định cách các hình tương tác (ví dụ: loại trừ, giao nhau, trừ).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Bước 6: Lưu tệp PSD đã sửa đổi
Ghi lại các thay đổi vào một tệp mới.

```java
psdImage.save(outPsdFilePath);
```

## Bước 7: Dọn dẹp Tài nguyên
Giải phóng `PsdImage` để giải phóng bộ nhớ.

```java
psdImage.dispose();
```

## Những lỗi thường gặp & Mẹo
- **Kiểm tra null** – luôn xác nhận `resource` không phải là `null` trước khi truy cập các đường dẫn.  
- **Giới hạn chỉ số đường dẫn** – đảm bảo các chỉ số bạn dùng (`[2]`, `[7]`, `[11]`) tồn tại trong PSD cụ thể mà bạn đang chỉnh sửa.  
- **Giấy phép** – chạy mà không có giấy phép hợp lệ sẽ chèn một watermark vào PSD đã lưu.  

## Kết luận
Bạn đã có một ví dụ hoàn chỉnh, từ đầu đến cuối, về cách **sửa đổi các hình vector trong PSD** bằng cách hỗ trợ các thuộc tính dữ liệu bản ghi độ dài với Aspose.PSD for Java. Dù bạn đang tự động hoá quy trình tài sản hay xây dựng công cụ thiết kế tùy chỉnh, các API này cho phép bạn thao tác các lớp vector mà không cần Photoshop thủ công. Hãy khám phá thêm bằng cách thử nghiệm các `PathOperations` khác hoặc kết hợp nhiều chỉnh sửa `LengthRecord` cho các hình dạng phức tạp.

## Các câu hỏi thường gặp

**H: Làm sao tôi xử lý một PSD không chứa lớp hình vector?**  
Đ: `VsmsResource` sẽ không tồn tại, vì vậy `resource` sẽ giữ giá trị `null`. Thêm kiểm tra và bỏ qua bước sửa đổi hoặc thông báo cho người dùng.

**H: Tôi có thể thay đổi các thuộc tính khác như màu nền hoặc độ rộng nét không?**  
Đ: Có, `LengthRecord` cung cấp các setter bổ sung cho màu nền, nét và độ trong suốt. Tham khảo tài liệu API để biết chi tiết.

**H: Có thể xử lý hàng loạt nhiều tệp PSD không?**  
Đ: Chắc chắn. Đặt mã vào vòng lặp duyệt qua một thư mục chứa các tệp PSD, điều chỉnh đường dẫn đầu vào và đầu ra cho mỗi lần.

**H: Tôi có cần đóng các luồng (streams) thủ công khi tải từ đường dẫn tệp không?**  
Đ: Phương thức `Image.load` tự động quản lý luồng tệp, nhưng nếu bạn tải từ một `InputStream`, hãy nhớ đóng nó sau khi sử dụng.

**H: Phiên bản Aspose.PSD nào cần thiết cho các API này?**  
Đ: Các lớp `LengthRecord` và `PathOperations` đã có từ Aspose.PSD 20.10. Khuyến nghị sử dụng phiên bản mới nhất.

---

**Cập nhật lần cuối:** 2025-12-17  
**Kiểm tra với:** Aspose.PSD for Java 24.11  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}