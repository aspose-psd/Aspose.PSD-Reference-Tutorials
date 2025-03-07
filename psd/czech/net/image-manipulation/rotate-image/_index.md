---
title: Otočení obrázku v Aspose.PSD pro .NET
linktitle: Otočení obrázku
second_title: Aspose.PSD .NET API
description: Naučte se otáčet obrázky bez námahy v .NET s Aspose.PSD. Postupujte podle našeho podrobného návodu.
weight: 15
url: /cs/net/image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Otočení obrázku v Aspose.PSD pro .NET

## Zavedení

Pokud se ponoříte do světa manipulace s obrázky pomocí .NET, Aspose.PSD je váš oblíbený nástroj pro bezproblémové a efektivní zpracování obrázků. V tomto tutoriálu se zaměříme na základní úkol – otáčení obrázku pomocí Aspose.PSD for .NET. Následujte, jak celý proces rozdělíme do jednoduchých, proveditelných kroků.

## Předpoklady

Než začneme, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.PSD for .NET Library: Stáhněte a nainstalujte knihovnu z[Dokumentace Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- Your Document Directory: Nastavte adresář, kde jsou uloženy vaše obrázky. Nahraďte "Your Document Directory" ve fragmentu kódu cestou k tomuto adresáři.

## Importovat jmenné prostory

Ujistěte se, že jste zahrnuli potřebné jmenné prostory pro přístup k funkcím Aspose.PSD. Na začátek svého projektu .NET přidejte následující řádky:

```csharp
using Aspose.PSD.ImageOptions;
```

## Krok 1: Načtěte obrázek

```csharp
string sourceFile = dataDir + @"sample.psd";

// Načtěte existující obrázek do instance třídy RasterImage
using (Image image = Image.Load(sourceFile))
{
```

## Krok 2: Otočte obrázek

```csharp
    // Otočte obrázek o 270 stupňů ve směru hodinových ručiček
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Krok 3: Uložte otočený obrázek

```csharp
    // Uložte otočený obrázek jako soubor JPEG
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

To je vše! Pomocí několika řádků kódu jste úspěšně otočili obrázek pomocí Aspose.PSD pro .NET.

## Závěr

tomto tutoriálu jsme prozkoumali základy otáčení obrázků pomocí Aspose.PSD pro .NET. Aspose.PSD poskytuje robustní sadu nástrojů pro manipulaci s obrázky, což z něj činí základní knihovnu pro vývojáře .NET. Experimentujte s různými rotacemi a prozkoumejte další možnosti pro vylepšení pracovních postupů zpracování obrazu.

## FAQ

### Q1: Mohu otočit obrázky o vlastní úhel pomocí Aspose.PSD?

 Ano, Aspose.PSD umožňuje zadat vlastní úhel pro rotaci. Jednoduše vyměňte`RotateFlipType.Rotate270FlipNone` linii s požadovaným úhlem natočení.

### Q2: Je Aspose.PSD kompatibilní s různými formáty obrázků?

 Absolutně. Aspose.PSD podporuje širokou škálu obrazových formátů, včetně PSD, JPEG, PNG a dalších. Zkontrolujte[dokumentace](https://reference.aspose.com/psd/net/) pro úplný seznam.

### Q3: Jak mohu získat dočasnou licenci pro Aspose.PSD?

 Navštivte[dočasná licenční stránka](https://purchase.aspose.com/temporary-license/) na webu Aspose k získání dočasné licence pro účely hodnocení.

### Q4: Kde najdu podporu pro Aspose.PSD?

 V případě jakýchkoli dotazů nebo pomoci navštivte stránku[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) a spojit se s komunitou.

### Q5: Mohu zakoupit Aspose.PSD pro komerční použití?

 Jistě. Prozkoumat[nákupní stránku](https://purchase.aspose.com/buy) získat licenci přizpůsobenou vašim potřebám.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
