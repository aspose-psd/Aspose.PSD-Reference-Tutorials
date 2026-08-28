---
date: 2026-08-28
description: Přidejte vzor do vrstvy v Javě pomocí Aspose.PSD. Postupujte podle tohoto
  krok‑za‑krokem průvodce, abyste použili stroke layer effect, nakonfigurovali pattern
  resources a efektivně uložili své PSD soubory.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Jak přidat Stroke Layer Pattern v Javě
og_description: Přidejte vzor do vrstvy v Javě pomocí Aspose.PSD. Postupujte podle
  tohoto stručného průvodce, abyste použili stroke layer effect, nakonfigurovali pattern
  resources a efektivně uložili své PSD soubory.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Přidat vzor do vrstvy v Javě – Aspose.PSD tutoriál
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
title: Jak přidat vzor do vrstvy v Javě
url: /cs/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak přidat vzor do vrstvy v Javě

## Úvod
Přidání vzoru do vrstvy v Javě je běžný požadavek, když potřebujete obohatit soubory Photoshop PSD o vlastní efekty tahů. S Aspose.PSD pro Java se tento úkol stává jednoduchým, i když jste v knihovně noví. V tomto tutoriálu se naučíte, jak načíst PSD, vytvořit zdroj vzoru, přiřadit jej k efektu tahu a výsledek uložit – vše s jasnými, krok za krokem instrukcemi.

## Rychlé odpovědi
- **What library is needed?** Aspose.PSD for Java.  
- **How long does implementation take?** Zhruba 10‑15 minut pro základní vzor.  
- **Do I need a license?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Which Java version is supported?** JDK 8 nebo novější.  
- **Can I use this in a web service?** Ano, API je platformově nezávislé a funguje v jakémkoli Java prostředí.

## Co znamená přidání vzoru do vrstvy?
Přidání vzoru do vrstvy znamená přiřazení dlaždicového bitmapového obrazu k efektu tahu nebo výplně, aby se grafika opakovala podél obrysu tvaru. Tato technika se široce používá pro dekorativní okraje, textury a brandingové překryvy, což umožňuje designérům vytvářet konzistentní vizuální motivy bez ručního kreslení každého prvku.

## Proč použít Aspose.PSD pro tento úkol?
Aspose.PSD podporuje **30+ formátů obrázků** a dokáže manipulovat se soubory PSD až do **2 GB** bez načítání celého dokumentu do paměti, což poskytuje rychlý výkon na typickém serverovém hardware. Jeho plynulé API vám umožňuje programově pracovat s efekty vrstev, čímž eliminuje potřebu Photoshopu v automatizovaných pipelinech.

## Požadavky
- Nainstalovaný Java Development Kit (JDK) 8 nebo novější.
- Aspose.PSD for Java – stáhněte jej ze **Aspose.PSD for Java download page**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) a přidejte JAR do classpath vašeho projektu.
- IDE, například IntelliJ IDEA nebo Eclipse, pro úpravu a spouštění ukázkového kódu.
- Ukázkový soubor PSD, který obsahuje vrstvu tvaru, kterou chcete upravit.

## Import balíčků
Nejprve importujte jmenné prostory, které poskytují přístup k objektům PSD, zdrojům a efektům.

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

## Jak přidat vzor do vrstvy v Javě?

Načtěte cílový PSD, vytvořte zdroj vzoru, připojte jej k efektu tahu požadované vrstvy a nakonec soubor uložte. Tento kompletní postup vyžaduje jen několik řádků kódu a funguje s libovolným standardním PSD, který obsahuje vektorovou vrstvu tvaru.

### Krok 1: načíst soubor PSD
Načtení dokumentu vám poskytne přístup k hierarchii vrstev a kolekci efektů.  
`PsdLoadOptions` konfiguruje, jak se PSD čte, zatímco `PsdImage` představuje načtený soubor v paměti.

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

Načtením souboru PSD můžete nyní přistupovat k jeho vrstvám a efektům a manipulovat s nimi.

### Krok 2: připravit nová data vzoru
Vytvořte `PatternResource`, který obsahuje bitmapu, kterou chcete použít jako dlaždicový vzor tahu.  
`PatternResource` je globální zdroj PSD, který ukládá opakující se bitmapový vzor. `Rectangle` určuje hranice vzoru a `UUID` poskytuje jedinečný identifikátor.

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

