---
date: 2026-02-17
description: Tìm hiểu cách xuất PSD sang PNG và xử lý luồng hình ảnh không nén với
  Aspose.PSD cho Java.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: Xuất PSD sang PNG – Tạo Đối tượng Đồ họa PSD – Luồng Không Nén trong Java
url: /vi/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất PSD sang PNG – Tạo Đối tượng Đồ họa PSD – Dòng dữ liệu không nén trong Java

## Giới thiệu
Chào mừng bạn đến với thế giới xử lý ảnh trong Java! Trong hướng dẫn này, bạn sẽ **tạo một đối tượng đồ họa PSD**, xử lý các đối tượng dòng ảnh không nén, và học cách **xuất PSD sang PNG** bằng Aspose.PSD cho Java. Dù bạn là nhà thiết kế đồ họa muốn tự động hoá quy trình làm việc hay là lập trình viên muốn tích hợp khả năng xử lý ảnh mạnh mẽ vào ứng dụng, hướng dẫn này được thiết kế riêng cho bạn. Chúng tôi sẽ đi qua mọi thứ từ các yêu cầu trước đến khi xuất file cuối cùng, đảm bảo bạn có hiểu biết vững chắc về toàn bộ quy trình.

## Câu trả lời nhanh
- **“tạo đối tượng đồ họa PSD” có nghĩa là gì?** Nó đề cập đến việc khởi tạo một ngữ cảnh đồ họa cho file PSD để bạn có thể vẽ hoặc chỉnh sửa nội dung của nó.  
- **Thư viện nào hỗ trợ các dòng không nén?** Aspose.PSD cho Java cung cấp hỗ trợ đầy đủ cho dữ liệu ảnh thô (không nén).  
- **Tôi có thể xuất PSD sang PNG sau khi chỉnh sửa không?** Có — một khi bạn có đối tượng `Graphics`, bạn có thể render PSD và lưu dưới dạng PNG.  
- **Có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Quá trình xuất có mất dữ liệu không?** Xuất sang PNG giữ nguyên chất lượng ảnh, kích thước file lớn hơn JPEG nhưng nhỏ hơn PSD không nén.  

## Cách xuất PSD sang PNG bằng Aspose.PSD cho Java
Khi bạn cần **xuất PSD sang PNG**, quy trình thường là:

1. Tải file PSD (hoặc tạo mới).  
2. Thực hiện bất kỳ thao tác vẽ hoặc chỉnh sửa lớp nào bằng đối tượng `Graphics`.  
3. Lưu ảnh kết quả bằng `PngOptions` (có thể tái sử dụng cùng một thể hiện `Graphics`).  

Mặc dù hướng dẫn này tập trung vào việc xử lý các dòng không nén, cùng một đối tượng `Graphics` bạn tạo ra có thể được tái sử dụng để render PSD thành file PNG sau này trong pipeline của bạn.

## Yêu cầu trước
Trước khi chúng ta bước vào code, hãy chắc chắn rằng bạn đã có mọi thứ cần thiết để bắt đầu hành trình này. Dưới đây là các yêu cầu trước:

### Java Development Kit (JDK)
Đảm bảo bạn đã cài đặt JDK trên máy. Bạn có thể tải từ trang web của Oracle hoặc dùng OpenJDK.

