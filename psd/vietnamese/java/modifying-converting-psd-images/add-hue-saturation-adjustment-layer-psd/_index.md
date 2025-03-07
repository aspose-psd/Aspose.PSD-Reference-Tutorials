---
title: Thêm lớp điều chỉnh độ bão hòa Hue vào PSD
linktitle: Thêm lớp điều chỉnh độ bão hòa Hue vào PSD
second_title: API Java Aspose.PSD
description: Tìm hiểu cách thêm các lớp điều chỉnh độ bão hòa màu sắc vào PSD bằng Aspose.PSD cho Java trong hướng dẫn từng bước toàn diện này. Nâng cao quy trình làm việc thiết kế đồ họa của bạn.
weight: 14
url: /vi/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thêm lớp điều chỉnh độ bão hòa Hue vào PSD

## Giới thiệu
Khi nói đến thiết kế đồ họa, thao tác màu sắc đóng một vai trò quan trọng—cụ thể, việc điều chỉnh màu sắc, độ bão hòa và độ sáng có thể biến đổi mạnh mẽ tâm trạng và chất lượng của bất kỳ hình ảnh nào. Một cách hiệu quả để đạt được điều này là sử dụng các lớp điều chỉnh trong Photoshop (tệp PSD). Nếu bạn đang tìm cách nâng cao các tệp PSD của mình theo chương trình bằng cách sử dụng Java, thì thư viện Aspose.PSD sẵn sàng trợ giúp! Hướng dẫn này sẽ hướng dẫn bạn qua các bước để thêm Lớp điều chỉnh độ bão hòa Huế vào các tệp PSD của bạn, giúp quy trình công việc của bạn hiệu quả và hiệu quả hơn.
Trong hướng dẫn này, chúng tôi sẽ đề cập đến mọi thứ từ việc nhập các gói cần thiết đến các chi tiết thực tế của các ví dụ về mã.
## Điều kiện tiên quyết
Trước khi chúng tôi chuyển sang mã, hãy đảm bảo bạn có những điều sau:
1.  Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt JDK 8 trở lên trên máy của mình. Bạn có thể tải nó xuống từ[Tải xuống bộ công cụ phát triển Java SE](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD for Java Library: Bạn cần có thư viện Aspose.PSD để có thể[tải về ở đây](https://releases.aspose.com/psd/java/). 
3. IDE: Môi trường phát triển tích hợp (IDE) phù hợp như IntelliJ IDEA hoặc Eclipse để phát triển Java.
4. Kiến thức Java cơ bản: Làm quen với lập trình Java là một lợi thế, nhưng đừng lo lắng; chúng tôi sẽ hướng dẫn bạn từng bước về mã.
Bây giờ chúng ta đã sắp xếp các điều kiện tiên quyết, hãy chuyển sang phần thú vị—viết mã!
## Gói nhập khẩu
Để bắt đầu làm việc với thư viện Aspose.PSD, bước đầu tiên là nhập các lớp cần thiết. Đây là cách bạn có thể thực hiện điều đó trong tệp Java của mình:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Đảm bảo rằng bạn đã thêm các thư viện thích hợp vào dự án của mình để các quá trình nhập này hoạt động trơn tru.
## Bước 1: Thiết lập thư mục tài liệu của bạn
Mọi dự án đều cần có điểm khởi đầu và dự án của chúng tôi cũng không ngoại lệ. Bạn cần chỉ định thư mục lưu trữ các tệp PSD của mình. Điều này rất quan trọng để tải và lưu hình ảnh đúng cách.
```java
String dataDir = "Your Document Directory"; // Cập nhật đường dẫn này vào thư mục thực tế của bạn
```
## Bước 2: Tải tệp PSD hiện có
Để thao tác với tệp PSD hiện có, trước tiên chúng ta cần tải nó vào chương trình của mình. Đây là cách bạn có thể làm điều đó:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Trong mã này, cập nhật`"HueSaturationAdjustmentLayer.psd"` vào tên của tệp PSD hiện có mà bạn muốn chỉnh sửa.
## Bước 3: Chỉnh sửa lớp Hue/Saturation
Tiếp theo, chúng ta sẽ duyệt qua các lớp của hình ảnh PSD đã tải để tìm và chỉnh sửa bất kỳ lớp Hue/Saturation hiện có nào. Bước này liên quan đến việc sửa đổi các giá trị màu sắc, độ bão hòa và độ sáng.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
Trong ví dụ này:
- Chúng tôi đang điều chỉnh màu sắc thành -25, độ bão hòa thành -12 và độ sáng thành +67.
-  các`getRange(2)` phương pháp cho phép chúng tôi điều chỉnh các dải màu cụ thể theo ý muốn.
## Bước 4: Lưu tệp PSD đã sửa đổi
Sau khi thực hiện điều chỉnh, bước tiếp theo là lưu file. Đây là một phần quan trọng trong quy trình của chúng tôi, đảm bảo rằng những thay đổi chúng tôi đã thực hiện không bị mất.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Bước 5: Thêm lớp Hue/Saturation mới
Tiếp theo, bạn có thể muốn thêm lớp điều chỉnh Hue/Saturation mới vào một tệp PSD khác. Chỉ cần làm theo cách tiếp cận tương tự như bạn đã sử dụng trước đó nhưng với các tệp PSD khác nhau.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Bước 6: Đặt giá trị Hue/Saturation mới cho lớp mới
Bây giờ bạn đã tạo lớp mới này, hãy áp dụng các cài đặt màu sắc, độ bão hòa và độ sáng mong muốn giống như trước đây.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## Bước 7: Lưu tệp PSD đã cập nhật
Cuối cùng, lưu tệp PSD với lớp Hue/Saturation đã thêm để bạn có thể thấy những thay đổi của mình.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Chúc mừng! Bạn đã thao tác thành công với file PSD bằng Aspose.PSD for Java. Giờ đây, bạn có thể thử nghiệm các hình ảnh khác nhau và những thay đổi sâu sắc hơn, biến các dự án thiết kế đồ họa của bạn thành hiện thực.
## Phần kết luận
Làm việc với đồ họa theo chương trình sẽ mở ra vô số khả năng. Việc sử dụng Aspose.PSD cho Java để thêm và sửa đổi Lớp điều chỉnh độ bão hòa Hue mang lại sự linh hoạt và hiệu quả có thể hợp lý hóa quy trình thiết kế của bạn. Cho dù bạn đang cải thiện ảnh cho một dự án hay tạo nội dung trực quan tuyệt đẹp, việc thành thạo các công cụ này có thể cải thiện đáng kể kết quả của bạn.
 Hãy thoải mái khám phá thêm các chức năng của Aspose.PSD bằng cách đi sâu vào[tài liệu](https://reference.aspose.com/psd/java/) hoặc xem xét việc lấy một[giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) để kiểm tra toàn bộ sức mạnh của thư viện.
## Câu hỏi thường gặp
### Lớp điều chỉnh độ bão hòa Hue là gì?
Lớp điều chỉnh độ bão hòa màu sắc cho phép bạn sửa đổi các thuộc tính màu của hình ảnh mà không làm thay đổi vĩnh viễn các pixel gốc.
### Tôi có cần cài đặt Photoshop để sử dụng Aspose.PSD không?
Không, Aspose.PSD là một thư viện độc lập hoạt động độc lập với Photoshop.
### Tôi có thể sử dụng Aspose.PSD để xử lý hàng loạt không?
Có, bạn có thể tự động hóa và xử lý hàng loạt nhiều tệp PSD bằng Aspose.PSD.
### Aspose.PSD có miễn phí không?
Aspose.PSD cung cấp bản dùng thử miễn phí nhưng cần có giấy phép để sử dụng lâu dài. Bạn có thể xem giá[đây](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
