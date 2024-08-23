---
title: Použijte filtry Median a Wiener s Aspose.PSD pro Java
linktitle: Použijte střední a Wienerův filtr
second_title: Aspose.PSD Java API
description: Prozkoumejte sílu zpracování obrazu v Javě s Aspose.PSD. Naučte se, jak aplikovat filtry Median a Wiener krok za krokem. Vylepšete kvalitu obrazu bez námahy.
type: docs
weight: 12
url: /cs/java/image-processing/apply-median-wiener-filters/
---
## Zavedení

V oblasti programování Java vyniká Aspose.PSD jako výkonný nástroj pro manipulaci a zpracování obrazu. Jednou z klíčových funkcí, které nabízí, je použití filtrů Median a Wiener, které hrají zásadní roli při zvyšování kvality obrazu a snižování šumu. Tento podrobný průvodce vás provede procesem použití těchto filtrů pomocí Aspose.PSD for Java.

## Předpoklady

Než se ponoříte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

1.  Aspose.PSD for Java Library: Stáhněte a nainstalujte knihovnu z[zde](https://releases.aspose.com/psd/java/).
2. Vývojové prostředí Java: Ujistěte se, že máte ve svém systému nastavené vývojové prostředí Java.

## Importujte balíčky

Začněte importováním potřebných balíčků, abyste mohli využít funkcionalitu Aspose.PSD v rámci vašeho projektu Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## Použití středního filtru

### Krok 1: Načtěte obrázek

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//Načtěte zdrojový obrázek
Image image = Image.load(sourceFile);
```

### Krok 2: Přeneste obrázek do rastrového obrázku

```java
// Přeneste obrázek do RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### Krok 3: Vytvořte instanci MedianFilterOptions

```java
// Vytvořte instanci třídy MedianFilterOptions a nastavte velikost filtru
MedianFilterOptions options = new MedianFilterOptions(4);
```

### Krok 4: Použijte střední filtr

```java
// Použijte filtr MedianFilterOptions na objekt RasterImage
rasterImage.filter(image.getBounds(), options);
```

### Krok 5: Uložte výsledný obrázek

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Uložte výsledný obrázek jako GIF
image.save(destName, new GifOptions());
```

Pomocí těchto kroků jste úspěšně aplikovali Mediánový filtr na svůj obrázek pomocí Aspose.PSD for Java.

## Závěr

V tomto tutoriálu jsme prozkoumali proces aplikace filtrů Median a Wiener pomocí Aspose.PSD pro Java. Tyto filtry jsou nepostradatelné pro zvýšení kvality obrazu a snížení šumu ve vašich aplikacích Java. Využitím výkonu Aspose.PSD můžete tyto filtry bez námahy začlenit do svých pracovních postupů zpracování obrazu.

## FAQ

### Q1: Mohu použít tyto filtry na obrázky libovolného formátu?

A1: Ano, Aspose.PSD podporuje širokou škálu obrazových formátů, díky čemuž je univerzální pro různé projekty.

### Q2: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro Java?

 A2: Ano, můžete získat bezplatnou zkušební verzi[zde](https://releases.aspose.com/).

### Q3: Jak získám podporu pro Aspose.PSD pro Java?

 A3: Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) za podporu komunity.

### Q4: Kde najdu dokumentaci k Aspose.PSD pro Java?

 A4: Viz dokumentace[zde](https://reference.aspose.com/psd/java/).

### Q5: Jak mohu zakoupit Aspose.PSD pro Java?

 A5: Můžete si koupit produkt[zde](https://purchase.aspose.com/buy).