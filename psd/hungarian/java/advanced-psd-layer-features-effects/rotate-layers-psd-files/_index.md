---
date: 2026-07-22
description: Ismerje meg, hogyan mentse a psd-t png-ként, őrizze meg a PNG átlátszóságát,
  és forgassa a PSD rétegeket Java-ban az Aspose.PSD segítségével. Lépésről‑lépésre
  útmutató, kód nélküli magyarázatok és hibaelhárítási tippek.
keywords:
- save psd as png
- export psd layers png
- convert photoshop file png
- psd to png transparency
lastmod: 2026-07-22
linktitle: psd mentése png-ként és rétegek forgatása Java-ban az Aspose.PSD használatával
og_description: psd mentése png-ként az Aspose.PSD for Java segítségével. Őrizze meg
  az átlátszóságot, forgassa a rétegeket, és exportálja a PNG-t néhány kódsorral—ideális
  automatizált munkafolyamatokhoz.
og_image_alt: 'Developer guide: save PSD as PNG and rotate layers using Aspose.PSD
  for Java'
og_title: psd mentése png-ként és rétegek forgatása Java-ban az Aspose.PSD használatával
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  headline: save psd as png and rotate layers in Java using Aspose.PSD
  type: TechArticle
- description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  name: save psd as png and rotate layers in Java using Aspose.PSD
  steps:
  - name: Set Up Your Java Project
    text: Create a new Java project in your IDE and add the Aspose.PSD JAR to the
      project’s build path.
  - name: Import Required Classes
    text: '`PsdImage` is the core class that represents a Photoshop document in memory.
      `PngOptions` controls PNG‑specific settings, and `RotateFlipType` defines rotation
      and flip operations. These imports give you access to image loading, rotation,
      and PNG‑specific options.'
  - name: Define File Paths
    text: Specify where your source PSD lives and where the output files should be
      written. Using absolute paths during testing avoids “file not found” errors.
      > **Pro tip:** Store paths in a configuration file for easier maintenance in
      larger projects.
  - name: Load the PSD File
    text: '`PsdImage` loads the entire Photoshop document, including all layers, masks,
      and effects, into a manipulable object. Now `im` represents the whole PSD, ready
      for transformations.'
  - name: Rotate the Image (How to rotate PSD)
    text: '`RotateFlipType` enumerates all supported rotations and flips. In this
      example we rotate 270° and flip both axes, which swaps width and height while
      mirroring the image. Feel free to experiment with other values such as `Rotate90FlipNone`
      or `Rotate180FlipX`.'
  - name: Save the Rotated Image as PNG (save PSD as PNG)
    text: Configure `PngOptions` to keep transparency (`PngColorType.TruecolorWithAlpha`)
      and then call `save`. The PNG retains layer transparency, ensuring it works
      seamlessly in web or mobile apps. The resulting PNG preserves alpha channels,
      making it suitable for compositing or further processing.
  - name: Save the Modified PSD (optional)
    text: If you also need a new PSD with the rotation applied, you can save the modified
      `PsdImage` back to disk. You now have both a PNG preview and an updated PSD
      file.
  type: HowTo
- questions:
  - answer: Yes, you can call `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`
      after iterating through `im.getLayers()`.
    question: Can I rotate a specific layer in a PSD file?
  - answer: The library handles most files efficiently, but extremely large PSDs (>500
      MB) may require additional memory or streaming options.
    question: Is there any performance limitation with Aspose.PSD for Java?
  - answer: Aspose offers a free trial, but a paid license is needed for production.
      See the [temporary license](https://purchase.aspose.com/temporary-license/)
      for testing.
    question: Is Aspose.PSD free to use?
  - answer: Comprehensive docs are available at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Get help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).
    question: What if I encounter issues while using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
- rotate PSD layers
title: psd mentése png-ként és rétegek forgatása Java-ban az Aspose.PSD használatával
url: /hu/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

## Kapcsolódó oktatóanyagok

- [PSD mentése PNG-ként és renderelt árnyék alkalmazása Aspose.PSD for Java-ban](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Hogyan tömörítsünk PNG fájlokat az Aspose.PSD for Java használatával](/psd/java/optimizing-png-files/compress-png-files/)
- [Hogyan forgassunk képet Java-ban az Aspose.PSD-vel](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/pf/main-wrap-class >}}

# PSD mentése PNG-ként és rétegek forgatása Java-ban az Aspose.PSD használatával

