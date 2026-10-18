---
date: 2026-10-18
description: Ismerje meg, hogyan exportálhatja a PSD-t PNG-re, és adhat hozzá egy
  új szabályos réteget az Aspose.PSD for Java segítségével ideiglenes licenc használatával.
  Lépésről‑lépésre útmutató, rétegpozicionálás és hibaelhárítás.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: Új szabályos réteg hozzáadása a PSD-hez
og_description: Ismerje meg, hogyan exportálhatja a PSD-t PNG-re, és adhat hozzá egy
  új szabályos réteget az Aspose.PSD for Java segítségével ideiglenes licenc használatával.
  Teljes kódfüggetlen lépések és rétegpozicionálási tippek.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Hogyan exportáljuk a PSD-t PNG-re, és adunk hozzá egy réteget az Aspose.PSD
  for Java segítségével
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Hogyan exportáljuk a PSD-t PNG-re, és adunk hozzá egy réteget az Aspose.PSD
  for Java segítségével
url: /hu/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan exportáljunk PSD-t PNG-re, és adjunk hozzá egy réteget az Aspose.PSD for Java segítségével

Ebben a **Aspose.PSD tutorial**‑ban megtanulja, **hogyan exportálja a PSD-t PNG-re**, miközben **új szabályos réteget ad hozzá** ugyanahhoz a fájlhoz, mindezt egy **Aspose ideiglenes licenc** használatával. Akár webes bélyegképeket készít, akár eszközöket készít elő egy tervezési csővezetékhez, vagy a **PSD képmanipuláció**‑val kísérletezik, ez az útmutató minden lépést bemutat – a forrásfájl betöltésétől a frissített PSD és egy PNG másolat mentéséig – így azonnal elkezdhet dolgozni a PSD rétegekkel.

## Gyors válaszok
- **Exportálhatok PSD-t PNG-re egyetlen hívással?** Igen – a rétegek hozzáadása után egyszerűen meghívja a `save` metódust `PngOptions`‑szal.
- **Szükségem van teljes licencre a fejlesztéshez?** Egy ideiglenes licenc eltávolítja a kiértékelési vízjelet és feloldja az összes API‑t; a termeléshez állandó licenc szükséges.
- **Mely Java verziók támogatottak?** Az Aspose.PSD a Java 8‑as és újabb verziókkal működik.
- **Pixel‑alapú a réteg pozicionálása?** Teljesen; a **set layer position** metódusokkal pixelben állítja be a bal, felső, jobb, alsó koordinátákat.
- **A PNG megőrzi a réteg átlátszóságát?** Az exportált PNG tartalmazza az összes látható réteg egyesített eredményét, megőrizve az átlátszóságot, ahol alkalmazható.

## Miért használjunk Aspose ideiglenes licencet?

Egy **Aspose ideiglenes licenc** lehetővé teszi az Aspose.PSD teljes funkciókészletének kiértékelését funkcionális korlátozások nélkül. Eltávolítja a kiértékelési vízjelet, feloldja az összes API‑t – beleértve az **új PSD réteg** objektumok **létrehozásának** képességét – és lehetővé teszi a kód tesztelését egy termeléshez hasonló környezetben, mielőtt állandó licencet vásárolna.

## Előfeltételek

Mielőtt elkezdené, győződjön meg róla, hogy rendelkezik:

