---
date: 2026-09-28
description: A Java képfeldolgozási útmutató bemutatja, hogyan állítható be egy kép
  fényerője az Aspose.PSD for Java használatával. Kövesse a lépésről‑lépésre kódot
  a PSD vagy TIFF fájlok betöltéséhez, módosításához és mentéséhez.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Kép fényerőjének beállítása
og_description: A Java képfeldolgozási útmutató bemutatja, hogyan állítható be egy
  kép fényerője az Aspose.PSD for Java használatával. Kövesse a lépésről‑lépésre kódot
  a PSD vagy TIFF fájlok betöltéséhez, módosításához és mentéséhez.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Java képfeldolgozás: fényerő beállítása az Aspose.PSD segítségével'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Java képfeldolgozás: fényerő beállítása az Aspose.PSD segítségével'
url: /hu/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kép fényerősségének beállítása az Aspose.PSD for Java-val

## Bevezetés

Ebben a **java image processing** oktatóanyagban megtanulja, hogyan állíthatja be egy kép fényerősségét közvetlenül Java kódból. A fényerő finomhangolása gyakori feladat a grafikusok, fotósok és mindenki számára, aki képfeldolgozó csővezetékeket épít. Ebben a **java image manipulation** útmutatóban végigvezetjük a teljes munkafolyamatot – PSD/TIFF betöltése, fényerő eltolás alkalmazása és az eredmény mentése – az Aspose.PSD for Java könyvtár használatával.

## Gyors válaszok
- **Melyik könyvtár kezeli a fényerőt?** Aspose.PSD for Java.  
- **Melyik metódus változtatja a fényerőt?** `RasterImage.adjustBrightness()`.  
- **Dolgozhatok PSD és TIFF fájlokkal?** Igen, az API támogatja mindkét formátumot és 10+ további képtípust.  
- **Szükségem van licencre a termeléshez?** Kereskedelmi licenc szükséges a nem‑értékelő használathoz.  
- **Mennyi időt vesz igénybe a megvalósítás?** Általában 10 perc alatt egy alap beállítás esetén.

## Mi az java képfeldolgozás?
`Java image processing` a technikák összességét jelenti, amelyek lehetővé teszik, hogy programozott módon olvass, alakíts és írj képadatokat Java segítségével. A fényerő beállítása az egyik alapvető művelet, amely minden pixel általános világosságát módosítja, sötét területeket világosabbá, a világos területeket sötétebbé téve.

## Miért használjuk az Aspose.PSD for Java-t?
Az Aspose.PSD for Java átfogó, pure‑Java megoldást nyújt, amely támogatja a széles körű raszter és vektor formátumokat, megszünteti a natív függőségeket, és nagy fájlokhoz magas teljesítményű gyorsítótárazást kínál. Kiterjedt API-ja lehetővé teszi a fejlesztők számára, hogy komplex színkorrekciós és réteg‑alapú szerkesztéseket végezzenek minimális kóddal, így ideális egyszerű beállításokhoz és fejlett képfeldolgozó csővezetékekhez egyaránt.
- **Támogatja a 10+ raszter és vektor formátumot** – PSD, TIFF, JPEG, PNG, BMP, GIF és továbbiak.  
- **Pure‑Java megvalósítás** – nincs natív DLL vagy külső függőség, így bármely JVM-en működik.  
- **Magas teljesítményű gyorsítótárazás** – a raszter adatokat gyorsítótárazni lehet, ami akár 2× gyorsabb ismételt szerkesztést tesz lehetővé nagy fájloknál.  
- **Gazdag API felület** – több mint 150 metódus színkorrekcióhoz, rétegkezeléshez, maszkokhoz és kompozíciókhoz.

## Előfeltételek

Mielőtt belemerülne az oktatóanyagba, győződjön meg róla, hogy rendelkezik a következő előfeltételekkel:
- Aspose.PSD for Java Library: Töltse le és telepítse a könyvtárat a [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) oldalról.  
- Java Development Kit (JDK) 8 vagy magasabb telepítve a gépén.  
- Fejlesztői környezet (IDE), például IntelliJ IDEA, Eclipse vagy VS Code.

## Csomagok importálása

A kezdéshez importálja a szükséges csomagokat a Java projektjébe. Ebben a példában a következőket használjuk:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Most bontsuk le a kép fényerő beállításának folyamatát egyszerű lépésekre:

## Hogyan állítsuk be a fényerőt az Aspose.PSD segítségével?

Töltse be a forrásképet, alkalmazzon egy fényerő eltolást, konfigurálja a mentési beállításokat, és írja az eredményt lemezre – mindezt négy tömör lépésben. A következő szakaszok világos, lépésről‑lépésre útmutatót nyújtanak, amelyet beilleszthet a saját projektjébe. Ez a megközelítés biztosítja, hogy minden művelet hatékonyan történjen, és a végső kép megőrizze az eredeti minőséget, miközben a kívánt fényerő változást tükrözi.

