---
date: 2025-12-02
description: Tanulja meg, hogyan rajzolhat képet a vászonra, és helyezzen el egy aláírást
  Java-ban az Aspose.PSD használatával. Kövesse ezt a lépésről‑lépésre szóló Java
  képfeldolgozási útmutatót, és mentse az eredményt PNG formátumban.
language: hu
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: Kép rajzolása a vásznon – Aláírás hozzáadása az Aspose.PSD for Java-val
url: /java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kép rajzolása a vászonra – Aláírás hozzáadása az Aspose.PSD for Java-val

## Bevezetés

Kézzel írt vagy digitális aláírás hozzáadása egy képhez gyakori követelmény szerződések, számlák vagy bármely olyan dokumentum esetén, amely hitelességi bizonyítékot igényel. Az **Aspose.PSD for Java** segítségével **draw image on canvas** műveletet végezhet, és az aláírást egyszerűen egy további átfedő rétegként kezelheti. Ebben a **java image processing tutorial**-ban végigvezetjük a teljes munkafolyamatot – a kiinduló kép és az aláírásfájl betöltésétől a grafika inicializálásán, az átfedés rajzolásán át egészen a **save image png java**‑stílusú mentésig.

## Gyors válaszok
- **Mi jelent a “draw image on canvas”?** Ez azt jelenti, hogy egy képet egy másikra renderelünk a `Graphics` osztály használatával.  
- **Hogyan adhatunk hozzá aláírást Java-ban?** Töltsük be az aláírásfájlt `Image`-ként, és használjuk a `Graphics.drawImage`.  
- **Melyik Aspose.PSD verzió szükséges?** Bármely friss 24.x kiadás; a kód a legújabb könyvtárral is működik.  
- **Átfedhetek több képet?** Igen – ismételje a `drawImage` hívást különböző forrásokkal.  
- **Szükség van licencre?** A próbaverzió fejlesztéshez működik; a termeléshez kereskedelmi licenc szükséges.

## Mi az a “Draw Image on Canvas”?
Az Aspose.PSD terminológiájában a kép vászonra rajzolása azt jelenti, hogy egy `Image` objektumot egy másikra festünk egy `Graphics` kontextus használatával. Ez a művelet a **overlay images java** technikák gerince, például vízjelek, logók vagy aláírások hozzáadásához.

## Miért használjuk az Aspose.PSD-t aláírás átfedésére?
- **Teljes PSD támogatás** – működik rétegekkel, maszkokkal és átlátszósággal.  
- **Nincs natív OS függőség** – tiszta Java, tökéletes szerver‑oldali feldolgozáshoz.  
- **Nagy teljesítményű renderelés** – optimalizált nagy fájlok és összetett kompozíciók számára.  

## Előfeltételek
- Java Development Kit (JDK) 8 vagy újabb.  
- Az Aspose.PSD for Java JAR hozzáadva a projekt classpath‑jához.  
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

> **Pro tipp:** Tartsa mindkét képet ugyanabban a színmódban (RGB), hogy elkerülje a váratlan színeltolódásokat rajzoláskor.

## 2. lépés: Grafika inicializálása (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

A `Graphics` objektum olyan, mint egy festőecset, amely lehetővé teszi a **draw image on canvas** műveletet. Az elsődleges `Image`‑vel való inicializálása minden további rajzolási parancsot ehhez a vászonhoz köt.

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

Ebben a kódrészletben **overlay images java** technikát alkalmazunk, az aláírást a jobb alsó sarokba helyezve. Ha más elhelyezésre van szükség, állítsa be a `Point` értékeket.

## Gyakori problémák és megoldások
| Tünet | Ok | Megoldás |
|---------|-------|-----|
| Az aláírás torzítva jelenik meg | Eltérő DPI a vászon és az aláírás között | `signature.resize` használata rajzolás előtt, vagy biztosítsa, hogy mindkét fájl ugyanazzal a DPI‑val rendelkezzen. |
| A kimeneti fájl hatalmas | Mentés tömörítés nélkül | Adjon meg egy konfigurált `PngOptions` objektumot, amelynek a `CompressionLevel` értéke magasabb. |
| Semmi sem jelenik meg | A Graphics nincs felszabadítva | Hívja meg a `graphics.dispose()`‑t a rajzolás után (opcionális, de jó gyakorlat). |

## Következtetés

Ezeknek a lépéseknek a követésével megtanulta, hogyan **draw image on canvas**, és zökkenőmentesen **add a signature** az Aspose.PSD for Java segítségével. Ez a technika kiterjeszthető vízjelekre, logókra vagy bármilyen átfedő grafikára, így Java alkalmazásai erőteljes **java image processing** képességekkel rendelkeznek.

## Gyakran ismételt kérdések

### Q1: Hozzáadhatok több aláírást egy képhez?

A1: Igen, több aláírást is hozzáadhat, ha a lépéseket különböző aláírásképekkel ismétli.

### Q2: Támogatja az Aspose.PSD más képformátumokat is?

A2: Igen, az Aspose.PSD számos képformátumot támogat, biztosítva a rugalmasságot a képfeldolgozásban.

### Q3: Szükséges licenc az Aspose.PSD for Java használatához?

A3: Igen, érvényes licenc szükséges az Aspose.PSD használatához. A licenc részleteiért látogasson el a [Purchase Aspose.PSD](https://purchase.aspose.com/buy) oldalra.

### Q4: Hogyan kaphatok támogatást az Aspose.PSD-hez?

A4: Látogasson el az [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) oldalra a közösségi támogatás és megbeszélések érdekében.

### Q5: Kipróbálhatom az Aspose.PSD for Java-t vásárlás előtt?

A5: Igen, a [free trial](https://releases.aspose.com/) segítségével kipróbálhatja a funkciókat vásárlás előtt.

## További gyakran ismételt kérdések

**Q: Hogyan változtathatom meg az aláírás átlátszóságát?**  
A: Használja a `graphics.setOpacity(float opacity)`‑t a `drawImage` hívása előtt. Az értékek 0.0 (átlátszó) és 1.0 (átlátszatlan) között vannak.

**Q: Lehet-e elforgatni az aláírást?**  
A: Igen – alkalmazzon transzformációs mátrixot a `graphics.rotateTransform(angle)` segítségével a rajzolás előtt.

**Q: Rajzolhatom az aláírást JPEG-re PNG helyett?**  
A: Természetesen. Cserélje le a `PngOptions`‑t `JpegOptions`‑ra, és adja meg a kívánt minőségi szintet.

**Legutóbb frissítve:** 2025-12-02  
**Tesztelve ezzel:** Aspose.PSD for Java 24.11  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}