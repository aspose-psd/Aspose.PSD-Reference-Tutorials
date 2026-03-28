---
date: 2026-03-28
description: Tìm hiểu cách tạo lớp PSD mới và quản lý thời gian tạo của nó bằng Aspose.PSD
  cho Java. Hướng dẫn từng bước này bao gồm việc tải, đọc, xác thực và thêm các lớp.
linktitle: Create New PSD Layer and Manage Creation DateTime in Java
second_title: Aspose.PSD Java API
title: Tạo Lớp PSD Mới và Quản Lý Thời Gian Tạo trong Java
url: /vi/java/psd-image-modification-conversion/manage-layer-creation-datetime-psd/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo Lớp PSD Mới và Quản Lý Thời Gian Tạo trong Java

## Giới thiệu
Khi bạn làm việc với các tệp Photoshop (PSD) một cách lập trình, khả năng **tạo lớp PSD mới** và theo dõi thời gian tạo của chúng thực sự là một bước đột phá. Dù bạn đang xây dựng hệ thống kiểm soát phiên bản cho tài sản thiết kế, tự động hoá các chỉnh sửa hàng loạt, hay chỉ cần một dấu vết kiểm toán cho các dự án hợp tác, việc biết cách đọc và đặt ngày tạo của lớp giúp bạn duy trì nguồn gốc đầy đủ của mọi thay đổi. Trong hướng dẫn này, chúng ta sẽ đi qua toàn bộ quy trình sử dụng Aspose.PSD cho Java — từ tải PSD, lấy ngày tạo của lớp, xác thực, đến cuối cùng là thêm một lớp điều chỉnh hoàn toàn mới.

## Câu trả lời nhanh
- **Thư viện nào xử lý tệp PSD trong Java?** Aspose.PSD for Java  
- **Tôi có thể đọc ngày tạo của lớp không?** Có, bằng cách sử dụng `layer.getLayerCreationDateTime()`  
- **Có thể thêm một lớp điều chỉnh mới không?** Chắc chắn – `im.addLevelsAdjustmentLayer()` tạo ra một lớp  
- **Tôi có cần giấy phép cho việc sử dụng trong môi trường sản xuất không?** Cần giấy phép thương mại cho các triển khai không dùng bản thử nghiệm  
- **Phiên bản Java nào được hỗ trợ?** JDK 8 hoặc mới hơn  

## “Tạo lớp PSD mới” là gì?
Tạo một lớp PSD mới có nghĩa là chèn một đối tượng lớp mới một cách lập trình — chẳng hạn như lớp điều chỉnh, lớp văn bản hoặc lớp pixel — vào một tài liệu PSD hiện có. Thao tác này cho phép bạn mở rộng hoặc chỉnh sửa hình ảnh mà không cần mở Photoshop thủ công.

## Tại sao quản lý Thời gian Tạo của lớp?
Theo dõi Thời gian Tạo của mỗi lớp giúp bạn:
- **Kiểm toán các phiên bản** – biết chính xác khi nào một lớp được thêm vào.  
- **Đồng bộ tài sản** giữa các nhóm bằng cách so sánh dấu thời gian.  
- **Tự động hoá quy trình làm việc** dựa trên các quy tắc thời gian (ví dụ, ẩn các lớp cũ hơn một tháng).  

## Yêu cầu trước
Trước khi bắt đầu, hãy chắc chắn rằng bạn đã chuẩn bị các mục sau:

