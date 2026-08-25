---
date: 2026-08-01
description: Ismerje meg, hogyan állíthatja be a gamma értéket a Java Image Processing-ben
  az Aspose.PSD segítségével, convert PSD to TIFF, és javítsa a kifakult képeket egy
  tömör útmutatóban.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Gamma beállítása egy képen
og_description: Ismerje meg, hogyan állíthatja be a gamma értéket a Java Image Processing-ben
  az Aspose.PSD használatával – egy gyors, server‑side könyvtár, amely javítja a kifakult
  képeket és converts PSD to TIFF néhány kódsorral.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: hogyan állítsuk be a gamma – Java processing az Aspose.PSD-vel
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Hogyan állítsuk be a gamma értéket a Java Image Processing-ben az Aspose.PSD
  segítségével
url: /hu/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan állítsuk be a gamma értéket a Java képfeldolgozásban az Aspose.PSD segítségével

## Bevezetés

Ha **java image processing**-en dolgozol, a **hogyan állítsuk be a gamma értéket** egy alapvető technika a fényerő és kontraszt javítására részletek elvesztése nélkül. Ebben az útmutatóban bemutatjuk, hogyan használhatod a **Aspose.PSD for Java**-t gamma korrekció alkalmazására egy PSD fájlra, **convert PSD to TIFF**, és elkerülheted a **kimosott kép** problémát. Meg fogod látni, miért gyors, megbízható, és tökéletes a **server‑side image processing** folyamatokhoz.

## Gyors válaszok
- **Mi a gamma korrekció feladata?** Átállítja a luminancia értékeket, hogy a sötét területek világosabbak, a világos területek sötétebbek legyenek, miközben az általános részleteket megőrzi.  
- **Melyik könyvtár kezeli a feldolgozást?** Az Aspose.PSD for Java egy dedikált `adjustGamma` metódust biztosít raszter képekhez.  
- **Átalakíthatom a PSD-t TIFF-re ugyanabban a folyamatban?** Igen – a gamma beállítás után a képet közvetlenül TIFF formátumban mentheted a `TiffOptions` használatával.  
- **Szükségem van licencre a fejlesztéshez?** Az ingyenes próba verzió tesztelésre működik; a kereskedelmi licenc szükséges a termelési használathoz.  
- **Melyik Java verzió támogatott?** Az Aspose.PSD támogatja a Java 8 és újabb verziókat.

## Mi a Java gamma korrekció?

A gamma korrekció megváltoztatja a kódolt pixelértékek és a megjelenített fényerő közötti nemlineáris kapcsolatot. A gamma görbe finomhangolásával **kimosott kép** problémákat orvosolhatsz vagy részleteket emelhetsz ki az árnyékokban anélkül, hogy a csúcsfényerőt túlzottan felfennéznéd. A működés egy hatványfüggvény alkalmazásán alapul minden pixelre, ami felvilágosítja a sötét tónusokat és összenyomja a csúcsfényeket, így természetesebb vizuális megjelenést eredményez.

## Miért használjuk az Aspose.PSD-t gamma korrekcióhoz?

Az Aspose.PSD egy **java image processing library**, amely elrejti a PSD formátum bonyolultságát. Támogatja akár 2 GB-ig terjedő fájlok feldolgozását, több mint 50 különböző képfájltípust kezel, és egy egyszerű `adjustGamma` hívást biztosít, így ideális **java gamma correction** és **convert PSD to TIFF** munkafolyamatokhoz.

## Előfeltételek

