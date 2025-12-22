---
date: 2025-12-19
description: Naučte se, jak upravit jas obrázku pomocí Aspose.PSD pro Javu. Tento
  tutoriál pro manipulaci s obrázky v Javě poskytuje krok za krokem návod.
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: Jak upravit jas obrázku pomocí Aspose.PSD pro Javu
url: /cs/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Upravit jas obrázku pomocí Aspose.PSD pro Java

## Úvod

Pokud potřebujete **se naučit, jak upravit jas** obrázku přímo z Java kódu, jste na správném místě. Úprava jasu je častý úkol pro grafické designéry, fotografy a každého, kdo buduje pipeline pro zpracování obrázků. V tomto **java image manipulation tutorial** projdeme kompletní workflow – načtení PSD/TIFF, aplikaci offsetu jasu a uložení výsledku – pomocí knihovny Aspose.PSD pro Java.

## Rychlé odpovědi
- **Jaká knihovna zpracovává jas?** Aspose.PSD pro Java  
- **Která metoda mění jas?** `RasterImage.adjustBrightness()`  
- **Mohu pracovat se soubory PSD a TIFF?** Ano, API podporuje oba formáty.  
- **Potřebuji licenci pro produkci?** Komerční licence je vyžadována pro ne‑evaluační použití.  
- **Jak dlouho trvá implementace?** Obvykle méně než 10 minut pro základní úpravu.

## Co je úprava jasu obrázku?

Úprava jasu obrázku mění celkovou světlost každého pixelu v obrázku. Zvýšením jasu se tmavé oblasti zesvětlí, snížením jasu se celý obrázek ztmaví. Tato operace je užitečná pro korekci podexponovaných fotografií, přípravu materiálů k tisku nebo tvorbu vizuálních efektů v aplikacích.

## Proč použít Aspose.PSD pro Java?

- **Plná podpora formátů** – PSD, TIFF, JPEG, PNG a další.  
- **Žádné externí nativní závislosti** – čistě Java, snadná integrace.  
- **Vysoce výkonná cache** – rastrová data lze cachovat pro rychlejší opakované operace.  
- **Bohaté API** – metody pro korekci barev, vrstvy, masky a další pokročilé úpravy.

## Požadavky

Před tím, než se ponoříte do tutoriálu, ujistěte se, že máte následující požadavky:

- Aspose.PSD pro Java Library: Stáhněte a nainstalujte knihovnu z [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

## Importování balíčků

Pro začátek importujte potřebné balíčky do svého Java projektu. V tomto příkladu použijeme následující:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Nyní rozdělíme proces úpravy jasu obrázku na jednoduché kroky:

## Jak upravit jas pomocí Aspose.PSD

### Krok 1: Načíst obrázek

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

V tomto kroku načteme cílový obrázek a přetypujeme jej na `RasterImage` pro další zpracování.

### Krok 2: Upravit jas

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Zde používáme metodu `adjustBrightness` k úpravě jasu obrázku. V tomto příkladu snížíme jas o 50 jednotek, ale můžete tuto hodnotu přizpůsobit podle svých požadavků.

### Krok 3: Nastavit TiffOptions

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Nakonfigurujte `TiffOptions` pro uložení upraveného obrázku. Upravit vlastnosti `bitsPerSample` a `photometric` podle konkrétních potřeb.

### Krok 4: Uložit výsledný obrázek

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Nakonec uložte modifikovaný obrázek pomocí specifikovaných `TiffOptions`.

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|---------|-------|--------|
| **`ClassCastException` při přetypování Image** | Soubor není rastrový obrázek (např. vektorový PSD). | Ověřte formát zdrojového souboru nebo použijte `image instanceof RasterImage` před přetypováním. |
| **Změna jasu nemá žádný efekt** | Obrázek nebyl před úpravou cachován. | Zavolejte `rasterImage.cacheData()` jak je ukázáno v Kroku 1. |
| **Uložený soubor se jeví jako poškozený** | Nesprávná konfigurace `TiffOptions`. | Ujistěte se, že `bitsPerSample` odpovídá hloubce zdrojového obrázku (obvykle 8‑bit na kanál). |

## Často kladené otázky

### Q1: Mohu upravit jas i v jiných formátech obrázků než PSD?

A1: Ano, Aspose.PSD pro Java podporuje různé formáty obrázků jako JPEG, PNG a TIFF.

### Q2: Jak mohu ošetřit chyby během procesu úpravy obrázku?

A2: Můžete implementovat ošetření chyb pomocí bloků try‑catch pro správu výjimek, které mohou nastat.

### Q3: Existuje limit rozsahu úpravy jasu?

A3: Rozsah úpravy závisí na obsahu a formátu obrázku, ale Aspose.PSD poskytuje flexibilitu v přizpůsobení.

### Q4: Mohu používat Aspose.PSD pro Java v komerčních projektech?

A4: Ano, Aspose.PSD pro Java je komerční knihovna a můžete získat licenci [zde](https://purchase.aspose.com/buy).

### Q5: Je k dispozici bezplatná zkušební verze Aspose.PSD pro Java?

A5: Ano, můžete si knihovnu vyzkoušet zdarma [zde](https://releases.aspose.com/).

### Q6: Ovlivňuje metoda `adjustBrightness` viditelnost vrstev?

A6: Metoda pracuje na rasterizovaném kompozitním obrázku, takže viditelnost vrstev je respektována během rasterizace.

### Q7: Mohu řetězit více úprav (např. kontrast, saturaci) najednou?

A7: Rozhodně. Po úpravě jasu můžete na stejném `RasterImage` volat `adjustContrast`, `adjustSaturation` a další metody.

**Poslední aktualizace:** 2025-12-19  
**Testováno s:** Aspose.PSD pro Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}