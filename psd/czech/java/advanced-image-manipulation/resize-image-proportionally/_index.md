---
date: 2025-12-08
description: Naučte se, jak převést PSD na PNG a proporčně měnit velikost obrázků
  v Javě pomocí Aspose.PSD. Tento krok‑za‑krokem tutoriál pokrývá cachování obrázků,
  změnu velikosti a ukládání jako PNG.
language: cs
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Jak převést PSD na PNG a změnit velikost proporcionálně pomocí Aspose.PSD pro
  Javu
url: /java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak převést PSD na PNG a měnit velikost proporcionálně pomocí Aspose.PSD pro Java

## Úvod

Pokud potřebujete **převést PSD na PNG** a zachovat původní poměr stran, jste na správném místě. V tomto tutoriálu projdeme kompletní **Aspose.PSD tutoriál**, který vám ukáže **jak měnit velikost obrázku** proporčně v Javě, jak kešovat obrázek pro optimální výkon a nakonec výsledek uložit jako PNG. Na konci budete schopni tento postup integrovat do jakéhokoli Java‑založeného zpracování obrázků.

## Rychlé odpovědi
- **Může Aspose.PSD převést PSD na PNG?** Ano – stačí načíst PSD a uložit jej pomocí `PngOptions`.
- **Podporuje knihovna proporcionální změnu velikosti?** Rozhodně; použijte `resizeWidthProportionally` a `resizeHeightProportionally`.
- **Je potřeba nejprve kešovat obrázek?** Kešování (`image.cacheData()`) zlepšuje výkon u velkých PSD souborů.
- **Jaká verze Javy je vyžadována?** Java 8 nebo novější je plně podporována.
- **Je pro produkci vyžadována licence?** Ano, komerční licence odstraňuje vodotisky z hodnocení.

## Co je „převést PSD na PNG“ a proč je to důležité?

Převod Photoshop dokumentu (PSD) na soubor portable network graphics (PNG) vám umožní sdílet vrstvené návrhy jako lehký, web‑přátelský formát. PNG zachovává průhlednost a bezztrátovou kvalitu, což ho činí ideálním pro UI assety, miniatury nebo jakýkoli scénář, kde je důležitá věrnost obrazu.

## Proč měnit velikost obrázku proporcionálně v Javě?

Změna velikosti **jak měnit velikost obrázku** bez zkreslení poměru stran zajišťuje, že grafika vypadá přirozeně na různých obrazovkách. API `Aspose.PSD` poskytuje dedikované metody pro proporcionální škálování, které automaticky vypočítají odpovídající výšku nebo šířku, čímž vás ušetří od ručních matematických chyb.

## Předpoklady

Než se ponoříme do kódu, ujistěte se, že máte:

1. **Java Development Kit (JDK)** – nainstalovanou Javu 8 nebo novější.
2. **Aspose.PSD for Java** – stáhněte nejnovější JAR z oficiální stránky [here](https://releases.aspose.com/psd/java/).
3. Vzorek souboru PSD (`sample.psd`) umístěný v adresáři, na který můžete odkazovat ze svého projektu.

## Import balíčků

Přidejte potřebné importy do své Java třídy. Tyto třídy vám poskytují přístup k načítání obrázků, kešování, změně velikosti a možnostem výstupu PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Načíst PSD obrázek

Nejprve načtěte zdrojový PSD soubor. Pokud je soubor velký, kešování dat obrázku snižuje zatížení paměti při provádění následných operací.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Krok 2: Proporcionální změna velikosti obrázku (Java)

Nyní určete nové rozměry. V tomto příkladu zmenšíme obrázek na **polovinu** jeho původní velikosti při zachování poměru stran. Cílovou šířku nebo výšku můžete upravit podle potřeby.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Tip:** Použijte buď `resizeWidthProportionally` *nebo* `resizeHeightProportionally`—knihovna automaticky vypočítá druhý rozměr, aby obrázek zůstal proporcionální.

## Krok 3: Uložit změněný obrázek jako PNG

Nakonec exportujte změněný obrázek do formátu PNG. Tento krok dokončuje workflow **převést PSD na PNG**.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Po spuštění kódu najdete PNG soubor, který je o polovinu menší než původní PSD, se stejnou vizuální kvalitou a bez zkreslení.

## Časté problémy a řešení

| Issue | Cause | Fix |
|-------|-------|-----|
| **OutOfMemoryError** | Velký PSD není kešován | Zavolejte `image.cacheData()` před změnou velikosti |
| **Blank PNG output** | Nesprávná cesta k souboru | Ověřte `dataDir` a oprávnění k zápisu |
| **Aspect ratio looks off** | Používání šířky i výšky ručně | Použijte proporcionální metody poskytované Aspose.PSD |

## Často kladené otázky

**Q: Je Aspose.PSD kompatibilní se všemi formáty obrázků?**  
A: Aspose.PSD podporuje PSD, PNG, JPEG, BMP, GIF a mnoho dalších. Kompletní seznam najdete v [dokumentaci](https://reference.aspose.com/psd/java/).

**Q: Mohu použít Aspose.PSD pro komerční projekty?**  
A: Ano. Zakupte komerční licenci v [Aspose store](https://purchase.aspose.com/buy).

**Q: Jsou k dispozici dočasné licence pro testování?**  
A: Rozhodně – požádejte o dočasnou licenci [zde](https://purchase.aspose.com/temporary-license/) pro evaluační účely.

**Q: Kde mohu najít komunitní podporu?**  
A: Fórum [Aspose.PSD](https://forum.aspose.com/c/psd/34) je skvělé místo pro kladení otázek a sdílení řešení.

**Q: Jak získám přístup k úplné referenci API?**  
A: Podrobné dokumenty API jsou k dispozici [zde](https://reference.aspose.com/psd/java/).

## Závěr

Nyní víte, jak **převést PSD na PNG**, změnit velikost obrázku proporcionálně a efektivně spravovat kešování pomocí Aspose.PSD pro Java. Začleňte tyto kroky do svých aplikací a poskytujte rychlé, vysoce kvalitní zpracování obrázků bez nutnosti nativních instalací Photoshopu.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2025-12-08  
**Testováno s:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose