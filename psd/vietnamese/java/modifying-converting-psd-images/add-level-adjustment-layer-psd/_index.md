---
date: 2026-03-07
description: Học cách điều chỉnh mức độ bằng cách thêm lớp Điều chỉnh Mức trong các
  tệp PSD sử dụng Aspose.PSD cho Java. Nắm vững các chỉnh sửa tông màu một cách nhanh
  chóng.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: Cách điều chỉnh Mức độ – Thêm lớp điều chỉnh Mức độ trong PSD
url: /vi/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thêm Level Adjustment Layer trong PSD

## Giới thiệu
Nếu bạn đang muốn **cách điều chỉnh mức** trong tài liệu Photoshop của mình, Level Adjustment Layer là công cụ hoàn hảo. Nó cho phép bạn tinh chỉnh bóng tối, tông trung và điểm sáng mà không làm thay đổi vĩnh viễn các pixel gốc. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn cách thêm Level Adjustment Layer vào tệp PSD bằng Aspose.PSD for Java, để bạn có thể đạt được kiểm soát tông màu chuyên nghiệp chỉ trong vài bước.

## Câu trả lời nhanh
- **Level Adjustment Layer làm gì?** Nó thay đổi dải tông màu của hình ảnh một cách không phá hủy.  
- **Thư viện nào được sử dụng?** Aspose.PSD for Java.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí hoạt động cho phát triển; cần giấy phép cho môi trường sản xuất.  
- **Thời gian thực hiện khoảng bao lâu?** Khoảng 10‑15 phút cho một điều chỉnh cơ bản.  
- **Có thể điều chỉnh nhiều kênh không?** Có, bạn có thể đặt mức đầu vào/đầu ra cho từng kênh màu riêng biệt.

## Level Adjustment Layer là gì?
Level Adjustment Layer cho phép bạn chỉnh sửa cân bằng tông màu của hình ảnh bằng cách điều chỉnh bóng tối đầu vào, tông trung và điểm sáng cũng như mức đầu ra. Vì nó tồn tại trên một lớp riêng, bạn có thể bật/tắt hoặc xóa lớp này mà không ảnh hưởng đến tác phẩm nền.

## Tại sao thêm Level Adjustment Layer bằng Aspose.PSD?
- **Tự động hoá:** Tích hợp việc tinh chỉnh mức vào quy trình xử lý hàng loạt.  
- **Đa nền tảng:** Hoạt động trên bất kỳ hệ điều hành nào hỗ trợ Java.  
- **Độ chính xác:** Truy cập cài đặt từng kênh một cách lập trình để có kết quả chính xác.  

## Yêu cầu trước
1. Java Development Kit (JDK). Nếu bạn chưa có, tải về từ [trang web Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) hoặc sử dụng OpenJDK.  
2. Thư viện Aspose.PSD for Java – tải JAR mới nhất từ [liên kết tải xuống này](https://releases.aspose.com/psd/java/).  
3. Kiến thức cơ bản về lập trình Java.  
4. Một IDE như IntelliJ IDEA, Eclipse hoặc NetBeans với JAR Aspose.PSD đã được thêm vào classpath của dự án.

## Nhập các gói
Trước khi bắt đầu viết mã, chúng ta cần nhập các gói cần thiết từ thư viện Aspose.PSD. Đây là cách thực hiện:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Các import này cho phép chúng ta truy cập các lớp để tải tệp PSD, làm việc với level adjustment layers và thao tác các cài đặt kênh riêng lẻ.

## Cách Điều Chỉnh Mức trong Tệp PSD
Dưới đây là hướng dẫn từng bước cho bạn biết **cách điều chỉnh mức** một cách lập trình.

### Bước 1: Thiết lập Đường dẫn Tệp
Xác định vị trí của PSD nguồn và nơi lưu tệp đã chỉnh sửa.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Thay thế `"Your Document Directory"` bằng thư mục thực tế trên máy của bạn.

### Bước 2: Tải Tệp PSD
Tạo một thể hiện `PsdImage` từ tệp nguồn.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Bây giờ bạn có quyền truy cập đầy đủ vào tất cả các lớp bên trong PSD.

### Bước 3: Duyệt qua các Lớp
Tìm Level Adjustment Layer mà bạn muốn chỉnh sửa.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
Kiểm tra `instanceof LevelsLayer` đảm bảo chúng ta chỉ làm việc với các level adjustment layer.

### Bước 4: Điều chỉnh Cài đặt Kênh Mức
Tinh chỉnh các giá trị đầu vào và đầu ra cho kênh đã chọn.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Input Midtone Level:** Thay đổi dải tông trung.  
- **Input Shadow Level:** Làm tối hoặc làm sáng các bóng tối.  
- **Input Highlight Level:** Kiểm soát các phần sáng nhất.  
- **Output Shadow/Highlight Levels:** Xác định dải đầu ra cuối cùng.

Bạn có thể thử nghiệm với các giá trị khác nhau để xem chúng ảnh hưởng như thế nào đến hình ảnh.

### Bước 5: Lưu Tệp PSD Đã Sửa
Lưu các thay đổi của bạn vào một tệp mới.
```java
im.save(psdPathAfterChange);
```
Bạn sẽ tìm thấy tệp PSD đã cập nhật tại vị trí bạn chỉ định trong `psdPathAfterChange`.

## Các Vấn Đề Thường Gặp và Giải Pháp
- **File not found:** Kiểm tra `dataDir` có trỏ đúng thư mục và PSD nguồn tồn tại.  
- **ClassCastException:** Đảm bảo tệp bạn tải thực sự là PSD; các định dạng khác yêu cầu lớp khác.  
- **License errors:** Sử dụng giấy phép Aspose.PSD hợp lệ cho bản dựng sản xuất; bản dùng thử hoạt động cho phát triển.

## Kết luận
Bạn giờ đã biết **cách điều chỉnh mức** bằng cách thêm và cấu hình Level Adjustment Layer trong tệp PSD với Aspose.PSD for Java. Kỹ thuật này cho phép bạn kiểm soát chính xác cân bằng tông màu đồng thời giữ quy trình làm việc hoàn toàn tự động. Tiếp tục thử nghiệm với các giá trị kênh khác nhau và khám phá xử lý hàng loạt để áp dụng cùng một điều chỉnh cho nhiều hình ảnh.

## Câu Hỏi Thường Gặp

**Q: Level Adjustment Layer là gì?**  
A: Đó là một lớp không phá hủy cho phép bạn thay đổi dải tông màu (bóng tối, tông trung, điểm sáng) của hình ảnh.

**Q: Tôi có thể sử dụng Aspose.PSD mà không mua giấy phép không?**  
A: Có, bạn có thể đánh giá thư viện bằng bản dùng thử miễn phí, nhưng cần giấy phép cho triển khai thương mại.

**Q: Tôi có thể tìm tài liệu cho Aspose.PSD ở đâu?**  
A: Bạn có thể tìm tài liệu [tại đây](https://reference.aspose.com/psd/java/).

**Q: Có hỗ trợ cộng đồng cho các sản phẩm Aspose không?**  
A: Chắc chắn! Bạn có thể đặt câu hỏi và nhận trợ giúp trong [diễn đàn Aspose](https://forum.aspose.com/c/psd/34).

**Q: Làm sao tôi có thể lấy giấy phép tạm thời cho Aspose.PSD?**  
A: Bạn có thể đăng ký giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

**Cập nhật lần cuối:** 2026-03-07  
**Kiểm tra với:** Phiên bản mới nhất của Aspose.PSD (Java)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}