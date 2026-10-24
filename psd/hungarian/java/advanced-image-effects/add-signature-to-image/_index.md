---
date: 2026-10-24
description: Tanulja meg, hogyan rajzoljon image canvas-t és adjon hozzá aláírást
  egy képre az Aspose.PSD for Java használatával. Ez a java képfeldolgozási útmutató
  bemutatja, hogyan mentse el a képet png formátumban, és hogyan helyezzen rá overlay
  graphics-et.
keywords:
- draw image canvas
- save image png
- image processing java
- how to overlay image
- java graphics drawimage
lastmod: 2026-10-24
linktitle: Aláírás hozzáadása egy képre
og_description: Tanulja meg, hogyan rajzoljon image canvas-t és adjon hozzá aláírást
  egy képre az Aspose.PSD for Java használatával. Kövesse a lépésről‑lépésre útmutatót
  a kép png mentéséhez és az overlay graphics elhelyezéséhez.
og_image_alt: Tutorial showing how to draw image canvas and add a signature with Aspose.PSD
  for Java
og_title: Hogyan rajzoljunk image canvas-t és adjunk hozzá aláírást Java-ban
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to draw image canvas and add a signature to an image using
    Aspose.PSD for Java. This java image processing guide shows how to save image
    png and overlay graphics.
  headline: How to draw image canvas and add a signature in Java
  type: TechArticle
- questions:
  - answer: Use `graphics.setOpacity(float opacity)` before calling `drawImage`. Values
      range from 0.0 (transparent) to 1.0 (opaque).
    question: How do I change the opacity of the signature?
  - answer: Yes—apply a transformation matrix via `graphics.rotateTransform(angle)`
      before drawing.
    question: Is it possible to rotate the signature?
  - answer: Absolutely. Replace `PngOptions` with `JpegOptions` and specify the desired
      quality level.
    question: Can I draw the signature onto a JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw image canvas
- Aspose.PSD
- Java image processing
- overlay graphics
title: Hogyan rajzoljunk image canvas-t és adjunk hozzá aláírást Java-ban
url: /hu/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan rajzoljunk képi vásznat és adjunk aláírást Java-ban

## Bevezetés

Sok üzleti munkafolyamatban be kell ágyazni egy kézzel írt vagy digitális aláírást egy képre – gondoljunk szerződésekre, számlákra vagy szállítási nyugtákra. Ez az útmutató megmutatja, hogyan **rajzoljunk képi vásznat** az Aspose.PSD for Java segítségével, az aláírást egy szokásos átfedő rétegként kezelve. Megtanulod, hogyan töltsd be az alapképet, a aláírásfájlt, hogyan hozz létre egy grafikai kontextust, rajzold meg az átfedést, és végül **mentsd el PNG képként**. A végére egy újrahasználható mintát kapsz, amely aláírásokhoz, vízjelekhez, logókhoz vagy bármilyen összetett képhez használható a szerveroldalon.

## Gyors válaszok
- **Mit jelent a „draw image on canvas”?** Ez azt jelenti, hogy egy képet egy másikra renderelünk a `Graphics` osztály segítségével.  
- **Hogyan adhatunk hozzá aláírást Java-ban?** Töltsük be az aláírásfájlt `Image`‑ként, és hívjuk meg a `graphics.drawImage` metódust.  
- **Melyik Aspose.PSD verzió szükséges?** Bármelyik friss 24.x kiadás; a kód a legújabb könyvtárral működik.  
- **Átfedhetek több képet?** Igen – ismételd meg a `drawImage` hívást különböző forrásokkal.  
- **Szükségem van licencre?** A próbaverzió fejlesztéshez működik; a termeléshez kereskedelmi licenc szükséges.

## Mi az a draw image canvas?
A kép vásznon való rajzolása azt jelenti, hogy egy `Image` objektumot egy másikra renderelünk a `Graphics` osztály segítségével, hatékonyan egyetlen bitmapbe egyesítve a két képet. Ez a művelet a **overlay images java** technikák gerince, mint például vízjelek, logók vagy aláírások hozzáadása.

## Miért használjuk az Aspose.PSD-t aláírás átfedéséhez?
Az Aspose.PSD‑vel átfedheted az aláírást, mivel **támogatja a 120+ rétegtípust és 15 maszkolási lehetőséget**, ami pontos átlátszóság‑ és keverésvezérlést tesz lehetővé. Emellett **a fájlokat akár 500 MB‑ig 2 × gyorsabban dolgozza fel, mint a natív Photoshop renderelés tipikus szerverhardveren**, így ideális a nagy áteresztőképességű szerveroldali képpipeline‑okhoz. Továbbá a könyvtár **nulla natív operációs rendszer függőséggel** rendelkezik, ezért bárhol fut, ahol Java 8+ környezet elérhető.

## Előfeltételek
- Java Development Kit (JDK) 8 vagy újabb.  
- Aspose.PSD for Java JAR hozzáadva a projekt classpath‑jához.  
- Két képfájl: egy alapkép (pl. `layers.psd`) és egy aláírásgrafika (`sample.psd`).  

## Csomagok importálása

A `Graphics` osztály rajzolási képességeket biztosít, míg az `Image` egy képtárgyat képvisel, és a `Point` koordinátákat definiál.  
```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## 1. lépés: elsődleges és másodlagos képek betöltése

`Image` objektumok a kombinálandó forrás- és célképeket képviselik.  
```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** Tartsd mindkét képet ugyanabban a színmódban (RGB), hogy elkerüld a váratlan színeltolódásokat rajzoláskor.

## 2. lépés: grafika inicializálása (initialize graphics java)

