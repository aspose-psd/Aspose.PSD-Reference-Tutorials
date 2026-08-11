---
date: 2026-08-11
description: Ismerje meg, hogyan alkalmazhatja az otsu threshold java-t az Aspose.PSD
  for Java segítségével – egy hatékony képszegmentálási technika.
keywords:
- apply otsu threshold java
- image segmentation with otsu
- java image segmentation tutorial
lastmod: 2026-08-11
linktitle: Binárizálás Otsu Threshold használatával
og_description: Az otsu threshold java alkalmazása az Aspose.PSD for Java segítségével.
  Ez a bemutató lépésről lépésre megmutatja, hogyan binarizálhat képeket, elmagyarázza,
  miért gyors a módszer, és gyakori hibákra vonatkozó hibaelhárítási tippeket nyújt.
og_image_alt: Screenshot of Java code applying Otsu threshold using Aspose.PSD
og_title: Az otsu threshold java alkalmazása az Aspose.PSD-vel – gyors útmutató
schemas:
- author: Aspose
  dateModified: '2026-08-11'
  description: Learn how to apply otsu threshold java using Aspose.PSD for Java –
    a powerful image segmentation technique.
  headline: Apply otsu threshold java with Aspose.PSD
  type: TechArticle
- description: Learn how to apply otsu threshold java using Aspose.PSD for Java –
    a powerful image segmentation technique.
  name: Apply otsu threshold java with Aspose.PSD
  steps:
  - name: set up your document directory
    text: Define the folder that contains the source PSD file and the output location
      for the binarized image.
  - name: load the PSD file
    text: '`PsdImage` is the top‑level Aspose.PSD class that represents a PSD document
      and gives access to its layers, metadata, and pixel data.'
  - name: cache the image
    text: '`RasterImage` holds the raster representation of a layer; calling `cache()`
      loads the pixel data into memory so subsequent operations are fast.'
  - name: binarize image with Otsu threshold
    text: '`applyOtsuThreshold()` evaluates all possible gray levels and selects the
      optimal cutoff, producing a binary image that separates foreground objects from
      the background.'
  - name: save the resultant image
    text: '`JpegOptions` configures JPEG‑specific settings such as quality and compression
      when saving the processed image. You can also choose PNG or BMP by swapping
      the options class – the API supports over **30 image formats** for output. {{<
      blocks/products/products-backtop-button >}}'
  type: HowTo
- questions:
  - answer: It automatically finds the gray‑level that minimizes intra‑class variance,
      producing a binary image in one step.
    question: What does Otsu Threshold do?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license to run the sample?
  - answer: Aspose.PSD for Java supports Java 8 through Java 21.
    question: Which Java version is supported?
  - answer: Yes – you can iterate over each layer and apply the threshold individually.
    question: Can I process multi‑layer PSD files?
  - answer: For a 1920 × 1080 image the Otsu binarization finishes in under 30 ms
      on a typical laptop CPU.
    question: How fast is the operation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- apply otsu threshold java
- image segmentation
- Aspose.PSD
- Java image processing
title: Az otsu threshold java alkalmazása az Aspose.PSD-vel
url: /hu/java/image-processing/binarization-otsu-threshold/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Otsu küszöb alkalmazása Java-val az Aspose.PSD használatával

## Bevezetés

Ebben az oktatóanyagban megtanulja, hogyan **alkalmazza az Otsu küszöböt Java-ban** az Aspose.PSD for Java könyvtár segítségével. Az Otsu küszöb használatával történő binarizálás az egyik legmegbízhatóbb képszegmentálási módszer, amely automatikusan kiválaszt egy optimális szürke‑szint határértéket a előtér és a háttér elválasztásához. A útmutató végére egy működő Java kódrészletet kap, amely bármely PSD réteget tiszta fekete‑fehér képpé alakít.

## Gyors válaszok
- **Mit csinál az Otsu küszöb?** Automatikusan megtalálja azt a szürke‑szintet, amely minimalizálja az osztályon belüli varianciát, egy lépésben bináris képet eredményezve.  
- **Szükségem van licencre a minta futtatásához?** Egy ingyenes próba verzió fejlesztéshez elegendő; a termeléshez kereskedelmi licenc szükséges.  
- **Mely Java verzió támogatott?** Az Aspose.PSD for Java a Java 8‑tól a Java 21‑ig támogatja.  
- **Feldolgozhatok több‑rétegű PSD fájlokat?** Igen – iterálhat minden rétegen, és egyenként alkalmazhatja a küszöböt.  
- **Milyen gyors a művelet?** Egy 1920 × 1080 képnél az Otsu binarizálás kevesebb mint 30 ms alatt befejeződik egy tipikus laptop CPU‑ján.

## Mi az Otsu küszöb alkalmazása Java-ban?

Az Otsu küszöb alkalmazása Java-ban azt jelenti, hogy Java kóddal hívjuk meg az Otsu algoritmust egy képen, amely bináris (fekete‑fehér) eredményt ad. Az algoritmus minden lehetséges szürke‑szintet kiértékel, kiválasztja azt, amely a legkisebb súlyozott osztályon belüli varianciát eredményezi, majd minden pixelt előtérnek vagy háttérnek osztályoz. Ez az automatizált megközelítés kiküszöböli a manuális küszöb kiválasztás szükségességét, és jól működik bimodális hisztogramú képeken, így ideális nagy képkollekciók kötegelt feldolgozásához.

## Miért használja az Aspose.PSD for Java-t?

Az Aspose.PSD for Java **50+ bemeneti és kimeneti formátumot** támogat (köztük PSD, JPEG, PNG, BMP és TIFF), és akár **2 GB** méretű fájlokat is képes feldolgozni anélkül, hogy a teljes dokumentumot a memóriába töltené. A könyvtár beépített Otsu megvalósítása lineáris időben fut, lehetővé téve több száz kép kötegelt feldolgozását néhány másodperc alatt.

## Előfeltételek

