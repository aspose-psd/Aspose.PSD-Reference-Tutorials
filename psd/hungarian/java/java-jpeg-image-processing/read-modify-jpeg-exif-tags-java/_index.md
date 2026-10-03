---
date: 2026-10-03
description: Ismerje meg, hogyan java olvassa a képek metaadatait és módosítsa a JPEG
  EXIF címkéket az Aspose.PSD for Java segítségével ebben a lépésről‑lépésre útmutatóban,
  amely tökéletes a képek metaadataival hatékonyan dolgozó fejlesztők számára.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: JPEG EXIF címkék olvasása és módosítása Java-ban
og_description: Ismerje meg, hogyan java olvassa a képek metaadatait és módosítja
  a JPEG EXIF címkéket az Aspose.PSD for Java segítségével. Ez az útmutató lépésről‑lépésre
  bemutatja a kódot az EXIF információk kinyeréséhez és frissítéséhez.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: Hogyan java olvassuk a képek metaadatait és módosítsuk a JPEG EXIF címkéket
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: Hogyan java olvassuk a képek metaadatait és módosítsuk a JPEG EXIF címkéket
url: /hu/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JPEG EXIF címkék olvasása és módosítása Java-ban

## Bevezetés
Ha **java read image metadata**-t kell olvasnod JPEG fájlokból, és programozottan módosítani szeretnéd, a megfelelő helyen vagy. Ebben az útmutatóban végigvezetünk az EXIF címkék kinyerésén és frissítésén az Aspose.PSD for Java segítségével. A végére képes leszel lekérni a kamera részleteit, a tájolást és egyedi mezőket, majd visszaírni őket a fájlba – mindezt grafikus szerkesztő nélkül.

## Gyors válaszok
- **Melyik könyvtár kezeli a JPEG EXIF-et Java-ban?** Aspose.PSD for Java.
- **Hány sor kód szükséges az EXIF olvasásához?** Körülbelül három sor a kép betöltése után.
- **Módosíthatók az EXIF címkék?** Igen, bármely szabványos vagy egyedi címkét megváltoztathatsz, és elmentheted az eredményt.
- **Támogatott képfájl formátumok?** Több mint 150 formátum, beleértve a PSD, JPEG, PNG, TIFF és BMP formátumokat.
- **Minimális Java verzió?** Java 7 vagy újabb.

## Miért használjuk az Aspose.PSD for Java-t?
Az Aspose.PSD **150+ képfájl formátumot** támogat, és akár **2 GB** méretű fájlokat is képes feldolgozni anélkül, hogy a teljes dokumentumot a memóriába töltené, így gyors, alacsony memóriaigényű metaadat-műveleteket biztosít nagy fotógyűjteményeken. Emellett egyszerű API-t kínál az EXIF, IPTC és XMP adatok olvasásához és írásához, ami a több ezer kép batch feldolgozását hatékonnyá és megbízhatóvá teszi.

