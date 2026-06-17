---
date: 2026-06-08
description: Tìm hiểu cách lưu PSD thành PNG bằng Aspose.PSD for Java và ngắt quá
  trình chuyển đổi khi cần. Quản lý quy trình làm việc với hình ảnh một cách hiệu
  quả.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Hỗ trợ Interrupt Monitor
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Cách lưu PSD thành PNG với Interrupt Monitor trong Aspose.PSD for Java
url: /vi/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu PSD dưới dạng PNG với Interrupt Monitor trong Aspose.PSD cho Java

## Giới thiệu

Nếu bạn cần **lưu PSD dưới dạng PNG** trong khi vẫn giữ kiểm soát đầy đủ đối với các quá trình chuyển đổi kéo dài, Interrupt Monitor của Aspose.PSD cho Java cung cấp chính xác điều đó. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn cách thiết lập monitor, chuyển đổi tệp PSD sang PNG, và hủy bỏ thao tác một cách an toàn khi cần. Bạn cũng sẽ thấy cách tính năng này phù hợp với quy trình xử lý ảnh điển hình và tại sao nó là một công cụ không thể thiếu cho các ứng dụng mạnh mẽ.

## Câu trả lời nhanh
- **Tôi có thể ngắt quá trình chuyển đổi PSD‑to‑PNG không?** Có, sử dụng `InterruptMonitor` để dừng quá trình khi cần.  
- **Phương thức nào lưu PSD dưới dạng PNG?** Gọi `save(outputPath, new PngOptions())`.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Cần giấy phép thương mại; bản dùng thử miễn phí có sẵn.  
- **Phiên bản Java nào được hỗ trợ?** Java 8 và các phiên bản sau được hỗ trợ đầy đủ.  
- **Thư viện có an toàn với đa luồng không?** Các chuyển đổi có thể chạy trong các luồng riêng; monitor xử lý việc ngắt một cách an toàn.

## Yêu cầu trước

Trước khi đi sâu vào các chi tiết phức tạp của việc sử dụng Interrupt Monitor, hãy đảm bảo bạn đã có các yêu cầu sau:

- **Môi trường phát triển Java:** Thiết lập môi trường phát triển Java trên hệ thống của bạn.  
- **Thư viện Aspose.PSD:** Có được thư viện Aspose.PSD cho Java. Bạn có thể tải xuống [tại đây](https://releases.aspose.com/psd/java/). Bạn cũng có thể truy cập trang chính của Aspose [tại đây](https://releases.aspose.com/).  
- **Thư mục tài liệu:** Có một thư mục được chỉ định cho các tài liệu PSD của bạn.

## Nhập gói

Bắt đầu bằng cách nhập các gói cần thiết vào dự án Java của bạn. Điều này đảm bảo bạn có quyền truy cập vào các chức năng của Aspose.PSD.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Bây giờ, chúng ta sẽ phân tích mã ví dụ thành hướng dẫn từng bước để tích hợp Interrupt Monitor vào dự án Aspose.PSD cho Java của bạn.

## Cách lưu PSD dưới dạng PNG bằng Interrupt Monitor?

`PsdImage` đại diện cho một tài liệu PSD được tải vào bộ nhớ.  
`SaveImageWorker` thực hiện việc chuyển đổi ảnh trong một luồng riêng.  

Tải tệp PSD của bạn bằng `new PsdImage("source.psd")`, gắn một `InterruptMonitor` vào `SaveImageWorker`, và gọi `save("output.png", new PngOptions())`. Monitor sẽ theo dõi yêu cầu hủy và dừng quá trình chuyển đổi một cách sạch sẽ, trả lại quyền kiểm soát cho ứng dụng của bạn trong vòng vài mili giây.

### Bước 1: Đặt thư mục tài liệu của bạn

```java
String dataDir = "Your Document Directory";
```

Đảm bảo thay thế “Your Document Directory” bằng đường dẫn thực tế nơi lưu trữ các tài liệu PSD của bạn.

### Bước 2: Xác định tùy chọn ảnh và đường dẫn đầu ra

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Xác định các tùy chọn ảnh, tệp PSD nguồn, và đường dẫn đầu ra mong muốn cho ảnh đã chuyển đổi.

### Bước 3: Khởi tạo Interrupt Monitor và SaveImageWorker

Lớp `InterruptMonitor` giám sát một quá trình chuyển đổi đang chạy và có thể ngắt nó khi `requestInterrupt()` được gọi.  

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Tạo các thể hiện của `InterruptMonitor` và `SaveImageWorker`, liên kết monitor với worker chuyển đổi ảnh.

### Bước 4: Bắt đầu luồng chuyển đổi ảnh

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Khởi tạo một luồng mới cho quá trình chuyển đổi ảnh và thiết lập thời gian chờ để dự đoán việc ngắt.

### Bước 5: Ngắt quá trình

Gọi `monitor.requestInterrupt()` sẽ báo hiệu cho monitor dừng quá trình chuyển đổi đang diễn ra.  

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

Ngắt quá trình chuyển đổi ảnh bằng `InterruptMonitor` và chờ cho việc ngắt hoàn tất. Cuối cùng, dọn dẹp bằng cách xóa tệp đầu ra.

## Tại sao nên sử dụng Interrupt Monitor cho việc chuyển đổi PSD‑to‑PNG?

Aspose.PSD hỗ trợ **hơn 30 định dạng đầu ra**, bao gồm PNG, JPEG, BMP và TIFF, và có thể xử lý các tệp lên tới **500 MB** mà không cần tải toàn bộ tài liệu vào bộ nhớ. Bằng cách thêm một interrupt monitor, bạn giảm lãng phí CPU và cải thiện độ phản hồi trong các pipeline xử lý hàng loạt, đặc biệt khi một chuyển đổi vượt quá thời gian dự kiến.

## Vấn đề thường gặp và giải pháp

- **Quá trình chuyển đổi bị treo vô thời hạn:** Đảm bảo monitor được gắn **trước** khi gọi `save`.  
- **Tệp đầu ra bị hỏng sau khi ngắt:** Monitor dừng sạch sẽ; tuy nhiên, luôn kiểm tra xem tệp có tồn tại trước khi sử dụng.  
- **Mối quan ngại về an toàn đa luồng:** Chạy mỗi chuyển đổi trong một luồng riêng; monitor chỉ ảnh hưởng đến worker liên quan.

## Câu hỏi thường gặp

**Q1: Interrupt Monitor là gì trong Aspose.PSD cho Java?**  
A: Interrupt Monitor cho phép các nhà phát triển tạm dừng hoặc hủy các chuyển đổi ảnh kéo dài, cung cấp kiểm soát thời gian thực đối với việc sử dụng tài nguyên.

**Q2: Làm sao tôi có thể lấy thư viện Aspose.PSD cho Java?**  
A: Bạn có thể tải xuống thư viện Aspose.PSD cho Java [tại đây](https://releases.aspose.com/psd/java/).

**Q3: Có bản dùng thử miễn phí cho Aspose.PSD cho Java không?**  
A: Có, bạn có thể khám phá bản dùng thử miễn phí của Aspose.PSD [tại đây](https://releases.aspose.com/).

**Q4: Tôi có thể tìm hỗ trợ cho Aspose.PSD cho Java ở đâu?**  
A: Truy cập diễn đàn hỗ trợ Aspose.PSD cho Java [tại đây](https://forum.aspose.com/c/psd/34).

**Q5: Làm sao tôi có thể mua giấy phép cho Aspose.PSD cho Java?**  
A: Bạn có thể mua giấy phép cho Aspose.PSD cho Java [tại đây](https://purchase.aspose.com/buy).

**Q6: Tôi có thể chuyển đổi nhiều tệp PSD sang PNG đồng thời không?**  
A: Có, tạo một luồng riêng cho mỗi tệp và gắn một `InterruptMonitor` riêng cho mỗi worker chuyển đổi.

**Q7: Thư viện có xử lý hồ sơ màu trong quá trình chuyển đổi PSD‑to‑PNG không?**  
A: Chắc chắn; Aspose.PSD giữ lại các hồ sơ ICC được nhúng và áp dụng chúng vào PNG đầu ra một cách tự động.

**Cập nhật lần cuối:** 2026-06-08  
**Được kiểm tra với:** Aspose.PSD 23.12 cho Java  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan

- [Lưu PSD dưới dạng PNG và áp dụng Rendering Drop Shadow trong Aspose.PSD cho Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Xuất PSD sang PNG & Thêm lớp Regular mới bằng Aspose.PSD cho Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Hỗ trợ Interrupt Monitor trong tệp PSD - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}