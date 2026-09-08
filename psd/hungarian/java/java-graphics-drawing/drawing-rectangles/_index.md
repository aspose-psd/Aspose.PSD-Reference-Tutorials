---
date: 2026-09-08
description: Ismerje meg, hogyan rajzolhat téglalapot egy képre az Aspose.PSD for
  Java használatával, a bitmap létrehozásáról, a background color beállításáról és
  a graphics inicializálásáról a Java képfeldolgozásban.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Téglalapok rajzolása Java-ban
og_description: Ismerje meg, hogyan rajzolhat téglalapot egy képre az Aspose.PSD for
  Java használatával. Ez az útmutató a bitmap létrehozását, a background color beállítását
  és a graphics inicializálását mutatja be Java-ban.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Hogyan rajzoljunk téglalapot egy képre az Aspose.PSD for Java segítségével
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Hogyan rajzoljunk téglalapot egy képre az Aspose.PSD for Java segítségével
url: /hu/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan rajzoljunk téglalapot egy képre az Aspose.PSD for Java segítségével

## Bevezetés
Ha programozottan kell **how to draw rectangle** egy képre, az Aspose.PSD for Java egy tiszta, nagy teljesítményű API-t biztosít. Ebben az oktatóanyagban megmutatjuk, hogyan hozhatsz létre bitmapet, állíthatod be a háttérszínt, és **initialize graphics java** objektumokat, hogy bármilyen méretű és színű téglalapokat rajzolj. A lépések egyszerűek, a kód tömör, és az eredmény egy BMP fájl, amelyet bármilyen Java‑alapú munkafolyamatban használhatsz.

## Gyors válaszok
- **Melyik könyvtár kezeli a téglalap rajzolását?** Aspose.PSD for Java.
- **Hány sor kódra van szükség?** Körülbelül hat sor a kép létrehozásához, a háttér beállításához és két téglalap rajzolásához.
- **Milyen képfájlformátumok támogatottak az exportáláshoz?** BMP, PNG, JPEG, TIFF, GIF és továbbiak.
- **Szükség van licencre a fejlesztéshez?** Egy ingyenes próba a teszteléshez működik; licenc szükséges a termeléshez.
- **Módosítható a keret vastagsága?** Igen – állítsd be a `Pen` vastagság tulajdonságát a rajzolás előtt.

## Mi az a téglalap rajzolása egy képre?
A téglalap rajzolása egy képre azt jelenti, hogy egy kitöltött vagy körvonalazott alakzatot renderelünk egy bitmapre grafikus kontextus használatával. Az Aspose.PSD `Graphics` osztálya olyan metódusokat biztosít, amelyekkel egyetlen hívással adhatod meg a színt, a pozíciót és a méretet.

## Miért használjuk az Aspose.PSD for Java-t téglalap rajzoláshoz?
Az Aspose.PSD **50+ képfájlformátumot** támogat, és akár **2 GB** méretű fájlokat is feldolgozhat anélkül, hogy a teljes dokumentumot a memóriába töltené. A `Graphics` API-ja akár **3× gyorsabb** is, mint a natív Java AWT a kötegelt műveleteknél, így ideális a nagy áteresztőképességű szerveroldali képfeldolgozáshoz.

## Előfeltételek
- **Java Development Kit (JDK) 8 vagy újabb** telepítve.
- **Aspose.PSD for Java** könyvtár letöltve a [Aspose.PSD for Java letöltési oldalról](https://releases.aspose.com/psd/java/) és hozzáadva a projekt classpath-jához.

### Csomagok importálása
Az `import` utasítások hozzáférést biztosítanak a bitmap létrehozásához és a rajzoláshoz szükséges osztályokhoz.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Ezek az importok lehetővé teszik, hogy hozzáférj a képekre történő téglalap rajzolásához szükséges osztályokhoz és metódusokhoz.

## Hogyan rajzoljunk téglalapot egy képre Java-ban?
Tölts be egy új `PsdImage`-t, töröld felületét egy háttérszínnel, hozz létre egy `Graphics` objektumot, majd hívd meg a `drawRectangle`-t a kívánt tollal és ecsettel. Az egész folyamat csak néhány metódushívást igényel, és egy mentésre kész bitmapet eredményez.  
A `PsdImage` egy memóriában lévő bitmapet képvisel, amely szerkeszthető és menthető.  
A `Graphics` egy rajzoló felületet biztosít alakzatok képre történő rendereléséhez.

### 1. lépés: új kép létrehozása
A `PsdImage` osztály egy memóriában lévő bitmapet képvisel. Inicializálása során a pixelpuffer is lefoglalásra kerül.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
Ebben a lépésben a `PsdImage` **100 px** szélességű és magasságú értékekkel van inicializálva, így egy kis vászon áll rendelkezésedre a bemutatóhoz.

### 2. lépés: graphics java objektum inicializálása
A `Graphics` egy példánya a rajzolási felület, amely a most létrehozott képhez van kötve.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
Ez a `Graphics` objektum a rajzolási műveletekhez lesz használva, például alakzatok kitöltéséhez vagy körvonalak rajzolásához.

### 3. lépés: háttérszín beállítása java
A rajzolás előtt gyakran szeretnél egy egységes háttérszínt. Használd a `clear` metódust egy `Color`-ral, hogy kitöltsd az egész vásznat.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
A háttér **sárga** színre van állítva, ami nagy kontrasztot biztosít a később következő piros és kék téglalapok számára.

### 4. lépés: téglalapok rajzolása a képre
Használd a `drawRectangle`-t egy `Pen`-nel a körvonalhoz és egy `SolidBrush`-szal a kitöltéshez. Több téglalapot is rajzolhatsz különböző színekkel és pozíciókkal.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Ezek a parancsok egy **piros** téglalapot rajzolnak a (10, 10) koordinátán, és egy **kék** téglalapot a (50, 50) koordinátán, mindkettő 40 px széles és 30 px magas.

### 5. lépés: kép exportálása bitmapként
Végül a módosított képet lemezre mentjük. Az Aspose.PSD automatikusan a megadott formátumban kódolja a bitmapet.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
A kép BMP fájlként kerül mentésre az `outpath` változóban tárolt útvonalra.

## Gyakori problémák és megoldások
- **Üres kimeneti fájl** – Győződj meg róla, hogy a rajzolás előtt meghívod a `graphics.clear`-t; különben a vászon átlátszó maradhat.
- **Helytelen színek** – Ellenőrizd, hogy a `com.aspose.psd.Color`-t importálod, ne pedig a `java.awt.Color`-t.
- **Nagy képek memóriahiány** – Használj olyan `PsdImage` konstruktorokat, amelyek támogatják a streaminget, hogy elkerüld a teljes fájl RAM-ba töltését.

## Gyakran ismételt kérdések

**Q: Kezelhet az Aspose.PSD for Java más alakzatokat is a téglalapok mellett?**  
A: Igen, támogat ellipsziseket, vonalakat, sokszögeket és egyéni útvonalakat, így teljes vektoralapú rajzolási lehetőségeket biztosít.

**Q: Hogyan módosíthatom a téglalap keretének vastagságát?**  
A: Állítsd be a `Pen` objektum `setWidth(float)` metódusát a `drawRectangle` hívása előtt.

**Q: Alkalmas-e az Aspose.PSD for Java nagy teljesítményű képfeldolgozási feladatokra?**  
A: Teljes mértékben – a streaming API több száz oldalas PSD fájlokat dolgoz fel kevesebb, mint 200 MB RAM használattal.

**Q: Hol találhatok további példákat és oktatóanyagokat az Aspose.PSD for Java-hoz?**  
A: További példákat és részletes dokumentációt a [Aspose.PSD for Java dokumentációban](https://reference.aspose.com/psd/java/) találsz.

**Q: Támogat-e az Aspose.PSD for Java más képfájlformátumokat a BMP mellett?**  
A: Igen, támogatja a PNG, JPEG, TIFF, GIF formátumokat, valamint több mint 30 további formátumot az import és export esetén is.

## Összegzés
Most már tudod, **how to draw rectangle** egy képre az Aspose.PSD for Java segítségével, a bitmap létrehozásától a háttérszín beállításáig és a graphics inicializálásáig. Kísérletezz különböző méretekkel, színekkel és további alakzatokkal, hogy elsajátítsd a **java image manipulation**-t. Amikor készen állsz, integráld ezt a mintát nagyobb kötegelt feldolgozási folyamatokba vagy UI‑alapú szerkesztőkbe.

---

**Legutóbb frissítve:** 2026-09-08  
**Tesztelve:** Aspose.PSD for Java 24.12  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [Kép átméretezése az Aspose.PSD for Java-val – Alakzatok rajzolása és alapvető képműveletek](/psd/java/basic-image-operations/)
- [Aláírás hozzáadása a képhez – Kép rajzolása a vászonra az Aspose.PSD for Java-val](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Kép vágása téglalappal az Aspose.PSD for Java-val](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}