Tato data vzoru budou použita k vytvoření nového efektu tahu.

### Krok 3: přístup k efektu tahu
Identifikujte vrstvu tvaru, která již má tah, a poté načtěte její objekt `StrokeEffect`.  
`StrokeEffect` představuje efekt tahové vrstvy aplikovaný na vrstvu tvaru.

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

Tím se zajistí, že pracujete se správnou vrstvou a efektem.

### Krok 4: upravit efekt tahu
Nyní aktualizujte vlastnosti tahu tak, aby odkazovaly na nový zdroj vzoru.

#### Aktualizovat vlastnosti efektu tahu
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### Aktualizovat zdroj vzoru
`PattResource` je globální zdroj vrstvy PSD, který ukládá data vzoru.

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

Tyto úryvky nahradí existující vzor tím, který jste poskytli.

### Krok 5: aplikovat nový vzor
`PatternFillSettings` obsahuje nastavení výplně pro efekt tahu založený na vzoru. Potvrďte změny ve vrstvě a zapište aktualizovaný PSD zpět na disk.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

Tím se zajistí, že nový vzor je aplikován správně a soubor je uložen se změnami.

### Krok 6: ověřit změny
Znovu načtěte soubor a zkontrolujte tah, aby bylo potvrzeno, že se vzor zobrazuje podle očekávání.

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

Tento krok ověřuje, že data vzoru byla správně aplikována na efekt tahu.

## Časté problémy a řešení
- **Vzor není viditelný:** Ujistěte se, že DPI obrázku vzoru odpovídá rozlišení PSD a že příznak `Enabled` tahu je nastaven na `true`.  
- **Velké soubory PSD způsobují OutOfMemoryError:** Použijte `PsdImage.load(..., LoadOptions)` s `LoadOptions.setLoadAllLayers(false)`, aby se vrstvy načítaly na požádání.  
- **Vybrána nesprávná vrstva:** Ověřte index nebo název vrstvy před přístupem k jejím efektům; můžete vypsat `psdImage.getLayers()`, abyste získali seznam dostupných vrstev.

## Často kladené otázky

**Q: Co je Aspose.PSD pro Java?**  
A: Aspose.PSD pro Java je knihovna, která umožňuje vývojářům programově vytvářet, upravovat a převádět soubory PSD (Photoshop Document).

**Q: Mohu použít Aspose.PSD pro Java v komerčním projektu?**  
A: Ano, můžete jej použít v komerčních projektech. Licenci si můžete zakoupit na **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).

**Q: Je k dispozici bezplatná zkušební verze Aspose.PSD pro Java?**  
A: Ano, můžete si stáhnout bezplatnou zkušební verzi ze **Aspose releases page**([Aspose releases page](https://releases.aspose.com/)).

**Q: Jak mohu získat podporu pro Aspose.PSD pro Java?**  
A: Podporu můžete získat na fóru komunity Aspose **zde**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)).

**Q: Jaké jsou systémové požadavky pro Aspose.PSD pro Java?**  
A: Potřebujete nainstalovaný JDK a IDE pro vývoj. Knihovna podporuje Windows, Linux a macOS.

## Závěr
Nyní jste se naučili, jak přidat vzor do vrstvy v Javě pomocí Aspose.PSD. Dodržením výše uvedených kroků můžete programově vylepšovat soubory PSD pomocí vlastních vzorů tahů, automatizovat workflow brandingu a integrovat zpracování grafiky do jakékoli aplikace založené na Javě. Prozkoumejte další funkce Aspose.PSD, jako je slučování vrstev, úpravy barev a export do PNG nebo JPEG, abyste dále rozšířili svůj nástroj pro zpracování obrázků.

---

**Poslední aktualizace:** 2026-08-28  
**Testováno s:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose

## Související tutoriály

- [Vykreslit vrstvu výplně vzoru v souborech PSD](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Překrytí vzoru PSD: Přidat efekty pomocí Aspose.PSD pro Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Jak změnit barvu tahu v Javě pomocí Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}