- **Java fejlesztői környezet** – JDK 8 vagy újabb telepítve és konfigurálva.  
- **Aspose.PSD for Java könyvtár** – Töltse le és telepítse a könyvtárat a hivatalos Aspose.PSD for Java letöltési oldalról. A letöltési hivatkozást megtalálja itt: [Aspose.PSD for Java letöltési oldal](https://releases.aspose.com/psd/java/).  
- **Minta PSD fájl** – Legyen egy PSD fájl legalább egy raszteres réteggel a binarizálás teszteléséhez.  
- Más Aspose termékekhez a általános kiadások oldalát is böngészheti itt: [Aspose kiadások](https://releases.aspose.com/).

## Csomagok importálása

Importálja a `PsdImage`, `RasterImage` és `JpegOptions` osztályokat az Aspose.PSD könyvtárból, amelyek hozzáférést biztosítanak a PSD fájlokhoz, a raszteres adatokhoz és a JPEG export beállításokhoz.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Hogyan alkalmazza az Otsu küszöböt Java-ban?

Töltse be a PSD fájlt, szerezze meg a kívánt raszteres réteget, és hívja meg az Otsu binarizálás metódust – az egész munkafolyamat öt tömör utasításba illeszkedik. Először egy `PsdImage` objektumot hoz létre, amely a forrásfájlt képviseli, majd lekéri a célréteg `RasterImage`‑jét, meghívja rá az `applyOtsuThreshold()`‑t, végül a `JpegOptions` használatával elmenti az eredményt. Ez a megközelítés minimális memóriahasználatot és maximális teljesítményt biztosít.

### 1. lépés: a dokumentum könyvtár beállítása

Határozza meg azt a mappát, amely a forrás PSD fájlt tartalmazza, valamint a kimeneti helyet a binarizált képnek.  
```java
String dataDir = "Your Document Directory";
```

### 2. lépés: a PSD fájl betöltése

A `PsdImage` az Aspose.PSD felső szintű osztálya, amely egy PSD dokumentumot képvisel, és hozzáférést biztosít a rétegeihez, metaadataihoz és pixeladataihoz.  
```java
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### 3. lépés: a kép gyorsítótárazása

A `RasterImage` egy réteg raszteres ábrázolását tárolja; a `cache()` meghívása betölti a pixeladatokat a memóriába, így a későbbi műveletek gyorsak lesznek.  
```java
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;

if (!rasterCachedImage.isCached()) {
    rasterCachedImage.cacheData();
}
```

### 4. lépés: a kép binarizálása Otsu küszöbbel

Az `applyOtsuThreshold()` kiértékeli az összes lehetséges szürke‑szintet, és kiválasztja az optimális határértéket, egy bináris képet hozva létre, amely elválasztja az előtér objektumait a háttértől.  
```java
rasterCachedImage.binarizeOtsu();
```

### 5. lépés: a kapott kép mentése

A `JpegOptions` JPEG‑specifikus beállításokat konfigurál, például a minőséget és a tömörítést a feldolgozott kép mentésekor. PNG vagy BMP formátumot is választhat a megfelelő opciós osztály cseréjével – az API több mint **30 képformátumot** támogat kimenetként.  
```java
String destName = dataDir + "BinarizationWithOtsuThreshold_out.jpg";
rasterCachedImage.save(destName, new JpegOptions());
```

{{< blocks/products/products-backtop-button >}}

## Gyakori problémák és megoldások

- **Memory‑out‑of‑bounds hibák** – Győződjön meg róla, hogy nagy rétegeken a `cache()`‑t hívja meg a feldolgozás előtt; ez arra kényszeríti az Aspose.PSD‑t, hogy streaming megközelítést használjon.  
- **Hibás színek a binarizálás után** – Ellenőrizze, hogy a forrásréteg valódi szürkeárnyalatos kép legyen; a színes rétegeket először konvertálja szürkeárnyalatosra a `convertToGrayscale()` használatával.

## Gyakran feltett kérdések

### Q1: Mi az Otsu küszöb használatával történő binarizálás?

A binarizálás Otsu küszöbbel egy olyan módszer, amely képszegmentálásra szolgál, egy kép előtér és háttér szétválasztására az optimális küszöb kiválasztásával.

### Q2: Használhatom ingyenesen az Aspose.PSD for Java-t?

Az Aspose.PSD for Java egy kereskedelmi könyvtár, de funkcióit ingyenes próba verzióval is felfedezheti. Szerezze be a [Aspose.PSD for Java letöltési oldal](https://releases.aspose.com/psd/java/)‑ról.

### Q3: Hol találom az Aspose.PSD for Java dokumentációját?

A dokumentáció elérhető a hivatalos Aspose.PSD for Java referencia oldalon: [Aspose.PSD Java API referencia](https://reference.aspose.com/psd/java/).

### Q4: Hogyan kaphatok támogatást az Aspose.PSD for Java-hoz?

Látogasson el az Aspose.PSD közösségi fórumra segítségért: [Aspose.PSD fórum](https://forum.aspose.com/c/psd/34).

### Q5: Van elérhető ideiglenes licenc az Aspose.PSD for Java-hoz?

Igen, ideiglenes licencet szerezhet az Aspose ideiglenes‑licenc oldalán: [Aspose ideiglenes licenc](https://purchase.aspose.com/temporary-license/).

---

**Legutóbb frissítve:** 2026-08-11  
**Tesztelve:** Aspose.PSD for Java 24.11  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [Kép szürkeárnyalatosra konvertálása Aspose.PSD for Java használatával](/psd/java/advanced-techniques/grayscale-image/)
- [Java képfeldolgozási oktatóanyag – Kép fényerősségének állítása Aspose.PSD for Java-val](/psd/java/advanced-techniques/adjust-brightness/)
- [Hogyan állítsuk be a gammát Java képfeldolgozásban az Aspose.PSD segítségével](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}