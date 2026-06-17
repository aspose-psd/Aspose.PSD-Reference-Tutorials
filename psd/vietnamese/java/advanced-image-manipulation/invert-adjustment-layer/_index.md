---
date: 2026-04-22
description: Tìm hiểu cách sử dụng thư viện xử lý ảnh Java Aspose.PSD để áp dụng nhiều
  lớp điều chỉnh, bao gồm lớp điều chỉnh Đảo ngược, cho việc thao tác PSD mượt mà.
keywords:
- image processing java library
- how to add invert
- invert colors psd
- batch process psd images
- apply multiple adjustment layers
linktitle: Lớp điều chỉnh Đảo ngược
second_title: Aspose.PSD Java API
title: 'Thư viện Java xử lý ảnh: Đảo ngược lớp bằng Aspose.PSD'
url: /vi/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lớp Điều Chỉnh Đảo Ngược trong Aspose.PSD cho Java

## Giới thiệu

Nếu bạn đang tìm kiếm một **image processing java library** mạnh mẽ, Aspose.PSD cho Java là một trong những lựa chọn đa năng nhất trên thị trường. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn cách thêm một **Invert Adjustment Layer** vào tệp PSD, một kỹ thuật mà bạn có thể kết hợp với các lớp điều chỉnh khác để đạt được các hiệu ứng hình ảnh tinh vi. Dù bạn đang xây dựng công cụ xử lý hàng loạt, dịch vụ ảnh phía máy chủ, hay trình chỉnh sửa ảnh đơn lẻ, hướng dẫn này cung cấp cho bạn một lộ trình rõ ràng, từng bước để hoàn thành công việc nhanh chóng và đáng tin cậy.

## Câu trả lời nhanh
- **What does the Invert Adjustment Layer do?** Nó đảo ngược tất cả các giá trị màu trong khu vực đã chọn, tạo hiệu ứng ảnh âm (tức là nó **converts PSD to negative**).  
- **Which library provides this feature?** Aspose.PSD, một **image processing java library** hàng đầu.  
- **Can I stack it with other adjustments?** Có – bạn có thể **apply multiple adjustment layers** như Brightness/Contrast, Hue/Saturation, và các thứ khác.  
- **Do I need a license for development?** Có bản dùng thử miễn phí; giấy phép cần thiết cho việc sử dụng trong môi trường sản xuất.  
- **How long does the implementation take?** Thông thường dưới 10 phút cho trường hợp sử dụng cơ bản.

## Lớp Điều Chỉnh Đảo Ngược là gì?

Lớp Điều Chỉnh Đảo Ngược là một chỉnh sửa không phá hủy, đảo ngược các giá trị RGB của mỗi pixel mà nó ảnh hưởng. Vì nó nằm trên đỉnh của ngăn xếp lớp, bạn có thể bật/tắt hiển thị hoặc sắp xếp lại mà không làm thay đổi vĩnh viễn dữ liệu ảnh gốc. Đây là cách dễ nhất để **invert colors PSD** các tệp hoặc tạo một ảnh âm.

## Tại sao nên sử dụng Aspose.PSD làm Thư viện Xử lý Ảnh Java của bạn?

- **Full PSD support** – đọc, chỉnh sửa và ghi các tệp Photoshop mà không cần cài đặt Photoshop.  
- **Cross‑platform** – hoạt động trên bất kỳ môi trường Java nào (Java 6+).  
- **Rich adjustment features** – bao gồm các phương thức tích hợp cho nhiều chỉnh sửa phổ biến, giúp dễ dàng **apply multiple adjustment layers** trong một quy trình làm việc duy nhất.  
- **Performance‑optimized** – xử lý các tệp lớn một cách hiệu quả, điều này rất quan trọng cho **batch process psd images**.  

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn bạn có những thứ sau:

