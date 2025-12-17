---
date: 2025-12-17
description: Tìm hiểu cách chuyển đổi PSD sang PNG trong khi đặt chế độ màu của PSD
  thành ảnh xám 16-bit bằng Aspose.PSD cho Java. Hướng dẫn từng bước kèm ví dụ mã.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Cách chuyển đổi PSD sang PNG với chế độ màu xám 16-bit trong Java
url: /vi/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi PSD sang PNG với chế độ màu xám 16‑bit trong Java

## Giới thiệu
Khi bạn bắt đầu khám phá thế giới thiết kế đồ họa và xử lý ảnh, việc **chuyển đổi PSD sang PNG** giống như có một vũ khí bí mật. Đặc biệt, sử dụng chế độ màu xám 16‑bit mang lại cho hình ảnh độ sâu và chi tiết tuyệt vời, khiến chúng thực sự nổi bật. Trong hướng dẫn này, chúng ta sẽ đi qua cách **đặt chế độ màu PSD** thành 16‑bit grayscale và sau đó **xuất PSD dưới dạng PNG** bằng Aspose.PSD cho Java. Sẵn sàng nâng cấp quy trình làm việc với ảnh của bạn? Hãy bắt đầu.

## Câu trả lời nhanh
- **“Chuyển đổi PSD sang PNG” bao gồm những gì?** Tải một tệp PSD, tùy chọn thay đổi chế độ màu, và lưu nó dưới dạng tệp PNG.  
- **Lớp Aspose nào thực hiện việc chuyển đổi?** `PsdImage` để tải và `PngOptions` để lưu.  
- **Tôi có cần giấy phép đặc biệt không?** Bản dùng thử đủ cho việc thử nghiệm; cần giấy phép trả phí cho môi trường sản xuất.  
- **Có thể giữ độ sâu 16‑bit trong PNG không?** Có, bằng cách sử dụng `PngColorType.GrayscaleWithAlpha`.  
- **Những IDE nào được hỗ trợ?** Bất kỳ IDE Java nào – IntelliJ IDEA, Eclipse, VS Code, v.v.

## Yêu cầu trước
Trước khi bắt đầu, hãy chắc chắn rằng bạn đã chuẩn bị đầy đủ để tận dụng tối đa hướng dẫn này. Bạn sẽ cần:

1. **Java Development Kit (JDK)** – Đảm bảo bạn đã cài phiên bản mới nhất. Bạn có thể tải từ [trang của Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Thư viện Aspose.PSD cho Java** – Đây là động cơ cho phép chúng ta thao tác với tệp PSD. Tải về từ [trang tải Aspose](https://releases.aspose.com/psd/java/).  
3. **Một IDE** – IntelliJ IDEA, Eclipse, hoặc Visual Studio Code đều hoạt động tốt.  
4. **Kiến thức cơ bản về Java** – Quen thuộc với cú pháp Java sẽ giúp các bước diễn ra suôn sẻ hơn.  
5. **Một tệp PSD mẫu** – Hoặc tạo một tệp trong Adobe Photoshop, hoặc tải mẫu miễn phí trực tuyến.

Sẵn sàng? Tuyệt vời! Hãy nhập các gói cần thiết và bắt đầu viết mã.

## Nhập các gói
Để khởi động, thêm các import cần thiết của Aspose.PSD vào tệp Java của bạn:

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

Các import này cung cấp quyền truy cập vào các chức năng bạn sẽ dùng để thao tác tệp PSD, đặt chế độ màu, và xuất kết quả dưới dạng PNG.

## Bước 1: Xác định thư mục của bạn
Đầu tiên, thiết lập các thư mục nguồn và đầu ra. Điều này cho chương trình biết nơi đọc tệp PSD gốc và nơi ghi các tệp đã chuyển đổi.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Thay thế các chuỗi placeholder bằng đường dẫn thực tế trên máy của bạn.

## Bước 2: Tạo phương thức xử lý ảnh
Chúng ta sẽ gói logic chuyển đổi vào một phương thức có thể tái sử dụng. Phương thức nhận tất cả các tham số bạn có thể muốn tùy chỉnh, chẳng hạn như chế độ màu, độ sâu bit và mức nén.

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
Bên trong phương thức, xây dựng đường dẫn tệp đầy đủ và tải PSD grayscale 16‑bit gốc:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

Biến `postfix` giúp bạn theo dõi các thiết lập đã dùng cho mỗi tệp xuất ra.

## Bước 4: Xử lý lớp hoặc toàn bộ ảnh
Bây giờ chúng ta hoặc vẽ trên một lớp cụ thể hoặc trên toàn bộ ảnh. Trong ví dụ này, chúng ta thêm một viền xám nhẹ để làm cho kết quả dễ nhìn hơn.

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
Cuối cùng, chúng ta tải lại PSD vừa lưu và xuất nó dưới dạng PNG. Bằng cách sử dụng `PngColorType.GrayscaleWithAlpha` chúng ta giữ nguyên độ sâu 16‑bit trong tệp PNG.

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
| **Ngoại lệ “Unsupported color type”** | Cố gắng lưu PSD với cấu hình kênh không được hỗ trợ. | Đảm bảo `channelBitsCount` khớp với độ sâu thực tế (16) và `channelsCount` đúng cho grayscale (1). |
| **Không tìm thấy tệp** | Đường dẫn thư mục nguồn không đúng. | Kiểm tra lại chuỗi `sourceDir` và xác nhận tệp PSD tồn tại. |
| **PNG đầu ra hiện màu đen** | PNG được lưu mà không xử lý kênh alpha. | Sử dụng `PngColorType.GrayscaleWithAlpha` như trong ví dụ trên. |

## Câu hỏi thường gặp

**H: Chế độ màu xám 16‑bit là gì?**  
Đ: Nó cung cấp 65 536 mức xám, mang lại chi tiết tonal nhiều hơn rất nhiều so với chế độ 8‑bit tiêu chuẩn (256 mức).

**H: Tôi có thể dùng Aspose.PSD cho ảnh không phải grayscale không?**  
Đ: Chắc chắn! Aspose.PSD hỗ trợ RGB, CMYK, Lab và nhiều chế độ màu khác.

**H: Có phiên bản dùng thử của Aspose.PSD không?**  
Đ: Có, bạn có thể thử phiên bản dùng thử miễn phí của Aspose.PSD. Chỉ cần truy cập [trang tải Aspose](https://releases.aspose.com/).

**H: Tôi có thể tìm thêm ví dụ về cách dùng Aspose.PSD ở đâu?**  
Đ: Bạn có thể xem [tài liệu](https://reference.aspose.com/psd/java/) để có thêm các ví dụ chi tiết và hướng dẫn.

**H: Làm sao mua giấy phép cho Aspose.PSD?**  
Đ: Bạn có thể mua giấy phép bằng cách truy cập [trang mua Aspose](https://purchase.aspose.com/buy).

---

**Cập nhật lần cuối:** 2025-12-17  
**Đã kiểm thử với:** Aspose.PSD cho Java 24.12 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}