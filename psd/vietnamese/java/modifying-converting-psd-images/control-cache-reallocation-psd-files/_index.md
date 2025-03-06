---
title: Kiểm soát việc phân bổ lại bộ đệm trong tệp PSD
linktitle: Kiểm soát việc phân bổ lại bộ đệm trong tệp PSD
second_title: API Java Aspose.PSD
description: Quản lý phân bổ lại bộ đệm trong tệp PSD bằng Aspose.PSD cho Java. Tìm hiểu cách tối ưu hóa bộ nhớ và xử lý tệp một cách hiệu quả—lý tưởng cho các nhà phát triển.
weight: 22
url: /vi/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kiểm soát việc phân bổ lại bộ đệm trong tệp PSD

## Giới thiệu
Khi làm việc với hình ảnh và tệp Photoshop theo chương trình, hiệu quả là yếu tố then chốt. Aspose.PSD cho Java cung cấp các tính năng mạnh mẽ để quản lý và thao tác các tệp PSD một cách liền mạch. Một trong những khía cạnh cơ bản của việc tối ưu hóa hiệu suất là kiểm soát việc phân bổ lại bộ đệm. Quản lý bộ đệm giúp duy trì sự cân bằng giữa việc sử dụng bộ nhớ và ổ đĩa, đảm bảo ứng dụng của bạn chạy trơn tru, không gặp sự cố hoặc chậm đột ngột. 
## Điều kiện tiên quyết
Trước khi chuyển sang phần mã hóa, có một số điều bạn cần đảm bảo để mọi thứ diễn ra suôn sẻ:
1. Bộ công cụ phát triển Java (JDK): Đảm bảo rằng bạn đã cài đặt JDK trên máy của mình. Bạn có thể tải nó xuống từ[trang web của Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Bạn cần tải xuống thư viện Aspose.PSD. Bạn có thể tìm thấy bản phát hành mới nhất[đây](https://releases.aspose.com/psd/java/).
3. Thiết lập IDE: Môi trường phát triển tích hợp (IDE) như IntelliJ IDEA hoặc Eclipse sẽ giúp bạn quản lý mã của mình dễ dàng hơn.
4. Hiểu biết cơ bản về Java: Làm quen với lập trình Java sẽ giúp bạn hiểu rõ hơn các khái niệm và đoạn mã.
5.  Giấy phép Aspose (Tùy chọn): Nếu bạn muốn xóa hình mờ và có được đầy đủ chức năng, hãy cân nhắc việc mua giấy phép[đây](https://purchase.aspose.com/buy) hoặc dùng thử miễn phí[đây](https://releases.aspose.com/).
## Gói nhập khẩu
Trước khi bắt đầu viết mã, hãy đảm bảo rằng chúng ta đã nhập các gói cần thiết. Dưới đây là danh sách ngắn gọn những gì cần đưa vào đầu tệp Java của bạn:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```
## Bước 1: Thiết lập thư mục dữ liệu của bạn
Trước tiên, bạn cần thiết lập một thư mục nơi bạn muốn lưu trữ các tệp bộ đệm của mình. Điều này rất cần thiết để quản lý bộ đệm hiệu quả.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- Chuỗi dataDir: Xác định thư mục cho bộ đệm tài liệu của bạn.
- Cache.setCacheFolder(dataDir): Phương thức này đặt thư mục bộ đệm vào thư mục đã chỉ định. Mọi bộ đệm được tạo bởi Aspose giờ đây sẽ được lưu trữ ở đây thay vì thư mục tạm thời mặc định.
## Bước 2: Cấu hình bộ đệm vào đĩa
Tiếp theo, chúng tôi sẽ chỉ định rằng chúng tôi muốn bộ đệm của mình chỉ được lưu trữ trên đĩa. Điều này đặc biệt hữu ích nếu ứng dụng của bạn sử dụng các tệp lớn và bạn muốn đảm bảo rằng bộ nhớ vẫn còn trống.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): Tùy chọn này đảm bảo rằng bộ đệm không được giữ trong bộ nhớ, điều này có lợi cho việc xử lý các tệp PSD lớn mà không tiêu tốn quá nhiều RAM.
## Bước 3: Đặt kích thước bộ nhớ đệm và đĩa tối đa
Bây giờ, hãy hạn chế kích thước bộ đệm của chúng tôi. Điều này rất quan trọng vì bộ nhớ đệm không giới hạn có thể dẫn đến các vấn đề về hiệu suất.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- Cache.setMaxDiskSpaceForCache(1073741824): Điều này đặt giới hạn 1 GB cho bộ đệm trên đĩa. Bạn có thể điều chỉnh kích thước này tùy theo nhu cầu của bạn.
- Cache.setMaxMemoryForCache(1073741824): Tương tự, điều này hạn chế bộ đệm trong bộ nhớ, đảm bảo rằng ứng dụng của bạn không sử dụng quá nhiều bộ nhớ.
## Bước 4: Quản lý chiến lược phân bổ lại bộ đệm
Quản lý cách phân bổ lại bộ đệm là điều cần thiết để duy trì hiệu suất. Đây là cách bạn có thể thiết lập nó.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): Khi được đặt thành false, điều này cho phép Aspose quản lý việc phân bổ lại bộ đệm linh hoạt hơn, điều này có thể dẫn đến hiệu suất tốt hơn.
## Bước 5: Kiểm tra kích thước bộ đệm được phân bổ
Bước này nhằm mục đích giám sát số byte hiện được phân bổ cho bộ đệm trong bộ nhớ hoặc trên đĩa. Hãy thực hiện điều đó:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: Lưu trữ số byte được phân bổ trên đĩa.
- long l2: Lưu trữ số byte được phân bổ trong bộ nhớ. 
Bạn có thể kiểm tra các giá trị này bất kỳ lúc nào để đảm bảo ứng dụng của bạn đang quản lý mức sử dụng bộ nhớ và ổ đĩa như mong đợi.
## Bước 6: Tạo hình ảnh PSD
Bây giờ chúng ta đã thiết lập xong cấu hình bộ đệm, hãy tạo một hình ảnh PSD đơn giản.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- Tùy chọn PsdOptions: Đối tượng này cho phép bạn chỉ định các tùy chọn khi tạo hình ảnh Photoshop.
- Màu sắc[] color: Một mảng chứa các màu sẽ được sử dụng trong bảng màu hình ảnh.
## Bước 7: Lưu dữ liệu pixel vào hình ảnh
Bây giờ, hãy điền vào hình ảnh của chúng ta dữ liệu pixel và lưu nó.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Màu sắc[] pixel: Đây là một mảng các đối tượng màu. Ở đây, chúng ta đang lấp đầy nó bằng các pixel màu trắng.
- image.savePixels(image.getBounds(), pixels): Phương thức này lưu dữ liệu pixel vào hình ảnh. Nó cập nhật hình ảnh với màu sắc mà chúng ta đã xác định.
## Bước 8: Giám sát bộ đệm được phân bổ sau khi tạo hình ảnh
Sau khi tạo hình ảnh, bạn nên kiểm tra lại xem có bao nhiêu byte được phân bổ cho bộ đệm.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- đĩa dàiBytes: Ghi lại phân bổ hiện tại trên đĩa sau khi tạo hình ảnh.
- bộ nhớ dàiBytes: Ghi lại phân bổ hiện tại trong bộ nhớ. 
Bước này sẽ giúp bạn xác định lượng bộ nhớ đệm đang được sử dụng sau các thao tác của bạn.
## Bước 9: Kiểm tra việc thải bỏ đúng cách
Cuối cùng, điều quan trọng là phải đảm bảo rằng tất cả các đối tượng Aspose.PSD được xử lý đúng cách để tránh rò rỉ bộ nhớ.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 và l2: Các biến này sẽ giúp bạn kiểm tra việc phân bổ cuối cùng. Nếu chúng khác 0, điều đó cho thấy một số đồ vật chưa được xử lý đúng cách.
## Phần kết luận
Kiểm soát việc phân bổ lại bộ đệm trong Aspose.PSD cho Java có thể tạo ra sự khác biệt đáng kể về hiệu suất ứng dụng của bạn. Bằng cách làm theo các bước được nêu ở trên, bạn có thể quản lý bộ nhớ đệm một cách hiệu quả, giảm thiểu mức sử dụng bộ nhớ và tạo các tệp PSD đẹp mắt một cách hiệu quả. Hãy nắm bắt những kỹ thuật này và xem ứng dụng của bạn phát triển mạnh mẽ với hiệu suất tối ưu!
## Câu hỏi thường gặp
### Aspose.PSD là gì?
Aspose.PSD là thư viện dành cho các nhà phát triển .NET và Java để tạo, thao tác và chuyển đổi các tệp Photoshop (PSD) theo chương trình.
### Làm cách nào để kiểm tra kích thước bộ đệm được phân bổ?
 Sử dụng các phương pháp như`Cache.getAllocatedDiskBytesCount()` Và`Cache.getAllocatedMemoryBytesCount()` để theo dõi việc sử dụng bộ đệm hiện tại.
### Tôi có thể đặt thư mục tùy chỉnh cho bộ đệm không?
 Có, bạn có thể chỉ định một thư mục khác bằng cách sử dụng`Cache.setCacheFolder("Your Directory Path")`.
### Aspose.PSD có được sử dụng miễn phí không?
Aspose.PSD là một thư viện trả phí, nhưng bạn có thể bắt đầu với bản dùng thử miễn phí có sẵn trên[trang web](https://releases.aspose.com/).
### Điều gì xảy ra nếu tôi không vứt bỏ đồ vật?
Việc không xử lý các đối tượng có thể dẫn đến rò rỉ bộ nhớ, khiến ứng dụng của bạn sử dụng nhiều tài nguyên hơn mức cần thiết.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
