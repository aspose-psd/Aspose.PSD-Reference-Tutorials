---
date: 2026-08-01
description: Ismerje meg, hogyan exportálhat PSD‑t PNG‑re, és kezelheti az uncompressed
  image streams-et az Aspose.PSD for Java segítségével.
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: Uncompressed Image Stream objektum kezelése PSD‑ben – Java
og_description: export psd to png using Aspose.PSD for Java. Ismerje meg, hogyan kezelje
  az uncompressed image streams-et, hozzon létre graphics objects-et, és mentse a
  high‑quality PNGs-et.
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: export psd to png – Java útmutató a uncompressed PSD streams-hez
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: Export PSD to PNG – PSD grafikai objektum létrehozása – Uncompressed Stream
  Java‑ban
url: /hu/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD exportálása PNG-re – PSD grafikus objektum létrehozása – Tömörítetlen adatfolyam Java-ban

## Bevezetés
Ebben a lépésről‑lépésre útmutatóban **export PSD to PNG** műveletet hajtja végre egy tömörítetlen képadatfolyammal dolgozva az Aspose.PSD for Java segítségével. Akár egy tervezési folyamatot automatizál, akár egy egyedi szerkesztőt épít, a Photoshop fájl minőségvesztés nélküli renderelése elengedhetetlen. Elkezdjük a szükséges beállításokkal, végigvezetünk egy `Graphics` objektum létrehozásán, és befejezzük egy veszteségmentes PNG exporttal. A végére megérti, miért kezeli hatékonyan az Aspose.PSD a nyers adatfolyamokat, és hogyan integrálható bármely Java projektbe.

## Gyors válaszok
- **Mi jelent a „create PSD graphics object”?** Ez egy `Graphics` kontextus példányosítását jelenti, amely lehetővé teszi, hogy programozott módon rajzolj vagy módosíts egy PSD képet.  
- **Melyik könyvtár kezeli a tömörítetlen adatfolyamokat?** Az Aspose.PSD for Java teljes támogatást nyújt a nyers (tömörítetlen) képadatokhoz.  
- **Exportálhatok PSD-t PNG-re a szerkesztés után?** Igen – miután van egy `Graphics` objektuma, renderelheti a PSD-t és egyetlen hívással mentheti PNG‑ként.  
- **Szükségem van licencre a fejlesztéshez?** Egy ingyenes próba verzió tesztelésre működik; a termelési környezethez kereskedelmi licenc szükséges.  
- **Az export veszteségmentes?** A PNG‑re exportálás megőrzi az eredeti pixeladatokat, veszteségmentes minőséget biztosítva, kisebb fájlmérettel, mint a nyers PSD.

## Mi az a PSD exportálása PNG-re?
A PSD‑t PNG‑re exportálás egy réteges Photoshop dokumentumot egyetlen rétegre, veszteségmentes raszteres képre konvertál, amely bármely webböngésző vagy képmegjelenítő által megjeleníthető. A folyamat megőrzi az átlátszóságot, a színmélységet és a réteg‑effekteket, miközben eldobja a Photoshop‑specifikus metaadatokat. Emellett megőrzi az eredeti színprofilt a pontos színreprodukció érdekében.

## Miért használjuk az Aspose.PSD for Java-t képműveletekhez?
Az Aspose.PSD **50+** bemeneti és kimeneti formátumot támogat – beleértve a PSD, PNG, JPEG, BMP és TIFF formátumokat – és képes **200+** réteggel rendelkező fájlokat feldolgozni anélkül, hogy az egész dokumentumot a memóriába töltené. A `Raw` tömörítési opció a pixeladatokat tömörítetlenül tárolja, ezzel garantálva a pixel‑pontos hűséget a későbbi szerkesztéshez vagy archiváláshoz.

## Előfeltételek
Mielőtt a kódba merülnénk, ellenőrizze, hogy a következőkkel rendelkezik:

