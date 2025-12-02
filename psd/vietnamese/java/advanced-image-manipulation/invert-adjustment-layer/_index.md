---
date: 2025-12-02
description: Tìm hiểu cách sử dụng thư viện xử lý ảnh Java Aspose.PSD để áp dụng nhiều
  lớp điều chỉnh, bao gồm lớp điều chỉnh Đảo ngược, nhằm thao tác PSD một cách liền
  mạch.
language: vi
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'Thư viện Java xử lý ảnh: Đảo ngược lớp bằng Aspose.PSD'
url: /java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lớp Điều Chỉnh Đảo Ngược trong Aspose.PSD cho Java

## Giới thiệu

Nếu bạn đang tìm kiếm một **image processing java library** mạnh mẽ, Aspose.PSD cho Java là một trong những lựa chọn đa năng nhất trên thị trường. Trong hướng dẫn này, chúng ta sẽ đi qua cách thêm một **Invert Adjustment Layer** vào tệp PSD, một kỹ thuật bạn có thể kết hợp với các lớp điều chỉnh khác để đạt được các hiệu ứng hình ảnh tinh vi. Dù bạn đang xây dựng một công cụ xử lý hàng loạt hay một trình chỉnh sửa ảnh đơn lẻ, hướng dẫn này cung cấp cho bạn một lộ trình rõ ràng, từng bước để hoàn thành công việc nhanh chóng.

## Câu trả lời nhanh
- **Lớp Điều Chỉnh Đảo Ngược làm gì?** Nó đảo ngược tất cả các giá trị màu trong khu vực được chọn, tạo hiệu ứng ảnh âm bản.  
- **Thư viện nào cung cấp tính năng này?** Aspose.PSD, một **image processing java library** hàng đầu.  
- **Tôi có thể xếp chồng nó với các điều chỉnh khác không?** Có – bạn có thể **apply multiple adjustment layers** như Brightness/Contrast, Hue/Saturation, và nhiều hơn nữa.  
- **Tôi có cần giấy phép để phát triển không?** Có bản dùng thử miễn phí; giấy phép bắt buộc cho việc sử dụng trong môi trường sản xuất.  
- **Thời gian triển khai mất bao lâu?** Thông thường dưới 10 phút cho một trường hợp sử dụng cơ bản.

## Lớp Điều Chỉnh Đảo Ngược là gì?

Lớp Điều Chỉnh Đảo Ngược là một chỉnh sửa không phá hủy (non‑destructive) làm đảo ngược các giá trị RGB của mỗi pixel mà nó ảnh hưởng. Vì nó nằm trên đỉnh của ngăn xếp lớp, bạn có thể bật/tắt hiển thị hoặc thay đổi vị trí mà không làm thay đổi dữ liệu ảnh gốc.

## Tại sao nên dùng Aspose.PSD làm thư viện Image Processing Java của bạn?

- **Hỗ trợ PSD đầy đủ** – đọc, chỉnh sửa và ghi các tệp Photoshop mà không cần cài Photoshop.  
- **Đa nền tảng** – hoạt động trên bất kỳ môi trường Java nào (Java 6+).  
- **Tính năng điều chỉnh phong phú** – bao gồm các phương thức tích hợp cho nhiều chỉnh sửa phổ biến, giúp bạn dễ dàng **apply multiple adjustment layers** trong một quy trình làm việc duy nhất.  
- **Tối ưu hiệu năng** – xử lý các tệp lớn một cách hiệu quả, rất cần thiết cho việc xử lý hàng loạt.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn bạn đã có:

1. **Thư viện Aspose.PSD** – tải về từ trang chính thức [here](https://releases.aspose.com/psd/java/).  
2. **Môi trường phát triển Java** – JDK 6.0 hoặc mới hơn đã được cài đặt và cấu hình.  

Bây giờ, chúng ta sẽ đi vào phần mã.

## Nhập các gói cần thiết

Bắt đầu bằng cách nhập các lớp cần thiết. Những import này cho phép bạn truy cập vào các API xử lý ảnh cốt lõi và chức năng đặc thù của PSD.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Bước 1: Thiết lập thư mục tài liệu

Xác định thư mục chứa tệp PSD nguồn và nơi sẽ lưu kết quả.

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

Gọi phương thức tích hợp để chèn một Invert Adjustment Layer lên trên ngăn xếp lớp hiện tại. Bạn có thể sau này thêm các lớp khác (ví dụ: Brightness, Hue) để **apply multiple adjustment layers**.

```java
im.addInvertAdjustmentLayer();
```

## Bước 4: Lưu kết quả

Ghi lại tệp PSD đã chỉnh sửa ra đĩa. Tệp đã lưu bây giờ chứa Lớp Điều Chỉnh Đảo Ngược và có thể mở trong Photoshop hoặc bất kỳ trình xem PSD nào tương thích.

```java
im.save(outputPath);
```

### Điều gì vừa xảy ra?

- PSD đã được tải vào bộ nhớ.  
- Một Invert Adjustment Layer đã được thêm vào vị trí trên cùng.  
- Ảnh đã được lưu, giữ nguyên chỉnh sửa không phá hủy.

Bạn đã thành công trong việc sử dụng Aspose.PSD, một **image processing java library**, để thao tác với tệp PSD.

## Các vấn đề thường gặp & Mẹo

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|-----------|
| **NullPointerException trên `Image.load`** | Đường dẫn tệp không đúng hoặc tệp không tồn tại | Kiểm tra lại `dataDir` và tên tệp; dùng đường dẫn tuyệt đối khi thử nghiệm |
| **Thứ tự lớp không như mong đợi** | Thêm lớp sau các lớp hiện có làm thay đổi vị trí xếp chồng | Dùng `im.addInvertAdjustmentLayer()` trước khi thêm các điều chỉnh khác, hoặc sắp xếp lại lớp qua `im.getLayers()` |
| **Chậm hiệu năng khi xử lý PSD lớn** | Tải các tệp rất lớn vào bộ nhớ | Xem xét xử lý từng phần hoặc tăng kích thước heap JVM (`-Xmx2g`) |

## Câu hỏi thường gặp

**Q: Aspose.PSD có tương thích với mọi phiên bản Java không?**  
A: Aspose.PSD hỗ trợ Java 6.0 và các phiên bản sau đó.

**Q: Tôi có thể áp dụng nhiều lớp điều chỉnh trong một thao tác không?**  
A: Có, bạn có thể xếp chồng nhiều lớp điều chỉnh—như Invert, Brightness, và Hue/Saturation—để đạt hiệu ứng phức tạp.

**Q: Tôi có thể tìm tài liệu bổ sung cho Aspose.PSD ở đâu?**  
A: Tham khảo tài liệu [here](https://reference.aspose.com/psd/java/) để có các hướng dẫn chi tiết và tham chiếu API.

**Q: Có bản dùng thử miễn phí cho Aspose.PSD không?**  
A: Có, bạn có thể khám phá bản dùng thử [here](https://releases.aspose.com/).

**Q: Làm sao để lấy giấy phép tạm thời cho Aspose.PSD?**  
A: Bạn có thể nhận giấy phép tạm thời [here](https://purchase.aspose.com/temporary-license/).

---

**Cập nhật lần cuối:** 2025-12-02  
**Được kiểm tra với:** Aspose.PSD 24.12 cho Java  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}