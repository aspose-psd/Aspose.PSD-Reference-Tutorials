---
date: 2026-04-03
description: تعلم كيفية تمييز ألوان الأوراق في ملفات PSD باستخدام Aspose.PSD للغة
  Java. اتبع دليلنا خطوة بخطوة لتعزيز مهاراتك في معالجة الصور باستخدام Java.
keywords:
- highlight sheet color psd
- change psd layer color
- Aspose.PSD Java
linktitle: تمييز لون الورقة في ملفات PSD باستخدام Aspise.PSD Java
second_title: Aspose.PSD Java API
title: تمييز لون الورقة في ملفات PSD باستخدام Aspise.PSD Java
url: /ar/java/psd-layer-management-effects/highlight-sheet-color-psd-files/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تسليط الضوء على لون الورقة في ملفات PSD باستخدام Aspose.PSD Java

## المقدمة

إذا كنت بحاجة إلى **highlight sheet color psd** ملفات برمجياً، فقد وجدت المكان المناسب. في هذا الدرس سنستعرض مثالاً كاملاً عملياً يوضح لك كيفية تغيير لون الورقة للطبقات الفردية باستخدام Aspose.PSD for Java. سواءً كنت تبني أداة معالجة دفعية، أو محرراً مخصصاً، أو مجرد أتمتة مهام التصميم المتكررة، فإن إتقان هذه التقنية سيمنحك تحكمًا دقيقًا في أصول PSD الخاصة بك.

## إجابات سريعة
- **ما معنى “highlight sheet color”؟** إنها إشارة بصرية تُعيّن للطبقة وتظهر كشريط ملون في لوحة الطبقات في Photoshop.  
- **أي مكتبة تتعامل مع هذا في Java؟** توفر Aspose.PSD for Java الـ `SheetColorHighlightEnum` وواجهات برمجة التطبيقات ذات الصلة.  
- **هل أحتاج إلى ترخيص لتجربتها؟** يتوفر تجربة مجانية؛ يلزم وجود ترخيص للاستخدام في الإنتاج.  
- **هل يمكنني تغيير طبقات متعددة في آن واحد؟** نعم—قم بالتكرار عبر مجموعة `Layer[]` واضبط تسليط الضوء لكل طبقة.  
- **ما نسخة Java المطلوبة؟** JDK 8 أو أعلى.

## ما هو “highlight sheet color psd”؟

تسليط الضوء على لون الورقة هو سمة بيانات وصفية مخزنة داخل ملف PSD تخبر Photoshop (والأدوات المتوافقة) برسم شريط ملون بجانب اسم الطبقة. إنه مفيد لتحديد مجموعات الطبقات بسرعة—فكر فيه كعلامة بصرية يمكن تعيينها بألوان مثل البنفسجي، البرتقالي، الأصفر، إلخ.

## لماذا تغيير لون طبقة PSD برمجياً؟

- **الأتمتة:** معالجة مئات الملفات دون نقرات يدوية.  
- **الاتساق:** فرض نظام تسمية/لون عبر نظام التصميم.  
- **التكامل:** دمج معالجة PSD مع سير عمل آخر قائم على Java (مثل إنشاء أصول لتطبيقات الهواتف المحمولة).

## المتطلبات المسبقة

قبل الغوص في الكود، تأكد من أن لديك ما يلي:

- **Java Development Kit (JDK) 8+** – قم بتنزيله من [Java website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **IDE** – IntelliJ IDEA أو Eclipse أو NetBeans (حسب اختيارك).  
- **Aspose.PSD for Java library** – احصل عليها من [Aspose's website](https://releases.aspose.com/psd/java/).  
- **Sample PSD file** – `SheetColorHighlightExample.psd` (أنشئ ملفًا خاصًا بك أو احصل على عينة عبر الإنترنت).  
- **Basic Java knowledge** – يجب أن تكون مرتاحًا مع الفئات، والطرق، وإدخال/إخراج الملفات البسيط.

## استيراد الحزم

أولاً، استورد الفئات التي سنحتاجها. هذه الاستيرادات تمنحنا الوصول إلى معالجة الصور الأساسية، وتعديل الطبقات، والتعداد الخاص بتسليط الضوء على لون الورقة.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layerresources.SheetColorHighlightEnum;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل ملف PSD

#### 1.1 تعريف مسارات الملفات

قم بإعداد مسارات المصدر والوجهة. استبدل العنصر النائب بالمجلد الفعلي الذي يحتوي على ملف PSD الخاص بك.

```java
String dataDir = "YOUR DOCUMENT DIRECTORY";

String sourceFileName = dataDir + "SheetColorHighlightExample.psd";
String exportPath = dataDir + "SheetColorHighlightExampleChanged.psd";
```

#### 1.2 تحميل ملف PSD

استخدم `Image.load()` وحوّل النتيجة إلى `PsdImage` حتى نتمكن من العمل مع ميزات PSD الخاصة.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### الخطوة 2: الوصول إلى الطبقات وفحصها

تحمل الطبقات المحتوى البصري لملف PSD. سنقرأ تسليط الضوء على لون الورقة الحالي للتحقق من الحالة الأولية.

#### 2.1 الوصول إلى الطبقة الأولى

```java
Layer layer1 = im.getLayers()[0];
Assert.areEqual(SheetColorHighlightEnum.Violet, layer1.getSheetColorHighlight());
```

#### 2.2 الوصول إلى الطبقة الثانية

```java
Layer layer2 = im.getLayers()[1];
Assert.areEqual(SheetColorHighlightEnum.Orange, layer2.getSheetColorHighlight());
```

### الخطوة 3: تعديل تسليط الضوء على لون الورقة

الآن سنغير تسليط الضوء للطبقة الأولى إلى الأصفر، موضحين كيفية **change psd layer color** برمجياً.

```java
layer1.setSheetColorHighlight(SheetColorHighlightEnum.Yellow);
```

### الخطوة 4: حفظ ملف PSD المعدل

احفظ التغييرات في ملف جديد بحيث يبقى الأصلي دون تعديل.

```java
im.save(exportPath);
```

## المشكلات الشائعة والحلول

| المشكلة | سبب حدوثها | الحل |
|-------|----------------|-----|
| `Assert` fails | تسليط الضوء الحالي للطبقة ليس ما يتوقعه الكود (مثلاً، PSD مختلف). | افتح ملف PSD في Photoshop للتحقق من الألوان، أو أزل فحوصات `Assert` للحصول على سكريبت أكثر مرونة. |
| `NullPointerException` on `im.getLayers()` | لم يتم تحميل الملف بشكل صحيح (مسار خاطئ أو ملف معطوب). | تحقق مرة أخرى من `sourceFileName` وتأكد من صحة ملف PSD. |
| Highlight doesn’t appear in Photoshop | يقوم Photoshop بتخزين معلومات الطبقة مؤقتًا؛ قد تحتاج إلى إعادة فتح الملف. | أغلق وأعد فتح ملف PSD بعد الحفظ، أو استخدم `im.flush()` قبل الحفظ. |

## الأسئلة المتكررة

**س: ما هو Aspose.PSD for Java؟**  
ج: Aspose.PSD for Java هي مكتبة تتيح للمطورين قراءة وتعديل وحفظ ملفات PSD دون الحاجة إلى تثبيت Photoshop.

**س: هل يمكنني استخدام Aspose.PSD for Java مع صيغ ملفات أخرى؟**  
ج: نعم—تدعم BMP، PNG، JPEG، GIF، TIFF، والمزيد، مما يسمح بالتحويل من وإلى PSD.

**س: هل من الممكن التراجع عن التغييرات التي تم إجراؤها على ملف PSD باستخدام Aspose.PSD for Java؟**  
ج: بعد الحفظ، تصبح التغييرات دائمة. احتفظ بنسخة احتياطية من الملف الأصلي إذا كنت بحاجة إلى التراجع.

**س: كيف أحصل على ترخيص لـ Aspose.PSD for Java؟**  
ج: اشترِ ترخيصًا من [Aspose website](https://purchase.aspose.com/buy). إذا كنت تقوم بالتقييم، يمكنك طلب [temporary license](https://purchase.aspose.com/temporary-license/) لفترة محدودة.

**س: هل يمكنني تسليط الضوء على طبقات متعددة في آن واحد في ملف PSD؟**  
ج: بالطبع. قم بالتكرار عبر `im.getLayers()` واستدعِ `setSheetColorHighlight()` على كل طبقة حسب الحاجة.

---

**آخر تحديث:** 2026-04-03  
**تم الاختبار مع:** Aspose.PSD 24.11 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}