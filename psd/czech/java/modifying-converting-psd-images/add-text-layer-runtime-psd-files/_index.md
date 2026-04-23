---
date: 2026-03-07
description: Naučte se, jak během běhu přidávat text do souborů PSD pomocí Javy a
  Aspose.PSD. Postupujte podle tohoto krok‑za‑krokem průvodce a rychle vytvořte textovou
  vrstvu v PSD.
linktitle: Add Text Layer on Runtime in PSD Files using Java
second_title: Aspose.PSD Java API
title: Přidat text do souborů PSD za běhu pomocí Javy
url: /cs/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidání textu do souborů PSD za běhu pomocí Javy

## Úvod
Pokud jste někdy ručně upravovali dokument Photoshopu, víte, jak mocné vrstvy mohou být. Co kdybyste mohli **přidávat text do PSD** souborů automaticky z vaší Java aplikace? S knihovnou Aspose.PSD pro Java můžete za běhu vytvořit textovou vrstvu v PSD, čímž otevřete dveře k dávkové zpracování, dynamické tvorbě grafiky a automatizovaným workflow značkování. V tomto tutoriálu projdeme celý proces, od nastavení projektu až po uložení aktualizovaného souboru.

## Rychlé odpovědi
- **Jaká knihovna je potřeba?** Aspose.PSD pro Java.  
- **Mohu přidat text do existujícího PSD?** Ano – stačí načíst soubor, přidat `TextLayer` a uložit.  
- **Potřebuji licenci pro produkci?** Komerční licence je vyžadována pro ne‑evaluační použití.  
- **Která verze Javy je podporována?** JDK 8 nebo vyšší (doporučujeme nejnovější LTS).  
- **Je to vhodné pro webové back‑endy?** Rozhodně – API funguje v jakémkoli Java‑založeném serverovém prostředí.

## Co znamená „přidat text do PSD“?
Přidání textu do PSD znamená programově vytvořit novou textovou vrstvu uvnitř dokumentu Photoshopu. Vrstva se chová jako jakákoli jiná textová vrstva ve Photoshopu: můžete ji přesouvat, upravovat její obsah a aplikovat stylování – vše bez otevření Photoshopu.

## Proč vytvořit textovou vrstvu v PSD pomocí Javy?
- **Automatizace** – Generujte marketingové materiály, vodoznaky nebo štítky produktů hromadně.  
- **Konzistence** – Zajistěte stejný font, velikost a umístění napříč tisíci soubory.  
- **Integrace** – Kombinujte s dalšími Java službami (e‑commerce, reporting, CI pipeline) a poskytujte grafiku za běhu.

## Předpoklady
Před psaním kódu se ujistěte, že máte:

1. **Java Development Kit (JDK)** – Nainstalujte JDK 8 nebo novější. Můžete si jej [stáhnout zde](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD pro Java** – Stáhněte nejnovější JAR ze [stránky vydání Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE (volitelné, ale užitečné)** – IntelliJ IDEA, Eclipse nebo jakýkoli editor dle vaší preference.  
4. **Základní znalost Javy** – Měli byste být obeznámeni s třídami, objekty a souborovým I/O.  
5. **Ukázkový PSD** – Pro tento návod použijeme `OneLayer.psd` umístěný ve složce dle vašeho výběru.

## Import balíčků
Nejprve importujte třídy, které budete potřebovat pro práci se soubory PSD a textovými vrstvami.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

Tyto importy vám poskytují přístup k základní funkčnosti Aspose.PSD.

## Postupný průvodce

### Krok 1: Nastavte adresář dokumentů
Definujte složku, která obsahuje váš zdrojový PSD a kam bude uloženo výstupní soubor.

```java
String dataDir = "Your Document Directory"; 
```

Nahraďte `"Your Document Directory"` absolutní nebo relativní cestou k vašim souborům.

### Krok 2: Načtěte zdrojový soubor PSD
Načtěte existující PSD do paměti pomocí `Image.load()`.

```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```

Pokud je cesta správná, `img` nyní představuje načtený Photoshop dokument.

### Krok 3: Přetypujte na `PsdImage`
Protože pracujeme s funkcemi specifickými pro Photoshop, přetypujte obecný `Image` na `PsdImage`.

```java
PsdImage im = (PsdImage)img;
```

Přetypování odemyká metody jako `addTextLayer()`.

### Krok 4: Definujte obdélník pro textovou vrstvu
Určete, kde se má nově vytvořený text objevit. Obdélník definuje pozici (x, y) a velikost (šířka, výška).

```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```

Neváhejte upravit výpočty podle potřeb vašeho rozvržení.

### Krok 5: Přidejte textovou vrstvu
Vytvořte skutečnou textovou vrstvu uvnitř definovaného obdélníku.

```java
TextLayer layer = im.addTextLayer("Added text", rect);
```

Nahraďte `"Added text"` libovolným řetězcem, který chcete zobrazit v PSD. Zde **programově vytváříme textovou vrstvu v PSD**.

### Krok 6: Uložte aktualizovaný soubor PSD
Zapište upravený dokument do nového souboru, abyste nepřepsali originál.

```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```

Po spuštění najdete `ImageWithTextLayer.psd` v cílové složce, nyní obsahující novou textovou vrstvu.

## Časté problémy a řešení
| Problém | Příčina | Řešení |
|---------|----------|--------|
| **`NullPointerException` on `im.addTextLayer`** | PSD nebyl načten správně (špatná cesta). | Ověřte, že `sourceFileName` ukazuje na existující PSD. |
| **Text není viditelný** | Obdélník je umístěn mimo plátno nebo je vrstva skrytá. | Upravte souřadnice obdélníku nebo zkontrolujte viditelnost vrstvy pomocí `layer.setVisible(true)`. |
| **LicenseException** | Používání knihovny bez platné licence v produkci. | Získejte komerční licenci a nastavte ji pomocí `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |

## Často kladené otázky

**Q: Mohu přidat více textových vrstev?**  
A: Ano – stačí opakovat kroky 4 a 5 pro každý text, který chcete vložit.

**Q: Jak mohu stylovat text (font, velikost, barvu)?**  
A: Třída `TextLayer` poskytuje metodu `getTextData()`, kde můžete měnit `Font`, `FontSize`, `Color` a další vlastnosti stylu. Pro podrobnosti se podívejte do dokumentace API Aspose.PSD.

**Q: Co když moje PSD už má mnoho vrstev?**  
A: Aspose.PSD pracuje s komplexními strukturami vrstev. Můžete cílit na konkrétní skupiny nebo vložit novou textovou vrstvu na požadovaný index pomocí přetížených metod `addTextLayer`.

**Q: Je tento přístup vhodný pro webové aplikace?**  
A: Rozhodně. Pokud váš server běží na Javě, můžete PSD soubory generovat nebo upravovat za běhu a poskytovat je klientům.

**Q: Kde mohu získat pomoc, pokud narazím na problémy?**  
A: Navštivte [fóra podpory Aspose](https://forum.aspose.com/c/psd/34), kde vám mohou pomoci jak komunita, tak inženýři Aspose.

## Závěr
Nyní jste viděli, jak snadné je **přidávat text do PSD** souborů za běhu pomocí Javy a Aspose.PSD. Tato technika vám umožní automatizovat tvorbu grafiky, personalizovat aktiva a integrovat úpravy na úrovni Photoshopu do jakéhokoli Java‑založeného řešení. Prozkoumejte další možnosti API Aspose.PSD, jako je přidávání tvarů, rastrových vrstev nebo aplikace filtrů pro ještě bohatší automatizaci.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-03-07  
**Testováno s:** Aspose.PSD for Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose