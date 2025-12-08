---
date: 2025-12-08
description: Học cách chuyển đổi PSD sang PNG và thay đổi kích thước ảnh một cách
  tỷ lệ trong Java bằng Aspose.PSD. Hướng dẫn từng bước này bao gồm việc lưu trữ bộ
  nhớ đệm ảnh, thay đổi kích thước và lưu dưới dạng PNG.
language: vi
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Cách chuyển đổi PSD sang PNG và thay đổi kích thước tỷ lệ với Aspose.PSD cho
  Java
url: /java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Chuyển Đổi PSD sang PNG và Thay Đổi Kích Thước Tỷ Lệ với Aspose.PSD cho Java

## Giới thiệu

Nếu bạn cần **chuyển đổi PSD sang PNG** trong khi giữ nguyên tỷ lệ khung hình gốc, bạn đã đến đúng nơi. Trong hướng dẫn này, chúng tôi sẽ trình bày một **bài học Aspose.PSD** đầy đủ cho thấy **cách thay đổi kích thước ảnh** một cách tỷ lệ trong Java, lưu trữ ảnh để tối ưu hiệu năng, và cuối cùng lưu kết quả dưới dạng PNG. Khi hoàn thành, bạn sẽ có thể tích hợp quy trình này vào bất kỳ pipeline xử lý ảnh nào dựa trên Java.

## Câu trả lời nhanh
- **Aspose.PSD có thể chuyển đổi PSD sang PNG không?** Có – chỉ cần tải PSD và lưu với `PngOptions`.
- **Thư viện có hỗ trợ thay đổi kích thước tỷ lệ không?** Chắc chắn; sử dụng `resizeWidthProportionally` và `resizeHeightProportionally`.
- **Có cần phải cache ảnh trước không?** Caching (`image.cacheData()`) cải thiện hiệu năng cho các tệp PSD lớn.
- **Yêu cầu phiên bản Java nào?** Java 8 hoặc mới hơn được hỗ trợ đầy đủ.
- **Cần giấy phép cho môi trường production không?** Có, giấy phép thương mại loại bỏ watermark đánh giá.

## “Chuyển đổi PSD sang PNG” là gì và tại sao lại quan trọng?

Việc chuyển đổi tài liệu Photoshop (PSD) sang tệp Portable Network Graphics (PNG) cho phép bạn chia sẻ các thiết kế có lớp dưới dạng định dạng nhẹ, thân thiện với web. PNG giữ được độ trong suốt và chất lượng không mất dữ liệu, làm cho nó lý tưởng cho các tài sản UI, thumbnail, hoặc bất kỳ trường hợp nào mà độ trung thực của ảnh quan trọng.

## Tại sao cần thay đổi kích thước ảnh tỷ lệ trong Java?

Thay đổi kích thước **cách thay đổi kích thước ảnh** mà không làm biến dạng tỷ lệ khung hình đảm bảo đồ họa trông tự nhiên trên các màn hình khác nhau. API `Aspose.PSD` cung cấp các phương thức dành riêng cho việc thu phóng tỷ lệ, tự động tính toán chiều cao hoặc chiều rộng phù hợp, giúp bạn tránh các lỗi tính toán thủ công.

## Yêu cầu trước

Trước khi chúng ta bắt đầu viết mã, hãy chắc chắn rằng bạn đã có:

1. **Java Development Kit (JDK)** – Java 8 hoặc phiên bản mới hơn đã được cài đặt.
2. **Aspose.PSD for Java** – tải JAR mới nhất từ trang chính thức [here](https://releases.aspose.com/psd/java/).
3. Một tệp PSD mẫu (`sample.psd`) được đặt trong thư mục mà bạn có thể tham chiếu từ dự án.

## Nhập khẩu các gói

Thêm các import cần thiết vào lớp Java của bạn. Những lớp này cho phép bạn tải ảnh, cache, thay đổi kích thước và xuất ra PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Bước 1: Tải ảnh PSD

Đầu tiên, tải tệp PSD nguồn. Nếu tệp lớn, việc cache dữ liệu ảnh sẽ giảm tải bộ nhớ khi bạn thực hiện các thao tác tiếp theo.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Bước 2: Thay đổi kích thước ảnh tỷ lệ (Java)

Bây giờ quyết định kích thước mới. Trong ví dụ này, chúng ta thu nhỏ ảnh xuống **một nửa** kích thước gốc trong khi vẫn giữ tỷ lệ khung hình. Bạn có thể điều chỉnh chiều rộng hoặc chiều cao mục tiêu tùy ý.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Mẹo chuyên nghiệp:** Sử dụng `resizeWidthProportionally` *hoặc* `resizeHeightProportionally`—thư viện sẽ tự động tính toán kích thước còn lại để giữ ảnh tỷ lệ.

## Bước 3: Lưu ảnh đã thay đổi kích thước dưới dạng PNG

Cuối cùng, xuất ảnh đã thay đổi kích thước sang định dạng PNG. Bước này hoàn thành quy trình **chuyển đổi PSD sang PNG**.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Khi mã chạy, bạn sẽ thấy một tệp PNG có kích thước bằng một nửa tệp PSD gốc, với chất lượng hình ảnh tương tự và không bị biến dạng.

## Các vấn đề thường gặp & Giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|----------|
| **OutOfMemoryError** | PSD lớn chưa được cache | Gọi `image.cacheData()` trước khi thay đổi kích thước |
| **Blank PNG output** | Đường dẫn tệp không đúng | Kiểm tra `dataDir` và quyền ghi |
| **Aspect ratio looks off** | Sử dụng cả chiều rộng và chiều cao một cách thủ công | Sử dụng các phương thức tỷ lệ được cung cấp bởi Aspose.PSD |

## Câu hỏi thường gặp

**Q: Aspose.PSD có tương thích với mọi định dạng ảnh không?**  
A: Aspose.PSD hỗ trợ PSD, PNG, JPEG, BMP, GIF và nhiều hơn nữa. Xem danh sách đầy đủ trong [documentation](https://reference.aspose.com/psd/java/).

**Q: Tôi có thể sử dụng Aspose.PSD cho các dự án thương mại không?**  
A: Có. Mua giấy phép thương mại tại [Aspose store](https://purchase.aspose.com/buy).

**Q: Có giấy phép tạm thời cho việc thử nghiệm không?**  
A: Chắc chắn – yêu cầu giấy phép tạm thời [here](https://purchase.aspose.com/temporary-license/) cho mục đích đánh giá.

**Q: Tôi có thể tìm hỗ trợ cộng đồng ở đâu?**  
A: Diễn đàn [Aspose.PSD](https://forum.aspose.com/c/psd/34) là nơi tuyệt vời để đặt câu hỏi và chia sẻ giải pháp.

**Q: Làm sao để truy cập tài liệu API đầy đủ?**  
A: Tài liệu API chi tiết có sẵn [here](https://reference.aspose.com/psd/java/).

## Kết luận

Bạn đã biết cách **chuyển đổi PSD sang PNG**, thay đổi kích thước ảnh một cách tỷ lệ, và xử lý cache hiệu quả bằng Aspose.PSD cho Java. Hãy tích hợp các bước này vào ứng dụng của mình để cung cấp xử lý ảnh nhanh, chất lượng cao mà không cần cài đặt Photoshop gốc.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-08  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose