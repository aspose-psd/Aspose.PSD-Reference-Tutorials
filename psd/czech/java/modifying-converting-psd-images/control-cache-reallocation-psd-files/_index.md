---
date: 2026-03-13
description: Naučte se, jak vytvářet projekty Java pro PSD obrázky a zároveň spravovat
  přerozdělování cache pomocí Aspose.PSD pro Java. Efektivně optimalizujte využití
  paměti a disku.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: Vytvořit PSD obrázek v Javě – Ovládání přerozdělování cache
url: /cs/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

ose" keep.

Then closing shortcodes.

Then backtop button shortcode.

Make sure to keep all shortcodes exactly.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Řízení přerozdělování mezipaměti v souborech PSD

## Úvod
Pokud potřebujete efektivně **create PSD image java** projekty, je nezbytné řídit přerozdělování mezipaměti. Při programové práci s obrázky a soubory Photoshopu je efektivita klíčovým faktorem. Aspose.PSD for Java nabízí robustní funkce pro správu a manipulaci se soubory PSD bez problémů. Jedním ze základních aspektů optimalizace výkonu je řízení přerozdělování mezipaměti. Správa mezipaměti pomáhá udržovat rovnováhu mezi využitím paměti a disku, což zajišťuje plynulý běh aplikace bez neočekávaných pádů nebo zpomalení. 

## Rychlé odpovědi
- **Co dělá přerozdělování mezipaměti?** Vyvažuje využití paměti a disku při zpracování velkých souborů PSD.  
- **Který typ mezipaměti je nejlepší pro velké obrázky?** `CacheOnDiskOnly` udržuje paměť volnou tím, že ukládá mezipaměť na disk.  
- **Kolik místa na disku mohu přidělit?** Až 1 GB (nebo jakoukoli velikost, kterou nastavíte pomocí `setMaxDiskSpaceForCache`).  
- **Potřebuji licenci k používání těchto funkcí?** Licence odstraňuje omezení zkušební verze; viz stránka nákupu Aspose.  
- **Mohu sledovat využití mezipaměti za běhu?** Ano, použijte `Cache.getAllocatedDiskBytesCount()` a `Cache.getAllocatedMemoryBytesCount()`.

## Proč řídit přerozdělování mezipaměti?
Správa mezipaměti je zásadní, když **create PSD image java** aplikace pracují s obrázky vysokého rozlišení nebo s vícevrstvými soubory. Správná nastavení mezipaměti zabraňují chybám nedostatku paměti, snižují pauzy GC a poskytují předvídatelný výkon na serverech i desktopových aplikacích.