## Bevezetés
Ha **PSD-t PNG-ként szeretne menteni**, miközben a rétegeket is forgatja, ez az útmutató Önnek szól. Akár kötegelt feldolgozó eszközt, akár egy webszolgáltatást épít, amelynek szüksége van valós idejű képmódosításra, vagy egyszerűen csak automatizálja a tervezési munkafolyamatot, a programozott megoldás időt takarít meg és megszünteti az Adobe Photoshop függőséget. Ebben az oktatóanyagban végigvezetjük, **hogyan forgassuk a PSD rétegeket**, és hogyan exportáljuk az eredményt PNG-ként az Aspose.PSD Java könyvtár segítségével. Gyerünk, tekerjük fel a gallért, és tegyük gördülékennyé a tervezési munkafolyamatot!

## Gyors válaszok
- **Melyik könyvtárat használhatom?** Aspose.PSD for Java  
- **Lehet egyszerre forgatni és PSD-t PNG-ként menteni?** Igen – először forgassa a PSD-t, majd mentse PNG-ként  
- **Szükség van licencre?** Ingyenes próba a teszteléshez; a termeléshez fizetett licenc szükséges  
- **Melyik Java verzió támogatott?** Java 8 és újabb  
- **Átlátszó lesz a PNG kimenet?** Igen, ha a `PngColorType.TruecolorWithAlpha` beállítást használja

## Mi az a „PSD konvertálása PNG-re”?
A Photoshop dokumentum (PSD) PNG képpé konvertálása a vizuális tartalmat – beleértve a rétegeket, maszkokat és alfa csatornákat – egy széles körben támogatott raszteres formátumba extrahálja, amely megőrzi az átlátszóságot. Ez a PNG ideálissá teszi webgrafikák, bélyegképek és további képfeldolgozás céljára. A kapott PNG közvetlenül felhasználható weboldalakon, mobilalkalmazásokban, vagy további feldolgozásra más képkönyvtárak által.

## Miért használjuk az Aspose.PSD for Java-t PSD PNG-ként mentésére és PSD rétegek forgatására?
Az Aspose.PSD lehetővé teszi, hogy **PSD-t PNG-ként mentse** és a rétegeket Photoshop telepítése nélkül forgassa. Támogat **50+ bemeneti és kimeneti formátumot**, több száz oldalas PSD fájlokat kevesebb, mint 200 MB RAM-mal dolgoz fel, és Windows, Linux, valamint macOS rendszereken fut. Az API csak néhány metódushívást igényel, magas hűségű eredményeket biztosít beépített réteg‑effektus, maszk és alfa csatorna kezelésével.

## Előfeltételek
Mielőtt a kódba merülnénk, győződjön meg róla, hogy a következőkkel rendelkezik:

- **Java Fejlesztői Készlet (JDK)** – letöltés az [Oracle weboldalról](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrált Fejlesztői Környezet (IDE)** – IntelliJ IDEA, Eclipse vagy NetBeans mind megfelelő.  
- **Aspose.PSD for Java könyvtár** – szerezze be a legújabb JAR-t a [release page](https://releases.aspose.com/psd/java/).  
- **Alap Java ismeretek** – osztályok, objektumok és kivételkezelés ismerete.

## Lépésről‑lépésre útmutató

### 1. lépés: Java projekt beállítása
Hozzon létre egy új Java projektet az IDE‑jében, és adja hozzá az Aspose.PSD JAR‑t a projekt build útvonalához.

### 2. lépés: Szükséges osztályok importálása
`PsdImage` az a fő osztály, amely egy Photoshop dokumentumot reprezentál memóriában. `PngOptions` a PNG‑specifikus beállításokat kezeli, a `RotateFlipType` pedig a forgatás‑ és tükrözési műveleteket definiálja.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Ezek az importok hozzáférést biztosítanak a kép betöltéséhez, forgatáshoz és a PNG‑specifikus beállításokhoz.

### 3. lépés: Fájl útvonalak meghatározása
Adja meg, hol található a forrás‑PSD, és hová kell írni a kimeneti fájlokat. A tesztelés során abszolút útvonalak használata elkerüli a „file not found” hibákat.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Pro tipp:** Tárolja az útvonalakat egy konfigurációs fájlban a nagyobb projektek könnyebb karbantartása érdekében.

### 4. lépés: PSD fájl betöltése
`PsdImage` betölti a teljes Photoshop dokumentumot, beleértve az összes réteget, maszkot és effektust, egy manipulálható objektumba.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Most a `im` a teljes PSD‑t képviseli, készen áll a transzformációkra.

### 5. lépés: Kép forgatása (Hogyan forgassuk a PSD-t)
A `RotateFlipType` felsorolja az összes támogatott forgatást és tükrözést. Ebben a példában 270°‑ot forgatunk és mindkét tengelyen tükrözünk, ami a szélességet és magasságot felcseréli, miközben a képet tükrözi.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Nyugodtan kísérletezzen más értékekkel, például `Rotate90FlipNone` vagy `Rotate180FlipX`.

### 6. lépés: Forgatott kép mentése PNG‑ként (PSD mentése PNG‑ként)
Állítsa be a `PngOptions`‑t, hogy megőrizze az átlátszóságot (`PngColorType.TruecolorWithAlpha`), majd hívja meg a `save` metódust. A PNG megőrzi a réteg‑átlátszóságot, biztosítva, hogy zökkenőmentesen működjön web‑ vagy mobilalkalmazásokban.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Az eredmény‑PNG megőrzi az alfa csatornákat, így alkalmas kompozícióra vagy további feldolgozásra.

### 7. lépés: Módosított PSD mentése (opcionális)
Ha szüksége van egy új PSD‑re is, amelyben a forgatás már alkalmazva van, mentheti a módosított `PsdImage`‑t vissza a lemezre.

```java
im.save(psdPath);
```

Most már rendelkezik egy PNG‑előnézettel és egy frissített PSD fájllal is.

## Gyakori problémák és megoldások
- **File not found:** Ellenőrizze, hogy a `dataDir` útvonal egy útvonal‑elválasztóval (`/` vagy `\`) végződik.  
- **OutOfMemoryError nagy PSD‑k esetén:** Növelje a JVM heap méretét (`-Xmx2g`).  
- **Átlátszóság elveszett:** Győződjön meg róla, hogy a `PngColorType.TruecolorWithAlpha` be van állítva; ellenkező esetben a PNG alfa nélkül lesz mentve.  
- **Flip PSD kép nem a várt módon viselkedik:** Ellenőrizze a kiválasztott `RotateFlipType` konstansot; egyes konstansok egy lépésben kombinálják a forgatást és a tükrözést.

## Gyakran Ismételt Kérdések

**K: Forgathatok egy adott réteget egy PSD fájlban?**  
V: Igen, a `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)` hívással a `im.getLayers()` iterálása után.

**K: Van valamilyen teljesítménykorlát az Aspose.PSD for Java‑val?**  
V: A könyvtár a legtöbb fájlt hatékonyan kezeli, de a rendkívül nagy PSD‑k (>500 MB) további memóriát vagy streaming opciókat igényelhetnek.

**K: Ingyen használható az Aspose.PSD?**  
V: Az Aspose ingyenes próbaverziót kínál, de a termeléshez fizetett licenc szükséges. Lásd a [temporary license](https://purchase.aspose.com/temporary-license/) oldalt a teszteléshez.

**K: Hol találok részletes dokumentációt?**  
V: A teljes dokumentáció elérhető a [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) oldalon.

**K: Mit tegyek, ha problémáim vannak az Aspose.PSD használatával?**  
V: Segítséget kaphat a [Aspose Support Forum](https://forum.aspose.com/c/psd/34) fórumon.

**K: A PSD‑t PNG‑re konvertálva megmaradnak a réteg‑effektusok?**  
V: Igen, ha a `PngColorType.TruecolorWithAlpha` beállítással ment, a legtöbb vizuális effektus rasterizálódik a PNG‑be.

**K: Batch‑processzálhatok több PSD fájlt?**  
V: Természetesen. A kódot egy ciklusba ágyazva iterálhat egy PSD‑fájlok könyvtárán.

**K: Beállítható a PNG tömörítési szint?**  
V: A `PngOptions` rendelkezik egy `setCompressionLevel(int)` metódussal a kimeneti méret finomhangolásához.

**K: Zárnom kell a képobjektust?**  
V: A `PsdImage` implementálja a `Closeable` interfészt; használjon try‑with‑resources blokkot vagy hívja meg az `im.close()`‑t egy `finally` blokkban.

**K: A forgatott PNG ugyanazokkal a méretekkel rendelkezik, mint az eredeti?**  
V: A 90°‑os vagy 270°‑os forgatás felcseréli a szélességet és magasságot, így a PNG automatikusan az új orientációt tükrözi.

## Összegzés
Az Aspose.PSD for Java segítségével **PSD‑t PNG‑ként menthet**, **megőrizheti a PNG átlátszóságát**, és **PSD rétegeket forgathat** néhány kódsorral. Ez a megközelítés megszünteti a Photoshop szükségességét, felgyorsítja az automatizált munkafolyamatokat, és teljes kontrollt ad a képkimenet felett. Próbálja ki saját projektjeiben, és tapasztalja meg, mennyi időt takaríthat meg!

---

**Last Updated:** 2026-07-22  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}