### Aspose.PSD cho Java
Bạn cần tải và cài đặt thư viện Aspose.PSD. Thư viện mạnh mẽ này cho phép bạn thao tác file PSD một cách dễ dàng. Bạn có thể lấy phiên bản mới nhất từ [liên kết này](https://releases.aspose.com/psd/java/).

### Integrated Development Environment (IDE)
Sử dụng một IDE để viết và kiểm thử code Java là một ý tưởng tốt. Bạn có thể dùng IntelliJ IDEA, Eclipse, hoặc bất kỳ IDE nào phù hợp với sở thích của mình.

### Kiến thức cơ bản về Java
Hiểu biết cơ bản về lập trình Java sẽ giúp quá trình diễn ra suôn sẻ hơn. Đảm bảo bạn nắm vững các khái niệm như lớp, phương thức và xử lý ngoại lệ.

Với mọi thứ đã sẵn sàng, hãy xắn tay áo và bắt đầu phần thú vị — viết code!

## Nhập khẩu các gói
Để bắt đầu, chúng ta cần nhập các gói cần thiết để làm việc với Aspose.PSD. Dưới đây là các import thường dùng cho việc xử lý file PSD.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Bây giờ, chúng ta sẽ chia nhỏ code thành các bước dễ hiểu để bạn có thể theo dõi một cách thuận lợi. Chúng ta sẽ thiết lập, tải file PSD, thao tác và lưu kết quả.

## Bước 1: Xác định thư mục tài liệu của bạn
Trước khi viết code, bạn cần xác định vị trí lưu trữ file PSD. Đây là bước chuẩn bị cho dự án.

```java
String dataDir = "Your Document Directory";
```

Thay thế `"Your Document Directory"` bằng đường dẫn thực tế nơi lưu file PSD (ví dụ: layers.psd). Điều này giúp bạn tìm file mà không gặp rắc rối.

## Bước 2: Tạo ByteArrayOutputStream
Bạn cần một nơi để lưu ảnh đã chỉnh sửa trước khi làm bất kỳ việc gì với nó. `ByteArrayOutputStream` sẽ giúp bạn nắm bắt dữ liệu ảnh một cách dễ dàng.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Dòng này khởi tạo một đối tượng `ByteArrayOutputStream` mới có tên `ms`. Bạn sẽ dùng đối tượng này để lưu ảnh không nén của mình.

## Bước 3: Tải file PSD
Bây giờ, đã đến lúc tải file PSD thực tế. Đây là nơi phép thuật bắt đầu!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Dòng này tải file PSD của bạn vào một đối tượng `PsdImage`. Đảm bảo đường dẫn đúng; nếu không sẽ xuất hiện lỗi như một bài kiểm tra bất ngờ.

## Bước 4: Thiết lập PsdOptions để lưu
Bạn cần chỉ định cách lưu ảnh — không nén, tất nhiên!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Ở đây, bạn tạo một đối tượng `PsdOptions` và đặt phương thức nén thành `Raw`. Phương thức này đảm bảo ảnh giữ nguyên chất lượng đầy đủ và được lưu mà không có bất kỳ nén nào.

## Bước 5: Lưu ảnh vào Output Stream
```java
psdImage.save(ms, saveOptions);
```

Dòng này lưu ảnh đã chỉnh sửa vào `ByteArrayOutputStream` bạn tạo ở Bước 2, sử dụng các tùy chọn đã định nghĩa ở Bước 4. Phương thức `save` sẽ tự động mã hoá ảnh đúng cách dựa trên cài đặt của bạn.

## Bước 6: Đặt lại Output Stream
Sau khi lưu, stream của bạn đang ở vị trí cuối. Bạn cần đặt lại để đọc từ đầu.

```java
ms.reset();
```

Phương thức `reset` này chuẩn bị `ByteArrayOutputStream` để đọc lại từ đầu. Hãy tưởng tượng như việc tua lại băng cassette trước khi nghe lại bài hát yêu thích!

## Bước 7: Tải lại ảnh vừa tạo
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Ở đây, chúng ta tải lại ảnh từ `ByteArrayOutputStream` vào một đối tượng `PsdImage` mới. Đây là lúc bạn có thể kiểm tra kết quả của các thao tác trước đó.

## Bước 8: Tạo đối tượng Graphics
Để tiếp tục chỉnh sửa hoặc render ảnh, bạn cần tạo một đối tượng graphics.

```java
Graphics graphics = new Graphics(psdImage);
```

Dòng này khởi tạo một đối tượng `Graphics` bằng cách sử dụng `psdImage` của bạn. Bây giờ bạn có thể dùng đối tượng graphics này để vẽ hoặc thao tác ảnh theo nhu cầu. Nó giống như có một cây cọ vẽ trong tay!

## Thao tác các lớp PSD bằng đối tượng Graphics
Khi đã có một thể hiện **Graphics**, bạn có thể **thao tác các lớp PSD** — ví dụ, vẽ hình, thêm văn bản, hoặc áp dụng bộ lọc cho một lớp cụ thể. Ngữ cảnh đồ họa làm việc trực tiếp trên dữ liệu pixel nền, cho phép bạn kiểm soát chi tiết từng lớp.

## Các vấn đề thường gặp và giải pháp
- **NullPointerException khi tải file** – kiểm tra lại đường dẫn `dataDir` và chắc chắn tên file đúng.  
- **Kết quả vẫn bị nén mặc dù đã dùng Raw** – xác nhận rằng `saveOptions.setCompressionMethod(CompressionMethod.Raw);` được gọi trước khi gọi `save`.  
- **Đối tượng Graphics xuất hiện trống** – đảm bảo bạn đang vẽ trên đúng instance của `PsdImage` (sử dụng đối tượng đã tải, không phải đối tượng mới tạo trừ khi có mục đích đặc biệt).

## Câu hỏi thường gặp
### Aspose.PSD là gì?
Aspose.PSD là một thư viện .NET cho phép các nhà phát triển tạo, chỉnh sửa và thao tác các file Photoshop PSD và các định dạng ảnh liên quan một cách lập trình.

### Làm sao để tải Aspose.PSD cho Java?
Bạn có thể tải nó từ [trang phát hành](https://releases.aspose.com/psd/java/).

### Có bản dùng thử miễn phí cho Aspose.PSD không?
Có, bạn có thể nhận phiên bản dùng thử miễn phí từ [đây](https://releases.aspose.com/).

### Tôi có thể nhận hỗ trợ cho Aspose.PSD không?
Chắc chắn! Bạn có thể tìm kiếm trợ giúp trên [diễn đàn hỗ trợ Aspose](https://forum.aspose.com/c/psd/34).

### Làm sao để lấy giấy phép tạm thời cho Aspose.PSD?
Chỉ cần truy cập [trang giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) để bắt đầu.

## Các câu hỏi thường gặp (FAQ)

**H: Tôi có thể dùng đối tượng graphics để chỉnh sửa chỉ một lớp cụ thể không?**  
Đ: Có. Sau khi tải PSD, chọn lớp mong muốn bằng `psdImage.getLayers().get_Item(index)` và truyền vào hàm khởi tạo `Graphics`.

**H: Phương thức nén Raw có ảnh hưởng đến kích thước file không?**  
Đ: Raw lưu dữ liệu pixel mà không nén, vì vậy kích thước file sẽ lớn hơn so với PSD đã nén, nhưng chất lượng ảnh vẫn nguyên vẹn.

**H: Có thể xuất PSD đã chỉnh sửa sang định dạng khác (ví dụ PNG) không?**  
Đ: Hoàn toàn có thể. Sử dụng phương thức `Image.save` phù hợp với `PngOptions` sau khi chỉnh sửa — đây là cách chuẩn để **xuất PSD sang PNG**.

**H: Yêu cầu phiên bản Java nào?**  
Đ: Aspose.PSD cho Java hỗ trợ JDK 8 trở lên.

**H: Làm sao giải phóng tài nguyên sau khi xử lý?**  
Đ: Gọi `psdImage.dispose()` và đóng mọi stream để giải phóng tài nguyên gốc.

---

**Cập nhật lần cuối:** 2026-02-17  
**Đã kiểm thử với:** Aspose.PSD cho Java (phiên bản mới nhất)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}