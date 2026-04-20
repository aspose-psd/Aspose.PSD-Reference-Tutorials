---
date: 2026-03-15
description: تعلم كيفية إنشاء ملفات PSD، وتوليد لوحة ألوان PSD، وتعيين وضع لون PSD
  باستخدام Aspose.PSD للغة Java في هذا الدليل خطوة بخطوة.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: كيفية إنشاء ملفات PSD باستخدام Aspose.PSD للـ Java
url: /ar/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء ملفات PSD باستخدام Aspose.PSD للـ Java

## مقدمة
إذا تساءلت يومًا **كيفية إنشاء PSD** برمجيًا، فأنت في المكان الصحيح. توفر لك Aspose.PSD للـ Java تحكمًا كاملاً في مستندات Photoshop، مما يتيح لك إنشاء، تعديل، وحفظ ملفات PSD دون الحاجة إلى فتح Photoshop. في هذا الدرس سنستعرض إنشاء ملف **PSD مفهرس**، ضبط وضع لون PSD، وإنشاء لوحة ألوان مخصصة—كل ذلك باستخدام كود Java واضح خطوة بخطوة. سواء كنت تبني خط أنابيب رسومي، أوتوماتيكيًا إنشاء الأصول، أو مجرد تجربة، فإن المفاهيم هنا ستساعدك على تحويل أفكارك البصرية إلى حقيقة.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.PSD for Java
- **هل يمكنني إنشاء PSD مفهرس؟** نعم، عن طريق ضبط وضع اللون إلى `Indexed`
- **هل أحتاج إلى تثبيت Photoshop؟** لا، Aspose.PSD يعمل بشكل مستقل
- **ما نسخة Java المطلوبة؟** JDK 8 أو أحدث
- **ما هو الحد الأقصى لحجم اللوحة؟** أي حجم؛ هذا المثال يستخدم 500 × 500 px

## ما هو ملف PSD المفهرس؟
يخزن ملف PSD المفهرس الألوان في لوحة ألوان بدلاً من قيم اللون الكاملة لكل بكسل. هذا يقلل من حجم الملف ويعد مثاليًا للرسومات ذات الألوان المحدودة، مثل الأيقونات أو عناصر واجهة المستخدم. من خلال إنشاء لوحة ألوان مخصصة يمكنك التحكم بدقة في الألوان التي تظهر في الصورة النهائية.

## لماذا إنشاء لوحة ألوان PSD؟
- الحفاظ على حجم الملفات صغيرًا للاستخدام على الويب أو الهواتف المحمولة  
- ضمان تناسق العلامة التجارية عن طريق حصر الألوان في لوحة ألوان الشركة  
- تسريع عملية العرض في التطبيقات التي تدعم الصور المفهرسة  

## المتطلبات المسبقة
قبل أن نغوص في الكود، تأكد من توفر ما يلي:

1. **معرفة أساسية بـ Java** – يجب أن تكون مرتاحًا مع الفئات، الطرق، وإنشاء الكائنات.  
2. **Java Development Kit (JDK) 8+** – مثبت ومُعد في بيئة التطوير المتكاملة الخاصة بك.  
3. **IDE (IntelliJ IDEA, Eclipse, إلخ)** – اختياري لكنه موصى به بشدة لتسهيل عملية التصحيح.  
4. **مكتبة Aspose.PSD للـ Java** – قم بتحميلها **[here](https://releases.aspose.com/psd/java/)** وأضف ملف JAR إلى مسار الفئة في مشروعك.  
5. **مفاهيم أساسية في التصميم الجرافيكي** – فهم أوضاع الألوان، اللوحات، والأشكال الأساسية سيساعدك على المتابعة.

## استيراد الحزم
قبل المتابعة مع الكود، دعنا نتأكد من استيراد جميع الحزم الضرورية إلى تطبيق Java الخاص بك. إليك ما ستحتاجه:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

ستتيح لك هذه الاستيرادات العمل مع خيارات PSD، الألوان، ومعالجة الرسومات عبر Aspose.PSD.

الآن، دعنا نفصل الكود خطوة بخطوة إلى **كيفية إنشاء PSD** بضعيفة لون مفهرسة.

## الخطوة 1: إعداد دليل المستندات الخاص بك
أولاً، حدد المكان الذي سيتم حفظ ملف PSD المُولد فيه.

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بمسار مطلق أو نسبي، مثال: `"/Users/YourName/Documents/"`.

## الخطوة 2: إنشاء نسخة من PsdOptions
`PsdOptions` يحتوي على جميع الإعدادات للملف الذي ستقوم بإنشائه.

```java
PsdOptions createOptions = new PsdOptions();
```

## الخطوة 3: تعيين الخصائص الأساسية لـ PsdOptions
هنا نحدد موقع الإخراج، **set psd color mode** إلى `Indexed`، وإصدار PSD.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – المسار الكامل للملف الجديد.  
- **Color Mode** – `Indexed` يخبر Aspose.PSD باستخدام صورة قائمة على لوحة ألوان.  
- **Version** – إصدار تنسيق PSD (5 يعمل مع معظم إصدارات Photoshop الحديثة).

## الخطوة 4: إنشاء لوحة ألوان (إنشاء لوحة ألوان PSD)
حدد الألوان التي ستكون متاحة في الصورة المفهرسة.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- مصفوفة `palette` يمكنها احتواء حتى 256 كائن `Color`.  
- `CompressionMethod.RLE` يوفر ضغطًا فعالًا غير فقدان للصور المفهرسة.

## الخطوة 5: إنشاء لوحة قماش صورة PSD
الآن نقوم بإنشاء PSD فارغ بالأبعاد التي نريدها.

```java
Image psd = Image.create(createOptions, 500, 500);
```

هذا ينشئ لوحة قماش بحجم 500 × 500 بكسل تستخدم لوحة الألوان المحددة سابقًا.

## الخطوة 6: رسم الرسومات على PSD
أضف محتوى بصري—هنا نرسم إهليلجًا أحمر بسيطًا على خلفية بيضاء.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` يملأ الخلفية باللون الأبيض.  
- `drawEllipse` يرسم إهليلجًا أحمر بحدٍّ عرض 6 بكسل.

## الخطوة 7: حفظ ملف PSD
أخيرًا، احفظ الصورة على القرص.

```java
psd.save();
```

سيظهر الملف `Newsample_out.psd` في الدليل الذي حددته مسبقًا.

## المشكلات الشائعة والنصائح
- **حجم اللوحة** – إذا كنت بحاجة إلى أكثر من 4 ألوان، ما عليك سوى إضافتها إلى مصفوفة `palette` (حتى 256).  
- **أذونات الملف** – تأكد من أن عملية Java لديها صلاحية كتابة إلى `dataDir`.  
- **وضع اللون غير الصحيح** – نسيان `createOptions.setColorMode(ColorModes.Indexed)` سيؤدي إلى إنشاء PSD بصيغة RGB بدلاً من مفهرسة.  

## الأسئلة المتكررة

**س: ما هو Aspose.PSD للـ Java؟**  
ج: Aspose.PSD للـ Java هي مكتبة تتيح التلاعب بملفات PSD (Photoshop) برمجيًا باستخدام Java.

**س: هل يمكنني استخدام Aspose.PSD مجانًا؟**  
ج: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية من Aspose.PSD **[here](https://releases.aspose.com/)**.

**س: هل أحتاج إلى تثبيت Photoshop للعمل مع Aspose.PSD؟**  
ج: لا، يمكنك إنشاء وتعديل ملفات PSD دون الحاجة إلى Photoshop، حيث يتعامل Aspose.PSD مع جميع العمليات بشكل مستقل.

**س: كيف أحصل على ترخيص مؤقت لـ Aspose.PSD؟**  
ج: يمكنك طلب ترخيص مؤقت **[here](https://purchase.aspose.com/temporary-license/)**.

**س: أين يمكنني الحصول على دعم لـ Aspose.PSD؟**  
ج: يمكنك الحصول على الدعم من منتدى Aspose **[here](https://forum.aspose.com/c/psd/34)**.

## الخلاصة
لقد تعلمت الآن **كيفية إنشاء PSD** بضعيفة لون مفهرسة، أنشأت لوحة ألوان مخصصة، وأضفت رسومات بسيطة—كل ذلك باستخدام Aspose.PSD للـ Java. باستخدام هذه الأساسيات يمكنك التوسع إلى رسومات أكثر تعقيدًا، إدارة الطبقات، ومعالجة دفعات. للمزيد من الاستكشاف، اطلع على مرجع API الرسمي **[here](https://reference.aspose.com/psd/java/)** واستمر في تجربة لوحات ألوان مختلفة وبدائل الرسم.

---

**آخر تحديث:** 2026-03-15  
**تم الاختبار مع:** Aspose.PSD for Java 24.12 (latest)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}