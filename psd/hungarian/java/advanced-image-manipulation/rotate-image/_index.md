---
date: 2026-05-19
description: Ismerje meg, hogyan konvertálhatja a PSD-t JPEG-re és forgathatja a képet
  270 fokkal az Aspose.PSD for Java használatával. Ez az útmutató bemutatja, hogyan
  lehet PSD fájlokat forgatni, képeket tükrözni, és a PSD-t JPEG-re konvertálni.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: Kép 270° forgatása
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: PSD konvertálása JPEG-re és 270° forgatás az Aspose.PSD for Java segítségével
url: /hu/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD konvertálása JPEG‑re és a kép 270 fokos forgatása az Aspose.PSD for Java segítségével

## Bevezetés

Ebben a **Java képfeldolgozási útmutatóban** megtanulja, hogyan **konvertálja a PSD‑t JPEG‑re**, miközben a képet 270 fokkal forgatja az Aspose.PSD for Java használatával. Akár kötegelt feldolgozási csővezeték, webes szerkesztő vagy asztali segédprogram építésén dolgozik, a könyvtár lehetővé teszi a PSD rétegek manipulálását Photoshop nélkül. Emellett bemutatjuk a választható tükrözést, és megmutatjuk a teljes vég‑től‑vég folyamatot a PSD fájl betöltésétől a JPEG mentéséig.

## Gyors válaszok
- **Melyik könyvtár kezeli a forgatást?** Aspose.PSD for Java  
- **Melyik forgatási szöget használja a példa?** 270 degrees  
- **Tükrözhetem is a képet?** Igen – használja a `RotateFlipType` opciókat, például `Rotate90FlipX`  
- **Hogyan mentem az eredményt?** A példában JPEG‑ként mentjük a `JpegOptions` használatával  
- **Szükségem van licencre a termeléshez?** Érvényes Aspose.PSD licenc szükséges kereskedelmi használathoz  

## Mi az a „kép 270 fokos forgatása”?
A kép 270 fokos forgatása azt jelenti, hogy a képet a teljes kör háromnegyedével forgatjuk az óramutató járásával megegyező irányba (vagy 90 fokkal az óramutató járásával ellentétesen). Ez az orientáció gyakran visszaállítja az eredeti álló formát korábbi átalakítások után, és gyakran használják, amikor a képeket fekvő módban rögzítették, de álló módban kell megjeleníteni őket. Az eredmény egy helyesen tájolású kép minőségromlás nélkül.

## Miért használja az Aspose.PSD‑t ehhez a feladathoz?
Az Aspose.PSD **50+ bemeneti és kimeneti formátumot** támogat — beleértve a PSD, JPEG, PNG, BMP, GIF és TIFF formátumokat — és akár **2 GB** méretű fájlokat is feldolgozhat anélkül, hogy a teljes dokumentumot a memóriába töltené. Az API bármely Java futtatókörnyezetben (JDK 8+) működik, nem igényel natív Photoshop telepítést, és egyetlen `rotateFlip` hívással képes a forgatást és a tükrözést egy lépésben elvégezni.

## Előfeltételek

