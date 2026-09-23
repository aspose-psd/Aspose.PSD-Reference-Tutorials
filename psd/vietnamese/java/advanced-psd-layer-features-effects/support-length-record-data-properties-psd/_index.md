---
date: 2026-09-23
description: Tìm hiểu cách chỉnh sửa vector shapes của PSD và batch process các tệp
  PSD bằng Aspose.PSD for Java. Các bước chi tiết, tips và code placeholders cho giải
  pháp hoàn chỉnh.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Hỗ trợ Length Record Data Properties trong PSD - Java
og_description: Tìm hiểu cách chỉnh sửa vector shapes của PSD và batch process các
  tệp PSD bằng Aspose.PSD for Java. Hướng dẫn step‑by‑step với code placeholders và
  expert tips.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Chỉnh sửa vector shapes của PSD với Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Chỉnh sửa vector shapes của PSD với Aspose.PSD for Java
url: /vi/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Sửa đổi các hình dạng vector PSD với Aspose.PSD cho Java

## Giới thiệu
Nếu bạn cần **sửa đổi các hình dạng vector PSD** một cách lập trình, Aspose.PSD cho Java cung cấp cho bạn toàn quyền kiểm soát các tệp Photoshop trực tiếp từ mã Java của mình. Hướng dẫn này sẽ đưa bạn qua việc hỗ trợ các thuộc tính bản ghi độ dài — một bước quan trọng khi chỉnh sửa các lớp hình dạng vector. Khi kết thúc, bạn sẽ có thể mở một tệp PSD, điều chỉnh dữ liệu hình dạng vector của nó và lưu tệp đã cập nhật mà không cần khởi chạy Photoshop.

## Câu trả lời nhanh
- **“modify PSD vector shapes” có nghĩa là gì?** Điều chỉnh hình học, các thao tác đường dẫn, hoặc các thuộc tính khác của các lớp dựa trên vector trong tệp PSD.  
- **Thư viện nào xử lý việc này?** Aspose.PSD cho Java.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc đánh giá; giấy phép thương mại là bắt buộc cho môi trường sản xuất.  
- **Thời gian thực hiện khoảng bao lâu?** Khoảng 10‑15 phút cho một script chỉnh sửa hình dạng cơ bản.  
- **Các yêu cầu trước tiên là gì?** Java JDK, Aspose.PSD cho Java, và một tệp PSD mẫu.

## “support length record properties” là gì?
Hỗ trợ các thuộc tính bản ghi độ dài có nghĩa là truy cập và cập nhật các đối tượng `LengthRecord` mô tả mỗi đường vector trong PSD. Các bản ghi này lưu trữ thông tin như độ dài đường, loại và cách chúng nối với các đường khác. Thay đổi chúng cho phép bạn kiểm soát cách các hình dạng kết hợp, giao nhau hoặc trừ nhau, tạo điều kiện cho việc chỉnh sửa vector chính xác.

## Tại sao nên sử dụng Aspose.PSD cho Java để hỗ trợ các thuộc tính bản ghi độ dài?
Tải PSD của bạn, chỉnh sửa dữ liệu vector và lưu — tất cả mà không cần Photoshop. Aspose.PSD xử lý các tệp PSD hàng trăm trang trong vòng dưới 2 giây trên một máy chủ tiêu chuẩn, cung cấp hơn 150 lớp (bao gồm hơn 30 loại liên quan đến vector), và chạy trên Windows, Linux hoặc macOS với bất kỳ JDK 11+ nào. Thư viện tập trung vào hiệu năng này loại bỏ nhu cầu sử dụng phần mềm máy tính để bàn đắt tiền.

## Yêu cầu trước
1. **Java Development Kit (JDK)** – tải xuống từ [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) hoặc sử dụng trình quản lý gói ưa thích của bạn.  
2. **Aspose.PSD cho Java** – lấy JAR mới nhất từ [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, hoặc bất kỳ trình chỉnh sửa nào tương thích với Java.  
4. **A PSD file** – tạo một tệp trong Photoshop hoặc lấy một mẫu PSD để thử nghiệm.  
5. **Basic Java knowledge** – quen thuộc với các lớp, đối tượng và xử lý ngoại lệ.

## Nhập các gói
Các câu lệnh import đưa các lớp cốt lõi của Aspose.PSD vào phạm vi, chẳng hạn như `PsdImage`, `VsmsResource` và `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Bước 1: Thiết lập thư mục nguồn và thư mục đầu ra
Xác định vị trí tệp PSD gốc và nơi tệp đã chỉnh sửa sẽ được ghi.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Bước 2: Tải tệp PSD
Sử dụng `Image.load` để mở tệp và ép kiểu thành `PsdImage` để sử dụng các tính năng đặc thù của PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Bước 3: Xác định tài nguyên Vsms trong lớp
`VsmsResource` là container lưu trữ dữ liệu hình dạng vector cho một lớp. Duyệt qua các tài nguyên của lớp thứ hai để tìm nó.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Bước 4: Truy cập các bản ghi độ dài
`LengthRecord` đại diện cho một đường vector riêng biệt. Lấy các bản ghi mà bạn dự định chỉnh sửa.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Bước 5: Sửa đổi các thuộc tính thao tác đường dẫn
`PathOperations` xác định cách các hình dạng riêng lẻ tương tác (ví dụ: loại trừ, giao nhau, trừ). Thay đổi các giá trị này sẽ cập nhật thành phần hình ảnh của lớp vector.

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

## Bước 7: Dọn dẹp tài nguyên
Giải phóng đối tượng `PsdImage` để giải phóng bộ nhớ và tránh rò rỉ tài nguyên.

```java
psdImage.dispose();
```

## Cách xử lý hàng loạt các tệp PSD với hỗ trợ các thuộc tính bản ghi độ dài
Bao bọc quy trình một tệp trong một vòng lặp duyệt qua một thư mục chứa các tệp PSD, cập nhật `inPsdFilePath` và `outPsdFilePath` cho mỗi tệp. Cách tiếp cận này cho phép bạn áp dụng các điều chỉnh hình dạng vector giống nhau cho hàng chục hoặc hàng trăm tệp trong vài phút, lý tưởng cho các pipeline tài sản tự động.

## Những khó khăn thường gặp & mẹo
- **Null checks** – luôn kiểm tra `resource` không phải là `null` trước khi truy cập các thành viên của nó.  
- **Path index bounds** – đảm bảo các chỉ mục bạn sử dụng (ví dụ: `[2]`, `[7]`, `[11]`) tồn tại trong PSD cụ thể mà bạn đang chỉnh sửa.  
- **License** – chạy mà không có giấy phép hợp lệ sẽ chèn watermark vào PSD đã lưu.

## Kết luận
Bây giờ bạn đã có một ví dụ hoàn chỉnh, từ đầu đến cuối về cách **modify PSD vector shapes** bằng cách hỗ trợ các thuộc tính bản ghi độ dài với Aspose.PSD cho Java. Dù bạn đang tự động hoá pipeline tài sản hay xây dựng công cụ thiết kế tùy chỉnh, các API này cung cấp cho bạn sự linh hoạt để thao tác các lớp vector mà không cần công việc thủ công trên Photoshop. Thử nghiệm với các giá trị `PathOperations` khác hoặc kết hợp nhiều chỉnh sửa `LengthRecord` để tạo ra các hình dạng phức tạp.

## Câu hỏi thường gặp

**Q: Làm thế nào để xử lý một PSD không chứa lớp hình dạng vector?**  
A: `VsmsResource` sẽ không tồn tại, vì vậy `resource` sẽ là `null`. Thêm kiểm tra và bỏ qua bước chỉnh sửa hoặc thông báo cho người dùng.

**Q: Tôi có thể thay đổi các thuộc tính khác như màu nền hoặc độ rộng nét không?**  
A: Có, `LengthRecord` cung cấp các setter cho màu nền, nét và độ trong suốt. Xem tài liệu API để biết danh sách đầy đủ.

**Q: Có thể xử lý hàng loạt nhiều tệp PSD không?**  
A: Chắc chắn. Bao bọc mã trong một vòng lặp duyệt qua thư mục các tệp PSD, điều chỉnh các đường dẫn đầu vào và đầu ra mỗi lần.

**Q: Tôi có cần đóng các stream một cách thủ công khi tải từ đường dẫn tệp không?**  
A: `Image.load` tự động xử lý các stream tệp, nhưng nếu bạn tải từ một `InputStream`, hãy nhớ đóng nó sau khi sử dụng.

**Q: Phiên bản Aspose.PSD nào cần thiết cho các API này?**  
A: Các lớp `LengthRecord` và `PathOperations` đã có từ Aspose.PSD 20.10. Khuyến nghị sử dụng phiên bản mới nhất (24.11 tại thời điểm viết).

---

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## Các hướng dẫn liên quan

- [Convert PSD to PNG and Create Vector Mask Java – Vmsk Resource in PSD Files](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Convert PSD to PNG with Layer Mask Support Using Aspose.PSD for Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Add Layer Support Psd Files](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}