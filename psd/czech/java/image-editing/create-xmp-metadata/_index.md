---
date: 2026-01-01
description: Naučte se vytvářet metadata XMP, přidávat XMP do souborů PSD a aktualizovat
  metadata obrázků pomocí Aspose.PSD pro Javu. Postupujte podle tohoto krok‑za‑krokem
  průvodce nyní.
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: Vytvořte XMP metadata pomocí Aspose.PSD pro Javu
url: /cs/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvoření XMP metadat pomocí Aspose.PSD pro Java

## Úvod

Správa metadat obrázků je běžnou požadavkem pro vývojáře Java, kteří pracují se soubory Photoshop (PSD). V tomto tutoriálu se naučíte **jak vytvořit XMP metadata** pomocí knihovny Aspose.PSD, přidat XMP do PSD obrázku a programově aktualizovat metadata obrázku. Provedeme vás každým krokem, vysvětlíme, proč je každá část důležitá, a poskytneme praktické tipy, které můžete použít v reálných projektech.

## Rychlé odpovědi
- **Co jsou XMP metadata?** Standardizovaný formát pro vkládání popisných informací (autor, klíčová slova atd.) do souborů obrázků.  
- **Proč použít Aspose.PSD?** Poskytuje čisté Java API pro vytváření, čtení a úpravu PSD souborů bez Photoshopu.  
- **Mohu přidat XMP do existujícího PSD?** Ano – můžete aktualizovat metadata obrázku za běhu pomocí `setXmpData`.  
- **Jaké jsou hlavní kroky?** Nastavit velikost obrázku, vytvořit hlavičku/patku, sestavit XMP balíčky, připojit je a uložit.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.

## Co znamená „vytvořit XMP metadata“ v Javě?

Vytvoření XMP metadat znamená sestavit XMP paket (hlavičku, tělo, patku), který popisuje obrázek, a poté tento paket vložit do PSD souboru. Knihovna Aspose.PSD abstrahuje nízkoúrovňové detaily, takže se můžete soustředit na obsah, který chcete uložit.

## Proč přidávat XMP do PSD souborů?

- **Vyhledatelnost:** Umožňuje výkonné vyhledávání v asset‑managementu na základě autora, názvu nebo vlastních značek.  
- **Interoperabilita:** XMP je rozpoznáváno produkty Adobe, Lightroom a mnoha DAM systémy.  
- **Kontrola verzí:** Ukládá historii zpracování (např. město, barevný režim) přímo v souboru.

## Předpoklady

- **Java vývojové prostředí:** Nainstalovaný JDK 8 nebo vyšší a základní znalost Javy.  
- **Aspose.PSD knihovna:** Stáhněte a nastavte knihovnu Aspose.PSD pro Java. Knihovnu a podrobnou dokumentaci najdete [zde](https://reference.aspose.com/psd/java/).  
- **Váš adresář dokumentů:** Rozhodněte, kde budete na svém systému číst/zapisovat PSD soubory.

## Import balíčků

Ve vašem Java projektu importujte potřebné balíčky pro využití funkcí Aspose.PSD:

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## Krok 1: Určete velikost obrázku

Nejprve definujte rozměry plátna pro nový PSD obrázek.

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Krok 2: Vytvořte nový obrázek

Vytvořte prázdný PSD obrázek, který později obohatíme o XMP metadata.

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## Krok 3: Vytvořte XMP hlavičku

Hlavička obsahuje úvodní XML instrukci a GUID, který identifikuje dokument.

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## Krok 4: Vytvořte XMP patku

Patka označuje konec XMP paketu. Nastavením příznaku `true` zapíšete uzavírací instrukci.

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Krok 5: Vytvořte XMP metadata

Přidejte obecné atributy jako autor a popis do hlavního XMP metadata objektu.

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Krok 6: Vytvořte obal XMP paketu

Zabalte hlavičku, patku a hlavní metadata do jednoho paketu, který lze připojit k obrázku.

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Krok 7: Nastavte Photoshop atributy

Vyplňte Photoshop‑specifické pole (město, země, barevný režim), která očekává mnoho Adobe nástrojů.

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Krok 8: Přidejte Photoshop balíček do XMP metadat

Připojte Photoshop balíček k XMP paketu.

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## Krok 9: Nastavte DublinCore atributy

Přidejte Dublin Core metadata jako autor, název a vlastní značku filmu.

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Krok 10: Přidejte DublinCore balíček do XMP metadat

Spojte Dublin Core balíček s existujícím XMP paketem.

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## Krok 11: Aktualizujte XMP metadata v obrázku

Nyní vložte kompletní XMP paket do PSD obrázku.

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## Krok 12: Uložte obrázek

Nakonec zapište PSD soubor na disk (nebo do paměťového proudu), aby byla metadata uložena.

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## Časté problémy a řešení

| Problém | Proč k tomu dochází | Řešení |
|---------|----------------------|--------|
| **`NullPointerException` při `setXmpData`** | XMP paket nebyl kompletně vytvořen (chybí hlavička/patka). | Ujistěte se, že vytvoříte `XmpHeaderPi`, `XmpTrailerPi` a přidáte všechny balíčky před voláním `setXmpData`. |
| **Metadata nejsou viditelné ve Photoshopu** | Photoshop očekává, že XMP paket bude správně zabalen. | Ověřte, že je použito `XmpTrailerPi(true)` a že je paket uložen spolu s obrázkem. |
| **Chyby cesty k souboru** | Použití relativní cesty bez odpovídajících oprávnění. | Použijte absolutní cestu nebo zajistěte, aby aplikace měla právo zápisu do cílové složky. |

## Často kladené otázky

**Q: Je Aspose.PSD kompatibilní s různými formáty obrázků?**  
A: Ano, Aspose.PSD podporuje PSD, PSB, BMP, GIF, JPEG, PNG, TIFF a další, což vám poskytuje flexibilitu napříč formáty.

**Q: Mohu manipulovat s existujícími metadaty pomocí Aspose.PSD?**  
A: Rozhodně. Můžete načíst existující PSD, získat jeho XMP data pomocí `getXmpData()`, upravit paket a znovu jej uložit.

**Q: Existují nějaká omezení velikosti obrázku, kterou Aspose.PSD dokáže zpracovat?**  
A: Aspose.PSD je navržen tak, aby pracoval s velkými obrázky (až několik gigapixelů), omezenými pouze dostupnou pamětí.

**Q: Je k dispozici zkušební verze pro Aspose.PSD?**  
A: Ano, můžete prozkoumat možnosti Aspose.PSD získáním bezplatné zkušební verze [zde](https://releases.aspose.com/).

**Q: Kde mohu získat podporu pro dotazy týkající se Aspose.PSD?**  
A: Pro jakoukoli pomoc nebo dotazy navštivte [Aspose.PSD fórum](https://forum.aspose.com/c/psd/34).

## Závěr

Nyní ovládáte **jak vytvořit XMP metadata**, přidat XMP do PSD a aktualizovat metadata obrázku pomocí Aspose.PSD pro Java. Tyto kroky vám dávají plnou kontrolu nad popisnými informacemi vloženými do vašich obrázků, což je činí vyhledatelnými a připravenými pro následné workflow. Nebojte se experimentovat s dalšími XMP schématy nebo integrovat tento kód do větších pipeline pro zpracování obrázků.

---

**Poslední aktualizace:** 2026-01-01  
**Testováno s:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}