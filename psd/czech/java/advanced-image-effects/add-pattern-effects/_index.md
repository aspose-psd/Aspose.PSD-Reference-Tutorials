---
title: Přidejte efekty vzoru v Aspose.PSD pro Javu
linktitle: Přidat vzorové efekty
second_title: Aspose.PSD Java API
description: Vylepšete své obrazové vzory Java bez námahy s Aspose.PSD pro Java. Postupujte podle našeho podrobného návodu a přidejte efekty podmanivého vzoru.
weight: 12
url: /cs/java/advanced-image-effects/add-pattern-effects/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidejte efekty vzoru v Aspose.PSD pro Javu

## Zavedení

Ve světě vývoje v Javě je vylepšování obrazových vzorů běžným úkolem a Aspose.PSD pro Javu pro to poskytuje robustní řešení. Tento tutoriál vás provede procesem přidávání vzorových efektů pomocí Aspose.PSD a zajistí, že vaše obrázky vyniknou jedinečnými překryvy a vylepšeními.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Java Development Kit (JDK) nainstalovaný ve vašem systému.
-  Knihovna Aspose.PSD for Java byla stažena a přidána do vašeho projektu. Můžete si jej stáhnout z[Web Aspose.PSD](https://releases.aspose.com/psd/java/).

## Importujte balíčky

Do svého projektu Java naimportujte potřebné balíčky pro práci s Aspose.PSD. Na začátek třídy Java vložte následující kód:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.PatternOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

import java.util.UUID;
```

## Krok 1: Načtěte obrázek

```java
// Načtěte obrázek PSD
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

Ujistěte se, že jste nahradili "YourImagePath" a "YourExportPath" skutečnými cestami ve vašem projektu.

## Krok 2: Extrahujte informace o překryvném vzoru

```java
// Extrahujte informace o překryvném vzoru
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Krok 3: Upravte nastavení překrytí vzoru

```java
// Upravte nastavení překrytí vzorem
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

## Krok 4: Upravte data vzoru

```java
// Upravte data vzoru
PattResource resource;
UUID guid = UUID.randomUUID();
String newPatternName = "$$/Presets/Patterns/Pattern=Some new pattern name\0";

for (int i = 0; i < im.getGlobalLayerResources().length; i++) {
    if (im.getGlobalLayerResources()[i] instanceof PattResource) {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName(newPatternName);
        resource.setPattern(new int[]{Color.getAqua().toArgb(), Color.getRed().toArgb(),
                        Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(),
                        Color.getWhite().toArgb(), Color.getAqua().toArgb()}, new Rectangle(0, 0, 4, 2));
    }
}
```

## Krok 5: Uložte upravený obrázek

```java
// Upravený obrázek uložte
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Krok 6: Ověřte změny

```java
// Ověřte změny v upraveném souboru
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

// Přidejte výrazy, abyste zajistili, že změny byly úspěšně použity
```

## Závěr

Gratuluji! Úspěšně jste se naučili přidávat efekty vzorů pomocí Aspose.PSD pro Javu. Tato výkonná knihovna vám umožňuje vytvářet vizuálně přitažlivé obrázky s přizpůsobenými vzory a poskytuje nekonečné možnosti pro vaše projekty založené na Javě.

## FAQ

### Q1: Mohu použít Aspose.PSD pro Java s jinými knihovnami pro zpracování obrazu Java?

Odpověď 1: Aspose.PSD for Java je navržen tak, aby fungoval nezávisle, ale v případě potřeby jej můžete integrovat s jinými knihovnami Java.

### Q2: Kde najdu podrobnou dokumentaci k Aspose.PSD pro Java?

 A2: Viz[Aspose.PSD pro dokumentaci Java](https://reference.aspose.com/psd/java/) pro komplexní informace.

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro Java?

 A3: Ano, máte přístup k bezplatné zkušební verzi[zde](https://releases.aspose.com/).

### Q4: Jak mohu získat podporu pro Aspose.PSD pro Java?

 A4: Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) pro podporu komunity nebo zvažte nákup plánu podpory.

### Q5: Mohu získat dočasnou licenci pro Aspose.PSD pro Java?

A5: Ano, můžete získat dočasnou licenci[zde](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
