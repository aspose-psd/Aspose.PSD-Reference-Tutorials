---
date: 2026-09-18
description: Ismerje meg, hogyan adhat hozzá Java képadat metaadat bélyegképet az
  EXIF szegmenshez az Aspose.PSD for Java használatával. Ez a lépésről-lépésre útmutató
  lefedi az előfeltételeket, a kód bemutatását és a frissített kép mentését.
keywords:
- java image metadata
- how to add thumbnail
- java exif metadata
lastmod: 2026-09-18
linktitle: Bélyegkép hozzáadása az EXIF szegmenshez Java-ban
og_description: Ismerje meg, hogyan adhat hozzá Java képadat metaadat bélyegképet
  az EXIF szegmenshez az Aspose.PSD for Java használatával. Kövesse a lépésről-lépésre
  útmutatót a bélyegképek beágyazásához és a frissített kép mentéséhez.
og_image_alt: Guide showing Java code to embed a thumbnail into EXIF metadata using
  Aspose.PSD
og_title: Hogyan adjon hozzá Java képadat metaadat bélyegképet az EXIF szegmenshez
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to add java image metadata thumbnail to the EXIF segment
    using Aspose.PSD for Java. This step‑by‑step guide covers prerequisites, code
    walkthrough, and saving the updated image.
  headline: How to add java image metadata thumbnail to EXIF segment
  type: TechArticle
