---
date: 2026-11-04
description: Tìm hiểu cách sử dụng Aspose.PSD cho Java để áp dụng invert adjustment
  layer, xử lý hàng loạt ảnh PSD và tạo tệp PSD ảnh âm.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Cách sử dụng Aspose.PSD cho Java để thêm invert adjustment layer,
  xử lý hàng loạt ảnh PSD và tạo ảnh âm PSD. Thực hiện theo hướng dẫn từng bước.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Cách sử dụng Aspose.PSD để thêm invert adjustment layer trong Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Cách sử dụng Aspose.PSD để thêm invert adjustment layer trong Java
url: /vi/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách sử dụng Aspose.PSD để thêm lớp điều chỉnh Đảo ngược trong Java

## Giới thiệu

Nếu bạn đang tìm kiếm một **thư viện xử lý ảnh java** mạnh mẽ, Aspose.PSD cho Java là một trong những lựa chọn đa năng nhất trên thị trường. Trong hướng dẫn này, bạn sẽ thấy **cách sử dụng Aspose** để chèn một **Invert Adjustment Layer** vào tệp PSD, xếp chồng nó với các điều chỉnh khác, và thậm chí thực hiện thao tác trên hàng chục tệp. Dù bạn đang xây dựng công cụ xử lý hàng loạt, dịch vụ ảnh phía máy chủ, hay trình chỉnh sửa ảnh đơn, các bước dưới đây sẽ đưa bạn từ PSD nguồn đến một hình ảnh âm bản có thể chỉnh sửa hoàn toàn trong vài phút.

## Câu trả lời nhanh
- **Lớp Điều chỉnh Đảo ngược làm gì?** Nó đảo ngược mọi giá trị RGB trong khu vực đã chọn, biến ảnh thành một ảnh âm bản.  
- **Thư viện nào cung cấp tính năng này?** Aspose.PSD, một **thư viện xử lý ảnh java** hàng đầu.  
- **Tôi có thể xếp chồng nó với các điều chỉnh khác không?** Có – bạn có thể **apply multiple adjustment layers** như Độ sáng/Tương phản, Hue/Saturation, và hơn nữa.  
- **Tôi có cần giấy phép cho việc phát triển không?** Có phiên bản dùng thử miễn phí; giấy phép cần thiết cho việc sử dụng trong môi trường sản xuất.  
- **Thời gian triển khai mất bao lâu?** Thông thường dưới 10 phút cho một trường hợp sử dụng cơ bản.

## Lớp Điều chỉnh Đảo ngược là gì?

Lớp Điều chỉnh Đảo ngược là một chỉnh sửa không phá hủy, đảo ngược các giá trị màu của mỗi pixel mà nó ảnh hưởng. Vì nó nằm trên đỉnh ngăn xếp lớp, bạn có thể bật/tắt hiển thị hoặc thay đổi thứ tự mà không làm thay đổi vĩnh viễn dữ liệu ảnh gốc. Đây là cách nhanh nhất để **tạo file PSD ảnh âm bản** hoặc đạt được hiệu ứng phim âm bản cổ điển.

## Tại sao nên sử dụng Aspose.PSD làm thư viện xử lý ảnh java của bạn?

Aspose.PSD hỗ trợ **hơn 200 tính năng PSD**, có thể đọc và ghi các tệp Photoshop mà không cần Photoshop, và xử lý các tài liệu hàng trăm trang sử dụng dưới 500 MB bộ nhớ heap. Nó chạy trên bất kỳ môi trường Java nào (Java 6+), làm cho nó trở thành lựa chọn lý tưởng cho **batch process psd images** trên các máy chủ Windows, Linux hoặc macOS.

## Yêu cầu trước

