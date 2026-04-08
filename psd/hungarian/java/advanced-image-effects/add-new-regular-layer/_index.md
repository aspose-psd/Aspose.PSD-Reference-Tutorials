---
date: 2026-04-08
description: Tanulja meg, hogyan exportálja a PSD‑t PNG‑re, és hogyan hozhat létre
  új PSD‑réteget az Aspose.PSD for Java segítségével egy aspose ideiglenes licenc
  használatával. Ez a lépésről‑lépésre útmutató a PSD‑képmódosítást és a réteg pozíciójának
  beállítását tárgyalja.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Új normál réteg hozzáadása a PSD-hez
second_title: Aspose.PSD Java API
title: PSD exportálása PNG formátumba és új normál réteg hozzáadása az Aspose.PSD
  for Java segítségével – aspose ideiglenes licenc
url: /hu/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD exportálása PNG‑be és új szabályos réteg hozzáadása az Aspose.PSD for Java használatával

## Bevezetés

Ebbe a **aspose psd tutorial**-ban megtudja, hogyan **exportálja a PSD‑t PNG‑be**, miközben **új szabályos réteget hoz létre** ugyanabban a fájlban, **aspose ideiglenes licenc** használatával fejlesztéshez. Akár web‑kész bélyegképeket kell generálnia, akár eszközöket készít a tervezési folyamat számára, vagy egyszerűen csak kísérletezni szeretne **psd image manipulation**‑nal, az Aspose.PSD for Java teljes programozási irányítást biztosít. Lépésről lépésre végigvezetünk – a forrásfájl betöltésétől az frissített PSD és egy PNG másolat mentéséig – hogy azonnal elkezdhesse a PSD rétegek manipulálását.

## Gyors válaszok

- **Exportálhatok PSD‑t PNG‑be egy hívással?** Igen, a rétegek hozzáadása után meghívhatja a `save`‑t `PngOptions`‑szel.
- **Szükségem van licencre fejlesztéshez?** Egy ideiglenes licenc teszteléshez működik; a teljes licenc a termeléshez szükséges.
- **Melyik Java verzió támogatott?** Az Aspose.PSD Java 8‑as és újabb verziókkal működik.
- **Pixel‑alapú a rétegpozicionálás?** Igen, a bal, felső, jobb, alsó koordinátákat pixelben állítja be a **set layer position** metódusokkal.
- **A PNG megőrzi a réteg átlátszóságát?** A PNG az összes látható réteg egyesített eredményét tartalmazza.

## Miért használjunk aspose ideiglenes licencet?

Az **aspose temporary license** lehetővé teszi, hogy a teljes Aspose.PSD funkciókészletet korlátozás nélkül értékelje. Eltávolítja a kiértékelési vízjelet, feloldja az összes API‑t – beleértve az **create new psd layer** objektumok létrehozásának lehetőségét – és lehetővé teszi, hogy a kódját egy termeléshez hasonló környezetben tesztelje, mielőtt állandó licencet vásárolna.

## Előfeltételek

