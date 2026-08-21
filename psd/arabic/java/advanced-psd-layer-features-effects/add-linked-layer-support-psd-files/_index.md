---
date: 2026-06-23
description: تعلم كيفية إنشاء ملفات PSD بطبقات مرتبطة باستخدام Aspose.PSD for Java.
  يوضح هذا الدليل خطوة بخطوة كيفية إضافة دعم الطبقات المرتبطة، ومعالجة ملفات PSD دفعة
  واحدة، وإلغاء ربط الطبقات بكفاءة.
keywords:
- create linked layers psd
- Aspose.PSD Java linking layers
- batch process PSD Java
linktitle: كيفية إنشاء ملفات PSD بطبقات مرتبطة باستخدام Java
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to create linked layers PSD files using Aspose.PSD for Java.
    This step‑by‑step tutorial shows how to add linked layer support, batch process
    PSD files, and unlink layers efficiently.
  headline: How to Create Linked Layers PSD Files Using Java
  type: TechArticle
- description: Learn how to create linked layers PSD files using Aspose.PSD for Java.
    This step‑by‑step tutorial shows how to add linked layer support, batch process
    PSD files, and unlink layers efficiently.
  name: How to Create Linked Layers PSD Files Using Java
  steps:
  - name: Load Your PSD File
    text: First, open the PSD you want to work with. The `PsdImage.load(String path)`
      method loads a PSD file into memory. Make sure the path points to an existing
      file; otherwise, `Image.load()` will throw an exception.
  - name: Retrieve All Layers (Manage PSD Layers)
    text: Obtain the document’s layer collection via `psdImage.getLayers()`, which
      returns an array of `Layer` objects. The `layers` array now holds the complete
      layer stack of the document.
  - name: Link the Layers
    text: Call `linkedLayersManager.linkLayers(Layer[] layers)` to create a linked‑layer
      group and receive a group ID. This call returns a **group ID** that uniquely
      identifies the new link group.
  - name: Verify the Link Group ID
    text: The returned integer `groupId` uniquely identifies the new link group; compare
      it with the first layer’s `getLinkGroupId()`. If the IDs differ, something went
      wrong during linking.
  - name: Retrieve and Unlink Layers (Unlink Layers PSD)
    text: Use `linkedLayersManager.getLinkedLayers(groupId)` to fetch linked layers,
      then `linkedLayersManager.unlinkLayer(Layer layer)` to remove each link. Each
      iteration removes the link while preserving the layer’s original data.
  - name: Validate the Unlink Process
    text: After unlinking, `linkedLayersManager.getLinkedLayers(groupId)` should return
      an empty collection. If `linkedLayers` is still populated, the unlink operation
      failed.
  - name: Save the Updated PSD
    text: Persist changes with `psdImage.save(String outputPath)` which writes the
      modified file to disk. Saving preserves all changes, including the new link
      group or its removal.
  - name: Dispose of the PSD Object
    text: Release native resources by invoking `psdImage.dispose()` when processing
      is complete. Calling `dispose()` is a best practice, especially when processing
      many files in a loop.
  type: HowTo
- questions:
  - answer: It creates a logical group so layers move together without being flattened.
    question: What does “link layers” mean?
  - answer: Aspose.PSD for Java provides a `LinkedLayersManager` API.
    question: Which library handles this?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license?
  - answer: Yes—use `unlinkLayer` or `unlinkLayers` methods.
    question: Can I unlink later?
  - answer: Java 8 or higher.
    question: Supported Java versions?
  type: FAQPage
second_title: Aspose.PSD Java API
title: كيفية إنشاء ملفات PSD بطبقات مرتبطة باستخدام Java
url: /ar/java/advanced-psd-layer-features-effects/add-linked-layer-support-psd-files/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء ملفات PSD بطبقات مرتبطة باستخدام Java  

