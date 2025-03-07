---
title: Lớp điều chỉnh mức kết xuất trong tệp PSD - Java
linktitle: Lớp điều chỉnh mức kết xuất trong tệp PSD - Java
second_title: API Java Aspose.PSD
description: Tìm hiểu cách dễ dàng nâng cao độ tương phản và độ sống động của hình ảnh bằng Aspose.PSD cho Java. Các lớp điều chỉnh cấp độ chính với hướng dẫn từng bước này.
weight: 17
url: /vi/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lớp điều chỉnh mức kết xuất trong tệp PSD - Java

## Giới thiệu

Bạn đã bao giờ mở một tệp PSD chỉ để thấy hình ảnh thiếu độ tương phản hoặc độ sống động chưa? Đừng sợ, các chiến binh chỉnh sửa hình ảnh! Aspose.PSD dành cho Java được giải cứu nhờ khả năng thao tác Lớp điều chỉnh cấp độ mạnh mẽ. Hướng dẫn này sẽ trang bị cho bạn kiến thức để tinh chỉnh hình ảnh của bạn bằng cách sử dụng Cấp độ một cách dễ dàng. 

## Điều kiện tiên quyết

- Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt phiên bản JDK mới nhất trên hệ thống của mình. Bạn có thể tải xuống từ trang web của Oracle ([https://www.oracle.com/java/technologists/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Thư viện Aspose.PSD cho Java: Tải xuống thư viện Aspose.PSD cho Java từ trang tải xuống ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Bạn sẽ cần giấy phép hợp lệ để sử dụng đầy đủ các tính năng nhưng có sẵn bản dùng thử miễn phí để giúp bạn bắt đầu ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Gói nhập khẩu

Trước khi đi sâu vào mã, chúng ta cần nhập các lớp Aspose.PSD cần thiết để tương tác với các tệp PSD. Đây là những gì bạn sẽ cần:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 các`com.aspose.psd` gói cung cấp quyền truy cập vào các chức năng thao tác PSD, trong khi`com.aspose.psd.imaging.PngOptions` cho phép chúng ta xác định các tùy chọn khi lưu hình ảnh dưới dạng PNG.

Bây giờ, hãy bắt tay vào cuộc phiêu lưu điều chỉnh Cấp độ của chúng tôi:

## Bước 1: Thiết lập đường dẫn tệp:

- Xác định các biến cho thư mục tài liệu của bạn (`dataDir`), tên tệp PSD nguồn (`sourceFileName`), tên tệp PSD đích sau khi sửa đổi (`psdPathAfterChange`) và đường dẫn xuất PNG cuối cùng (`pngExportPath`). Hãy cân nhắc sử dụng tên mô tả để cải thiện khả năng đọc mã.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Bước 2: Tải hình ảnh PSD:

-  Sử dụng`Image.load` phương pháp mở tệp PSD nguồn và lưu trữ nó trong một`PsdImage`sự vật (`im`). Aspose.PSD tự động phát hiện định dạng tệp.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Bước 3: Lặp lại qua các lớp:

- Chúng tôi cần tìm Lớp điều chỉnh cấp độ trong PSD của bạn. Aspose cung cấp một cách thuận tiện để lặp qua tất cả các lớp bằng vòng lặp.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (mã kiểm tra Lớp Cấp độ sẽ được thêm vào đây)
}
```

## Bước 4: Xác định lớp cấp độ:

- Bên trong vòng lặp, kiểm tra xem lớp hiện tại (`im.getLayers()[i]` ) là một thể hiện của`LevelsLayer` lớp sử dụng`instanceof` nhà điều hành. 
-  Nếu đúng như vậy, hãy chuyển lớp đó thành một`LevelsLayer` đối tượng để thao tác tiếp theo.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (mã điều chỉnh cấp độ sẽ được thêm vào đây)
   }
}
```
## Bước 5: Mức độ tinh chỉnh (Tiếp theo):

-  Điều chỉnh mức đầu ra bằng cách sử dụng`setOutputShadowLevel` Và`setOutputHighlightLevel` để kiểm soát độ tối và độ sáng của hình ảnh thu được. Các giá trị này xác định phạm vi mức đầu vào sẽ được ánh xạ tới phạm vi đầu ra.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Điều chỉnh mức đầu vào (0-255):
	   channel.setInputShadowLevel((short) 10); // Làm tối bóng một chút
	   channel.setInputMidtoneLevel(2.0f);     // Tăng âm trung
	   channel.setInputHighlightLevel((short) 230); // Giảm điểm nổi bật

	   // Điều chỉnh mức đầu ra (0-255):
	   channel.setOutputShadowLevel((short) 20); // Làm tối bóng tối hơn nữa
	   channel.setOutputHighlightLevel((short) 200); //Làm sáng vùng sáng
   }
}
```

## Bước 6: Lưu PSD đã sửa đổi:

-  Sử dụng`save` phương pháp của`PsdImage` đối tượng để lưu hình ảnh đã sửa đổi vào đường dẫn đã chỉ định (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Bước 7: Xuất dưới dạng PNG (Tùy chọn):

-  Nếu bạn cần phiên bản PNG của hình ảnh đã điều chỉnh, hãy tạo một`PngOptions` đối tượng và đặt loại màu thành`TruecolorWithAlpha` . Sau đó, sử dụng`save` lại phương thức này với đường dẫn và tùy chọn xuất PNG.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Và bạn có nó! Bạn đã điều chỉnh thành công Lớp điều chỉnh cấp độ trong tệp PSD của mình bằng Aspose.PSD cho Java. Bằng cách hiểu các bước này và thử nghiệm các giá trị khác nhau, bạn có thể nâng cao độ tương phản và hình thức tổng thể của hình ảnh.

## Phần kết luận

Aspose.PSD cho Java trao quyền cho bạn kiểm soát quá trình chỉnh sửa hình ảnh của mình. Bằng cách thành thạo Lớp điều chỉnh cấp độ, bạn có thể thổi sức sống mới vào ảnh và thiết kế của mình. Hãy nhớ rằng, luyện tập sẽ tạo nên sự hoàn hảo, vì vậy đừng ngần ngại thử nghiệm và khám phá toàn bộ tiềm năng của công cụ mạnh mẽ này.
 
## Câu hỏi thường gặp

### Tôi có thể điều chỉnh riêng từng kênh màu (RGB) không? 
Có, bạn có thể truy cập từng kênh màu bằng cách sử dụng`getChannel` phương pháp của`LevelsLayer` đối tượng và sửa đổi cấp độ của nó một cách độc lập.

### Làm cách nào để xử lý nhiều Lớp điều chỉnh cấp độ trong PSD?
Mã lặp qua tất cả các lớp, do đó, nó sẽ tự động xử lý bất kỳ lớp Cấp độ bổ sung nào được tìm thấy trong hình ảnh.

### Có cách nào khác để điều chỉnh độ tương phản hình ảnh ngoài Levels không?
Tuyệt đối! Aspose.PSD cung cấp nhiều công cụ điều chỉnh hình ảnh khác nhau như Đường cong, Độ sáng/Độ tương phản, v.v.

### Tôi có thể tự động hóa quá trình này cho nhiều hình ảnh không? 
Có, bạn có thể kết hợp mã này vào tập lệnh xử lý vòng lặp hoặc hàng loạt để xử lý hiệu quả nhiều tệp PSD.

### Tôi có thể tìm thêm thông tin và hỗ trợ ở đâu?
Aspose cung cấp tài liệu mở rộng ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) và một diễn đàn hỗ trợ ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) nếu có bất kỳ câu hỏi hoặc vấn đề nào bạn có thể gặp phải.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
