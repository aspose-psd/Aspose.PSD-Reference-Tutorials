---
title: Đặt độ mờ tô cho các lớp PSD bằng Aspose.PSD Java
linktitle: Đặt độ mờ tô cho các lớp PSD bằng Aspose.PSD Java
second_title: API Java Aspose.PSD
description: Tìm hiểu cách đặt độ mờ tô cho các lớp PSD bằng Aspose.PSD cho Java trong hướng dẫn từng bước này. Nâng cao hiệu quả các dự án thiết kế đồ họa của bạn.
weight: 13
url: /vi/java/psd-image-modification-conversion/set-fill-opacity-psd-layers/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đặt độ mờ tô cho các lớp PSD bằng Aspose.PSD Java

## Giới thiệu
Bạn có thường thấy mình phải chỉnh sửa các file thiết kế, cố gắng đạt được hiệu ứng hình ảnh hoàn hảo đó không? Cho dù bạn là một nhà thiết kế đồ họa dày dạn hay một nhà phát triển mới bắt đầu muốn thao tác với các tệp PSD, việc biết cách điều chỉnh các thuộc tính của lớp có thể tạo ra sự khác biệt. Hôm nay, chúng ta sẽ đi sâu vào cách đặt độ mờ cho các lớp trong tệp PSD bằng Aspose.PSD cho Java. Bạn đã sẵn sàng biến các lớp của mình thành những phần bắt mắt chưa? Hãy bắt đầu!
## Điều kiện tiên quyết
Trước khi đi sâu vào mã, bạn cần đảm bảo có một số điều sau:
1.  Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt JDK trên máy của mình. Bạn có thể tải nó xuống từ[trang web của Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Thư viện Aspose.PSD cho Java: Bạn sẽ cần thiết lập Aspose.PSD cho Java trong dự án của mình. Bạn có thể tải xuống thư viện từ[Trang phát hành Aspose](https://releases.aspose.com/psd/java/).
3. IDE: Môi trường phát triển tích hợp như IntelliJ IDEA hoặc Eclipse sẽ giúp việc mã hóa trở nên đơn giản và dễ quản lý hơn.
4. Kiến thức Java cơ bản: Bạn cần có hiểu biết sâu sắc về các khái niệm lập trình Java để có thể thực hiện suôn sẻ.
5.  Tệp PSD của bạn: Chuẩn bị sẵn tệp PSD mẫu. Đối với hướng dẫn này, chúng tôi sẽ sử dụng một tệp có tên`FillOpacitySample.psd`.
## Gói nhập khẩu
Để bắt đầu viết mã, bạn cần nhập các gói Aspose.PSD cần thiết. Các gói này sẽ cung cấp cho bạn quyền truy cập vào chức năng cần thiết để thao tác với các tệp PSD.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```
Đặt các mục nhập này ở đầu tệp Java của bạn để đảm bảo bạn có thể sử dụng các lớp trong dự án của mình.

Bây giờ, hãy chia nhiệm vụ của chúng ta thành các bước có thể quản lý được để điều chỉnh độ mờ của màu tô đó như một người chuyên nghiệp!
## Bước 1: Xác định thư mục tài liệu
Trước tiên, bạn cần đặt thư mục tài liệu nơi chứa các tệp PSD. Đây là nơi bạn sẽ yêu cầu chương trình của mình tìm kiếm PSD mà bạn muốn thao tác.
```java
String dataDir = "Your Document Directory";
```
## Bước 2: Chỉ định đường dẫn nguồn và xuất
Tiếp theo, bạn sẽ xác định đường dẫn cho tệp nguồn của mình — đường dẫn bạn muốn điều chỉnh — và đường dẫn xuất nơi tệp PSD đã sửa đổi sẽ được lưu.
```java
String sourceFileName = dataDir + "FillOpacitySample.psd";
String exportPath = dataDir + "FillOpacitySampleChanged.psd";
```
## Bước 3: Tải tệp PSD
Bây giờ là lúc tải tệp PSD của bạn vào bộ nhớ bằng thư viện Aspose.PSD. Đây là nơi phép thuật thực sự bắt đầu!
```java
PsdImage im = (PsdImage)(Image.load(sourceFileName));
```
Những gì dòng này làm là chuyển đổi tệp PSD của bạn thành một đối tượng mà bạn có thể thao tác theo mã.
## Bước 4: Truy cập lớp
Trước khi điều chỉnh độ mờ của màu tô, bạn cần nhắm mục tiêu vào một lớp cụ thể. Trong ví dụ này, chúng tôi đang thao tác lớp thứ ba của tệp PSD. Bạn có thể điều chỉnh chỉ mục này dựa trên lớp bạn muốn làm việc.
```java
Layer layer = im.getLayers()[2];
```
 Lưu ý: Việc lập chỉ mục lớp bắt đầu từ 0, có nghĩa là`im.getLayers()[2]` đề cập đến lớp thứ ba.
## Bước 5: Đặt độ mờ điền
Đây là phần thú vị! Bạn có thể thay đổi độ mờ của lớp bạn đã chọn. Giá trị có thể nằm trong khoảng từ 0 (hoàn toàn trong suốt) đến 100 (hoàn toàn mờ).
```java
layer.setFillOpacity(5);
```
 Đặt nó thành`5` có nghĩa là lớp này sẽ rất mờ, cho phép các lớp bên dưới hiển thị rõ ràng.
## Bước 6: Lưu thay đổi
Sau khi thay đổi các thuộc tính mong muốn, bước cuối cùng của bạn là lưu tệp PSD mới và cải tiến vào đường dẫn xuất đã xác định.
```java
im.save(exportPath);
```
Và thế là xong! Bạn đã sửa đổi thành công độ mờ của lớp trong tệp PSD.
## Phần kết luận
Và bạn có nó! Bạn đã học cách thay đổi độ mờ của lớp trong tệp PSD bằng Aspose.PSD cho Java. Chỉ với một vài dòng mã, bạn có thể đạt được một số hiệu ứng thiết kế tuyệt vời giúp nâng tầm dự án đồ họa của bạn. Đừng ngần ngại thử nghiệm với các mức độ mờ khác nhau và khám phá các chức năng khác mà Aspose.PSD cung cấp.
## Câu hỏi thường gặp
### Độ mờ điền trong các lớp PSD là gì?
Độ mờ của lớp phủ xác định mức độ trong suốt của một lớp, ảnh hưởng đến mức độ hiển thị của các lớp bên dưới nó.
### Tôi có thể thay đổi độ mờ của nhiều lớp cùng một lúc không?
Có, bằng cách lặp qua các lớp bằng vòng lặp, bạn có thể đặt độ mờ cho từng lớp theo nhu cầu của mình.
### Aspose.PSD cho Java có được sử dụng miễn phí không?
 Bạn có thể bắt đầu với bản dùng thử miễn phí có sẵn tại[Giả định phát hành](https://releases.aspose.com/). Tuy nhiên, cần có giấy phép hợp lệ để sử dụng lâu dài.
### Tôi có thể thao tác những thuộc tính nào khác trong tệp PSD?
Bên cạnh độ mờ của lớp nền, bạn có thể thao tác mức độ hiển thị của lớp, chế độ hòa trộn, vị trí, kích thước, v.v. bằng cách sử dụng Aspose.PSD.
### Tôi có thể tìm thêm tài liệu về Aspose.PSD cho Java ở đâu?
 Bạn có thể tham khảo tài liệu đầy đủ[đây](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