1. **Java Development Environment** – Java 8 vagy újabb telepítve.  
2. **Aspose.PSD Library** – Töltsd le és add hozzá a JAR-t a projektedhez. Lásd a hivatalos [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – Egy PSD fájl, amelyet feldolgozni szeretnél (pl. `sample.psd`).  

## Csomagok importálása

Mielőtt elkezdenéd, importáld a szükséges névtereket, amelyek hozzáférést biztosítanak a raszter kezeléshez és a fájlformátum beállításokhoz.

## 1. lépés: Kép betöltése

A `RasterImage` osztály a PSD réteg rasterizált pixeladatait reprezentálja a memóriában. A kép egyszeri betöltése és gyorsítótárazása csökkenti a memóriahasználatot a későbbi módosítások során.

## 2. lépés: Gamma beállítása

Töltsd be a PSD-t a `new RasterImage("sample.psd")` paranccsal, és hívd meg a `rasterImage.adjustGamma(2.0f)`‑t – ez az egyetlen sor 2.0 gamma értéket alkalmaz minden színcsatornára, felvilágosítva az árnyékokat, miközben a csúcsfényeket érintetlenül hagyja. Ha csatorna‑specifikus finomhangolásra van szükség, külön értékeket adhat meg a piros, zöld és kék csatornákhoz.

## 3. lépés: TiffOptions létrehozása

A `TiffOptions` lehetővé teszi a tömörítés, a mintánkénti bitek és egyéb TIFF‑specifikus beállítások vezérlését. 8‑bit mintát (`{8,8,8}`) beállítva a TIFF fájl mérete ésszerű marad, miközben a színpontosságot megőrzi.

## 4. lépés: Az eredménykép mentése

Hívd meg a `rasterImage.save("output.tif", tiffOptions)`‑t a feldolgozott kép lemezre írásához. Mentés után a TIFF-et továbbíthatod lejjebb lévő rendszereknek, például nyomtatási szolgáltatásoknak vagy web API‑knak.

## Gyakori felhasználási esetek

- **Automated graphics pipelines** – Gamma beállítása menet közben a bélyegképek generálása előtt.  
- **Batch conversion tools** – Nagy PSD archívumok konvertálása TIFF-re a fényerő normalizálása közben.  
- **Web services** – Egy végpont kitettsége, amely PSD-t fogad, gamma korrekciót alkalmaz, és TIFF-et ad vissza a kliens számára.

## Gyakori problémák és megoldások

| Probléma | Miért fordul elő | Hogyan javítsuk |
|----------|------------------|-----------------|
| **A kép kimosott** | A gamma érték túl magas (pl. > 2.5) | Csökkentsd a gamma tényezőt 1.8 és 2.2 közötti értékre. |
| **`rasterImage.isCached()` returns false** | A kép még nincs betöltve a memóriába | Hívd meg a `rasterImage.cacheData()`‑t a gamma beállítása előtt. |
| **A TIFF fájl mérete nagy** | A mintánkénti bitek 16‑bitre vannak beállítva | Használj 8‑bit mintát (`{8,8,8}`) a példában látható módon. |

## Gyakran Ismételt Kérdések

**Q: Alkalmazhatok különböző gamma értékeket minden színcsatornára?**  
A: Igen – a `adjustGamma` metódus külön float értékeket fogad a piros, zöld és kék csatornákhoz.

**Q: Lehet több képmódosítást láncolni a mentés előtt?**  
A: Teljesen. Végrehajthatsz átméretezést, vágást vagy színkorrekciókat egymás után ugyanazon `RasterImage` példányon.

**Q: Az Aspose.PSD támogatja a többoldalas PSD fájlokat?**  
A: Igen, minden réteg egyenként hozzáférhető és feldolgozható.

**Q: Milyen formátumokba exportálhatok a TIFF-en kívül?**  
A: Az Aspose.PSD támogatja a PNG, JPEG, BMP és sok más formátumot a megfelelő opció osztályokon keresztül.

**Q: Hogyan kerülhetem el a kimosott képet a gamma korrekció után?**  
A: Kezdj egy mérsékelt gamma értékkel (körülbelül 2.0), és tekintsd meg az eredményt; ha a kép túl világos, csökkentsd a gamma értéket.

## Összegzés

Gratulálunk! Sikeresen megtanultad, **hogyan állítsuk be a gamma értéket** egy **java image processing** munkafolyamatban, átalakítottad a PSD-t TIFF-re, és elkerülted a gyakori hibákat, mint a **kimosott kép**. Ez a minta finomhangolt vezérlést biztosít a fényerő és kontraszt felett, így ideális automatizált grafikai csővezetékekhez, webszolgáltatásokhoz vagy asztali segédprogramokhoz.

---

**Legutóbb frissítve:** 2026-08-01  
**Tesztelve a következővel:** Aspose.PSD 24.11 for Java  
**Szerző:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó útmutatók

- [Java képfeldolgozási útmutató – Kép fényerősségének beállítása az Aspose.PSD for Java segítségével](/psd/java/advanced-techniques/adjust-brightness/)
- [Hogyan konvertáljunk PSD-t TIFF-re és állítsuk be a kontrasztot az Aspose.PSD for Java segítségével](/psd/java/advanced-techniques/adjust-contrast/)
- [PSD konvertálása képpé Java-ban – Állíts be módosító rétegeket az Aspose.PSD segítségével](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```