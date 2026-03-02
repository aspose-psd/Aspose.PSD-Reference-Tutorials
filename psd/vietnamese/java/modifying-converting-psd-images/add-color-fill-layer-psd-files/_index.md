---
date: 2026-03-02
description: Học cách thêm màu nền bằng cách tạo lớp màu trong các tệp PSD sử dụng
  Java và Aspose.PSD. Thực hiện theo hướng dẫn từng bước của chúng tôi để nhanh chóng
  thiết lập màu cho lớp nền.
linktitle: Add Color Fill Layer to PSD Files using Java
second_title: Aspose.PSD Java API
title: 'Cách Thêm Đổ Màu: Thêm Lớp Đổ Màu vào Tệp PSD bằng Java'
url: /vi/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thêm Lớp Đổ Màu vào Tệp PSD bằng Java

## Giới thiệu
Bạn đã bao giờ cần thao tác các tệp Photoshop một cách lập trình, có thể để thêm một chút màu sắc vào thiết kế? Nếu bạn đang tự hỏi **cách thêm fill** vào một PSD, bạn đang ở đúng nơi. Trong hướng dẫn này chúng ta sẽ đi qua cách thêm một lớp đổ màu vào các tệp PSD (Photoshop Document) bằng Java và thư viện Aspose.PSD. Hãy nghĩ PSD của bạn như một canvas kỹ thuật số—cuối cùng bạn sẽ biết cách tạo một lớp đổ màu, đặt màu cho lớp đổ, và lưu tệp đã cập nhật chỉ trong vài dòng code.

## Câu trả lời nhanh
- **Thư viện cần thiết?** Aspose.PSD for Java  
- **Trường hợp sử dụng chính?** Thêm hoặc thay đổi màu fill PSD một cách lập trình  
- **Thời gian triển khai?** Khoảng 10‑15 phút cho kịch bản cơ bản  
- **Cần giấy phép?** Bản dùng thử miễn phí đủ cho đánh giá; giấy phép thương mại cần cho môi trường sản xuất  
- **Phiên bản Java được hỗ trợ?** Java 8 trở lên  

## Lớp Đổ Màu là gì?
Lớp đổ màu là một lớp phủ màu đồng nhất nằm trên các lớp khác trong tài liệu Photoshop. Nó thường được dùng để thêm màu nền, tạo mặt nạ, hoặc nhanh chóng thay đổi giao diện thiết kế mà không cần chỉnh sửa từng pixel.

## Tại sao thêm lớp đổ màu bằng mã?
- **Tự động hoá:** Tạo ra các tài sản thương hiệu nhất quán trên nhiều tệp.  
- **Xử lý hàng loạt:** Cập nhật hàng chục PSD trong vài giây thay vì làm thủ công.  
- **Thiết kế động:** Thay đổi màu sắc ngay lập tức dựa trên đầu vào của người dùng hoặc nguồn dữ liệu.

## Yêu cầu trước
Trước khi chúng ta đi vào code, hãy chắc chắn rằng bạn đã chuẩn bị đầy đủ:

