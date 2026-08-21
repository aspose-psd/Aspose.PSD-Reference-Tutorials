---
date: 2026-06-13
description: Tanulja meg, hogyan lehet téglalapot rajzolni PSD fájlokban az Aspose.PSD
  for Java használatával. Ez az útmutató lépésről‑lépésre bemutatja a kódot, rétegek
  hozzáadását, szerveroldali képfeldolgozást és alakzatrajzolást.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: Egyszerű rajzolás végrehajtása
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Hogyan rajzoljunk téglalapot PSD-ben az Aspose.PSD for Java segítségével
url: /hu/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan rajzoljunk téglalapot PSD-ben az Aspose.PSD for Java segítségével

## Bevezetés

Ebben az útmutatóban megtudja, hogyan **rajzoljon téglalap** alakzatokat egy Photoshop PSD fájlban a tisztán Java‑os Aspose.PSD könyvtár segítségével. Akár szerveroldali eszközcsővezeték építésén dolgozik, bélyegkép‑generálást automatizál, vagy dinamikus grafikákat ad hozzá meglévő tervekhez, az alábbi lépések egy teljes, termelésre kész megoldást nyújtanak. Kitérünk egy új PSD dokumentum létrehozására, egy réteg hozzáadására, a háttér törlésére, és végül a piros és kék téglalapok megrajzolására – mindezt anélkül, hogy valaha is elindítaná a Photoshopot.

## Gyors válaszok
- **Mi a fő osztály a PSD fájl létrehozásához?** `PsdImage`
- **Melyik metódus törli egy réteg háttérszínét?** `Graphics.clear(Color)`
- **Hogyan rajzol egy piros téglalapot?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Szükségem van licencre a fejlesztéshez?** A ingyenes próba a teszteléshez megfelelő; a termeléshez licenc szükséges.
- **Manipulálhatok meglévő PSD fájlokat ugyanazzal az API-val?** Igen, az Aspose.PSD teljes PSD szerkesztést támogat.

## Mi a piros téglalap rajzolása egy PSD fájlban?

A piros téglalap rajzolása azt jelenti, hogy a `Graphics` objektumot használva egy téglalap alakzatot renderelünk, amely piros színnel van kitöltve vagy körvonalazva, egy PSD kép adott rétegére. Ez a művelet gyakori a területek kiemelésére, helyőrzők létrehozására vagy egyszerű grafikák programozott hozzáadására.

## Miért használjuk az Aspose.PSD for Java-t PSD fájlok manipulálásához?

Az Aspose.PSD for Java **50+ bemeneti és kimeneti formátumot** támogat, képes több száz oldalas PSD fájlok feldolgozására anélkül, hogy az egész fájlt a memóriába töltené, és bármely, Java 8 vagy újabb verziót támogató platformon fut. A szerveroldali képfeldolgozó motorja megszünteti a Photoshop szükségességét, csökkenti a licencköltségeket, és lehetővé teszi az automatizált munkafolyamatokat, amelyek akár **10 GB** képadatot is kezelnek óránként egy közepes VM-en.

## Előfeltételek

- Java Development Kit (JDK) 8 vagy újabb telepítve a gépén.  
- Aspose.PSD for Java könyvtár. Letöltheti a [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/) oldalról.

## Csomagok importálása

Az `import` utasítások a szükséges osztályokat a láthatóságba hozzák, így dolgozhat PSD képekkel, rétegekkel, színekkel és grafikákkal.

`PsdImage` osztály az Aspose.PSD legfelső szintű objektuma, amely egyetlen PSD fájlt képvisel a memóriában.  
`Graphics` rajzolási primitíveket biztosít, mint például vonalak, téglalapok és ellipszisek.  
`Color` és `Pen` lehetővé teszi a vonal színének és vastagságának megadását.  
`Layer` osztály egy egyedi képréteget képvisel egy PSD dokumentumban.  
`Rectangle` osztály meghatározza a rajzolási műveletekhez használt téglalap terület pozícióját és méretét.  
`SolidBrush` osztály szilárd színnel tölti ki a formákat.

## Mi az első lépés egy PSD dokumentum létrehozásához?

A `PsdImage` példányosításához megadja a vászon szélességét és magasságát pixelben, ami egy üres PSD fájlstruktúrát hoz létre. Az esetleges kezdeti rétegek vagy háttér beállítása után hívja meg a `save` metódust egy fájlúttal, hogy a dokumentumot lemezre írja. Ez előkészíti a képet a későbbi szerkesztési műveletekhez.

## 1. lépés: Új dokumentum létrehozása

Először hozzon létre egy friss PSD dokumentumot a kívánt vászonmérettel. Ez a dokumentum fogja tartalmazni azt a réteget, amelyre rajzolni fogunk.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Hogyan ad hozzá egy új üres réteget egy PSD képhez?

Először hozzon létre egy új `Layer` példányt, amelynek szélessége és magassága megegyezik a szülő `PsdImage` méreteivel. Ezután adja hozzá ezt a réteget a kép `Layers` gyűjteményéhez az `add` metódus segítségével. Miután a réteg része a képnek, szerezze meg a `Graphics` objektumát a rajzolási műveletek végrehajtásához; ez a lépés nélkül a rajzok nem fognak megjelenni.

## 2. lépés: Réteg hozzáadása

Ezután adjon hozzá egy új üres réteget, amely lefedi a kép teljes szélességét és magasságát. A rétegek elengedhetetlenek a rajzolási műveletek elkülönítéséhez.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Mi a célja egy réteg háttérszínének törlésével?

