---
date: 2026-04-05
description: Tìm hiểu cách xuất PSD sang PNG và dễ dàng nâng cao độ tương phản hình
  ảnh bằng Aspose.PSD cho Java. Thành thạo các lớp điều chỉnh Levels qua hướng dẫn
  chi tiết từng bước này.
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: Xuất PSD sang PNG và kết xuất lớp điều chỉnh mức độ trong Java
second_title: Aspose.PSD Java API
title: Xuất PSD sang PNG và Kết xuất lớp Điều chỉnh Mức trong Java
url: /vi/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD sang PNG và Render Lớp Điều Chỉnh Mức Độ trong Java

## Giới thiệu

Bạn đã bao giờ mở một tệp PSD và nhận thấy màu sắc trông nhợt nhạt hoặc độ tương phản không đúng? Bạn có thể nhanh chóng **export PSD to PNG** trong khi tinh chỉnh hình ảnh bằng một Levels Adjustment Layer bằng cách sử dụng Aspose.PSD cho Java. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn toàn bộ quy trình — từ việc tải PSD, điều chỉnh mức độ, đến lưu kết quả dưới dạng PNG — để bạn có thể tăng độ sống động và chuẩn bị các tài sản sẵn sàng cho web trong vài phút.

## Câu trả lời nhanh
- **Ý nghĩa của “export PSD to PNG” là gì?** Nó chuyển đổi tài liệu Photoshop thành ảnh PNG không mất dữ liệu trong khi giữ nguyên độ trong suốt.  
- **Tôi có thể điều chỉnh mức độ trước khi xuất không?** Có, Aspose.PSD cho phép bạn sửa đổi mức đầu vào và đầu ra một cách lập trình.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Có thể thực hiện xử lý hàng loạt không?** Chắc chắn — bạn có thể đặt mã vào trong vòng lặp để xử lý nhiều tệp PSD.  
- **Phiên bản Java nào được yêu cầu?** Khuyến nghị sử dụng Java 8 hoặc mới hơn.

## “export PSD to PNG” là gì?
Việc export PSD sang PNG có nghĩa là lấy tệp Photoshop có nhiều lớp và làm phẳng nó thành một hình ảnh Portable Network Graphics. PNG hỗ trợ nén không mất dữ liệu và kênh alpha, làm cho nó trở nên lý tưởng cho đồ họa web và tài sản giao diện người dùng.

## Tại sao cần điều chỉnh mức độ trước khi xuất?
Việc điều chỉnh mức độ cho phép bạn kiểm soát bóng tối, tông trung và điểm sáng, cải thiện độ tương phản và cân bằng màu tổng thể. Bước này đảm bảo PNG cuối cùng trông hoàn thiện mà không cần chỉnh sửa thủ công trong Photoshop.

## Yêu cầu trước

