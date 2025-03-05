---
title: Vytvářejte miniatury ze souborů PSD pomocí Java
linktitle: Vytvářejte miniatury ze souborů PSD pomocí Java
second_title: Aspose.PSD Java API
description: Naučte se, jak snadno vytvářet miniatury ze souborů PSD pomocí Java a Aspose.PSD. Postupujte podle našeho podrobného průvodce pro bezproblémové zpracování obrazu.
type: docs
weight: 24
url: /cs/java/modifying-converting-psd-images/create-thumbnails-psd-files/
---
## Zavedení
Ve světě grafického designu je práce se soubory PSD (Photoshop Document) samozřejmostí. Ať už jste zkušený vývojář, grafik nebo jen někdo, kdo se chce ponořit do zpracování obrázků, vytváření miniatur ze souborů PSD vám může ušetřit čas a zefektivnit váš pracovní postup. Tento tutoriál vás provede celým procesem pomocí Aspose.PSD pro Javu. Aspose.PSD je nejen robustní knihovna pro správu souborů Photoshopu, ale také umožňuje intuitivní a zvládnutelný úkol. Jste připraveni naučit se efektivně vytvářet miniatury ze souborů PSD?
## Předpoklady
Než se ponoříme do toho nejhrubšího z tvorby náhledů, pojďme si probrat, co budete potřebovat, abyste mohli začít.
### Vývojové prostředí Java
-  Java JDK: Ujistěte se, že máte v počítači nainstalovanou sadu Java Development Kit (JDK). Můžete si jej stáhnout[zde](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- IDE: Integrované vývojové prostředí (IDE) jako IntelliJ IDEA, Eclipse nebo NetBeans usnadní kódování.
### Knihovna Aspose.PSD
- Do projektu musíte zahrnout knihovnu Aspose.PSD. Můžete[stáhněte si nejnovější verzi zde](https://releases.aspose.com/psd/java/).
### Základní znalost Javy
- Znalost základů jazyka Java vám pomůže efektivněji procházet ukázkovým kódem. Koncepty jako třídy, objekty a smyčky budou často používány.
## Importujte balíčky
Začněte importem potřebných tříd z knihovny Aspose.PSD. Tento krok je zásadní, protože vám umožňuje využít funkce knihovny ve vašem kódu.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
S předpoklady mimo cestu, pojďme skočit do hlavní události! Vytváření miniatur ze souborů PSD zahrnuje několik jednoduchých kroků a já to pro vás rozeberu.
## Krok 1: Nastavte své prostředí
Zde je návod, jak zahájit svůj projekt a připravit se na generování miniatur.
1. Vytvořte projekt Java:
   - Otevřete své IDE a vytvořte nový Java projekt.
   - Pojmenujte to něco jako "PsdThumbnailGenerator".
2. Zahrnout knihovnu Aspose.PSD:
   -  Přidejte soubor Aspose.PSD JAR do cesty sestavení vašeho projektu. Pokud používáte Maven, zahrňte jej do svého`pom.xml`:
     ```xml
     <dependency>
         <groupId>com.aspose</groupId>
         <artifactId>aspose-psd</artifactId>
         <version>your_version_here</version>
     </dependency>
     ```
## Krok 2: Načtěte soubor PSD
Dále musíme načíst PSD soubor, ze kterého chceme vytvořit náhledy. 
1. Zadejte svůj adresář dokumentů:
   Definujte adresář, kde se nachází váš soubor PSD.
   ```java
   String dataDir = "Your Document Directory"; // Nahraďte svou cestou
   ```
2. Načtěte soubor PSD:
    Použijte`PsdImage` třídy k načtení souboru PSD.
   ```java
   PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
   ```
 Zde,`sample.psd` je název vašeho PSD souboru. Upravte to podle názvu vašeho souboru.
## Krok 3: Opakujte zdroje PSD
Nyní, když máme načtený obrázek PSD, dalším krokem je prozkoumat jeho zdroje.
1. Získejte počet zdrojů:
   Projdeme všechny zdroje v souboru PSD.
   ```java
   for (int i = 0; i < image.getImageResources().length; i++) {
       // Zpracování zdrojů
   }
   ```
   
2. Identifikujte zdroje miniatur:
   Uvnitř smyčky zkontrolujte, zda je zdrojem miniatura.
   ```java
   if (image.getImageResources()[i] instanceof ThumbnailResource) {
       // Zpracujte miniaturu
   }
   ```
## Krok 4: Zpracujte miniaturu
Jakmile identifikujeme zdroj miniatur, budeme s ním muset náležitě zacházet.
1. Načíst a zkontrolovat formát miniatur:
   Pokud je zdrojem skutečně miniatura, načtěte ji a zkontrolujte její formát.
   ```java
   ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
   if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
       // Vytvořte a uložte miniaturu
   }
   ```
## Krok 5: Vytvořte a uložte miniaturu
Tady se děje kouzlo! Z dat náhledu vytvoříme nový obrázek a uložíme jej.
1. Vytvořit nový obrázek:
   K vytvoření nového bitmapového obrázku použijeme šířku a výšku zdroje miniatur.
   ```java
   PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
   ```
2. Uložit pixely do nového obrázku:
   Přeneste data miniatur do nově vytvořeného obrázku.
   ```java
   thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
   ```
3. Uložit obrázek miniatury:
   Nakonec uložte obrázek miniatury do adresáře dokumentů s jedinečným názvem.
   ```java
   thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
   ```

## Závěr
Vytváření náhledů ze souborů PSD pomocí Java a Aspose.PSD může být přímočarým úkolem, jakmile jej rozdělíte do zvládnutelných kroků. S tímto tutoriálem nyní můžete snadno extrahovat miniatury ze souborů PSD, což vám poskytne šikovný nástroj pro vylepšení vašeho pracovního postupu. Tak co ti v tom brání? Získejte nějaké soubory PSD a vyzkoušejte to!
## FAQ
### Co je Aspose.PSD?
Aspose.PSD je knihovna Java, která umožňuje vývojářům pracovat se soubory Photoshopu, což usnadňuje manipulaci a programovou správu souborů PSD.
### Mohu používat Aspose.PSD zdarma?
Ano, Aspose nabízí bezplatnou zkušební verzi, kterou můžete použít k otestování knihovny před zakoupením licence.
### V jakých formátech mohu uložit náhledy?
V tomto příkladu jsme uložili náhledy ve formátu BMP, ale Aspose.PSD podporuje také různé další formáty.
### Potřebuji nainstalovaný Photoshop, abych mohl používat Aspose.PSD?
Ne, Aspose.PSD funguje nezávisle na Photoshopu.
### Kde najdu více informací o Aspose.PSD?
 Můžete se podívat na[Dokumentace Aspose.PSD](https://reference.aspose.com/psd/java/) pro více podrobností, výukových programů a zdrojů.