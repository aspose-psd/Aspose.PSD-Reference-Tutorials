---
date: 2026-04-05
description: Tìm hiểu cách hiển thị lớp điều chỉnh phơi sáng trong các tệp PSD bằng
  Aspose.PSD cho Java. Hướng dẫn từng bước kèm ví dụ mã để chỉnh sửa và thêm các lớp
  phơi sáng.
keywords:
- render exposure adjustment layer
- exposure adjustment layer
- Aspose.PSD Java
linktitle: Kết xuất lớp điều chỉnh phơi sáng trong các tệp PSD - Java
second_title: Aspose.PSD Java API
title: Kết xuất lớp điều chỉnh phơi sáng trong tệp PSD - Java
url: /vi/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kết xuất lớp điều chỉnh phơi sáng trong tệp PSD - Java

## Giới thiệu

Bạn đang làm việc với các tệp Photoshop PSD và cần **render exposure adjustment layer** một cách lập trình? Dù bạn đang chỉnh sửa các lớp hiện có hay thêm lớp mới, Aspose.PSD for Java cung cấp một cách mạnh mẽ và trực quan để xử lý các nhiệm vụ này. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn cách sử dụng Aspose.PSD for Java để render và chỉnh sửa các lớp điều chỉnh phơi sáng trong tệp PSD. Khi kết thúc bài hướng dẫn này, bạn sẽ biết cách điều chỉnh các thiết lập phơi sáng trong các lớp hiện có và thêm lớp điều chỉnh phơi sáng mới vào tệp PSD của mình. Hãy bắt đầu!

## Câu trả lời nhanh
- **Thư viện nào cần thiết?** Aspose.PSD for Java
- **Tôi có thể chỉnh sửa một lớp phơi sáng hiện có không?** Có, bạn có thể thay đổi exposure, offset và gamma correction.
- **Làm thế nào để thêm một lớp điều chỉnh phơi sáng mới?** Sử dụng `addExposureAdjustmentLayer()` trên một thể hiện `PsdImage`.
- **Xuất PNG có được hỗ trợ không?** Hoàn toàn có – sử dụng `PngOptions` để lưu kết quả dưới dạng PNG.
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Cần giấy phép thương mại cho việc sử dụng trong sản xuất; bản dùng thử miễn phí có sẵn.

## Lớp điều chỉnh phơi sáng render là gì?

Lớp điều chỉnh phơi sáng là một lớp Photoshop không phá hủy (non‑destructive) thay đổi độ sáng, offset và gamma của hình ảnh nền. Render lớp này có nghĩa là áp dụng các thiết lập đó để kết quả hình ảnh phản ánh các điều chỉnh, sau đó bạn có thể xuất ra các định dạng như PNG.

## Tại sao nên sử dụng Aspose.PSD for Java để render lớp điều chỉnh phơi sáng?

- **Kiểm soát đầy đủ** – thao tác các thuộc tính lớp mà không cần mở Photoshop.
- **Xử lý hàng loạt** – tự động hoá các điều chỉnh trên nhiều tệp.
- **Đa nền tảng** – chạy trên bất kỳ hệ thống nào có JDK.
- **Bảo tồn cấu trúc PSD** – giữ các lớp có thể chỉnh sửa cho các lần sửa đổi sau.

## Yêu cầu trước

1. **Java Development Kit (JDK)** – ít nhất JDK 8.
2. **Aspose.PSD for Java** – tải xuống từ [here](https://releases.aspose.com/psd/java/).
3. **Kiến thức cơ bản về Java** – bạn nên quen thuộc với cú pháp Java tiêu chuẩn.
4. **IDE hoặc Trình soạn thảo văn bản** – IntelliJ IDEA, Eclipse, VS Code, hoặc bất kỳ trình soạn thảo nào bạn thích.

## Nhập gói

Đầu tiên, nhập các lớp Aspose.PSD cần thiết:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Cách render lớp điều chỉnh phơi sáng – Hướng dẫn từng bước

### Bước 1: Tải tệp PSD

```java
String dataDir = "Your Document Directory";  // Define your document directory
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Source PSD file path

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Load the PSD file
```

Thay thế `"Your Document Directory"` bằng thư mục chứa các tệp PSD của bạn. Phương thức `Image.load()` trả về một đối tượng `PsdImage` cho phép bạn truy cập đầy đủ vào các lớp của tài liệu.

### Bước 2: Chỉnh sửa một lớp điều chỉnh phơi sáng hiện có

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Adjust the exposure level
        expLayer.setOffset(-0.25f);  // Set the offset
        expLayer.setGammaCorrection(0.5f);  // Adjust the gamma correction
    }
}
```

Vòng lặp duyệt qua mọi lớp, tìm bất kỳ `ExposureLayer` nào và cập nhật ba tham số chính của nó. Đây là phần cốt lõi của **rendering the exposure adjustment layer** với các giá trị tùy chỉnh của bạn.

### Bước 3: Lưu tệp PSD đã chỉnh sửa

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Path to save the modified PSD file

im.save(psdPathAfterChange);  // Save the changes to the PSD file
```

