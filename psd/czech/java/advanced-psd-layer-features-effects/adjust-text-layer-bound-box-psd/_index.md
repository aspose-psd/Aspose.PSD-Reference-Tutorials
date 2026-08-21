---
date: 2026-06-28
description: Naučte se upravovat soubory PSD pomocí Aspose.PSD for Java – načíst a
  upravit ohraničující rámeček textu v PSD. Podrobný návod krok za krokem, jak programově
  upravit psd.
keywords:
- how to edit psd
- change photoshop text layer
- adjust text bound box
- retrieve text bound box
- update text bound box
linktitle: Upravit ohraničující rámeček textové vrstvy v PSD pomocí Java
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to edit PSD files with Aspose.PSD for Java – retrieve and
    adjust a text bound box in a PSD. Step‑by‑step guide for how to edit psd programmatically.
  headline: 'how to edit psd: Adjust Text Layer Bound Box in Java'
  type: TechArticle
- description: Learn how to edit PSD files with Aspose.PSD for Java – retrieve and
    adjust a text bound box in a PSD. Step‑by‑step guide for how to edit psd programmatically.
  name: 'how to edit psd: Adjust Text Layer Bound Box in Java'
  steps:
  - name: '**Java Development Kit (JDK)** – download from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – download from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Integrated Development Environment (IDE)** – Eclipse, IntelliJ IDEA,
      or NetBeans.'
    text: '**Integrated Development Environment (IDE)** – Eclipse, IntelliJ IDEA,
      or NetBeans.'
  - name: '**Aspose.PSD for Java Library** – obtain the latest version from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java Library** – obtain the latest version from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and arrays.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and arrays.'
  type: HowTo
