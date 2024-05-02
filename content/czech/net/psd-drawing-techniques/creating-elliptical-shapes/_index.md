---
title: Vytváření eliptických tvarů pomocí Aspose.PSD pro .NET
linktitle: Vytváření eliptických tvarů pomocí Aspose.PSD pro .NET
second_title: Aspose.PSD .NET API
description: Naučte se kreslit eliptické tvary v .NET pomocí Aspose.PSD. Podrobný průvodce s příklady kódu. Vytvářejte úžasnou grafiku bez námahy.
type: docs
weight: 13
url: /cs/net/psd-drawing-techniques/creating-elliptical-shapes/
---
## Úvod

Vítejte v našem komplexním průvodci vytvářením eliptických tvarů pomocí Aspose.PSD pro .NET. Aspose.PSD je výkonná knihovna .NET, která umožňuje vývojářům manipulovat a převádět soubory Photoshopu bez potřeby Adobe Photoshop. V tomto tutoriálu vás provedeme procesem kreslení eliptických tvarů pomocí knihovny.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Knihovna Aspose.PSD for .NET: Ujistěte se, že máte ve svém projektu .NET nainstalovanou knihovnu Aspose.PSD. Můžete si jej stáhnout z[Aspose.PSD pro dokumentaci .NET](https://reference.aspose.com/psd/net/).

- Prostředí .NET: Tento výukový program předpokládá, že máte pracovní znalosti rozhraní .NET.

## Importovat jmenné prostory

Chcete-li začít, importujte potřebné jmenné prostory do svého projektu. To zajistí, že budete mít přístup ke třídám a metodám potřebným pro kreslení eliptických tvarů. Zde je příklad:

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

Nyní si proces vytváření eliptických tvarů rozdělíme do několika kroků:

## Krok 1: Nastavte adresář dokumentů

```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";
```

## Krok 2: Vytvořte instanci BmpOptions

```csharp
// Vytvořte instanci BmpOptions a nastavte její různé vlastnosti
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## Krok 3: Vytvořte instanci obrázku

```csharp
// Vytvořte instanci Image
using (Image image = new PsdImage(100, 100))
{
    // Vytvořte a inicializujte instanci třídy Graphics a povrchu Clear Graphics
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## Krok 4: Nakreslete tvar tečkované elipsy

```csharp
    // Nakreslete tvar tečkované elipsy tak, že určíte, že objekt Pero má červenou barvu a obklopující obdélník
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## Krok 5: Nakreslete tvar spojité elipsy

```csharp
    //Nakreslete tvar souvislé elipsy zadáním objektu Pero s plným štětcem s modrou barvou a obklopujícím obdélníkem
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // Export obrázku do formátu souboru bmp.
    image.Save(outpath, saveOptions);
}
```

## Závěr

Gratulujeme! Úspěšně jste vytvořili eliptické tvary pomocí Aspose.PSD pro .NET. Tento tutoriál se zabýval základními kroky, od nastavení prostředí až po kreslení tečkovaných i souvislých tvarů elips.

## FAQ

### Q1: Kde najdu dokumentaci k Aspose.PSD pro .NET?

 A1: Dokumentace je k dispozici[tady](https://reference.aspose.com/psd/net/).

### Q2: Jak stáhnu Aspose.PSD pro .NET?

 A2: Můžete si jej stáhnout ze stránky vydání[tady](https://releases.aspose.com/psd/net/).

### Q3: Je k dispozici bezplatná zkušební verze?

 A3: Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).

### Q4: Jak mohu získat podporu pro Aspose.PSD pro .NET?

 A4: Navštivte fórum podpory[tady](https://forum.aspose.com/c/psd/34).

### Q5: Potřebuji pro testování dočasnou licenci?

 A5: Ano, můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).