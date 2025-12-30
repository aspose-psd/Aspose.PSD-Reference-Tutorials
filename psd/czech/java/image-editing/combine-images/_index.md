---
date: 2025-12-30
description: Naučte se, jak vytvořit soubor PSD v Javě kombinací dvou obrázků pomocí
  Aspose.PSD. Postupujte podle našeho krok‑za‑krokem průvodce a rychle sloučte obrázky
  do souboru PSD.
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: Jak vytvořit PSD soubor v Javě – Kombinovat obrázky pomocí Aspose.PSD
url: /cs/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvoření souboru PSD v Javě – Kombinace obrázků pomocí Aspose.PSD

## Úvod

Pokud potřebujete **vytvořit soubor PSD v Javě** sloučením několika obrázků, Aspose.PSD vám práci usnadní. V tomto tutoriálu projdeme kombinaci dvou obrázků do jedné PSD plátna, vysvětlíme, proč je tento přístup užitečný, a poskytneme připravený kód. Na konci budete schopni **kombinovat dva obrázky v Javě** a vygenerovat profesionálně vypadající vrstvený soubor.

## Rychlé odpovědi
- **Která knihovna je nejlepší pro sloučení obrázků do PSD?** Aspose.PSD pro Java.
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní kombinaci.
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence.
- **Mohu přidat více než dva obrázky?** Ano – opakujte volání `drawImage` pro každou další vrstvu.
- **Která verze Javy je podporována?** Java 8 a novější.

## Předpoklady

Než se pustíte do práce, ujistěte se, že máte následující:

1. **Aspose.PSD knihovna** – stáhněte ji [zde](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – doporučena verze Java 8+.  
3. **Adresář dokumentů** – složka ve vašem počítači, kde budou uloženy zdrojové obrázky i výsledný PSD.

## Import balíčků

Začněte importováním potřebných tříd Aspose.PSD do vašeho projektu:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## Průvodce krok za krokem

### Krok 1: Vytvoření PSD možností (příprava souboru)

Nejprve vytvoříme instanci `PsdOptions`, která bude obsahovat nastavení výstupu.

```java
PsdOptions imageOptions = new PsdOptions();
```

### Krok 2: Nastavení FileCreateSource (definice místa uložení PSD)

Přiřaďte `FileCreateSource` k možnostem a určete požadovaný výstupní soubor.

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### Krok 3: Vytvoření instance Image (inicializace velikosti plátna)

Vytvořte objekt `Image` s možnostmi a specifikujte plátno o rozměrech 600 × 600 pixelů.

```java
Image image = Image.create(imageOptions, 600, 600);
```

### Krok 4: Inicializace Graphics a vykreslení prvního obrázku

Objekt `Graphics` nám umožní kreslit na plátno. Vyčistíme pozadí na bílou a vykreslíme první zdrojový obrázek na levou polovinu.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### Krok 5: Vykreslení druhého obrázku (dokončení kombinace)

Nyní umístíme druhý obrázek na pravou polovinu stejného plátna.

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### Krok 6: Uložení výsledného PSD souboru

Nakonec uložíme kombinované plátno na disk.

```java
image.save();
```

Gratulujeme! Úspěšně jste **sloučili obrázky do PSD** a vytvořili soubor PSD v Javě.

## Proč kombinovat obrázky pomocí Aspose.PSD?

- **Vrstvené** – každé volání `drawImage` přidá samostatnou vrstvu, kterou můžete později upravit.  
- **Flexibilita formátů** – podporuje PSD, PNG, JPEG, BMP a další.  
- **Žádné nativní závislosti** – čistá Java, funguje na jakémkoli OS, který spouští JDK.  

## Časté problémy a řešení

| Problém | Příčina | Oprava |
|-------|-------|-----|
| Chyba `File not found` při načítání zdrojových obrázků | Nesprávná cesta `dataDir` | Ověřte, že `dataDir` ukazuje na složku obsahující `example1.psd` a `example2.psd`. |
| Výstupní PSD je prázdný | `graphics.clear` bylo zavoláno po vykreslení | Ujistěte se, že `graphics.clear(Color.getWhite())` je provedeno **před** jakýmkoli voláním `drawImage`. |
| Výjimka licence za běhu | Chybějící nebo prošlá licence Aspose.PSD | Aplikujte platnou licenci pomocí `License license = new License(); license.setLicense("Aspose.PSD.lic");` před jakýmkoli voláním API. |

## Často kladené otázky

### Q1: Je Aspose.PSD kompatibilní se všemi formáty obrázků?
A1: Aspose.PSD se primárně zaměřuje na formát PSD. Nicméně podporuje různé další formáty pro vstup i výstup.

### Q2: Mohu provádět další úpravy na sloučeném obrázku?
A2: Rozhodně! Po sloučení obrázků můžete dále manipulovat s výsledným PSD pomocí rozsáhlých funkcí Aspose.PSD.

### Q3: Existují licenční požadavky pro používání Aspose.PSD?
A3: Ano, pro komerční použití je vyžadována platná licence. Získejte ji [zde](https://purchase.aspose.com/buy).

### Q4: Je k dispozici bezplatná zkušební verze Aspose.PSD?
A4: Ano, bezplatnou zkušební verzi můžete vyzkoušet [zde](https://releases.aspose.com/).

### Q5: Kde mohu najít podporu pro dotazy týkající se Aspose.PSD?
A5: Navštivte [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pro komunitní podporu a diskuze.

---

**Poslední aktualizace:** 2025-12-30  
**Testováno s:** Aspose.PSD 24.11 pro Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}