### 1. lépés: Kép betöltése

A `RasterImage` osztály egy PSD vagy TIFF fájl rasterizált változatát képviseli a memóriában. Közvetlen pixelhozzáférést biztosít a színkorrekciós műveletekhez.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Ebben a lépésben betöltjük a célképet, és `RasterImage`‑re cast-eljük a további feldolgozáshoz.

### 2. lépés: Fényerő beállítása

`adjustBrightness(int value)` minden pixel fényességét módosítja a megadott egész értékkel. A pozitív számok világosabbá teszik a képet; a negatív számok sötétebb. A metódus a képet helyben dolgozza fel, így nincs szükség további objektum létrehozására.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Itt a `adjustBrightness` metódust használjuk a kép fényerőjének módosításához. Ebben a példában 50 egységgel csökkentjük a fényerőt, de igényei szerint testre szabhatja ezt az értéket.

### 3. lépés: TiffOptions beállítása

`TiffOptions` meghatározza a TIFF kimenet kódolási paramétereit, például a mintánkénti bitek számát és a fotometrikus interpretációt. Lehetővé teszi, hogy szabályozza, hogyan kódolják a létrejövő fájlt.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Állítsa be a `TiffOptions`‑t a módosított kép mentéséhez. A `bitsPerSample` és `photometric` tulajdonságokat a konkrét igényei szerint módosítsa.

### 4. lépés: Az eredménykép mentése

`save` hívása a feldolgozott raszter adatokat egy fájlba írja a korábban definiált beállításokkal. A művelet atomikus, és garantálja, hogy a kimeneti fájl érvényes TIFF kép legyen.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Végül mentse a módosított képet a megadott `TiffOptions` használatával.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| **`ClassCastException` a kép cast-olásakor** | A fájl nem raszter kép (pl. vektor PSD). | Ellenőrizze a forrásfájl formátumát, vagy a cast előtt használja a `image instanceof RasterImage` kifejezést. |
| **A fényerő változtatásnak nincs hatása** | A kép nem volt gyorsítótárazva a beállítás előtt. | Hívja meg a `rasterImage.cacheData()`‑t, ahogy az 1. lépésben látható. |
| **A mentett fájl sérültnek tűnik** | Helytelen `TiffOptions` konfiguráció. | Győződjön meg arról, hogy a `bitsPerSample` megegyezik a forráskép mélységével (általában 8‑bit csatornánként). |

## Gyakran ismételt kérdések

**Q: Adjustálhatom a fényerőt más képtípusokban is a PSD-n kívül?**  
A: Igen, az Aspose.PSD for Java támogatja a JPEG, PNG, BMP, GIF és számos más raszter formátumot a PSD és TIFF mellett.

**Q: Hogyan kezeljem a hibákat a kép beállítási folyamat során?**  
A: A feldolgozó kódot helyezze try‑catch blokkba, és fogja el az `IOException` vagy `ImageProcessingException` kivételeket a fájlhozzáférési és raszter‑műveleti hibák kezeléséhez.

**Q: Van korlát a fényerő beállítás tartományára?**  
A: A metódus -255 és +255 közötti egész értékeket fogad; a tartományon kívüli értékek a legközelebbi határra lesznek korlátozva.

**Q: Használhatom az Aspose.PSD for Java‑t kereskedelmi projektekben?**  
A: Igen, a termeléshez kereskedelmi licenc szükséges. Licencet vásárolhat [itt](https://purchase.aspose.com/buy).

**Q: Elérhető ingyenes próba?**  
A: Igen, a könyvtárat ingyenes próba verzióval is kipróbálhatja [innen](https://releases.aspose.com/).

**Q: Befolyásolja a `adjustBrightness` metódus a rétegek láthatóságát?**  
A: A metódus a rasterizált kompozit képen dolgozik, így a rejtett rétegek a rasterizálás során figyelmen kívül maradnak, megőrizve a kívánt vizuális eredményt.

**Q: Láncolhatok több beállítást (pl. kontraszt, telítettség) egymás után?**  
A: Természetesen. A fényerő beállítása után meghívhatja a `adjustContrast`, `adjustSaturation` vagy más színkorrekciós metódusokat ugyanazon `RasterImage` példányon.

**Utoljára frissítve:** 2026-09-28  
**Tesztelve:** Aspose.PSD for Java 24.12 (a legújabb a írás időpontjában)  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [Java képfeldolgozó könyvtár: Réteg invertálása az Aspose.PSD segítségével](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Kép konvertálása szürkeárnyalatosra az Aspose.PSD for Java használatával](/psd/java/advanced-techniques/grayscale-image/)
- [Hogyan forgassuk el a képet egy adott szöggel az Aspose.PSD for Java-val](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}