---
date: 2026-01-17
description: Tanulja meg, hogyan adjon hozzá vonalmintát Java-ban az Aspose.PSD for
  Java segítségével. Kövesse ezt a lépésről‑lépésre útmutatót, hogy gyorsan javítsa
  PSD képeit.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Hogyan adjon hozzá vonalmintát Java-ban az Aspose.PSD használatával
url: /hu/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan adjunk hozzá Stroke Pattern Java-t az Aspose.PSD-hez

## Bevezetés
Ha **stroke pattern java** hozzáadására van szüksége egy Photoshop fájlhoz, az Aspose.PSD for Java meglepően egyszerű megoldást kínál. Akár grafikai tervező eszközt épít, akár kötegelt szerkesztéseket automatizál, vagy csak kísérletezik réteg‑effektekkel, ez a bemutató minden lépésen végigvezet – a PSD betöltésétől az új minta ellenőrzéséig. Merüljünk el, és nézzük meg, milyen gyorsan gazdagíthatja képeit.

## Gyors válaszok
- **Milyen könyvtárra van szükségem?** Aspose.PSD for Java  
- **Melyik Java verzió támogatott?** JDK 8 vagy újabb  
- **Szükségem van licencre a teszteléshez?** Egy ingyenes próba verzió elegendő fejlesztéshez; licenc szükséges a termeléshez  
- **Mennyi időt vesz igénybe a megvalósítás?** Körülbelül 10‑15 perc egy alapvető mintás vonalhoz  
- **Újra felhasználhatom a mintát több rétegen?** Igen, egyszerűen rendelje hozzá ugyanazt a `PattResource`‑t a többi réteghez  

## Mi az a stroke pattern hozzáadása Java-ban?
A stroke pattern hozzáadása Java-ban azt jelenti, hogy egy egyedi kitöltést (gyakran ismétlődő bitmapet) alkalmazunk egy réteg vonal‑effektusára. Ez a technika lehetővé teszi stilizált körvonalak létrehozását – gondoljunk csak szaggatott vonalakra, tégla textúrára vagy egyedi grafikus keretre – közvetlenül egy PSD fájlban, Photoshop megnyitása nélkül.

## Miért használjuk az Aspose.PSD-t a stroke pattern hozzáadásához Java-ban?
- **Teljes PSD hűség** – Minden réteg‑effektus, erőforrás és keverési mód megmarad.  
- **Nincs szükség natív Photoshopra** – Bármely operációs rendszeren működik JDK‑val.  
- **Programozott vezérlés** – Automatizálja a kötegelt feldolgozást vagy integrálja szerver‑oldali szolgáltatásokba.  
- **Gazdag API** – Hozzáférés globális erőforrásokhoz, mintázat kitöltésekhez és keverési módokhoz egyetlen folyékony felületen.

## Előfeltételek
- **Java Development Kit (JDK)** – Győződjön meg róla, hogy JDK 8 vagy újabb telepítve van.  
- **Aspose.PSD for Java** – Töltse le a könyvtárat [itt](https://releases.aspose.com/psd/java/), és adja hozzá a JAR-t a projekt osztályútvonalához.  
- **IDE** – IntelliJ IDEA, Eclipse vagy bármelyik kedvenc szerkesztő.

## Csomagok importálása
Először importálja a PSD fájlok, színek, téglalapok és vonal‑effektek kezeléséhez szükséges osztályokat.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```

## 1. lépés: PSD fájl betöltése
Töltse be a forrás PSD‑t, hogy dolgozhasson a rétegekkel és erőforrásokkal.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## 2. lépés: Új minta adat előkészítése
Hozzon létre egy egyszerű 4 × 4 pixeles mintát, amelyet a vonalhoz fog használni.

```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```

## 3. lépés: A Stroke effektus elérése
Keresse meg a stroke effektust a cél rétegen (ebben a példában a negyedik rétegen).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## 4. lépés: A Stroke effektus módosítása
### Stroke effektus tulajdonságainak frissítése
Állítsa be az átlátszóságot és a keverési módot, hogy lássa az új minta vizuális hatását.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### A minta erőforrás frissítése
Cserélje le a meglévő globális mintá erőforrást az újonnan létrehozottra.

```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```

## 5. lépés: Az új minta alkalmazása
Kösse össze a frissített mintá erőforrást a stroke effektussal, majd mentse a PSD‑t.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## 6. lépés: A változások ellenőrzése
Töltse be újra a fájlt, és ellenőrizze, hogy az új minta, átlátszóság és keverési mód helyesen alkalmazva van‑e.

```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```

## Gyakori problémák és megoldások
| Probléma | Ok | Megoldás |
|----------|----|----------|
| A minta nem jelenik meg | Helytelen `PatternId` hivatkozás | Győződjön meg arról, hogy a `PattResource`‑on beállított `PatternId` megegyezik a `PatternFillSettings`‑ben használtal. |
| A stroke eltűnik mentés után | Az átlátszóság 0-ra van állítva vagy az effektus rejtett | Ellenőrizze, hogy a `setOpacity` 0‑255 között van, és az `isVisible()` `true` értéket ad. |
| Váratlan színek | Blend mód eltérés | Használja a `BlendMode.Color` (vagy más mód) értéket, amely megfelel a tervezési szándékának. |

## Gyakran ismételt kérdések
### Mi az Aspose.PSD for Java?
Az Aspose.PSD for Java egy könyvtár, amely lehetővé teszi a fejlesztők számára, hogy programozottan hozzanak létre, szerkesszenek és konvertáljanak PSD (Photoshop Document) fájlokat.

### Használhatom az Aspose.PSD for Java‑t kereskedelmi projektben?
Igen, kereskedelmi projektekben is használható. Licencet vásárolhat [itt](https://purchase.aspose.com/buy).

### Van ingyenes próba verzió az Aspose.PSD for Java‑hoz?
Igen, letölthető egy ingyenes próba verzió [itt](https://releases.aspose.com/).

### Hogyan kaphatok támogatást az Aspose.PSD for Java‑hoz?
Támogatást kaphat az Aspose közösségi fórumokon [itt](https://forum.aspose.com/c/psd/34).

### Mik a rendszerkövetelmények az Aspose.PSD for Java‑hoz?
Szüksége van telepített JDK‑ra és fejlesztői IDE‑re. A könyvtár több operációs rendszert támogat, beleértve a Windows, Linux és macOS platformokat.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Utolsó frissítés:** 2026-01-17  
**Tesztelve ezzel:** Aspose.PSD for Java 24.12 (a legújabb a írás időpontjában)  
**Szerző:** Aspose