- **Aspose.PSD for Java** library installed. You can download it and view the full API reference [here](https://reference.aspose.com/psd/java/).  
- Java fejlesztői környezet (JDK 8 vagy újabb).  
- Egy minta PSD fájl, amelyet forgatni szeretne. Frissítse a `sourceFile` változót a kódban a fájl helyes elérési útjára.

## Csomagok importálása

A `Image`, `RotateFlipType` és `JpegOptions` osztályok szükségesek a fájl betöltéséhez, átalakításához és mentéséhez.  
`Image` a PSD dokumentumot a memóriában képviselő alaposztály.  
`RotateFlipType` felsorolja a támogatott forgatási és tükrözési műveleteket.  
`JpegOptions` a JPEG kimeneti beállításokat, például a minőséget konfigurálja.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Hogyan konvertáljuk a PSD‑t JPEG‑re a forgatás után?

Töltse be a forrás PSD‑t, alkalmazza a 270 fokos forgatást, és azonnal mentse JPEG‑ként. Ez a háromlépéses folyamat egy modern CPU‑n tipikus 10 MP képnél kevesebb, mint egy másodperc alatt lefut, így ideális nagy áteresztőképességű kötegelt feladatokhoz. Csak a szükséges képadatokat feldolgozva alacsony marad a memóriahasználat, és a kapott JPEG megőrzi a vizuális hűséget, miközben csökkenti a fájlméretet.

### 1. lépés: PSD fájl betöltése

`Image` az Aspose.PSD alaposztálya, amely egy PSD dokumentumot képvisel a memóriában. Példányosításakor csak a fejlécinformációkat olvassa, így alacsony a memóriahasználat.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### 2. lépés: A kép 270 fokos forgatása

`rotateFlip` végrehajtja a megadott forgatást és opcionális tükrözést a képen. A `RotateFlipType.Rotate270FlipNone` a vásznat 270 fokkal az óramutató járásával megegyező irányban forgatja, miközben a kép orientációja változatlan marad.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** Ha a képet vízszintesen vagy függőlegesen is tükrözni kell, válasszon másik `RotateFlipType`-ot, például `Rotate90FlipX` vagy `Rotate180FlipY`.

### 3. lépés: PSD konvertálása JPEG‑re és mentés

`JpegOptions` a JPEG‑specifikus paramétereket, például a tömörítési minőséget definiálja. A `save` metódus a átalakított képet a kívánt formátumban a lemezre írja.

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

A `RotatedImage_out.jpg` fájl most már a 270 fokkal forgatott eredeti PSD tartalmat tartalmazza, JPEG‑ként mentve.

## Gyakori problémák és megoldások

| Probléma | Megoldás |
|----------|----------|
| **A kép fejjel lefelé jelenik meg** | Ellenőrizze, hogy a `Rotate270FlipNone`-t használta-e. 90 fokos óramutató járásával megegyező forgatáshoz használja a `Rotate90FlipNone`-t. |
| **A kimeneti fájl sérült** | Győződjön meg arról, hogy a célmappa létezik, és van írási jogosultsága. |
| **Licenckivétel** | Telepítsen ideiglenes vagy állandó Aspose.PSD licencet a kép betöltése előtt a termelésben. |

## Gyakran feltett kérdések

**Q: Kompatibilis az Aspose.PSD különböző képformátumokkal?**  
A: Igen, az Aspose.PSD támogatja a PSD, JPEG, PNG, BMP, GIF, TIFF és számos más raszteres formátumot.

**Q: Alkalmazhatok egyedi forgatásokat, nem csak előre definiált tükrözéseket?**  
A: Természetesen! Bár a `RotateFlipType` közös szögeket biztosít, több hívást láncolhat vagy transzformációs mátrixokat használhat tetszőleges szögekhez.

**Q: Hogyan konvertálom a forgatott PSD‑t egy másik formátumba, például PNG‑be?**  
A: Cserélje le a `JpegOptions`-t `PngOptions`-ra (vagy a megfelelő opciós osztályra) a `save` metódusban.

**Q: Hol találok további támogatást vagy segítséget?**  
A: Közösségi segítségért látogassa meg a [Aspose.PSD Fórumot](https://forum.aspose.com/c/psd/34).

**Q: Van ingyenes próba elérhető?**  
A: Igen, az Aspose.PSD-t egy [ingyenes próbaverzióval](https://releases.aspose.com/) fedezheti fel.

**Q: Hogyan szerezhetek ideiglenes licencet?**  
A: Ha ideiglenes licencre van szüksége, azt [itt](https://purchase.aspose.com/temporary-license/) szerezheti meg.

---

**Utolsó frissítés:** 2026-05-19  
**Tesztelve ezzel:** Aspose.PSD for Java 24.12  
**Szerző:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó útmutatók

- [PSD konvertálása raszteres képformátumokra az Aspose.PSD for Java segítségével](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [PSD konvertálása PNG‑re és rétegek forgatása PSD fájlokban Java használatával](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Hogyan forgassuk a képet Java‑ban az Aspose.PSD segítségével](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}