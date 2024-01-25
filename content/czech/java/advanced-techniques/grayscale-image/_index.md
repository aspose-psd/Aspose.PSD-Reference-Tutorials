---
title: Obrázek ve stupních šedi pomocí Aspose.PSD pro Javu
linktitle: Obrázek ve stupních šedi
second_title: Aspose.PSD Java API
description: Prozkoumejte Aspose.PSD for Java a naučte se, jak bez námahy vytvářet obrázky ve stupních šedi pomocí našeho podrobného návodu.
type: docs
weight: 10
url: /cs/java/advanced-techniques/grayscale-image/
---
## Úvod

V oblasti zpracování obrazu je převod obrazu na stupně šedi základní operací. Aspose.PSD for Java poskytuje výkonné řešení pro vývojáře Java, jak toho dosáhnout bez problémů. V tomto tutoriálu vás provedeme procesem škálování šedi na obrázku pomocí Aspose.PSD a zajistíme, že i začátečníci budou moci bez námahy následovat.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

1. Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovanou Javu.
2.  Aspose.PSD for Java: Stáhněte si a nainstalujte knihovnu Aspose.PSD pro Java z[tady](https://releases.aspose.com/psd/java/).

## Importujte balíčky

Začněte importováním potřebných balíčků do vašeho projektu Java. Tento krok zajistí, že budete mít přístup k funkcím Aspose.PSD ve vašem kódu. Na začátek souboru Java přidejte následující řádky:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
import java.io.FileNotFoundException;
```

## Krok 1: Nastavte adresář dokumentů

Definujte adresář, kde se nachází váš soubor PSD a kam se uloží výstup ve stupních šedi:

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Načtěte zdrojový obrázek

Načtěte zdrojový obrázek PSD do kódu pomocí následujícího úryvku:

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "Grayscaling_out.jpg";

Image image = Image.load(sourceFile);
```

## Krok 3: Zkontrolujte a uložte obrázek do mezipaměti

Zajistěte, aby byl načtený obrázek uložen do mezipaměti, optimalizujte rychlost zpracování:

```java
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;
if (!rasterCachedImage.isCached())
{
    rasterCachedImage.cacheData();
}
```

## Krok 4: Transformace do stupňů šedi

Převeďte obrázek do zobrazení ve stupních šedi:

```java
rasterCachedImage.grayscale();
```

## Krok 5: Uložte výsledný obrázek

Uložte obrázek ve stupních šedi pomocí zadaného názvu cíle a možností JPEG:

```java
rasterCachedImage.save(destName, new JpegOptions());
```

Opakujte tyto kroky pro všechny další obrázky, které chcete použít ve stupních šedi.

## Závěr

Gratulujeme! Úspěšně jste upravili obrázek ve stupních šedi pomocí Aspose.PSD for Java. Tento jednoduchý, ale výkonný proces lze integrovat do různých aplikací a vylepšit tak možnosti zpracování obrazu.

## FAQ

### Q1: Mohu použít Aspose.PSD for Java pro komerční projekty?

Odpověď 1: Ano, Aspose.PSD for Java je k dispozici pro komerční použití. Můžete si zakoupit licenci[tady](https://purchase.aspose.com/buy).

### Q2: Existuje bezplatná zkušební verze Aspose.PSD pro Java?

 Odpověď 2: Ano, funkce Aspose.PSD pro Javu můžete prozkoumat pomocí bezplatné zkušební verze. Stáhnout to[tady](https://releases.aspose.com/).

### Q3: Kde najdu dokumentaci k Aspose.PSD pro Java?

 A3: Viz dokumentace[tady](https://reference.aspose.com/psd/java/).

### Q4: Jak mohu získat dočasné licence pro Aspose.PSD pro Java?

 A4: Získejte dočasné licence[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Potřebujete podporu nebo máte otázky?

 A5: Navštivte fórum Aspose.PSD[tady](https://forum.aspose.com/c/psd/34).