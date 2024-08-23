---
title: Crop Image by Rectangle v Aspose.PSD pro Javu
linktitle: Oříznout obrázek podle obdélníku
second_title: Aspose.PSD Java API
description: Prozkoumejte možnosti bezproblémového ořezávání obrázků v Javě s Aspose.PSD. Postupujte podle našeho podrobného průvodce pro snadné oříznutí obrázků pomocí Aspose.PSD pro Java.
type: docs
weight: 15
url: /cs/java/image-editing/crop-image-by-rectangle/
---
## Zavedení

Ve světě vývoje v Javě je manipulace s obrázky běžným úkolem a Aspose.PSD pro Javu poskytuje výkonné řešení pro zpracování obrázků. V tomto tutoriálu vás provedeme procesem oříznutí obrázku pomocí obdélníku pomocí Aspose.PSD for Java. Postupujte podle níže uvedených kroků, abyste toho dosáhli snadno.

## Předpoklady

Než se ponoříte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Java Development Kit (JDK) nainstalovaný na vašem počítači.
- Aspose.PSD pro knihovnu Java. Můžete si jej stáhnout z[webové stránky](https://releases.aspose.com/psd/java/).

## Importujte balíčky

Ujistěte se, že jste do svého projektu Java zahrnuli potřebné balíčky, abyste mohli využít schopností Aspose.PSD pro Java. Na začátek souboru Java přidejte následující příkazy pro import:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Nyní si tento proces rozdělíme do několika kroků, které vás provedou oříznutím obrázku pomocí obdélníku pomocí Aspose.PSD for Java.

## Krok 1: Nastavte adresář dokumentů

```java
String dataDir = "Your Document Directory";
```

 Nahradit`"Your Document Directory"` se skutečnou cestou, kde se nachází váš soubor PSD.

## Krok 2: Zadejte zdrojové a cílové soubory

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Definujte cesty pro váš zdrojový soubor PSD a cílový soubor JPEG.

## Krok 3: Načtěte a uložte obrázek do mezipaměti

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Nahrajte obrázek PSD do a`RasterImage` instance a ukládat její data do mezipaměti.

## Krok 4: Vytvořte a definujte ořezový obdélník

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

 Vytvořte instanci souboru`Rectangle` třídy s požadovanou velikostí pro oříznutí.

## Krok 5: Ořízněte a uložte obrázek

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Proveďte operaci oříznutí pomocí určeného obdélníku a uložte výsledky jako soubor JPEG.

Opakujte tyto kroky podle potřeby a upravte parametry podle svých specifických požadavků.

## Závěr

V tomto tutoriálu jsme prošli procesem oříznutí obrázku pomocí obdélníku pomocí Aspose.PSD pro Java. Pomocí těchto kroků můžete snadno integrovat výkonné možnosti manipulace s obrázky do svých aplikací Java.

## FAQ

### Q1: Mohu použít Aspose.PSD pro Java s jinými frameworky Java?

Odpověď 1: Ano, Aspose.PSD for Java lze integrovat s různými frameworky Java, což poskytuje flexibilitu ve vašich vývojových projektech.

### Q2: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro Java?

 A2: Ano, máte přístup k bezplatné zkušební verzi[zde](https://releases.aspose.com/).

### Q3: Kde najdu další podporu nebo pomoc?

 A3: Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) za podporu komunity a diskuze.

### Q4: Jak získám dočasnou licenci pro Aspose.PSD for Java?

 A4: Můžete získat dočasnou licenci[zde](https://purchase.aspose.com/temporary-license/).

### Q5: Jaké jsou podporované formáty obrázků pro oříznutí v Aspose.PSD pro Java?

Odpověď 5: Aspose.PSD for Java podporuje různé formáty obrázků, včetně PSD, PNG, JPEG a dalších.