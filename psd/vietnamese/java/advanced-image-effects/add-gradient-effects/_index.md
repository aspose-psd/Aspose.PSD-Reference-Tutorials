---
date: 2026-10-18
description: Tìm hiểu cách tạo hiệu ứng gradient dạng tròn trong hình ảnh Java bằng
  Aspose.PSD. Thực hiện theo hướng dẫn từng bước để tích hợp liền mạch.
keywords:
- create radial gradient java
- apply gradient overlay psd
- add radial gradient image
lastmod: 2026-10-18
linktitle: Thêm hiệu ứng gradient
og_description: Tìm hiểu cách tạo hiệu ứng gradient dạng tròn Java bằng Aspose.PSD.
  Bài hướng dẫn này chỉ ra cách thêm, tùy chỉnh và lưu các lớp phủ gradient chỉ trong
  vài phút.
og_image_alt: Screenshot of Aspose.PSD Java code creating a radial gradient effect
og_title: Tạo gradient dạng tròn Java với Aspose.PSD – hướng dẫn từng bước
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  headline: How to create radial gradient effects in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  name: How to create radial gradient effects in Aspose.PSD for Java
  steps:
  - name: Load the PSD file and access the gradient overlay
    text: '`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable
      loading of effect resources. `Image.load` reads the file into an `Image` object.
      In this step, we load a PSD file and retrieve the first `GradientOverlayEffect`
      from the second layer (index 1). The `loadOptions.setLoadEffec'
  - name: Verify Initial Settings
    text: Before making changes, it’s a good practice to confirm the current blend
      mode, opacity, and visibility. This helps you understand the baseline state
      of the gradient overlay.
  - name: Modify Gradient Settings
    text: Here you can customize the gradient’s color, opacity, and blend mode. The
      example changes the color to green, reduces opacity to 193 (out of 255), and
      switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode`
      values such as `Multiply`, `Screen`, or `Overlay`.
  - name: Save the Edited Image
    text: After applying your modifications, persist the changes by saving the PSD
      to a new file. This step ensures the original file remains untouched.
  - name: Verify Changes
    text: The snippet above demonstrates how to open a PSD, pull the second layer’s
      first effect (assumed to be a gradient overlay), and prepare it for modification.
  - name: Verify the original settings (optional but recommended)
    text: Before you change anything, checking the existing blend mode, opacity, and
      visibility helps you understand the baseline. The `Assert` calls in the code
      confirm that the effect is currently set to **Normal** blend mode, fully opaque,
      and visible.
  - name: Adjust gradient properties to achieve a radial style
    text: 'You can change the gradient’s color, opacity, and blend mode. For a true
      radial effect, set the gradient style: *Pro tip:* Use `Color.getGreen()` or
      any `java.awt.Color` instance to define the start color, and `gradientOverlay.setColor2(Color.getBlue())`
      for the end color.'
  - name: Save the edited PSD
    text: Calling `im.save(exportPath);` writes the modified image to disk. The saved
      file retains the radial gradient overlay and can be opened in Photoshop, previewed
      in browsers, or converted to other formats.
  type: HowTo
