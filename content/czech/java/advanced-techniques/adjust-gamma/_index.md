---
title: Upravte Gamma obrázku pomocí Aspose.PSD pro Javu
linktitle: Upravte gamu obrázku
second_title: Aspose.PSD Java API
description: Naučte se bez námahy upravovat gamu obrazu pomocí Aspose.PSD pro Javu. Pro optimální výsledky postupujte podle našeho podrobného průvodce.
type: docs
weight: 23
url: /cs/java/advanced-techniques/adjust-gamma/
---
## Zavedení

V oblasti zpracování obrazu je úprava gama obrazu zásadním krokem ke zvýšení jeho vizuální přitažlivosti. Aspose.PSD for Java nabízí vývojářům Java výkonné řešení pro snadnou manipulaci s obrazem gama. V tomto tutoriálu prozkoumáme, jak upravit gamu pomocí Aspose.PSD, přičemž rozebereme každý krok, abychom zajistili bezproblémovou implementaci.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte nastaveny následující předpoklady:

1. Vývojové prostředí Java: Ujistěte se, že máte ve svém systému nainstalované vývojové prostředí Java.
2.  Knihovna Aspose.PSD: Stáhněte si a integrujte knihovnu Aspose.PSD do svého projektu Java. Potřebné zdroje najdete v[dokumentace](https://reference.aspose.com/psd/java/).
3. Ukázkový obrázek: Připravte si ukázkový obrázek PSD, který použijete k aplikaci úpravy gama.

## Importujte balíčky

Chcete-li zahájit proces, importujte požadované balíčky do svého projektu Java. To nastavuje půdu pro bezproblémové využití funkcí Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Krok 1: Načtěte obrázek

 Začněte načtením ukázkového obrázku PSD do instance souboru`RasterImage` třída. To je základ pro následné úpravy gama.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Načtěte existující obrázek do instance třídy RasterImage
Image image = Image.load(sourceFile);

// Odeslání objektu obrázku do rastrového obrázku
RasterImage rasterImage = (RasterImage)image;

// Pro lepší výkon zkontrolujte, zda je RasterImage uložen v mezipaměti
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Krok 2: Upravte Gamma

 Nyní upravte gama načteného obrázku pomocí`adjustGamma` metoda. Dolaďte hodnoty gama podle svých požadavků.

```java
// Upravte gama
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Krok 3: Vytvořte TiffOptions

 Vytvořte instanci`TiffOptions` pro výsledný obrázek. Nastavte různé vlastnosti, jako jsou bity na vzorek a fotometrické možnosti, abyste přizpůsobili výstup svým specifikacím.

```java
// Vytvořte instanci TiffOptions pro výsledný obrázek
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Krok 4: Uložte výsledný obrázek

 Uložte upravený obrázek do formátu TIFF pomocí dříve definovaného`TiffOptions`.

```java
// Uložte výsledný obrázek do formátu TIFF
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Závěr

Gratuluji! Úspěšně jste upravili gamu obrázku pomocí Aspose.PSD pro Javu. Tento proces umožňuje vývojářům bez námahy vylepšovat kvalitu obrazu, což přispívá k vizuálně přitažlivému uživatelskému zážitku.

## FAQ

### Q1: Kde najdu dokumentaci Aspose.PSD?

 A1: K dokumentaci se dostanete na adrese[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: Jak stáhnu Aspose.PSD pro Java?

 A2: Stáhněte si knihovnu z[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: Kde mohu zakoupit Aspose.PSD?

 A3: Návštěva[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) k nákupu Aspose.PSD.

### Q4: Je k dispozici bezplatná zkušební verze?

 A4: Ano, můžete prozkoumat bezplatnou zkušební verzi na[https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: Kde mohu hledat podporu pro Aspose.PSD?

 Odpověď 5: Podporu získáte na fóru Aspose.PSD na adrese[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).