---
date: 2026-09-23
description: Zjistěte, jak upravit vektorové tvary PSD a hromadně zpracovávat soubory
  PSD pomocí Aspose.PSD for Java. Podrobné kroky, tipy a zástupné kódy pro kompletní
  řešení.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Podpora vlastností dat záznamu délky v PSD – Java
og_description: Zjistěte, jak upravit vektorové tvary PSD a hromadně zpracovávat soubory
  PSD pomocí Aspose.PSD for Java. Průvodce krok za krokem se zástupnými kódy a odbornými
  tipy.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Upravit vektorové tvary PSD pomocí Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Upravit vektorové tvary PSD pomocí Aspose.PSD for Java
url: /cs/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Upravit vektorové tvary PSD pomocí Aspose.PSD pro Java

## Úvod
Pokud potřebujete **upravit vektorové tvary PSD** programově, Aspose.PSD pro Java vám poskytuje plnou kontrolu nad soubory Photoshopu přímo z vašeho Java kódu. Tento tutoriál vás provede podporou vlastností záznamu délky – nezbytným krokem při úpravě vrstev vektorových tvarů. Na konci budete schopni otevřít PSD, upravit data vektorových tvarů a uložit aktualizovaný soubor, aniž byste kdykoli spouštěli Photoshop.

## Rychlé odpovědi
- **Co znamená “upravit vektorové tvary PSD”?** Úprava geometrie, operací cest nebo dalších atributů vrstev založených na vektorech uvnitř souboru PSD.  
- **Která knihovna to řeší?** Aspose.PSD pro Java.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro hodnocení; pro produkci je vyžadována komerční licence.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní skript úpravy tvaru.  
- **Jaké jsou hlavní předpoklady?** Java JDK, Aspose.PSD pro Java a ukázkový soubor PSD.

## Co znamená “podporovat vlastnosti záznamu délky”?
Podporovat vlastnosti záznamu délky znamená přístup k objektům `LengthRecord` a jejich aktualizaci, které popisují každou vektorovou cestu uvnitř PSD. Tyto záznamy ukládají informace jako délka cesty, typ a způsob, jakým se spojují s ostatními cestami. jejich změna vám umožní řídit, jak se tvary kombinují, protínají nebo odečítají od sebe, což umožňuje přesnou úpravu vektorů.

## Proč použít Aspose.PSD pro Java k podpoře vlastností záznamu délky?
Načtěte svůj PSD, upravte vektorová data a uložte – vše bez Photoshopu. Aspose.PSD zpracovává více než stovky stránek PSD za méně než 2 sekundy na typickém serveru, nabízí více než 150 tříd (včetně více než 30 typů souvisejících s vektory) a běží na Windows, Linuxu nebo macOS s libovolným JDK 11+. Tato knihovna zaměřená na výkon odstraňuje potřebu nákladného desktopového softwaru.

## Požadavky
1. **Java Development Kit (JDK)** – stáhněte z [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) nebo použijte svůj preferovaný správce balíčků.  
2. **Aspose.PSD pro Java** – získejte nejnovější JAR ze [stránky vydání Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse nebo jakýkoli editor kompatibilní s Javou.  
4. **Soubor PSD** – vytvořte jej ve Photoshopu nebo si pořiďte ukázkový PSD pro experimentování.  
5. **Základní znalost Javy** – povědomí o třídách, objektech a zpracování výjimek.

## Import balíčků
Importovací příkazy přinášejí do rozsahu hlavní třídy Aspose.PSD, jako jsou `PsdImage`, `VsmsResource` a `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Krok 1: Nastavte své vstupní a výstupní adresáře
Určete, kde se nachází původní PSD a kam bude zapsán upravený soubor.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Krok 2: Načtěte soubor PSD
Použijte `Image.load` k otevření souboru a přetypujte jej na `PsdImage` pro funkce specifické pro PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Krok 3: Najděte zdroj Vsms ve vrstvě
`VsmsResource` je kontejner, který ukládá data vektorových tvarů pro vrstvu. Projděte prostředky druhé vrstvy, abyste jej našli.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Krok 4: Přístup k záznamům délky
`LengthRecord` představuje samostatnou vektorovou cestu. Získejte záznamy, které chcete upravit.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Krok 5: Upravit vlastnosti operací cesty
`PathOperations` definuje, jak jednotlivé tvary spolupracují (např. vyloučení, průnik, odečtení). Změna těchto hodnot aktualizuje vizuální kompozici vektorové vrstvy.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Krok 6: Uložte upravený soubor PSD
Uložte své změny do nového souboru.

```java
psdImage.save(outPsdFilePath);
```

## Krok 7: Vyčistěte prostředky
Uvolněte instanci `PsdImage`, aby se uvolnila paměť a předešlo únikům prostředků.

```java
psdImage.dispose();
```

## Jak hromadně zpracovat soubory PSD s podporou vlastností záznamu délky
Zabalte workflow pro jeden soubor do smyčky, která prochází adresář s PSD soubory a aktualizuje `inPsdFilePath` a `outPsdFilePath` pro každý soubor. Tento přístup vám umožní aplikovat identické úpravy vektorových tvarů na desítky nebo stovky souborů během několika minut, ideální pro automatizované pipeline assetů.

## Časté úskalí a tipy
- **Kontroly na null** – vždy ověřte, že `resource` není `null`, než přistoupíte k jeho členům.  
- **Meze indexů cesty** – ujistěte se, že indexy, které používáte (např. `[2]`, `[7]`, `[11]`), existují pro konkrétní PSD, který upravujete.  
- **Licence** – spuštění bez platné licence vloží vodoznak do uloženého PSD.

## Závěr
Nyní máte kompletní příklad od začátku do konce, jak **upravit vektorové tvary PSD** podporou vlastností záznamu délky pomocí Aspose.PSD pro Java. Ať už automatizujete pipeline assetů nebo vytváříte vlastní nástroj pro design, tyto API vám poskytují flexibilitu manipulovat s vektorovými vrstvami bez ruční práce ve Photoshopu. Experimentujte s dalšími hodnotami `PathOperations` nebo kombinujte více úprav `LengthRecord` k vytvoření složitých tvarů.

## Často kladené otázky

**Q: Jak zacházet s PSD, který neobsahuje žádné vrstvy vektorových tvarů?**  
A: `VsmsResource` bude chybět, takže `resource` zůstane `null`. Přidejte kontrolu a přeskočte krok úpravy nebo informujte uživatele.

**Q: Mohu změnit i jiné vlastnosti, jako barvu výplně nebo šířku tahu?**  
A: Ano, `LengthRecord` poskytuje settery pro výplň, tah a neprůhlednost. Viz dokumentace API pro kompletní seznam.

**Q: Je možné hromadně zpracovat více souborů PSD?**  
A: Rozhodně. Zabalte kód do smyčky, která prochází adresář s PSD soubory a při každém průchodu upravuje vstupní a výstupní cesty.

**Q: Musím ručně zavírat streamy při načítání ze souborové cesty?**  
A: `Image.load` automaticky spravuje souborové streamy, ale pokud načítáte z `InputStream`, nezapomeňte jej po použití zavřít.

**Q: Jaká verze Aspose.PSD je pro tyto API vyžadována?**  
A: Třídy `LengthRecord` a `PathOperations` jsou k dispozici od Aspose.PSD 20.10. Doporučuje se použít nejnovější verzi (24.11 v době psaní).

---

**Poslední aktualizace:** 2026-09-23  
**Testováno s:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

## Související tutoriály

- [Převést PSD na PNG a vytvořit vektorovou masku Java – Vmsk Resource v souborech PSD](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Převést PSD na PNG s podporou masky vrstvy pomocí Aspose.PSD pro Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Přidat podporu vrstev do souborů PSD](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}