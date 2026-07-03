---
date: 2026-07-03
description: Tanulja meg, hogyan lehet képet vágni Java-ban az Aspose.PSD for Java
  használatával. Ez a lépésről-lépésre útmutató a kép vágásához bemutatja a PSD fájlok
  betöltését, az eltolási értékek beállítását és az eredmény mentését.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Kép vágása eltolásokkal
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Kép vágása Java-ban eltolásokkal az Aspose.PSD segítségével
url: /hu/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kép levágása Java-ban eltolásokkal az Aspose.PSD segítségével

## Bevezetés

A Java képfeldolgozásban a **crop image java** gyakori követelmény a grafika, bélyegkép vagy UI elemek előkészítéséhez. Az Aspose.PSD for Java egyszerűvé teszi ezt a feladatot egy egyszerű `crop` metódus biztosításával, amely bármely támogatott raszteres formátumon működik. Ebben az útmutatóban megtanulja, hogyan töltsön be egy PSD fájlt, határozza meg a bal‑jobb‑felső‑alsó eltolási értékeket, alkalmazza a vágást, és mentse az eredményt – mindezt anélkül, hogy egyedi pixelmanipulációs kódot kellene írnia.

## Gyors válaszok
- **Melyik könyvtár kezeli a vágást?** Az Aspose.PSD for Java beépített `crop` metódust biztosít.  
- **Szükségem van licencre?** Egy ideiglenes licenc elegendő értékeléshez; a teljes licenc szükséges a termeléshez.  
- **Támogatott formátumok?** Több mint 30 raszteres formátum, többek között PSD, JPEG, PNG, BMP és TIFF.  
- **Maximum fájlméret?** Akár 2 GB-ig terjedő fájlok kezelhetők anélkül, hogy a teljes képet a memóriába töltené.  
- **Hány kódsorra van szükség?** Csak öt logikai lépés – betöltés, gyorsítótárazás, eltolások meghatározása, vágás és mentés.

## Mi az a crop image java?
`crop image java` a bitmap vágásának műveletét jelenti egy Java alkalmazásban. Az Aspose.PSD használatával a műveletet a `crop` metódus hajtja végre, amely minden oldalra eltolási értékeket fogad, és egy új kép példányt ad vissza.

## Miért használja az Aspose.PSD-t képvágáshoz?
Az Aspose.PSD **30+** képformátumot támogat, és képes több száz oldalas PSD fájlok feldolgozására kevesebb, mint 150 MB RAM használatával, köszönhetően a lusta betöltés architektúrájának. A könyvtár garantálja a pixel‑pontos eredményeket, megőrizve a rétegeket, maszkokat és színprofilokat – amit sok általános képkönyvtár nem tud biztosítani.

## Előfeltételek

### Java Fejlesztői Készlet (JDK)

Győződjön meg róla, hogy a legújabb JDK verzió telepítve van a rendszerén. Letöltheti [innen](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD for Java Könyvtár

A kezdéshez meg kell szereznie az Aspose.PSD for Java könyvtárat. Látogasson el a [letöltési oldalra](https://releases.aspose.com/psd/java/), és töltse le a legújabb verziót.

### Integrált Fejlesztői Környezet (IDE)

Válassza kedvenc Java IDE-jét, például az Eclipse-et vagy az IntelliJ-t, a zökkenőmentes kódolási élmény érdekében.

## Hogyan vágjunk le képet Java-ban?

Töltse be a forrásfájlt, határozza meg a pixel eltolásokat minden oldalra, és hívja meg a `crop` metódust – ez a teljes munkafolyamat öt tömör kódsorban megírható. A `crop` művelet egy új képet hoz létre, amely csak a megadott területet tartalmazza, az eredeti fájlt érintetlenül hagyva.

### 1. lépés: Kép betöltése

`Image` az összes kép típus alaposztálya az Aspose.PSD-ben.  
`RasterImage` egy raszteres képet képvisel, és vágási képességeket biztosít.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### 2. lépés: Képadatok gyorsítótárazása

`cacheData()` betölti a képadatokat a memóriába a gyorsabb feldolgozás érdekében.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### 3. lépés: Eltolási értékek meghatározása

Adja meg az eltolási értékeket a kép négy oldalára (bal, felső, jobb, alsó) pixelekben.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### 4. lépés: Vágás alkalmazása

`crop(left, right, top, bottom)` levágja a képet a megadott pixel eltolásokkal minden oldalon.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### 5. lépés: Eredmények mentése

`JpegOptions` meghatározza a JPEG kódolási beállításokat, mint például a minőséget és a színprofilt.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Gratulálunk! Sikeresen levágott egy képet az Aspose.PSD for Java segítségével.

## Gyakori problémák és megoldások

- **A kép változatlan marad:** Ellenőrizze, hogy az eltolási értékek pozitívak és nem haladják meg az eredeti méreteket.  
- **OutOfMemoryError nagy fájlok esetén:** Engedélyezze a gyorsítótárazást a 2. lépésben bemutatott módon; ez arra kényszeríti az Aspose.PSD-t, hogy ideiglenes fájlt használjon a teljes kép RAM-ban tartása helyett.  
- **Színeltolás a vágás után:** Győződjön meg róla, hogy megőrzi a színprofilt a `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` hívással, ha pontos színpontosságra van szükség.

## Gyakran Ismételt Kérdések

**Q: Az Aspose.PSD kompatibilis minden képformátummal?**  
A: Igen, az Aspose.PSD több mint 30 raszteres formátumot támogat, beleértve a PSD, JPEG, PNG, BMP, TIFF és GIF formátumokat, biztosítva a széles körű kompatibilitást.

**Q: Alkalmazhatok több vágási műveletet ugyanarra a képre?**  
A: Természetesen. Minden `crop` hívás után egy új képobjektumot kap, amelyet szükség szerint újra levághat.

**Q: Van közösségi fórum az Aspose.PSD támogatásához?**  
A: Igen, támogatást és közösségi részvételt talál a [Aspose.PSD Fórumon](https://forum.aspose.com/c/psd/34).

**Q: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD-hez?**  
A: Látogasson el [ide](https://purchase.aspose.com/temporary-license/), hogy ideiglenes licencet szerezzen.

**Q: Vannak minta projektek, amelyek bemutatják az Aspose.PSD funkciókat?**  
A: Tekintse meg a dokumentációt és a példákat a [Aspose.PSD Java Dokumentációban](https://reference.aspose.com/psd/java/).

---

**Utoljára frissítve:** 2026-07-03  
**Tesztelve:** Aspose.PSD 24.11 for Java  
**Szerző:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Kapcsolódó útmutatók

- [Kép levágása téglalappal az Aspose.PSD for Java-ban](/psd/java/image-editing/crop-image-by-rectangle/)
- [Kép levágása Java - Képek kiterjesztése és levágása az Aspose.PSD for Java-val](/psd/java/image-editing/expand-and-crop-images/)
- [Kép átméretezése Java - Resize Type enumeráció használata az Aspose.PSD for Java-ban](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}