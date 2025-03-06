---
title: Áp dụng các lớp điều chỉnh trong tệp PSD bằng Java
linktitle: Áp dụng các lớp điều chỉnh trong tệp PSD bằng Java
second_title: API Java Aspose.PSD
description: Tìm hiểu cách áp dụng các lớp điều chỉnh trong tệp PSD bằng Aspose.PSD cho Java trong hướng dẫn từng bước đầy đủ này dành cho nhà phát triển.
weight: 15
url: /vi/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Áp dụng các lớp điều chỉnh trong tệp PSD bằng Java

## Giới thiệu
Bạn có phải là nhà phát triển Java đang tìm cách cải thiện hình ảnh được lưu trữ trong tệp PSD không? Nếu vậy, bạn đang ở đúng nơi! Trong bài viết này, chúng ta sẽ khám phá cách áp dụng các lớp điều chỉnh trong tệp PSD bằng thư viện Aspose.PSD cho Java. Cho dù bạn đang làm việc trên một dự án cá nhân hay một ứng dụng chuyên nghiệp, việc hiểu cách thao tác với các tệp PSD có thể nâng cao đáng kể khả năng của phần mềm của bạn. 

## Điều kiện tiên quyết
Trước khi chúng ta chuyển sang mã và bắt đầu áp dụng các lớp điều chỉnh đó, bạn cần có một số điều kiện tiên quyết:
1. Bộ công cụ phát triển Java (JDK): Đảm bảo rằng bạn đã cài đặt JDK trên máy của mình. Bạn có thể tải nó xuống từ[trang web của Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Thư viện Aspose.PSD: Nếu chưa có, bạn sẽ cần tải xuống thư viện Aspose.PSD cho Java. Bạn có thể tìm thấy nó[đây](https://releases.aspose.com/psd/java/).
3. Môi trường phát triển: Thiết lập môi trường phát triển tích hợp Java (IDE) như IntelliJ IDEA hoặc Eclipse nơi bạn sẽ viết và chạy mã của mình.
4. Làm quen cơ bản với Java: Hiểu biết chung về lập trình Java sẽ giúp bạn thực hiện suôn sẻ.
5. Tệp PSD: Có sẵn một vài tệp PSD cho mục đích thử nghiệm. Bạn có thể tạo một số bằng cách sử dụng Adobe Photoshop hoặc tải xuống các tệp mẫu từ internet.
## Gói nhập khẩu
Trước khi bắt đầu viết mã, hãy làm rõ những gói chúng ta cần nhập. Aspose.PSD cho phép chúng ta làm việc với các tệp Photoshop theo nhiều cách khác nhau, vì vậy hãy lấy các lớp cần thiết để xử lý hình ảnh PSD và các lớp điều chỉnh.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```
Bây giờ chúng ta đã có sẵn các gói, hãy chia nhỏ các ví dụ theo từng bước!
## Bước 1: Tải tệp PSD
Bước đầu tiên trong hành trình của chúng ta là tải tệp PSD. Đây là tệp chúng tôi sẽ làm việc để áp dụng các lớp điều chỉnh của mình.
```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```
 Trong đoạn mã này, chúng tôi xác định thư mục chứa các tệp PSD của chúng tôi và tải tệp cụ thể mà chúng tôi muốn thao tác. Đảm bảo thay thế`"Your Document Directory"` với đường dẫn thực tế tới các tệp PSD trên máy của bạn.
## Bước 2: Lặp lại các lớp
Bây giờ chúng ta đã tải tệp PSD, chúng ta sẽ duyệt qua các lớp của nó để tìm các lớp điều chỉnh của mình.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) im.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(im.getLayers()[0]);
        }
    }
}
```
 Trong bước này, chúng tôi lặp qua từng lớp trong tệp PSD để xác định bất kỳ lớp nào thuộc về`AdjustmentLayer` kiểu. Nếu tìm thấy, chúng tôi hợp nhất nó với lớp cơ sở, thường là lớp đầu tiên (`im.getLayers()[0]`). Quá trình hợp nhất này áp dụng hiệu quả các điều chỉnh cho hình ảnh của chúng tôi. 
## Bước 3: Lưu tệp PSD đã sửa đổi
Sau khi sửa đổi các lớp, điều quan trọng là phải lưu những thay đổi mà chúng ta đã thực hiện. Hãy thực hiện điều này trong bước tiếp theo.
```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```
 Ở đây, chúng tôi chỉ định đường dẫn xuất cho tệp PSD đã sửa đổi của mình và gọi`save()` phương pháp ghi các thay đổi của chúng tôi vào đĩa.
## Bước 4: Lớp điều chỉnh cấp độ
Hãy lặp lại quy trình cho một loại lớp điều chỉnh khác: lớp điều chỉnh Cấp độ. 
### Tải lớp điều chỉnh mức PSD
```java
String sourceFileName2 = dataDir + "LevelsAdjustmentLayerRgb.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName2);
```
Như trước đây, chúng tôi tải tệp PSD chứa lớp điều chỉnh Cấp độ của chúng tôi. 
### Lặp lại qua các lớp cấp độ
Tiếp theo, chúng ta sẽ lặp lại các lớp một lần nữa, giống như chúng ta đã làm trước đây, nhưng bây giờ chúng ta đang làm việc với một tệp PSD khác.
```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) img.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(img.getLayers()[0]);
        }
    }
}
```
Mã này hoạt động tương tự như lần lặp trước đó; nó tìm kiếm các lớp điều chỉnh trong tệp PSD hiện tại, cho phép chúng tôi áp dụng bất kỳ điều chỉnh nào có sẵn.
## Lưu PSD lớp điều chỉnh cấp độ
Cuối cùng, chúng tôi sẽ lưu tệp mới này sau khi áp dụng các điều chỉnh.
```java
String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";
img.save(exportPath2);
```
Bây giờ, chúng ta đã xử lý thành công lớp điều chỉnh Levels!
## Phần kết luận
Chúc mừng! Bạn vừa học cách áp dụng các lớp điều chỉnh trong tệp PSD bằng cách sử dụng thư viện Java và Aspose.PSD. Cho dù bạn đang điều chỉnh màu sắc hay điều chỉnh mức độ, giờ đây bạn đã có các kỹ năng cơ bản để thao tác với các tệp PSD theo chương trình.
Việc sử dụng Aspose.PSD có thể hợp lý hóa đáng kể quy trình công việc chỉnh sửa hình ảnh, cho phép tự động hóa và tùy chỉnh theo những cách mà các công cụ truyền thống không thể thực hiện được. Đừng ngần ngại khám phá thêm thư viện và thử nghiệm các loại lớp khác nhau để xem có những khả năng sáng tạo nào.
## Câu hỏi thường gặp
### Thư viện Aspose.PSD là gì?
Aspose.PSD là thư viện cho phép các nhà phát triển tải, thao tác và lưu các tệp Photoshop PSD trong các ứng dụng Java.
### Tôi có thể sử dụng Aspose.PSD miễn phí không?
 Đúng! Aspose cung cấp bản dùng thử miễn phí để bạn khám phá thư viện của họ. Bạn có thể đăng ký[đây](https://releases.aspose.com/).
### Tôi có cần cài đặt Photoshop để sử dụng Aspose.PSD không?
Không, bạn không cần Photoshop. Aspose.PSD hoạt động độc lập để thao tác các tệp PSD theo chương trình.
### Tôi có thể tìm tài liệu về Aspose.PSD ở đâu?
Bạn có thể truy cập trang tài liệu[đây](https://reference.aspose.com/psd/java/) để khám phá các tính năng, lớp và phương thức.
### Làm cách nào để nhận được hỗ trợ cho các sản phẩm Aspose?
 Bạn có thể truy cập hỗ trợ thông qua[diễn đàn giả định](https://forum.aspose.com/c/psd/34) nơi bạn có thể đặt câu hỏi và tìm giải pháp.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
