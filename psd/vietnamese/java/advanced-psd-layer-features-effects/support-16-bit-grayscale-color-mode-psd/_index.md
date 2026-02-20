---
date: 2026-02-20
description: Tìm hiểu cách chuyển đổi PSD sang PNG đồng thời đặt chế độ màu của PSD
  thành ảnh xám 16‑bit bằng Aspose.PSD cho Java. Hướng dẫn chi tiết từng bước kèm
  ví dụ mã.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Cách chuyển đổi PSD sang PNG với chế độ màu xám 16-bit trong Java
url: /vi/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

 Frequently Asked Questions" -> "## Câu hỏi thường gặp". Then each Q/A translate.

Make sure to keep markdown formatting for Q/A.

Then last updated etc translate.

Then closing shortcodes.

Let's produce final.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi PSD sang PNG với chế độ màu xám 16-bit trong Java

## Giới thiệu
Khi bạn đang khám phá thế giới thiết kế đồ họa và xử lý ảnh, việc **chuyển đổi PSD sang PNG** giống như có một vũ khí bí mật. Sử dụng chế độ màu xám 16‑bit mang lại độ sâu và sự phong phú về tông màu đáng kinh ngạc, giúp hình ảnh của bạn nổi bật hơn. Trong hướng dẫn này, chúng ta sẽ đi qua cách **đặt chế độ màu PSD** thành 16‑bit grayscale và sau đó **xuất PSD dưới dạng PNG** bằng Aspose.PSD cho Java. Sẵn sàng nâng cấp quy trình làm việc với ảnh? Hãy bắt đầu.

## Câu trả lời nhanh
- **“convert PSD to PNG” bao gồm những gì?** Tải một file PSD, tùy chọn thay đổi chế độ màu, và lưu nó dưới dạng file PNG.  
- **Lớp Aspose nào chịu trách nhiệm chuyển đổi?** `PsdImage` để tải và `PngOptions` để lưu.  
- **Tôi có cần giấy phép đặc biệt không?** Bản dùng thử đủ cho việc thử nghiệm; cần giấy phép trả phí cho môi trường sản xuất.  
- **Có thể giữ độ sâu 16‑bit trong PNG không?** Có, bằng cách sử dụng `PngColorType.GrayscaleWithAlpha`.  
- **Các IDE nào được hỗ trợ?** Bất kỳ IDE Java nào – IntelliJ IDEA, Eclipse, VS Code, v.v.

## Tại sao chuyển đổi PSD sang PNG với màu xám 16‑bit?
* **Bảo tồn chi tiết tông màu:** 16‑bit grayscale lưu trữ 65 536 mức xám, nhiều hơn rất nhiều so với 256 mức của ảnh 8‑bit.  
* **Tương thích rộng rãi:** PNG được hỗ trợ rộng rãi trên trình duyệt, ứng dụng di động và công cụ desktop, đồng thời vẫn giữ dữ liệu chất lượng cao.  
* **Quy trình không mất dữ liệu:** Chuyển đổi bằng Aspose.PSD đảm bảo không có hiện tượng nén gây mất mát, lý tưởng cho lưu trữ hoặc xử lý tiếp theo.

## Yêu cầu trước
Trước khi bắt đầu, hãy chắc chắn rằng bạn đã chuẩn bị đầy đủ để tận dụng tối đa hướng dẫn này. Bạn sẽ cần:

1. **Java Development Kit (JDK)** – Đảm bảo bạn đã cài phiên bản mới nhất. Bạn có thể tải từ [trang của Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Thư viện Aspose.PSD cho Java** – Đây là động cơ cho phép chúng ta thao tác với file PSD. Tải về từ [trang tải Aspose](https://releases.aspose.com/psd/java/).  
3. **Một IDE** – IntelliJ IDEA, Eclipse, hoặc Visual Studio Code đều hoạt động tốt.  
4. **Kiến thức cơ bản về Java** – Hiểu cú pháp Java sẽ giúp các bước diễn ra suôn sẻ hơn.  
5. **File PSD mẫu** – Tạo một file trong Adobe Photoshop hoặc tải mẫu miễn phí trực tuyến.

Sẵn sàng? Tuyệt vời! Hãy nhập các gói cần thiết và bắt đầu viết mã.

## Nhập các gói
Để khởi động, thêm các import cần thiết của Aspose.PSD vào file Java của bạn:

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

Các import này cung cấp cho bạn quyền truy cập vào các chức năng cần dùng để thao tác file PSD, đặt chế độ màu và xuất kết quả dưới dạng PNG.

## Bước 1: Xác định Thư mục của Bạn
Đầu tiên, thiết lập các thư mục nguồn và đầu ra. Điều này cho chương trình biết nơi đọc file PSD gốc và nơi ghi các file đã chuyển đổi.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Thay thế các chuỗi placeholder bằng đường dẫn thực tế trên máy của bạn.

## Bước 2: Tạo một phương thức để xử lý hình ảnh
Chúng ta sẽ gói logic chuyển đổi vào một phương thức có thể tái sử dụng. Phương thức nhận tất cả các tham số bạn có thể muốn điều chỉnh, như chế độ màu, độ sâu bit và mức nén.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Phương thức này cho phép bạn **đặt chế độ màu PSD** và sau đó **xuất PSD dưới dạng PNG** trong một luồng duy nhất.

## Bước 3: Xác định đường dẫn tệp và tải PSD
Trong phương thức, xây dựng đường dẫn tệp đầy đủ và tải PSD grayscale 16‑bit gốc:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

Biến `postfix` giúp bạn theo dõi các thiết lập đã dùng cho mỗi file xuất ra.

## Bước 4: Xử lý lớp hoặc toàn bộ hình ảnh
Bây giờ chúng ta hoặc vẽ lên một lớp cụ thể hoặc trên toàn bộ hình ảnh. Trong ví dụ này, chúng ta thêm một viền xám nhẹ để làm cho kết quả dễ nhìn hơn.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

Hình chữ nhật được tính toán động để luôn ở trung tâm bất kể kích thước ảnh.

## Bước 5: Lưu tệp PSD đã chỉnh sửa
Sau khi vẽ, chúng ta lưu PSD với chế độ màu và độ sâu bit chính xác mà bạn đã chỉ định. Đây là phần cốt lõi của **đặt chế độ màu PSD** trước khi chuyển đổi.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Bước 6: Chuyển đổi PSD sang PNG
Cuối cùng, chúng ta tải lại PSD vừa lưu và xuất nó dưới dạng PNG. Bằng cách sử dụng `PngColorType.GrayscaleWithAlpha` chúng ta bảo tồn độ sâu 16‑bit trong file PNG.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Bây giờ bạn đã **chuyển đổi PSD sang PNG** thành công trong khi giữ dữ liệu grayscale 16‑bit chất lượng cao.

## Các vấn đề thường gặp và giải pháp
| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| **“Unsupported color type” exception** | Cố gắng lưu PSD với cấu hình kênh không được hỗ trợ. | Đảm bảo `channelBitsCount` khớp với độ sâu thực tế (16) và `channelsCount` đúng cho grayscale (1). |
| **File not found** | Đường dẫn thư mục nguồn không đúng. | Kiểm tra lại chuỗi `sourceDir` và xác nhận file PSD tồn tại. |
| **Output PNG appears black** | PNG được lưu mà không xử lý kênh alpha. | Sử dụng `PngColorType.GrayscaleWithAlpha` như hướng dẫn ở trên. |

## Câu hỏi thường gặp

**Q: Chế độ màu xám 16-bit là gì?**  
A: Nó cung cấp 65 536 mức xám, mang lại chi tiết tông màu vượt trội so với chuẩn 8‑bit (256 mức).

**Q: Tôi có thể dùng Aspose.PSD cho ảnh không phải grayscale không?**  
A: Chắc chắn! Aspose.PSD hỗ trợ RGB, CMYK, Lab và nhiều chế độ màu khác.

**Q: Có phiên bản dùng thử của Aspose.PSD không?**  
A: Có, bạn có thể thử bản dùng thử miễn phí của Aspose.PSD. Chỉ cần truy cập [trang tải Aspose](https://releases.aspose.com/).

**Q: Tôi có thể tìm thêm ví dụ về việc sử dụng Aspose.PSD ở đâu?**  
A: Bạn có thể xem [tài liệu](https://reference.aspose.com/psd/java/) để có các ví dụ và hướng dẫn chi tiết hơn.

**Q: Làm sao để mua giấy phép cho Aspose.PSD?**  
A: Bạn có thể mua giấy phép bằng cách truy cập [trang mua Aspose](https://purchase.aspose.com/buy).

---

**Cập nhật lần cuối:** 2026-02-20  
**Đã kiểm tra với:** Aspose.PSD cho Java 24.12 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}