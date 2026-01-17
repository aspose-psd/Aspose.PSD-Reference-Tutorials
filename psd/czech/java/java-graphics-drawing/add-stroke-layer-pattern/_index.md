---
date: 2026-01-17
description: Naučte se, jak přidat vzor tahů v Javě pomocí Aspose.PSD pro Java. Postupujte
  podle tohoto krok‑za‑krokem průvodce a rychle vylepšete své PSD obrázky.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Jak přidat vzor tahu v Javě pomocí Aspose.PSD
url: /cs/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak přidat vzor obrysu v Javě pomocí Aspose.PSD

## Úvod
Pokud potřebujete **add stroke pattern java** do souboru Photoshop, Aspose.PSD for Java to dělá překvapivě jednoduše. Ať už vytváříte nástroj pro grafický design, automatizujete hromadné úpravy, nebo jen experimentujete s efekty vrstev, tento tutoriál vás provede každým krokem – od načtení PSD až po ověření nového vzoru. Ponořme se a podívejme se, jak rychle můžete vylepšit své obrázky.

## Rychlé odpovědi
- **Jakou knihovnu potřebuji?** Aspose.PSD for Java  
- **Která verze Javy je podporována?** JDK 8 nebo novější  
- **Potřebuji licenci pro testování?** Bezplatná zkušební verze funguje pro vývoj; licence je vyžadována pro produkci  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní vzor obrysu  
- **Mohu vzor použít na více vrstev?** Ano, stačí přiřadit stejný `PattResource` ostatním vrstvám  

## Co je add stroke pattern java?
Přidání vzoru obrysu v Javě znamená aplikaci vlastního výplně (často opakující se bitmapy) na efekt obrysu vrstvy. Tato technika vám umožní vytvořit stylizované obrysy – představte si čárkovanou čáru, cihlovou texturu nebo vlastní grafický okraj – přímo v souboru PSD bez nutnosti otevírat Photoshop.

## Proč použít Aspose.PSD pro add stroke pattern java?
- **Plná věrnost PSD** – Všechny efekty vrstev, zdroje a režimy prolnutí jsou zachovány.  
- **Není vyžadován nativní Photoshop** – Funguje na jakémkoli OS s JDK.  
- **Programová kontrola** – Automatizujte hromadné zpracování nebo integrujte do serverových služeb.  
- **Bohaté API** – Př k globálním zdrojům, výplním vzorů a režimům prolnutí v jedné plynulé rozhraní.

## Požadavky
- **Java Development Kit (JDK)** – Ujistěte se, že máte nainstalovaný JDK 8 nebo novější.  
- **Aspose.PSD for Java** – Stáhněte knihovnu z [zde](https://releases.aspose.com/d/java/) a přidejte JAR do classpath vašeho projektu.  
- **IDE** – IntelliJ IDEA, Eclipse nebo jakýkoli editor, který preferujete.

## Import balíčků
Nejprve importujte třídy, které budete potřebovat pro práci se soubory PSD, barvami, obdélníky a efekty obrysu.

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

## Krok 1: Načtení souboru PSD
Načtěte zdrojový PSD, abyste mohli pracovat s jeho vrstvami a zdroji.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Krok 2: Připravte nová data vzoru
Vytvořte jednoduchý 4 × 4 pixelový vzor, který bude použit pro obrys.

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

## Krok 3: Přístup k efektu obrysu
Najděte efekt obrysu na cílové vrstvě (v tomto příkladu čtvrtá vrstva).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Krok 4: Úprava efektu obrysu
### Aktualizace vlastností efektu obrysu
Upravte neprůhlednost a režim prolnutí, abyste viděli vizuální dopad nového vzoru.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Aktualizace zdroje vzoru
Nahraďte existující globální zdroj vzoru tím, který jste právě vytvořili.

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

## Krok 5: Použití nového vzoru
Připojte aktualizovaný zdroj vzoru k efektu obrysu a uložte PSD.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Krok 6: Ověření změn
Znovu načtěte soubor a potvrďte, že nový vzor, neprůhlednost a režim prolnutí jsou správně aplikovány.

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

## Časté problémy a řešení
| Problém | Příčina | Řešení |
|---------|---------|--------|
| Vzor se nezobrazuje | Špatná reference `PatternId` | Ujistěte se, že `PatternId` nastavený na `PattResource` odpovídá tomu, který je použit v `PatternFillSettings`. |
| Obrys zmizí po uložení | Neprůhlednost nastavena na 0 nebo efekt skrytý | Zkontrolujte, že `setOpacity` je v rozmezí 0‑255 a `isVisible()` vrací `true`. |
| Neočekávané barvy | Neshoda režimu prolnutí | Použijte `BlendMode.Color` (nebo jiný režim), který odpovídá vašemu designovému záměru. |

## Často kladené otázky
### Co je Aspose.PSD for Java?
Aspose.PSD for Java je knihovna, která umožňuje vývojářům programově vytvářet, upravovat a konvertovat soubory PSD (Photoshop Document).

### Mohu použít Aspose.PSD for Java v komerčním projektu?
Ano, můžete ji použít v komerčních projektech. Licenci můžete zakoupit [zde](https://purchase.aspose.com/buy).

### Je k dispozici bezplatná zkušební verze pro Aspose.PSD for Java?
Ano, můžete si stáhnout bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Jak mohu získat podporu pro Aspose.PSD for Java?
Podporu můžete získat na fórech komunity Aspose [zde](https://forum.aspose.com/c/psd/34).

### Jaké jsou systémové požadavky pro Aspose.PSD for Java?
Potřebujete nainstalovaný JDK a IDE pro vývoj. Knihovna podporuje více operačních systémů, včetně Windows, Linuxu a macOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-17  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose