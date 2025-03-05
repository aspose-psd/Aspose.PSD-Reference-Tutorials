---
title: Làm phẳng các lớp trong tệp PSD bằng cách sử dụng Aspose.PSD Java
linktitle: Làm phẳng các lớp trong tệp PSD bằng cách sử dụng Aspose.PSD Java
second_title: API Java Aspose.PSD
description: Làm phẳng và hợp nhất các lớp trong tệp PSD một cách dễ dàng bằng Aspose.PSD cho Java. Hãy làm theo hướng dẫn từng bước này để đơn giản hóa việc quản lý tệp PSD của bạn.
type: docs
weight: 13
url: /vi/java/psd-layer-management-effects/flatten-layers-psd-files/
---
## Giới thiệu

Bạn đã bao giờ thấy mình làm việc với các tệp Photoshop và mong muốn có một cách dễ dàng hơn để quản lý các lớp phức tạp đó chưa? Vâng, bạn thật may mắn! Hôm nay, chúng ta sẽ đi sâu vào thế giới Aspose.PSD cho Java, một công cụ mạnh mẽ giúp bạn dễ dàng làm việc với các tệp PSD theo chương trình. Một trong những tính năng tiện dụng mà chúng ta sẽ khám phá là làm phẳng các lớp. Cho dù bạn muốn làm phẳng toàn bộ hình ảnh hay hợp nhất có chọn lọc các lớp cụ thể, Aspose.PSD cho Java đều đáp ứng được nhu cầu của bạn. Hướng dẫn này sẽ hướng dẫn bạn thực hiện quy trình, từng bước một, đảm bảo bạn sẵn sàng xử lý các tệp PSD của mình một cách tự tin.

## Điều kiện tiên quyết

Trước khi chúng ta chuyển sang mã, hãy đảm bảo bạn có mọi thứ bạn cần:

1. Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt JDK 8 trở lên trên hệ thống của mình.
2.  Aspose.PSD cho Java: Tải xuống và thêm thư viện Aspose.PSD vào dự án của bạn. Bạn có thể tìm thấy nó[đây](https://releases.aspose.com/psd/java/).
3. Môi trường phát triển tích hợp (IDE): Một IDE như IntelliJ IDEA hoặc Eclipse sẽ giúp trải nghiệm mã hóa của bạn mượt mà hơn.
4. Kiến thức cơ bản về Java: Mặc dù hướng dẫn này thân thiện với người mới bắt đầu nhưng một số kiến thức cơ bản về Java sẽ giúp bạn theo dõi dễ dàng hơn.
5. Tệp PSD mẫu: Chuẩn bị sẵn tệp PSD để thử nghiệm. Chúng ta sẽ sử dụng một lớp có nhiều lớp để minh họa quá trình làm phẳng.

Bây giờ chúng ta đã nắm được những điều cần thiết, hãy chuyển sang phần thú vị—làm việc với mã!

## Gói nhập khẩu

Để bắt đầu, bạn cần nhập các gói cần thiết vào dự án Java của mình. Các gói này sẽ cho phép bạn làm việc với các tệp PSD bằng Aspose.PSD cho Java.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

Những lần nhập này sẽ cho phép chúng tôi tải các tệp PSD, thao tác các lớp và lưu các thay đổi. Bây giờ, hãy chia quá trình làm phẳng các lớp thành các bước có thể quản lý được.

## Bước 1: Làm phẳng toàn bộ hình ảnh PSD

Nhiệm vụ đầu tiên là làm phẳng toàn bộ hình ảnh PSD. Điều này rất hữu ích khi bạn muốn kết hợp tất cả các lớp thành một lớp duy nhất, giúp quản lý và xuất hình ảnh dễ dàng hơn.

### 1.1 Tải tệp PSD

 Đầu tiên, chúng ta sẽ tải tệp PSD vào chương trình của mình. Tệp này phải được đặt trong thư mục dự án của bạn, chúng tôi sẽ gọi nó là`Your Document Directory`.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Đoạn mã này tải tệp PSD có tên`ThreeRegularLayersSemiTransparent.psd` từ thư mục được chỉ định của bạn.

### 1.2 Làm phẳng hình ảnh

Tiếp theo, chúng ta sẽ làm phẳng toàn bộ hình ảnh. Làm phẳng kết hợp tất cả các lớp có thể nhìn thấy thành một lớp nền duy nhất.

```java
im.flattenImage();
```

Với lớp lót này, tất cả các lớp trong tệp PSD của bạn sẽ được hợp nhất thành một.

### 1.3 Lưu ảnh đã được làm phẳng

Cuối cùng, chúng ta sẽ lưu hình ảnh đã được làm phẳng vào một file mới.

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

 Thao tác này sẽ lưu tệp PSD đã được làm phẳng dưới tên mới`ThreeRegularLayersSemiTransparentFlattened.psd`. Chúc mừng! Bạn vừa làm phẳng hình ảnh PSD đầu tiên của mình bằng Aspose.PSD cho Java.

## Bước 2: Hợp nhất các lớp cụ thể

Đôi khi, bạn có thể không muốn làm phẳng toàn bộ hình ảnh mà chỉ hợp nhất một số lớp nhất định. Hãy xem làm thế nào bạn có thể đạt được điều đó.

### 2.1 Tải lại tệp PSD

Vì chúng ta đang thực hiện một thao tác khác nên hãy bắt đầu bằng cách tải lại tệp PSD.

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

Thao tác này sẽ tải cùng một tệp PSD, sẵn sàng cho các hoạt động theo từng lớp cụ thể.

### 2.2 Xác định và chọn lớp

Để hợp nhất các lớp cụ thể, trước tiên, hãy xác định và chọn các lớp bạn muốn hợp nhất.

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

Ở đây, chúng tôi đang chọn lớp đầu tiên, thứ hai và thứ ba của tệp PSD. Các lớp này được lưu trữ trong một mảng và bạn có thể truy cập chúng theo chỉ mục của chúng.

### 2.3 Hợp nhất các lớp

Bây giờ, hãy hợp nhất các lớp đã chọn. Chúng ta sẽ bắt đầu bằng cách hợp nhất các lớp dưới cùng và giữa, sau đó hợp nhất kết quả với lớp trên cùng.

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

Mã này hợp nhất các lớp một cách tuần tự, tạo thành một lớp kết hợp duy nhất.

### 2.4 Thay thế các lớp hiện có bằng lớp đã hợp nhất

Sau khi hợp nhất, bạn cần thay thế các lớp hiện có trong ảnh bằng lớp mới được hợp nhất.

```java
img.setLayers(new Layer[]{layer2});
```

Bước này đảm bảo rằng hình ảnh bây giờ chỉ chứa lớp đã hợp nhất.

### 2.5 Lưu tệp PSD đã cập nhật

Cuối cùng, lưu tệp PSD đã cập nhật với các lớp đã hợp nhất.

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

Thao tác này sẽ lưu PSD với các lớp đã hợp nhất dưới một tên mới, cho phép bạn giữ nguyên tệp gốc.

## Phần kết luận

Làm việc với các lớp trong tệp PSD thường có thể có cảm giác giống như đang điều hướng một mê cung, nhưng với Aspose.PSD cho Java, điều đó giống như bạn có một bản đồ trong tay. Cho dù bạn cần làm phẳng toàn bộ hình ảnh hay hợp nhất các lớp đã chọn một cách cẩn thận, Aspose.PSD sẽ đơn giản hóa quy trình, biến những gì có thể là một nhiệm vụ khó khăn thành một thao tác đơn giản. Bằng cách làm theo hướng dẫn này, giờ đây bạn có thể thoải mái xử lý thao tác lớp trong tệp PSD bằng Java. Vậy tại sao bạn không thử thực hiện các dự án của riêng mình và xem bạn tiết kiệm được bao nhiêu thời gian và công sức?

## Câu hỏi thường gặp

### Tôi có thể hoàn tác việc làm phẳng các lớp trong Aspose.PSD không?  
Không, sau khi bạn làm phẳng các lớp bằng Aspose.PSD, hành động này sẽ không thể thay đổi được. Luôn luôn là một cách tốt để sao lưu tệp gốc.

### Có thể chỉ làm phẳng các lớp nhìn thấy được không?  
 Có, bạn có thể kiểm soát lớp nào sẽ được làm phẳng dựa trên khả năng hiển thị của chúng. Đảm bảo chỉ có các lớp bạn muốn làm phẳng mới hiển thị trước khi sử dụng`flattenImage` phương pháp.

### Các lớp làm phẳng có làm giảm kích thước tập tin không?  
Làm phẳng các lớp có thể làm giảm kích thước tệp, đặc biệt nếu có nhiều lớp phức tạp. Tuy nhiên, mức giảm chính xác còn phụ thuộc vào nội dung của các lớp.

### Tôi có thể hợp nhất các lớp với các chế độ hòa trộn khác nhau không?  
Có, bạn có thể hợp nhất các lớp với các chế độ hòa trộn khác nhau bằng Aspose.PSD và lớp kết quả sẽ duy trì giao diện của các lớp đã hợp nhất.

### Điều gì xảy ra nếu tôi cố gắng hợp nhất các lớp không liền kề nhau?  
Aspose.PSD cho phép bạn hợp nhất bất kỳ lớp nào bất kể thứ tự của chúng trong ngăn xếp lớp. Quá trình hợp nhất sẽ kết hợp các lớp đã chọn theo quy định.