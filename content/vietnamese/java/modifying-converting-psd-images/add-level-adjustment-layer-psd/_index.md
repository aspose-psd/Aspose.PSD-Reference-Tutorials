---
title: Thêm lớp điều chỉnh cấp độ trong PSD
linktitle: Thêm lớp điều chỉnh cấp độ trong PSD
second_title: API Java Aspose.PSD
description: Tìm hiểu cách thêm Lớp điều chỉnh cấp độ một cách hiệu quả trong các tệp PSD của bạn bằng Aspose.PSD cho Java. Nâng cao kỹ năng chỉnh sửa hình ảnh của bạn.
type: docs
weight: 16
url: /vi/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---
## Giới thiệu
Khi nói đến chỉnh sửa hình ảnh, việc quản lý các cấp độ có thể tạo nên sự khác biệt lớn về độ sống động và độ rõ nét cho ảnh của bạn. Một công cụ tiện dụng trong kho Photoshop là "Lớp điều chỉnh cấp độ", cho phép bạn điều chỉnh phạm vi tông màu và cân bằng màu sắc của hình ảnh. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn cách triển khai Lớp điều chỉnh cấp độ trong tệp PSD bằng Aspose.PSD cho Java. Vì vậy, hãy lấy Java IDE của bạn.
## Điều kiện tiên quyết
Trước khi bước vào thế giới điều chỉnh cấp độ, bạn sẽ cần thiết lập một số điều để đảm bảo chuyến đi suôn sẻ:
1.  Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt JDK trên máy của mình. Nếu bạn không có nó, bạn có thể lấy nó từ[Trang web của Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) hoặc sử dụng OpenJDK.
2.  Aspose.PSD for Java Library: Để thao tác với tệp PSD, bạn cần tải xuống thư viện Aspose.PSD. Bạn có thể lấy phiên bản mới nhất từ đây[liên kết tải xuống](https://releases.aspose.com/psd/java/) và đảm bảo bạn đã đưa JAR vào thư viện dự án của mình.
3. Kiến thức cơ bản về Java: Hiểu biết cơ bản về lập trình Java sẽ giúp ích vì chúng ta sẽ đi sâu vào các đoạn mã trong suốt hướng dẫn này.
4. Thiết lập IDE: Bạn có thể sử dụng bất kỳ IDE Java nào mà bạn thích—như IntelliJ IDEA, Eclipse hoặc NetBeans—để viết và chạy mã của mình. Chỉ cần đảm bảo rằng bạn đã thiết lập dự án Java của mình và thêm thư viện Aspose.PSD.

## Gói nhập khẩu
Trước khi bắt đầu viết mã, chúng ta cần nhập các gói cần thiết từ thư viện Aspose.PSD. Đây là cách bạn có thể làm điều đó:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Bằng cách nhập các gói này, chúng tôi sẽ có quyền truy cập vào các lớp cần thiết để tải, sửa đổi và lưu các tệp PSD của mình.

Bây giờ, hãy chia nhỏ quy trình thành các bước dễ hiểu. Hãy làm theo khi chúng tôi hướng dẫn tải tệp PSD, điều chỉnh mức độ và sau đó lưu các thay đổi của bạn. 
## Bước 1: Thiết lập đường dẫn tệp của bạn
Bước đầu tiên là xác định vị trí tệp PSD của chúng tôi và nơi chúng tôi muốn lưu đầu ra đã sửa đổi. Bạn có thể tùy chỉnh đường dẫn thư mục cho phù hợp với nhu cầu của mình.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 Ở đây thay thế`"Your Document Directory"`với đường dẫn thực tế trên hệ thống nơi lưu trữ tệp PSD của bạn. Điều này tạo tiền đề cho mọi việc chúng ta sẽ làm tiếp theo.
## Bước 2: Tải tệp PSD
 Bây giờ, hãy tải tệp PSD bằng cách sử dụng`PsdImage` lớp học. Bước này rất cần thiết vì nó cho phép chúng ta truy cập và thao tác các lớp.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Khi bạn gọi`Image.load()` , nó sẽ đọc tệp PSD và tạo một phiên bản của`PsdImage` mà bạn có thể làm việc cùng.
## Bước 3: Lặp lại qua các lớp
Vì chúng tôi muốn điều chỉnh Lớp điều chỉnh cấp độ, nên chúng tôi sẽ cần lặp qua từng lớp trong tệp PSD của mình. Điều này giúp chúng tôi tìm thấy lớp cụ thể mà chúng tôi muốn sửa đổi.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Thao tác tiếp theo sẽ diễn ra ở đây...
    }
}
```
 Trong vòng lặp này,`instanceof LevelsLayer` kiểm tra xem lớp hiện tại có phải là Lớp điều chỉnh cấp độ hay không. Nếu đúng như vậy, chúng ta có thể tiến hành điều chỉnh các thuộc tính của nó.
## Bước 4: Điều chỉnh cài đặt kênh cấp độ
Khi chúng tôi xác định được lớp chính xác, chúng tôi có thể sửa đổi mức đầu vào và đầu ra của nó. Đây là nơi phép thuật xảy ra! Điều chỉnh các thông số khác nhau để xem chúng ảnh hưởng như thế nào đến hình ảnh.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Đây là chức năng của từng tham số:
- Mức âm trung đầu vào: Điều chỉnh âm trung.
- Mức độ bóng đầu vào: Tinh chỉnh các vùng tối hơn của hình ảnh.
- Mức độ nổi bật đầu vào: Thay đổi vùng sáng của hình ảnh.
- Mức độ bóng đầu ra: Đặt cách bóng tối sẽ xuất hiện.
- Mức độ nổi bật đầu ra: Đặt cách các điểm sáng sẽ xuất hiện.
Hãy thoải mái thử nghiệm với các giá trị khác nhau!
## Bước 5: Lưu tệp PSD đã sửa đổi
Bây giờ chúng ta đã thực hiện các điều chỉnh của mình, đã đến lúc lưu tệp PSD đã sửa đổi. Bước này rất quan trọng để đảm bảo rằng những thay đổi của bạn được áp dụng và lưu trữ.
```java
im.save(psdPathAfterChange);
```
 Bây giờ bạn có thể tìm thấy tệp PSD đã điều chỉnh của mình tại địa chỉ được chỉ định`psdPathAfterChange`. 
## Phần kết luận
Bạn vừa học cách thêm Lớp điều chỉnh cấp độ vào tệp PSD bằng Aspose.PSD cho Java! Bằng cách làm theo hướng dẫn này, bạn có thể dễ dàng điều chỉnh chất lượng tông màu của hình ảnh, mở đường cho kết quả sống động và hấp dẫn hơn về mặt hình ảnh. Hãy nhớ rằng, luyện tập sẽ tạo nên sự hoàn hảo, vì vậy, hãy thoải mái điều chỉnh các điều chỉnh và khám phá các tệp PSD khác nhau để xem tác động của những thay đổi của bạn.
## Câu hỏi thường gặp
### Lớp điều chỉnh cấp độ là gì?
Lớp điều chỉnh cấp độ cho phép bạn điều chỉnh phạm vi tông màu trong hình ảnh, cân bằng bóng, tông trung tính và vùng sáng.
### Tôi có thể sử dụng Aspose.PSD mà không cần mua hàng không?
Đúng! Aspose cung cấp bản dùng thử miễn phí để kiểm tra thư viện trước khi mua.
### Tôi có thể tìm tài liệu về Aspose.PSD ở đâu?
 Bạn có thể tìm thấy tài liệu[đây](https://reference.aspose.com/psd/java/).
### Có sự hỗ trợ cộng đồng nào cho các sản phẩm Aspose không?
 Tuyệt đối! Bạn có thể đặt câu hỏi và nhận hỗ trợ trong[diễn đàn giả định](https://forum.aspose.com/c/psd/34).
### Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.PSD?
 Bạn có thể xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).