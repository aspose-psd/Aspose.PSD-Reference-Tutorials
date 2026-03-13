---
date: 2026-03-13
description: Học cách tạo các dự án Java xử lý ảnh PSD trong khi quản lý việc phân
  bổ lại bộ nhớ đệm với Aspose.PSD cho Java. Tối ưu hóa việc sử dụng bộ nhớ và đĩa
  một cách hiệu quả.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: Tạo ảnh PSD Java – Kiểm soát việc phân bổ lại bộ nhớ cache
url: /vi/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kiểm soát việc phân bổ lại bộ nhớ đệm trong tệp PSD

## Giới thiệu
Nếu bạn cần **create PSD image java** các dự án một cách hiệu quả, việc kiểm soát việc phân bổ lại bộ nhớ đệm là điều thiết yếu. Khi làm việc với hình ảnh và tệp Photoshop một cách lập trình, hiệu suất là yếu tố then chốt. Aspose.PSD for Java cung cấp các tính năng mạnh mẽ để quản lý và thao tác các tệp PSD một cách liền mạch. Một trong những khía cạnh cơ bản của việc tối ưu hiệu năng là kiểm soát việc phân bổ lại bộ nhớ đệm. Quản lý bộ nhớ đệm giúp duy trì cân bằng giữa việc sử dụng bộ nhớ và đĩa, đảm bảo ứng dụng của bạn chạy mượt mà, không gặp sự cố hoặc chậm trễ bất ngờ. 

## Câu trả lời nhanh
- **Cache reallocation làm gì?** Nó cân bằng việc sử dụng bộ nhớ và đĩa khi xử lý các tệp PSD lớn.  
- **Loại bộ nhớ đệm nào tốt nhất cho hình ảnh lớn?** `CacheOnDiskOnly` giữ cho bộ nhớ trống bằng cách lưu bộ nhớ đệm trên đĩa.  
- **Tôi có thể cấp bao nhiêu không gian đĩa?** Lên tới 1 GB (hoặc bất kỳ kích thước nào bạn đặt bằng `setMaxDiskSpaceForCache`).  
- **Tôi có cần giấy phép để sử dụng các tính năng này không?** Giấy phép sẽ loại bỏ các hạn chế của bản dùng thử; xem trang mua hàng của Aspose.  
- **Tôi có thể giám sát việc sử dụng bộ nhớ đệm trong thời gian chạy không?** Có, sử dụng `Cache.getAllocatedDiskBytesCount()` và `Cache.getAllocatedMemoryBytesCount()`.

## Tại sao cần kiểm soát việc phân bổ lại bộ nhớ đệm?
Quản lý bộ nhớ đệm là rất quan trọng khi bạn **create PSD image java** các ứng dụng xử lý các tệp có độ phân giải cao hoặc đa lớp. Cài đặt bộ nhớ đệm phù hợp ngăn ngừa lỗi hết bộ nhớ, giảm thời gian tạm dừng GC, và mang lại hiệu năng dự đoán được trên máy chủ hoặc ứng dụng desktop.