- **Java Development Kit (JDK)** – JDK 8 vagy újabb telepítve.  
- **Aspose.PSD for Java** – Töltse le a legújabb JAR‑t a hivatalos kiadási oldalról: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/). Elérheti a [this link](https://releases.aspose.com/psd/java/) vagy a [release page](https://releases.aspose.com/psd/java/) segítségével is. Más Aspose termékekhez kattintson [here](https://releases.aspose.com/).  
- **IDE** – IntelliJ IDEA, Eclipse vagy bármely Java‑kompatibilis szerkesztő.  
- **Alap Java ismeretek** – Osztályok, metódusok és kivételkezelés ismerete.

Ezekkel a feltételekkel készen áll a kódolás megkezdésére.

## Csomagok importálása
A `Graphics` osztály az Aspose.PSD rajzfelülete, amely lehetővé teszi a pixeladatok közvetlen renderelését vagy szerkesztését. A `PsdImage` osztály egy PSD fájlt képvisel a memóriában, míg a `PsdOptions` szabályozza, hogyan kerül mentésre a kép.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Most bontsuk le a kódot emészthető lépésekre, hogy könnyen követhesse. Beállítjuk a környezetet, betöltünk egy PSD fájlt, módosítjuk, és végül elmentjük a kimenetet.

## 1. lépés: A dokumentum könyvtárának meghatározása
Minden fájlművelet előtt meg kell adnia a programnak, hogy hol keresse a PSD eszközöket. Ez a könyvtárútvonal a teljes útmutató során használatos.

```java
String dataDir = "Your Document Directory";
```

Cserélje le a `"Your Document Directory"` értéket arra az abszolút útvonalra, amely a `layers.psd` fájlt tartalmazza. Az útvonal konfigurálhatóvá tétele lehetővé teszi a kód újrahasználhatóságát különböző projektekben.

## 2. lépés: ByteArrayOutputStream létrehozása
A `ByteArrayOutputStream` egy Java adatfolyam, amely adatokat tárol memóriában bájt tömbként. In‑memory pufferként működik a módosított képhez, lehetővé téve a nyers bájtok rögzítését, mielőtt lemezre írnák vagy hálózaton keresztül továbbítanák.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

A `ms` változó a `save` művelet után a tömörítetlen képadatokat fogja tárolni.

## 3. lépés: PSD fájl betöltése
A `PsdImage` osztály betölt egy PSD fájlt a memóriába a manipulációhoz. A fájl betöltése a lemezen lévő PSD‑t egy `PsdImage` objektummá alakítja, amelyet módosíthat. Ebben a lépésben az Aspose.PSD beolvassa a fájlfejlécet, a rétegeket és az erőforrásokat.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Ha az útvonal helytelen, az Aspose.PSD `FileNotFoundException`‑t dob, amelyet a termelési kódban le kell kezelni.

## 4. lépés: PsdOptions beállítása mentéshez
A `PsdOptions` a PSD fájlok mentési paramétereit határozza meg. A tömörítési módszer `Raw`‑ra állítása azt jelzi, hogy a pixeladatok tömörítés nélkül legyenek tárolva, megőrizve minden pixel pontos állapotát a memóriában.

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

A `CompressionMethod.Raw` opció a pixeladatokat tömörítés nélkül tárolja, ami ideális, ha később további szerkesztéseket tervez.

## 5. lépés: Kép mentése a kimeneti adatfolyamba
Most a PSD‑t (bármilyen módosítással) a korábban létrehozott `ByteArrayOutputStream`‑ba menti. A `save` metódus figyelembe veszi a beállított `PsdOptions`‑t.

```java
psdImage.save(ms, saveOptions);
```

Ekkor a `ms` a tömörítetlen PSD teljes bináris reprezentációját tartalmazza.

## 6. lépés: Kimeneti adatfolyam visszaállítása
A írás után az adatfolyam belső mutatója a végén áll. Visszaállítva a mutató visszatekeri az adatfolyamot, így az elejéről olvasható.

```java
ms.reset();
```

Ezt úgy képzelje el, mintha a szalaghúzót visszatekerné a lejátszás előtt.

## 7. lépés: Az újonnan létrehozott kép betöltése
Most közvetlenül a bájt tömbből hozhat létre egy új `PsdImage` példányt. Ez a lépés ellenőrzi, hogy a mentett adat sértetlenül újratölthető-e.

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Ha a kép sikeresen betöltődik, tudja, hogy a tömörítetlen adatfolyam helyesen lett írva.

## 8. lépés: Graphics objektum létrehozása
A `Graphics` osztály az Aspose.PSD rajzvászna. Metódusokat biztosít alakzatok, szöveg rajzolásához és szűrők alkalmazásához közvetlenül egy `PsdImage` pixelmátrixára.

```java
Graphics graphics = new Graphics(psdImage);
```

Ezzel a `Graphics` példánnyal új tartalmat festhet, részeket törölhet, vagy további rétegeket kombinálhat.

## Hogyan exportálhatok PSD-t PNG-re az Aspose.PSD for Java használatával?
Töltse be a PSD-t a `new PsdImage(dataDir + "layers.psd")` segítségével, hozza létre a `Graphics` objektumot, végezze el a szükséges rajzolást, majd hívja a `psdImage.save("output.png", new PngOptions())` metódust. Ez a sorozat rendereli a szerkesztett PSD‑t és egyetlen lépésben veszteségmentes PNG‑t ír ki, az Aspose.PSD beépített konverziós motorját használva.

## PSD rétegek manipulálása Graphics objektummal
A `Graphics` példány pixel‑szintű vezérlést biztosít minden réteg felett. Rajzolhat geometriai alakzatokat, renderelhet szöveget, vagy egyedi szűrőket alkalmazhat. Mivel a grafikus kontextus a réteg rasterizált nézetén dolgozik, a változások azonnal láthatóak a kép mentésekor.

## Gyakori problémák és megoldások
- **NullPointerException a fájl betöltésekor** – ellenőrizze a `dataDir` útvonalat, és győződjön meg arról, hogy a fájlnév pontosan egyezik, beleértve a kis‑ és nagybetűket is.  
- **Tömörített kimenet a Raw használata ellenére** – ellenőrizze, hogy a `saveOptions.setCompressionMethod(CompressionMethod.Raw);` **a** `save` hívás **előtt** van-e meghívva.  
- **Graphics objektum üresnek tűnik** – győződjön meg róla, hogy a megfelelő `PsdImage` példányon (a betöltöttön, nem egy újonnan létrehozott üres képen) rajzol.  
- **OutOfMemoryError nagy fájloknál** – használja a `PsdImage.load(dataDir, LoadOptions)`‑t a `loadOptions.setLoadMode(LoadMode.Memory)` beállítással, hogy nagy fájlokat streameljen anélkül, hogy az egész dokumentumot a RAM‑ba töltené.

## GYIK

### Mi az az Aspose.PSD?
Az Aspose.PSD egy Java könyvtár, amely lehetővé teszi a fejlesztők számára, hogy programozott módon hozzanak létre, szerkesszenek és konvertáljanak Photoshop PSD fájlokat anélkül, hogy az Adobe Photoshopra lenne szükség. Támogatja a PSD fájlok olvasását és írását, a rétegek, maszkok, csatornák és különféle kép erőforrások kezelését, valamint API‑kat biztosít raszter és vektor műveletekhez, így alkalmas szerver‑oldali képfeldolgozási és automatizálási feladatokra.

### Hogyan tölthetem le az Aspose.PSD for Java‑t?
Letöltheti a hivatalos kiadási oldalról: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/).