Tệp PSD đã chỉnh sửa giữ nguyên tất cả các lớp gốc, nhưng lớp điều chỉnh phơi sáng bây giờ phản ánh các thiết lập mới.

### Bước 4: Xuất kết quả dưới dạng PNG

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Path to save the PNG file

PngOptions saveOptions = new PngOptions();  // Create PNG options
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

im.save(pngExportPath, saveOptions);  // Save as PNG
```

Sử dụng `PngOptions` với `TruecolorWithAlpha` đảm bảo PNG xuất ra giữ đầy đủ độ sâu màu và bất kỳ độ trong suốt nào từ PSD.

### Bước 5: Thêm một lớp điều chỉnh phơi sáng mới

Nếu bạn cần **add a new exposure adjustment layer** vào một tài liệu hiện có, hãy sử dụng đoạn mã sau:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Source PSD file path

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Load the PSD file

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Add new exposure adjustment layer

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Path to save the modified PSD file
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Path to save the PNG file

img.save(psdPathAfterChange);  // Save the changes to the PSD file

PngOptions options = new PngOptions();  // Create PNG options
options.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

img.save(pngExportPath, options);  // Save as PNG
```

Phương thức `addExposureAdjustmentLayer` tạo một lớp điều chỉnh mới với các giá trị exposure, offset và gamma được chỉ định, sau đó bạn có thể render và xuất nó giống như trước.

## Các vấn đề thường gặp & Mẹo

- **Không tìm thấy lớp** – Đảm bảo PSD thực sự chứa một `ExposureLayer`. Sử dụng `instanceof ExposureLayer` như trong ví dụ để tránh `ClassCastException`.
- **Lỗi đường dẫn tệp** – Sử dụng đường dẫn tuyệt đối hoặc xác minh rằng `dataDir` kết thúc bằng ký tự phân tách tệp (`/` hoặc `\`).
- **Ngoại lệ giấy phép** – Chạy mà không có giấy phép hợp lệ sẽ thêm watermark vào đầu ra. Đăng ký giấy phép sớm trong mã (`License license = new License(); license.setLicense("Aspose.PSD.lic");`).

## Câu hỏi thường gặp

### Aspose.PSD for Java là gì?

Aspose.PSD for Java là một thư viện cho phép bạn tạo, chỉnh sửa và chuyển đổi các tệp PSD một cách lập trình bằng Java. Nó cung cấp chức năng toàn diện để làm việc với tài liệu Photoshop.

### Tôi có thể sử dụng Aspose.PSD for Java để thao tác các loại lớp khác không?

Có, Aspose.PSD for Java hỗ trợ nhiều loại lớp, bao gồm lớp văn bản, lớp điều chỉnh và lớp hình ảnh, cho phép thao tác rộng rãi các tệp PSD.

### Làm thế nào để bắt đầu với Aspose.PSD for Java?

Bạn có thể bắt đầu bằng cách tải thư viện từ [website](https://releases.aspose.com/psd/java/) và tham khảo [documentation](https://reference.aspose.com/psd/java/) để có hướng dẫn chi tiết và ví dụ.

### Có bản dùng thử miễn phí cho Aspose.PSD for Java không?

Có, bản dùng thử miễn phí có sẵn. Bạn có thể tải xuống [here](https://releases.aspose.com/).

### Làm sao tôi có thể nhận hỗ trợ cho Aspose.PSD for Java?

Để được hỗ trợ, bạn có thể truy cập [Aspose support forum](https://forum.aspose.com/c/psd/34) nơi bạn có thể đặt câu hỏi và nhận trợ giúp từ cộng đồng.

**Câu hỏi bổ sung**

**Q: Tôi có thể batch‑process nhiều tệp PSD không?**  
A: Chắc chắn. Đặt logic tải, chỉnh sửa và lưu trong một vòng lặp lặp qua danh sách các đường dẫn tệp.

**Q: Thư viện có giữ nguyên cấu trúc lớp khi tôi thêm lớp exposure mới không?**  
A: Có. Lớp mới được thêm lên trên các lớp hiện có, duy trì cấu trúc gốc.

**Q: Tôi có thể xuất sang những định dạng ảnh nào ngoài PNG?**  
A: Aspose.PSD hỗ trợ JPEG, BMP, TIFF và một số định dạng khác thông qua các lớp `*Options` tương ứng.

---

**Last Updated:** 2026-04-05  
**Tested With:** Aspose.PSD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}