1. **Java Development Kit (JDK)** – phiên bản 8 hoặc mới hơn.  
2. **IDE** – IntelliJ IDEA, Eclipse, NetBeans, hoặc bất kỳ trình chỉnh sửa nào bạn thích.  
3. **Aspose.PSD for Java** – bạn có thể [tải xuống tại đây](https://releases.aspose.com/psd/java/) để cài đặt.  
4. **Kiến thức cơ bản về Java** – nếu bạn mới bắt đầu với Java, đừng lo; mã nguồn đã được chú thích đầy đủ.

Mọi thứ đã sẵn sàng? Tuyệt vời! Hãy chuyển sang phần thú vị của việc lập trình.

## Nhập các gói
Đầu tiên, nhập các lớp Aspose.PSD và tiện ích Java mà bạn sẽ cần. Các import này cung cấp cho bạn khả năng xử lý ảnh, thao tác lớp và định dạng ngày.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

## Bước 1: Thiết lập Thư mục Tài liệu của Bạn
Xác định thư mục chứa tệp PSD mà bạn muốn làm việc. Thay thế phần giữ chỗ bằng đường dẫn tuyệt đối trên máy của bạn.

```java
String dataDir = "Your Document Directory";
```

## Bước 2: Tải tệp PSD
Tạo một thể hiện `PsdImage` bằng cách tải tệp mục tiêu. Đối tượng này là điểm khởi đầu cho mọi thao tác với lớp.

```java
String sourceName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceName);
```

## Bước 3: Truy cập Lớp và Ngày Tạo của Nó
Lấy lớp đầu tiên (chỉ mục 0) và truy xuất dấu thời gian tạo của nó. Đây là ngày mà bạn sẽ so sánh hoặc ghi lại sau này.

```java
Layer layer = im.getLayers()[0];
Date creationDateTime = layer.getLayerCreationDateTime();
```

## Bước 4: Định dạng Ngày Tạo
Chuyển đổi đối tượng `Date` thô thành chuỗi có thể đọc được. Điều chỉnh mẫu nếu bạn muốn định dạng khác.

```java
DateFormat dateFormat = new SimpleDateFormat("yyyy/MM/dd HH:mm:ss");
```

## Bước 5: Xác thực Ngày Tạo
Để minh họa, chúng ta so sánh ngày đã lấy được với một giá trị mong đợi. Trong các dự án thực tế, bạn có thể so sánh với bản ghi trong cơ sở dữ liệu hoặc tệp cấu hình.

```java
Date expectedDateTime = new Date("2018/7/17 8:57:24");
Assert.areEqual(expectedDateTime, creationDateTime);
```

## Bước 6: Tạo Lớp Mới
Bây giờ chúng ta thực sự **tạo lớp PSD mới**. Ở đây chúng ta thêm một lớp điều chỉnh Levels, cho phép bạn điều chỉnh dải tông mà không thay đổi pixel gốc.

```java
Date now = new Date();
Layer createdLayer = im.addLevelsAdjustmentLayer();
```

> **Mẹo chuyên nghiệp:** Biến `now` ghi lại thời điểm bạn thêm lớp, bạn có thể lưu nó như siêu dữ liệu nếu cần một dấu thời gian tùy chỉnh.

## Các vấn đề thường gặp và giải pháp
| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| `NullPointerException` trên `layer.getLayerCreationDateTime()` | PSD không có lớp nào hoặc chỉ mục lớp vượt quá phạm vi. | Kiểm tra `im.getLayers().length > 0` trước khi truy cập. |
| Không khớp ngày trong xác thực | Hàm khởi tạo `Date` phân tích chuỗi theo cài đặt địa phương. | Sử dụng `SimpleDateFormat.parse("2018/07/17 08:57:24")` để phân tích đáng tin cậy. |
| Lớp mới không hiển thị trong Photoshop | Lớp điều chỉnh có thể bị ẩn mặc định. | Gọi `createdLayer.setVisible(true);` sau khi tạo. |

## Kết luận
Bây giờ bạn đã biết cách **tạo lớp PSD mới**, đọc dấu thời gian tạo của chúng, xác thực các dấu thời gian đó, và thêm các lớp điều chỉnh — tất cả đều sử dụng Aspose.PSD cho Java. Khả năng này mở ra cánh cửa cho tự động hoá tinh vi, dấu vết kiểm toán và quy trình hợp tác trong bất kỳ pipeline xử lý ảnh nào dựa trên Java.

Nếu bạn thích hướng dẫn này, hãy khám phá các tính năng khác của Aspose.PSD như hợp nhất lớp, áp dụng bộ lọc, hoặc xuất ra các định dạng khác. Các khả năng là vô hạn!

## Câu hỏi thường gặp
### Aspose.PSD là gì?
Aspose.PSD là một thư viện mạnh mẽ để làm việc với các tệp Photoshop (PSD) một cách lập trình.

### Tôi có thể sử dụng Aspose.PSD miễn phí không?
Có! Bạn có thể bắt đầu với bản dùng thử miễn phí có sẵn [tại đây](https://releases.aspose.com/).

### Tôi có cần mua giấy phép cho việc sử dụng lâu dài không?
Có, bạn có thể mua giấy phép [tại đây](https://purchase.aspose.com/buy) khi đã sẵn sàng.

### Tôi có thể tìm thêm thông tin về Aspose.PSD ở đâu?
Bạn có thể xem [tài liệu](https://reference.aspose.com/psd/java/) để có hướng dẫn chi tiết và tham chiếu API.

### Làm thế nào tôi có thể nhận hỗ trợ nếu gặp vấn đề với Aspose.PSD?
Bạn có thể truy cập [diễn đàn hỗ trợ](https://forum.aspose.com/c/psd/34) để nhận sự trợ giúp từ cộng đồng.

**Cập nhật lần cuối:** 2026-03-28  
**Kiểm tra với:** Aspose.PSD for Java 24.10  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}