## Předpoklady
1. Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovaný JDK. Můžete jej stáhnout z [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. Aspose.PSD for Java: Potřebujete stáhnout knihovnu Aspose.PSD. Nejnovější verzi najdete [zde](https://releases.aspose.com/psd/java/).  
3. Nastavení IDE: Integrované vývojové prostředí (IDE) jako IntelliJ IDEA nebo Eclipse vám usnadní správu kódu.  
4. Základní znalost Javy: Znalost programování v Javě vám pomůže lépe pochopit koncepty a úryvky kódu.  
5. Aspose License (Optional): Pokud chcete odstranit vodoznaky a získat plnou funkčnost, zvažte zakoupení licence [zde](https://purchase.aspose.com/buy) nebo vyzkoušejte bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

## Import balíčků
Než začneme psát kód, ujistěme se, že máme importovány potřebné balíčky. Níže je stručný seznam toho, co zahrnout na začátek vašeho Java souboru:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```

## Jak vytvořit PSD Image Java s řízením mezipaměti
Níže je podrobný průvodce, který spojuje konfiguraci mezipaměti přímo s procesem vytváření PSD obrázku v Javě.

### Krok 1: Nastavení adresáře pro data
Nejprve je třeba nastavit adresář, kam budou ukládány soubory mezipaměti. To je nezbytné pro efektivní správu mezipaměti.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: Definuje adresář pro mezipaměť dokumentu.  
- `Cache.setCacheFolder(dataDir)`: Tato metoda nastaví složku mezipaměti na zadaný adresář. Veškerá mezipaměť vytvořená Aspose bude nyní uložena zde místo výchozího dočasného adresáře.

### Krok 2: Konfigurace mezipaměti na disk
Dále specifikujeme, že chceme mezipaměť ukládat pouze na disk. To je užitečné, pokud vaše aplikace pracuje s velkými soubory a chcete zajistit, aby paměť zůstala volná.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: Tato volba zajišťuje, že mezipaměť není držena v paměti, což je výhodné při práci s velkými soubory PSD bez nadměrné spotřeby RAM.

### Krok 3: Nastavení maximální velikosti mezipaměti na disku a v paměti
Nyní omezíme velikosti naší mezipaměti. To je důležité, protože neomezená mezipaměť může vést k problémům s výkonem.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: Nastavuje limit 1 GB pro mezipaměť na disku. Velikost můžete upravit podle svých potřeb.  
- `Cache.setMaxMemoryForCache(1073741824)`: Podobně omezuje mezipaměť v paměti, aby vaše aplikace nevyužívala nadměrnou paměť.

### Krok 4: Správa strategie přerozdělování mezipaměti
Správa toho, jak je mezipaměť přerozdělována, je klíčová pro udržení výkonu. Zde je, jak to nastavit.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: Když je nastaveno na `false`, umožňuje Aspose flexibilněji spravovat přerozdělování mezipaměti, což může vést k lepšímu výkonu.

### Krok 5: Kontrola přidělené velikosti mezipaměti
Tento krok se zaměřuje na sledování, kolik bajtů je aktuálně přiděleno pro mezipaměť v paměti nebo na disku. Implementujme to:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: Ukládá počet bajtů přidělených na disku.  
- `long l2`: Ukládá počet bajtů přidělených v paměti.  
Tyto hodnoty můžete kdykoli zkontrolovat, abyste se ujistili, že aplikace spravuje paměť a disk podle očekávání.

### Krok 6: Vytvoření PSD obrázku
Nyní, když máme nastavenou konfiguraci mezipaměti, vytvoříme jednoduchý PSD obrázek.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Tento objekt umožňuje zadat možnosti při vytváření Photoshop obrázku.  
- `Color[] color`: Pole obsahující barvy, které budou použity v paletě obrázku.

### Krok 7: Uložení pixelových dat do obrázku
Nyní naplníme náš obrázek pixelovými daty a uložíme jej.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: Jedná se o pole objektů barvy. Zde jej naplňujeme bílými pixely.  
- `image.savePixels(image.getBounds(), pixels)`: Tato metoda ukládá pixelová data do obrázku. Aktualizuje obrázek barvami, které jsme definovali.

### Krok 8: Monitorování přidělené mezipaměti po vytvoření obrázku
Po vytvoření obrázku je dobré znovu zkontrolovat, kolik bajtů je přiděleno pro mezipaměť.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: Zachycuje aktuální přidělení na disku po vytvoření obrázku.  
- `long memoryBytes`: Zachycuje aktuální přidělení v paměti.  
Tento krok vám pomůže určit, kolik mezipaměti je spotřebováno po vašich operacích.

### Krok 9: Kontrola správného uvolnění
Nakonec je důležité zajistit, aby všechny objekty Aspose.PSD byly řádně uvolněny, aby nedošlo k únikům paměti.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` a `l2`: Tyto proměnné vám pomohou zkontrolovat konečné přidělení. Pokud nejsou nula, naznačuje to, že některé objekty nebyly řádně uvolněny.

## Časté problémy a řešení
- **Složka mezipaměti nebyla vytvořena** – Ověřte, že aplikace má oprávnění k zápisu do cesty, kterou jste předali `Cache.setCacheFolder`.  
- **Chyby nedostatku paměti** – Zkontrolujte, že `Cache.setCacheType(CacheType.CacheOnDiskOnly)` je nastaveno před načtením velkých souborů PSD.  
- **Neočekávaná velikost mezipaměti** – Použijte metody `Cache.getAllocated*BytesCount()` po každé hlavní operaci pro sledování růstu.

## Často kladené otázky

**Q: Co je Aspose.PSD?**  
A: Aspose.PSD je knihovna pro vývojáře .NET a Java, která umožňuje programově vytvářet, manipulovat a konvertovat soubory Photoshop (PSD).

**Q: Jak zkontrolovat přidělenou velikost mezipaměti?**  
A: Použijte metody jako `Cache.getAllocatedDiskBytesCount()` a `Cache.getAllocatedMemoryBytesCount()` k monitorování aktuálního využití mezipaměti.

**Q: Mohu nastavit vlastní adresář pro mezipaměť?**  
A: Ano, můžete zadat jiný adresář pomocí `Cache.setCacheFolder("Your Directory Path")`.

**Q: Je Aspose.PSD zdarma k použití?**  
A: Aspose.PSD je placená knihovna, ale můžete začít s bezplatnou zkušební verzí dostupnou na jejich [website](https://releases.aspose.com/).

**Q: Co se stane, pokud nebudu uvolňovat objekty?**  
A: Nepouvolnění objektů může vést k únikům paměti, což způsobí, že aplikace bude spotřebovávat více zdrojů, než je nutné.

## Závěr
Řízení přerozdělování mezipaměti při **create PSD image java** aplikacích může výrazně ovlivnit výkon. Dodržením výše uvedených kroků budete efektivně spravovat mezipaměť, minimalizovat spotřebu paměti a generovat vysoce kvalitní PSD soubory s Aspose.PSD for Java. Použijte tyto techniky a vaše projekty poběží plynuleji a budou lépe škálovatelné.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}