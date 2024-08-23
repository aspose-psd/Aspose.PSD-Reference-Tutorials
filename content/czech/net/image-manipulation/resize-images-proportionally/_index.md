---
title: Proporcionální změna velikosti obrázků v Aspose.PSD pro .NET
linktitle: Proporcionální změna velikosti obrázků
second_title: Aspose.PSD .NET API
description: Prozkoumejte bezproblémovou změnu velikosti obrázku s Aspose.PSD pro .NET. Stáhněte si knihovnu, postupujte podle našeho návodu a vylepšete své možnosti zpracování obrazu.
type: docs
weight: 14
url: /cs/net/image-manipulation/resize-images-proportionally/
---
oblasti manipulace s obrázky vyniká Aspose.PSD for .NET jako výkonná sada nástrojů, která poskytuje vývojářům možnost snadno proporcionálně měnit velikost obrázků. V tomto podrobném průvodci vás provedeme procesem změny velikosti obrázků pomocí Aspose.PSD for .NET a zajistíme, že si vaše obrázky zachovají své proporce bezchybně.

## Zavedení

Proporcionální změna velikosti obrázků je běžným úkolem v mnoha aplikacích a Aspose.PSD for .NET tento proces pro vývojáře zjednodušuje. Ať už pracujete na webové aplikaci, softwaru pro stolní počítače nebo mobilní aplikaci, pochopení toho, jak změnit velikost obrázků při zachování jejich poměru stran, je zásadní pro zachování vizuální přitažlivosti a konzistence.

## Předpoklady

Než se ponoříte do magie změny velikosti s Aspose.PSD pro .NET, ujistěte se, že máte splněny následující předpoklady:

1.  Aspose.PSD for .NET Library: Ujistěte se, že máte nainstalovanou knihovnu Aspose.PSD for .NET. Můžete si jej stáhnout z[Aspose.PSD pro vydání .NET](https://releases.aspose.com/psd/net/) strana.

2. Adresář dokumentů: Vytvořte adresář pro ukládání dokumentů a nahraďte "Váš adresář dokumentů" v poskytnutém kódu skutečnou cestou k tomuto adresáři.

Nyní, když máte nastavené předpoklady, pojďme se vrhnout na průvodce krok za krokem.

## Importovat jmenné prostory

```csharp
using Aspose.PSD.ImageOptions;
```

Importujte potřebné jmenné prostory pro přístup k požadovaným třídám a metodám.

## Krok 1: Načtěte obrázek

```csharp
// Cesta k adresáři dokumentů.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Načtěte existující obrázek do instance třídy RasterImage
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// Zbývající kroky jděte sem
}
```

 Načtěte zdrojový obrázek pomocí`Image.Load` metoda.

## Krok 2: Zadejte šířku a výšku

```csharp
// Určení šířky a výšky
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Určete novou šířku a výšku obrázku se změněnou velikostí. V tomto příkladu jsou šířka a výška poloviční, ale tyto hodnoty můžete upravit podle svých požadavků.

## Krok 3: Uložte obrázek se změněnou velikostí

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Uložte obrázek se změněnou velikostí pomocí`Save` metoda se zadanými možnostmi. V tomto případě jej ukládáme jako soubor PNG.

## Závěr

Proporcionální změna velikosti obrázků v Aspose.PSD pro .NET je přímočarý proces, který přidává hodnotu vašemu pracovnímu postupu zpracování obrázků. Tato příručka vás vybavila znalostmi pro bezproblémovou integraci této funkce do vašich aplikací.

## FAQ

### Q1: Mohu změnit velikost obrázků na konkrétní rozměry?

A1: Ano, můžete přizpůsobit novou šířku a výšku podle vašich požadavků v kódu.

### Q2: Je Aspose.PSD pro .NET vhodný pro dávkovou změnu velikosti obrázku?

A2: Rozhodně! Tyto kroky můžete začlenit do smyčky pro dávkové zpracování více obrázků.

### Q3: Existují další funkce pro manipulaci s obrázky v Aspose.PSD pro .NET?

Odpověď 3: Ano, Aspose.PSD pro .NET nabízí širokou škálu funkcí, včetně oříznutí, otočení a použití filtrů na obrázky.

### Q4: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro .NET?

 A4: Ano, můžete prozkoumat možnosti Aspose.PSD pro .NET pomocí bezplatné zkušební verze. Návštěva[zde](https://releases.aspose.com/) začít.

### Q5: Kde najdu podporu pro Aspose.PSD pro .NET?

 A5: Navštivte[Aspose.PSD for .NET fórum](https://forum.aspose.com/c/psd/34) za podporu komunity a diskuze.