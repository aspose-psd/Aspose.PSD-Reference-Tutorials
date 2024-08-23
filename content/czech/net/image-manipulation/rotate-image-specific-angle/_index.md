---
title: Otočení obrázku pod určitým úhlem v Aspose.PSD pro .NET
linktitle: Otočení obrázku pod určitým úhlem
second_title: Aspose.PSD .NET API
description: Prozkoumejte sílu Aspose.PSD pro .NET. Otočte snímky bez námahy ve specifických úhlech. Stáhněte si knihovnu a začněte bez problémů manipulovat s obrázky.
type: docs
weight: 16
url: /cs/net/image-manipulation/rotate-image-specific-angle/
---
Pokud se ponoříte do světa manipulace s obrázky pomocí .NET, Aspose.PSD poskytuje výkonné řešení. V tomto tutoriálu vás provedeme procesem otáčení obrázku pod určitým úhlem pomocí Aspose.PSD. Než se vrhneme na kroky, připravíme jeviště úvodem.

## Zavedení

Aspose.PSD for .NET je všestranná knihovna, která umožňuje vývojářům bezproblémově pracovat s formáty PSD a rastrových obrázků. Jednou z jeho klíčových vlastností je schopnost otáčet obrázky v přesných úhlech, což poskytuje flexibilitu při manipulaci s obrázky. Tento tutoriál vás provede kroky k otočení obrázku v určitém úhlu pomocí Aspose.PSD for .NET.

## Předpoklady

Než se vydáme na tuto cestu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.PSD for .NET Library: Stáhněte a nainstalujte knihovnu z[stránka ke stažení](https://releases.aspose.com/psd/net/).
- Adresář dokumentů: Nastavte adresář pro ukládání zdrojových a výstupních souborů.

## Importovat jmenné prostory

Chcete-li začít, importujte potřebné jmenné prostory do svého projektu .NET:

```csharp
using Aspose.PSD.ImageOptions;
```

Nyní si příklad rozdělíme do několika kroků ve formátu podrobného průvodce.

## Krok 1: Nastavte adresář dokumentů

```csharp
string dataDir = "Your Document Directory";
```

 Nahradit`"Your Document Directory"` s cestou k adresáři, kam ukládáte zdrojové a výstupní soubory.

## Krok 2: Načtěte obrázek

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    // Zde budou vloženy další kroky
}
```

 Načtěte obrázek, který chcete otočit, do instance`RasterImage`.

## Krok 3: Uložte data obrázku do mezipaměti

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

Uložte obrazová data do mezipaměti pro lepší výkon při otáčení.

## Krok 4: Otočte obrázek

```csharp
image.Rotate(20f, true, Color.Red);
```

Otočte obrázek o 20 stupňů, zachovejte proporcionální velikost a použijte červené pozadí.

## Krok 5: Uložte výsledek

```csharp
image.Save(destName, new JpegOptions());
```

Uložte otočený obrázek se zadanými možnostmi (v tomto případě jako JPEG).

## Závěr

 Gratuluji! Úspěšně jste otočili obrázek v určitém úhlu pomocí Aspose.PSD pro .NET. Tato knihovna poskytuje robustní sadu nástrojů pro manipulaci s obrázky a tento tutoriál je jen špičkou ledovce. Prozkoumat[dokumentace](https://reference.aspose.com/psd/net/) pro více funkcí a možností.

## FAQ

### Q1: Mohu otáčet obrázky o jiné úhly než 20 stupňů?

 A1: Ano, můžete upravit parametr úhlu v`image.Rotate` metodou na libovolnou požadovanou hodnotu.

### Q2: Podporuje Aspose.PSD jiné obrazové formáty kromě JPEG?

A2: Rozhodně! Aspose.PSD podporuje širokou škálu formátů, včetně PNG, GIF, BMP a TIFF.

### Otázka 3: Je nutné před otočením uložit obrazová data do mezipaměti?

Odpověď 3: I když to není povinné, ukládání dat do mezipaměti může výrazně zvýšit výkon, zejména u větších obrázků.

### Q4: Kde mohu získat podporu pro dotazy související s Aspose.PSD?

 A4: Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) za podporu komunity a diskuze.

### Q5: Mohu vyzkoušet Aspose.PSD před nákupem?

 A5: Určitě! Chyťte se[zkušební verze zdarma](https://releases.aspose.com/)prozkoumat možnosti knihovny.