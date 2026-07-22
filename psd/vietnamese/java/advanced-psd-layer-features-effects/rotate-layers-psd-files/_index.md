---
date: 2026-07-22
description: Tìm hiểu cách lưu psd thành png, giữ nguyên độ trong suốt PNG, và xoay
  các lớp PSD trong Java với Aspose.PSD. Hướng dẫn từng bước, giải thích không cần
  mã, và mẹo khắc phục sự cố.
keywords:
- save psd as png
- export psd layers png
- convert photoshop file png
- psd to png transparency
lastmod: 2026-07-22
linktitle: lưu psd thành png và xoay các lớp trong Java bằng Aspose.PSD
og_description: lưu psd thành png với Aspose.PSD cho Java. Giữ độ trong suốt, xoay
  các lớp, và xuất PNG chỉ trong vài dòng mã—lý tưởng cho quy trình tự động.
og_image_alt: 'Developer guide: save PSD as PNG and rotate layers using Aspose.PSD
  for Java'
og_title: lưu psd thành png và xoay các lớp trong Java bằng Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  headline: save psd as png and rotate layers in Java using Aspose.PSD
  type: TechArticle
- description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  name: save psd as png and rotate layers in Java using Aspose.PSD
  steps:
  - name: Set Up Your Java Project
    text: Create a new Java project in your IDE and add the Aspose.PSD JAR to the
      project’s build path.
  - name: Import Required Classes
    text: '`PsdImage` is the core class that represents a Photoshop document in memory.
      `PngOptions` controls PNG‑specific settings, and `RotateFlipType` defines rotation
      and flip operations. These imports give you access to image loading, rotation,
      and PNG‑specific options.'
  - name: Define File Paths
    text: Specify where your source PSD lives and where the output files should be
      written. Using absolute paths during testing avoids “file not found” errors.
      > **Pro tip:** Store paths in a configuration file for easier maintenance in
      larger projects.
  - name: Load the PSD File
    text: '`PsdImage` loads the entire Photoshop document, including all layers, masks,
      and effects, into a manipulable object. Now `im` represents the whole PSD, ready
      for transformations.'
  - name: Rotate the Image (How to rotate PSD)
    text: '`RotateFlipType` enumerates all supported rotations and flips. In this
      example we rotate 270° and flip both axes, which swaps width and height while
      mirroring the image. Feel free to experiment with other values such as `Rotate90FlipNone`
      or `Rotate180FlipX`.'
  - name: Save the Rotated Image as PNG (save PSD as PNG)
    text: Configure `PngOptions` to keep transparency (`PngColorType.TruecolorWithAlpha`)
      and then call `save`. The PNG retains layer transparency, ensuring it works
      seamlessly in web or mobile apps. The resulting PNG preserves alpha channels,
      making it suitable for compositing or further processing.
  - name: Save the Modified PSD (optional)
    text: If you also need a new PSD with the rotation applied, you can save the modified
      `PsdImage` back to disk. You now have both a PNG preview and an updated PSD
      file.
  type: HowTo
- questions:
  - answer: Yes, you can call `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`
      after iterating through `im.getLayers()`.
    question: Can I rotate a specific layer in a PSD file?
  - answer: The library handles most files efficiently, but extremely large PSDs (>500
      MB) may require additional memory or streaming options.
    question: Is there any performance limitation with Aspose.PSD for Java?
  - answer: Aspose offers a free trial, but a paid license is needed for production.
      See the [temporary license](https://purchase.aspose.com/temporary-license/)
      for testing.
    question: Is Aspose.PSD free to use?
  - answer: Comprehensive docs are available at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Get help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).
    question: What if I encounter issues while using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
- rotate PSD layers
title: lưu psd thành png và xoay các lớp trong Java bằng Aspose.PSD
url: /vi/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

## Các hướng dẫn liên quan

- [Lưu PSD dưới dạng PNG và Áp dụng Đổ bóng Kết xuất trong Aspose.PSD cho Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Cách nén tệp PNG bằng Aspose.PSD cho Java](/psd/java/optimizing-png-files/compress-png-files/)
- [Cách Xoay ảnh trong Java với Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/pf/main-wrap-class >}}

# Lưu PSD dưới dạng PNG và xoay các lớp trong Java bằng Aspose.PSD

## Giới thiệu
Nếu bạn cần **lưu PSD dưới dạng PNG** đồng thời xoay các lớp, hướng dẫn này dành cho bạn. Dù bạn đang xây dựng công cụ xử lý hàng loạt, dịch vụ web cần thao tác ảnh nhanh chóng, hay chỉ đơn giản là tự động hoá quy trình thiết kế, việc thực hiện bằng mã nguồn sẽ tiết kiệm thời gian và loại bỏ phụ thuộc vào Adobe Photoshop. Trong tutorial này chúng ta sẽ đi qua **cách xoay các lớp PSD** và xuất kết quả dưới dạng PNG bằng thư viện Aspose.PSD cho Java. Hãy cùng bắt tay vào và làm cho quy trình thiết kế của bạn chạy mượt mà!

## Câu trả lời nhanh
- **Thư viện nào tôi có thể sử dụng?** Aspose.PSD for Java  
- **Tôi có thể vừa xoay vừa lưu PSD dưới dạng PNG trong một lần không?** Có – xoay PSD rồi lưu dưới dạng PNG  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc kiểm tra; giấy phép trả phí cần cho môi trường sản xuất  
- **Phiên bản Java nào được hỗ trợ?** Java 8 trở lên  
- **Đầu ra PNG có trong suốt không?** Có, khi bạn đặt `PngColorType.TruecolorWithAlpha`

## “Chuyển đổi PSD sang PNG” là gì?
Chuyển đổi một tài liệu Photoshop (PSD) sang ảnh PNG trích xuất nội dung hình ảnh—bao gồm các lớp, mặt nạ và kênh alpha—vào một định dạng raster được hỗ trợ rộng rãi và giữ được tính trong suốt. Điều này làm cho PNG trở nên lý tưởng cho đồ họa web, ảnh thu nhỏ và các quy trình xử lý ảnh tiếp theo. PNG kết quả có thể được sử dụng trực tiếp trong trang web, ứng dụng di động, hoặc được xử lý thêm bởi các thư viện ảnh khác.

## Tại sao sử dụng Aspose.PSD cho Java để lưu PSD dưới dạng PNG và xoay các lớp PSD?
Aspose.PSD cho phép bạn **lưu PSD dưới dạng PNG** và xoay các lớp mà không cần cài đặt Photoshop. Nó hỗ trợ **hơn 50 định dạng đầu vào và đầu ra**, xử lý các tệp PSD hàng trăm trang với dung lượng RAM dưới 200 MB, và chạy trên Windows, Linux và macOS. API chỉ yêu cầu một vài lời gọi phương thức, cung cấp kết quả độ chính xác cao với việc xử lý sẵn các hiệu ứng lớp, mặt nạ và kênh alpha.

## Yêu cầu trước
Trước khi chúng ta đi vào mã, hãy chắc chắn bạn đã có:

