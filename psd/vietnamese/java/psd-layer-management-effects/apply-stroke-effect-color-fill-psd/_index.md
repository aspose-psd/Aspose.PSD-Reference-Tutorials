---
date: 2026-04-03
description: Tìm hiểu cách lưu tệp PSD thành PNG với hiệu ứng viền và tô màu bằng
  Aspose.PSD cho Java. Hướng dẫn từng bước này cho thấy cách xuất PSD sang PNG một
  cách nhanh chóng.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: Lưu PSD dưới dạng PNG với hiệu ứng viền – Java
second_title: Aspose.PSD Java API
title: Lưu PSD thành PNG với hiệu ứng viền – Java
url: /vi/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu PSD dưới dạng PNG với Hiệu ứng Đường viền và Đổ màu – Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ học cách **lưu PSD dưới dạng PNG** đồng thời áp dụng hiệu ứng đường viền với đổ màu bằng Aspose.PSD cho Java. Dù bạn là nhà phát triển dày dặn kinh nghiệm hay mới bắt đầu, tutorial từng bước này sẽ giúp bạn hoàn thành công việc một cách dễ dàng. Chúng tôi sẽ đề cập đến mọi thứ từ việc thiết lập môi trường đến xuất ảnh cuối cùng, để bạn có thể nhanh chóng **xuất PSD sang PNG** trong các dự án của mình.

## Câu trả lời nhanh
- **Mục tiêu của hướng dẫn này là gì?** Nó cho thấy cách lưu một tệp PSD dưới dạng PNG sau khi áp dụng hiệu ứng đường viền có thể tùy chỉnh.  
- **Thư viện nào được sử dụng?** Aspose.PSD for Java.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; cần giấy phép cho môi trường sản xuất.  
- **Tôi có thể thay đổi màu đường viền không?** Có – bạn có thể đặt bất kỳ màu nào qua `ColorFillSettings`.  
- **Có thể xử lý hàng loạt không?** Chắc chắn – bao bọc mã trong vòng lặp để xử lý nhiều tệp PSD.

## PSD lưu dưới dạng PNG là gì?
Lưu một PSD dưới dạng PNG có nghĩa là chuyển đổi tệp lớp của Photoshop sang định dạng ảnh phẳng, thân thiện với web trong khi vẫn giữ được độ trung thực hình ảnh. Điều này hữu ích khi bạn cần hiển thị nội dung PSD trên website, ứng dụng di động, hoặc bất kỳ nền tảng nào không hỗ trợ trực tiếp tệp PSD.

## Tại sao áp dụng hiệu ứng đường viền với đổ màu?
Đường viền tạo ra một viền sắc nét quanh nội dung lớp, giúp đồ họa nổi bật hơn trên nền phức tạp. Kết hợp với màu đổ tùy chỉnh cho phép bạn thương hiệu hoá hình ảnh, làm nổi bật các yếu tố UI, hoặc tạo các thumbnail bắt mắt mà không cần rời Photoshop.

## Yêu cầu trước

