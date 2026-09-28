---
date: 2026-09-28
description: Tìm hiểu cách xuất PSD sang PNG đồng thời đặt chế độ màu của PSD thành
  xám 16-bit bằng Aspose.PSD cho Java. Hướng dẫn từng bước kèm ví dụ mã.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: Xuất PSD sang PNG – Xám 16-bit – Java
og_description: Xuất PSD sang PNG với xám 16‑bit bằng Aspose.PSD cho Java. Thực hiện
  theo hướng dẫn từng bước này để giữ lại 65.536 mức xám.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Xuất PSD sang PNG với xám 16‑bit trong Java – Hướng dẫn Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Cách xuất PSD sang PNG với chế độ màu xám 16‑bit trong Java
url: /vi/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD dưới dạng PNG với chế độ màu xám 16‑bit trong Java

## Giới thiệu
Việc export PSD dưới dạng PNG đồng thời giữ chế độ màu xám 16‑bit mang lại độ sâu của một bức ảnh chuyên nghiệp và khả năng tương thích toàn cầu của PNG. Trong hướng dẫn này, bạn sẽ học cách **đặt chế độ màu của PSD thành 16‑bit grayscale** và sau đó **export PSD dưới dạng PNG** bằng Aspose.PSD cho Java. Bài học bao gồm mọi thứ từ các yêu cầu trước đến khắc phục sự cố, giúp bạn tích hợp quy trình này vào bất kỳ pipeline xử lý ảnh nào dựa trên Java.

## Câu trả lời nhanh
- **Việc “export PSD as PNG” bao gồm gì?** Tải một tệp PSD, tùy chọn thay đổi chế độ màu, và lưu nó dưới dạng tệp PNG.  
- **Lớp Aspose nào xử lý việc chuyển đổi?** `PsdImage` tải PSD và `PngOptions` định nghĩa các thiết lập đầu ra PNG.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Có – bản dùng thử hoạt động cho việc thử nghiệm, nhưng cần giấy phép trả phí cho việc sử dụng thương mại.  
- **Có thể giữ độ sâu 16‑bit trong PNG không?** Chắc chắn, bằng cách sử dụng `PngColorType.GrayscaleWithAlpha`.  
- **Các IDE nào được hỗ trợ?** Bất kỳ IDE Java nào – IntelliJ IDEA, Eclipse, VS Code, hoặc NetBeans.

## Export PSD dưới dạng PNG là gì?
Export PSD as PNG là quá trình chuyển đổi một tài liệu Adobe Photoshop (PSD) thành tệp Portable Network Graphics (PNG) trong khi bảo toàn dữ liệu pixel và độ sâu màu của hình ảnh. Việc chuyển đổi này thường được sử dụng để chia sẻ các tài sản màu xám chất lượng cao trên web mà không mất chi tiết tonal.

## Tại sao export PSD dưới dạng PNG với màu xám 16‑bit?
Export sang PNG đồng thời giữ màu xám 16‑bit bảo tồn 65 536 mức xám, cung cấp độ phong phú tonal vượt trội so với ảnh 8‑bit. Hỗ trợ rộng rãi của PNG đảm bảo các tệp có thể hiển thị trong trình duyệt, ứng dụng di động và trình chỉnh sửa desktop mà không mất dữ liệu, trong khi nén không mất dữ liệu của Aspose.PSD đảm bảo không có hiện tượng artefact nào xuất hiện.

## Yêu cầu trước
Trước khi bắt đầu, hãy chắc chắn bạn đã chuẩn bị các mục sau:

1. **Java Development Kit (JDK)** – Cài đặt JDK mới nhất từ [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Thư viện Aspose.PSD cho Java** – Tải JAR từ [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **Một IDE** – IntelliJ IDEA, Eclipse, hoặc Visual Studio Code hoạt động hoàn hảo.  
4. **Kiến thức Java cơ bản** – Bạn nên thoải mái tạo lớp, xử lý ngoại lệ, và làm việc với đường dẫn tệp.  
5. **Một tệp PSD mẫu** – Tạo trong Adobe Photoshop hoặc tải mẫu miễn phí trực tuyến.

## Cách export PSD dưới dạng PNG từng bước

## Làm thế nào để đặt chế độ màu của PSD thành màu xám 16‑bit?
`PsdImage` là lớp Aspose.PSD dùng để tải và đại diện cho một tệp PSD trong bộ nhớ.  
`ColorMode` là một enumeration định nghĩa chế độ màu của ảnh PSD.  

Tải PSD bằng `PsdImage`, thay đổi chế độ màu bằng thuộc tính `ColorMode`, và sau đó lưu tệp đã chỉnh sửa. Hoạt động này diễn ra hoàn toàn trong bộ nhớ, loại bỏ nhu cầu tạo tệp trung gian và đảm bảo quá trình chuyển đổi nhanh chóng và hiệu quả.

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

Các import này cung cấp quyền truy cập vào các chức năng bạn sẽ dùng để thao tác tệp PSD, đặt chế độ màu và export kết quả dưới dạng PNG.

## Làm thế nào để xác định thư mục nguồn và thư mục đầu ra?
`File` là lớp java.io đại diện cho một đường dẫn tệp hoặc thư mục trên hệ thống.  

Bạn cần chỉ định cho chương trình nơi đọc PSD gốc và nơi ghi PNG đã chuyển đổi. Việc sử dụng đường dẫn tuyệt đối hoặc tương đối đều được, nhưng hãy giữ chúng nhất quán giữa các môi trường để tránh lỗi giải quyết đường dẫn.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Thay thế các chuỗi placeholder bằng các đường dẫn thực tế trên máy của bạn.

## Làm thế nào để đóng gói logic chuyển đổi trong một phương thức có thể tái sử dụng?
`convertPsdToPng` là một phương thức tùy chỉnh bao gồm tất cả các bước cần thiết để chuyển đổi một tệp PSD sang PNG với các thiết lập tùy chọn.  

Tạo một phương thức riêng cho phép bạn tái sử dụng cùng một quy trình chuyển đổi cho nhiều tệp hoặc các thiết lập khác nhau. Truyền các tham số như đường dẫn nguồn, thư mục đích và mức nén tùy chọn, giúp workflow linh hoạt và dễ bảo trì.

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

Phương thức này cho phép bạn **đặt chế độ màu PSD** và sau đó **export PSD dưới dạng PNG** trong một luồng duy nhất.

## Làm thế nào để tải PSD và áp dụng chế độ màu xám 16‑bit?
`PsdImage` là lớp Aspose.PSD tải tệp PSD vào bộ nhớ.  
`ColorMode.GRAYSCALE_16` là giá trị enumeration đặt ảnh thành màu xám 16‑bit.  
`channelBitsCount` là thuộc tính xác định số bit trên mỗi kênh.  

Trong phương thức chuyển đổi, xây dựng đầy đủ đường dẫn tệp, khởi tạo `PsdImage`, và thay đổi `ColorMode` thành `ColorMode.GRAYSCALE_16`. Thuộc tính `channelBitsCount` phải được đặt thành 16 để giữ độ sâu bit cao, đảm bảo ảnh giữ toàn bộ thông tin tonal.

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` giúp bạn theo dõi các thiết lập đã dùng cho mỗi tệp xuất.

## Làm thế nào để vẽ một viền nhẹ trên hình ảnh (bước tùy chọn)?
`Graphics` là lớp cung cấp khả năng vẽ trên canvas `PsdImage`.  

Bạn có thể tùy chọn vẽ một hình chữ nhật màu xám quanh ảnh để làm cho kết quả dễ quan sát hơn trong quá trình thử nghiệm. Bước này minh họa cách làm việc với lớp và đối tượng đồ họa, và hình chữ nhật được tính toán động để luôn ở trung tâm bất kể kích thước ảnh.

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

## Làm thế nào để lưu PSD đã chỉnh sửa với chế độ màu mới?
`PsdOptions` là lớp kiểm soát cách lưu tệp PSD, bao gồm các thiết lập chế độ màu và độ sâu bit.  

Sau khi vẽ (hoặc bỏ qua bước này), gọi `save` trên đối tượng `PsdImage`, truyền vào một đối tượng `PsdOptions` giữ cấu hình màu xám 16‑bit. Điều này đảm bảo PSD đã lưu giữ chế độ màu mong muốn mà không mất dữ liệu.

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

## Làm thế nào để chuyển PSD sang PNG trong khi giữ độ sâu 16‑bit?
`PngOptions` là lớp định nghĩa các thiết lập đầu ra PNG như loại màu và mức nén.  
`PngColorType.GrayscaleWithAlpha` là giá trị enumeration lưu dữ liệu màu xám 16‑bit kèm kênh alpha.  

Tải PSD vừa lưu, cấu hình `PngOptions` với `PngColorType.GrayscaleWithAlpha`, và gọi `save`. Điều này giữ dữ liệu màu xám 16‑bit trong tệp PNG, cung cấp hình ảnh không mất dữ liệu, chất lượng cao, phù hợp cho các bước xử lý hoặc phân phối tiếp theo.

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

Bây giờ bạn đã **export PSD dưới dạng PNG** thành công trong khi giữ dữ liệu màu xám 16‑bit chất lượng cao.

## Các vấn đề thường gặp và giải pháp
| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| **“Unsupported color type” exception** | Cố gắng lưu PSD với cấu hình kênh không được hỗ trợ. | Đảm bảo `channelBitsCount` khớp với độ sâu bit thực tế (16) và `channelsCount` đúng cho màu xám (1). |
| **File not found** | Đường dẫn thư mục nguồn không đúng. | Kiểm tra lại chuỗi `sourceDir` và xác nhận tệp PSD tồn tại ở vị trí đó. |
| **Output PNG appears black** | PNG được lưu mà không xử lý alpha đúng cách. | Sử dụng `PngColorType.GrayscaleWithAlpha` như trên. |
| **Memory overflow on large PSDs** | Tải toàn bộ tệp vào bộ nhớ. | Kích hoạt chế độ streaming bằng `PsdImage.load(inputStream, new LoadOptions())` để xử lý các tệp lớn một cách hiệu quả. |

## Câu hỏi thường gặp

**Q: Chế độ màu xám 16‑bit là gì?**  
A: Nó cung cấp 65 536 mức xám, mang lại chi tiết tonal vượt trội so với ảnh 8‑bit tiêu chuẩn (256 mức).

**Q: Tôi có thể dùng Aspose.PSD cho ảnh không phải màu xám không?**  
A: Chắc chắn! Aspose.PSD hỗ trợ RGB, CMYK, Lab, Indexed và nhiều chế độ màu khác.

**Q: Có phiên bản dùng thử của Aspose.PSD không?**  
A: Có, bạn có thể thử phiên bản dùng thử miễn phí của Aspose.PSD. Chỉ cần truy cập [Aspose download page](https://releases.aspose.com/).

**Q: Tôi có thể tìm thêm ví dụ Aspose.PSD ở đâu?**  
A: Kiểm tra tài liệu chính thức tại [documentation](https://reference.aspose.com/psd/java/) để xem các hướng dẫn chi tiết, tham chiếu API và dự án mẫu.

**Q: Làm sao mua giấy phép cho Aspose.PSD?**  
A: Bạn có thể mua giấy phép bằng cách truy cập [Aspose purchase page](https://purchase.aspose.com/buy).

---

**Cập nhật lần cuối:** 2026-09-28  
**Kiểm thử với:** Aspose.PSD for Java 24.12 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Chuyển đổi PSD sang PNG với độ sâu bit được chỉ định bằng Aspose.PSD cho Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Export PSD sang PNG với hiệu ứng lớp bằng Aspose.PSD cho Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Lưu PSD dưới dạng JPEG và hỗ trợ màu RGB với Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}