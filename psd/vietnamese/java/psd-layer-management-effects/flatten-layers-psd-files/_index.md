---
date: 2026-04-03
description: Tìm hiểu cách giảm kích thước tệp PSD bằng cách làm phẳng các lớp với
  Aspose.PSD cho Java. Hướng dẫn từng bước này chỉ ra cách làm phẳng tệp PSD một cách
  nhanh chóng.
keywords:
- reduce psd file size
- how to flatten psd
- flatten visible layers psd
linktitle: Giảm kích thước tệp PSD bằng cách làm phẳng các lớp – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: Giảm kích thước tệp PSD bằng cách hợp nhất các lớp – Aspose.PSD Java
url: /vi/java/psd-layer-management-effects/flatten-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Giảm kích thước tệp PSD bằng cách làm phẳng các lớp – Aspose.PSD Java

## Giới thiệu

Nếu bạn từng mở một tài liệu Photoshop và tự hỏi làm thế nào để **reduce PSD file size**, việc làm phẳng các lớp là một trong những mẹo hiệu quả nhất. Với Aspose.PSD cho Java, bạn có thể lập trình làm phẳng toàn bộ PSD hoặc chỉ hợp nhất các lớp bạn chọn, cho phép bạn kiểm soát chi tiết trọng lượng tệp mà không làm giảm chất lượng hình ảnh. Trong hướng dẫn này, chúng tôi sẽ trình bày cả hai cách—làm phẳng toàn bộ hình ảnh và hợp nhất các lớp cụ thể—để bạn có thể nhanh chóng thu nhỏ các tệp PSD và duy trì quy trình làm việc mượt mà.

## Câu trả lời nhanh
- **Flattening làm gì?** Nó hợp nhất các lớp hiển thị thành một lớp nền duy nhất, loại bỏ thông tin lớp và thường giảm kích thước tệp.  
- **Có thể chỉ làm phẳng các lớp đã chọn không?** Có, bạn có thể hợp nhất các lớp cụ thể trong khi để các lớp khác không bị ảnh hưởng.  
- **Có cần giấy phép không?** Bản dùng thử miễn phí hoạt động cho phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Phiên bản Java nào được yêu cầu?** JDK 8 hoặc cao hơn.  
- **Flattening có ảnh hưởng đến chất lượng hình ảnh không?** Không, ngoại hình vẫn giữ nguyên; chỉ cấu trúc lớp thay đổi.

## “reduce PSD file size” là gì?

Giảm kích thước tệp PSD có nghĩa là loại bỏ dữ liệu không cần thiết—như các lớp thừa, kênh ẩn, hoặc siêu dữ liệu quá mức—để tệp nhẹ hơn và tải nhanh hơn, chia sẻ hoặc xử lý. Làm phẳng các lớp là kỹ thuật phổ biến vì nó loại bỏ các đối tượng lớp riêng biệt trong khi vẫn giữ lại hình ảnh tổng hợp cuối cùng.

## Tại sao nên làm phẳng các lớp với Aspose.PSD cho Java?

- **Tự động hóa:** Không cần mở Photoshop thủ công; tích hợp trực tiếp vào các ứng dụng Java của bạn.  
- **Độ chính xác:** Chọn làm phẳng toàn bộ tài liệu hoặc chỉ các lớp hiển thị (`flattenImage`) hoặc hợp nhất các lớp đã chọn (`mergeLayers`).  
- **Hiệu suất:** Các tệp nhỏ hơn tải nhanh hơn và tiêu thụ ít bộ nhớ hơn trong các quy trình tiếp theo.  
- **Đa nền tảng:** Hoạt động trên bất kỳ hệ điều hành nào hỗ trợ Java.

## Yêu cầu trước