1. **Bộ công cụ phát triển Java (JDK)** – JDK 8 hoặc mới hơn đã được cài đặt.  
2. **Thư viện Aspose.PSD** – Tải JAR mới nhất từ [trang Aspose Releases](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, NetBeans, hoặc bất kỳ trình chỉnh sửa nào bạn thích.  
4. **Kiến thức cơ bản về Java** – Quen thuộc với các đối tượng, vòng lặp và xử lý ngoại lệ.

## Nhập khẩu các gói
Bây giờ chúng ta đã có nền tảng, hãy nhập các lớp cần thiết. Những import này cho phép chúng ta làm việc với PSD và thao tác lớp fill.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IColorFillSettings;
```

## Cách Thêm Fill – Hướng Dẫn Từng Bước

### Bước 1: Thiết lập môi trường
Xác định vị trí PSD nguồn và nơi tệp đã chỉnh sửa sẽ được lưu, sau đó tải tài liệu.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath     = dataDir + "ColorFillLayer_output.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` chỉ tới thư mục chứa PSD của bạn.  
- `sourceFileName` là tệp gốc bạn sẽ sửa đổi.  
- `exportPath` là nơi tệp mới với **thêm lớp đổ màu** sẽ được ghi.  

### Bước 2: Duyệt qua các lớp
Chúng ta cần tìm bất kỳ lớp fill nào đã tồn tại để có thể sửa chúng hoặc tạo lớp mới.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof FillLayer) {
        FillLayer fillLayer = (FillLayer) im.getLayers()[i];
```

- Vòng lặp `for` lặp qua mọi lớp trong PSD.  
- Kiểm tra `instanceof FillLayer` đảm bảo chúng ta chỉ làm việc với các lớp fill.

### Bước 3: Xác minh loại Fill
Đảm bảo lớp chúng ta tìm được là **lớp đổ màu** trước khi cố gắng thay đổi màu của nó.

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Color) {
    throw new Exception("Wrong Fill Layer");
}
```

Nếu loại fill không phải là `FillType.Color`, chúng ta sẽ dừng lại để tránh vô tình thay đổi gradient hoặc pattern fill.

### Bước 4: Đặt màu cho Fill
Đây là nơi chúng ta **đặt màu cho lớp fill**. Ví dụ thay đổi lớp thành màu đỏ, nhưng bạn có thể thay `Color.getRed()` bằng bất kỳ `Color` nào khác bạn cần (ví dụ, `Color.getBlue()`, `new Color(255, 165, 0)` cho màu cam).

```java
IColorFillSettings settings = (IColorFillSettings) fillLayer.getFillSettings();
settings.setColor(Color.getRed());
fillLayer.update();
```

- `settings.setColor(...)` thay đổi màu fill thực tế.  
- `fillLayer.update()` làm mới lớp để màu mới được áp dụng.  

### Bước 5: Lưu các thay đổi
Cuối cùng, ghi lại PSD đã chỉnh sửa trở lại đĩa.

```java
im.save(exportPath);
break;
```

- `break` dừng vòng lặp sau khi lớp fill phù hợp đầu tiên được cập nhật, thường là những gì bạn muốn khi chỉ cần **thay đổi màu fill PSD** một lần.

## Vấn đề thường gặp & Mẹo
- **Không tìm thấy FillLayer:** Nếu PSD của bạn không chứa lớp fill, bạn cần tạo một bằng cách dùng `new FillLayer(im)` và thêm vào `im.getLayers()`.  
- **Màu không cập nhật:** Đảm bảo bạn gọi `fillLayer.update()` sau khi đặt màu.  
- **Tệp không được lưu:** Kiểm tra `exportPath` chỉ tới thư mục có thể ghi và bạn có quyền ghi tệp ở đó.  

## Câu hỏi thường gặp

**Q: Aspose.PSD là gì?**  
A: Aspose.PSD là một thư viện Java mạnh mẽ cho phép bạn tạo, chỉnh sửa và chuyển đổi các tệp Photoshop PSD mà không cần Adobe Photoshop.

**Q: Có thể sử dụng Aspose.PSD miễn phí không?**  
A: Có, bản dùng thử miễn phí có sẵn trên [trang Aspose Releases](https://releases.aspose.com/).  

**Q: Tôi có thể làm việc với các định dạng tệp nào ngoài PSD?**  
A: Aspose.PSD hỗ trợ PSD, PSB, BMP, JPEG, PNG, GIF, TIFF, và hơn nữa.

**Q: Làm sao tôi có thể nhận hỗ trợ nếu gặp vấn đề?**  
A: Bạn có thể đặt câu hỏi trên [Diễn đàn Hỗ trợ Aspose](https://forum.aspose.com/c/psd/34).  

**Q: Tôi có thể mua giấy phép đầy đủ ở đâu?**  
A: Giấy phép được bán qua [trang Mua Aspose](https://purchase.aspose.com/buy).

## Kết luận
Bạn giờ đã biết **cách thêm fill** vào tài liệu Photoshop một cách lập trình bằng Java. Bằng cách tạo hoặc tìm một lớp đổ màu, đặt màu cho nó, và lưu kết quả, bạn có thể tự động hoá các nhiệm vụ thiết kế lặp lại, tạo ra các tài sản động, hoặc tích hợp việc thao tác PSD vào các ứng dụng Java lớn hơn. Hãy thử—thử nghiệm với các màu khác nhau, thêm nhiều lớp đổ, hoặc kết hợp kỹ thuật này với các tính năng khác của Aspose.PSD để có các pipeline xử lý ảnh mạnh mẽ.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2026-03-02  
**Kiểm tra với:** Aspose.PSD for Java 24.11 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose