---
date: 2026-07-22
description: Naučte se, jak extrahovat vrstvy PSD a převést vrstvy PSD do PNG pomocí
  Aspose.PSD pro Java. Ideální pro vývojáře, kteří potřebují robustní manipulaci s
  grafikou.
keywords:
- extract psd layers
- how to extract psd
- convert psd to png
lastmod: 2026-07-22
linktitle: Extrahujte vrstvy PSD a přidejte podporu vrstev pro soubory PSD pomocí
  Aspose.PSD Java
og_description: Extrahujte vrstvy PSD a převádějte je do PNG pomocí Aspose.PSD pro
  Java. Postupujte podle tohoto krok‑za‑krokem průvodce a automatizujte extrakci vrstev
  a konverzi obrázků.
og_image_alt: Developer guide showing Java code to extract PSD layers and save as
  PNG using Aspose.PSD
og_title: Extrahujte vrstvy PSD – Přidejte podporu vrstev pro soubory PSD pomocí Aspose.PSD
  Java
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  headline: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
    Java
  type: TechArticle
- description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  name: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD Java
  steps:
  - name: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
  - name: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
    text: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
    text: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that allows you to manipulate PSD files
      without having Photoshop installed.
    question: What is Aspose.PSD for Java?
  - answer: Yes! While primarily for PSD files, Aspose offers libraries for a wide
      range of formats, including AI, PDF, and SVG.
    question: Can I use Aspose.PSD for other file formats?
  - answer: Absolutely! You can download a free trial version [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: Access the Aspose forum for PSD‑related questions [here](https://forum.aspose.com/c/psd/34).
    question: Where can I get support if I run into problems?
  - answer: Iterate over `image.getLayers()`, create a new `Bitmap` for each layer,
      and save it with its own `PngOptions`. This yields individual PNG files per
      layer.
    question: Can I convert each layer to a separate PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- extract psd
- Aspose.PSD
- Java image processing
title: Extrahujte vrstvy PSD a přidejte podporu vrstev pro soubory PSD pomocí Aspose.PSD
  Java
url: /cs/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extrahujte vrstvy PSD a přidejte podporu vrstev pro soubory PSD pomocí Aspose.PSD Java

## Úvod
Práce se soubory Photoshop Document (PSD) je každodenní realitou pro grafické designéry i vývojáře a **extract psd layers** je často prvním krokem k opětovnému využití aktiv nebo automatizaci obrazových pipeline. V tomto tutoriálu se naučíte, jak získat jednotlivé vrstvy z PSD, povolit plnou podporu vrstev a **convert PSD layers to PNG** pomocí Aspose.PSD pro Java. Pokryjeme vše od nastavení prostředí po tipy na osvědčené postupy, abyste mohli tento workflow integrovat do jakékoli Java aplikace během několika minut.

## Rychlé odpovědi
- **Co znamená “extract PSD layers”?** Znamená to načtení souboru PSD a přístup k jednotlivým vrstvám pro manipulaci nebo export.  
- **Která knihovna to v Javě zpracovává?** Aspose.PSD for Java poskytuje plnohodnotné zpracování PSD bez potřeby Photoshopu.  
- **Mohu převést vrstvy PSD do PNG najednou?** Ano – načtením souboru s odpovídajícími možnostmi a uložením s PNG možnostmi, které zachovávají průhlednost.  
- **Potřebuji licenci pro produkční použití?** Pro produkci je vyžadována komerční licence; pro vyhodnocení je k dispozici bezplatná zkušební verze.  
- **Jaká verze Javy je požadována?** JDK 8 nebo vyšší (v tutoriálu je použito JDK 11 jako příklad).

## Jak extrahovat vrstvy PSD pomocí Aspose.PSD pro Java?
Načtěte PSD, povolte efekty vrstev a výsledek uložte jako PNG během několika řádků Java kódu. Tento přímý přístup eliminuje potřebu Photoshopu na serveru a funguje na jakékoli platformě, která podporuje Java 8+.  
Začnete vytvořením objektu `PsdLoadOptions` s `setLoadEffectsResource(true)` a `setUseDiskForLoadEffectsResource(true)`, poté načtěte soubor pomocí `PsdImage.load(path, options)`. Po načtení můžete buď sloučit vrstvy pomocí `image.save(outputPath, new PngOptions())`, nebo iterovat přes `image.getLayers()` a exportovat každou vrstvu samostatně, čímž zajistíte zachování všech efektů při nízké spotřebě paměti.

## Proč extrahovat vrstvy PSD a převést je do PNG?
Extrahování vrstev vám umožní **reuse assets**, **automate thumbnail generation**, a **preserve transparency** pro web‑připravenou grafiku. Aspose.PSD podporuje **50+ vstupních a výstupních formátů** a může zpracovávat více‑stovkové PSD soubory, aniž by načítal celý soubor do paměti, díky disk‑založenému zpracování zdrojů.

## Požadavky
Předtím, než se pustíme dál, ujistěte se, že máte následující:

1. **Java Development Environment** – Nainstalovaný JDK. Můžete jej stáhnout z [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – Stáhněte si nejnovější knihovnu z oficiální stránky ke stažení [zde](https://releases.aspose.com/psd/java/).  
3. **Basic Java knowledge** – Znalost kompilace a spouštění Java programů.  
4. **IDE** – IntelliJ IDEA, Eclipse nebo jakýkoli editor, který preferujete.  
5. **A PSD file** – Použijte libovolný PSD, který máte, nebo si stáhněte ukázkový PSD pro testování.

Jakmile máte vše připravené, můžete začít extrahovat vrstvy PSD.

## Import balíčků
Třídy `PsdImage`, `PsdLoadOptions` a `PngOptions` jsou jádrem workflow.  

`PsdImage` je objekt nejvyšší úrovně Aspose.PSD, který představuje jeden PSD soubor v paměti.  

`PsdLoadOptions` vám umožňuje řídit, jak jsou načítány zdroje, jako jsou efekty vrstev.  

`PngOptions` definuje výstupní formát a zacházení s průhledností pro PNG soubor.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Definujte své adresáře
Nastavte cesty pro zdrojový PSD a výstupní PNG. Upravit `dataDir`, aby ukazoval na složku, kde se vaše soubory nacházejí.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – Nahraďte `"Your Document Directory"` skutečnou cestou ke složce.  
- `sourceFileName` – Úplná cesta k PSD, který chcete zpracovat.  
- `output` – Cílová cesta pro PNG, který bude obsahovat extrahované vrstvy.

## Krok 2: Nastavte možnosti načítání
Nastavení `PsdLoadOptions` zajišťuje, že všechny efekty vrstev a zdroje jsou načteny správně, což je nezbytné při **extract PSD layers**.

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – Načte další efekty (např. stíny), které jsou připojeny k vrstvám.  
- `setUseDiskForLoadEffectsResource(true)` – Přesune těžké zdroje na disk, čímž snižuje zatížení paměti.

## Krok 3: Načtěte soubor PSD
Nyní načteme PSD do objektu `PsdImage` pomocí výše definovaných možností.

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

V tomto okamžiku `image` obsahuje všechny vrstvy, masky a efekty, připravené k extrahování.

## Krok 4: Nastavte možnosti uložení
Nastavte, jak bude PNG uloženo. Použití `TruecolorWithAlpha` zachovává průhlednost z původních vrstev.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Krok 5: Uložte obrázek (převod vrstev PSD do PNG)
Exportujte načtený PSD (se všemi jeho vrstvami) do jediného PNG souboru. Tento krok efektivně **convert psd layers png** v jedné operaci.

```java
image.save(output, saveOptions);
```

Pokud potřebujete každou vrstvu jako samostatný PNG, můžete iterovat přes `image.getLayers()` – ale pro mnoho případů je sloučený PNG dostačující.

## Krok 6: Dokončete
Přidejte přátelskou zprávu do konzole, abyste věděli, že proces byl úspěšný.

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## Časté problémy a tipy
- **Out‑of‑Memory Errors:** Pokud zpracováváte velmi velké PSD, nechte `setUseDiskForLoadEffectsResource(true)` povoleno, aby se dočasná data přesunula na disk.  
- **Missing Effects:** Ujistěte se, že je nastaveno `setLoadEffectsResource(true)`; jinak mohou být některé efekty vrstev ignorovány.  
- **Path Problems:** Použijte `Paths.get(...)` z `java.nio.file` pro platformově nezávislé zpracování cest.

## Často kladené otázky

**Q: Co je Aspose.PSD for Java?**  
A: Aspose.PSD for Java je knihovna, která vám umožňuje manipulovat se soubory PSD bez nutnosti mít nainstalovaný Photoshop.

**Q: Mohu použít Aspose.PSD i pro jiné formáty souborů?**  
A: Ano! Přestože je primárně určen pro PSD soubory, Aspose nabízí knihovny pro širokou škálu formátů, včetně AI, PDF a SVG.

**Q: Je k dispozici zkušební verze?**  
A: Rozhodně! Bezplatnou zkušební verzi si můžete stáhnout [zde](https://releases.aspose.com/).

**Q: Kde mohu získat podporu, pokud narazím na problémy?**  
A: Přístup k fóru Aspose pro otázky týkající se PSD [zde](https://forum.aspose.com/c/psd/34).

**Q: Mohu převést každou vrstvu na samostatný PNG?**  
A: Iterujte přes `image.getLayers()`, vytvořte nový `Bitmap` pro každou vrstvu a uložte jej s vlastním `PngOptions`. To vytvoří samostatné PNG soubory pro každou vrstvu.

## Závěr
Nyní jste se naučili, jak **extract PSD layers**, povolit plnou podporu vrstev a **convert PSD layers to PNG** pomocí Aspose.PSD pro Java. Ať už budujete automatizovanou pipeline aktiv nebo přidáváte grafické možnosti do desktopové aplikace, tento přístup vám poskytuje detailní kontrolu nad soubory Photoshopu bez nutnosti samotného Photoshopu. Dále můžete zkoumat aplikaci filtrů, programové slučování vrstev nebo export každé vrstvy samostatně podle vašich potřeb.

---

**Last Updated:** 2026-07-22  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose

## Související tutoriály

- [Export PSD do PNG a přidat novou běžnou vrstvu pomocí Aspose.PSD pro Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Export PSD do PNG s podporou masky vrstvy v Javě](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Převod PSD na obrázek v Javě – aplikovat vrstvy úprav s Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}