1. **Java Development Kit (JDK):** Đã cài đặt JDK 8 hoặc mới hơn.  
2. **Aspose.PSD for Java:** Tải thư viện từ [here](https://releases.aspose.com/psd/java/).  
3. **IDE:** IntelliJ IDEA, Eclipse, hoặc bất kỳ IDE nào hỗ trợ Java.  
4. **Kiến thức Java cơ bản:** Hữu ích nhưng không bắt buộc để thực hiện các bước.  
5. **Sample PSD:** Một tệp có nhiều lớp (chúng tôi sẽ sử dụng `ThreeRegularLayersSemiTransparent.psd`).  

Bây giờ chúng ta đã sẵn sàng, hãy đi vào phần mã.

## Nhập gói

Để bắt đầu, nhập các lớp Aspose.PSD cần thiết:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

Các import này cho phép chúng ta tải tệp PSD, làm việc với các lớp của chúng và lưu kết quả.

## Bước 1: Làm phẳng toàn bộ ảnh PSD

Làm phẳng toàn bộ ảnh là cách nhanh nhất để **reduce PSD file size** vì nó loại bỏ tất cả dữ liệu lớp riêng lẻ.

### 1.1 Tải tệp PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 1.2 Làm phẳng ảnh

```java
im.flattenImage();
```

### 1.3 Lưu ảnh đã làm phẳng

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

Tệp mới của bạn hiện chứa một lớp nền duy nhất, thường dẫn đến kích thước PSD nhỏ hơn.

## Bước 2: Hợp nhất các lớp cụ thể (Cách làm phẳng PSD một cách chọn lọc)

Đôi khi bạn chỉ muốn **flatten visible layers** hoặc kết hợp một tập hợp con các lớp trong khi giữ các lớp khác có thể chỉnh sửa.

### 2.1 Tải lại tệp PSD

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 2.2 Xác định và chọn các lớp

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

### 2.3 Hợp nhất các lớp

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

### 2.4 Thay thế các lớp hiện có bằng lớp đã hợp nhất

```java
img.setLayers(new Layer[]{layer2});
```

### 2.5 Lưu tệp PSD đã cập nhật

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

Bây giờ PSD chỉ chứa lớp đã hợp nhất, đạt được kích thước tệp giảm trong khi vẫn giữ lại các lớp bạn muốn giữ.

## Các vấn đề thường gặp & Mẹo

- **Sao lưu trước khi làm phẳng:** Khi các lớp đã được làm phẳng, thao tác không thể hoàn tác. Giữ một bản sao của PSD gốc.  
- **Tầm quan trọng của độ hiển thị:** `flattenImage()` chỉ hợp nhất các lớp *hiển thị*. Ẩn bất kỳ lớp nào bạn không muốn bao gồm.  
- **Sử dụng bộ nhớ:** PSD lớn có thể tiêu tốn RAM đáng kể; hãy cân nhắc xử lý chúng trên máy có đủ bộ nhớ.  
- **Chế độ hòa trộn:** Việc hợp nhất tôn trọng chế độ hòa trộn của mỗi lớp, vì vậy kết quả hình ảnh khớp với những gì bạn thấy trong Photoshop.

## Câu hỏi thường gặp

**Q: Có thể hoàn tác việc làm phẳng các lớp trong Aspose.PSD không?**  
A: Không, việc làm phẳng là không thể đảo ngược. Luôn giữ bản sao lưu của tệp gốc.

**Q: Có thể chỉ làm phẳng các lớp hiển thị không?**  
A: Có. `flattenImage()` tôn trọng độ hiển thị của lớp, vì vậy hãy ẩn bất kỳ lớp nào bạn không muốn làm phẳng trước khi gọi phương thức.

**Q: Việc làm phẳng các lớp có giảm kích thước tệp không?**  
A: Nói chung, có. Loại bỏ dữ liệu lớp và siêu dữ liệu thường dẫn đến PSD nhỏ hơn, mặc dù mức giảm cụ thể phụ thuộc vào nội dung.

**Q: Có thể hợp nhất các lớp có chế độ hòa trộn khác nhau không?**  
A: Chắc chắn. Aspose.PSD hợp nhất các lớp trong khi giữ nguyên ngoại hình được tạo ra bởi chế độ hòa trộn của chúng.

**Q: Điều gì sẽ xảy ra nếu tôi cố gắng hợp nhất các lớp không liền kề?**  
A: Aspose.PSD cho phép hợp nhất bất kỳ lớp nào bất kể vị trí trong ngăn xếp; kết quả phản ánh sự xuất hiện kết hợp.

---

**Cập nhật lần cuối:** 2026-04-03  
**Kiểm tra với:** Aspose.PSD 24.11 for Java  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}