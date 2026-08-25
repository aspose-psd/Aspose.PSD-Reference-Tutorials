---
date: 2026-08-01
description: Zjistěte, jak exportovat PSD do PNG a zpracovávat nezkomprimované obrazové
  streamy pomocí Aspose.PSD for Java.
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: Zpracování objektu nezkomprimovaného obrazového streamu v PSD – Java
og_description: export psd do png pomocí Aspose.PSD for Java. Zjistěte, jak zpracovávat
  nezkomprimované obrazové streamy, vytvářet grafické objekty a ukládat PNG ve vysoké
  kvalitě.
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: export psd do png – Průvodce Java pro nezkomprimované streamy PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: Export PSD do PNG – Vytvoření objektu grafiky PSD – Nezkomprimovaný stream
  v Javě
url: /cs/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportovat PSD do PNG – Vytvořit objekt PSD Graphics – Nezkomprimovaný proud v Javě

## Úvod
V tomto krok‑za‑krokem průvodci **exportujete PSD do PNG** při práci s nekomprimovaným obrazovým proudem pomocí Aspose.PSD pro Java. Ať už automatizujete designový pipeline nebo vytváříte vlastní editor, schopnost vykreslit soubor Photoshopu bez ztráty kvality je nezbytná. Začneme požadovaným nastavením, projdeme vytvoření objektu `Graphics` a skončíme exportem PNG beze ztráty. Na konci pochopíte, proč Aspose.PSD efektivně pracuje s raw proudy a jak jej integrovat do jakéhokoli Java projektu.

## Rychlé odpovědi
- **Co znamená „create PSD graphics object“?** Znamená to vytvoření kontextu `Graphics`, který vám umožňuje programově kreslit na nebo upravovat PSD obrázek.  
- **Která knihovna pracuje s nekomprimovanými proudy?** Aspose.PSD pro Java poskytuje plnou podporu pro raw (nekomprimovaná) obrazová data.  
- **Mohu exportovat PSD do PNG po úpravě?** Ano — jakmile máte objekt `Graphics`, můžete PSD vykreslit a uložit jej jako PNG v jediném volání.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkční nasazení je vyžadována komerční licence.  
- **Je export bezeztrátový?** Export do PNG zachovává původní pixelová data, poskytuje bezeztrátovou kvalitu s menší velikostí souboru než raw PSD.

## Co je export PSD do PNG?
Exportování PSD do PNG převádí vrstvený dokument Photoshopu na jednovrstvý, bezeztrátový rastrový obrázek, který může zobrazit jakýkoli webový prohlížeč nebo prohlížeč obrázků. Proces zachovává průhlednost, barevnou hloubku a efekty vrstev, zatímco odstraňuje specifická metadata Photoshopu. Také zachovává originální barevný profil pro přesnou reprodukci barev.

## Proč použít Aspose.PSD pro Java pro manipulaci s obrázky?
Aspose.PSD podporuje **více než 50** vstupních a výstupních formátů — včetně PSD, PNG, JPEG, BMP a TIFF — a může zpracovávat soubory s **více než 200 vrstvami** bez načítání celého dokumentu do paměti. Jeho volba komprese `Raw` ukládá pixelová data nekomprimovaná, což zaručuje pixel‑dokonalou věrnost pro následné úpravy nebo archivaci.

## Požadavky
Než se ponoříme do kódu, ověřte, že máte následující:

- **Java Development Kit (JDK)** — nainstalovaný JDK 8 nebo novější.  
- **Aspose.PSD pro Java** — Stáhněte nejnovější JAR z oficiální stránky vydání: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/). Můžete také získat přístup přes [this link](https://releases.aspose.com/psd/java/) nebo [release page](https://releases.aspose.com/psd/java/). Pro další produkty Aspose klikněte [here](https://releases.aspose.com/).  
- **IDE** — IntelliJ IDEA, Eclipse nebo jakýkoli Java‑kompatibilní editor.  
- **Základní znalost Javy** — Znalost tříd, metod a zpracování výjimek.

S těmito věcmi na místě jste připraveni začít programovat.

## Import balíčků
Třída `Graphics` je kreslicí plocha Aspose.PSD, která vám umožňuje přímo vykreslovat nebo upravovat pixelová data. Třída `PsdImage` představuje PSD soubor v paměti, zatímco `PsdOptions` řídí, jak je obrázek uložen.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Nyní rozdělíme kód na stravitelné kroky, abyste mohli snadno sledovat. Nastavíme prostředí, načteme PSD soubor, upravíme jej a nakonec uložíme výstup.

## Krok 1: Definujte adresář dokumentů
Před jakýmikoli operacemi se soubory musíte programu sdělit, kde hledat vaše PSD zdroje. Tato cesta adresáře je používána v celém tutoriálu.

```java
String dataDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` absolutní cestou, která obsahuje `layers.psd`. Udržení cesty konfigurovatelné činí kód znovupoužitelným napříč projekty.

## Krok 2: Vytvořte ByteArrayOutputStream
`ByteArrayOutputStream` je Java proud, který uchovává data v paměti jako pole bajtů. Funguje jako paměťová vyrovnávací paměť pro upravený obrázek, což vám umožňuje zachytit raw bajty před jejich zápisem na disk nebo odesláním přes síť.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Proměnná `ms` bude po operaci `save` obsahovat nekomprimovaná data obrázku.

## Krok 3: Načtěte PSD soubor
Třída `PsdImage` načte PSD soubor do paměti pro manipulaci. Načtení souboru převádí PSD na disku na objekt `PsdImage`, který můžete upravovat. V tomto kroku Aspose.PSD čte hlavičku souboru, vrstvy a zdroje.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Pokud je cesta nesprávná, Aspose.PSD vyhodí `FileNotFoundException`, kterou byste měli zachytit v produkčním kódu.

## Krok 4: Nastavte PsdOptions pro ukládání
`PsdOptions` určuje parametry ukládání pro PSD soubory. Nastavení kompresní metody na `Raw` znamená, že pixelová data budou uložena bez komprese, zachovávajíce každý pixel přesně tak, jak je v paměti.

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Volba `CompressionMethod.Raw` ukládá pixelová data bez jakékoli komprese, což je ideální, pokud plánujete později provádět další úpravy.

## Krok 5: Uložte obrázek do výstupního proudu
Nyní uložíte PSD (s případnými úpravami) do dříve vytvořeného `ByteArrayOutputStream`. Metoda `save` respektuje nastavené `PsdOptions`.

```java
psdImage.save(ms, saveOptions);
```

V tomto okamžiku `ms` obsahuje úplnou binární reprezentaci nekomprimovaného PSD.

## Krok 6: Resetujte výstupní proud
Po zápisu ukazatel proudu zůstane na konci. Resetováním jej přetočíte zpět na začátek, abyste mohli číst od začátku.

```java
ms.reset();
```

Představte si to jako přesunutí hlavy pásky zpět na začátek před přehráváním.

## Krok 7: Načtěte nově vytvořený obrázek
Nyní můžete vytvořit novou instanci `PsdImage` přímo z pole bajtů. Tento krok ověřuje, že uložená data lze načíst zpět bez poškození.

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Pokud se obrázek načte úspěšně, víte, že nekomprimovaný proud byl zapsán správně.

## Krok 8: Vytvořte objekt Graphics
Třída `Graphics` je kreslicí plátno Aspose.PSD. Poskytuje metody pro kreslení tvarů, textu a aplikaci filtrů přímo na pixelovou mřížku `PsdImage`.

```java
Graphics graphics = new Graphics(psdImage);
```

S touto instancí `Graphics` můžete malovat nový obsah, mazat části nebo kombinovat další vrstvy.

## Jak exportovat PSD do PNG pomocí Aspose.PSD pro Java?
Načtěte PSD pomocí `new PsdImage(dataDir + "layers.psd")`, vytvořte objekt `Graphics`, proveďte potřebné kreslení a poté zavolejte `psdImage.save("output.png", new PngOptions())`. Tento postup vykreslí upravený PSD a zapíše bezeztrátový PNG v jediném kroku, využívající vestavěný konverzní engine Aspose.PSD.

## Manipulace s vrstvami PSD pomocí objektu Graphics
Mít instanci `Graphics` vám poskytuje kontrolu na úrovni pixelů nad každou vrstvou. Můžete kreslit geometrické tvary, vykreslovat text nebo aplikovat vlastní filtry. Protože grafický kontext pracuje na rasterizovaném zobrazení vrstvy, změny jsou okamžitě viditelné po uložení obrázku.

## Časté problémy a řešení
- **NullPointerException při načítání souboru** — zkontrolujte cestu `dataDir` a ujistěte se, že název souboru přesně odpovídá, včetně velikosti písmen.  
- **Komprimovaný výstup i přes použití Raw** — ověřte, že `saveOptions.setCompressionMethod(CompressionMethod.Raw);` je voláno **před** voláním `save`.  
- **Objekt Graphics se zdá být prázdný** — ujistěte se, že kreslíte na správnou instanci `PsdImage` (tu, kterou jste načetli, ne nově vytvořený prázdný obrázek).  
- **OutOfMemoryError u velkých souborů** — použijte `PsdImage.load(dataDir, LoadOptions)` s `loadOptions.setLoadMode(LoadMode.Memory)`, aby se velké soubory streamovaly bez načítání celého dokumentu do RAM.

## Často kladené otázky

### Co je Aspose.PSD?
Aspose.PSD je Java knihovna, která umožňuje vývojářům programově vytvářet, upravovat a konvertovat Photoshop PSD soubory bez potřeby Adobe Photoshopu. Podporuje čtení a zápis PSD souborů, práci s vrstvami, maskami, kanály a různými obrazovými zdroji a poskytuje API pro rastrové i vektorové operace, což ji činí vhodnou pro server‑side zpracování obrázků a automatizační úkoly.

### Jak mohu stáhnout Aspose.PSD pro Java?
Můžete si jej stáhnout z oficiální stránky vydání: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/).

### Existuje bezplatná zkušební verze pro Aspose.PSD?
Ano, plně funkční zkušební verze je k dispozici na stejné stránce ke stažení. Funguje pro vývoj a evaluační účely.

### Mohu získat podporu pro Aspose.PSD?
Rozhodně! Fórum podpory Aspose poskytuje odpovědi od týmu produktu a komunity: [Aspose support forum](https://forum.aspose.com/c/psd/34).

### Jak mohu získat dočasnou licenci pro Aspose.PSD?
Můžete požádat o dočasnou licenci přímo z licenčního portálu Aspose, který poskytuje časově omezený klíč platný 30 dní. To vám umožní vyhodnotit plnou funkčnost Aspose.PSD bez zakoupení komerční licence. Po uplynutí zkušební doby musíte dočasný klíč nahradit trvalou licencí, abyste mohli knihovnu nadále používat v produkci. Navštivte stránku dočasné licence pro vygenerování časově omezeného klíče: [temporary license page](https://purchase.aspose.com/temporary-license/).

## Často kladené otázky

**Q: Mohu použít objekt graphics k úpravě pouze jedné konkrétní vrstvy?**  
A: Ano. Po načtení PSD získáte požadovanou vrstvu pomocí `psdImage.getLayers().get_Item(index)` a předáte tuto vrstvu konstruktoru `Graphics`.

**Q: Ovlivňuje metoda komprese Raw velikost souboru?**  
A: Raw ukládá pixelová data bez jakékoli komprese, takže výsledný soubor je větší než komprimovaný PSD, ale zaručuje 100 % pixelovou věrnost.

**Q: Je možné exportovat upravený PSD do jiného formátu (např. PNG)?**  
A: Rozhodně. Po úpravě zavolejte `psdImage.save("output.png", new PngOptions())` — to je standardní způsob, jak **exportovat PSD do PNG** s bezeztrátovou kvalitou.

**Q: Jaká verze Javy je vyžadována?**  
A: Aspose.PSD pro Java podporuje JDK 8 a novější, včetně všech LTS verzí až po JDK 21.

**Q: Jak uvolním zdroje po zpracování?**  
A: Zavolejte `psdImage.dispose()` a zavřete všechny proudy (např. `ms.close()`), aby se uvolnila nativní paměť a předešlo se únikům.

---

**Poslední aktualizace:** 2026-08-01  
**Testováno s:** Aspose.PSD for Java (latest release)  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Uložit obrázky do proudu pomocí Aspose.PSD pro Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [Exportovat skupinu vrstev PSD do obrázku pomocí Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [Vytvořit obrázek pomocí proudu v Aspose.PSD pro Java](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}