---
title: Implementace úpravy jasu v Aspose.PSD pro .NET
linktitle: Provádění úpravy jasu
second_title: Aspose.PSD .NET API
description: Prozkoumejte sílu Aspose.PSD pro .NET při úpravě jasu obrazu. Postupujte podle našeho podrobného průvodce pro bezproblémovou implementaci.
type: docs
weight: 10
url: /cs/net/image-adjustment/brightness-adjustment/
---
## Zavedení

Vylepšení a úprava atributů obrázků je běžným požadavkem v různých aplikacích a Aspose.PSD for .NET poskytuje výkonné řešení pro bezproblémovou manipulaci se soubory PSD. Jednou z takových manipulací je úprava jasu, která vám umožňuje bez námahy upravit jas obrazu.

V tomto tutoriálu si projdeme proces implementace úpravy jasu pomocí Aspose.PSD pro .NET. Chcete-li získat ucelené informace o tom, jak začlenit úpravy jasu do souborů PSD, postupujte podle následujících kroků.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Knihovna Aspose.PSD for .NET: Stáhněte a nainstalujte knihovnu Aspose.PSD for .NET z[odkaz ke stažení](https://releases.aspose.com/psd/net/).

-  Adresář dokumentů: Nastavte adresář pro ukládání souborů PSD a aktualizaci`dataDir` proměnnou v poskytnutém fragmentu kódu s cestou k adresáři vašeho dokumentu.

## Importovat jmenné prostory

Ve svém projektu .NET zahrňte potřebné jmenné prostory pro přístup k funkcím Aspose.PSD. Přidejte do svého kódu následující jmenné prostory:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

Nyní si příklad rozdělíme do několika kroků:

## Krok 1: Načtěte soubor PSD

```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";
string sourceFile = dataDir + @"sample.psd";

// Načtěte soubor PSD pomocí Aspose.PSD
using (var image = (PsdImage)Image.Load(sourceFile))
{
    // Váš kód pro další kroky je zde
}
```

## Krok 2: Získejte rastrový obrázek

```csharp
// Získejte rastrový obrázek z načteného souboru PSD
RasterCachedImage rasterImage = image;
```

## Krok 3: Upravte jas

```csharp
// Nastavte hodnotu jasu. Akceptované hodnoty jasu jsou v rozsahu [-255, 255].
rasterImage.AdjustBrightness(-50);
```

## Krok 4: Uložte upravený obrázek

```csharp
// Uložte upravený obrázek s upraveným jasem
string destName = dataDir + @"AdjustBrightness_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
rasterImage.Save(destName, tiffOptions);
```

Nyní, když jsme příklad rozdělili do zvládnutelných kroků, můžete plynule integrovat úpravu jasu do svého projektu .NET pomocí Aspose.PSD.

## Závěr

Aspose.PSD for .NET zjednodušuje proces implementace úprav jasu v souborech PSD. Podle výše uvedeného podrobného průvodce můžete bez námahy vylepšit vizuální přitažlivost svých obrázků. Experimentujte s různými hodnotami jasu, abyste dosáhli požadovaných výsledků.

## FAQ

### Q1: Kde najdu dokumentaci k Aspose.PSD pro .NET?

 A1: Dokumentace je k dispozici[zde](https://reference.aspose.com/psd/net/).

### Q2: Jak mohu stáhnout knihovnu Aspose.PSD pro .NET?

 A2: Knihovnu si můžete stáhnout z[stránka vydání](https://releases.aspose.com/psd/net/).

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro .NET?

 A3: Ano, máte přístup k bezplatné zkušební verzi[zde](https://releases.aspose.com/).

### Q4: Kde mohu získat podporu pro Aspose.PSD pro .NET?

 A4: Pro podporu navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Jak získám dočasnou licenci pro Aspose.PSD pro .NET?

 A5: Můžete získat dočasnou licenci[zde](https://purchase.aspose.com/temporary-license/).