1. **Aspose.PSD Library** – tải xuống từ trang chính thức [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – JDK 6.0 hoặc mới hơn đã được cài đặt và cấu hình.  

Bây giờ, chúng ta hãy đi vào phần mã.

## Nhập khẩu Gói

Bắt đầu bằng việc nhập các lớp cần thiết. Các import này cho phép bạn truy cập vào các API xử lý ảnh cốt lõi và chức năng đặc thù của PSD.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Bước 1: Thiết lập Thư mục Tài liệu

Xác định thư mục chứa tệp PSD nguồn của bạn và nơi sẽ lưu kết quả.

```java
String dataDir = "Your Document Directory";
```

## Bước 2: Tải tệp PSD

Tải tệp nguồn vào một đối tượng `PsdImage`. Đối tượng này đại diện cho toàn bộ tài liệu PSD trong bộ nhớ.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Bước 3: Thêm Lớp Điều Chỉnh Đảo Ngược

Gọi phương thức tích hợp để chèn một **Invert Adjustment Layer** lên trên ngăn xếp lớp hiện tại. Bạn có thể sau này thêm nhiều lớp hơn (ví dụ: Brightness, Hue) để **apply multiple adjustment layers**.

```java
im.addInvertAdjustmentLayer();
```

## Bước 4: Lưu Kết quả

Lưu PSD đã chỉnh sửa vào đĩa. Tệp đã lưu hiện chứa **Invert Adjustment Layer** và có thể mở trong Photoshop hoặc bất kỳ trình xem PSD nào tương thích.

```java
im.save(outputPath);
```

### Điều gì vừa xảy ra?

- PSD đã được tải vào bộ nhớ.  
- Một **Invert Adjustment Layer** đã được thêm làm lớp trên cùng.  
- Ảnh đã được lưu, giữ nguyên chỉnh sửa không phá hủy.

Bạn đã thành công sử dụng Aspose.PSD, một **image processing java library**, để thao tác với tệp PSD.

## Xử lý hàng loạt ảnh PSD với điều chỉnh đảo ngược

Nếu bạn cần áp dụng cùng một hiệu ứng đảo ngược cho hàng chục hoặc hàng trăm tệp, bạn có thể đặt đoạn mã trên vào một vòng lặp đơn giản duyệt qua một thư mục chứa các PSD. Vì thư viện này **performance‑optimized**, việc xử lý các lô lớn vẫn nhanh, và bạn có thể kết hợp bước đảo ngược với các điều chỉnh khác (ví dụ: brightness, hue) trong cùng một vòng lặp.

## Chuyển đổi PSD thành ảnh âm

Lớp Điều Chỉnh Đảo Ngược thực chất là thao tác **convert PSD to negative**. Bằng cách thêm lớp này làm mục trên cùng, bạn đạt được hiệu ứng âm toàn phần mà không làm thay đổi vĩnh viễn dữ liệu pixel gốc. Bạn có thể sau này xóa hoặc tắt lớp để quay lại hình ảnh ban đầu.

## Các vấn đề thường gặp & Mẹo

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|-----------|
| **NullPointerException on `Image.load`** | Đường dẫn tệp không đúng hoặc tệp thiếu | Xác minh `dataDir` và tên tệp; sử dụng đường dẫn tuyệt đối để thử nghiệm |
| **Layer order not as expected** | Thêm lớp sau các lớp hiện có làm thay đổi thứ tự xếp chồng | Sử dụng `im.addInvertAdjustmentLayer()` trước khi thêm các điều chỉnh khác, hoặc sắp xếp lại các lớp qua `im.getLayers()` |
| **Performance slowdown on large PSDs** | Tải các tệp rất lớn vào bộ nhớ | Xem xét xử lý các trang theo từng phần hoặc tăng kích thước heap JVM (`-Xmx2g`) |

## Câu hỏi thường gặp

**Q: Aspose.PSD có tương thích với mọi phiên bản Java không?**  
A: Aspose.PSD hỗ trợ Java 6.0 và các phiên bản sau.

**Q: Tôi có thể áp dụng nhiều lớp điều chỉnh trong một thao tác duy nhất không?**  
A: Có, bạn có thể xếp chồng nhiều lớp điều chỉnh—như Invert, Brightness và Hue/Saturation—để đạt được các hiệu ứng phức tạp.

**Q: Tôi có thể tìm tài liệu bổ sung cho Aspose.PSD ở đâu?**  
A: Tham khảo tài liệu [here](https://reference.aspose.com/psd/java/) để có hướng dẫn chi tiết và tham chiếu API.

**Q: Có bản dùng thử miễn phí cho Aspose.PSD không?**  
A: Có, bạn có thể khám phá bản dùng thử miễn phí [here](https://releases.aspose.com/).

**Q: Làm thế nào tôi có thể nhận giấy phép tạm thời cho Aspose.PSD?**  
A: Bạn có thể nhận giấy phép tạm thời [here](https://purchase.aspose.com/temporary-license/).

**Last Updated:** 2026-04-22  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}