## Yêu cầu trước
Trước khi chúng ta nhảy vào phần mã, có một vài điều bạn cần đảm bảo để mọi thứ chạy trơn tru:
1. Java Development Kit (JDK): Đảm bảo rằng bạn đã cài đặt JDK trên máy của mình. Bạn có thể tải xuống từ [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Bạn cần tải xuống thư viện Aspose.PSD. Bạn có thể tìm phiên bản mới nhất [here](https://releases.aspose.com/psd/java/).
3. IDE Setup: Một môi trường phát triển tích hợp (IDE) như IntelliJ IDEA hoặc Eclipse sẽ giúp bạn quản lý mã dễ dàng hơn.
4. Basic Understanding of Java: Hiểu biết cơ bản về lập trình Java sẽ giúp bạn nắm bắt các khái niệm và đoạn mã tốt hơn.
5. Aspose License (Optional): Nếu bạn muốn loại bỏ watermark và có đầy đủ chức năng, hãy cân nhắc mua giấy phép [here](https://purchase.aspose.com/buy) hoặc thử bản dùng thử miễn phí [here](https://releases.aspose.com/).

## Nhập các gói
Trước khi bắt đầu viết mã, hãy chắc chắn rằng chúng ta đã nhập các gói cần thiết. Dưới đây là danh sách ngắn gọn những gì cần đưa vào đầu file Java của bạn:
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

## Cách tạo PSD Image Java với kiểm soát bộ nhớ đệm
Dưới đây là hướng dẫn từng bước liên kết cấu hình bộ nhớ đệm trực tiếp với quá trình tạo ảnh PSD trong Java.

### Bước 1: Thiết lập thư mục dữ liệu của bạn
Đầu tiên, bạn cần thiết lập một thư mục nơi bạn muốn lưu các tệp bộ nhớ đệm. Điều này rất cần thiết để quản lý bộ nhớ đệm một cách hiệu quả.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: Xác định thư mục cho bộ nhớ đệm tài liệu của bạn.  
- `Cache.setCacheFolder(dataDir)`: Phương thức này đặt thư mục bộ nhớ đệm thành thư mục đã chỉ định. Bất kỳ bộ nhớ đệm nào được tạo bởi Aspose sẽ được lưu ở đây thay vì thư mục tạm mặc định.

### Bước 2: Cấu hình bộ nhớ đệm lưu trên đĩa
Tiếp theo, chúng ta sẽ chỉ định rằng bộ nhớ đệm chỉ được lưu trên đĩa. Điều này đặc biệt hữu ích nếu ứng dụng của bạn sử dụng các tệp lớn và bạn muốn đảm bảo bộ nhớ vẫn trống.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: Tùy chọn này đảm bảo bộ nhớ đệm không được giữ trong bộ nhớ, có lợi cho việc xử lý các tệp PSD lớn mà không tiêu tốn quá nhiều RAM.

### Bước 3: Đặt kích thước tối đa cho bộ nhớ đệm trên đĩa và trong bộ nhớ
Bây giờ, chúng ta hãy giới hạn kích thước bộ nhớ đệm. Điều này quan trọng vì bộ nhớ đệm không giới hạn có thể gây ra các vấn đề về hiệu năng.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: Đặt giới hạn 1 GB cho bộ nhớ đệm trên đĩa. Bạn có thể điều chỉnh kích thước này tùy theo nhu cầu.  
- `Cache.setMaxMemoryForCache(1073741824)`: Tương tự, giới hạn bộ nhớ đệm trong bộ nhớ, đảm bảo ứng dụng của bạn không sử dụng quá nhiều bộ nhớ.

### Bước 4: Quản lý chiến lược phân bổ lại bộ nhớ đệm
Quản lý cách bộ nhớ đệm được phân bổ lại là cần thiết để duy trì hiệu năng. Dưới đây là cách bạn có thể thiết lập.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: Khi đặt thành `false`, Aspose sẽ quản lý việc phân bổ lại bộ nhớ đệm một cách linh hoạt hơn, có thể mang lại hiệu năng tốt hơn.

### Bước 5: Kiểm tra kích thước bộ nhớ đệm đã cấp phát
Bước này liên quan đến việc giám sát số byte hiện đang được cấp phát cho bộ nhớ đệm trong bộ nhớ hoặc trên đĩa. Hãy thực hiện điều này:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: Lưu số byte đã cấp phát trên đĩa.  
- `long l2`: Lưu số byte đã cấp phát trong bộ nhớ.  
Bạn có thể kiểm tra các giá trị này bất kỳ lúc nào để đảm bảo ứng dụng của bạn đang quản lý bộ nhớ và sử dụng đĩa như mong đợi.

### Bước 6: Tạo ảnh PSD
Bây giờ chúng ta đã thiết lập cấu hình bộ nhớ đệm, hãy tạo một ảnh PSD đơn giản.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Đối tượng này cho phép bạn chỉ định các tùy chọn khi tạo ảnh Photoshop.  
- `Color[] color`: Một mảng chứa các màu sẽ được sử dụng trong bảng màu của ảnh.

### Bước 7: Lưu dữ liệu pixel vào ảnh
Bây giờ, hãy điền dữ liệu pixel vào ảnh và lưu lại.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: Đây là một mảng các đối tượng màu. Ở đây, chúng ta đang điền nó bằng các pixel màu trắng.  
- `image.savePixels(image.getBounds(), pixels)`: Phương thức này lưu dữ liệu pixel vào ảnh. Nó cập nhật ảnh với các màu mà chúng ta đã định nghĩa.

### Bước 8: Giám sát bộ nhớ đệm đã cấp phát sau khi tạo ảnh
Sau khi tạo ảnh, việc kiểm tra lại số byte đã cấp phát cho bộ nhớ đệm là một thực hành tốt.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: Ghi lại lượng bộ nhớ đệm hiện tại trên đĩa sau khi tạo ảnh.  
- `long memoryBytes`: Ghi lại lượng bộ nhớ đệm hiện tại trong bộ nhớ.  
Bước này sẽ giúp bạn xác định mức độ tiêu thụ bộ nhớ đệm sau các thao tác của bạn.

### Bước 9: Kiểm tra việc giải phóng đúng cách
Cuối cùng, việc đảm bảo tất cả các đối tượng Aspose.PSD được giải phóng đúng cách là rất quan trọng để tránh rò rỉ bộ nhớ.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` và `l2`: Các biến này sẽ giúp bạn kiểm tra cấp phát cuối cùng. Nếu chúng không bằng zero, điều đó cho thấy một số đối tượng chưa được giải phóng đúng cách.

## Các vấn đề thường gặp và giải pháp
- **Cache folder not created** – Kiểm tra xem ứng dụng có quyền ghi vào đường dẫn bạn đã truyền cho `Cache.setCacheFolder` hay không.  
- **Out‑of‑memory errors** – Đảm bảo rằng `Cache.setCacheType(CacheType.CacheOnDiskOnly)` đã được áp dụng trước khi tải các tệp PSD lớn.  
- **Unexpected cache size** – Sử dụng các phương thức `Cache.getAllocated*BytesCount()` sau mỗi thao tác quan trọng để theo dõi sự tăng trưởng.

## Câu hỏi thường gặp

**Q: Aspose.PSD là gì?**  
A: Aspose.PSD là một thư viện cho các nhà phát triển .NET và Java để tạo, thao tác và chuyển đổi các tệp Photoshop (PSD) một cách lập trình.

**Q: Làm sao để kiểm tra kích thước bộ nhớ đệm đã cấp phát?**  
A: Sử dụng các phương thức như `Cache.getAllocatedDiskBytesCount()` và `Cache.getAllocatedMemoryBytesCount()` để giám sát việc sử dụng bộ nhớ đệm hiện tại.

**Q: Tôi có thể đặt thư mục tùy chỉnh cho bộ nhớ đệm không?**  
A: Có, bạn có thể chỉ định một thư mục khác bằng cách sử dụng `Cache.setCacheFolder("Your Directory Path")`.

**Q: Aspose.PSD có miễn phí không?**  
A: Aspose.PSD là một thư viện trả phí, nhưng bạn có thể bắt đầu với bản dùng thử miễn phí có sẵn trên [website](https://releases.aspose.com/).

**Q: Điều gì xảy ra nếu tôi không giải phóng các đối tượng?**  
A: Không giải phóng các đối tượng có thể dẫn đến rò rỉ bộ nhớ, khiến ứng dụng của bạn tiêu thụ nhiều tài nguyên hơn mức cần thiết.

## Kết luận
Kiểm soát việc phân bổ lại bộ nhớ đệm khi bạn **create PSD image java** các ứng dụng có thể tạo ra sự khác biệt đáng kể về hiệu năng. Bằng cách thực hiện các bước trên, bạn sẽ quản lý bộ nhớ đệm một cách hiệu quả, giảm thiểu việc tiêu thụ bộ nhớ và tạo ra các tệp PSD chất lượng cao với Aspose.PSD for Java. Áp dụng những kỹ thuật này, dự án của bạn sẽ chạy mượt mà hơn và mở rộng tốt hơn.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}