### Van ingyenes próba verzió az Aspose.PSD‑hez?
Igen, egy teljes funkcionalitású próba verzió elérhető ugyanazon a letöltési oldalon. Fejlesztési és értékelési célokra használható.

### Kaphatok támogatást az Aspose.PSD‑hez?
Természetesen! Az Aspose támogatási fórum a termékcsapattól és a közösségtől származó válaszokat kínál: [Aspose support forum](https://forum.aspose.com/c/psd/34).

### Hogyan szerezhetek ideiglenes licencet az Aspose.PSD‑hez?
Kérhet ideiglenes licencet közvetlenül az Aspose licencportáljáról, amely 30 napra érvényes, időkorlátos kulcsot biztosít. Ez lehetővé teszi az Aspose.PSD teljes funkcionalitásának kiértékelését anélkül, hogy kereskedelmi licencet vásárolna. A próbaidőszak után a temporális kulcsot állandó licencre kell cserélni a könyvtár termelésben való használatához. Látogassa meg az ideiglenes licenc portált egy időkorlátos kulcs generálásához: [temporary license page](https://purchase.aspose.com/temporary-license/).

## Gyakran Ismételt Kérdések

**Q: Használhatom a graphics objektumot csak egy adott réteg szerkesztésére?**  
A: Igen. A PSD betöltése után a kívánt réteget a `psdImage.getLayers().get_Item(index)` segítségével érheti el, és ezt a réteget adja át a `Graphics` konstruktorának.

**Q: Befolyásolja a Raw tömörítési módszer a fájlméretet?**  
A: A Raw a pixeladatokat tömörítés nélkül tárolja, így a kapott fájl nagyobb lesz, mint egy tömörített PSD, de 100 % pixel‑hűséget garantál.

**Q: Lehetséges a szerkesztett PSD-t más formátumba (pl. PNG) exportálni?**  
A: Természetesen. Szerkesztés után hívja meg a `psdImage.save("output.png", new PngOptions())`‑t – ez a szabványos módja a **export PSD to PNG** veszteségmentes minőséggel.

**Q: Milyen Java verzió szükséges?**  
A: Az Aspose.PSD for Java támogatja a JDK 8‑at és újabb verziókat, beleértve az összes LTS kiadást a JDK 21‑ig.

**Q: Hogyan szabadítsam fel az erőforrásokat a feldolgozás után?**  
A: Hívja meg a `psdImage.dispose()`‑t és zárja be az összes adatfolyamot (pl. `ms.close()`), hogy felszabadítsa a natív memóriát és elkerülje a szivárgásokat.

---

**Utoljára frissítve:** 2026-08-01  
**Tesztelve:** Aspose.PSD for Java (legújabb kiadás)  
**Szerző:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó oktatóanyagok

- [Képek mentése adatfolyamra az Aspose.PSD for Java-val](/psd/java/advanced-techniques/save-images-to-stream/)
- [PSD rétegcsoport exportálása képre Java használatával](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [Kép létrehozása adatfolyam használatával az Aspose.PSD for Java-ban](/psd/java/image-editing/create-image-using-stream/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}