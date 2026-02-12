---
date: 2026-02-12
description: Naučte se, jak změnit velikost obrázku v Javě pomocí Aspose.PSD pro Javu.
  Podrobný návod krok za krokem s výčtem typů změny velikosti a tipy na převod PSD
  do JPEG.
linktitle: Resizing with Resize Type Enumeration
second_title: Aspose.PSD Java API
title: Změna velikosti obrázku v Javě – Použití výčtu typu změny velikosti v Aspose.PSD
  pro Javu
url: /cs/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Resize Image Java: Použití výčtu typu změny velikosti v Aspose.PSD pro Javu

## Úvod

Změna velikosti obrázků je běžnou požadavkem v Java aplikacích a operace **resize image java** se stávají snadnými s Aspose.PSD. V tomto tutoriálu se naučíte, jak **resize image java** pomocí výkonného výčtu Resize Type, a také uvidíte, jak **convert psd to jpeg** po změně velikosti. Ať už vytváříte desktopový nástroj nebo server‑side službu, tyto kroky vám pomohou spolehlivě pracovat s rozměry obrázku a dosáhnout vysoce kvalitní změny velikosti obrázku.

## Rychlé odpovědi
- **Jaká knihovna zpracovává resize image java?** Aspose.PSD for Java.  
- **Který typ změny velikosti poskytuje nejlepší kvalitu?** `ResizeType.LanczosResample`.  
- **Mohu po změně velikosti převést PSD na JPEG?** Yes – just save with `JpegOptions`.  
- **Potřebuji licenci pro produkci?** A valid Aspose.PSD license is required for production use.  
- **Je tento přístup vhodný pro velké dávky?** Absolutely; the API is optimized for performance.

## Co je Resize Image Java?

Termín “resize image java” označuje programatickou změnu pixelových rozměrů obrázku pomocí Java kódu. Aspose.PSD poskytuje stručné API, které abstrahuje nízkoúrovňovou manipulaci s pixely, takže se můžete soustředit na obchodní logiku místo detailů zpracování obrázků.

## Proč použít výčet Resize Type?

Výčet Resize Type vám poskytuje detailní kontrolu nad algoritmem přeresamplování, což vám umožňuje vyvážit rychlost a kvalitu. Pro většinu aplikací `LanczosResample` nabízí skvělý kompromis, poskytuje ostré výsledky bez velkého dopadu na výkon. Výběr správného typu změny velikosti je klíčový pro dosažení vysoce kvalitní změny velikosti obrázku.

## Požadavky

Před zahájením tohoto tutoriálu se ujistěte, že máte následující požadavky:

1. **Java Development Environment** – nainstalovaný a nakonfigurovaný JDK 8+.  
2. **Aspose.PSD Library** – stáhněte a nainstalujte knihovnu Aspose.PSD z [webu](https://releases.aspose.com/psd/java/).  
3. **Sample PSD File** – připravte ukázkový PSD soubor pro experimentování. Pro tento tutoriál můžete použít soubor [sample.psd](Your Document Directory/sample.psd).

## Import balíčků

Pro začátek importujte potřebné balíčky do vašeho Java projektu:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Krok 1: Načtení obrázku

Začněte načtením existujícího obrázku do instance třídy `RasterImage`. Použijte následující úryvek kódu:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Krok 2: Změna velikosti obrázku

Nyní změňte velikost načteného obrázku pomocí výčtu Resize Type. V tomto příkladu používáme metodu Lanczos Resample, která je ideální, když **how to resize image** s vysokou kvalitou:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Krok 3: Uložení změněného obrázku

Po změně velikosti uložte obrázek s určenými rozměry a zvoleným typem změny velikosti. Zde také ukazujeme **convert psd to jpeg** uložením výsledku jako JPEG soubor:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

Nyní jste provedli kompletní workflow **resize image java**, který vytváří vysoce kvalitní změnu velikosti obrázku a připravený JPEG výstup.

## Časté problémy a řešení

- **Obrázek je po změně rozmazaný** – Vyzkoušejte jiný `ResizeType`, například `Bicubic` nebo `NearestNeighbour`, abyste zjistili, který poskytne nejlepší vizuální výsledek pro váš konkrétní obrázek.  
- **OutOfMemoryError u velkých PSD souborů** – Zpracovávejte obrázek v menších částech nebo zvýšte velikost haldy JVM (`-Xmx` flag).  

## Často kladené otázky

### Q1: Je Aspose.PSD pro Javu vhodný jak pro malé, tak pro rozsáhlé projekty?

A1: Rozhodně! Aspose.PSD pro Javu je navržen tak, aby vyhovoval projektům všech velikostí, poskytuje škálovatelnost a efektivitu.

### Q2: Mohu použít jiný typ změny velikosti než Lanczos Resample?

A2: Ano, Aspose.PSD pro Javu nabízí různé typy změny velikosti, jako Nearest Neighbour, Bicubic a další. Prozkoumejte dokumentaci pro úplný seznam.

### Q3: Kde mohu najít další podporu pro Aspose.PSD pro Javu?

A3: Pro jakékoli dotazy nebo pomoc navštivte [Aspose.PSD fórum](https://forum.aspose.com/c/psd/34).

### Q4: Je k dispozici bezplatná zkušební verze Aspose.PSD pro Javu?

A4: Ano, bezplatnou zkušební verzi můžete získat [zde](https://releases.aspose.com/).

### Q5: Jak mohu získat dočasnou licenci pro Aspose.PSD pro Javu?

A5: Pro získání dočasné licence navštivte [tento odkaz](https://purchase.aspose.com/temporary-license/).

## Často kladené otázky

**Q: Jak programově převést PSD soubor na JPEG bez změny velikosti?**  
A: Načtěte PSD pomocí `Image.load`, poté zavolejte `image.save("output.jpg", new JpegOptions());`.

**Q: Je možné zachovat původní DPI při změně velikosti?**  
A: Ano, můžete nastavit vlastnost `Resolution` na objektu `Image` před uložením.

**Q: Mohu řetězit více operací změny velikosti?**  
A: I když můžete volat `resize` vícekrát, je efektivnější vypočítat konečné rozměry a změnit velikost jednou.

## Další FAQ

**Q: Ovlivňuje výčet Resize Type rychlost zpracování?**  
A: Ano, jednodušší algoritmy jako `NearestNeighbour` jsou rychlejší, ale mohou produkovat nižší kvalitu výsledků, zatímco `LanczosResample` nabízí vyšší kvalitu za mírný výkonový náklad.

**Q: Mohu měnit velikost obrázků v multi‑threaded prostředí?**  
A: API Aspose.PSD je thread‑safe pro operace pouze ke čtení. Pro souběžnou změnu velikosti vytvořte pro každý vlákno samostatné instance `Image`.

**Q: Jak zacházet s obrázky s alfa kanály během změny velikosti?**  
A: Knihovna ve výchozím nastavení zachovává alfa průhlednost. Pokud potřebujete obrázek zploštit, nastavte barvu pozadí před uložením.

---

**Poslední aktualizace:** 2026-02-12  
**Testováno s:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}