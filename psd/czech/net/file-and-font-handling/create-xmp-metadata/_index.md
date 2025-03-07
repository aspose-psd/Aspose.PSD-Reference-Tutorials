---
title: Vytváření metadat XMP v Aspose.PSD pro .NET
linktitle: Vytváření metadat XMP
second_title: Aspose.PSD .NET API
description: Prozkoumejte vytváření metadat XMP v Aspose.PSD pro .NET. Vylepšete organizaci obrázků bezproblémovou manipulací.
weight: 10
url: /cs/net/file-and-font-handling/create-xmp-metadata/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytváření metadat XMP v Aspose.PSD pro .NET

## Zavedení

dynamickém světě vývoje .NET je precizní manipulace s obrázky klíčovým aspektem mnoha aplikací. Tento výukový program zkoumá vytváření metadat XMP v Aspose.PSD for .NET, výkonné knihovně, která zjednodušuje úlohy zpracování obrazu. XMP (Extensible Metadata Platform) umožňuje vkládat metadata do obrazových souborů, což usnadňuje efektivní organizaci a získávání informací spojených s obrazy.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.PSD for .NET Library: Stáhněte a nainstalujte knihovnu z[Dokumentace Aspose.PSD](https://reference.aspose.com/psd/net/).

- Vývojové prostředí: Nastavte vývojové prostředí .NET pomocí sady Visual Studio nebo vašeho preferovaného IDE.

- Základní znalosti .NET: Seznamte se se základními pojmy .NET, protože tento tutoriál předpokládá základní pochopení vývoje .NET.

## Importovat jmenné prostory

Ve svém projektu .NET zahrňte potřebné jmenné prostory pro přístup k funkcím Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.Xmp;
using Aspose.PSD.Xmp.Schemas.DublinCore;
using Aspose.PSD.Xmp.Schemas.Photoshop;
using System;
using System.IO;
```

Nyní si rozdělme proces vytváření metadat XMP do řady komplexních kroků.

## Krok 1: Zadejte velikost obrázku a obdélník

```csharp
// Cesta k adresáři dokumentů.
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();

//Určete velikost obrázku definováním obdélníku
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Krok 2: Vytvořte nový obrázek

```csharp
// Vytvořte zcela nový obrázek pro ukázkové účely
using (var image = new PsdImage(rect.Width, rect.Height))
{
    // Zde je kód pro manipulaci s obrázky...
}
```

## Krok 3: Vytvořte XMP-Header a XMP-Trailer

```csharp
// Vytvořte instanci XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi(Guid.NewGuid().ToString());

// Vytvořte instanci XMP-TrailerPi, třída XMPmeta pro nastavení různých atributů
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
XmpMeta xmpMeta = new XmpMeta();
```

## Krok 4: Nastavte atributy XMP

```csharp
// Nastavte atributy XMP, například:
xmpMeta.AddAttribute("Author", "Mr Smith");
xmpMeta.AddAttribute("Description", "The fake metadata value");
```

## Krok 5: Vytvořte XMP Packet Wrapper

```csharp
// Vytvořte instanci XmpPacketWrapper, která obsahuje všechna metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Krok 6: Vytvořte balíček Photoshopu a nastavte atributy

```csharp
// Vytvořte instanci balíku Photoshop a nastavte atributy Photoshopu
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.SetCity("London");
photoshopPackage.SetCountry("England");
photoshopPackage.SetColorMode(ColorMode.Rgb);
photoshopPackage.SetCreatedDate(DateTime.UtcNow);
```

## Krok 7: Přidejte balíček Photoshop do metadat XMP

```csharp
// Přidejte balíček photoshop do metadat XMP
xmpData.AddPackage(photoshopPackage);
```

## Krok 8: Vytvořte balíček DublinCore a nastavte atributy

```csharp
// Vytvořte instanci balíčku DublinCore a nastavte atributy dublinCore
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.SetAuthor("Mudassir Fayyaz");
dublinCorePackage.SetTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.AddValue("dc:movie", "Barfly");
```

## Krok 9: Přidejte balíček DublinCore do metadat XMP

```csharp
// Přidejte balíček dublinCore do metadat XMP
xmpData.AddPackage(dublinCorePackage);
```

## Krok 10: Aktualizujte metadata XMP a uložte obrázek

```csharp
using (var ms = new MemoryStream())
{
    // Aktualizujte metadata XMP do obrázku a uložte obrázek na disk nebo do datového proudu paměti
    image.XmpData = xmpData;
    image.Save(ms);
    image.Save(dataDir + "ee.psd");
    ms.Seek(0, System.IO.SeekOrigin.Begin);
}
```

## Krok 11: Načtěte obrázek a čtěte metadata

```csharp
// Chcete-li číst/získat metadata, načtěte obrázek z paměti nebo z disku
using (var img = (PsdImage)Image.Load(ms))
{
    // Získání metadat XMP
    XmpPacketWrapper imgXmpData = img.XmpData;
    foreach (XmpPackage package in imgXmpData.Packages)
    {
        // Použít data balíčku...
    }
}
```

## Závěr

Gratuluji! Úspěšně jste vytvořili metadata XMP v Aspose.PSD pro .NET. Tato výkonná funkce vylepšuje vaše možnosti zpracování obrazu a umožňuje efektivní organizaci a získávání důležitých informací.

## FAQ

### Q1: Je Aspose.PSD for .NET kompatibilní se všemi formáty obrázků?

A1: Aspose.PSD se primárně zaměřuje na formát souborů PSD (Adobe Photoshop), ale podporuje různé další formáty.

### Q2: Mohu manipulovat se stávajícími metadaty XMP pomocí Aspose.PSD pro .NET?

Odpověď 2: Ano, Aspose.PSD umožňuje číst i upravovat existující metadata XMP.

### Otázka 3: Existují nějaká omezení velikosti obrázku při použití Aspose.PSD pro .NET?

Odpověď 3: Aspose.PSD dokáže zpracovat obrázky různých velikostí, ale extrémně velké obrázky mohou vyžadovat další úvahy.

### Q4: Jak často je Aspose.PSD pro .NET aktualizován?

A4: Aktualizace jsou pravidelně vydávány, aby byla zajištěna kompatibilita s nejnovějšími verzemi rozhraní .NET a průmyslovými standardy.

### Q5: Existuje komunitní fórum pro podporu Aspose.PSD?

 Odpověď: Ano, podporu a diskuze najdete na[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
