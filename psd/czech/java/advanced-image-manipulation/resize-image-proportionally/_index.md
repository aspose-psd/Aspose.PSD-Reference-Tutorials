---
date: 2026-06-23
description: Naučte se, jak převést PSD na PNG a změnit velikost obrázků proporcionálně
  v Javě pomocí Aspose.PSD. Tento podrobný návod pokrývá cachování obrázků, změnu
  velikosti a ukládání jako PNG.
keywords:
- convert psd to png
- save psd as png
- how to cache image
- resize image without distortion
- proportional image scaling
linktitle: Převést PSD na PNG a změnit velikost proporcionálně
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to convert PSD to PNG and resize images proportionally in
    Java using Aspose.PSD. This step‑by‑step tutorial covers image caching, resizing,
    and saving as PNG.
  headline: How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for
    Java
  type: TechArticle
- description: Learn how to convert PSD to PNG and resize images proportionally in
    Java using Aspose.PSD. This step‑by‑step tutorial covers image caching, resizing,
    and saving as PNG.
  name: How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – Java 8 or later installed.'
    text: '**Java Development Kit (JDK)** – Java 8 or later installed.'
  - name: '**Aspose.PSD for Java** – download the latest JAR from the official site [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – download the latest JAR from the official site [here](https://releases.aspose.com/psd/java/).'
  - name: A sample PSD file (`sample.psd`) placed in a directory you can reference
      from your project.
    text: A sample PSD file (`sample.psd`) placed in a directory you can reference
      from your project.
  type: HowTo
