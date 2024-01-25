---
title: Přidejte barvu vrstvy tahu v Aspose.PSD pro Javu
linktitle: Přidat barvu vrstvy tahu
second_title: Aspose.PSD Java API
description: Prozkoumejte sílu Aspose.PSD pro Java pomocí našeho podrobného průvodce přidáním barvy vrstvy tahu. Vylepšete své grafické návrhy bez námahy.
type: docs
weight: 14
url: /cs/java/advanced-image-effects/add-stroke-layer-color/
---
## Úvod

Odemkněte potenciál grafického designu vaší Java aplikace s Aspose.PSD. V tomto tutoriálu se ponoříme do fascinujícího světa přidávání barvy vrstvy tahu pomocí Aspose.PSD pro Java. Vylepšete svou grafiku tahy, které praskají, a bez námahy vytvářejte vizuálně přitažlivé návrhy.

## Předpoklady

Než se vydáte na tuto kreativní cestu, ujistěte se, že máte splněny následující předpoklady:

-  Knihovna Aspose.PSD: Stáhněte a nastavte knihovnu Aspose.PSD podle pokynů v[dokumentace](https://reference.aspose.com/psd/java/).

- Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovanou Javu.

- Integrované vývojové prostředí (IDE): Vyberte si IDE podle svých preferencí; Oblíbenými volbami jsou Eclipse nebo IntelliJ.

## Importujte balíčky

Začněme importem potřebných balíčků, aby se stalo kouzlo Aspose.PSD.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Krok 1: Nastavte svůj projekt

Začněte vytvořením nového projektu Java ve vámi preferovaném IDE. Ujistěte se, že knihovna Aspose.PSD je přidána do vašeho projektu.

## Krok 2: Načtěte soubor PSD

Načtěte soubor PSD pomocí Aspose.PSD, což umožňuje načítání zdrojů efektů.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Krok 3: Přístup k vrstvě tahu

Přístup k vrstvě efektu tahu v souboru PSD.

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Krok 4: Ověřte vlastnosti tahu

Ujistěte se, že vlastnosti zdvihu jsou podle očekávání.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Krok 5: Nastavte barvu a krytí

Upravte barvu a krytí vrstvy tahu.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Krok 6: Uložte upravené PSD

Uložte upravený soubor PSD s nově přidanou barvou vrstvy tahu.

```java
im.save(exportPath);
```

## Závěr

Gratulujeme! Úspěšně jste přidali barvu vrstvy tahu do svého souboru PSD pomocí Aspose.PSD for Java. Experimentujte s různými barvami a nastaveními, abyste své grafické návrhy oživili.

## FAQ

### Q1: Mohu používat Aspose.PSD s jinými grafickými knihovnami Java?

Odpověď 1: Ano, Aspose.PSD lze integrovat s jinými grafickými knihovnami Java pro vylepšenou funkčnost.

### Q2: Je Aspose.PSD kompatibilní s nejnovějším formátem souborů PSD?

A2: Rozhodně! Aspose.PSD drží krok s nejnovějšími specifikacemi formátu souborů PSD a zajišťuje kompatibilitu.

### Q3: Jak mohu zpracovat výjimky při používání Aspose.PSD?

 A3: Viz[Fórum podpory](https://forum.aspose.com/c/psd/34) za pomoc při zpracování výjimek a odstraňování problémů.

### Q4: Mohu vyzkoušet Aspose.PSD před nákupem?

 A4: Určitě! Chyť a[zkušební verze zdarma](https://releases.aspose.com/) prozkoumat funkce Aspose.PSD, než se zavážete.

### Q5: Kde mohu získat dočasnou licenci pro Aspose.PSD?

 A5: Získejte a[dočasná licence](https://purchase.aspose.com/temporary-license/) pro Aspose.PSD k vyhodnocení jeho schopností ve vašich projektech.