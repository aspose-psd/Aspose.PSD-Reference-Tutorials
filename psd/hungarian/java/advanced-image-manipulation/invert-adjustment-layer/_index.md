---
date: 2026-11-04
description: Ismerje meg, hogyan használja az Aspose.PSD for Java-t invert adjustment
  layer alkalmazásához, PSD képek kötegelt feldolgozásához, és negatív kép PSD fájlok
  létrehozásához.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Hogyan használja az Aspose.PSD for Java-t invert adjustment layer
  hozzáadásához, PSD képek kötegelt feldolgozásához, és negatív kép PSD létrehozásához.
  Kövesse a lépésről‑lépésre útmutatót.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Hogyan használja az Aspose.PSD-t invert adjustment layer hozzáadásához Java-ban
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Hogyan használja az Aspose.PSD-t invert adjustment layer hozzáadásához Java-ban
url: /hu/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan használjuk az Aspose.PSD-t invertálás beállítási réteg hozzáadásához Java-ban

## Bevezetés

Ha egy robusztus **image processing java library**-t keres, az Aspose.PSD for Java az egyik legváltozatosabb lehetőség a piacon. Ebben az útmutatóban megmutatjuk, **how to use Aspose**-t, hogy hogyan szúrjon be egy **Invert Adjustment Layer**-t egy PSD fájlba, hogyan halmozza más beállításokkal, és akár több tucat fájlon is végrehajtsa a műveletet. Akár kötegelt feldolgozó eszközt, szerver‑oldali képszolgáltatást vagy egyetlen képszerkesztőt épít, az alábbi lépések segítenek a forrás PSD‑t egy teljesen szerkeszthető negatív képpé alakítani percek alatt.

## Gyors válaszok
- **Mi a Invert Adjustment Layer funkciója?** Az kiválasztott területen minden RGB értéket megfordít, a képet fotónegatívvá alakítva.  
- **Melyik könyvtár biztosítja ezt a funkciót?** Aspose.PSD, a leading **image processing java library**.  
- **Hozzáadhatom más beállításokhoz?** Igen – **apply multiple adjustment layers** használható, például Brightness/Contrast, Hue/Saturation, és továbbiak.  
- **Szükségem van licencre fejlesztéshez?** Elérhető egy ingyenes próba; licenc szükséges a termelésben való használathoz.  
- **Mennyi időt vesz igénybe a megvalósítás?** Általában 10 percnél kevesebb egy alap esetben.

## Mi az Invert Adjustment Layer?

Az Invert Adjustment Layer egy nem destruktív szerkesztés, amely megfordítja az általa érintett minden pixel színértékét. Mivel a rétegek tetején helyezkedik el, a láthatóságát be‑ vagy kikapcsolhatja, illetve átrendezheti anélkül, hogy véglegesen módosítaná az eredeti képadatokat. Ez a leggyorsabb mód a **create negative image PSD** fájlok létrehozására vagy egy klasszikus filmnegatív hatás elérésére.

## Miért használja az Aspose.PSD-t image processing java library‑ként?

Az Aspose.PSD **200+ PSD features** támogat, képes Photoshop fájlok olvasására és írására Photoshop nélkül, és több száz oldalas dokumentumokat dolgoz fel kevesebb, mint 500 MB heap memória használatával. Bármely Java futtatókörnyezeten (Java 6+) fut, így ideális **batch process psd images** Windows, Linux vagy macOS szervereken.

## Előfeltételek

Az indulás előtt győződjön meg róla, hogy rendelkezik:

1. **Aspose.PSD for Java** – töltse le a legújabb JAR‑t a hivatalos oldalról [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 vagy újabb telepítve és beállítva a `PATH`‑ban.  

Most már készen áll a kód írására.

## Csomagok importálása

A `PsdImage` osztály egy teljes Photoshop dokumentumot képvisel a memóriában, míg az adjustment‑layer osztályok a `com.aspose.psd.layers.adjustments` csomagban találhatók.

A `PsdImage` osztály az Aspose.PSD legfelső szintű objektuma, amely egy PSD fájl szerkezetét és pixeladatait foglalja magába. Importálja a névtereket, így képes lesz PSD fájlokat betölteni, szerkeszteni és menteni.

## 1. lépés: dokumentum könyvtár beállítása

Adja meg azt a mappát, amely a forrás PSD fájlt tartalmazza, és ahová a kimenetet menteni szeretné. Az abszolút útvonalak használata elkerüli a `NullPointerException`-t, ha a munkakönyvtár megváltozik.

## 2. lépés: PSD fájl betöltése

Töltse be a forrásfájlt egy `PsdImage` objektumba. Ez az objektum a teljes réteg-hierarchiát tárolja a memóriában, lehetővé téve a nem destruktív szerkesztéseket.

A `PsdImage` osztály egy statikus `load` metódust biztosít, amely beolvassa a fájlfejlécet, ellenőrzi a formátumot, és egy memóriában lévő reprezentációt hoz létre a további manipulációhoz.

## 3. lépés: invertálás beállítási réteg hozzáadása

Hívja meg a beépített metódust, hogy egy Invert Adjustment Layer‑t szúrjon be a jelenlegi rétegstack tetejére. Később további rétegeket (pl. Brightness, Hue) adhat hozzá, hogy egyetlen munkafolyamatban **apply multiple adjustment layers** használhassa.

`addInvertAdjustmentLayer()` egy Invert Adjustment Layer‑t ad a PSD réteggyűjteményéhez.

## 4. lépés: kimenet mentése

Mentse a módosított PSD‑t a lemezre.  

`save()` a megadott útvonalra írja a PSD fájlt, beleértve az összes réteget és metaadatot.

A mentés ugyanazt a `save` metódust használja, amely a teljes dokumentumot, az összes beállítási réteget, maszkot és metaadatot a megadott formátumba írja.

### Mi történt?

A PSD fájl betöltésre került egy `PsdImage` objektumba, egy `InvertAdjustmentLayer` lett létrehozva és a legfelső rétegként hozzáadva, majd a dokumentum mentésre került. Ez a sorrend megőrzi az eredeti képadatokat, miközben egy nem destruktív invertálási hatást ad hozzá, amely később be‑ vagy kikapcsolható, illetve átrendezhető.

Most sikeresen használta az Aspose.PSD‑t, egy **image processing java library**‑t, egy PSD fájl manipulálásához.

## Hogyan kötegelt feldolgozást végez PSD képeken invertálás beállítással?

Töltse be minden fájlt egy `for` ciklusban, alkalmazza ugyanazokat a lépéseket, és minden iterációban hívja meg a `save` metódust. Mivel az Aspose.PSD fájlokat streaming módon dolgozza fel, **hundreds of PSDs** kezelhet anélkül, hogy a memóriahasználat 300 MB fölé nőne, ha ugyanazt a `PsdImage` példányt újrahasználja.

## Hogyan konvertáljunk egy PSD-t negatív képpé?

Adja hozzá az Invert Adjustment Layer‑t legfelső elemként, majd mentse a dokumentumot – ez a művelet egyenértékű a **convert PSD to negative**‑val. Később letilthatja vagy törölheti a réteget, hogy az eredeti megjelenésre térjen vissza a forrásfájl újratöltése nélkül.

## Gyakori problémák és tippek

| Issue | Cause | Solution |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | Helytelen fájlútvonal vagy hiányzó fájl | Ellenőrizze a `dataDir` és a fájlnév helyességét; teszteléshez használjon abszolút útvonalakat |
| **Layer order not as expected** | Rétegek hozzáadása a meglévők után megváltoztatja a stack-et | Helyezze be az invert réteget a többi beállítás előtt, vagy rendezze át a `psdImage.getLayers().move()` segítségével |
| **Performance slowdown on large PSDs** | Nagyon nagy fájlok betöltése a memóriába | Növelje a JVM heap méretét (`-Xmx2g`) vagy dolgozza fel a fájlokat darabokban a `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` használatával |

## Gyakran ismételt kérdések

**Q: Kompatibilis az Aspose.PSD minden Java verzióval?**  
A: Igen, támogatja a Java 6.0‑t és újabbakat, beleértve a Java 8, 11 és 17 verziókat.

**Q: Alkalmazhatok több beállítási réteget egyetlen műveletben?**  
A: Természetesen. Az invert réteg hozzáadása után meghívhatja a `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()` stb. metódusokat a hatások halmozásához.

**Q: Hol találom a teljes API referenciát?**  
A: A teljes dokumentáció elérhető [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: Van ingyenes próba az Aspose.PSD-hez?**  
A: Igen, letölthet egy próbaverziót [Aspose.PSD trial download](https://releases.aspose.com/).

**Q: Hogyan szerezhetek ideiglenes licencet teszteléshez?**  
A: Kérjen ideiglenes licencet [temporary license request page](https://purchase.aspose.com/temporary-license/).

**Utoljára frissítve:** 2026-11-04  
**Tesztelve:** Aspose.PSD 24.12 for Java  
**Szerző:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## Kapcsolódó oktatóanyagok

- [Szint beállítási réteg hozzáadása PSD fájlokhoz Aspose.PSD for Java használatával](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [Hogyan adjunk hozzá Adjustment Layer – Channel Mixer-t PSD-hez (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [Hogyan szerkesszünk PSD-t – Curves Adjustment Layer hozzáadása Java-val](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}