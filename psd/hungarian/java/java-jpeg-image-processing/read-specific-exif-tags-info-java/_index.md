---
date: 2026-10-08
description: Ismerje meg, hogyan olvashatja ki az EXIF címkéket Java-ban az Aspose.PSD
  for Java (asp) segítségével lépésről‑lépésre útmutatónkban, és növelje képfeldolgozási
  képességeit.
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: Specifikus EXIF címkék információinak olvasása Java-ban
og_description: Olvassa ki az EXIF címkéket – a Java fejlesztők gyorsan kinyerhetik
  a képadatokat az Aspose.PSD használatával. Ez az útmutató végigvezeti a PSD betöltésén,
  a bélyegkép-erőforrások megtalálásán, és a kulcsfontosságú EXIF mezők, például a
  WhiteBalance és az ISO speed kiíratásán.
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: Hogyan olvassuk ki az EXIF címkéket Java-ban az Aspose.PSD segítségével
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  headline: How to read EXIF tags in Java with Aspose.PSD
  type: TechArticle
- description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  name: How to read EXIF tags in Java with Aspose.PSD
  steps:
  - name: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
    text: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
    text: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
  - name: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
    text: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
  type: HowTo
- questions:
  - answer: Aspose.PSD (asp)
    question: What library reads EXIF data from PSD in Java?
  - answer: WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength,
      and more.
    question: Which tags can be extracted?
  - answer: Yes, a commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: The same API supports PNG, JPEG, TIFF via Java image metadata extraction.
    question: Can I use this with other image formats?
  - answer: About 10‑15 minutes for a basic read‑only scenario.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- read exif tags java
- Aspose.PSD
- java image metadata extraction
- EXIF extraction
- PSD processing
title: Hogyan olvassuk ki az EXIF címkéket Java-ban az Aspose.PSD segítségével
url: /hu/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Olvassa el a specifikus EXIF címkék információit Java-ban az Aspose (asp) segítségével

## Bevezetés
Ha **EXIF címkék olvasása Java-ban**-ra van szüksége, az Aspose.PSD (asp) tiszta, tisztán Java‑alapú API‑t kínál, amely Photoshop nélkül működik. Ebben az útmutatóban megtanulja, hogyan vonja ki az EXIF adatokat egy PSD képből, hogyan válassza ki csak a kívánt címkéket, és hogyan írja ki azokat a konzolra. Kitérünk a fejlesztői környezet beállításától a metaadatok, például WhiteBalance, ISO speed és fókusztávolság kinyeréséig. Kezdjünk is!

## Gyors válaszok
- **Melyik könyvtár olvassa az EXIF adatokat PSD‑ből Java‑ban?** Aspose.PSD (asp)  
- **Mely címkék vonhatók ki?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength és még sok más.  
- **Szükség van licencre a termeléshez?** Igen, kereskedelmi licenc szükséges; ingyenes próba elérhető.  
- **Használható-e más képfájlformátumokkal?** Ugyanaz az API támogatja a PNG, JPEG, TIFF formátumokat a Java képadat‑metaadat kinyerésen keresztül.  
- **Mennyi időt vesz igénybe a megvalósítás?** Körülbelül 10‑15 perc egy alap, csak‑olvasás szcenárióhoz.

## Mi az asp (Aspose.PSD for Java)?
Az Aspose.PSD for Java egy tisztán Java‑alapú könyvtár, amely lehetővé teszi a fejlesztők számára, hogy Adobe Photoshop fájlokkal (PSD, PSB) dolgozzanak Photoshop telepítése nélkül. Programozott hozzáférést biztosít a rétegekhez, erőforrásokhoz és metaadatokhoz – beleértve az EXIF címkéket – így ideális **java image metadata extraction** feladatokhoz.

## Miért használja az Aspose.PSD‑t (asp) EXIF kinyeréshez?
Csak két metódushívással vonhat ki EXIF címkéket Java‑ban, és a könyvtár akár 2 GB‑os fájlokat is kezel anélkül, hogy a teljes dokumentumot a memóriába töltené. Támogat **30+ képfájlformátumot**, és pontosan megőrzi a kamera beállításait, determinisztikus eredményeket biztosítva Windows, Linux és macOS környezetekben.

## Előfeltételek
Mielőtt a kódba merülnénk, néhány dologra szüksége lesz:

1. Java Development Kit (JDK): Győződjön meg róla, hogy a JDK telepítve van a gépén. Letöltheti a [Oracle JDK weboldaláról](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. Aspose.PSD for Java: Töltse le a könyvtárat a [Aspose.PSD for Java letöltési oldalról](https://releases.aspose.com/psd/java/).  
3. Integrated Development Environment (IDE): Egy IDE, mint az IntelliJ IDEA, Eclipse vagy NetBeans, megkönnyíti a kódolást.  
4. PSD fájl: Egy EXIF adatokat tartalmazó PSD fájl. Használhatja ebben az útmutatóban szereplő mintát vagy bármely más, EXIF címkékkel rendelkező PSD fájlt.

## Csomagok importálása
Importálja a szükséges Aspose.PSD osztályokat, például az Image, PsdImage, ThumbnailResource és JpegExifData osztályokat a PSD fájlok kezeléséhez.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## 1. lépés: PSD kép betöltése
`Image.load()` betölt egy fájlt, és egy Image objektumot ad vissza, amely a képadatokat képviseli.  
`PsdImage` az Aspose.PSD osztály, amely PSD‑specifikus funkcionalitást biztosít.  
Az `Image.load()` metódus bármely támogatott képfájlt betölt a memóriába, egy általános `Image` objektumot ad vissza, amelyet PSD‑specifikus típusra lehet castolni.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

Ebben a lépésben a `Image.load()` metódussal töltjük be a PSD fájlt. A `PsdImage` osztályt használjuk a PSD kép reprezentálására, és a betöltött képet erre az osztályra castoljuk, hogy hozzáférjünk a PSD‑specifikus funkciókhoz.

## 2. lépés: képernyőforrások bejárása
`PsdImage.getResources()` egy beágyazott erőforrások gyűjteményét adja vissza, például bélyegképeket és EXIF adatokat.  
A `PsdImage.getResources()` hívás minden beágyazott erőforrást visszaad. Ennek a gyűjteménynek a bejárásával megtalálhatók azok a bélyegkép‑erőforrások, amelyek EXIF metaadatokat tartalmaznak.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

Egy `for` ciklussal végigiterálunk a képernyőforrásokon. A cél az, hogy azonosítsuk azokat az erőforrásokat, amelyek `ThumbnailResource` vagy `Thumbnail4Resource` példányai, mivel ezek a típusok tárolják az EXIF adatokat.

## 3. lépés: EXIF adatok kinyerése
`ThumbnailResource.getJpegOptions()` hozzáférést biztosít a JPEG beállításokhoz, beleértve az EXIF metaadatokat.  
`JpegExifData` egyedi EXIF címkeértékeket tartalmaz.  
A `ThumbnailResource.getJpegOptions()` metódus egy `JpegExifData` objektumhoz ad hozzáférést, amely egyedi EXIF címkéket, például WhiteBalance, ISOSpeed és FocalLength tárol.  
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

Egy `if` utasítással ellenőrizzük, hogy az erőforrás `ThumbnailResource` példány-e. Ha igen, castoljuk, és lekérjük a `JpegOptions`‑t, hogy hozzáférjünk az `ExifData`‑hoz. Végül kiírunk különböző EXIF címkéket, például WhiteBalance, Pixel Dimensions, ISOSpeed és FocalLength.

## Gyakori problémák és tippek
- **Null EXIF adat:** Egyes PSD fájlok nem tartalmaznak bélyegkép‑erőforrást EXIF információval. Mindig ellenőrizze a `null` értéket, mielőtt a címkeértékekhez hozzáférne.  
- **Fájlútvonal hibák:** Használjon abszolút útvonalakat, vagy győződjön meg róla, hogy a munkakönyvtár a PSD fájlt tartalmazó mappára mutat.  
- **Licenckorlátozások:** Az ingyenes próba korlátozza a feldolgozható oldalak számát; a teljes licencre való frissítés korlátlan használatot biztosít.

## Gyakran feltett kérdések
### Mi az EXIF adat?
Az EXIF (Exchangeable Image File Format) adatok olyan metaadatok, amelyek a képfájlokba vannak beágyazva, és információkat tartalmaznak a kamera beállításairól, a dátum‑időről és a képméretekről.

### Szerkeszthetem az EXIF adatokat az Aspose.PSD‑vel?
Igen, az Aspose.PSD lehetővé teszi az EXIF adatok olvasását és módosítását. Frissíthet címkéket, és a változtatásokat visszaírhatja a képfájlba.

### Ingyenes-e az Aspose.PSD for Java?
Az Aspose.PSD egy ingyenes próba verziót kínál, amely letölthető a [Aspose.PSD hivatalos kiadási oldaláról](https://releases.aspose.com/). A teljes funkciókhoz licenc vásárlása szükséges.

### Milyen egyéb formátumokat támogat az Aspose.PSD?
Az Aspose.PSD különféle Adobe Photoshop formátumokat támogat, beleértve a PSD, PSB és továbbiakat. Emellett lehetőséget nyújt ezek konvertálására PNG, JPEG, TIFF stb. formátumokra.

### Hogyan kaphatok támogatást az Aspose.PSD‑hez?
Támogatást kaphat az Aspose.PSD [fórumán](https://forum.aspose.com/c/psd/34).

### Hogyan segít ez a **java image metadata extraction** feladatban?
A `JpegExifData` objektum használatával programozottan kinyerhet bármely szükséges EXIF címkét, ami erős alapot biztosít a szélesebb körű metaadat‑kinyerési feladatokhoz különböző képfájlformátumok esetén.

---

**Utoljára frissítve:** 2026-10-08  
**Tesztelve:** Aspose.PSD for Java 24.11 (a cikk írásakor legújabb)  
**Szerző:** Aspose

## Kapcsolódó útmutatók

- [Read Modify Jpeg Exif Tags Java](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [Java Jpeg Image Processing](/psd/java/java-jpeg-image-processing/)
- [How to Rotate Image on a Specific Angle with Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}