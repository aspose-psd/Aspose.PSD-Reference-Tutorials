---
title: JPEG EXIF címkék olvasása és módosítása Java nyelven
linktitle: JPEG EXIF címkék olvasása és módosítása Java nyelven
second_title: Aspose.PSD Java API
description: Ebből a lépésről lépésre szóló útmutatóból megtudhatja, hogyan olvashat és módosíthat JPEG EXIF címkéket az Aspose.PSD for Java használatával. Tökéletes azoknak a fejlesztőknek, akik könnyedén szeretnék kezelni a képek metaadatait.
weight: 18
url: /hu/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JPEG EXIF címkék olvasása és módosítása Java nyelven

## Bevezetés
Szia! Gondolkozott már azon, hogyan olvashatja és módosíthatja a JPEG EXIF címkéket Java használatával? Ha igen, akkor jó helyen jársz! Ez az oktatóanyag lépésről lépésre végigvezeti a folyamaton az Aspose.PSD for Java használatával. Akár tapasztalt fejlesztő, akár kezdő, ennek az útmutatónak a végére profiként fog tudni kezelni a JPEG EXIF címkéket. Szóval, merüljünk bele!
## Előfeltételek
Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik az alábbiakkal:
1.  Java Development Kit (JDK): Győződjön meg arról, hogy a JDK telepítve van a rendszeren. Letöltheti a[Oracle webhely](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD for Java Library: Le kell töltenie az Aspose.PSD for Java könyvtárat. Szerezd meg a[Az Aspose kiadási oldala](https://releases.aspose.com/psd/java/).
3. Integrált fejlesztői környezet (IDE): Az olyan IDE, mint az IntelliJ IDEA vagy az Eclipse, simábbá teszi a kódolási élményt.
4. Alapvető Java-ismeretek: Az oktatóanyag követéséhez a Java alapvető ismerete szükséges.
## Csomagok importálása
Először is importáljuk a szükséges csomagokat. Nyissa meg a Java IDE-jét, és hozzon létre egy új Java projektet. Ezután vegye fel az Aspose.PSD for Java könyvtárat a projektfüggőségek közé.
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## 1. lépés: Töltse be a PSD-képet
Ebben a lépésben betöltjük azt a PSD-képet, amelyről az EXIF-adatokat ki szeretnénk olvasni. Győződjön meg arról, hogy a kép a megfelelő könyvtárban van.
```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```
## 2. lépés: Ismételje meg a képforrásokat
A kép betöltése után a következő lépés az erőforrások iterációja, hogy megtalálja a miniatűr erőforrást, amely általában az EXIF-adatokat tartalmazza.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Folytassa a következő lépéssel
    }
}
```
## 3. lépés: EXIF adatok kibontása
Most, hogy megvan a miniatűr erőforrás, kinyerhetjük belőle az EXIF adatokat. Az EXIF-adatok olyan értékes információkat tartalmaznak, mint a fényképezőgép tulajdonosának neve, rekesznyílás értéke, tájolása stb.
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
## 4. lépés: Módosítsa az EXIF-adatokat
Az EXIF adatok elolvasása után érdemes lehet módosítani néhány mezőt. A következőképpen teheti meg:
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
## 5. lépés: Mentse el a változtatásokat
Végül az EXIF-adatok módosítása után mentse el a változtatásokat egy új PSD-fájlba.
```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Következtetés
És megvan! Az alábbi lépések követésével könnyedén olvashatja és módosíthatja a JPEG EXIF címkéket az Aspose.PSD for Java használatával. Ezzel a nagy teljesítményű könyvtárral gyerekjáték a képek metaadatainak kezelése. Tehát próbálja ki saját projektjein. Boldog kódolást!
## GYIK
### Mi az EXIF adat?
Az EXIF (Exchangeable Image File Format) adatok metaadatokat tartalmaznak a képről, például a fényképezőgép beállításait és tájolását.
### Használhatom ingyenesen az Aspose.PSD for Java-t?
 Ingyenes próbaverziót kaphat a[Az Aspose kiadási oldala](https://releases.aspose.com/).
### Az Aspose.PSD for Java kompatibilis a Java összes verziójával?
Az Aspose.PSD for Java támogatja a Java SE 7 és újabb verzióit.
### Hol találok további dokumentációt az Aspose.PSD for Java-ról?
 Nézze meg a[dokumentáció](https://reference.aspose.com/psd/java/) további részletekért.
### Hogyan kaphatok támogatást az Aspose.PSD for Java számára?
 Támogatást kaphat a[Aspose PSD támogatási fórum](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
