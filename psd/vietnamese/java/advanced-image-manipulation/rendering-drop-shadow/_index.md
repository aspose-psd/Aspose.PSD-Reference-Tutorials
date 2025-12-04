---
date: 2025-12-04
description: Tìm hiểu cách lưu tệp PSD thành PNG và áp dụng bóng đổ khi render bằng
  Aspose.PSD cho Java. Hướng dẫn này bao gồm cách thêm bóng, chuyển đổi PSD sang PNG
  và áp dụng bóng đổ trong Java.
language: vi
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Lưu PSD dưới dạng PNG & Thêm đổ bóng bằng Aspose.PSD Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu PSD dưới dạng PNG & Thêm Đổ Bóng với Aspose.PSD Java

## Giới thiệu

Nếu bạn đang làm việc với các tệp Photoshop trong Java, **lưu PSD dưới dạng PNG** đồng thời thêm một đổ bóng chuyên nghiệp là một yêu cầu phổ biến. Aspose.PSD giúp thực hiện nhiệm vụ này một cách đơn giản, cho phép bạn **chuyển đổi PSD sang PNG** và **áp dụng đổ bóng Java** chỉ trong vài dòng mã. Trong hướng dẫn này, chúng ta sẽ đi qua toàn bộ quy trình, từ việc tải tệp PSD đến xuất PNG cuối cùng với hiệu ứng đổ bóng được render.

## Câu hỏi nhanh
- **“Lưu PSD dưới dạng PNG” có nghĩa là gì?** Nó chuyển một tệp Photoshop có lớp thành một hình ảnh PNG phẳng, giữ lại độ trong suốt.  
- **Tôi có thể thêm đổ bóng khi chuyển đổi không?** Có — Aspose.PSD cho phép bạn chỉnh sửa hiệu ứng lớp trước khi xuất.  
- **Có cần giấy phép để chạy mã không?** Bản dùng thử miễn phí đủ cho việc đánh giá; cần giấy phép cho môi trường sản xuất.  
- **Phiên bản Java nào được hỗ trợ?** Java 8 hoặc cao hơn.  
- **Hiệu ứng đổ bóng có thể tùy chỉnh không?** Chắc chắn — bạn có thể điều chỉnh màu, độ mờ, khoảng cách, kích thước, góc và nhiều hơn nữa.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