## Előfeltételek
1. **Java Development Kit (JDK)** – győződj meg róla, hogy JDK 11 vagy újabb van telepítve. Letöltheted a [Oracle weboldaláról](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java könyvtár** – szerezd be a legújabb JAR-t a [Aspose kiadási oldalról](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse vagy bármely kedvelt szerkesztő.  
4. **Alapvető Java ismeretek** – képesnek kell lenned projektek létrehozására és külső JAR-ok hozzáadására.

## Mi az a Java read image metadata?
A Java read image metadata a beágyazott információk, például EXIF, IPTC és XMP programozott hozzáférését jelenti képfájlokban Java kóddal. Ezek a metaadatok tartalmazhatnak kamera beállításokat, időbélyegeket, GPS koordinátákat, szerzői jogi megjegyzéseket és felhasználói kommentárokat, lehetővé téve az alkalmazások számára a képek szervezését, keresését és manipulálását leíró adataik alapján.

## Csomagok importálása
Először add hozzá az Aspose.PSD JAR-t a projekted classpath-jához, majd importáld a szükséges osztályokat.

A `com.aspose.psd` csomag biztosítja a mag API-t a képek betöltéséhez és erőforrásaik eléréséhez.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Hogyan olvassuk ki a képek metaadatait JPEG fájlokból Java-ban?
Töltsd be a JPEG-et a `PsdImage.load("image.jpg")` metódussal, keresd meg a bélyegkép erőforrást, amely az EXIF adatokat tartalmazza, majd hívd meg az `ExifData.read()`-t egy feltöltött `ExifData` objektum lekéréséhez. Ez az egylépéses megközelítés teljes hozzáférést biztosít minden szabványos EXIF mezőhöz és az esetlegesen hozzáadott egyedi címkékhez.

## 1. lépés: PSD kép betöltése
A PsdImage az Aspose.PSD osztálya, amely egy PSD fájlt reprezentál, és módszereket biztosít erőforrásai és metaadatai eléréséhez.  
Ebben a lépésben betöltjük azt a PSD képet, amelyből az EXIF adatokat szeretnénk kiolvasni. Győződj meg róla, hogy a kép a megfelelő könyvtárban van.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## 2. lépés: Képernyő erőforrások bejárása
A ThumbnailResource egy bélyegkép képet reprezentál, amely egy PSD fájlban tárolódik, és gyakran beágyazott EXIF adatokat tartalmaz.  
Miután a kép betöltődött, a következő lépés az erőforrások bejárása a bélyegkép erőforrás megtalálásához, amely általában az EXIF adatokat hordozza.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## 3. lépés: EXIF adatok kinyerése
A JpegExifData osztály tartalmazza a JPEG képből kinyert EXIF információkat, lehetővé téve az egyes címkék olvasását és módosítását.  
Most, hogy megvan a bélyegkép erőforrás, kinyerhetjük belőle az EXIF adatokat. Az EXIF adatok értékes információkat tartalmaznak, például a kamera tulajdonosának nevét, a rekeszértéket, a tájolást és egyebeket.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## 4. lépés: EXIF adatok módosítása
Az EXIF adatok olvasása után előfordulhat, hogy módosítani szeretnéd néhány mezőjét. Így teheted ezt meg:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## 5. lépés: Változások mentése
Végül, az EXIF adatok módosítása után mentsd el a változásokat egy új PSD fájlba.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Gyakori problémák és megoldások
- **Hiányzó bélyegkép erőforrás** – Egyes JPEG-ek közvetlenül a fő képfejlécben tárolják az EXIF-et. Ha a bélyegkép erőforrás hiányzik, használd helyette az `image.getExifData()` metódust.  
- **Nagy fájlok OutOfMemoryError-t okoznak** – Győződj meg róla, hogy a JVM elegendő halommal (`-Xmx2g`) fut, vagy dolgozd fel a képet streaming módban a `PsdImage.load(inputStream, loadOptions)` használatával.  
- **Nem támogatott címketípusok** – Az Aspose.PSD támogatja az összes szabványos EXIF címkét; az egyedi címkék esetén manuális bájtszintű kezelést igényelhetnek.

## Gyakran feltett kérdések

**K: Mi az EXIF adat?**  
V: Az EXIF (Exchangeable Image File Format) metaadatok a kamera beállításait, időbélyegeket, GPS koordinátákat és egyéb információkat tárolnak, amelyek JPEG és más képfájlokba vannak beágyazva.

**K: Használhatom ingyenesen az Aspose.PSD for Java-t?**  
V: Ingyenes próbaverziót kaphatsz a [Aspose releases page](https://releases.aspose.com/) oldalról.

**K: Az Aspose.PSD for Java kompatibilis-e minden Java verzióval?**  
V: Az Aspose.PSD for Java támogatja a Java SE 7-et és újabb verziókat.

**K: Hol találok további dokumentációt az Aspose.PSD for Java-hoz?**  
V: Tekintsd meg a [documentation](https://reference.aspose.com/psd/java/) oldalt a részletekért.

**K: Hogyan kaphatok támogatást az Aspose.PSD for Java-hoz?**  
V: Támogatást a [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/) oldalon kaphatsz.

## Összegzés
Ezeknek a lépéseknek a követésével **java read image metadata**-t tudsz kiolvasni bármely JPEG-ből, módosítani a szükséges EXIF mezőket, és visszaírni a frissített adatokat a fájlba – mindezt néhány tiszta Java sorral. Az Aspose.PSD gazdag API-ja megbízható és teljesítményorientált metaadat-kezelést biztosít, így könnyen integrálható batch feldolgozó csővezetékekbe, fotókezelő eszközökbe vagy bármely olyan alkalmazásba, amely képinformációkkal dolgozik.

---

**Last Updated:** 2026-10-03  
**Tested With:** Aspose.PSD for Java 24.5  
**Author:** Aspose

## Kapcsolódó oktatóanyagok

- [Specifikus EXIF címkék információinak olvasása Java-ban az Aspose (asp) segítségével](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [XMP metaadat létrehozása PSD fájlokban az Aspose.PSD for Java használatával](/psd/java/image-editing/create-xmp-metadata/)
- [Kép átméretezése az Aspose.PSD for Java-val – Alakzatok rajzolása és alapvető képműveletek](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}