1. **Java Development Kit (JDK) 8+** – đảm bảo `java` có trong PATH.  
2. **Aspose.PSD for Java** – tải về từ [website](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, hoặc bất kỳ trình chỉnh sửa nào bạn thích.  
4. **PSD mẫu** – một tệp đã có sẵn hiệu ứng đường viền (hoặc thêm trong Photoshop).  
5. **Kiến thức Java cơ bản** – bạn sẽ viết một vài dòng mã, nhưng không phức tạp.

Khi đã chuẩn bị xong, chúng ta có thể bắt đầu viết mã.

## Nhập các gói

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Các import này đưa vào tất cả các lớp cần thiết để tải PSD, chỉnh sửa đường viền, và lưu cả đầu ra PSD và PNG.

## Cách lưu PSD dưới dạng PNG với hiệu ứng đường viền

### Bước 1: Tải tệp PSD

Đầu tiên, chỉ định thư mục chứa PSD nguồn của bạn.

```java
String dataDir = "Your Document Directory";
```

Thay thế `"Your Document Directory"` bằng đường dẫn thực tế trên máy của bạn.

Bây giờ tải tệp trong khi giữ nguyên mọi tài nguyên hiệu ứng hiện có:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Bước 2: Đặt màu đường viền (và tùy chọn tùy chỉnh độ rộng)

Vòng lặp dưới đây duyệt qua mỗi lớp, lấy `StrokeEffect` đầu tiên và thay đổi màu đổ của nó. Bạn cũng có thể điều chỉnh `setWidth` hoặc `setPosition` trên đối tượng `StrokeEffect` nếu cần **tùy chỉnh độ rộng đường viền**.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **Mẹo chuyên nghiệp:** `Color.getDeepPink()` chỉ là một ví dụ. Sử dụng `new Color(r, g, b)` cho các giá trị RGB tùy chỉnh.

### Bước 3: Lưu PSD đã chỉnh sửa (tùy chọn)

Nếu bạn muốn giữ một phiên bản PSD với đường viền đã cập nhật, lưu nó như sau:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### Bước 4: Xuất ảnh dưới dạng PNG (bước “lưu PSD dưới dạng PNG” chính)

Cuối cùng, chuyển PSD đã chỉnh sửa thành tệp PNG sẵn sàng cho web:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

PNG sẽ giữ lại đường viền màu hồng đậm bạn đã đặt trước, và tùy chọn `TruecolorWithAlpha` đảm bảo độ trong suốt được bảo tồn.

## Các vấn đề thường gặp & Giải pháp

| Vấn đề | Lý do | Cách khắc phục |
|-------|--------|-----|
| **`ArrayIndexOutOfBoundsException`** | Lớp không có hiệu ứng nào hoặc hiệu ứng đầu tiên không phải là `StrokeEffect`. | Xác minh lớp thực sự chứa đường viền hoặc lặp qua `getEffects()` để tìm loại đúng. |
| **Màu không thay đổi** | Bạn có thể đang chỉnh sửa một bản sao của cài đặt thay vì bản gốc. | Đảm bảo bạn ép kiểu trực tiếp sang `ColorFillSettings` từ `effect.getFillSettings()`. |
| **PNG xuất hiện trống** | PSD được tải mà không raster hoá lớp. | Gọi `im.save(..., new PngOptions())` sau tất cả các chỉnh sửa; tránh lưu `im` gốc trước khi thay đổi. |

## Câu hỏi thường gặp

**H: Tôi có thể áp dụng nhiều hiệu ứng cho một lớp duy nhất bằng Aspose.PSD for Java không?**  
Đ: Có, bạn có thể truy cập các tùy chọn hòa trộn của lớp và thêm bao nhiêu hiệu ứng nào cần thiết, bao gồm bóng, phát sáng và đường viền.

**H: Có thể tự động hoá quy trình cho một loạt tệp PSD không?**  
Đ: Chắc chắn. Bao bọc việc tải, áp dụng hiệu ứng và lưu trong một vòng lặp `for‑each` để duyệt qua các tệp trong thư mục.

**H: Làm sao để khôi phục lại các thay đổi đã thực hiện trên tệp PSD?**  
Đ: Tải lại tệp gốc trước khi lưu bất kỳ sửa đổi nào; Aspose.PSD không cung cấp ngăn xếp undo.

**H: Tôi có thể tùy chỉnh độ rộng và vị trí của đường viền không?**  
Đ: Có. Sử dụng `effect.setWidth(float)` và `effect.setPosition(StrokeEffect.Position)` để điều khiển độ dày và vị trí (bên trong, bên ngoài, hoặc trung tâm).

**H: Thư viện Aspose.PSD for Java có miễn phí không?**  
Đ: Bản dùng thử miễn phí có sẵn để đánh giá. Để sử dụng đầy đủ chức năng cần mua giấy phép. Xem [buy options](https://purchase.aspose.com/buy) để biết chi tiết.

**Cập nhật lần cuối:** 2026-04-03  
**Kiểm tra với:** Aspose.PSD 24.12 for Java  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}