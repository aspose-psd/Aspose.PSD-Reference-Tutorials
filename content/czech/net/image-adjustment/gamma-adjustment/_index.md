---
title: Implementace Gamma Adjustment v Aspose.PSD pro .NET
linktitle: Implementace Gamma Adjustment
second_title: Aspose.PSD .NET API
description: Prozkoumejte sílu Aspose.PSD pro .NET pomocí našeho podrobného průvodce implementací Gamma Adjustment. Bez námahy dolaďte jas a kontrast obrazu.
type: docs
weight: 12
url: /cs/net/image-adjustment/gamma-adjustment/
---
## Úvod

Vítejte v tomto komplexním průvodci implementací Gamma Adjustment v Aspose.PSD pro .NET! Nastavení gama je klíčová technika zpracování obrazu, která umožňuje jemně doladit jas a kontrast obrazu. V tomto tutoriálu vás provedeme procesem pomocí výkonné knihovny Aspose.PSD pro .NET.

## Předpoklady

Než se pustíte do implementace, ujistěte se, že máte splněny následující předpoklady:

-  Knihovna Aspose.PSD pro .NET: Ujistěte se, že máte nainstalovanou knihovnu Aspose.PSD pro .NET. Můžete si jej stáhnout[tady](https://releases.aspose.com/psd/net/).

- .NET Framework: Tento kurz předpokládá, že máte základní znalosti o vývoji .NET a máte nainstalované rozhraní .NET Framework.

- Integrované vývojové prostředí (IDE): Vyberte si preferované IDE pro vývoj .NET, jako je Visual Studio.

## Importovat jmenné prostory

Ve svém projektu .NET začněte importováním jmenných prostorů nezbytných pro práci s Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Krok 1: Nastavte svůj projekt

Vytvořte nový .NET projekt ve vámi zvoleném IDE. Nezapomeňte přidat odkazy na knihovnu Aspose.PSD.

## Krok 2: Definujte adresář dokumentů

```csharp
string dataDir = "Your Document Directory";
```

## Krok 3: Načtěte obrázek

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // Další kroky budou provedeny uvnitř tohoto pomocí bloku.
}
```

## Krok 4: Odeslání na rastrový obrázek a data do mezipaměti

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## Krok 5: Upravte Gamma

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## Krok 6: Vytvořte TiffOptions a uložte

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## Závěr

Gratulujeme! Úspěšně jste implementovali Gamma Adjustment pomocí Aspose.PSD pro .NET. Tato výkonná knihovna poskytuje robustní možnosti pro zpracování obrazu, což z ní činí cenný nástroj pro vývojáře .NET.

## FAQ

### Q1: Kde najdu dokumentaci Aspose.PSD?

 A1: Můžete nahlédnout do dokumentace[tady](https://reference.aspose.com/psd/net/).

### Q2: Jak stáhnu Aspose.PSD pro .NET?

 A2: Můžete si stáhnout knihovnu.[tady](https://releases.aspose.com/psd/net/).

### Q3: Je k dispozici bezplatná zkušební verze?

 A3: Ano, můžete získat bezplatnou zkušební verzi.[tady](https://releases.aspose.com/).

### Q4: Kde mohu získat podporu pro Aspose.PSD?

 A4: Můžete navštívit fórum podpory.[tady](https://forum.aspose.com/c/psd/34).

### Q5: Potřebuji dočasnou licenci?

 A5: V případě potřeby můžete získat dočasnou licenci.[tady](https://purchase.aspose.com/temporary-license/).