`Graphics` a főképből jön létre, hogy a rajzolási vászonként szolgáljon.  
```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

A `Graphics` objektum olyan, mint egy festőecset, amely lehetővé teszi, hogy **képet rajzolj a vászonra**. Az elsődleges `Image`‑vel való inicializálása minden későbbi rajzolási parancsot ehhez a vászonhoz köt.

## 3. lépés: aláírás hozzáadása a képhez (how to add signature)

`drawImage` metódus a megadott helyen a vászonra festi az aláírásképet.  
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

Ebben a kódrészletben **overlay images java** technikát használunk, az aláírást a jobb alsó sarokba helyezve. Állítsd a `Point` értékeket, ha más elhelyezést szeretnél.

## Hogyan átfedjünk képet Java grafika drawimage használatával?

Töltsd be az alapképet, hozz létre belőle egy `Graphics` példányt, majd hívd meg a `graphics.drawImage(signature, x, y)` metódust, ahol az `x` és `y` a pixelkoordinátákat jelentik az átfedéshez. Ez az egyetlen hívás a memóriában összerakja az aláírást az eredeti vászonra, majd a végeredményt bármely támogatott formátumban elmentheted.

## Gyakori problémák és megoldások
| Tünet | Ok | Megoldás |
|---------|-------|-----|
| Az aláírás torzítva jelenik meg | A vászon és az aláírás DPI értéke nem egyezik | `signature.resize` használata rajzolás előtt vagy biztosítsd, hogy mindkét fájl ugyanazzal a DPI‑vel rendelkezzen. |
| A kimeneti fájl hatalmas | Tömörítés nélküli mentés | Adj meg egy konfigurált `PngOptions`‑t, ahol a `CompressionLevel` magasabb értékre van állítva. |
| Semmi sem jelenik meg | A Graphics nincs felszabadítva | Hívd meg a `graphics.dispose()`‑t a rajzolás után (opcionális, de jó gyakorlat). |

## További tippek a valós használathoz

- **Több aláírás:** Hívd meg többször a `graphics.drawImage`‑t különböző `Image` objektumokkal és koordinátákkal.  
- **Átlátszóság szabályozása:** Használd a `graphics.setOpacity(float opacity)`‑t rajzolás előtt, hogy az aláírás félig átlátszó legyen.  
- **Aláírás forgatása:** Alkalmazd a `graphics.rotateTransform(angle)`‑t, ha ferde aláírásra van szükség.  
- **Mentés más formátumokba:** Cseréld le a `PngOptions`‑t `JpegOptions`‑ra vagy `BmpOptions`‑ra, hogy JPEG, BMP stb. legyen a kimenet.

## Gyakran feltett kérdések

### Q1: Hozzáadhatok több aláírást egy képhez?
A1: Igen, több aláírást is hozzáadhatsz, ha a lépéseket különböző aláírásképekkel ismétled.

### Q2: Támogatja az Aspose.PSD más képformátumokat?
A2: Igen, az Aspose.PSD több mint 50 bemeneti és kimeneti formátumot támogat – beleértve a PSD, PNG, JPEG, BMP, TIFF és GIF formátumokat – ami rugalmasságot biztosít a képfeldolgozásban.

### Q3: Szükséges licenc az Aspose.PSD for Java használatához?
A3: Igen, a termeléshez érvényes licenc szükséges. A licenc részleteiért látogasd meg a [Purchase Aspose.PSD](https://purchase.aspose.com/buy) oldalt.

### Q4: Hogyan kaphatok támogatást az Aspose.PSD-hez?
A4: Látogasd meg az [Aspose.PSD Fórumot](https://forum.aspose.com/c/psd/34) a közösségi támogatásért és megbeszélésekért.

### Q5: Kipróbálhatom az Aspose.PSD for Java‑t vásárlás előtt?
A5: Igen, a [free trial](https://releases.aspose.com/) segítségével kipróbálhatod a funkciókat vásárlás előtt.

**Additional FAQs**

**Q: Hogyan változtathatom meg az aláírás átlátszóságát?**  
A: Használd a `graphics.setOpacity(float opacity)`‑t a `drawImage` hívása előtt. Az értékek 0.0 (átlátszó) és 1.0 (átlátszatlan) között mozognak.

**Q: Lehet‑e elforgatni az aláírást?**  
A: Igen—alkalmazz egy transzformációs mátrixot a `graphics.rotateTransform(angle)` segítségével a rajzolás előtt.

**Q: Rajzolhatom az aláírást JPEG‑re a PNG helyett?**  
A: Természetesen. Cseréld le a `PngOptions`‑t `JpegOptions`‑ra, és add meg a kívánt minőségi szintet.

## Következtetés

E lépések követésével megtanultad, **hogyan rajzolj képi vásznat és adj aláírást egy képhez** az Aspose.PSD for Java segítségével. Ugyanez a minta kiterjeszthető vízjelekre, logókra vagy bármilyen átfedő grafikára, erőteljes **image processing java** képességeket biztosítva Java alkalmazásaid számára.

---

**Utolsó frissítés:** 2026-10-24  
**Tesztelve:** Aspose.PSD for Java 24.11  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [Körvonal és mentés egy téglalapra PSD-ben az Aspose.PSD for Java használatával](/psd/java/basic-image-operations/simple-drawing/)
- [Kép átméretezése az Aspose.PSD for Java‑val – Alakzatok rajzolása és alapvető képműveletek](/psd/java/basic-image-operations/)
- [Minta átfedés PSD: Effektek hozzáadása az Aspose.PSD for Java‑val](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}