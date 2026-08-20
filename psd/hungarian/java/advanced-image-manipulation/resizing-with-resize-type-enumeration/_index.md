---
date: 2026-06-03
description: Ismerje meg, hogyan méretezzen képet az Aspose.PSD for Java segítségével.
  Ez a lépésről‑lépésre útmutató bemutatja a Resize Type Enumeration-t, a magas minőségű
  képméretezést, valamint a PSD JPEG‑re konvertálását.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Átméretezés a Resize Type Enumeration használatával
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Hogyan méretezzen képet Java-ban a Resize Type Enumeration használatával
url: /hu/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan méretezzen át képet Java-ban a Resize Type enumeráció használatával

## Bevezetés

Ha hatékonyan szeretnél **how to resize image** fájlokat átméretezni egy Java projektben, az Aspose.PSD for Java tiszta, nagy teljesítményű API-t biztosít. Ebben az útmutatóban végigvezetünk a PSD betöltésén, a **Resize Type Enumeration** alkalmazásán a magas minőségű képméretezéshez, és végül a **convert PSD to JPEG** műveleten. Akár asztali szerkesztőt, akár automatizált szerveroldali folyamatot építesz, ezek a lépések lehetővé teszik a méretek, a minőség és a formátum vezérlését néhány kódsorral.

## Gyors válaszok
- **Melyik könyvtár kezeli a resize image java?** Aspose.PSD for Java.
- **Melyik resize type adja a legjobb minőséget?** `ResizeType.LanczosResample`.
- **Átkonvertálhatom a PSD-t JPEG-re átméretezés után?** Igen – egyszerűen mentse a `JpegOptions` használatával.
- **Szükségem van licencre a termeléshez?** Érvényes Aspose.PSD licenc szükséges a termelési használathoz.
- **Alkalmas ez a megközelítés nagy kötegekhez?** Teljesen; az API több száz oldalas fájlokat dolgoz fel anélkül, hogy az egész dokumentumot a memóriába töltené.

## Mi az a "how to resize image" Java-ban?

**How to resize image** arra utal, hogy programozottan módosítjuk egy kép pixelméreteit a vizuális hűség megőrzése mellett. Az Aspose.PSD `Resize` metódusa a `ResizeType` enumerációval együtt pontos irányítást biztosít a skálázási algoritmusok felett, lehetővé téve a fejlesztőknek a minőség fenntartását a különféle forrásfájlok és célméretek széles skáláján.

## Miért használjuk a Resize Type enumerációt?

`ResizeType` lehetővé teszi a resampling algoritmus kiválasztását, amely a legjobban egyensúlyozza a sebességet és a vizuális minőséget. A legtöbb esetben a **LanczosResample** éles eredményeket nyújt mérsékelt teljesítményköltséggel, egy 2000 × 1500 képet 120 ms alatt dolgoz fel egy tipikus szerver‑osztályú CPU-n, miközben a részletek épségét megőrzi.

## Előfeltételek

Mielőtt elkezdené, győződjön meg róla, hogy rendelkezik:

1. **Java Development Environment** – JDK 8 vagy újabb telepítve és konfigurálva.  
2. **Aspose.PSD Library** – Töltse le a legújabb JAR-t a [website](https://releases.aspose.com/psd/java/) oldalról.  
3. **Sample PSD File** – Használja a [sample.psd](Your Document Directory/sample.psd) fájlt, amely az SDK-val együtt kerül a gyakorlati teszteléshez.

## Csomagok importálása

`Image` az alap osztály minden kép típushoz az Aspose.PSD-ben. Adja hozzá a szükséges importokat a Java forrásfájljához:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 1. lépés: Kép betöltése

### Definíció horgony
`RasterImage` osztály az Aspose.PSD alap objektuma, amely egy raster‑alapú képet képvisel, amely PSD fájlból lett betöltve.

Töltse be a PSD-t egy `RasterImage` példányba, hogy manipulálhassa a pixeleket:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## 2. lépés: Kép átméretezése

`image.resize(width, height, resizeType)` átméretezi a képet a megadott méretekre a kiválasztott algoritmus használatával.

Most méretezze át a betöltött képet a **Resize Type Enumeration** használatával. Ebben a példában a Lanczos Resample módszert használjuk, amely ideális, amikor **how to resize image** magas minőségben:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## 3. lépés: Átméretezett kép mentése

`image.save(path, options)` a megadott opciók által definiált formátumban írja a képet a lemezre.

Átméretezés után mentse a képet a megadott méretekkel és a kiválasztott resize típussal. Itt bemutatjuk a **convert psd to jpeg** műveletet is, a végeredményt JPEG fájlként mentve:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## Miért használjuk a Resize Type enumerációt?

`ResizeType` finomhangolt irányítást biztosít a resampling algoritmus felett, lehetővé téve a sebesség és a minőség egyensúlyozását. A legtöbb alkalmazásnál a `LanczosResample` nagyszerű kompromisszumot kínál, éles eredményeket nyújtva nagy teljesítménybeli büntetés nélkül, és jól működik különféle kép tartalmak esetén.

## Gyakori problémák és megoldások

- **Image appears blurry after resize** – Próbáljon ki egy másik `ResizeType`-ot, például `Bicubic` vagy `NearestNeighbour`, hogy megtudja, melyik adja a legjobb vizuális eredményt az adott képre.  
- **OutOfMemoryError on large PSD files** – Dolgozza fel a képet kisebb darabokban, vagy növelje a JVM heap méretét (`-Xmx` flag). Az Aspose.PSD képes **2 GB**-ig terjedő fájlok kezelésére anélkül, hogy az egész dokumentumot a memóriába töltené.

## GyIK

### Q1: Alkalmas-e az Aspose.PSD for Java kis és nagy léptékű projektekhez egyaránt?
A1: Teljesen! Az Aspose.PSD for Java úgy lett tervezve, hogy minden méretű projektet kiszolgáljon, skálázhatóságot és hatékonyságot biztosítva.

### Q2: Használhatok másik resize típust a Lanczos Resample helyett?
A2: Igen, az Aspose.PSD for Java különféle resize típusokat kínál, például **NearestNeighbour**, **Bicubic**, és mások. Tekintse meg az API dokumentációt a teljes listáért.

### Q3: Hol találok további támogatást az Aspose.PSD for Java-hoz?
A3: Bármilyen kérdés vagy segítség esetén látogassa meg a [Aspose.PSD fórumot](https://forum.aspose.com/c/psd/34).

### Q4: Elérhető ingyenes próba az Aspose.PSD for Java-hoz?
A4: Igen, ingyenes próba verziót érhet el [itt](https://releases.aspose.com/).

### Q5: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD for Java-hoz?
A5: Ideiglenes licenc megszerzéséhez látogassa meg [ezt a linket](https://purchase.aspose.com/temporary-license/).

## Gyakran Ismételt Kérdések

**Q: Hogyan konvertálhatok programozottan egy PSD fájlt JPEG-re átméretezés nélkül?**  
A: Töltse be a PSD-t `Image.load`-dal, majd hívja meg `image.save("output.jpg", new JpegOptions());`.

**Q: Lehetséges az eredeti DPI megtartása átméretezéskor?**  
A: Igen, beállíthatja a `Resolution` tulajdonságot az `Image` objektumon a mentés előtt.

**Q: Láncolhatok több resize műveletet?**  
A: Bár többször is meghívhatja a `resize`-et, hatékonyabb egyszer kiszámolni a végső méreteket és egyszer átméretezni.

---

**Utolsó frissítés:** 2026-06-03  
**Tesztelve:** Aspose.PSD for Java 24.12  
**Szerző:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó útmutatók

- [Egyszerű átméretezés az Aspose.PSD‑vel – Java képmódosító könyvtár](/psd/java/basic-image-operations/simple-resizing/)
- [Magas minőségű képméretezés Bicubic Resamplerrel az Aspose.PSD for Java-ban](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Hogyan konvertáljunk PSD-t PNG-re és méretezzünk arányosan az Aspose.PSD for Java-val](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}