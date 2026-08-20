---
date: 2026-04-28
description: Tanulja meg, hogyan adhat aláírást egy képhez, egy képet rajzolva a vászonra
  az Aspose.PSD for Java segítségével. Ez a Java képfeldolgozási útmutató bemutatja,
  hogyan menthet képet PNG formátumban, és hogyan helyezhet rá grafikai elemeket.
keywords:
- add signature to image
- draw image on canvas
- save image as png
- java image processing
- add watermark java
linktitle: Aláírás hozzáadása egy képhez
second_title: Aspose.PSD Java API
title: Aláírás hozzáadása a képhez – Kép rajzolása vászonra az Aspose.PSD for Java-val
url: /hu/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aláírás hozzáadása a képhez – Kép rajzolása vászonra az Aspose.PSD for Java segítségével

## Bevezetés

Kézzel írt vagy digitális **add signature to image** hozzáadása gyakori követelmény szerződések, számlák vagy bármely hitelességet igénylő dokumentum esetén. Ebben az útmutatóban megmutatjuk, hogyan teszi lehetővé az Aspose.PSD for Java a **draw image on canvas** funkciót, és kezeli az aláírást, mint egy további átfedő réteget. Lépésről lépésre bemutatjuk az alapkép betöltését, az aláírásfájl betöltését, egy grafikus kontextus inicializálását, az átfedés rajzolását, és végül a **save image as PNG** műveletet. A végére egy újrahasználható mintát kap, amely bármely **java image processing** szituációra alkalmazható, legyen az aláírás, vízjel vagy logó.

## Gyors válaszok
- **What does “draw image on canvas” mean?** Ez azt jelenti, hogy egy képet egy másikra renderelünk a `Graphics` osztály segítségével.  
- **How to add a signature in Java?** Az aláírásfájlt `Image`‑ként töltse be, és használja a `Graphics.drawImage`‑t.  
- **Which Aspose.PSD version is required?** Bármely friss 24.x kiadás; a kód a legújabb könyvtárral működik.  
- **Can I overlay multiple images?** Igen—ismételje a `drawImage` hívást különböző forrásokkal.  
- **Do I need a license?** A próbaverzió fejlesztéshez működik; a termeléshez kereskedelmi licenc szükséges.

## Mi az a “Draw Image on Canvas”?
Az Aspose.PSD terminológiájában a kép vászonra rajzolása azt jelenti, hogy egy `Image` objektumot egy másikra festünk egy `Graphics` kontextus használatával. Ez a művelet a **overlay images java** technikák gerince, például vízjelek, logók vagy aláírások hozzáadásához.

## Miért használja az Aspose.PSD-t aláírás átfedésére?
- **Full PSD support** – rétegekkel, maszkokkal és átlátszósággal működik.  
- **No native OS dependencies** – tiszta Java, tökéletes szerveroldali feldolgozáshoz.  
- **High‑performance rendering** – nagy fájlok és összetett kompozíciók számára optimalizált.  

## Előfeltételek
- Java Development Kit (JDK) 8 vagy újabb.  
- Aspose.PSD for Java JAR hozzáadva a projekt classpath‑jához.  
- Két képfájl: egy alapkép (pl. `layers.psd`) és egy aláírásgrafika (`sample.psd`).  

## Csomagok importálása

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## 1. lépés: Elsődleges és másodlagos képek betöltése

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** Tartsa mindkét képet ugyanabban a színmódban (RGB), hogy elkerülje a váratlan színeltolódásokat rajzolás közben.

## 2. lépés: Grafika inicializálása (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

A `Graphics` objektum olyan, mint egy festőecset, amely lehetővé teszi a **draw image on canvas** műveletet. Az elsődleges `Image`‑vel történő inicializálása minden további rajzolási parancsot ehhez a vászonhoz köt.

## 3. lépés: Aláírás hozzáadása a képhez (how to add signature)