## مقدمة  
صيغة `.PSD` من Adobe Photoshop لا تزال المعيار الصناعي للرسومات الطبقية، ويحتاج العديد من مطوري Java إلى معالجة تلك الطبقات دون تشغيل Photoshop. تسمح لك **إنشاء ملفات PSD بطبقات مرتبطة** بتجميع عدة طبقات بحيث تتحرك وتتحول معًا بينما تحتفظ كل طبقة بقابليتها للتحرير. في هذا الدرس الخاص بـ Aspose.PSD سنستعرض العملية الكاملة لإنشاء ملفات PSD بطبقات مرتبطة، وإدارة تلك الروابط، ومعالجة دفعة من الملفات المتعددة، وإلغاء ربط الطبقات عند الحاجة. سواء كنت تبني خط أنابيب لأتمتة التصميم، أو محررًا سحابيًا، أو مهمة CI تُعد الأصول، فإن إتقان التعامل مع الطبقات المرتبطة يمنحك تحكمًا دقيقًا في هياكل PSD.  

## إجابات سريعة  
- **ما معنى “link layers”؟** يخلق مجموعة منطقية بحيث تتحرك الطبقات معًا دون أن تُسطح.  
- **أي مكتبة تتعامل مع ذلك؟** توفر Aspose.PSD for Java واجهة برمجة تطبيقات `LinkedLayersManager`.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تعمل للتطوير؛ الترخيص التجاري مطلوب للإنتاج.  
- **هل يمكنني إلغاء الربط لاحقًا؟** نعم — استخدم طرق `unlinkLayer` أو `unlinkLayers`.  
- **إصدارات Java المدعومة؟** Java 8 أو أعلى.  

## ما هو ربط الطبقات في ملف PSD؟  
ربط الطبقات هو ميزة في Photoshop تربط عدة طبقات معًا بحيث تتصرف ككيان واحد عند التحويل أو النقل أو التعديل. تظل البيانات الأساسية منفصلة، مما يعني أنه يمكنك لاحقًا **إلغاء ربط طبقات PSD** وتحرير كل واحدة على حدة.  

## كيفية إنشاء ملفات PSD بطبقات مرتبطة باستخدام Java؟  
حمّل ملف PSD الخاص بك، اختر الطبقات التي تريد تجميعها، واستدعِ طريقة `linkLayers` — تقوم Aspose.PSD بكل عمليات التسجيل اللازمة في استدعاء API واحد، وتعيد معرف مجموعة فريد يمكنك تخزينه أو إعادة استخدامه لاحقًا. يعمل هذا النهج في أقل من ثانية لملفات ذات 10 طبقات نموذجية ويتوسع إلى مئات الطبقات مع استهلاك ذاكرة قليل.  

## لماذا تستخدم Aspose.PSD for Java لإدارة طبقات PSD؟  
تدعم Aspose.PSD **أكثر من 150 ميزة من Photoshop**، بما في ذلك طبقات الضبط، الأقنعة، الكائنات الذكية، وتأثيرات الطبقات، ويمكنها معالجة ملفات تصل إلى **2 GB** دون تحميل المستند بالكامل في الذاكرة. تعمل المكتبة على أي نظام تشغيل يدعم Java، مما يجعلها مثالية للخوادم بدون واجهة، خطوط أنابيب CI، أو أدوات سطح المكتب متعددة المنصات.  

## المتطلبات المسبقة  
قبل الغوص في الكود، تأكد من أن لديك:  