- **Java Development Kit (JDK)** – tải phiên bản mới nhất từ trang web Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).  
- **Aspose.PSD for Java Library** – tải về từ trang tải chính thức ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Bản dùng thử miễn phí có sẵn ([https://releases.aspose.com/](https://releases.aspose.com/)).  

## Nhập Gói

Before diving into the code, import the classes that give us access to PSD manipulation and PNG export:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## Hướng dẫn từng bước

### Bước 1: Xác định Đường dẫn Tệp (Cách tự động xử lý PSD)

Đặt các biến rõ ràng, mô tả cho PSD nguồn, PSD đã chỉnh sửa, và vị trí xuất PNG cuối cùng.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### Bước 2: Tải ảnh PSD

Sử dụng `Image.load` để đọc tệp PSD vào một đối tượng `PsdImage`. Aspose.PSD tự động phát hiện định dạng.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Bước 3: Duyệt qua các Lớp (Cách điều chỉnh mức độ)

Lặp qua mọi lớp để tìm Levels Adjustment Layer.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### Bước 4: Xác định Lớp Levels

Kiểm tra mỗi lớp bằng `instanceof LevelsLayer`. Khi tìm thấy, ép kiểu để chúng ta có thể sửa đổi các thuộc tính của nó.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### Bước 5: Tinh chỉnh Levels (Cách điều chỉnh mức độ)

Điều chỉnh cả mức đầu vào và đầu ra cho kênh đầu tiên (thường là kênh tổng hợp). Các giá trị này chỉ là ví dụ; bạn có thể tự thử nghiệm.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### Bước 6: Lưu PSD đã chỉnh sửa (Cách tự động PSD)

Lưu các thay đổi trở lại một tệp PSD mới.

```java
im.save(psdPathAfterChange);
```

### Bước 7: Xuất dưới dạng PNG (Export PSD to PNG)

Nếu bạn cần phiên bản PNG, cấu hình `PngOptions` và lưu ảnh.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## Các trường hợp sử dụng phổ biến

- **Web asset preparation:** Chuyển đổi các mẫu PSD do nhà thiết kế cung cấp thành PNG sẵn sàng cho trình duyệt.  
- **Batch processing:** Tự động chuyển đổi hàng chục tệp PSD trong quy trình CI.  
- **Dynamic image generation:** Điều chỉnh mức độ ngay lập tức dựa trên đầu vào của người dùng trước khi xuất.

## Khắc phục sự cố & Mẹo

- **Null pointer khi truy cập các lớp:** Đảm bảo PSD thực sự chứa Levels Adjustment Layer; nếu không, thêm kiểm tra null.  
- **Màu sắc không mong muốn sau khi xuất:** Xác minh rằng loại màu PNG được đặt thành `TruecolorWithAlpha` để giữ độ trong suốt.  
- **Hiệu năng với nhiều tệp:** Tái sử dụng cùng một thể hiện `PsdImage` khi xử lý hàng loạt để giảm việc tiêu tốn bộ nhớ.

## Câu hỏi thường gặp

**Q: Tôi có thể điều chỉnh các kênh màu riêng lẻ (RGB) không?**  
A: Có. Sử dụng `levelsLayer.getChannel(index)` trong đó `index` = 0 (Đỏ), 1 (Xanh lá), 2 (Xanh dương) để điều chỉnh từng kênh một cách độc lập.

**Q: Làm thế nào để xử lý nhiều Levels Adjustment Layer trong một PSD?**  
A: Vòng lặp sẽ xử lý mọi lớp; mỗi `LevelsLayer` được tìm thấy sẽ được điều chỉnh theo mã bên trong khối `if`.

**Q: Có cách nào khác để cải thiện độ tương phản ngoài Levels không?**  
A: Aspose.PSD cũng cung cấp các điều chỉnh Curves, Brightness/Contrast và Histogram Equalization.

**Q: Tôi có thể tự động hoá quy trình này cho một thư mục chứa các tệp PSD không?**  
A: Đặt toàn bộ quy trình trong một vòng lặp `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` và xử lý từng tệp một cách tuần tự.

**Q: Tôi có thể tìm tài liệu và hỗ trợ thêm ở đâu?**  
A: Truy cập tài liệu tham khảo chính thức ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) và diễn đàn cộng đồng ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)).

## Kết luận

Bằng cách nắm vững quy trình **export PSD to PNG** và học **cách điều chỉnh mức độ** một cách lập trình, bạn sẽ có toàn quyền kiểm soát chất lượng hình ảnh mà không cần rời khỏi môi trường Java. Dù bạn đang chuẩn bị tài sản cho web, tự động hoá quy trình thiết kế, hay xây dựng bộ xử lý hàng loạt, Aspose.PSD cho Java giúp công việc trở nên đơn giản và đáng tin cậy.

---

**Cập nhật lần cuối:** 2026-04-05  
**Đã kiểm tra với:** Aspose.PSD 24.11 for Java  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}