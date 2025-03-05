---
title: Bélyegkép kibontása a PSD-ből Java nyelven
linktitle: Bélyegkép kibontása a PSD-ből Java nyelven
second_title: Aspose.PSD Java API
description: Ismerje meg, hogyan bonthat ki miniatűröket PSD-fájlokból az Aspose.PSD for Java használatával. Ez a részletes útmutató a beállítástól a kinyert képek mentéséig mindent lefed.
type: docs
weight: 15
url: /hu/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## Bevezetés
Ebben az oktatóanyagban megvizsgáljuk, hogyan lehet miniatűröket kivonni PSD-fájlokból az Aspose.PSD for Java segítségével. A miniatűrök hasznosak lehetnek a gyors előnézetekhez vagy a PSD dokumentumokba ágyazott képek kisebb verzióinak létrehozásához. Vessen egy pillantást az Aspose.PSD használatához szükséges lépésekre.
## Előfeltételek
Mielőtt elkezdené, győződjön meg arról, hogy az alábbiakat beállította:
- Java Development Kit (JDK) telepítve a rendszerére.
-  Aspose.PSD a Java könyvtárhoz. Letöltheti innen[itt](https://releases.aspose.com/psd/java/).
- Java programozási alapismeretek.
## Csomagok importálása
A kezdéshez vegye fel a szükséges Aspose.PSD csomagot a Java osztályba:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## 1. lépés: Töltse be a PSD fájlt
Először töltse be a PSD-fájlt, amely tartalmazza a kicsomagolni kívánt bélyegképet.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Cserélje ki`"Your_Document_Directory/"` a könyvtár elérési útjával, ahol a PSD-fájl található, és`"your_file.psd"` a PSD-fájl nevével.
## 2. lépés: Ismételje meg a képforrásokat
Iteráljon a képforrásokon, hogy megtalálja a miniatűr erőforrást.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Miniatűr adatok kibontása
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Hozzon létre egy új képet a kibontott miniatűr adatokkal
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Mentse el a kibontott bélyegképet külön JPEG fájlként
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Sikerüzenet megjelenítése
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // A miniatűr megtalálása és feldolgozása után lépjen ki a ciklusból
    }
}
```
## 3. lépés: Mentse el a kibontott bélyegképet
Mentse el a kibontott bélyegképet külön képfájlként (jelen esetben JPEG fájlként).
## 4. lépés: Különböző miniatűr típusok kezelése
 Ha a PSD-fájl többféle bélyegképet is tartalmazhat, mint pl`Thumbnail4Resource`, kibővítheti a logikát az esetek hasonló kezelésére.

## Következtetés
Ebben az oktatóanyagban megvizsgáltuk, hogyan lehet miniatűröket kivonni PSD-fájlokból az Aspose.PSD for Java használatával. A fent vázolt lépések követésével hatékonyan lekérheti és mentheti a PSD-dokumentumokba ágyazott miniatűröket.

## GYIK
### Mi az Aspose.PSD?
Az Aspose.PSD egy Java-könyvtár, amely lehetővé teszi a fejlesztők számára, hogy programozottan dolgozzanak PSD-vel és más képfájlformátumokkal.
### Hol találok további dokumentációt az Aspose.PSD for Java-ról?
 Hivatkozhat a[dokumentáció](https://reference.aspose.com/psd/java/) részletes API-referenciákért és példákért.
### Vásárlás előtt ingyenesen kipróbálhatom az Aspose.PSD-t?
 Igen, letöltheti a[ingyenes próbaverzió](https://releases.aspose.com/) hogy értékelje a könyvtár képességeit.
### Hogyan szerezhetek ideiglenes licenceket az Aspose.PSD-hez?
 Ideiglenes engedélyek szerezhetők be[itt](https://purchase.aspose.com/temporary-license/).
### Az Aspose.PSD alkalmas kereskedelmi használatra?
Igen, az Aspose.PSD felhasználható személyes és kereskedelmi projektekhez is a licencfeltételei szerint.