- questions:
  - answer: Yes. Retrieve the layer’s `BlendingOptions`, iterate through the `Effects`
      collection, and add a new `GradientOverlayEffect` for each gradient you need.
    question: Can I apply multiple gradient effects to a single image?
  - answer: Aspose.PSD provides shadows, glows, bevels, and more. Each effect appears
      in the `Effects` array and can be configured independently.
    question: What other effects can I combine with gradient overlays?
  - answer: Verify that the PSD was loaded with `setLoadEffectsResource(true)`, check
      layer visibility, and confirm you are modifying the correct effect index.
    question: How can I troubleshoot if the effects are not rendering correctly?
  - answer: Yes, you can get a free trial [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing
      information.
    question: Where can I purchase a license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
title: Cách tạo hiệu ứng gradient dạng tròn trong Aspose.PSD cho Java
url: /vi/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách tạo hiệu ứng gradient dạng tròn trong Aspose.PSD cho Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ học cách **tạo hiệu ứng radial gradient java** bằng thư viện Aspose.PSD. Gradient dạng tròn rất phù hợp để thêm độ sâu, tiêu điểm hoặc ánh sáng nhẹ vào các lớp PSD của bạn mà không cần mở Photoshop. Khi kết thúc tutorial, bạn sẽ có thể tải một tệp PSD, áp dụng lớp phủ gradient, điều chỉnh các thuộc tính của nó và lưu kết quả — tất cả bằng mã Java.

## Câu trả lời nhanh
- **Bạn có thể đạt được gì?** Thêm, chỉnh sửa và pha trộn các lớp phủ gradient dạng tròn trên các lớp PSD.  
- **Thư viện nào cần thiết?** Aspose.PSD for Java (phiên bản mới nhất).  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí đủ cho phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Thời gian thực hiện khoảng bao lâu?** Khoảng 10‑15 phút cho một lớp phủ gradient dạng tròn cơ bản.  
- **Có tương thích với Java 8+ không?** Có, API hỗ trợ Java 8 và các runtime mới hơn.

## Yêu cầu trước

Trước khi chúng ta bắt đầu tutorial, hãy chắc chắn rằng bạn đã chuẩn bị đầy đủ các yêu cầu sau:

1. **Thư viện Aspose.PSD cho Java** – Đảm bảo bạn đã tải xuống và cài đặt thư viện Aspose.PSD cho Java. Bạn có thể tìm thư viện và tài liệu của nó trên [trang tài liệu Aspose.PSD Java](https://reference.aspose.com/psd/java/).  
2. **Môi trường phát triển Java** – Thiết lập môi trường phát triển Java trên máy của bạn (JDK 8 trở lên, IDE bạn chọn).  
3. **Bản phát hành Aspose.PSD mới nhất** – Tải phiên bản mới nhất từ [trang phát hành Aspose](https://releases.aspose.com/).  
4. **Tài nguyên hỗ trợ** – Nếu gặp vấn đề, tham khảo [diễn đàn hỗ trợ Aspose.PSD](https://forum.aspose.com/c/psd/34).  
5. **Mua giấy phép** – Khi bạn sẵn sàng cho sản xuất, mua giấy phép qua [trang mua hàng](https://purchase.aspose.com/buy).

Bây giờ bạn đã có mọi thứ sẵn sàng, hãy tiếp tục với hướng dẫn từng bước.

## Hiệu ứng lớp phủ gradient là gì?

Hiệu ứng lớp phủ gradient vẽ một chuyển đổi mượt mà giữa hai hoặc nhiều màu trên một khu vực đã chọn của một lớp. Trong Photoshop, hiệu ứng này có thể được pha trộn, tô màu và định vị để tạo ra các thiết kế trực quan tinh tế. Lớp `GradientOverlayEffect` là đại diện của Aspose.PSD cho kiểu lớp này, cung cấp các thuộc tính như điểm dừng màu, độ mờ, chế độ pha trộn và kiểu gradient.

## Cách tạo hiệu ứng gradient dạng tròn

Tải PSD, xác định lớp mục tiêu, điều chỉnh các thuộc tính của `GradientOverlayEffect`, và cuối cùng lưu tệp. Quy trình hoàn chỉnh chỉ cần bốn dòng mã Java ngắn gọn sau khi ảnh đã được tải.

### Bước 1: Tải tệp PSD và truy cập lớp phủ gradient

`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable loading of effect resources. `Image.load` reads the file into an `Image` object.

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

Trong bước này, chúng ta tải một tệp PSD và lấy `GradientOverlayEffect` đầu tiên từ lớp thứ hai (chỉ mục 1). Lệnh `loadOptions.setLoadEffectsResource(true)` đảm bảo các tài nguyên hiệu ứng có sẵn để chỉnh sửa.

### Bước 2: Xác minh cài đặt ban đầu

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

Trước khi thực hiện thay đổi, nên xác nhận chế độ pha trộn, độ mờ và trạng thái hiển thị hiện tại. Điều này giúp bạn hiểu trạng thái cơ bản của lớp phủ gradient.

### Bước 3: Sửa đổi cài đặt gradient

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

Ở đây bạn có thể tùy chỉnh màu, độ mờ và chế độ pha trộn của gradient. Ví dụ thay đổi màu thành xanh lá, giảm độ mờ xuống 193 (trong 255), và chuyển chế độ pha trộn sang **Lighten**. Bạn có thể thử các giá trị `BlendMode` khác như `Multiply`, `Screen`, hoặc `Overlay`.

### Bước 4: Lưu hình ảnh đã chỉnh sửa

```java
// Save the edited image
im.save(exportPath);
```

Sau khi áp dụng các chỉnh sửa, lưu lại các thay đổi bằng cách lưu PSD vào một tệp mới. Bước này đảm bảo tệp gốc không bị thay đổi.

### Bước 5: Xác minh các thay đổi

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

Đoạn mã trên minh họa cách mở một PSD, lấy hiệu ứng đầu tiên của lớp thứ hai (giả định là một lớp phủ gradient), và chuẩn bị cho việc chỉnh sửa.

### Bước 2: Xác minh cài đặt gốc (tùy chọn nhưng được khuyến nghị)

Trước khi thay đổi bất kỳ thứ gì, việc kiểm tra chế độ pha trộn, độ mờ và trạng thái hiển thị hiện có giúp bạn hiểu nền tảng. Các lệnh `Assert` trong mã xác nhận rằng hiệu ứng hiện đang ở chế độ pha trộn **Normal**, hoàn toàn không trong suốt và hiển thị.

### Bước 3: Điều chỉnh thuộc tính gradient để đạt kiểu dạng tròn

Bạn có thể thay đổi màu, độ mờ và chế độ pha trộn của gradient. Để có hiệu ứng dạng tròn thực sự, hãy đặt kiểu gradient:

```java
gradientOverlay.setGradientStyle(GradientStyle.Radial);
gradientOverlay.setAngle(0f); // angle is ignored for radial, but required by API
gradientOverlay.setScale(100f); // 100 % fills the layer
```

*Mẹo:* Sử dụng `Color.getGreen()` hoặc bất kỳ đối tượng `java.awt.Color` nào để định nghĩa màu bắt đầu, và `gradientOverlay.setColor2(Color.getBlue())` cho màu kết thúc.

### Bước 4: Lưu PSD đã chỉnh sửa

Gọi `im.save(exportPath);` ghi ảnh đã chỉnh sửa vào đĩa. Tệp đã lưu giữ lại lớp phủ gradient dạng tròn và có thể mở trong Photoshop, xem trước trong trình duyệt, hoặc chuyển đổi sang các định dạng khác.

## Tại sao tạo lớp phủ gradient dạng tròn?

Gradient dạng tròn thêm độ sâu và tiêu điểm cho thiết kế, khiến các yếu tố trông ba chiều hoặc nổi bật. Chúng lý tưởng cho:

- **Đổ nền** thu hút ánh nhìn về phía chủ thể trung tâm.  
- **Nổi bật nút hoặc biểu tượng** khi cần ánh sáng nhẹ.  
- **Hiệu ứng ảnh sáng tạo** như viền tối (vignette) hoặc bùng nổ ánh sáng.  

Aspose.PSD xử lý **hơn 50 định dạng đầu vào và đầu ra** và có thể làm việc với các tệp PSD hàng trăm trang mà không cần tải toàn bộ tài liệu vào bộ nhớ, cho phép bạn tự động tạo gradient trên các thư viện tài sản lớn.

## Vấn đề thường gặp & mẹo

- **Hiệu ứng không hiển thị:** Đảm bảo `gradientOverlay.isVisible()` trả về `true`. Một số tệp PSD ẩn hiệu ứng theo mặc định.  
- **Chỉ mục lớp không đúng:** Các lớp được đánh số bắt đầu từ 0; kiểm tra lại bạn đang nhắm đúng lớp (`im.getLayers()[1]` là lớp thứ hai).  
- **Ép kiểu độ mờ:** Phương thức `setOpacity` yêu cầu một `byte`. Truyền một `int` sẽ gây lỗi biên dịch; hãy ép kiểu rõ ràng như trong ví dụ.  
- **Tải tài nguyên:** Nếu gặp `null` khi truy cập hiệu ứng, xác nhận rằng `loadOptions.setLoadEffectsResource(true)` đã được đặt trước khi tải ảnh.

## Câu hỏi thường gặp

**Hỏi:** Tôi có thể áp dụng nhiều hiệu ứng gradient cho một hình ảnh duy nhất không?  
**Đáp:** Có. Lấy `BlendingOptions` của lớp, duyệt qua bộ sưu tập `Effects`, và thêm một `GradientOverlayEffect` mới cho mỗi gradient bạn cần.

**Hỏi:** Những hiệu ứng khác nào tôi có thể kết hợp với lớp phủ gradient?  
**Đáp:** Aspose.PSD cung cấp bóng, hào quang, viền nổi và hơn thế nữa. Mỗi hiệu ứng xuất hiện trong mảng `Effects` và có thể cấu hình độc lập.

**Hỏi:** Làm thế nào để khắc phục nếu các hiệu ứng không hiển thị đúng?  
**Đáp:** Xác nhận PSD đã được tải bằng `setLoadEffectsResource(true)`, kiểm tra trạng thái hiển thị của lớp, và chắc chắn bạn đang chỉnh sửa chỉ mục hiệu ứng đúng.

**Hỏi:** Có phiên bản dùng thử cho Aspose.PSD cho Java không?  
**Đáp:** Có, bạn có thể nhận bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

**Hỏi:** Tôi có thể mua giấy phép cho Aspose.PSD cho Java ở đâu?  
**Đáp:** Tham khảo [trang mua hàng](https://purchase.aspose.com/buy) để biết thông tin cấp phép.

## Câu hỏi thường gặp bổ sung

**Hỏi:** Tôi có thể thay đổi hướng gradient bằng lập trình không?  
**Đáp:** Có. Sử dụng phương thức `GradientOverlayEffect.setAngle(float angle)` để đặt góc gradient theo độ. Đối với gradient dạng tròn, góc sẽ bị bỏ qua, nhưng vẫn cần gọi phương thức này.

**Hỏi:** Aspose.PSD có hỗ trợ gradient dạng tròn không?  
**Đáp:** Chắc chắn có. Đặt kiểu gradient thành `GradientStyle.Radial` thông qua các thuộc tính của `GradientOverlayEffect`.

**Hỏi:** Các lớp phủ gradient có được giữ lại khi chuyển PSD sang định dạng khác (ví dụ PNG) không?  
**Đáp:** Khi raster hoá PSD (ví dụ lưu dưới dạng PNG), kết quả hình ảnh của lớp phủ gradient được giữ lại, nhưng hiệu ứng sẽ trở thành dữ liệu pixel.

**Hỏi:** Làm sao để xóa lớp phủ gradient khỏi một lớp?  
**Đáp:** Lấy `BlendingOptions` của lớp, tìm `GradientOverlayEffect` trong bộ sưu tập `Effects`, và xóa nó bằng `remove(effect)`.

**Hỏi:** Có thể tạo hoạt ảnh cho các thay đổi gradient không?  
**Đáp:** Mặc dù Aspose.PSD không trực tiếp xử lý hoạt ảnh, bạn có thể tạo một chuỗi các tệp PSD với các tham số gradient khác nhau và sau đó ghép chúng thành video hoặc GIF bằng thư viện khác.

## Kết luận

Chúc mừng! Bạn đã học cách **tạo hiệu ứng radial gradient java** cho hình ảnh của mình bằng Aspose.PSD cho Java. Bằng cách thực hiện các bước trên, bạn có thể thêm, chỉnh sửa và lưu lớp phủ gradient một cách lập trình, mang lại cho bạn toàn quyền kiểm soát sáng tạo đối với các tài sản PSD. Hãy thử nghiệm với các màu sắc, chế độ pha trộn và giá trị độ mờ khác nhau để đạt được hiệu quả hình ảnh mong muốn.

---

**Last Updated:** 2026-10-18  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  








```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Hướng dẫn liên quan

- [Tạo Gradient Fill PSD với Java bằng Aspose.PSD – Thêm lớp Gradient Fill](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Pattern Overlay PSD: Thêm hiệu ứng bằng Aspose.PSD cho Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Áp dụng Color Overlay và Đặt Độ mờ trong Java với Aspose.PSD](/psd/java/image-editing/color-overlay-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}