- **Bộ công cụ phát triển Java (JDK)** – tải xuống từ [trang web Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Môi trường phát triển tích hợp (IDE)** – IntelliJ IDEA, Eclipse hoặc NetBeans đều được.  
- **Thư viện Aspose.PSD cho Java** – lấy JAR mới nhất từ [trang phát hành](https://releases.aspose.com/psd/java/).  
- **Kiến thức cơ bản về Java** – quen thuộc với lớp, đối tượng và xử lý ngoại lệ.

## Hướng dẫn từng bước

### Bước 1: Thiết lập dự án Java của bạn
Tạo một dự án Java mới trong IDE và thêm JAR Aspose.PSD vào đường dẫn biên dịch của dự án.

### Bước 2: Nhập các lớp cần thiết
`PsdImage` là lớp cốt lõi đại diện cho tài liệu Photoshop trong bộ nhớ. `PngOptions` điều khiển các cài đặt đặc thù cho PNG, và `RotateFlipType` định nghĩa các thao tác xoay và lật.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Các import này cho phép bạn truy cập vào việc tải ảnh, xoay và các tùy chọn đặc thù cho PNG.

### Bước 3: Xác định đường dẫn tệp
Xác định nơi lưu trữ PSD nguồn và nơi các tệp đầu ra sẽ được ghi. Sử dụng đường dẫn tuyệt đối trong quá trình thử nghiệm giúp tránh lỗi “file not found”.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Mẹo chuyên nghiệp:** Lưu các đường dẫn trong tệp cấu hình để dễ bảo trì hơn trong các dự án lớn.

### Bước 4: Tải tệp PSD
`PsdImage` tải toàn bộ tài liệu Photoshop, bao gồm tất cả các lớp, mặt nạ và hiệu ứng, vào một đối tượng có thể thao tác.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Bây giờ `im` đại diện cho toàn bộ PSD, sẵn sàng cho các biến đổi.

### Bước 5: Xoay ảnh (Cách xoay PSD)
`RotateFlipType` liệt kê tất cả các kiểu xoay và lật được hỗ trợ. Trong ví dụ này chúng ta xoay 270° và lật cả hai trục, điều này hoán đổi chiều rộng và chiều cao đồng thời phản chiếu ảnh.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Bạn có thể thử các giá trị khác như `Rotate90FlipNone` hoặc `Rotate180FlipX`.

### Bước 6: Lưu ảnh đã xoay dưới dạng PNG (lưu PSD dưới dạng PNG)
Cấu hình `PngOptions` để giữ tính trong suốt (`PngColorType.TruecolorWithAlpha`) và sau đó gọi `save`. PNG sẽ giữ lại độ trong suốt của lớp, đảm bảo hoạt động liền mạch trong web hoặc ứng dụng di động.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

PNG kết quả bảo toàn các kênh alpha, phù hợp cho việc ghép lớp hoặc xử lý tiếp theo.

### Bước 7: Lưu PSD đã chỉnh sửa (tùy chọn)
Nếu bạn cũng cần một tệp PSD mới với việc xoay đã được áp dụng, bạn có thể lưu lại `PsdImage` đã chỉnh sửa trở lại đĩa.

```java
im.save(psdPath);
```

Bây giờ bạn có cả bản xem trước PNG và tệp PSD đã cập nhật.

## Các vấn đề thường gặp và giải pháp
- **Tệp không tìm thấy:** Kiểm tra `dataDir` kết thúc bằng dấu phân cách đường dẫn (`/` hoặc `\`).  
- **OutOfMemoryError trên các PSD lớn:** Tăng kích thước heap JVM (`-Xmx2g`).  
- **Mất tính trong suốt:** Đảm bảo đã đặt `PngColorType.TruecolorWithAlpha`; nếu không PNG sẽ được lưu mà không có alpha.  
- **Ảnh PSD bị lật không hoạt động như mong đợi:** Kiểm tra lại hằng số `RotateFlipType` bạn đã chọn; một số hằng số kết hợp xoay và lật trong một bước.

## Câu hỏi thường gặp

**H: Tôi có thể xoay một lớp cụ thể trong tệp PSD không?**  
**Đ:** Có, bạn có thể gọi `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)` sau khi duyệt qua `im.getLayers()`.

**H: Có giới hạn hiệu năng nào với Aspose.PSD cho Java không?**  
**Đ:** Thư viện xử lý hầu hết các tệp một cách hiệu quả, nhưng các PSD cực lớn (>500 MB) có thể cần thêm bộ nhớ hoặc tùy chọn streaming.

**H: Aspose.PSD có miễn phí không?**  
**Đ:** Aspose cung cấp bản dùng thử miễn phí, nhưng cần giấy phép trả phí cho môi trường sản xuất. Xem [giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) để thử nghiệm.

**H: Tôi có thể tìm tài liệu chi tiết ở đâu?**  
**Đ:** Tài liệu đầy đủ có sẵn tại [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**H: Nếu tôi gặp vấn đề khi sử dụng Aspose.PSD thì sao?**  
**Đ:** Nhận trợ giúp qua [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

**H: Việc chuyển PSD sang PNG có giữ lại hiệu ứng lớp không?**  
**Đ:** Có, khi lưu với `PngColorType.TruecolorWithAlpha`, hầu hết các hiệu ứng trực quan sẽ được raster hoá vào PNG.

**H: Tôi có thể xử lý hàng loạt nhiều tệp PSD không?**  
**Đ:** Chắc chắn. Đặt mã trong vòng lặp duyệt qua thư mục chứa các tệp PSD.

**H: Có thể đặt mức nén PNG không?**  
**Đ:** `PngOptions` cung cấp phương thức `setCompressionLevel(int)` để tinh chỉnh kích thước đầu ra.

**H: Tôi có cần đóng đối tượng ảnh không?**  
**Đ:** `PsdImage` triển khai `Closeable`; sử dụng try‑with‑resources hoặc gọi `im.close()` trong khối `finally`.

**H: PNG đã xoay sẽ có cùng kích thước với bản gốc không?**  
**Đ:** Xoay 90° hoặc 270° sẽ hoán đổi chiều rộng và chiều cao, vì vậy PNG sẽ tự động phản ánh hướng mới.

## Kết luận
Bằng cách tận dụng Aspose.PSD cho Java, bạn có thể **lưu PSD dưới dạng PNG**, **giữ tính trong suốt của PNG**, và **xoay các lớp PSD** chỉ với vài dòng mã. Cách tiếp cận này loại bỏ nhu cầu Photoshop, tăng tốc quy trình tự động và cho bạn toàn quyền kiểm soát đầu ra ảnh. Hãy thử trên các dự án của mình và cảm nhận sự tiết kiệm thời gian!

---

**Last Updated:** 2026-07-22  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}