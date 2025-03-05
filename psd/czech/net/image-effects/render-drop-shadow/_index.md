---
title: Vykreslování efektu vrženého stínu v Aspose.PSD pro .NET
linktitle: Vykreslování efektu vrženého stínu
second_title: Aspose.PSD .NET API
description: Prozkoumejte sílu Aspose.PSD pro .NET v tomto tutoriálu a ovládněte umění vykreslování úchvatných efektů vrženého stínu.
type: docs
weight: 12
url: /cs/net/image-effects/render-drop-shadow/
---
## Zavedení

Vítejte v našem podrobném návodu k vykreslování efektů vrženého stínu v Aspose.PSD pro .NET! Pokud chcete zlepšit své dovednosti manipulace s obrázky pomocí Aspose.PSD, jste na správném místě. V této příručce vás provedeme procesem snadného použití efektů vržených stínů na vaše obrázky.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.PSD for .NET Library: Ujistěte se, že máte nainstalovanou knihovnu Aspose.PSD. Můžete si jej stáhnout[zde](https://releases.aspose.com/psd/net/).

- Adresář dokumentů: Nastavte adresář, kde jsou uloženy vaše dokumenty a obrázky. Tento adresář budete muset zadat v kódu.

## Importovat jmenné prostory

Ve svém projektu .NET začněte importováním potřebných jmenných prostorů:

```csharp
using Aspose.PSD.FileFormats.Png;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
using System;
```

Nyní rozeberme příklad kódu do několika kroků pro jasné pochopení:

## Krok 1: Nastavte adresář dokumentů

```csharp
string dataDir = "Your Document Directory";
```

Ujistěte se, že jste nahradili "Your Document Directory" skutečnou cestou, kde jsou uloženy vaše obrázky.

## Krok 2: Načtěte soubor PSD se zdrojem efektů

```csharp
string sourceFileName = dataDir + "Shadow.psd";
string pngExportPath = dataDir + "Shadowchanged1.png";
var loadOptions = new PsdLoadOptions()
{
	LoadEffectsResource = true
};
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
```

Načtěte soubor PSD a povolte načítání zdrojů efektů.

## Krok 3: Načtěte a ověřte vlastnosti efektu vrženého stínu

```csharp
var shadowEffect = (DropShadowEffect)(im.Layers[1].BlendingOptions.Effects[0]);
if ((shadowEffect.Color != Color.Black) ||
	(shadowEffect.Opacity != 255) ||
	(shadowEffect.Distance != 3) ||
	(shadowEffect.Size != 7) ||
	(shadowEffect.UseGlobalLight != true) ||
	(shadowEffect.Angle != 90) ||
	(shadowEffect.Spread != 0) ||
	(shadowEffect.Noise != 0))
{
	throw new Exception("Shadow Effect properties were read wrong");
}
```

Získejte vlastnosti efektu vrženého stínu a ověřte je podle svých očekávání.

## Krok 4: Uložte obrázek s aplikovaným stínovým efektem

```csharp
var saveOptions = new PngOptions();
saveOptions.ColorType = PngColorType.TruecolorWithAlpha;
im.Save(pngExportPath, saveOptions);
```

Uložte upravený obrázek s aplikovaným efektem vrženého stínu ve formátu PNG.

A je to! Úspěšně jste vykreslili efekt vrženého stínu pomocí Aspose.PSD pro .NET.

## Závěr

tomto tutoriálu jsme prozkoumali proces vykreslování efektů vrženého stínu v Aspose.PSD pro .NET. Pomocí těchto jednoduchých kroků můžete svým obrázkům přidat hloubku a rozměr a bez námahy vytvářet vizuálně úžasné výsledky.

## FAQ

### Q1: Je Aspose.PSD for .NET kompatibilní se všemi formáty obrázků?

A1: Aspose.PSD primárně podporuje formát PSD, ale poskytuje také možnosti převodu pro různé jiné formáty.

### Q2: Mohu dále upravit vlastnosti vrženého stínu?

A2: Rozhodně! Neváhejte a upravte kód tak, aby vyhovoval vašim specifickým požadavkům a dosáhl požadovaných vizuálních efektů.

### Q3: Kde najdu další dokumentaci k Aspose.PSD pro .NET?

 A3: Viz dokumentace[zde](https://reference.aspose.com/psd/net/) pro podrobné informace o funkcích Aspose.PSD.

### Q4: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro .NET?

 A4: Ano, můžete prozkoumat bezplatnou zkušební verzi[zde](https://releases.aspose.com/).

### Otázka 5: Jak mohu získat podporu nebo vyhledat pomoc s Aspose.PSD pro .NET?

 A5: Navštivte fórum Aspose.PSD[zde](https://forum.aspose.com/c/psd/34) zapojit se do komunity a vyhledat odbornou radu.