- questions:
  - answer: Aspose.PSD is a robust library that lets developers create, edit, and
      convert Adobe Photoshop PSD files without needing Photoshop installed.
    question: What is Aspose.PSD?
  - answer: No, Aspose.PSD operates completely independently of Adobe Photoshop, making
      it ideal for server‑side automation.
    question: Do I need Photoshop installed to use Aspose.PSD?
  - answer: Yes, Aspose.PSD is available for .NET, Java, and Python, providing a consistent
      API across platforms.
    question: Can I use Aspose.PSD with other programming languages?
  - answer: You can get help on the official [Aspose Forum](https://forum.aspose.com/c/psd/34)
      where both staff and community members answer questions.
    question: Where can I find support for Aspose.PSD?
  - answer: Yes! Download a free trial from the [Aspose website](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 'jak upravit psd: Upravit ohraničující rámeček textové vrstvy v Java'
url: /cs/java/advanced-psd-layer-features-effects/adjust-text-layer-bound-box-psd/
weight: 25
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak upravit PSD: Nastavit ohraničující rámeček textové vrstvy v Javě

## Úvod
Pokud se zajímáte o **jak upravit PSD** soubory programově—zejména když potřebujete **upravit textovou vrstvu Photoshopu** vlastnosti—knihovna Aspose.PSD pro Java září. Tento tutoriál vás provede přesné kroky k **úpravě ohraničujícího rámečku textu** a **získání informací o ohraničujícím rámečku textu** pomocí **aspose psd java**. Ať už jste zkušený vývojář nebo teprve začínáte s Javou, najdete zde jasné, konverzační vedení, které dělá manipulaci s PSD jednoduchou a přístupnou. Pojďme na to!

## Rychlé odpovědi
- **Jaká knihovna pomáhá upravovat soubory PSD v Javě?** Aspose.PSD for Java.  
- **Mohu upravit ohraničující rámeček textové vrstvy?** Ano—použijte `getTextBoundBox()` a `setSize()` k jeho úpravě.  
- **Potřebuji mít nainstalovaný Photoshop?** Ne, Aspose.PSD funguje nezávisle na Adobe Photoshopu.  
- **Jaké jsou hlavní předpoklady?** JDK, IDE a knihovna Aspose.PSD pro Java.  
- **Jak dlouho trvá základní implementace?** Přibližně 10‑15 minut k spuštění ukázkového kódu.

## Co znamená „jak upravit PSD“ s Aspose.PSD?
Úprava PSD programově znamená otevření souboru, přístup k jeho vrstvám a modifikaci vlastností jako velikost, pozice nebo textový obsah—vše bez spuštění Photoshopu. Aspose.PSD poskytuje bohaté API, které abstrahuje složitý formát PSD, takže se můžete soustředit na logiku, kterou potřebujete.

## Proč používat Aspose.PSD pro Java?
Aspose.PSD pro Java nabízí komplexní sadu funkcí, které činí manipulaci s PSD přímočarou a efektivní. Odstraňuje potřebu Photoshopu, podporuje všechny hlavní typy vrstev, poskytuje rychlé zpracování i pro velké soubory a běží konzistentně napříč Windows, Linux a macOS prostředími.

- **Není vyžadován Photoshop** – funguje na jakémkoli serveru nebo desktopovém prostředí.  
- **Plná podpora vrstev** – rastrové, vektorové a textové vrstvy lze číst nebo upravovat.  
- **Vysoce výkonný engine** – zpracuje soubory až do 500 MB za méně než 2 sekundy a zvládne dávkové úlohy s 1 000 soubory s méně než 200 MB špičkovou pamětí.  
- **Cross‑platform** – běží na Windows, Linuxu nebo macOS se stejným kódem.

## Předpoklady
1. **Java Development Kit (JDK)** – stáhněte z [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Integrované vývojové prostředí (IDE)** – Eclipse, IntelliJ IDEA nebo NetBeans.  
3. **Knihovna Aspose.PSD pro Java** – získejte nejnovější verzi ze [Aspose releases page](https://releases.aspose.com/psd/java/).  
4. **Základní znalost Javy** – povědomí o třídách, objektech a polích.

Skvělé! S těmito předpoklady můžeme začít kódovat.

## Import balíčků
Prvním krokem je importovat třídy, které budete potřebovat. Představte si to jako shromáždění všech nástrojů před zahájením DIY projektu.

`TextLayer` je třída Aspose.PSD, která představuje textovou vrstvu uvnitř souboru PSD.  
`PsdImage` je objekt nejvyšší úrovně, který drží celý dokument v paměti.  

```java
import com.aspose.psd.Image;
import com.aspose.psd.Size;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

Tyto importy vám poskytují přístup k manipulaci s obrázky, úpravě velikosti a třídě `TextLayer`, se kterou budeme pracovat.

## Krok 1: Nastavte cesty k souborům
Určete, kde se váš PSD soubor nachází. Je to jako nastavení scény před zahájením představení.

Objekty `File` umožňují Javě najít zdroje na disku.  
Proměnné typu `String` ukládají absolutní nebo relativní cestu ke zdrojovému PSD a výstupní složce.

```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "LayerWithText.psd";
```

Nahraďte `"Your Document Directory"` skutečnou cestou ke složce na vašem počítači.

## Krok 2: Načtěte soubor PSD
Nyní otevřeme PSD, abychom mohli pracovat s jeho vrstvami.

`Image.load` načte soubor a vrátí objekt `PsdImage` připravený k manipulaci.  
`PsdImage` poskytuje metody pro výčet vrstev, přístup k metadatům a uložení změn.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Metoda `Image.load` načte soubor a vrátí objekt `PsdImage` připravený k manipulaci.

## Krok 3: Získejte textovou vrstvu
Identifikujte konkrétní textovou vrstvu, kterou chcete upravit. Vrstvy jsou indexovány od nuly, takže `[1]` odkazuje na druhou vrstvu.

`TextLayer` je konkrétní třída pro vrstvy typu text; expose text‑specific properties such as font, color, and bounding box.  

```java
TextLayer textLayer = (TextLayer) im.getLayers()[1];
```

Ujistěte se, že cílíte na správnou vrstvu; jinak můžete upravit nesprávný obsah.

## Krok 4: Zkontrolujte velikost vrstvy
Před jakoukoliv změnou je dobré ověřit aktuální velikost. Slouží to jako sanity check.

Objekty `Size` obsahují šířku a výšku v pixelech.  
`Assert` (nebo jednoduchý `if`) vám umožní validovat očekávání během vývoje.

```java
Size correctOpticalSize = new Size(127, 45);
Size opticalSize = textLayer.getSize();
Assert.areEqual(correctOpticalSize, opticalSize);
```

Pokud se velikosti neshodují, `Assert` vyvolá upozornění, že něco není v pořádku.

## Krok 5: Získejte velikost ohraničujícího rámečku
Nyní získáme **textový ohraničující rámeček**—obdélník, který obklopuje vykreslený text.

`getTextBoundBox()` vrací instanci `Size`, která popisuje přesný obdélník, který text zabírá po vykreslení, s ohledem na metriky fontu a řádkování.

```java
Size correctBoundBox = new Size(172, 62);
Size boundBox = textLayer.getTextBoundBox();
Assert.areEqual(correctBoundBox, boundBox);
```

Můžete tuto velikost porovnat s očekávanými rozměry nebo ji použít k dalším úpravám.

## Jak získat ohraničující rámeček textu pomocí Aspose.PSD Java?
Pro získání ohraničujícího rámečku nejprve načtěte PSD soubor pomocí `Image.load` a získejte instanci `PsdImage`. Pak najděte cílový `TextLayer` iterací přes `psdImage.getLayers()` nebo podle indexu. Zavolejte metodu `getTextBoundBox()` na této vrstvě; vrátí objekt `Size` s přesnou šířkou a výškou v pixelech, který můžete zaznamenat nebo použít pro další výpočty.

## Jak mohu upravit ohraničující rámeček textu pomocí Aspose.PSD Java?
Po získání aktuálního ohraničujícího rámečku jej můžete upravit voláním `setSize(new Size(width, height))` přímo na `TextLayer`, přičemž zadáte požadované hodnoty šířky a výšky. Alternativně můžete použít transformační matici pomocí metody `transform()` k měřítku nebo repositionování textu před rasterizací vrstvy. Oba přístupy aktualizují vizuální rozložení tak, aby splňovalo vaše designové požadavky.

## Běžné případy použití
- **Dynamické generování miniatur** – upravit ohraničení textu před rasterizací náhledu.  
- **Automatizované brandování** – programově nahradit text loga a zajistit, že se vejde do designových omezení.  
- **Dávkové zpracování** – iterovat přes mnoho souborů PSD a standardizovat velikosti textových vrstev napříč produktovou řadou.

## Řešení problémů a tipy
- **Nesprávný index vrstvy** – zkontrolujte pořadí vrstev ve Photoshopu; index se může lišit od očekávaného.  
- **Problémy s licencí** – trial verze může omezovat některé operace; ujistěte se, že máte platnou licenci pro produkci.  
- **Neočekávané velikosti** – nastavení DPI může ovlivnit výpočty velikosti; ověřte rozlišení PSD, pokud se čísla zdají nesprávná.  
- **Tip pro výkon** – znovu použijte stejnou instanci `PsdImage` při zpracování více vrstev, abyste minimalizovali alokace paměti.

## Závěr
Nyní jste se naučili **jak upravit PSD** soubory získáním a úpravou ohraničujícího rámečku textové vrstvy pomocí **aspose psd java**. Pouze několika řádky kódu můžete načíst PSD, zaměřit se na konkrétní vrstvu, ověřit její rozměry a zajistit, že text bude perfektně zapadat. Pro hlubší průzkum—například úpravu textového obsahu, aplikaci efektů nebo export do jiných formátů—si prohlédněte kompletní dokumentaci Aspose.PSD [zde](https://reference.aspose.com/psd/java/).

## Často kladené otázky
**Q: Co je Aspose.PSD?**  
A: Aspose.PSD je robustní knihovna, která umožňuje vývojářům vytvářet, upravovat a konvertovat soubory Adobe Photoshop PSD bez potřeby instalovaného Photoshopu.

**Q: Potřebuji mít nainstalovaný Photoshop pro použití Aspose.PSD?**  
A: Ne, Aspose.PSD funguje zcela nezávisle na Adobe Photoshopu, což jej činí ideálním pro automatizaci na straně serveru.

**Q: Mohu použít Aspose.PSD s jinými programovacími jazyky?**  
A: Ano, Aspose.PSD je dostupný pro .NET, Java a Python, poskytující konzistentní API napříč platformami.

**Q: Kde mohu najít podporu pro Aspose.PSD?**  
A: Pomoc získáte na oficiálním [Aspose Forum](https://forum.aspose.com/c/psd/34), kde odpovídají jak zaměstnanci, tak i členové komunity.

**Q: Je k dispozici zkušební verze pro Aspose.PSD?**  
A: Ano! Stáhněte si bezplatnou zkušební verzi z [Aspose website](https://releases.aspose.com/).

**Poslední aktualizace:** 2026-06-28  
**Testováno s:** Aspose.PSD for Java (latest)  
**Autor:** Aspose

## Související tutoriály

- [Jak upravit textové vrstvy PSD pomocí Aspose.PSD pro Java](/psd/java/advanced-psd-layer-features-effects/update-text-layer-psd-files/)
- [Přidat textovou vrstvu za běhu v PSD souborech pomocí Javy](/psd/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/)
- [Vykreslit otočenou textovou vrstvu v PSD souborech pomocí Javy](/psd/java/psd-layer-management-effects/render-rotated-text-layer-psd/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}