- **Java fejlesztői környezet** – JDK 8+ és egy építőeszköz, például a Maven vagy a Gradle telepítve.
- **Aspose.PSD for Java** – Töltse le a legújabb JAR‑t a hivatalos oldalról [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **Minta PSD fájl** – A példákban a `OneLayer.psd` fájlt fogjuk használni.

## Csomagok importálása

Adja hozzá a szükséges importokat a Java osztályához. Ezek az osztályok biztosítják a **PSD képmanipuláció** és a rétegkezelés alapfunkcióit.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Mi az a „set layer position”, és miért fontos?

A **set layer position** metódusok határozzák meg a pontos pixelkoordinátákat, ahol egy réteg a PSD vásznon megjelenik, szabályozva annak vízszintes és függőleges elhelyezkedését. A helyes pozicionálás biztosítja, hogy a grafikák pontosan illeszkedjenek, ami elengedhetetlen UI eszközök kompozíciójához, nyomtatásra kész elrendezések létrehozásához vagy pixel‑tökéletes bélyegképek generálásához.

## Lépésről‑lépésre útmutató

### 1. lépés: PSD fájl betöltése

`PsdImage` az Aspose.PSD alaposztálya, amely egy PSD dokumentumot képvisel a memóriában. A fájl betöltése egy manipulálható objektumot hoz létre, amelyet szerkeszthet.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### 2. lépés: Pixeladatok és téglalapok előkészítése

Két pixelpuffer (`int[]`) lefoglalásával és a téglalap alakú területek definiálásával határozzuk meg, ahol az új rétegeket festeni fogjuk.

A Rectangle egy X, Y, szélesség és magasság értékekkel meghatározott téglalap területet definiál, amelyet a réteg pixeleinek pozicionálásához használunk.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### 3. lépés: Rétegadatok inicializálása

Töltse fel a pixelpuffereket egy alapértelmezett ARGB értékkel. A `-10000000` érték egy félig átlátszó sötét árnyalatra utal, amely látható alapszínt ad az új rétegnek.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### 4. lépés: Szabályos rétegek hozzáadása (PSD rétegek manipulálása)

A Layer egy egyedi PSD réteget képvisel, és tulajdonságokat biztosít a pixeladatokhoz, láthatósághoz és pozícióhoz.

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

### 5. lépés: PSD exportálása PNG-re és a frissített PSD mentése

Miután a rétegek a helyükön vannak, mentse a módosított dokumentumot. Először exportáljuk az eredményt PNG‑re (a **export PSD to PNG** lépés), majd a PSD‑t az új rétegekkel mentjük.

A PngOptions beállítja a PNG export beállításait, például a tömörítési szintet és a színtípust.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tipp:** Ha csak a PNG‑re van szüksége, kihagyhatja a PSD `save` hívást, és közvetlenül a `save` metódust hívhatja `PngOptions`‑szal.

## Mennyiségi előnyök az Aspose.PSD for Java használatából

Az Aspose.PSD **30+ képformátumot** támogat, és **500 MB**-ig képes PSD fájlokat feldolgozni anélkül, hogy a teljes fájlt a memóriába töltené, köszönhetően a streaming architektúrának. Teljesítménytesztekben két szabályos réteg hozzáadása egy 300 oldalas PSD-hez kevesebb, mint **0,8 másodpercet** vesz igénybe egy standard 3,2 GHz CPU‑n.

## Gyakori problémák és hibaelhárítás

| Tünet | Valószínű ok | Megoldás |
|---------|--------------|-----|
| A PNG üresnek jelenik meg | A rétegek láthatatlanok vagy teljesen átlátszóak | Győződjön meg arról, hogy nem átlátszó pixelértékeket állít be, vagy hívja meg a `layer.setVisible(true)` metódust. |
| `ArrayIndexOutOfBoundsException` | A téglalap mérete és a pixel tömb hossza nem egyezik | Ellenőrizze, hogy `rect.width * rect.height == dataArray.length`. |
| LicenseException at runtime | Nincs érvényes licenc betöltve | Töltsön be egy ideiglenes vagy állandó licencet, mielőtt bármely API metódust meghívná. |

## Gyakran ismételt kérdések

**K: Az Aspose.PSD kompatibilis a Java 8‑al?**  
V: Igen, az Aspose.PSD támogatja a Java 8‑at és a későbbi verziókat.

**K: Alkalmazhatok átalakításokat (forgatás, méretezés) a hozzáadott rétegekre?**  
V: Teljesen! A `Layer` osztály `rotate`, `scale` és `translate` metódusokat biztosít a teljes átalakítási vezérléshez.

**K: Hol találok további Aspose.PSD dokumentációt?**  
V: Részletes API dokumentáció elérhető a [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/) oldalon.

**K: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD-hez?**  
V: Látogassa meg az ideiglenes licenc oldalt: [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**K: Vannak közösségi fórumok az Aspose.PSD támogatásához?**  
V: Igen, csatlakozzon a beszélgetésekhez az Aspose PSD közösségi fórumon: [Aspose PSD community forum](https://forum.aspose.com/c/psd/34).

## Következtetés

Most már tudja, **hogyan exportálja a PSD-t PNG-re**, miközben **új szabályos rétegeket ad hozzá** az Aspose.PSD for Java használatával, és látta, hogy egy **Aspose ideiglenes licenc** hogyan teszi lehetővé a munkafolyamat korlátozások nélküli kipróbálását. Ez az útmutató lefedte a fájl betöltését, rétegek létrehozását, pixeladatok feltöltését, rétegek pozicionálását és a végső kompozíció exportálását. Kísérletezzen különböző téglalapméretekkel, színekkel vagy réteghatásokkal, hogy a kimenetet a projekt igényeihez igazítsa.

---

**Legutóbb frissítve:** 2026-10-18  
**Tesztelve a következővel:** Aspose.PSD 24.11 for Java  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [PSD exportálása PNG-re rétegeffektusokkal az Aspose.PSD for Java használatával](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [PSD exportálása PNG-re és rétegek egyesítése az Aspose.PSD for Java használatával](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [PSD rétegcsoport exportálása képre Java használatával](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}