- **Java Development Environment** – JDK 8+ és egy build eszköz (Maven/Gradle) telepítve.
- **Aspose.PSD for Java** – Töltse le a legújabb JAR‑t a hivatalos oldalról [here](https://releases.aspose.com/psd/java/).
- **A sample PSD file** – A példákban a `OneLayer.psd` fájlt használjuk.

## Csomagok importálása

Adja hozzá a szükséges importokat a Java osztályához. Ezek az osztályok biztosítják a **psd image manipulation** és a rétegkezelés alapvető funkcióit.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Mi az a „set layer position”, és miért fontos?

Amikor új réteget ad hozzá, meg kell határoznia, hol jelenik meg a vásznon. A `setLeft`, `setTop`, `setRight` és `setBottom` metódusok **set layer position** pixel koordinátákban. A helyes pozicionálás biztosítja, hogy a grafikák pontosan a várt helyen legyenek, ami kulcsfontosságú feladatoknál, mint a UI eszközök kompozíciója vagy a nyomtatásra kész fájlok előkészítése.

## Lépésről‑lépésre útmutató

### 1. lépés: PSD fájl betöltése

Először töltse be a módosítani kívánt meglévő PSD‑t. Ez egy `PsdImage` objektumot ad, amellyel dolgozhat.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### 2. lépés: Pixel adatok és téglalapok előkészítése

Két pixelpuffer (`int[]`) lesz létrehozva, és meghatározzuk a téglalap alakú területeket, ahol az új rétegeket festeni fogjuk. Ez a **creating a new psd layer** alapja.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### 3. lépés: Rétegadatok inicializálása

Töltse fel a pixelpuffereket egy alapértelmezett ARGB értékkel. A `-10000000` érték egy félig átlátszó sötét árnyalatnak felel meg.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### 4. lépés: Szabályos rétegek hozzáadása (PSD rétegek manipulálása)

Most **add regular layers** a PSD képre, és a bal, felső, jobb, alsó tulajdonságokkal **set layer position**. Ez bemutatja, hogyan **manipulate PSD layers** programozottan.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### 5. lépés: PSD exportálása PNG‑be és a frissített PSD mentése

Miután a rétegek a helyükön vannak, mentse a módosított dokumentumot. Először exportáljuk az eredményt PNG‑be (a **export psd to png** lépés), majd a PSD‑t az új rétegekkel mentjük.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** Ha csak a PNG‑re van szüksége, kihagyhatja a PSD `save` hívást, és közvetlenül a `save`‑t `PngOptions`‑szel hívhatja.

## Gyakori problémák és hibaelhárítás

| Tünet | Valószínű ok | Javítás |
|---------|--------------|-----|
| A PNG üresnek jelenik meg | A rétegek láthatatlanok vagy teljesen átlátszóak | Győződjön meg róla, hogy nem átlátszó pixelértékeket állít be, vagy hívja a `layer.setVisible(true)`‑t. |
| `ArrayIndexOutOfBoundsException` | Eltérés a téglalap mérete és a pixel tömb hossza között | Ellenőrizze, hogy `rect.width * rect.height == dataArray.length`. |
| LicenseException futás közben | Nincs érvényes licenc betöltve | Töltsön be egy ideiglenes vagy állandó licencet, mielőtt bármely API metódust hívna. |

## Gyakran feltett kérdések

**Q: Kompatibilis az Aspose.PSD a Java 8‑al?**  
A: Igen, az Aspose.PSD támogatja a Java 8‑at és az újabb verziókat.

**Q: Alkalmazhatok transzformációkat (forgatás, méretezés) a hozzáadott rétegekre?**  
A: Természetesen! A `Layer` osztály olyan metódusokat biztosít, mint a `rotate`, `scale` és `translate` a teljes transzformációs vezérléshez.

**Q: Hol találok további Aspose.PSD dokumentációt?**  
A: Részletes API dokumentáció elérhető [here](https://reference.aspose.com/psd/java/).

**Q: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD‑hez?**  
A: Látogassa meg az ideiglenes licenc oldalát [here](https://purchase.aspose.com/temporary-license/).

**Q: Vannak közösségi fórumok az Aspose.PSD támogatásához?**  
A: Igen, csatlakozzon a beszélgetésekhez az Aspose fórumokon [here](https://forum.aspose.com/c/psd/34).

## Összegzés

Most már megtanulta, hogyan **export PSD to PNG** miközben **new regular layers** hozzáad az Aspose.PSD for Java használatával, és látta, hogyan teszi lehetővé egy **aspose temporary license**, hogy korlátozások nélkül kipróbálja ezt a munkafolyamatot. Ez a bemutató a **psd image manipulation** alapvető képességeit mutatja be: fájl betöltése, rétegek létrehozása, pixeladatok feltöltése és a végső kompozíció exportálása. Nyugodtan kísérletezzen különböző téglalapméretekkel, pixel színekkel vagy réteg hatásokkal, hogy a kimenetet a projekt igényeihez igazítsa.

---

**Legutóbb frissítve:** 2026-04-08  
**Tesztelve ezzel:** Aspose.PSD 24.11 for Java  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}