`Graphics.clear` meghívása egy adott `Color` értékkel az egész réteget azzal a színnel tölti ki, hatékonyan visszaállítva az összes pixel adatot. Ez biztosítja, hogy minden korábbi tartalom eltávolításra kerüljön, és a réteg egy ismert háttérrel induljon, ami elkerüli a váratlan átlátszóságot vagy színkeveredést, amikor a PSD később megnyílik vagy szerkesztésre kerül Photoshopban.

## 3. lépés: Alakzatok rajzolása

A `Graphics` osztályt fogjuk használni a réteg pixel adatainak manipulálásához. Az alábbiakban három példa látható, amelyek bemutatják a háttér törlését és a különböző színű téglalapok rajzolását.

### Réteg szín törlése (háttér beállítása sárgára)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### Piros téglalap rajzolása (fő fókusz)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Kék téglalap rajzolása (további példa)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## Hogyan menti a szerkesztett PSD fájlt lemezre?

Használja a `save` metódust a `PsdImage` objektumon, megadva a teljes fájlútvonalat, és opcionálisan a kívánt képformátumot (alapértelmezés szerint PSD). Ez minden réteget, maszkot és rajzolási parancsot egyetlen PSD fájlba ír, amely megfelel a Photoshop specifikációnak, így figyelmeztetés nélkül nyitható meg.

## 4. lépés: Változások mentése

Végül írja a módosított PSD képet lemezre. A fájl tartalmazni fogja az új réteget és a megrajzolt alakzatokat.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Gyakori problémák és megoldások

- **A réteg nem látható a rajzolás után:** Győződjön meg arról, hogy a réteg a képhez **előtt** van hozzáadva, mielőtt a `Graphics` objektumot létrehozná. A rajzfelületnek egy érvényes réteghez kell csatlakoznia.
- **A színek helytelennek tűnnek:** Ellenőrizze, hogy a `Color.getRed()` (vagy `Color.getBlue()`) metódust használja, ahelyett, hogy egy 0‑255 tartományt meghaladó egyedi RGB értéket hozna létre.
- **A fájl nem lett mentve:** Ellenőrizze, hogy az `outputDir` útvonal létezik, és az alkalmazásnak van írási joga. Linuxon előfordulhat, hogy módosítania kell a mappa tulajdonjogát vagy a `Files.createDirectories` metódust kell használni.
- **Teljesítménycsökkenés nagy fájlok esetén:** Használja a `PsdImage` `setLoadOptions` metódusát, hogy csak a szükséges csatornákat töltse be, ezáltal csökkentve a memóriahasználatot a 200 MB-nál nagyobb PSD-k esetén.

## Gyakran feltett kérdések

**Q1: Használhatom az Aspose.PSD for Java-t meglévő PSD fájlok manipulálására?**  
A1: Igen, az Aspose.PSD for Java kiterjedt funkcionalitást biztosít a meglévő PSD fájlok szerkesztéséhez és manipulálásához, beleértve a rétegek átrendezését, maszk beállításokat és vektoros rajzolást.

**Q2: Hol találhatok támogatást az Aspose.PSD for Java-hoz?**  
A2: A [Aspose.PSD for Java Fórum](https://forum.aspose.com/c/psd/34) oldalon találhat közösségi segítséget és hivatalos Aspose válaszokat.

**Q3: Van ingyenes próba verzió az Aspose.PSD for Java-hoz?**  
A3: Igen, a [itt](https://releases.aspose.com/) elérhető ingyenes próba verzióval. A próba minden funkciót tartalmaz, de vízjelet ad a mentett fájlokhoz.

**Q4: Hogyan vásárolhatok licencet az Aspose.PSD for Java-hoz?**  
A4: Licencet a [Aspose.PSD vásárlási oldalról](https://purchase.aspose.com/buy) vásárolhat. A licencelési lehetőségek közé tartozik a örökös, előfizetéses és helyi (site) licenc.

**Q5: Elérhetők ideiglenes licencek az Aspose.PSD for Java-hoz?**  
A5: Igen, ideiglenes licencet szerezhet [innen](https://purchase.aspose.com/temporary-license/).

## További gyakran feltett kérdések

**K: Rajzolhatok más alakzatokat is a téglalapok mellett?**  
A: Igen, a `Graphics` osztály támogatja az ellipszisek, vonalak és egyedi útvonalak (`drawPath` metódus) rajzolását is.

**K: Támogatja az Aspose.PSD a rajzolt alakzatok átlátszóságát?**  
A: Természetesen; a `SolidBrush`-t ARGB színnel használva alfa átlátszóságot adhat hozzá, lehetővé téve a félig átlátszó átfedéseket.

**K: Lehetséges a réteg átlátszóságának szerkesztése?**  
A: Igen, minden `Layer` objektumnak van egy `setOpacity` metódusa, amely 0‑255 közötti értéket fogad, így finomhangolt vezérlést biztosít a réteg átlátszósága felett.

**K: Hogyan tölthetek be egy meglévő PSD fájlt az új létrehozása helyett?**  
A: Használja a `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` kifejezést a rétegek manipulálása előtt. A betöltött kép megtartja az összes eredeti réteget és maszkot.

## Összegzés

Most már elsajátította, **hogyan rajzoljon téglalap** alakzatokat és manipulálja a rétegeket egy PSD fájlban az Aspose.PSD for Java segítségével. Dokumentum létrehozásával, réteg hozzáadásával, a háttér törlésével és a `Graphics` API-val való rajzolással számtalan grafikai feladatot automatizálhat a szerveroldalon. Kísérletezzen különböző tollakkal, ecsetekkel és réteghatásokkal, hogy ezt az alapot teljes körű képgeneráló csővezetékekre bővítse.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó útmutatók

- [How to Draw Shapes Java – Basic Image Operations](/psd/java/basic-image-operations/)
- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [Crop Image by Rectangle in Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**Last Updated:** 2026-06-13  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose