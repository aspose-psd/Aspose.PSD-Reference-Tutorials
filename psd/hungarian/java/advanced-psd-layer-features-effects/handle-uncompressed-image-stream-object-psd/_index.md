---
date: 2026-02-17
description: Ismerje meg, hogyan exportálhat PSD-t PNG-re, és kezelheti a tömörítetlen
  képadat-áramokat az Aspose.PSD for Java segítségével.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: PSD exportálása PNG-be – PSD grafikus objektum létrehozása – Nem tömörített
  adatfolyam Java-ban
url: /hu/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

-button >}}

Now produce final content with translations, preserving all placeholders.

Be careful with markdown formatting: keep headings with same number of #. Keep bold markup.

Let's craft Hungarian translations.

I'll write Hungarian text.

Note: Keep code block placeholders unchanged.

Proceed.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD exportálása PNG‑be – PSD Graphics Object létrehozása – Nem tömörített adatfolyam Java‑ban

## Introduction
Üdvözöljük a képfeldolgozás világában Java‑ban! Ebben az útmutatóban **létrehozza a PSD graphics object‑et**, kezelni fogja a nem tömörített képadatfolyam objektumokat, és megtanulja, hogyan **exportálja a PSD‑t PNG‑be** az Aspose.PSD for Java segítségével. Akár grafikus tervező, aki automatizálni szeretné a munkafolyamatait, akár szoftverfejlesztő, aki erőteljes képfeldolgozó képességeket szeretne beépíteni alkalmazásaiba, ez az útmutató kifejezetten Önnek készült. Áttekintjük a szükséges előkészületektől a végső exportig minden lépést, hogy alapos megértést szerezzen a teljes folyamatról.

## Quick Answers
- **Mit jelent a „create PSD graphics object”?** Ez egy grafikus kontextus példányosítását jelenti egy PSD fájlhoz, amely lehetővé teszi a tartalom rajzolását vagy szerkesztését.  
- **Melyik könyvtár kezeli a nem tömörített adatfolyamokat?** Az Aspose.PSD for Java teljes támogatást nyújt a raw (nem tömörített) képadatokhoz.  
- **Exportálhatom a PSD‑t PNG‑be a szerkesztés után?** Igen — miután rendelkezik egy `Graphics` objektummal, renderelheti a PSD‑t és mentheti PNG‑ként.  
- **Szükség van licencre fejlesztéshez?** Egy ingyenes próba verzió elegendő a teszteléshez; a kereskedelmi licenc a termeléshez kötelező.  
- **Az export veszteségmentes?** A PNG‑be exportálás megőrzi a képminőséget, a fájlméret nagyobb lesz, mint a JPEG‑é, de kisebb, mint egy nem tömörített PSD‑é.  

## How to export PSD to PNG using Aspose.PSD for Java
Amikor **exportálni kell a PSD‑t PNG‑be**, a tipikus munkafolyamat a következő:

1. Töltse be a PSD fájlt (vagy hozzon létre egy újat).  
2. Végezze el a rajzolást vagy a rétegmódosítást egy `Graphics` objektummal.  
3. Mentse a keletkezett képet `PngOptions` használatával (az ugyanaz a `Graphics` példány újra felhasználható).  

Bár ez az útmutató a nem tömörített adatfolyamok kezelésére fókuszál, a létrehozott `Graphics` objektum később is újra felhasználható a PSD PNG‑fájlba való rendereléséhez a folyamatban.

## Prerequisites
Mielőtt belevágunk a kódba, győződjünk meg róla, hogy minden szükséges eszköz rendelkezésre áll a feladat megkezdéséhez. Íme a követelmények:

### Java Development Kit (JDK)
Győződjön meg róla, hogy a JDK telepítve van a gépén. Letöltheti az Oracle weboldaláról, vagy használhatja az OpenJDK‑t.

### Aspose.PSD for Java
Le kell töltenie és telepítenie kell az Aspose.PSD könyvtárat. Ez a hatékony könyvtár lehetővé teszi a PSD fájlok egyszerű manipulálását. A legújabb verziót letöltheti a [this link](https://releases.aspose.com/psd/java/) címről.

### Integrated Development Environment (IDE)
Ajánlott egy IDE‑t használni a Java kód írásához és teszteléséhez. Használhatja az IntelliJ IDEA‑t, az Eclipse‑t vagy bármely más, Önnek megfelelő fejlesztőkörnyezetet.

### Basic Understanding of Java
A Java programozás alapjainak ismerete gördülékenyebbé teszi a folyamatot. Bizonyosodjon meg róla, hogy ismeri az osztályokat, metódusokat és a kivételkezelést.

Mindez megvan, tekerjük fel a ujjainkat, és vágjunk bele a legizgalmasabb részbe – a kódolásba!

## Import Packages
A kezdéshez importálnunk kell a szükséges csomagokat az Aspose.PSD használatához. Az alábbiakban megtalálja a PSD fájlok kezeléséhez általában szükséges importokat.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Most bontsuk le a kódot emészthető lépésekre, hogy könnyen követhesse. Beállítjuk, betöltünk egy PSD fájlt, módosítjuk, majd elmentjük a kimenetet.

## Step 1: Define Your Document Directory
Mielőtt elkezdené a kódolást, meg kell adnia, hol található a PSD fájlja. Ez lényegében a projekt színpadra állítását jelenti.

```java
String dataDir = "Your Document Directory";
```

Cserélje le a `"Your Document Directory"` szöveget a tényleges útvonalra, ahol a PSD fájl (például layers.psd) található. Ez megkönnyíti a fájlok megtalálását.

## Step 2: Create a Byte Array Output Stream
Szüksége van egy helyre, ahol a módosított képet tárolja, mielőtt bármit tenne vele. A `ByteArrayOutputStream` segít egyszerűen rögzíteni a képadatokat.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Ez a sor egy új `ByteArrayOutputStream` objektumot hoz létre `ms` néven. Ezt az objektumot fogja használni a nem tömörített kép mentéséhez.

## Step 3: Load the PSD File
Most jön a PSD fájl betöltése. Itt kezdődik a varázslat!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Ez a sor betölti a PSD fájlt egy `PsdImage` objektumba. Győződjön meg róla, hogy a helyes útvonalat adta meg; ellenkező esetben hiba jelenik meg, mint egy nem ellenőrzött felmérés.

## Step 4: Set Up the PsdOptions for Saving
Meg kell határoznia, hogyan szeretné menteni a képet — természetesen nem tömörítve!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Itt hoz létre egy `PsdOptions` objektumot, és a tömörítési módszert `Raw`‑ra állítja. Ez a módszer biztosítja, hogy a kép megőrizze teljes minőségét, és tömörítés nélkül legyen mentve.

## Step 5: Save the Image to the Output Stream
```java
psdImage.save(ms, saveOptions);
```

Ez a sor a módosított képet a Step 2‑ben létrehozott `ByteArrayOutputStream`‑be menti, a Step 4‑ben definiált beállításokkal. A `save` metódus gondoskodik a kép megfelelő kódolásáról a beállítások alapján.

## Step 6: Reset the Output Stream
A mentés után a kimeneti adatfolyam a végére került. Vissza kell állítania, hogy az elejéről olvashassa.

```java
ms.reset();
```

Ez a `reset` metódus előkészíti a `ByteArrayOutputStream`‑et, hogy újra az elejéről olvashassa. Olyan, mintha egy szalagot visszatekerne, mielőtt meghallgatná a kedvenc dalát!

## Step 7: Load the Newly Created Image
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Itt betöltjük a képet újra a `ByteArrayOutputStream`‑ből egy új `PsdImage` objektumba. Itt ellenőrizheti az előző lépésben végzett munka eredményét.

## Step 8: Create Graphics Object
A kép további módosításához vagy rendereléséhez szüksége lesz egy graphics objektumra.

```java
Graphics graphics = new Graphics(psdImage);
```

Ez a sor egy `Graphics` objektumot inicializál a `psdImage` használatával. Most már ezt a graphics objektumot használhatja a kép rajzolására vagy manipulálására, ahogy csak szükséges. Olyan, mintha egy ecsetet tartana a kezében!

## Manipulate PSD Layers with Graphics Object
Most, hogy rendelkezik egy **Graphics** példánnyal, **manipulálhatja a PSD rétegeket** — például alakzatok rajzolásával, szöveg hozzáadásával vagy szűrők alkalmazásával egy adott rétegre. A graphics kontextus közvetlenül a pixeladatokon dolgozik, így finomhangolt vezérlést biztosít minden réteg megjelenése felett.

## Common Issues and Solutions
- **NullPointerException a fájl betöltésekor** – ellenőrizze a `dataDir` útvonalat, és győződjön meg a fájlnév helyességéről.  
- **Tömörített kimenet a Raw használata ellenére** – ellenőrizze, hogy a `saveOptions.setCompressionMethod(CompressionMethod.Raw);` hívás megtörtént-e a `save` metódus előtt.  
- **Graphics objektum üresnek tűnik** – győződjön meg róla, hogy a megfelelő `PsdImage` példányon rajzol (használja a betöltöttet, ne az újat, hacsak nem ez a szándék).

## FAQ's
### What is Aspose.PSD?
Az Aspose.PSD egy .NET könyvtár, amely lehetővé teszi a fejlesztők számára, hogy programozott módon hozzanak létre, szerkesszenek és manipuláljanak Photoshop PSD fájlokat és a kapcsolódó képformátumokat.

### How can I download Aspose.PSD for Java?
Letöltheti a [release page](https://releases.aspose.com/psd/java/) oldalról.

### Is there a free trial for Aspose.PSD?
Igen, ingyenes próba verziót szerezhet [itt](https://releases.aspose.com/).

### Can I get support for Aspose.PSD?
Természetesen! Segítséget kérhet a [Aspose support forum](https://forum.aspose.com/c/psd/34) oldalon.

### How can I obtain a temporary license for Aspose.PSD?
Látogasson el a [temporary license page](https://purchase.aspose.com/temporary-license/) oldalra a kezdéshez.

## Frequently Asked Questions

**Q: Can I use the graphics object to edit only one specific layer?**  
A: Igen. A PSD betöltése után válassza ki a kívánt réteget a `psdImage.getLayers().get_Item(index)` segítségével, és adja át a `Graphics` konstruktorának.

**Q: Does the Raw compression method affect file size?**  
A: A Raw módszer a pixeladatokat tömörítés nélkül tárolja, ezért a fájlméret nagyobb lesz, mint a tömörített PSD‑képek esetén, de a képminőség érintetlen marad.

**Q: Is it possible to export the edited PSD to another format (e.g., PNG)?**  
A: Teljesen lehetséges. Használja a megfelelő `Image.save` overload‑ot `PngOptions`‑szel a szerkesztés után — ez a szabványos módja a **export PSD to PNG** folyamatnak.

**Q: What Java version is required?**  
A: Az Aspose.PSD for Java támogatja a JDK 8‑at és az azt követő verziókat.

**Q: How do I release resources after processing?**  
A: Hívja meg a `psdImage.dispose()` metódust, és zárja be a stream‑eket a natív erőforrások felszabadításához.

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}