```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

Ebben a kódrészletben **overlay images java** technikát alkalmazunk, az aláírást a jobb alsó sarokba helyezve. Ha más elhelyezést szeretne, állítsa be a `Point` értékeket.

## Gyakori problémák és megoldások
| Tünet | Ok | Megoldás |
|---------|-------|-----|
| Aláírás torzult | Nem egyező DPI a vászon és az aláírás között | Használja a `signature.resize`‑et a rajzolás előtt, vagy biztosítsa, hogy mindkét fájl ugyanazt a DPI‑t használja. |
| A kimeneti fájl hatalmas | Tömörítés nélküli mentés | Adjon meg egy konfigurált `PngOptions`‑t, ahol a `CompressionLevel` magasabb értékre van állítva. |
| Semmi sem jelenik meg | A Graphics nincs felszabadítva | Hívja meg a `graphics.dispose()`‑t a rajzolás után (opcionális, de jó gyakorlat). |

## További tippek a gyakorlati használathoz

- **Multiple signatures:** Hívja többször a `graphics.drawImage`‑t különböző `Image` objektumokkal és koordinátákkal.  
- **Opacity control:** A rajzolás előtt használja a `graphics.setOpacity(float opacity)`‑t, hogy az aláírás félig átlátszó legyen.  
- **Rotating the signature:** Alkalmazza a `graphics.rotateTransform(angle)`‑t, ha ferde aláírásra van szükség.  
- **Saving to other formats:** Cserélje le a `PngOptions`‑t `JpegOptions`‑ra vagy `BmpOptions`‑ra, hogy JPEG, BMP stb. formátumban mentse.  

## Gyakran Ismételt Kérdések

### Q1: Hozzáadhatok több aláírást egy képhez?
A1: Igen, több aláírást is hozzáadhat a lépések ismétlésével különböző aláírásképekkel.

### Q2: Támogatja az Aspose.PSD más képformátumokat?
A2: Igen, az Aspose.PSD számos képformátumot támogat, biztosítva a rugalmasságot a képfeldolgozásban.

### Q3: Szükséges licenc az Aspose.PSD for Java használatához?
A3: Igen, szüksége van érvényes licencre az Aspose.PSD használatához. Látogassa meg a [Purchase Aspose.PSD](https://purchase.aspose.com/buy) oldalt a licenc részleteiért.

### Q4: Hogyan kaphatok támogatást az Aspose.PSD-hez?
A4: Látogassa meg az [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) oldalt a közösségi támogatás és megbeszélésekért.

### Q5: Kipróbálhatom az Aspose.PSD for Java-t vásárlás előtt?
A5: Igen, kaphat egy [free trial](https://releases.aspose.com/) verziót, hogy a vásárlás előtt felfedezze a funkciókat.

**További GYIK**

**Q: Hogyan változtathatom meg az aláírás átlátszóságát?**  
A: Használja a `graphics.setOpacity(float opacity)`‑t a `drawImage` hívása előtt. Az értékek 0.0 (átlátszó) és 1.0 (átlátszatlan) között mozognak.

**Q: Lehet-e elforgatni az aláírást?**  
A: Igen—alkalmazzon transzformációs mátrixot a `graphics.rotateTransform(angle)`‑vel a rajzolás előtt.

**Q: Rajzolhatom az aláírást JPEG-re a PNG helyett?**  
A: Természetesen. Cserélje le a `PngOptions`‑t `JpegOptions`‑ra, és adja meg a kívánt minőségi szintet.

## Következtetés

Ezekkel a lépésekkel megtanulta, hogyan **add signature to image** **draw image on canvas** segítségével az Aspose.PSD for Java-val. Ugyanezt a mintát kiterjesztheti vízjelekre, logókra vagy bármilyen átfedő grafikára, így Java alkalmazásai erőteljes **java image processing** képességekkel rendelkeznek.

---

**Last Updated:** 2026-04-28  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}