1. **Aspose.PSD for Java** – tải xuống JAR mới nhất từ trang chính thức [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 hoặc mới hơn đã được cài đặt và cấu hình trong `PATH` của bạn.  

Bây giờ bạn đã sẵn sàng viết mã.

## Nhập các gói

Lớp `PsdImage` đại diện cho toàn bộ tài liệu Photoshop trong bộ nhớ, trong khi các lớp lớp điều chỉnh nằm trong gói `com.aspose.psd.layers.adjustments`.

Lớp `PsdImage` là đối tượng cấp cao nhất của Aspose.PSD, bao gói cấu trúc và dữ liệu pixel của tệp PSD. Nhập các namespace, sau đó bạn sẽ có thể tải, chỉnh sửa và lưu các tệp PSD.

## Bước 1: thiết lập thư mục tài liệu

Xác định thư mục chứa tệp PSD nguồn của bạn và nơi sẽ lưu kết quả. Sử dụng đường dẫn tuyệt đối tránh `NullPointerException` khi thư mục làm việc thay đổi.

## Bước 2: tải tệp PSD

Tải tệp nguồn vào một đối tượng `PsdImage`. Đối tượng này giữ toàn bộ cấu trúc lớp trong bộ nhớ, cho phép chỉnh sửa không phá hủy.

Lớp `PsdImage` cung cấp phương thức tĩnh `load` đọc tiêu đề tệp, xác thực định dạng và tạo ra một biểu diễn trong bộ nhớ sẵn sàng cho việc thao tác.

## Bước 3: thêm lớp điều chỉnh Đảo ngược

Gọi phương thức tích hợp để chèn một Invert Adjustment Layer lên đầu ngăn xếp lớp hiện tại. Bạn có thể sau này thêm nhiều lớp hơn (ví dụ: Brightness, Hue) để **apply multiple adjustment layers** trong một quy trình duy nhất.

`addInvertAdjustmentLayer()` thêm một Invert Adjustment Layer vào bộ sưu tập lớp của PSD.

## Bước 4: lưu kết quả

Lưu PSD đã chỉnh sửa vào đĩa.

`save()` ghi tệp PSD, bao gồm tất cả các lớp và siêu dữ liệu, vào đường dẫn đã chỉ định.

Việc lưu sử dụng cùng phương thức `save` ghi toàn bộ tài liệu, bao gồm tất cả các lớp điều chỉnh, mặt nạ và siêu dữ liệu, vào định dạng đã chỉ định.

### Điều gì vừa xảy ra?

Tệp PSD đã được tải vào một đối tượng `PsdImage`, một `InvertAdjustmentLayer` được tạo và thêm vào làm lớp trên cùng, và tài liệu đã được lưu. Trình tự này bảo tồn dữ liệu ảnh gốc trong khi thêm hiệu ứng đảo ngược không phá hủy, có thể bật/tắt hoặc thay đổi thứ tự sau này.

Bây giờ bạn đã thành công sử dụng Aspose.PSD, một **image processing java library**, để thao tác với tệp PSD.

## Cách xử lý hàng loạt ảnh PSD với điều chỉnh đảo ngược?

Tải mỗi tệp trong một vòng lặp `for`, áp dụng các bước giống nhau, và gọi `save` cho mỗi lần lặp. Vì Aspose.PSD xử lý tệp theo dạng luồng, bạn có thể xử lý **hundreds of PSDs** trong khi giữ mức sử dụng bộ nhớ dưới 300 MB bằng cách tái sử dụng cùng một thể hiện `PsdImage`.

## Cách chuyển đổi PSD thành ảnh âm bản?

Thêm Invert Adjustment Layer làm mục trên cùng và lưu tài liệu – thao tác này tương đương với **convert PSD to negative**. Bạn có thể sau này tắt hoặc xóa lớp để quay lại giao diện gốc mà không cần tải lại tệp nguồn.

## Các vấn đề thường gặp & mẹo

| Issue | Cause | Solution |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | Đường dẫn tệp không đúng hoặc tệp bị thiếu | Xác minh `dataDir` và tên tệp; sử dụng đường dẫn tuyệt đối để kiểm tra |
| **Layer order not as expected** | Thêm lớp sau các lớp hiện có làm thay đổi thứ tự xếp chồng | Chèn lớp đảo ngược trước các điều chỉnh khác, hoặc thay đổi thứ tự bằng `psdImage.getLayers().move()` |
| **Performance slowdown on large PSDs** | Tải các tệp rất lớn vào bộ nhớ | Tăng bộ nhớ heap JVM (`-Xmx2g`) hoặc xử lý tệp theo từng phần bằng `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` |

## Câu hỏi thường gặp

**Q: Aspose.PSD có tương thích với tất cả các phiên bản Java không?**  
A: Có, nó hỗ trợ Java 6.0 và các phiên bản sau, bao gồm Java 8, 11 và 17.

**Q: Tôi có thể áp dụng nhiều lớp điều chỉnh trong một thao tác duy nhất không?**  
A: Chắc chắn. Sau khi thêm lớp đảo ngược, bạn có thể gọi `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()`, v.v., để xếp chồng các hiệu ứng.

**Q: Tôi có thể tìm tài liệu API đầy đủ ở đâu?**  
A: Tài liệu đầy đủ có sẵn tại [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: Có bản dùng thử miễn phí cho Aspose.PSD không?**  
A: Có, bạn có thể tải phiên bản dùng thử [Aspose.PSD trial download](https://releases.aspose.com/).

**Q: Làm thế nào để tôi nhận được giấy phép tạm thời để thử nghiệm?**  
A: Yêu cầu giấy phép tạm thời [temporary license request page](https://purchase.aspose.com/temporary-license/).

**Cập nhật lần cuối:** 2026-11-04  
**Kiểm tra với:** Aspose.PSD 24.12 for Java  
**Tác giả:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## Hướng dẫn liên quan

- [Thêm lớp Điều chỉnh Level vào tệp PSD với Aspose.PSD cho Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [Cách thêm lớp Điều chỉnh – Channel Mixer trong PSD (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [Cách chỉnh sửa PSD - Thêm lớp Điều chỉnh Curves bằng Java](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}