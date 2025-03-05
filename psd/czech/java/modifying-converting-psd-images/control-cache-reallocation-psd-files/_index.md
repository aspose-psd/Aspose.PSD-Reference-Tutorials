---
title: Ovládejte přerozdělení mezipaměti v souborech PSD
linktitle: Ovládejte přerozdělení mezipaměti v souborech PSD
second_title: Aspose.PSD Java API
description: Spravujte přerozdělení mezipaměti v souborech PSD pomocí Aspose.PSD for Java. Naučte se, jak efektivně optimalizovat práci s pamětí a soubory – ideální pro vývojáře.
type: docs
weight: 22
url: /cs/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---
## Zavedení
Při programové práci s obrázky a soubory Photoshopu je klíčovým faktorem efektivita. Aspose.PSD for Java nabízí robustní funkce pro bezproblémovou správu a manipulaci se soubory PSD. Jedním ze základních aspektů optimalizace výkonu je řízení realokace mezipaměti. Správa mezipaměti pomáhá udržovat rovnováhu mezi využitím paměti a disku a zajišťuje, že vaše aplikace běží hladce, bez neočekávaných selhání nebo zpomalení. 
## Předpoklady
Než se pustíme do kódovací části, je potřeba zajistit několik věcí, aby vše běželo hladce:
1. Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovaný JDK. Můžete si jej stáhnout z[Web společnosti Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Musíte si stáhnout knihovnu Aspose.PSD. Můžete najít nejnovější verzi[zde](https://releases.aspose.com/psd/java/).
3. Nastavení IDE: Integrované vývojové prostředí (IDE) jako IntelliJ IDEA nebo Eclipse vám usnadní správu kódu.
4. Základní porozumění Javě: Znalost programování v Javě vám pomůže lépe porozumět konceptům a úryvkům kódu.
5.  Aspose License (Volitelné): Pokud chcete odstranit vodoznaky a získat plnou funkčnost, zvažte zakoupení licence[zde](https://purchase.aspose.com/buy) nebo vyzkoušet bezplatnou zkušební verzi[zde](https://releases.aspose.com/).
## Importujte balíčky
Než začneme psát kód, ujistěte se, že máme naimportované potřebné balíčky. Níže je stručný seznam toho, co zahrnout na začátek souboru Java:
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
## Krok 1: Nastavení datového adresáře
Nejprve musíte nastavit adresář, kam chcete uložit soubory mezipaměti. To je nezbytné pro efektivní správu mezipaměti.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: Definujte adresář pro mezipaměť dokumentů.
- Cache.setCacheFolder(dataDir): Tato metoda nastaví složku mezipaměti na zadaný adresář. Jakákoli mezipaměť vytvořená Aspose bude nyní uložena zde namísto výchozího dočasného adresáře.
## Krok 2: Konfigurace mezipaměti na disk
Dále určíme, že chceme, aby byla naše mezipaměť uložena pouze na disku. To je zvláště užitečné, pokud vaše aplikace používá velké soubory a chcete zajistit, aby paměť zůstala volná.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): Tato možnost zajišťuje, že mezipaměť nebude uchovávána v paměti, což je výhodné pro práci s velkými soubory PSD bez přílišné spotřeby RAM.
## Krok 3: Nastavení maximální velikosti disku a mezipaměti
Nyní omezme velikost mezipaměti. To je zásadní, protože neomezená mezipaměť může vést k problémům s výkonem.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabajt
Cache.setMaxMemoryForCache(1073741824); // 1 gigabajt
```

- Cache.setMaxDiskSpaceForCache(1073741824): Nastavuje limit 1 GB pro mezipaměť na disku. Tuto velikost si můžete upravit podle svých potřeb.
- Cache.setMaxMemoryForCache(1073741824): Podobně to omezuje mezipaměť v paměti a zajišťuje, že vaše aplikace nebude používat nadměrnou paměť.
## Krok 4: Správa strategie přerozdělení mezipaměti
Správa způsobu přerozdělení mezipaměti je nezbytná pro udržení výkonu. Zde je návod, jak jej nastavit.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): Když je nastaveno na hodnotu false, umožňuje to Aspose spravovat přerozdělení mezipaměti flexibilněji, což může vést k lepšímu výkonu.
## Krok 5: Zkontrolujte velikost přidělené mezipaměti
Tento krok je o sledování, kolik bajtů je aktuálně přiděleno pro mezipaměť v paměti nebo na disku. Pojďme to implementovat:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: Ukládá počet bajtů přidělených na disku.
- long l2: Ukládá počet bajtů přidělených v paměti. 
Tyto hodnoty můžete kdykoli zkontrolovat, abyste se ujistili, že vaše aplikace spravuje využití paměti a disku podle očekávání.
## Krok 6: Vytvoření obrázku PSD
Nyní, když máme nastavenou konfiguraci mezipaměti, vytvoříme jednoduchý obrázek PSD.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- Volby PsdOptions: Tento objekt umožňuje určit volby při vytváření obrazu Photoshopu.
- Barva[] barva: Pole obsahující barvy, které budou použity v paletě obrázků.
## Krok 7: Uložení dat pixelů do obrázku
Nyní naplníme náš obrázek daty pixelů a uložíme jej.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Barva[] pixelů: Toto je pole barevných objektů. Tady to vyplňujeme bílými pixely.
- image.savePixels(image.getBounds(), pixely): Tato metoda uloží data pixelů do obrázku. Aktualizuje obrázek barvami, které jsme definovali.
## Krok 8: Monitorování přidělené mezipaměti po vytvoření obrázku
Po vytvoření bitové kopie je vhodné znovu zkontrolovat, kolik bajtů je alokováno pro mezipaměť.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes: Zachycuje aktuální alokaci na disku po vytvoření obrazu.
- long memoryBytes: Zachycuje aktuální alokaci v paměti. 
Tento krok vám pomůže určit, kolik mezipaměti je spotřebováno po vašich operacích.
## Krok 9: Zkontrolujte správnou likvidaci
Nakonec je důležité zajistit, aby všechny objekty Aspose.PSD byly správně zlikvidovány, aby se zabránilo úniku paměti.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 a l2: Tyto proměnné vám pomohou zkontrolovat konečnou alokaci. Pokud nejsou nulové, znamená to, že některé předměty nebyly správně zlikvidovány.
## Závěr
Řízení realokace mezipaměti v Aspose.PSD pro Java může mít významný rozdíl ve výkonu vaší aplikace. Podle výše uvedených kroků můžete efektivně spravovat mezipaměť, minimalizovat využití paměti a efektivně vytvářet krásné soubory PSD. Osvojte si tyto techniky a sledujte, jak vaše aplikace prosperují s optimálním výkonem!
## FAQ
### Co je Aspose.PSD?
Aspose.PSD je knihovna pro vývojáře .NET a Java, která umožňuje programově vytvářet, manipulovat a převádět soubory Photoshopu (PSD).
### Jak zkontroluji velikost přidělené mezipaměti?
 Použijte metody jako`Cache.getAllocatedDiskBytesCount()` a`Cache.getAllocatedMemoryBytesCount()` sledovat aktuální využití mezipaměti.
### Mohu nastavit vlastní adresář pro mezipaměť?
 Ano, můžete zadat jiný adresář pomocí`Cache.setCacheFolder("Your Directory Path")`.
### Je Aspose.PSD zdarma k použití?
Aspose.PSD je placená knihovna, ale můžete začít s bezplatnou zkušební verzí, která je na nich dostupná[webové stránky](https://releases.aspose.com/).
### Co se stane, když se předmětů nezbavím?
Neodstranění objektů může vést k nevracení paměti, což způsobí, že vaše aplikace bude využívat více prostředků, než je nutné.