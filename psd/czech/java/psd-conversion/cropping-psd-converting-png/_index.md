---
date: 2026-03-21
description: Naučte se, jak převést PSD na PNG a oříznout soubory PSD pomocí Aspose.PSD
  pro Javu. Tento průvodce ukazuje krok za krokem zpracování obrázků v Java aplikacích.
linktitle: Cropping PSD when Converting to PNG
second_title: Aspose.PSD Java API
title: Jak převést PSD na PNG při ořezu pomocí Aspose.PSD pro Javu
url: /cs/java/psd-conversion/cropping-psd-converting-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak převést PSD na PNG při ořezu pomocí Aspose.PSD pro Java

## Úvod
V dynamickém světě vývoje v Javě je zvládnutí efektivního zpracování obrázků klíčové. V tomto tutoriálu se naučíte **jak převést PSD na PNG** a oříznout obrázek v jednom workflow pomocí výkonné knihovny Aspose.PSD pro Java. Na konci tohoto krok‑za‑krokem průvodce budete schopni přidat přesné ořezání k vašim exportům PNG a nechat vaše Java aplikace spolehlivě pracovat s PSD zdroji.

## Rychlé odpovědi
- **Co kód dělá?** Načte PSD, ořízne obdélník a uloží jej jako PNG.  
- **Která knihovna je vyžadována?** Aspose.PSD pro Java (nejnovější verze).  
- **Potřebuji licenci?** Ano, pro produkční použití je vyžadována komerční licence.  
- **Mohu definovat libovolnou oblast ořezu?** Samozřejmě – nastavíte požadované X, Y, šířku a výšku.  
- **Je tento přístup rychlý pro velké soubory?** Ano, Aspose.PSD je optimalizováno pro vysoký výkon.

## Co je převod PSD na PNG?
Převod PSD na PNG znamená převést vrstvený Photoshop dokument na bezztrátový PNG obrázek. Tento formát je ideální pro webové doručení, náhledy nebo jakýkoli scénář, kde potřebujete rastrový obrázek bez původních vrstev.

## Proč ořezávat PSD před převodem na PNG?
Ořezání vám umožní extrahovat jen tu část návrhu, kterou potřebujete, čímž snížíte velikost souboru a zaměříte se na relevantní vizuální obsah. Je to zvláště užitečné při generování náhledů, UI assetů nebo přípravě obrázků pro responzivní rozvržení.

## Požadavky
Předtím, než se pustíte do tutoriálu, zajistěte si následující:
- Základní znalosti programování v Javě.  
- Nainstalovaný Java Development Kit (JDK) na vašem systému.  
- Staženou knihovnu Aspose.PSD pro Java a přidanou do vašeho projektu.  
- Ukázkový PSD soubor pro experimentování.

## Import balíčků
Ve vašem Java projektu nezapomeňte importovat potřebné balíčky pro používání funkcí Aspose.PSD:
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Nastavte svůj projekt
Začněte vytvořením Java projektu a přidáním knihovny Aspose.PSD pro Java do classpath vašeho projektu. Tím získáte přístup ke všem třídám pro zpracování obrázků, které budete potřebovat.

## Krok 2: Načtěte PSD obrázek
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// Load an existing PSD image
RasterImage image = (RasterImage)Image.load(srcPath);
```
*Zde načteme zdrojový PSD soubor do objektu `RasterImage`, který poskytuje operace založené na rastrech, jako je ořezání.*

## Krok 3: Definujte oblast ořezu
```java
// Create an instance of Rectangle class by passing x, y, width, and height
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
*Objekt `Rectangle` určuje oblast, kterou chcete zachovat. Upravit hodnoty `x`, `y`, `width` a `height` podle potřeby vašeho návrhu. Tento krok přímo odpovídá klíčovému slovu „definovat oblast ořezu“.*

## Krok 4: Ořízněte PSD obrázek
```java
// Call the crop method of Image class and pass the Rectangle instance
image.crop(cropRegion);
```
*Voláním `crop` upravíte obrázek v paměti a odstraníte vše mimo zadaný obdélník.*

## Krok 5: Nastavte možnosti exportu PNG
```java
// Create an instance of PngOptions class
PngOptions pngOptions = new PngOptions();
```
*`PngOptions` vám umožňuje řídit nastavení specifická pro PNG, jako je úroveň komprese, typ barev a další.*

## Krok 6: Uložte oříznutý obrázek jako PNG
```java
// Provide output path and PngOptions to convert the PSD file to PNG and save the output
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
*Metoda `save` provádí **převod PSD na PNG** a zachovává ořez, který jste definovali.*

## Časté chyby a tipy
- **Nesprávné rozměry obdélníku:** Ujistěte se, že šířka a výška nepřekračují původní velikost obrázku, jinak bude vyvolána výjimka.  
- **Spotřeba paměti u velkých PSD:** Po uložení uvolněte objekt `RasterImage` (`image.dispose()`), aby se uvolnily nativní zdroje.  
- **Licence není nastavena:** Pokud spustíte kód bez platné licence, na výstupním PNG se objeví vodoznak.

## Často kladené otázky
### Mohu ořezávat PSD soubory s nepravidelnými tvary pomocí Aspose.PSD pro Java?
Ano, Aspose.PSD pro Java vám umožňuje definovat vlastní oblast ořezu, což vám umožní ořezávat obrázky do různých tvarů.

### Je Aspose.PSD pro Java vhodné pro rozsáhlé úlohy zpracování obrázků?
Rozhodně! Aspose.PSD je navrženo tak, aby efektivně zvládalo velké obrázky, což ho činí ideálním pro projekty s rozsáhlými požadavky na zpracování obrázků.

### Potřebuji licenci pro Aspose.PSD pro Java?
Ano, pro komerční použití je vyžadována platná licence. Můžete ji získat na [Aspose Purchase](https://purchase.aspose.com/buy).

### Jak mohu získat pomoc nebo nahlásit problémy s Aspose.PSD pro Java?
Navštivte [Aspose.PSD fórum](https://forum.aspose.com/c/psd/34), kde můžete požádat o pomoc, sdílet své zkušenosti a nahlásit jakékoli problémy, na které narazíte.

### Můžu si Aspose.PSD pro Java vyzkoušet před zakoupením?
Samozřejmě! Prozkoumejte funkce knihovny s volným zkušebním obdobím dostupným [zde](https://releases.aspose.com/).

---

**Poslední aktualizace:** 2026-03-21  
**Testováno s:** Aspose.PSD pro Java 24.12 (nejnovější v čase psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}