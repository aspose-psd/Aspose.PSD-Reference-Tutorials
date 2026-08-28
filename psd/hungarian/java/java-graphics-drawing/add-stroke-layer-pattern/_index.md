---
date: 2026-08-28
description: Adjon mintát a réteghez Java-ban az Aspose.PSD segítségével. Kövesse
  ezt a lépésről‑lépésre útmutatót a stroke layer effect alkalmazásához, a pattern
  erőforrások konfigurálásához, és a PSD fájlok hatékony mentéséhez.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Hogyan adjon Stroke Layer Pattern-et Java-ban
og_description: Minta hozzáadása a réteghez Java-ban az Aspose.PSD használatával.
  Kövesse ezt a tömör útmutatót a stroke layer effect alkalmazásához, a pattern erőforrások
  konfigurálásához, és a PSD fájlok hatékony mentéséhez.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Minta hozzáadása a réteghez Java-ban – Aspose.PSD tutorial
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Hogyan adjon mintát a réteghez Java-ban
url: /hu/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan adjon mintát a réteghez Java-ban

## Bevezetés
A minták hozzáadása egy réteghez Java-ban gyakori igény, amikor Photoshop PSD fájlokat szeretnénk egyedi vonalhatásokkal gazdagítani. Az Aspose.PSD for Java-val ez a feladat egyszerűvé válik, még ha újonc is vagy a könyvtárban. Ebben az oktatóanyagban megtanulod, hogyan tölts be egy PSD-t, hozz létre egy minta erőforrást, csatold egy vonalhatáshoz, és mentsd el az eredményt – mindezt világos, lépésről‑lépésre útmutatóval.

## Gyors válaszok
- **Melyik könyvtár szükséges?** Aspose.PSD for Java.  
- **Mennyi időt vesz igénybe a megvalósítás?** Körülbelül 10‑15 perc egy alap mintához.  
- **Szükségem van licencre?** A ingyenes próba verzió fejlesztéshez működik; a kereskedelmi licenc szükséges a termeléshez.  
- **Melyik Java verzió támogatott?** JDK 8 vagy újabb.  
- **Használhatom ezt webszolgáltatásban?** Igen, az API platform‑független és bármely Java környezetben működik.

## Mi az a minta hozzáadása egy réteghez?
A minták hozzáadása egy réteghez azt jelenti, hogy egy csempézett bitmapet rendelünk egy vonal- vagy kitöltés‑hatáshoz, így a grafika ismétlődik a forma körvonala mentén. Ezt a technikát gyakran használják dekoratív szegélyek, textúrák és márka‑átfedések létrehozására, lehetővé téve a tervezők számára, hogy konzisztens vizuális témákat hozzanak létre anélkül, hogy minden elemet kézzel kellene megrajzolniuk.

## Miért használja az Aspose.PSD-t ehhez a feladathoz?
Az Aspose.PSD **30+ képformátumot** támogat, és képes PSD fájlokat akár **2 GB** méretben is kezelni anélkül, hogy a teljes dokumentumot a memóriába töltené, gyors teljesítményt biztosítva a tipikus szerverhardveren. A folyékony API lehetővé teszi a réteg‑hatások programozott kezelését, kiküszöbölve a Photoshop szükségességét az automatizált folyamatokban.

## Előfeltételek
Mielőtt elkezdenéd, győződj meg róla, hogy rendelkezel:
- Java Development Kit (JDK) 8 vagy újabb telepítve.
- Aspose.PSD for Java – töltsd le a **[Aspose.PSD for Java letöltési oldal](https://releases.aspose.com/psd/java/)**‑ról, és add hozzá a JAR‑t a projekted classpath‑jához.
- Egy IDE, például IntelliJ IDEA vagy Eclipse a minta kód szerkesztéséhez és futtatásához.
- Egy minta PSD fájl, amely tartalmaz egy alakzatréteget, amelyet módosítani szeretnél.

## Csomagok importálása
Először importáld a névtereket, amelyek hozzáférést biztosítanak a PSD objektumokhoz, erőforrásokhoz és hatásokhoz.

```
// No actual code block is added to preserve original placeholders.
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
```

## Hogyan adjon mintát a réteghez Java-ban?

Töltsd be a cél PSD-t, hozz létre egy minta erőforrást, csatold a kívánt réteg vonalhatásához, majd mentsd el a fájlt. Ez az átfogó folyamat csak néhány kódsort igényel, és bármely szabványos PSD-vel működik, amely tartalmaz vektoros alakzatréteget.

### 1. lépés: PSD fájl betöltése
A dokumentum betöltése hozzáférést biztosít a réteg‑hierarchiához és a hatás‑gyűjteményhez.  
A `PsdLoadOptions` beállítja, hogyan olvassuk be a PSD‑t, míg a `PsdImage` a memóriában lévő betöltött fájlt képviseli.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

A PSD fájl betöltésével most már hozzáférhetsz és módosíthatod a rétegeket és hatásokat.

### 2. lépés: új minta adat előkészítése
Hozz létre egy `PatternResource`‑t, amely a bitmapet tárolja, amit csempézni szeretnél vonalmintaként.  
A `PatternResource` egy PSD globális erőforrás, amely ismétlődő bitmap mintát tárol. A `Rectangle` meghatározza a minta határait, az `UUID` pedig egyedi azonosítót biztosít.

```
// Placeholder for original code.
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
```

Ez a minta adat lesz felhasználva az új vonalhatás létrehozásához.

### 3. lépés: a vonalhatás elérése
Azonosítsd azt az alakzatréteget, amely már rendelkezik vonallal, majd szerezd meg a `StrokeEffect` objektumát.  
A `StrokeEffect` a vonal‑réteg‑hatást képviseli, amely egy alakzatrétegre van alkalmazva.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

Ez biztosítja, hogy a megfelelő réteggel és hatással dolgozol.

### 4. lépés: a vonalhatás módosítása
Most frissítsd a vonal tulajdonságait, hogy az új minta erőforrást használja.

#### Vonalhatás tulajdonságainak frissítése
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### A minta erőforrás frissítése
A `PattResource` egy PSD globális réteg‑erőforrás, amely minta adatot tárol.

```
// Placeholder for original code.
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
```

Ezek a kódrészletek lecserélik a meglévő mintát a megadott útra.

### 5. lépés: az új minta alkalmazása
A `PatternFillSettings` tartalmazza a kitöltési beállításokat egy minta‑alapú vonalhatáshoz. Vidd véghez a módosításokat a rétegen, és írd vissza a frissített PSD‑t a lemezre.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

Ez biztosítja, hogy az új minta helyesen legyen alkalmazva, és a fájl a változásokkal mentésre kerüljön.

### 6. lépés: a változások ellenőrzése
Töltsd be újra a fájlt, és ellenőrizd a vonalat, hogy megbizonyosodj róla, a minta a várt módon jelenik‑e meg.

```
// Placeholder for original code.
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
```

Ez a lépés ellenőrzi, hogy a minta adat helyesen lett‑e alkalmazva a vonalhatáshoz.

## Gyakori problémák és hibaelhárítás
- **A minta nem látható:** Győződj meg arról, hogy a minta kép DPI-je megegyezik a PSD felbontásával, és hogy a vonal `Enabled` jelzője `true` értékre van állítva.  
- **Nagy PSD fájlok OutOfMemoryError-t okoznak:** Használja a `PsdImage.load(..., LoadOptions)`‑t a `LoadOptions.setLoadAllLayers(false)` beállítással, hogy igény szerint töltse be a rétegeket.  
- **Helytelen réteg kiválasztva:** Ellenőrizze a réteg indexét vagy nevét a hatások elérése előtt; felsorolhatja a `psdImage.getLayers()`‑t a rendelkezésre álló rétegek listázásához.

## Gyakran feltett kérdések

**Q: Mi az az Aspose.PSD for Java?**  
A: Az Aspose.PSD for Java egy könyvtár, amely lehetővé teszi a fejlesztők számára, hogy programozottan hozzanak létre, szerkesszenek és konvertáljanak PSD (Photoshop Document) fájlokat.

**Q: Használhatom ezt az Aspose.PSD for Java‑t kereskedelmi projektben?**  
A: Igen, használhatod kereskedelmi projektekben. Licencet vásárolhatsz a **[Aspose vásárlási oldal](https://purchase.aspose.com/buy)**‑ról.

**Q: Elérhető ingyenes próba verzió az Aspose.PSD for Java‑hoz?**  
A: Igen, letöltheted az ingyenes próba verziót a **[Aspose kiadási oldal](https://releases.aspose.com/)**‑ról.

**Q: Hogyan kaphatok támogatást az Aspose.PSD for Java‑hoz?**  
A: Támogatást kaphatsz az Aspose közösségi fórumokon **[itt](https://forum.aspose.com/c/psd/34)**.

**Q: Mik a rendszerkövetelmények az Aspose.PSD for Java‑hoz?**  
A: Szükséged van egy telepített JDK‑ra és egy IDE‑re a fejlesztéshez. A könyvtár támogatja a Windows, Linux és macOS rendszereket.

## Következtetés
Most már megtanultad, hogyan adj mintát egy réteghez Java‑ban az Aspose.PSD segítségével. A fenti lépések követésével programozottan gazdagíthatod a PSD fájlokat egyedi vonalmintákkal, automatizálhatod a márka‑folyamatokat, és integrálhatod a grafikai feldolgozást bármely Java‑alapú alkalmazásba. Fedezd fel az Aspose.PSD további funkcióit, például a rétegek egyesítését, színkorrekciókat és a PNG vagy JPEG formátumba való exportálást, hogy tovább bővítsd a képfeldolgozó eszköztáradat.

---

**Utolsó frissítés:** 2026-08-28  
**Tesztelve ezzel:** Aspose.PSD 24.11 for Java  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [Minta kitöltés réteg renderelése PSD fájlok](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Minta átfedés PSD: hatások hozzáadása az Aspose.PSD for Java‑val](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Hogyan változtassuk meg a vonal színét Java-ban az Aspose.PSD segítségével](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}