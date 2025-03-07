---
title: Použijte Gaussovy a Wienerovy filtry v Aspose.PSD pro Javu
linktitle: Použijte Gaussův a Wienerův filtr
second_title: Aspose.PSD Java API
description: Vylepšete své zpracování obrazu Java pomocí Aspose.PSD. Naučte se používat Gaussovy a Wienerovy filtry krok za krokem pro ohromující vizuální výsledky.
weight: 10
url: /cs/java/image-processing/apply-gaussian-wiener-filters/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Použijte Gaussovy a Wienerovy filtry v Aspose.PSD pro Javu

## Zavedení

Vítejte v našem komplexním tutoriálu o použití Gaussových a Wienerových filtrů v Aspose.PSD pro Javu! V této příručce vás provedeme procesem vylepšování obrázků pomocí těchto výkonných filtrů. Aspose.PSD for Java poskytuje robustní sadu funkcí pro zpracování obrazu a s použitím Gaussových a Wienerových filtrů můžete dosáhnout plynulejších a jemnějších obrázků.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Vývojové prostředí Java: Ujistěte se, že máte na svém počítači nastavené vývojové prostředí Java.

- Aspose.PSD for Java Library: Stáhněte si a nainstalujte knihovnu Aspose.PSD for Java. Odkaz ke stažení najdete[zde](https://releases.aspose.com/psd/java/).

## Importujte balíčky

Ve svém projektu Java naimportujte potřebné balíčky pro Aspose.PSD. Zde je ukázkový příkaz k importu, který vám pomůže začít:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

Nyní rozdělme příklad do několika kroků pro použití Gaussových a Wienerových filtrů.

## Krok 1: Načtěte obrázek

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

V tomto kroku načteme soubor obrázku PSD ze zadaného adresáře.

## Krok 2: Zkontrolujte rastrový obrázek

```java
if (rasterImage == null) {
    return;
}
```

Ujistěte se, že načtený obrázek je platný rastrový obrázek; jinak je proces ukončen.

## Krok 3: Nakonfigurujte možnosti filtru

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

Vytvořte instanci GaussWienerFilterOptions, nastavte velikost poloměru, hodnotu vyhlazení a určete, zda chcete použít filtr ve stupních šedi.

## Krok 4: Použijte filtr a uložte

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

Nakonec použijte nakonfigurované Gaussovy a Wienerovy filtry na RasterImage a uložte výsledný obrázek ve formátu GIF.

## Závěr

Gratuluji! Úspěšně jste se naučili, jak používat Gaussovy a Wienerovy filtry pomocí Aspose.PSD pro Javu. Experimentujte s různými parametry, abyste dosáhli požadovaného vylepšení obrazu.

## FAQ

### Q1: Mohu použít tyto filtry na obrázky v jiných formátech než PSD?

Odpověď 1: Ano, Aspose.PSD for Java podporuje různé formáty obrázků mimo PSD.

### Otázka 2: Existují nějaká omezení ve zkušební verzi Aspose.PSD pro Javu?

Odpověď 2: Zkušební verze má omezení a můžete prozkoumat plné možnosti získáním platné licence.

### Q3: Jak mohu získat podporu pro Aspose.PSD pro Java?

 A3: Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) za podporu komunity a diskuze.

### Q4: Je k dispozici dočasná licence pro testovací účely?

 A4: Ano, můžete získat dočasnou licenci[zde](https://purchase.aspose.com/temporary-license/).

### Q5: Kde najdu podrobnou dokumentaci k Aspose.PSD pro Java?

 A5: Viz[dokumentace](https://reference.aspose.com/psd/java/) pro podrobné informace.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