1. **Java Development Kit (JDK) 8+** – يُنصح بأحدث JDK.  
2. **Aspose.PSD for Java** – حمّل من [صفحة إصدارات Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE أو محرر** – Eclipse، IntelliJ IDEA، VS Code، إلخ.  
4. **ملف PSD تجريبي** – أنشئه في Photoshop أو احصل على عينة مجانية للاختبار.  

## استيراد الحزم  
فئة `LinkedLayersManager` هي نقطة الدخول في Aspose.PSD لإنشاء وإدارة مجموعات الطبقات المرتبطة. استورد الفئات اللازمة قبل البدء:  

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```  

تمنحك هذه الاستيرادات الوصول إلى معالجة الصور الأساسية، والميزات الخاصة بـ PSD، وطرق معالجة الطبقات.  

## دليل خطوة بخطوة  

### الخطوة 1: تحميل ملف PSD الخاص بك  
أولاً، افتح ملف PSD الذي تريد العمل معه. طريقة `PsdImage.load(String path)` تقوم بتحميل ملف PSD إلى الذاكرة.  

```java
String dataDir = "Your Document Directory"; // specify your document directory
PsdImage psd = (PsdImage) Image.load(dataDir + "LinkedLayerexample.psd");
```  

تأكد من أن المسار يشير إلى ملف موجود؛ وإلا ستطلق `Image.load()` استثناءً.  

### الخطوة 2: استرجاع جميع الطبقات (إدارة طبقات PSD)  
احصل على مجموعة طبقات المستند عبر `psdImage.getLayers()`، التي تُعيد مصفوفة من كائنات `Layer`.  

```java
Layer[] layers = psd.getLayers();
```  

الآن تحتوي مصفوفة `layers` على كامل مجموعة طبقات المستند.  

### الخطوة 3: ربط الطبقات  
استدعِ `linkedLayersManager.linkLayers(Layer[] layers)` لإنشاء مجموعة طبقات مرتبطة والحصول على معرف مجموعة.  

```java
short layersLinkGroupId = psd.getLinkedLayersManager().linkLayers(layers);
```  

تُعيد هذه الاستدعاء **معرف مجموعة** يحدد بشكل فريد مجموعة الربط الجديدة.  

### الخطوة 4: التحقق من معرف مجموعة الربط  
المتغير الصحيح `groupId` المُعاد يحدد بشكل فريد مجموعة الربط الجديدة؛ قارنها مع `getLinkGroupId()` للطبقة الأولى.  

```java
short linkGroupId = psd.getLinkedLayersManager().getLinkGroupId(layers[0]);
if (layersLinkGroupId != linkGroupId) {
    throw new Exception("layersLinkGroupId and linkGroupId are not equal.");
}
```  

إذا اختلفت المعرفات، فهناك خطأ ما حدث أثناء الربط.  

### الخطوة 5: استرجاع وإلغاء ربط الطبقات (Unlink Layers PSD)  
استخدم `linkedLayersManager.getLinkedLayers(groupId)` لجلب الطبقات المرتبطة، ثم `linkedLayersManager.unlinkLayer(Layer layer)` لإزالة كل ربط.  

```java
Layer[] linkedLayers = psd.getLinkedLayersManager().getLayersByLinkGroupId(linkGroupId);
for (Layer linkedLayer : linkedLayers) {
    psd.getLinkedLayersManager().unlinkLayer(linkedLayer);
}
```  

كل تكرار يزيل الربط مع الحفاظ على البيانات الأصلية للطبقة.  

### الخطوة 6: التحقق من عملية إلغاء الربط  
بعد إلغاء الربط، يجب أن تُعيد `linkedLayersManager.getLinkedLayers(groupId)` مجموعة فارغة.  

```java
linkedLayers = psd.getLinkedLayersManager().getLayersByLinkGroupId(linkGroupId);
if (linkedLayers != null) {
    throw new Exception("The linkedLayers field is not NULL.");
}
```  

إذا كانت `linkedLayers` لا تزال تحتوي على عناصر، فعملية إلغاء الربط فشلت.  

### الخطوة 7: حفظ ملف PSD المحدث  
احفظ التغييرات باستخدام `psdImage.save(String outputPath)` الذي يكتب الملف المعدل إلى القرص.  

```java
psd.save(dataDir + "LinkedLayerexample_output.psd");
```  

الحفظ يحافظ على جميع التغييرات، بما في ذلك مجموعة الربط الجديدة أو إزالتها.  

### الخطوة 8: تحرير كائن PSD  
حرّر الموارد الأصلية باستدعاء `psdImage.dispose()` عند الانتهاء من المعالجة.  

```java
finally {
    psd.dispose();
}
```  

استدعاء `dispose()` هو ممارسة جيدة، خاصة عند معالجة العديد من الملفات في حلقة.  

## كيفية إضافة دعم الطبقة المرتبطة في سير عمل معالجة دفعة ملفات PSD  
ضع الخطوات السابقة في حلقة بسيطة تتكرر عبر دليل يحتوي على ملفات PSD. لأن **Aspose.PSD** لا تحتاج إلى واجهة مستخدم، يمكنك تشغيل هذا الكود على خادم بدون واجهة، مما يجعله مثاليًا لسيناريوهات **batch process psd**. فقط تذكر إنشاء كائن `PsdImage` جديد لكل ملف لتجنب مشكلات سلامة الخيوط.  

## الأخطاء الشائعة والنصائح  

- **مسار ملف غير صحيح** – استخدم دائمًا مسارات مطلقة أو تحقق من دليل العمل.  
- **غياب الترخيص** – النسخة التجريبية تعمل للتقييم، لكن الترخيص الكامل يزيل العلامات المائية للتقييم.  
- **ربط جزء فقط** – إذا كنت تحتاج فقط جزءًا من مجموعة الطبقات، أنشئ مصفوفة `Layer[]` جديدة بالطبقات المطلوبة قبل استدعاء `linkLayers`.  
- **سلامة الخيوط** – كائنات `PsdImage` غير آمنة للاستخدام المتعدد الخيوط؛ أنشئ كائنًا منفصلًا لكل خيط.  

## الخلاصة  
أصبح لديك الآن سير عمل كامل وجاهز للإنتاج لإنشاء ملفات **how to create linked layers PSD** باستخدام Aspose.PSD for Java. من خلال إتقان هذه الواجهات البرمجية يمكنك أتمتة مهام التصميم المعقدة، بناء محررات مخصصة، أو دمج معالجة الطبقات بأسلوب Photoshop في أي تطبيق Java. استمر في تجربة ميزات أخرى مثل تأثيرات الطبقات، الأقنعة، والكائنات الذكية لتوسيع مجموعة أدواتك.  

## الأسئلة المتكررة  

**س:** ما هو Aspose.PSD for Java؟  
**ج:** Aspose.PSD for Java هي مكتبة تسمح للمطورين بمعالجة ملفات Photoshop PSD برمجيًا دون الحاجة إلى تثبيت Photoshop.  

**س:** هل يمكنني استخدام Aspose.PSD على أي نظام تشغيل؟  
**ج:** نعم، لأنها مبنية على Java، فهي تعمل على Windows، Linux، macOS، أو أي منصة تدعم Java.  

**س:** هل تتوفر نسخة تجريبية؟  
**ج:** نعم، يمكنك تجربة Aspose.PSD for Java مجانًا. تحقق من [رابط النسخة التجريبية](https://releases.aspose.com/).  

**س:** أين يمكنني العثور على مزيد من الوثائق؟  
**ج:** يمكنك استكشاف الوثائق الشاملة [هنا](https://reference.aspose.com/psd/java/).  

**س:** كيف يمكنني الحصول على الدعم إذا واجهت مشاكل؟  
**ج:** إذا واجهت أي مشاكل، يمكنك العثور على المساعدة في [منتدى الدعم](https://forum.aspose.com/c/psd/34).  

---  

**آخر تحديث:** 2026-06-23  
**تم الاختبار مع:** Aspose.PSD 24.12 for Java  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [استخراج طبقات PSD وإضافة دعم الطبقة لملفات PSD باستخدام Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)
- [إضافة طبقات تعبئة إلى ملفات PSD في Aspose.PSD for Java](/psd/java/modifying-converting-psd-images/add-fill-layers-psd-files/)
- [تطبيق طبقات الضبط Java - معالجة ملفات PSD باستخدام Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}