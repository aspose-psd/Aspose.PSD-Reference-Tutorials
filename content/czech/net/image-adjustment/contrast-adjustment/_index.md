---
title: Implementace úpravy kontrastu v Aspose.PSD pro .NET
linktitle: Provádění úpravy kontrastu
second_title: Aspose.PSD .NET API
description: Naučte se, jak implementovat úpravu kontrastu v Aspose.PSD pro .NET pomocí tohoto podrobného průvodce.
type: docs
weight: 11
url: /cs/net/image-adjustment/contrast-adjustment/
---
## Úvod

Vítejte v tomto komplexním průvodci implementací úpravy kontrastu v Aspose.PSD pro .NET! V tomto tutoriálu prozkoumáme proces vylepšení kontrastu obrázku pomocí Aspose.PSD, výkonné knihovny .NET pro obrázky. Na konci této příručky budete dobře rozumět tomu, jak plynule aplikovat úpravy kontrastu na vaše obrázky.

## Předpoklady

Než se pustíme do procesu krok za krokem, ujistěte se, že máte splněny následující předpoklady:

1.  Knihovna Aspose.PSD pro .NET: Stáhněte a nainstalujte knihovnu Aspose.PSD pro .NET. Odkaz ke stažení najdete[tady](https://releases.aspose.com/psd/net/).

2. Adresář dokumentů: Nastavte adresář, kde budou uloženy vaše zdrojové a cílové soubory. Nahraďte "Your Document Directory" v poskytnutém kódu cestou k tomuto adresáři.

Nyní, když máme naše předpoklady v pořádku, přistoupíme k implementaci.

## Importovat jmenné prostory

V tomto kroku naimportujeme potřebné jmenné prostory pro přístup k funkcím poskytovaným knihovnou Aspose.PSD.

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Krok 1: Načtěte obrázek

Načtěte zdrojový obrázek do instance souboru`RasterImage` třída.

```csharp
//ExStart:LoadImage
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    RasterImage rasterImage = (RasterImage)image;
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    // Pokračujte dalším krokem...
}
//ExEnd:LoadImage
```

## Krok 2: Upravte kontrast

V tomto kroku upravíme kontrast načteného obrázku.

```csharp
//ExStart:AdjustContrast
rasterImage.AdjustContrast(50); // Upravte kontrast o 50 %
// Pokračujte dalším krokem...
//ExEnd:AdjustContrast
```

## Krok 3: Vytvořte možnosti TIFF

 Vytvořte instanci`TiffOptions` Pro výsledný obrázek nastavte různé vlastnosti a uložte obrázek ve formátu TIFF.

```csharp
//ExStart:CreateTiffOptions
string destName = dataDir + @"AdjustContrast_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
//ExEnd:CreateTiffOptions
```

Gratulujeme! Úspěšně jste implementovali úpravu kontrastu pomocí Aspose.PSD pro .NET.

## Závěr

V tomto tutoriálu jsme prozkoumali proces vylepšení kontrastu obrazu pomocí Aspose.PSD pro .NET. Knihovna poskytuje přímočarý způsob manipulace s vlastnostmi obrázků a umožňuje vývojářům bez námahy vytvářet vizuálně přitažlivé obrázky.

## FAQ

### Q1: Je Aspose.PSD pro .NET vhodný pro začátečníky?

A1: Aspose.PSD for .NET je navržen tak, aby byl pro vývojáře přívětivý, takže je vhodný pro začátečníky i zkušené vývojáře.

### Q2: Mohu použít Aspose.PSD pro komerční projekty?

 A2: Ano, Aspose.PSD pro .NET lze použít v komerčních projektech. Podrobnosti o licencích naleznete na adrese[tady](https://purchase.aspose.com/buy).

### Q3: Je k dispozici bezplatná zkušební verze?

 A3: Ano, můžete prozkoumat bezplatnou zkušební verzi Aspose.PSD pro .NET.[tady](https://releases.aspose.com/).

### Q4: Kde najdu podporu pro Aspose.PSD pro .NET?

 Odpověď 4: Navštivte fórum podpory Aspose.PSD for .NET[tady](https://forum.aspose.com/c/psd/34) pro pomoc.

### Q5: Jak mohu získat dočasnou licenci?

 A5: V případě potřeby můžete získat dočasnou licenci.[tady](https://purchase.aspose.com/temporary-license/).