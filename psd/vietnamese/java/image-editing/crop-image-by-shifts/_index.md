---
date: 2026-07-03
description: Tìm hiểu cách crop image java bằng cách sử dụng Aspose.PSD for Java.
  Hướng dẫn step‑by‑step image cropping này bao gồm loading PSD files, setting shift
  values và saving the result.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Crop Image bằng Shifts
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Crop Image Java by Shifts với Aspose.PSD
url: /vi/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cắt Ảnh Java bằng Dịch Chuyển với Aspose.PSD

## Giới thiệu

Trong xử lý ảnh bằng Java, **crop image java** là một yêu cầu phổ biến để chuẩn bị đồ họa, ảnh thu nhỏ hoặc tài sản UI. Aspose.PSD for Java làm cho nhiệm vụ này trở nên đơn giản bằng cách cung cấp một phương thức `crop` dễ dùng, hoạt động trên bất kỳ định dạng raster nào được hỗ trợ. Trong hướng dẫn này, bạn sẽ học cách tải tệp PSD, xác định các giá trị dịch chuyển trái‑phải‑trên‑dưới, áp dụng việc cắt và lưu kết quả—tất cả mà không cần viết mã thao tác pixel tùy chỉnh.

## Câu trả lời nhanh
- **Thư viện nào xử lý việc cắt?** Aspose.PSD for Java cung cấp phương thức `crop` tích hợp.  
- **Tôi có cần giấy phép không?** Giấy phép tạm thời hoạt động cho việc đánh giá; giấy phép đầy đủ cần thiết cho môi trường sản xuất.  
- **Các định dạng được hỗ trợ?** Hơn 30 định dạng raster, bao gồm PSD, JPEG, PNG, BMP và TIFF.  
- **Kích thước tệp tối đa?** Xử lý các tệp lên tới 2 GB mà không cần tải toàn bộ ảnh vào bộ nhớ.  
- **Cần bao nhiêu dòng mã?** Chỉ năm bước logic—tải, cache, định nghĩa dịch chuyển, cắt và lưu.

## Crop image java là gì?
`crop image java` đề cập đến thao tác cắt bớt một bitmap trong ứng dụng Java. Khi sử dụng Aspose.PSD, thao tác này được thực hiện bằng phương thức `crop`, nhận các giá trị dịch chuyển cho mỗi phía của ảnh và trả về một thể hiện ảnh mới.

## Tại sao nên dùng Aspose.PSD để cắt ảnh?
Aspose.PSD hỗ trợ **30+** định dạng ảnh và có thể xử lý các tệp PSD hàng trăm trang trong khi sử dụng dưới 150 MB RAM, nhờ kiến trúc tải lười. Thư viện cũng đảm bảo kết quả pixel‑perfect, giữ nguyên các lớp, mặt nạ và hồ sơ màu—điều mà nhiều thư viện ảnh chung không thể đảm bảo.

## Yêu cầu trước

### Java Development Kit (JDK)

Đảm bảo bạn đã cài đặt phiên bản mới nhất của JDK trên hệ thống. Bạn có thể tải về từ [đây](https://www.oracle.com/java/technologies/javase-downloads.html).

### Thư viện Aspose.PSD cho Java

Để bắt đầu, bạn cần lấy thư viện Aspose.PSD for Java. Truy cập [trang tải xuống](https://releases.aspose.com/psd/java/) và tải phiên bản mới nhất.

### Môi trường Phát triển Tích hợp (IDE)

Chọn IDE Java yêu thích của bạn, chẳng hạn Eclipse hoặc IntelliJ, để có trải nghiệm lập trình mượt mà.

## Cách cắt ảnh java?

Tải tệp nguồn, xác định các dịch chuyển pixel cho mỗi phía, và gọi phương thức `crop`—toàn bộ quy trình này có thể được viết trong năm dòng mã ngắn gọn. Thao tác `crop` tạo ra một ảnh mới chỉ chứa vùng bạn chỉ định, để nguyên tệp gốc không bị thay đổi.

### Bước 1: Tải ảnh

`Image` là lớp cơ sở cho tất cả các loại ảnh trong Aspose.PSD.  
`RasterImage` đại diện cho ảnh raster và cung cấp khả năng cắt.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Bước 2: Cache Dữ liệu Ảnh

`cacheData()` tải dữ liệu ảnh vào bộ nhớ để xử lý nhanh hơn.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Bước 3: Định nghĩa Giá trị Dịch Chuyển

Xác định các giá trị dịch chuyển cho bốn phía của ảnh (trái, trên, phải, dưới) tính bằng pixel.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Bước 4: Áp dụng Cắt

`crop(left, right, top, bottom)` cắt ảnh theo các dịch chuyển pixel đã chỉ định ở mỗi phía.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Bước 5: Lưu Kết quả

`JpegOptions` định nghĩa các cài đặt mã hoá JPEG như chất lượng và hồ sơ màu.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Chúc mừng! Bạn đã cắt thành công một ảnh bằng Aspose.PSD for Java.

## Các vấn đề thường gặp và giải pháp

- **Ảnh không thay đổi:** Kiểm tra các giá trị dịch chuyển là dương và không vượt quá kích thước gốc.  
- **OutOfMemoryError khi xử lý tệp lớn:** Bật cache như trong Bước 2; điều này buộc Aspose.PSD sử dụng tệp tạm thời thay vì giữ toàn bộ ảnh trong RAM.  
- **Màu sắc bị dịch sau khi cắt:** Đảm bảo giữ hồ sơ màu bằng cách gọi `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` nếu bạn cần độ chính xác màu tuyệt đối.

## Câu hỏi thường gặp

**Q: Aspose.PSD có tương thích với tất cả các định dạng ảnh không?**  
A: Có, Aspose.PSD hỗ trợ hơn 30 định dạng raster, bao gồm PSD, JPEG, PNG, BMP, TIFF và GIF, đảm bảo tính tương thích rộng rãi.

**Q: Tôi có thể áp dụng nhiều thao tác cắt lên cùng một ảnh không?**  
A: Hoàn toàn có thể. Sau mỗi lần gọi `crop` bạn sẽ nhận được một đối tượng ảnh mới, có thể cắt lại nếu cần.

**Q: Có diễn đàn cộng đồng hỗ trợ Aspose.PSD không?**  
A: Có, bạn có thể tìm kiếm hỗ trợ và tham gia cộng đồng tại [Diễn đàn Aspose.PSD](https://forum.aspose.com/c/psd/34).

**Q: Làm sao để lấy giấy phép tạm thời cho Aspose.PSD?**  
A: Truy cập [đây](https://purchase.aspose.com/temporary-license/) để nhận giấy phép tạm thời.

**Q: Có dự án mẫu nào minh họa các tính năng của Aspose.PSD không?**  
A: Khám phá tài liệu và ví dụ tại [Tài liệu Aspose.PSD Java](https://reference.aspose.com/psd/java/).

---

**Cập nhật lần cuối:** 2026-07-03  
**Kiểm thử với:** Aspose.PSD 24.11 for Java  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Hướng dẫn liên quan

- [Cắt ảnh bằng hình chữ nhật trong Aspose.PSD cho Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Cắt ảnh Java - Mở rộng và Cắt ảnh với Aspose.PSD cho Java](/psd/java/image-editing/expand-and-crop-images/)
- [Thay đổi kích thước ảnh Java - Sử dụng Enumeration Resize Type trong Aspose.PSD cho Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}