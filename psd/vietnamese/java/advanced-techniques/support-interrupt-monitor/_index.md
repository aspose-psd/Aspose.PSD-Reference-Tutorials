---
date: 2025-12-25
description: Tìm hiểu cách chuyển đổi PSD sang PNG bằng Aspose.PSD cho Java với hỗ
  trợ giám sát ngắt, bao gồm ví dụ ngắt luồng Java và các mẹo lưu PSD dưới dạng PNG.
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: Cách chuyển đổi PSD sang PNG với hỗ trợ giám sát ngắt trong Aspose.PSD cho
  Java
url: /vi/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi PSD sang PNG với Interrupt Monitor trong Aspose.PSD cho Java

## Giới thiệu

Nếu bạn cần **chuyển đổi PSD sang PNG** đồng thời giữ toàn quyền kiểm soát quá trình chuyển đổi hình ảnh kéo dài, Interrupt Monitor của Aspose.PSD cho Java là công cụ bạn đang tìm kiếm. Trong hướng dẫn này, chúng ta sẽ đi qua một **ví dụ ngắt luồng Java** thực tế cho phép bạn dừng quá trình chuyển đổi ở giữa, mang lại sự linh hoạt trong việc quản lý tài nguyên, áp dụng thời gian chờ, hoặc phản hồi khi người dùng hủy bỏ.

## Câu trả lời nhanh
- **Interrupt Monitor làm gì?** Nó cho phép bạn gửi tín hiệu dừng một quá trình chuyển đổi hình ảnh đang diễn ra một cách an toàn.  
- **Tôi có thể chuyển đổi PSD sang PNG với nó không?** Có – monitor hoạt động với bất kỳ thao tác lưu nào, bao gồm PNG.  
- **Cần một luồng riêng không?** Thông thường bạn chạy quá trình chuyển đổi trong một luồng riêng để có thể ngắt nó.  
- **Phiên bản Aspose.PSD nào cần?** Bất kỳ phiên bản gần đây nào có `com.aspose.psd.multithreading.InterruptMonitor`.  
- **Có cần giấy phép cho môi trường sản xuất không?** Có, cần giấy phép Aspose.PSD hợp lệ cho việc sử dụng không phải thử nghiệm.

## “Chuyển đổi PSD sang PNG” với Interrupt Monitor là gì?

Việc chuyển đổi một tài liệu Photoshop lớn (PSD/PSB) sang hình ảnh PNG có thể tiêu tốn nhiều CPU. Bằng cách gắn một **Interrupt Monitor** vào công việc chuyển đổi, bạn có khả năng dừng quá trình một cách có chương trình—rất phù hợp cho các dịch vụ web, công việc batch, hoặc ứng dụng UI nơi người dùng có thể hủy thao tác.

## Tại sao nên sử dụng Interrupt Monitor?

- **Giao diện đáp ứng:** Ngăn ứng dụng của bạn bị treo khi một tệp lớn đang được xử lý.  
- **Quản lý tài nguyên:** Dừng các chuyển đổi vượt quá thời gian hoặc ngân sách bộ nhớ.  
- **Xử lý lỗi:** Dọn dẹp một cách nhẹ nhàng các tệp đầu ra một phần khi xảy ra gián đoạn.

## Yêu cầu trước

- Môi trường phát triển Java (JDK 8 trở lên).  
- Thư viện Aspose.PSD cho Java – tải xuống **[here](https://releases.aspose.com/psd/java/)**.  
- Một thư mục chứa các tệp PSD/PSB mà bạn muốn làm việc.

## Nhập các gói

Bắt đầu bằng cách nhập các lớp cần thiết. Điều này sẽ cho phép bạn truy cập các tùy chọn hình ảnh, interrupt monitor và các tiện ích đa luồng.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## Hướng dẫn từng bước

### Bước 1: Đặt thư mục tài liệu của bạn

```java
String dataDir = "Your Document Directory";
```

Thay thế `"Your Document Directory"` bằng đường dẫn tuyệt đối nơi các tệp PSD của bạn nằm.

### Bước 2: Định nghĩa tùy chọn hình ảnh và đường dẫn đầu ra

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Ở đây chúng ta **lưu PSD dưới dạng PNG** bằng cách sử dụng `PngOptions`. Điều chỉnh tên tệp theo nhu cầu.

### Bước 3: Khởi tạo Interrupt Monitor và SaveImageWorker

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Đối tượng `InterruptMonitor` sẽ được sử dụng sau này để dừng quá trình chuyển đổi. `SaveImageWorker` liên kết monitor với nhiệm vụ chuyển đổi.

### Bước 4: Bắt đầu chuyển đổi hình ảnh trong một luồng riêng

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Chúng ta khởi chạy quá trình chuyển đổi trên một luồng nền để luồng chính vẫn đáp ứng. Lệnh `Thread.sleep(3000)` mô phỏng một kịch bản timeout.

### Bước 5: Ngắt quá trình (Ví dụ Java Thread Interrupt)

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

Gọi `monitor.interrupt()` kích hoạt logic **cách ngắt monitor**. Sau khi ngắt, chúng ta dọn dẹp bất kỳ tệp PNG đã ghi một phần nào đó.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|----------|
| Quá trình chuyển đổi không bao giờ dừng | Monitor không được liên kết với worker | Đảm bảo `SaveImageWorker` nhận cùng một thể hiện `InterruptMonitor`. |
| Tệp đầu ra vẫn còn lại sau khi ngắt | Mã dọn dẹp không được thực thi | Kiểm tra khối `finally` có chạy và đường dẫn tệp đúng. |
| `OutOfMemoryError` trên các tệp PSB lớn | Không sử dụng tùy chọn streaming | Sử dụng `PsdImage` với `LoadOptions` cho phép tải hiệu quả về bộ nhớ. |

## Câu hỏi thường gặp

### Câu hỏi 1: Interrupt Monitor là gì trong Aspose.PSD cho Java?

Interrupt Monitor cho phép các nhà phát triển **quản lý và ngắt các quá trình chuyển đổi hình ảnh**, cung cấp kiểm soát chi tiết đối với các tác vụ kéo dài.

### Câu hỏi 2: Làm sao để tôi có được thư viện Aspose.PSD cho Java?

Bạn có thể tải xuống thư viện Aspose.PSD cho Java **[here](https://releases.aspose.com/psd/java/)**.

### Câu hỏi 3: Có bản dùng thử miễn phí cho Aspose.PSD cho Java không?

Có, bạn có thể khám phá bản dùng thử miễn phí của Aspose.PSD **[here](https://releases.aspose.com/)**.

### Câu hỏi 4: Tôi có thể tìm hỗ trợ cho Aspose.PSD cho Java ở đâu?

Truy cập diễn đàn hỗ trợ Aspose.PSD cho Java **[here](https://forum.aspose.com/c/psd/34)**.

### Câu hỏi 5: Làm sao để mua giấy phép cho Aspose.PSD cho Java?

Bạn có thể mua giấy phép cho Aspose.PSD cho Java **[here](https://purchase.aspose.com/buy)**.

---

**Cập nhật lần cuối:** 2025-12-25  
**Kiểm tra với:** Aspose.PSD 24.11 for Java  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}