- questions:
  - answer: Aspose.PSD supports PSD, PNG, JPEG, BMP, GIF, and many more. See the full
      list in the [documentation](https://reference.aspose.com/psd/java/). For the
      full API reference, see the guide **here**.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Yes. Purchase a commercial license on the [Aspose store](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for commercial projects?
  - answer: Absolutely – request a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for evaluation purposes.
    question: Are temporary licenses available for testing?
  - answer: The [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) is a great place
      to ask questions and share solutions.
    question: Where can I find community support?
  - answer: Detailed API docs are available [here](https://reference.aspose.com/psd/java/).
    question: How do I access the full API reference?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Jak převést PSD na PNG a změnit velikost proporcionálně pomocí Aspose.PSD pro
  Java
url: /cs/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak převést PSD na PNG a proporciálně změnit velikost pomocí Aspose.PSD pro Java

## Úvod

Pokud potřebujete **převést PSD na PNG** a zachovat původní poměr stran, jste na správném místě. V tomto **Aspose.PSD Java** tutoriálu vás provedeme kompletním **java image processing tutorial**, který vám ukáže **jak změnit velikost obrázku** proporciálně, kešovat obrázek pro optimální výkon a nakonec uložit výsledek jako PNG. Na konci budete schopni tento workflow integrovat do libovolného Java‑založeného pipeline pro zpracování obrázků.

## Rychlé odpovědi
- **Umí Aspose.PSD převést PSD na PNG?** Ano – stačí načíst PSD a uložit jej pomocí `PngOptions`.
- **Podporuje knihovna proporciální změnu velikosti?** Rozhodně; použijte `resizeWidthProportionally` a `resizeHeightProportionally`.
- **Musím nejprve kešovat obrázek?** Kešování (`image.cacheData()`) zlepšuje výkon u velkých souborů PSD.
- **Jaká verze Javy je požadována?** Java 8 nebo novější je plně podporována.
- **Je pro produkci vyžadována licence?** Ano, komerční licence odstraňuje evaluační vodoznaky.

## Co je „převod PSD na PNG“ a proč je důležitý?

**convert PSD to PNG** znamená převod vrstveného dokumentu Photoshopu do jednovrstvového, bezztrátového souboru PNG, který zachovává průhlednost a vizuální věrnost. Tento převod vám umožní sdílet návrhy bez potřeby Photoshopu, vytvářet web‑připravená aktiva a náhledy a odlehčit těžké soubory PSD z prohlížečů klientů při zachování kvality potřebné pro UI komponenty a značku.

## Proč měnit velikost obrázku proporciálně v Javě?

Změna velikosti obrázku **bez deformace** zachovává původní poměr šířky k výšce, takže grafika si udržuje zamýšlený vzhled na jakékoli velikosti obrazovky. Proporciální škálovací metody Aspose.PSD automaticky vypočítají chybějící rozměr, čímž eliminují ruční výpočty a riziko natažených nebo zploštělých vizuálů.

## Proč je to důležité pro vývojáře

Pro vývojáře snižuje proporciální změna velikosti a převod PSD‑na‑PNG spotřebu paměti a zlepšuje rychlost načítání, což zajišťuje, že aplikace efektivně pracují s velkou grafikou. Včasným škálováním obrázků udržujete renderování UI konzistentní napříč zařízeními a odstraňujete potřebu Photoshopu na build serverech, což usnadňuje nasazení a snižuje provozní náklady.

- **Snížená velikost souboru PSD** – Škálováním velkých PSD před převodem snižujete využití paměti a urychlujete následné zpracování.  
- **Konzistentní renderování UI** – Proporciální změna velikosti zaručuje, že ikony a grafika zachovají vizuální rovnováhu napříč zařízeními.  
- **Žádná závislost na Photoshopu** – Tyto operace můžete provádět na serveru nebo v CI pipeline bez instalace Photoshopu.

## Požadavky

Předtím, než se ponoříme do kódu, ujistěte se, že máte:

1. **Java Development Kit (JDK)** – nainstalovanou Javu 8 nebo novější.  
2. **Aspose.PSD for Java** – stáhněte nejnovější JAR z oficiální stránky [here](https://releases.aspose.com/psd/java/).  
3. Vzorek souboru PSD (`sample.psd`) umístěný v adresáři, na který můžete odkazovat z vašeho projektu.

## Import balíčků

Třída `PsdImage` je jádrový objekt Aspose.PSD, který představuje soubor PSD v paměti. Importujte potřebné jmenné prostory pro práci s načítáním, kešováním, změnou velikosti a exportem do PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Načtení PSD obrázku

**Přímá odpověď:** Načtěte zdrojový soubor pomocí `new PsdImage("sample.psd")`; pak zavolejte `image.cacheData()`, aby se přednačetla data obrázku, což zabraňuje opakovanému čtení z disku během následných operací.

`cacheData()` načte celý PSD do paměti, což umožňuje rychlejší následné zpracování. Metoda `cacheData()` načte celý dokument do paměti, což umožňuje rychlejší následné zpracování velkých souborů. Nejprve načtěte zdrojový soubor PSD. Pokud je soubor velký, kešování dat obrázku snižuje zatížení paměti při provádění následných operací.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Krok 2: Proporciální změna velikosti obrázku (Java)

**Přímá odpověď:** Zavolejte `image.resizeWidthProportionally(targetWidth)` (nebo `resizeHeightProportionally`), aby se obrázek zmenšil a automaticky zachoval původní poměr stran.

`resizeWidthProportionally(int targetWidth)` mění šířku obrázku a automaticky vypočítá odpovídající výšku pro zachování původního poměru stran. Nyní určete nové rozměry. V tomto příkladu zmenšujeme obrázek na **polovinu** jeho původní velikosti při zachování poměru stran. Cílovou šířku nebo výšku můžete upravit podle potřeby.

Metoda `resizeWidthProportionally` vypočítá odpovídající výšku na základě původního poměru, takže je obrázek změněn **bez deformace**. Použijte libovolnou metodu – Aspose.PSD za vás vypočítá doplňující rozměr.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Tip:** Použijte buď `resizeWidthProportionally` *nebo* `resizeHeightProportionally` – knihovna automaticky vypočítá druhý rozměr, aby obrázek zůstal proporciální.

## Krok 3: Uložení změněného obrázku jako PNG

**Přímá odpověď:** Vytvořte instanci `PngOptions`, přiřaďte ji k obrázku a zavolejte `image.save("output.png", pngOptions)`, abyste zapsali změněný soubor ve formátu PNG.

`PngOptions` určuje nastavení pro export do PNG, jako je úroveň komprese a barevná hloubka. Nakonec exportujte změněný obrázek do formátu PNG. Tento krok dokončuje workflow **convert PSD to PNG**.

Když kód spustíte, najdete soubor PNG, který je o polovinu menší než původní PSD, se stejnou vizuální kvalitou a bez deformace.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Když kód spustíte, najdete soubor PNG, který je o polovinu menší než původní PSD, se stejnou vizuální kvalitou a bez deformace.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|---------|---------|--------|
| **OutOfMemoryError** | Velký PSD není kešován | Zavolejte `image.cacheData()` před změnou velikosti |
| **Blank PNG output** | Nesprávná cesta k souboru | Ověřte `dataDir` a oprávnění k zápisu |
| **Aspect ratio looks off** | Manuální nastavení šířky i výšky | Použijte proporciální metody poskytované Aspose.PSD |

## Tipy pro snížení velikosti souboru PSD

- **Ořízněte zbytečné vrstvy** před načtením souboru.  
- **Proporciálně změňte velikost** jak je uvedeno výše, aby se rozměry zmenšily již včas.  
- **Uložte jako PNG s vhodnou bitovou hloubkou** aby se předešlo nadbytečným datům.

## Často kladené otázky

**Q: Je Aspose.PSD kompatibilní se všemi formáty obrázků?**  
A: Aspose.PSD podporuje PSD, PNG, JPEG, BMP, GIF a mnoho dalších. Kompletní seznam najdete v [dokumentaci](https://reference.aspose.com/psd/java/). Pro kompletní referenci API viz průvodce **zde**.

**Q: Mohu používat Aspose.PSD pro komerční projekty?**  
A: Ano. Zakupte komerční licenci v [Aspose store](https://purchase.aspose.com/buy).

**Q: Jsou k dispozici dočasné licence pro testování?**  
A: Rozhodně – požádejte o dočasnou licenci [zde](https://purchase.aspose.com/temporary-license/) pro evaluační účely.

**Q: Kde mohu najít komunitní podporu?**  
A: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) je skvělé místo pro kladení otázek a sdílení řešení.

**Q: Jak získám přístup k úplné referenci API?**  
A: Podrobné API dokumenty jsou k dispozici [zde](https://reference.aspose.com/psd/java/).

## Závěr

Nyní víte, jak **převést PSD na PNG**, **proporciálně změnit velikost obrázku** a efektivně spravovat kešování pomocí Aspose.PSD pro Java. Začleňte tyto kroky do svých aplikací, abyste poskytovali rychlé a vysoce kvalitní zpracování obrázků bez závislosti na nativních instalacích Photoshopu. Tento **aspose psd java** přístup je spolehlivou součástí libovolného **java image processing tutorial** a pomáhá udržovat velikost souborů PSD pod kontrolou při zachování vizuální věrnosti.

---

**Poslední aktualizace:** 2026-06-23  
**Testováno s:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Jednoduché změny velikosti s Aspose.PSD – Knihovna pro manipulaci s obrázky v Javě](/psd/java/basic-image-operations/simple-resizing/)
- [Změna velikosti obrázku v Javě – Použití výčtu Resize Type v Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [Vysoce kvalitní škálování obrázků s Bicubic Resampler v Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}