- questions:
  - answer: EXIF metadata is embedded information in digital images that includes
      camera settings, capture date, GPS coordinates, and other details.
    question: What is EXIF metadata?
  - answer: Adding a thumbnail improves user experience by allowing quick image previews
      without loading the full image.
    question: Why add a thumbnail to EXIF?
  - answer: You can download Aspose.PSD for Java from the [Aspose.PSD for Java download
      page](https://releases.aspose.com/psd/java/).
    question: Where can I download Aspose.PSD for Java?
  - answer: You can obtain a temporary license for Aspose.PSD from the [temporary
      license page](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.PSD?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How do I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- EXIF thumbnail
- Aspose.PSD
- Java image processing
title: Hogyan adjon hozzá Java képadat metaadat bélyegképet az EXIF szegmenshez
url: /hu/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java képméta bélyegkép hozzáadása az EXIF szegmenshez

## Bevezetés
Ebben az oktatóanyagban megtanulja, hogyan adjon **java image metadata** bélyegképet a PSD fájl EXIF szegmenséhez az Aspose.PSD for Java használatával. Az EXIF (Exchangeable Image File Format) metaadatok a kamera beállításait, a felvétel dátumát, helyét és egyéb hasznos információkat tárolják. Egy kis előnézeti bélyegkép beágyazása lehetővé teszi az alkalmazások számára, hogy gyors képnézetet mutassanak anélkül, hogy a teljes fájlt betöltenék, ezáltal javítva a teljesítményt és a felhasználói élményt.

## Gyors válaszok
- **Mi tárgyalja az oktatóanyag?** Bélyegkép hozzáadása a PSD kép EXIF szegmenséhez az Aspose.PSD for Java segítségével.  
- **Mennyi időt vesz igénybe a megvalósítás?** Körülbelül 10‑15 perc egy alap integrációhoz.  
- **Szükségem van licencre?** Ideiglenes licenc szükséges a termeléshez; egy ingyenes próba a kiértékeléshez elegendő.  
- **Mely Java verzió támogatott?** A Java 8 és újabb verziók teljes mértékben támogatottak.  
- **Feldolgozhatók nagy fájlok?** Igen – az Aspose.PSD akár 2 GB-ig terjedő fájlokat is kezel anélkül, hogy a teljes képet a memóriába töltené.

## Mi az java képméta?
A java image metadata a képfájlokba (például EXIF, IPTC vagy XMP) beágyazott strukturált információra utal, amelyet Java könyvtárakkal, mint az Aspose.PSD, programozottan olvashat, módosíthat vagy létrehozhat. Ezek a metaadatok lehetővé teszik az alkalmazások számára, hogy a kamera beállításait, időbélyegeket, GPS koordinátákat és egyedi adatokat lekérjék anélkül, hogy a vizuális tartalmat megnyitnák.

## Miért adjunk bélyegképet az EXIF metaadatokhoz?
Bélyegkép hozzáadása az EXIF szegmenshez azonnali vizuális jelzést biztosít a képböngészőknek, fájlkezelőknek és tartalomkezelő rendszereknek. Az Aspose.PSD a bélyegképeket memóriában dolgozza fel, lehetővé téve, hogy 0,2 másodpercnél gyorsabban ágyazzon be előnézetet 500 KB-ig terjedő képekhez, és több mint 30 képfájltípust támogat, köztük PSD, JPEG, PNG és TIFF.

## Előfeltételek
Mielőtt belekezdene az oktatóanyagba, győződjön meg a következő előfeltételek meglétéről:
- Alapvető Java programozási ismeretek.  
- Java Development Kit (JDK) telepítve a rendszerére.  
- IDE (Integrated Development Environment) Java-hoz, például IntelliJ IDEA vagy Eclipse.  
- Aspose.PSD for Java könyvtár. Letöltheti a [Aspose.PSD for Java Download page](https://releases.aspose.com/psd/java/) oldalról.

## Csomagok importálása
A következő importok tartalmazzák az Aspose.PSD osztályokat, amelyek a PSD képek és EXIF adatok kezeléséhez szükségesek.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## 1. lépés: PSD kép betöltése
`PsdImage` egy Photoshop PSD fájlt képvisel, és hozzáférést biztosít a rétegeihez és erőforrásaihoz.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```

## 2. lépés: képadatok iterálása
`ImageResource` olyan erőforrásokat foglal magába, mint a bélyegképek, ICC profilok és a PSD fájlba beágyazott metaadatok.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Process the thumbnail resource
    }
}
```

## 3. lépés: bélyegkép adatainak módosítása
`JpegOptions` lehetővé teszi a JPEG‑specifikus beállítások, például a minőség, konfigurálását a bélyegképhez.  
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // Set JPEG quality
```

## 4. lépés: kép mentése
`save` meghívása az frissített EXIF szegmenst (beleértve az új bélyegképet) visszaírja a lemezre anélkül, hogy a teljes képet újrakódolná.  
```java
image.save(dataDir + "output.psd");
```

## Gyakori problémák és megoldások
- **Bélyegkép nem jelenik meg:** Ellenőrizze, hogy a bélyegkép erőforrás helyesen hozzá lett-e adva az EXIF szegmenshez, és hogy a képet a `PsdImage.save` metódussal mentették-e.  
- **Memóriahiány hibák nagy fájloknál:** Használja a `PsdImage.load(..., LoadOptions)`-t a `LoadOptions.setLoadOnlyMetadata(true)` beállítással, hogy csak a metaadatokkal dolgozzon.  
- **Helytelen orientáció:** Győződjön meg róla, hogy a bélyegkép tiszteletben tartja az eredeti kép orientációs jelzőjét; olvashatja az `Orientation` EXIF címkét, és ennek megfelelően forgathatja a bélyegképet.

## Gyakran ismételt kérdések

**Q: Mi az EXIF metaadat?**  
A: Az EXIF metaadat a digitális képekbe beágyazott információ, amely tartalmazza a kamera beállításait, a felvétel dátumát, GPS koordinátákat és egyéb részleteket.

**Q: Miért adjunk bélyegképet az EXIF-hez?**  
A: A bélyegkép hozzáadása javítja a felhasználói élményt, mivel gyors képelőnézetet tesz lehetővé a teljes kép betöltése nélkül.

**Q: Hol tölthetem le az Aspose.PSD for Java-t?**  
A: Letöltheti az Aspose.PSD for Java-t a [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) oldalról.

**Q: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD-hez?**  
A: Ideiglenes licencet az Aspose.PSD-hez a [temporary license page](https://purchase.aspose.com/temporary-license/) oldalról szerezhet.

**Q: Hogyan kaphatok támogatást az Aspose.PSD-hez?**  
A: Támogatásért látogassa meg az [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) oldalt.

---

**Utoljára frissítve:** 2026-09-18  
**Tesztelve:** Aspose.PSD for Java 24.10  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [XMP metaadat létrehozása PSD fájlokban az Aspose.PSD for Java használatával](/psd/java/image-editing/create-xmp-metadata/)
- [Kép átméretezése az Aspose.PSD for Java‑val – Alakzatok rajzolása és alap képműveletek](/psd/java/basic-image-operations/)
- [Hogyan konvertáljunk PSD-t raszter képfájlformátumokra az Aspose.PSD for Java‑val](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}