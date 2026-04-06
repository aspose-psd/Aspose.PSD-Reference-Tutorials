---
date: 2026-01-12
description: Naučte se, jak převést soubory Illustrator do PNG v Javě pomocí Aspose.PSD.
  Tento krok‑za‑krokem průvodce ukazuje, jak načíst AI soubory, nastavit možnosti
  PNG a uložit obrázek jako PNG.
linktitle: Convert AI to PNG in Java
second_title: Aspose.PSD Java API
title: Převod Illustratoru do PNG v Javě – Průvodce Aspose.PSD
url: /cs/java/java-ai-to-image-format-conversion/convert-ai-to-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod Illustratoru na PNG v Javě

## Úvod
Pokud potřebujete **převést Illustrator na PNG** programově, jste na správném místě. V tomto tutoriálu projdeme celý proces pomocí knihovny Aspose.PSD pro Java. Pouhých několik řádků kódu vám umožní načíst soubor AI, upravit nastavení PNG a uložit výsledek jako vysoce kvalitní PNG obrázek. Pojďme začít!

## Rychlé odpovědi
- **Jaká knihovna provádí převod AI → PNG?** Aspose.PSD for Java  
- **Kolik řádků kódu je potřeba?** Přibližně 15 řádků (importy + 3 kroky)  
- **Potřebuji licenci pro produkci?** Ano, je vyžadována komerční licence (k dispozici je bezplatná zkušební verze)  
- **Podporované verze Javy? J 8 a vyšší  
- **Mohu dávkově zpracovávat více souborů AI?** Ano – stačí provést smyčku přes kroky uvedené níže  

## Co znamená „převod illustratoru na png“?
Převod souborů Illustrator (AI) na PNG znamená vykreslení vektorové grafiky do rastrového formátu. PNG zachovává průhlednost a nabízí bezztrátovou kompresi, což je ideální pro webovou grafiku, UI assety a náhledy.

## Proč použít Aspose.PSD pro tento převod?
- **Kompletní podpora formátů** – Zpracovává AI, PSD, PSB a mnoho dalších Adobe formátů.  
- **Žádné externí závislosti** – Čistá Java, nevyžaduje nativní knihovny.  
- **Detailní kontrola** – Můžete specifikovat typ barvy PNG, úroveň komprese a další.  
- **Škálovatelné** – Funguje stejně dobře pro jednotlivé soubory i velké dávkové úlohy.

## Předpoklady
1. **Java Development Kit (JDK)** – Nainstalovaný JDK 8 nebo novější.  
2. **Aspose.PSD for Java** – Stáhněte z [stránky vydání Aspose](https://releases.aspose.com/psd/java/) nebo získáte [bezplatnou zkušební verzi](https://releases.aspose.com/).  
3. **IDE** – IntelliJ IDEA, Eclipse, NetBeans nebo jakýkoli editor kompatibilní s Javou.  
4. **Základní znalost Javy** – Znalost tříd, metod a souborového I/O.

## Import balíčků
Nejprve importujte třídy Aspose.PSD, které budete potřebovat. Tím nastavíte prostředí pro kroky převodu.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## Průvodce krok za krokem

### Krok 1: Načtení souboru AI
Načtěte svůj soubor Illustrator do objektu `AiImage`. Tím připravíte vektorová data pro vykreslení.

```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "34992OStroke.ai";       
AiImage image = (AiImage)Image.load(sourceFileName);
```

### Krok 2: Nastavení PNG možností
Nastavte, jak bude PNG generováno. Zde volíme **Truecolor with Alpha**, aby se zachovala průhlednost.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
```

### Krok 3: Uložení obrázku jako PNG
Nakonec zapište rasterizovaný obrázek na disk pomocí výše definovaných možností.

```java
String outFileName = dataDir + "34992OStroke.png";
image.save(outFileName, options);
```

> **Tip:** Pokud potřebujete převést mnoho souborů AI, umístěte tyto tři kroky do smyčky a změňte `sourceFileName`/`outFileName` pro každou iteraci.

## Časté problémy a řešení
| Problém | Řešení |
|-------|----------|
| **Chyba nedostatku paměti u velkých AI souborů** | Zvyšte velikost haldy JVM (`-Xmx2g`) nebo zpracovávejte soubory po jednom. |
| **Průhledné pozadí se zobrazuje černě** | Ujistěte se, že je nastaven `PngColorType.TruecolorWithAlpha`; tím se zachová alfa kanál. |
| **Chybějící fonty ve výstupu** | Vložte požadované fonty do AI souboru před převodem, nebo použijte funkce substituce fontů v `AiImage`. |

## Často kladené otázky

### Co je Aspose.PSD?
Aspose.PSD je knihovna pro Javu, která umožňuje vývojářům pracovat se soubory PSD (Photoshop) a dalšími Adobe formáty. Podporuje různé operace, jako je úprava, převod a vykreslování.

### Můžu používat Aspose.PSD zdarma?
Aspose.PSD můžete používat s [bezplatnou zkušební verzí](https://releases.aspose.com/), ale pro plnou funkčnost je nutné zakoupit licenci. Pro evaluační účely můžete také získat [dočasnou licenci](https://purchase.aspose.com/temporary-license/).

### Jaké souborové formáty Aspose.PSD podporuje?
Aspose.PSD podporuje PSD, PSB, AI a další Adobe formáty. Umožňuje převod do různých formátů obrázků, jako jsou PNG, JPEG, BMP a TIFF.

### Je Aspose.PSD kompatibilní se všemi verzemi Javy?
Aspose.PSD je kompatibilní s JDK 8 a vyššími. Ujistěte se, že máte nainstalovanou odpovídající verzi JDK.

### Kde najdu další dokumentaci?
Podrobnou dokumentaci najdete na [stránce dokumentace Aspose.PSD](https://reference.aspose.com/psd/java/).

---

**Poslední aktualizace:** 2026-01-12  
**Testováno s:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}