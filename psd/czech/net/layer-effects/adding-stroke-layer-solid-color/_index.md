---
title: Přidání vrstvy tahu s plnou barvou v Aspose.PSD pro .NET
linktitle: Přidání vrstvy tahu s plnou barvou
second_title: Aspose.PSD .NET API
description: Vylepšete své dovednosti manipulace s obrázky .NET pomocí Aspose.PSD. Naučte se krok za krokem přidávat vrstvy tahu s plnými barvami.
type: docs
weight: 11
url: /cs/net/layer-effects/adding-stroke-layer-solid-color/
---
## Zavedení

V oblasti vývoje .NET je vytváření vizuálně přitažlivých obrázků běžným požadavkem. Aspose.PSD for .NET poskytuje výkonnou sadu nástrojů pro bezproblémovou manipulaci a vylepšování obrázků. Jednou ze základních funkcí je přidání vrstvy tahu s plnou barvou, která dodá vašim obrázkům živost a hloubku. V tomto tutoriálu vás provedeme procesem krok za krokem pomocí Aspose.PSD pro .NET.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte následující předpoklady:

- Základní znalost vývoje .NET.
- Visual Studio nainstalované na vašem počítači.
- Aspose.PSD pro knihovnu .NET. Můžete si jej stáhnout z[webové stránky](https://releases.aspose.com/psd/net/).

## Importovat jmenné prostory

Začněte importem potřebných jmenných prostorů, abyste mohli využít funkčnost Aspose.PSD pro .NET:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## Krok 1: Načtěte soubor PSD

Začněte načtením souboru PSD, který chcete vylepšit vrstvou tahu. Ujistěte se, že máte správnou cestu k souboru:

```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "Stroke.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // Zde bude přidán kód pro další kroky
}
```

## Krok 2: Otevřete Vlastnosti efektu tahu

Získejte vlastnosti efektu tahu ze souboru PSD:

```csharp
var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

if ((colorStroke.BlendMode != BlendMode.Normal) ||
    (colorStroke.Opacity != 255) ||
    (colorStroke.IsVisible != true))
{
    throw new Exception("Color stroke effect was read wrong");
}
```

## Krok 3: Upravte nastavení zdvihu

Upravte nastavení zdvihu podle svých preferencí. V tomto příkladu změníme barvu na žlutou, nastavíme krytí na 127 a použijeme režim prolnutí barev:

```csharp
var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

if ((fillSettings.Color != Color.Black) || (fillSettings.FillType != FillType.Color))
{
    throw new Exception("Color stroke effect settings were read wrong");
}

fillSettings.Color = Color.Yellow;
colorStroke.Opacity = 127;
colorStroke.BlendMode = BlendMode.Color;
```

## Krok 4: Uložte upravený obrázek

Po použití změn vrstvy tahu uložte obrázek:

```csharp
string exportPath = dataDir + "StrokeGradientChanged.psd";
im.Save(exportPath);
```

## Krok 5: Ověřte změny

Zajistěte, aby byly změny správně aplikovány načtením a kontrolou upraveného obrázku:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    // Zde bude přidán kód pro ověření změn
}
```

Opakujte tyto kroky pro další úpravy nebo experimentujte s různými efekty tahu, abyste dosáhli požadovaného vizuálního efektu.

## Závěr

Gratuluji! Úspěšně jste se naučili, jak přidat vrstvu tahu s plnou barvou pomocí Aspose.PSD pro .NET. Tato výkonná funkce otevírá svět možností pro vylepšení vašich obrázků v prostředí .NET.

## Nejčastější dotazy

### Q1: Je Aspose.PSD for .NET kompatibilní s nejnovějšími verzemi rozhraní .NET?

A1: Ano, Aspose.PSD pro .NET je pravidelně aktualizován, aby byla zajištěna kompatibilita s nejnovějšími verzemi .NET frameworku.

### Q2: Mohu použít Aspose.PSD pro .NET pro komerční projekty?

A2: Rozhodně! Aspose.PSD for .NET je komerční produkt a můžete jej používat ve svých projektech zakoupením licence.

### Q3: Kde najdu další příklady a dokumentaci pro Aspose.PSD pro .NET?

 A3: Prozkoumejte[dokumentace](https://reference.aspose.com/psd/net/) pro komplexní příklady a návody.

### Q4: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro .NET?

 A4: Ano, můžete získat bezplatnou zkušební verzi z[stránka vydání](https://releases.aspose.com/).

### Q5: Jak mohu získat podporu pro Aspose.PSD pro .NET?

 A5: Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) vyhledat pomoc a spojit se s komunitou.