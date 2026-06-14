---
date: 2026-03-15
description: Naučte se, jak vytvářet soubory PSD, generovat barevnou paletu PSD a
  nastavit barevný režim PSD pomocí Aspose.PSD pro Javu v tomto průvodci krok za krokem.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Jak vytvořit soubory PSD pomocí Aspose.PSD pro Java
url: /cs/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

Let's produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak vytvořit soubory PSD pomocí Aspose.PSD pro Java

## Úvod
Pokud jste se někdy zamýšleli **jak vytvořit PSD** soubory programově, jste na správném místě. Aspose.PSD pro Java vám dává plnou kontrolu nad dokumenty Photoshopu, umožňuje generovat, upravovat a ukládat PSD soubory, aniž byste kdy otevřeli Photoshop. V tomto tutoriálu projdeme vytvořením **indexovaného PSD** souboru, nastavením barevného režimu PSD a generováním vlastní palety barev — vše s jasným, krok‑za‑krokem Java kódem. Ať už budujete grafický pipeline, automatizujete tvorbu assetů, nebo jen experimentujete, koncepty zde vám pomohou přenést vaše vizuální nápady do reality.

## Rychlé odpovědi
- **Jaká knihovna je potřeba?** Aspose.PSD pro Java
- **Mohu vytvořit indexovaný PSD?** Ano, nastavením barevného režimu na `Indexed`
- **Potřebuji mít nainstalovaný Photoshop?** Ne, Aspose.PSD funguje nezávisle
- **Která verze Javy je vyžadována?** JDK 8 nebo novější
- **Jak velké může být plátno?** Jakékoliv; tento příklad používá 500 × 500 px

## Co je indexovaný soubor PSD?
Indexovaný PSD ukládá barvy v paletě místo plnohodnotných barevných hodnot pro každý pixel. To snižuje velikost souboru a je ideální pro grafiku s omezeným počtem barev, jako jsou ikony nebo UI assety. Vytvořením vlastní palety máte přesnou kontrolu nad tím, které barvy se objeví ve finálním obrázku.

## Proč generovat paletu barev PSD?
Vytvoření **palety barev PSD** vám umožní:
- Udržet velikost souboru malou pro web nebo mobilní použití  
- Zajistit konzistentní branding omezením barev na vaši firemní paletu  
- Zrychlit vykreslování v aplikacích, které podporují indexované obrázky  

## Předpoklady
Předtím, než se ponoříme do kódu, ujistěte se, že máte následující:

1. **Základní znalost Javy** – měli byste být pohodlní s třídami, metodami a vytvářením objektů.  
2. **Java Development Kit (JDK) 8+** – nainstalovaný a nastavený ve vašem IDE.  
3. **IDE (IntelliJ IDEA, Eclipse, atd.)** – volitelné, ale vysoce doporučené pro snadnější ladění.  
4. **Aspose.PSD pro Java knihovna** – stáhněte ji **[zde](https://releases.aspose.com/psd/java/)** a přidejte JAR do classpath projektu.  
5. **Základní koncepty grafického designu** – pochopení barevných režimů, palet a základních tvarů vám pomůže sledovat postup.

## Import balíčků
Než budeme pokračovat s kódem, ujistěme se, že máme do vaší Java aplikace importovány všechny potřebné balíčky. Zde je, co budete potřebovat:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

Tyto importy vám umožní pracovat s PSD možnostmi, barvami a grafickou manipulací prostřednictvím Aspose.PSD.

Nyní rozdělíme kód krok‑za‑krokem, abychom vám ukázali **jak vytvořit PSD** soubory s indexovaným barevným režimem.

## Krok 1: Nastavte adresář dokumentu
Nejprve definujte, kam bude vygenerovaný PSD uložen.

```java
String dataDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` absolutní nebo relativní cestou, např. `"/Users/YourName/Documents/"`.

## Krok 2: Vytvořte instanci PsdOptions
`PsdOptions` obsahuje všechna nastavení pro soubor, který se chystáte vygenerovat.

```java
PsdOptions createOptions = new PsdOptions();
```

## Krok 3: Nastavte základní vlastnosti PsdOptions
Zde specifikujeme výstupní umístění, **nastavíme PSD barevný režim** na `Indexed` a verzi PSD.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – úplná cesta nového souboru.  
- **Color Mode** – `Indexed` říká Aspose.PSD, aby použil obrázek založený na paletě.  
- **Version** – verze formátu PSD (5 funguje pro většinu moderních verzí Photoshopu).

## Krok 4: Vytvořte paletu barev (Generování palety barev PSD)
Definujte barvy, které budou k dispozici v indexovaném obrázku.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- `palette` pole obsahuje až 256 objektů `Color`.  
- `CompressionMethod.RLE` poskytuje efektivní bezztrátovou kompresi pro indexované obrázky.

## Krok 5: Vytvořte plátno PSD obrázku
Nyní vytvoříme prázdný PSD s požadovanými rozměry.

```java
Image psd = Image.create(createOptions, 500, 500);
```

Tím vytvoříte plátno o rozměrech 500 × 500 pixelů, které používá dříve definovanou paletu.

## Krok 6: Nakreslete grafiku na PSD
Přidejte vizuální obsah — zde nakreslíme jednoduchou červenou elipsu na bílém pozadí.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` vyplní pozadí bílou.  
- `drawEllipse` vykreslí červenou elipsu s 6‑pixelovým tahy.

## Krok 7: Uložte soubor PSD
Nakonec uložte obrázek na disk.

```java
psd.save();
```

Soubor `Newsample_out.psd` se objeví v adresáři, který jste uvedli dříve.

## Časté problémy a tipy
- **Palette Size** – Pokud potřebujete více než 4 barvy, jednoduše je přidejte do pole `palette` (až 256).  
- **File Permissions** – Ujistěte se, že Java proces má právo zápisu do `dataDir`.  
- **Incorrect Color Mode** – Zapomenutí `createOptions.setColorMode(ColorModes.Indexed)` vytvoří RGB PSD místo indexovaného.

## Často kladené otázky

**Q: Co je Aspose.PSD pro Java?**  
A: Aspose.PSD pro Java je knihovna, která umožňuje programově manipulovat se soubory PSD (Photoshop) pomocí Javy.

**Q: Mohu používat Aspose.PSD zdarma?**  
A: Ano, můžete získat bezplatnou zkušební verzi Aspose.PSD **[zde](https://releases.aspose.com/)**.

**Q: Potřebuji mít nainstalovaný Photoshop, abych mohl pracovat s Aspose.PSD?**  
A: Ne, můžete vytvářet a manipulovat se soubory PSD bez Photoshopu, protože Aspose.PSD provádí všechny operace nezávisle.

**Q: Jak získám dočasnou licenci pro Aspose.PSD?**  
A: Dočasnou licenci můžete požádat **[zde](https://purchase.aspose.com/temporary-license/)**.

**Q: Kde mohu získat podporu pro Aspose.PSD?**  
A: Podporu můžete získat na fóru Aspose **[zde](https://forum.aspose.com/c/psd/34)**.

## Závěr
Právě jste se naučili **jak vytvořit PSD** soubory s indexovaným barevným režimem, vygenerovali vlastní paletu a přidali jednoduchou grafiku — vše pomocí Aspose.PSD pro Java. S těmito stavebními kameny můžete rozšířit své projekty o složitější kresby, správu vrstev a hromadné zpracování. Pro hlubší průzkum se podívejte na oficiální API referenci **[zde](https://reference.aspose.com/psd/java/)** a nadále experimentujte s různými paletami a kreslícími primitivy.

---

**Last Updated:** 2026-03-15  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}