- **Môi trường phát triển Java** – JDK 8 hoặc mới hơn đã được cài đặt.  
- **Thư viện Aspose.PSD** – Tải JAR mới nhất từ trang chính thức [here](https://releases.aspose.com/psd/java/).  
- **Một tệp PSD** – Tệp chứa ít nhất một lớp mà bạn muốn thêm đổ bóng.

## Cách lưu PSD dưới dạng PNG với đổ bóng trong Java?

Dưới đây là hướng dẫn từng bước. Mỗi bước bao gồm một mô tả ngắn gọn và đoạn mã cần sao chép.

### Bước 1: Nhập các gói cần thiết

Chúng ta bắt đầu bằng cách nhập các lớp cung cấp khả năng tải ảnh, xử lý hiệu ứng và xuất PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### Bước 2: Định nghĩa thư mục tài liệu

Đặt thư mục nơi tệp PSD nguồn và PNG kết quả sẽ được lưu.

```java
String dataDir = "Your Document Directory";
```

### Bước 3: Đặt đường dẫn tệp PSD và PNG

Xác định đường dẫn đầy đủ cho PSD đầu vào và PNG đầu ra.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Bước 4: Tải tệp PSD với hiệu ứng được bật

Bật **loadEffectsResource** để đảm bảo các hiệu ứng lớp (như đổ bóng) có thể được thao tác.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Bước 5: Truy cập hiệu ứng Đổ Bóng

Ở đây chúng ta lấy hiệu ứng đầu tiên được áp dụng cho lớp thứ hai (chỉ mục 1). Đây là nơi chúng ta sẽ đọc hoặc chỉnh sửa các tham số của đổ bóng.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Bước 6: Xác thực các thuộc tính của hiệu ứng đổ bóng (Tùy chọn nhưng hữu ích)

Kiểm tra các thuộc tính hiện có giúp bạn quyết định có cần thay đổi gì không. Các khẳng định dưới đây xác nhận các giá trị mặc định.

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **Mẹo chuyên nghiệp:** Nếu bạn muốn **cách thêm đổ bóng** với cài đặt tùy chỉnh, hãy sửa các thuộc tính trên `shadowEffect` trước khi lưu (ví dụ, `shadowEffect.setColor(Color.getRed());`).

### Bước 7: Lưu ảnh đã chỉnh sửa dưới dạng PNG

Cuối cùng, chúng ta xuất PSD (với đổ bóng đã render) ra tệp PNG. Tùy chọn `TruecolorWithAlpha` giữ lại độ trong suốt.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Và thế là bạn đã có một quy trình **chuyển đổi PSD sang PNG** hoàn chỉnh, đồng thời **áp dụng đổ bóng java** trong một lần xử lý.

## Tại sao nên dùng Aspose.PSD cho nhiệm vụ này?

- **Không cần Photoshop gốc** – Hoạt động trên bất kỳ nền tảng nào hỗ trợ Java.  
- **Độ trung thực PSD đầy đủ** – Tất cả thông tin lớp, mặt nạ và hiệu ứng được bảo lưu.  
- **Kiểm soát chi tiết** – Điều chỉnh mọi tham số của đổ bóng trước khi xuất.  
- **Hiệu năng cao** – Tối ưu cho các tệp lớn và xử lý hàng loạt.

## Các vấn đề thường gặp & Khắc phục

| Triệu chứng | Nguyên nhân có thể | Cách khắc phục |
|------------|-------------------|----------------|
| `NullPointerException` trên `shadowEffect` | Lớp mục tiêu không có hiệu ứng hoặc chỉ mục sai. | Kiểm tra chỉ mục lớp (`im.getLayers()[i]`) và đảm bảo tồn tại hiệu ứng. |
| PNG xuất ra trắng | Các tùy chọn PNG không được đặt đúng hoặc ảnh chưa được lưu. | Sử dụng `PngColorType.TruecolorWithAlpha` và xác nhận đường dẫn `im.save()` có quyền ghi. |
| Màu đổ bóng không hiển thị | Độ mờ của đổ bóng được đặt thành 0 hoặc màu trùng nền. | Đặt `shadowEffect.setOpacity(255);` và chọn màu tương phản. |

## Câu hỏi thường gặp

**H: Tôi có thể áp dụng đổ bóng cho nhiều lớp cùng lúc không?**  
Đ: Có. Duyệt qua `im.getLayers()` và chỉnh sửa `DropShadowEffect` của mỗi lớp theo nhu cầu.

**H: Tham số ‘Spread’ làm gì?**  
Đ: Nó điều chỉnh mức độ chuyển đổi từ hoàn toàn không trong suốt đến trong suốt. Giá trị spread cao tạo cạnh bóng cứng hơn.

**H: Aspose.PSD có tương thích với mọi phiên bản Photoshop không?**  
Đ: Nó hỗ trợ một loạt các phiên bản PSD, từ các bản phát hành sớm đến các tệp Photoshop CC mới nhất.

**H: Tôi có thể nhận hỗ trợ khi gặp vấn đề không?**  
Đ: Tham khảo [diễn đàn Aspose.PSD](https://forum.aspose.com/c/psd/34) để được cộng đồng và đội ngũ hỗ trợ chính thức giúp đỡ.

**H: Tôi có thể dùng thử Aspose.PSD trước khi mua không?**  
Đ: Chắc chắn. Tải bản dùng thử miễn phí từ [trang web Aspose](https://releases.aspose.com/).

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Cập nhật lần cuối:** 2025-12-04  
**Đã kiểm tra với:** Aspose.PSD 24.12 cho Java  
**Tác giả:** Aspose  

---