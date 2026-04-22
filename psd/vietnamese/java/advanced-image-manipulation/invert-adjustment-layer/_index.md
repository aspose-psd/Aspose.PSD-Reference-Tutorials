---
date: 2026-02-07
description: Tìm hiểu cách sử dụng thư viện xử lý ảnh Java Aspose.PSD để áp dụng nhiều
  lớp điều chỉnh, bao gồm Lớp Điều chỉnh Đảo ngược, nhằm thao tác PSD một cách liền
  mạch.
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'Thư viện Java xử lý ảnh: Đảo ngược lớp bằng Aspose.PSD'
url: /vi/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lớp Điều Chỉnh Đảo Ngược (Invert Adjustment Layer) trong Aspose.PSD cho Java

## Giới thiệu

Nếu bạn đang tìm kiếm một **thư viện xử lý ảnh java** mạnh mẽ, Aspose.PSD cho Java là một trong những lựa chọn đa năng nhất trên thị trường. Trong hướng dẫn này, chúng ta sẽ đi qua cách thêm **Lớp Điều Chỉnh Đảo Ngược** vào tệp PSD, một kỹ thuật bạn có thể kết hợp với các lớp điều chỉnh khác để tạo ra các hiệu ứng hình ảnh tinh vi. Dù bạn đang xây dựng công cụ xử lý hàng loạt hay trình chỉnh sửa ảnh đơn lẻ, hướng dẫn này cung cấp cho bạn một lộ trình rõ ràng, từng bước để hoàn thành công việc một cách nhanh chóng.

## Trả Lời Nhanh
- **Lớp Điều Chỉnh Đảo Ngược làm gì?** Nó đảo ngược tất cả các giá trị màu trong khu vực được chọn, tạo hiệu ứng ảnh âm bản.  
- **Thư viện nào cung cấp tính năng này?** Aspose.PSD, một thư viện xử lý ảnh java hàng đầu.  
- **Tôi có thể xếp chồng nó với các điều chỉnh khác không?** Có – bạn có thể **áp dụng nhiều lớp điều chỉnh** như Brightness/Contrast, Hue/Saturation, và nhiều hơn nữa.  
- **Có cần giấy phép để phát triển không?** Có bản dùng thử miễn phí; giấy phép bắt buộc đối với môi trường sản xuất.  
- **Thời gian triển khai mất bao lâu?** Thông thường dưới 10 phút cho một trường hợp sử dụng cơ bản.

## Lớp Điều Chỉnh Đảo Ngược là gì?

Lớp Điều Chỉnh Đảo Ngược là một chỉnh sửa không phá hủy, đảo ngược các giá trị RGB của mỗi pixel mà nó ảnh hưởng. Vì nó nằm trên đỉnh của ngăn xếp lớp, bạn có thể bật/tắt hiển thị hoặc thay đổi vị trí mà không làm thay đổi dữ liệu ảnh gốc.

## Cách đảo ngược lớp bằng Aspose.PSD

Dưới đây là cách **đảo ngược lớp** trong một tệp PSD. Các bước được trình bày đơn giản để bạn tập trung vào khái niệm hơn là mã mẫu.

## Tại sao nên sử dụng Aspose.PSD làm Thư viện Xử lý Ảnh Java của bạn?

- **Hỗ trợ PSD đầy đủ** – đọc, chỉnh sửa và ghi các tệp Photoshop mà không cần cài Photoshop.  
- **Đa nền tảng** – hoạt động trên bất kỳ môi trường Java nào (Java 6+).  
- **Tính năng điều chỉnh phong phú** – bao gồm các phương thức tích hợp cho nhiều chỉnh sửa phổ biến, giúp dễ dàng **áp dụng nhiều lớp điều chỉnh** trong một quy trình làm việc.  
- **Tối ưu hiệu năng** – xử lý các tệp lớn một cách hiệu quả, rất cần thiết cho việc xử lý hàng loạt.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn bạn đã có:

1. **Thư viện Aspose.PSD** – tải về từ trang chính thức [ở đây](https://releases.aspose.com/psd/java/).  
2. **Môi trường phát triển Java** – JDK 6.0 hoặc mới hơn đã được cài đặt và cấu hình.  

Bây giờ, chúng ta cùng xem mã nguồn.

## Nhập Gói

Bắt đầu bằng việc nhập các lớp cần thiết. Các import này cho phép bạn truy cập vào API xử lý ảnh cốt lõi và các chức năng đặc thù của PSD.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Bước 1: Thiết lập Thư mục Tài liệu

Xác định thư mục chứa tệp PSD nguồn và nơi sẽ lưu tệp đầu ra.

```java
String dataDir = "Your Document Directory";
```

## Bước 2: Tải Tệp PSD

Tải tệp nguồn vào đối tượng `PsdImage`. Đối tượng này đại diện cho toàn bộ tài liệu PSD trong bộ nhớ.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Bước 3: Thêm Lớp Điều Chỉnh Đảo Ngược

Gọi phương thức tích hợp để chèn một Lớp Điều Chỉnh Đảo Ngược lên đầu ngăn xếp lớp hiện tại. Bạn có thể sau này thêm các lớp khác (ví dụ: Brightness, Hue) để **áp dụng nhiều lớp điều chỉnh**.

```java
im.addInvertAdjustmentLayer();
```

## Bước 4: Lưu Kết Quả

Ghi lại PSD đã chỉnh sửa ra đĩa. Tệp đã lưu bây giờ chứa Lớp Điều Chỉnh Đảo Ngược và có thể mở trong Photoshop hoặc bất kỳ trình xem PSD nào tương thích.

```java
im.save(outputPath);
```

### Điều gì vừa xảy ra?

- PSD đã được tải vào bộ nhớ.  
- Một Lớp Điều Chỉnh Đảo Ngược đã được thêm vào vị trí trên cùng.  
- Ảnh đã được lưu, giữ nguyên chỉnh sửa không phá hủy.

Bạn đã thành công trong việc sử dụng Aspose.PSD, một **thư viện xử lý ảnh java**, để thao tác với tệp PSD.

## Các Vấn Đề Thường Gặp & Mẹo

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|-----------|
| **NullPointerException khi `Image.load`** | Đường dẫn tệp không đúng hoặc tệp thiếu | Kiểm tra `dataDir` và tên tệp; dùng đường dẫn tuyệt đối khi thử nghiệm |
| **Thứ tự lớp không như mong đợi** | Thêm lớp sau các lớp hiện có làm thay đổi vị trí xếp chồng | Dùng `im.addInvertAdjustmentLayer()` trước khi thêm các điều chỉnh khác, hoặc sắp xếp lại lớp bằng `im.getLayers()` |
| **Chậm hiệu năng với PSD lớn** | Tải các tệp rất lớn vào bộ nhớ | Xem xét xử lý từng phần hoặc tăng kích thước heap JVM (`-Xmx2g`) |

## Câu Hỏi Thường Gặp

**H: Aspose.PSD có tương thích với mọi phiên bản Java không?**  
Đ: Aspose.PSD hỗ trợ Java 6.0 và các phiên bản sau đó.

**H: Tôi có thể áp dụng nhiều lớp điều chỉnh trong một thao tác không?**  
Đ: Có, bạn có thể xếp chồng nhiều lớp điều chỉnh—như Đảo Ngược, Brightness, và Hue/Saturation—để đạt được các hiệu ứng phức tạp.

**H: Tôi có thể tìm tài liệu bổ sung cho Aspose.PSD ở đâu?**  
Đ: Tham khảo tài liệu [ở đây](https://reference.aspose.com/psd/java/) để có hướng dẫn chi tiết và tham chiếu API.

**H: Có bản dùng thử miễn phí cho Aspose.PSD không?**  
Đ: Có, bạn có thể khám phá bản dùng thử [ở đây](https://releases.aspose.com/).

**H: Làm sao để lấy giấy phép tạm thời cho Aspose.PSD?**  
Đ: Bạn có thể nhận giấy phép tạm thời [ở đây](https://purchase.aspose.com/temporary-license/).

---

**Cập nhật lần cuối:** 2026-02-07  
**Đã kiểm thử với:** Aspose.PSD 24.12 cho Java  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}