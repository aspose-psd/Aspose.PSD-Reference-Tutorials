---
date: 2026-03-28
description: Naučte se, jak vytvořit vrstvu foto filtru a přidat vrstvu úpravy do
  souborů PSD pomocí Aspose.PSD pro Javu. Postupujte podle tohoto návodu pro snadné
  úpravy a přidávání filtrů.
linktitle: How to Create Photo Filter Layer in PSD Using Java
second_title: Aspose.PSD Java API
title: Jak vytvořit vrstvu foto filtru v PSD pomocí Javy
url: /cs/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spravovat vrstvu úpravy filtru fotografie v PSD – Java

## Úvod
Pokud jste vývojář Java a hledáte, jak **create photo filter layer** objekty uvnitř souborů PSD, jste na správném místě. V tomto tutoriálu vás provedeme používáním Aspose.PSD pro Java k úpravě existujících vrstev úpravy filtru fotografie i k přidání nových. Na konci přesně vědět, jak **create photo filter layer**, upravit její vlastnosti a dokonce **add adjustment layer PSD** soubory programově – což urychlí váš grafický workflow.

## Rychlé odpovědi
- **Která knihovna zpracovává vrstvy PSD v Javě?** Aspose.PSD for Java  
- **Mohu upravit existující vrstvu Photo Filter?** Ano – načtěte PSD, najděte `PhotoFilterLayer` a poté upravte její vlastnosti.  
- **Jak přidám novou vrstvu filtru?** Použijte `addPhotoFilterLayer(Color)` na instanci `PsdImage`.  
- **Potřebuji licenci pro produkci?** Je vyžadována komerční licence; je k dispozici bezplatná zkušební verze.  
- **Jaká verze Javy je podporována?** JDK 8 nebo vyšší (doporučeno JDK 11).  

## Co je vrstva úpravy filtru fotografie?
Vrstva úpravy filtru fotografie je nedestruktivní efekt, který zabarvuje celý obrázek vybranou barvou, podobně jako aplikace fotografického filtru. Žije na vlastní vrstvě, což vám umožňuje upravovat barvu, hustotu a jasnost bez změny původních pixelů.

## Proč použít Aspose.PSD k vytvoření vrstvy filtru fotografie?
- **Plná kontrola** nad strukturou PSD bez Adobe Photoshop.  
- **Cross‑platform** Java API funguje na Windows, Linux a macOS.  
- **Žádná COM interop** – čistá Java, ideální pro server‑side zpracování.  
- **Podporuje PSD verzi 1‑8**, zachovává efekty vrstev a masky.

## Předpoklady
### Základní software
1. Java Development Kit (JDK): Ujistěte se, že máte nainstalovanou kompatibilní verzi JDK na vašem počítači. Můžete si ji stáhnout z [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Pro manipulaci se soubory PSD budete potřebovat knihovnu Aspose.PSD. Můžete si ji stáhnout ze [Aspose releases page](https://releases.aspose.com/psd/java/). Nezapomeňte si prohlédnout [Aspose documentation](https://reference.aspose.com/psd/java/) pro více informací.
3. IDE (Integrated Development Environment): Dobré IDE jako IntelliJ IDEA nebo Eclipse vám usnadní programování.

### Pochopení základů
Znalost programování v Javě a základní pochopení fungování souborů PSD bude užitečná. Pokud jste v používání knihoven v Javě noví, je dobré si zvyknout na importování a využívání frameworků.

## Import balíčků
Pro zahájení je potřeba importovat potřebné třídy z knihovny Aspose.PSD. Zde je jednoduchý import, který budete potřebovat na začátku vašeho Java souboru:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
Jednoduše vložte toto na začátek vašeho Java souboru a můžete začít pracovat s PSD obrázky!

## Úprava existující vrstvy filtru fotografie
### Krok 1: Nastavte adresář s daty
Nejprve musíte definovat adresář, kde jsou uloženy vaše PSD soubory. Nahraďte `"Your Document Directory"` skutečnou cestou. Takto si vše uspořádáte:
```java
String dataDir = "Your Document Directory";
```

### Krok 2: Načtěte svůj PSD soubor
Nyní načtěte PSD soubor, který chcete upravit. Ujistěte se, že `PhotoFilterAdjustmentLayer.psd` existuje ve vámi zadaném adresáři.
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```

### Krok 3: Inicializujte objekt obrázku
Pomocí vestavěné funkčnosti Aspose načteme obrázek do našeho projektu:
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### Krok 4: Procházejte vrstvy
Dále prozkoumáme vrstvy v PSD souboru. Naším cílem je najít `PhotoFilterLayer`:
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // Make changes to the layer
    }
}
```

### Krok 5: Přizpůsobte vrstvu filtru fotografie
Zde se děje magie! Můžete upravit `Color` a `Density`. Například můžeme nastavit barvu na živou červenou a upravit hustotu:
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```

### Krok 6: Uložte upravený PSD soubor
Nakonec uložte změny a vytvořte nový PSD soubor s vašimi úpravami:
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
Právě jste upravili vrstvu úpravy filtru fotografie v souboru PSD.

## Přidání nové vrstvy filtru fotografie
### Krok 1: Nastavte cestu k adresáři
Stejně jako dříve, začneme definováním našeho datového adresáře:
```java
String dataDir = "Your Document Directory";
```

### Krok 2: Načtěte zdrojový soubor
Pro tento příklad načtěme jiný PSD soubor, do kterého chceme **add adjustment layer PSD**:
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```

### Krok 3: Znovu inicializujte objekt obrázku
Musíme vytvořit novou instanci `PsdImage`, takže soubor načteme:
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### Krok 4: Přidejte vrstvu filtru fotografie
Nyní můžeme přidat novou vrstvu Photo Filter s vlastní barvou. Takto se to provádí:
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```

### Krok 5: Uložte nový PSD soubor
Opět je čas uložit naše změny. Zde je řádek, který to provede:
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
Úspěšně jste přidali novou vrstvu filtru fotografie do vašeho PSD souboru.

## Časté problémy a řešení
- **`ClassCastException` při načítání obrázku** – Ujistěte se, že načítaný soubor je PSD; jiné formáty vyžadují jiné třídy.  
- **Hodnoty barev jsou nesprávné** – Použijte `Color.fromArgb(alpha, red, green, blue)`, kde každá komponenta je 0‑255.  
- **Vrstva nebyla nalezena** – Ověřte, že zdrojový PSD skutečně obsahuje `PhotoFilterLayer`. Použijte `im.getLayers().length` pro ladění.

## Často kladené otázky
### Co je Aspose.PSD?
Aspose.PSD je knihovna pro .NET a Javu pro vytváření, úpravu a konverzi souborů PSD.

### Můžu vyzkoušet Aspose.PSD zdarma?
Ano, Aspose nabízí bezplatnou zkušební verzi. Vyzkoušejte ji [zde](https://releases.aspose.com/).

### Kde najdu dokumentaci?
Kompletní dokumentaci najdete na [referenční stránce Aspose](https://reference.aspose.com/psd/java/).

### Jak mohu zakoupit Aspose.PSD?
Software můžete zakoupit na [tomto odkazu](https://purchase.aspose.com/buy).

### Je k dispozici podpora pro Aspose.PSD?
Určitě! Podporu můžete získat prostřednictvím fóra Aspose [zde](https://forum.aspose.com/c/psd/34).

---

**Poslední aktualizace:** 2026-03-28  
**Testováno s:** Aspose.PSD for Java 24.11 (nejnovější k roku 2026)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}