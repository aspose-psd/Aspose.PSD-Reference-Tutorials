---
title: Přidání vrstvy tahu se vzorem v Aspose.PSD pro .NET
linktitle: Přidání vrstvy tahu se vzorem
second_title: Aspose.PSD .NET API
description: Vylepšete své soubory PSD pomocí vrstev a vzorů tahů pomocí Aspose.PSD pro .NET. Postupujte podle našeho podrobného průvodce pro bezproblémovou integraci.
type: docs
weight: 13
url: /cs/net/layer-effects/adding-stroke-layer-pattern/
---
## Zavedení

Vylepšení souborů PSD (Photoshop Document) vrstvami tahů a vzory může dodat vašim návrhům dynamický nádech. V tomto tutoriálu prozkoumáme, jak využít Aspose.PSD pro .NET k snadnému přidání vrstvy tahu se vzorem do vašich souborů PSD. Aspose.PSD je výkonná .NET knihovna, která poskytuje komplexní podporu pro manipulaci se soubory PSD, což z ní činí neocenitelný nástroj pro vývojáře i designéry.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Základní znalost programovacího jazyka C#.
- Visual Studio nainstalované na vašem počítači.
-  Aspose.PSD pro .NET knihovnu, kterou si můžete stáhnout[zde](https://releases.aspose.com/psd/net/).

## Importovat jmenné prostory

Ujistěte se, že importujete potřebné jmenné prostory do kódu C#:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## Krok 1: Nastavte své prostředí

Začněte definováním zdrojového a výstupního adresáře v kódu C#:

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";
```

## Krok 2: Načtěte soubor PSD

Načtěte soubor PSD pomocí třídy PsdImage Aspose.PSD:

```csharp
var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

string sourceFileName = Path.Combine(SourceDir, "Stroke.psd");
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // Zde je váš kód pro zpracování souboru PSD
}
```

## Krok 3: Připravte data nového vzoru

Definujte nový vzor a jeho hranice:

```csharp
var newPattern = new int[]
{
    // Zde jsou barvy vašeho vzoru
};

var newPatternBounds = new Rectangle(0, 0, 4, 4);
var guid = Guid.NewGuid();
```

## Krok 4: Upravte vrstvu tahu

Otevřete vrstvu tahu a aktualizujte její vlastnosti:

```csharp
var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

// Zkontrolujte a aktualizujte vlastnosti tahu
// ...

// Aktualizujte krytí a režim prolnutí
patternStroke.Opacity = 127;
patternStroke.BlendMode = BlendMode.Color;
```

## Krok 5: Aktualizujte informace o vzoru

Aktualizujte informace o vzoru v souboru PSD:

```csharp
foreach (var globalLayerResource in im.GlobalLayerResources)
{
    if (globalLayerResource is PattResource)
    {
        // Zde je váš kód pro aktualizaci informací o vzoru
    }
}

// Uložte upravený soubor PSD
im.Save(exportPath);
```

## Krok 6: Ověřte změny

Načtěte upravený soubor PSD a ověřte změny:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

    // Zde je váš kód pro ověření změn
}
```

## Závěr

Gratuluji! Úspěšně jste se naučili, jak přidat vrstvu tahu se vzorem v Aspose.PSD pro .NET. Tato všestranná knihovna umožňuje vývojářům vytvářet vizuálně přitažlivé návrhy a zvyšovat flexibilitu souborů PSD.

## FAQ

### Q1: Mohu použít Aspose.PSD pro .NET s jakoukoli verzí sady Visual Studio?

Odpověď 1: Ano, Aspose.PSD for .NET je kompatibilní s různými verzemi sady Visual Studio.

### Q2: Jak mohu získat dočasnou licenci pro Aspose.PSD?

 A2: Návštěva[zde](https://purchase.aspose.com/temporary-license/) získat dočasnou licenci.

### Q3: Jsou k dispozici nějaké ukázkové soubory PSD pro testování?

 Odpověď 3: Vzorové soubory PSD najdete v dokumentaci[zde](https://reference.aspose.com/psd/net/).

### Q4: Je Aspose.PSD vhodný pro dávkové zpracování souborů PSD?

A4: Aspose.PSD pro .NET samozřejmě poskytuje robustní podporu pro dávkové zpracování.

### Q5: Kde mohu vyhledat pomoc nebo se zúčastnit diskusí komunity?

 A5: Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) za podporu a komunikaci s komunitou.