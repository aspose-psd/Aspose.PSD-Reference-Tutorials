---
title: Oříznutí PSD při převodu do PNG pomocí Aspose.PSD pro Javu
linktitle: Oříznutí PSD při převodu do PNG
second_title: Aspose.PSD Java API
description: Naučte se oříznout soubory PSD a převést je na PNG pomocí Aspose.PSD for Java. Vylepšete své Java aplikace o efektivní zpracování obrazu.
weight: 13
url: /cs/java/psd-conversion/cropping-psd-converting-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Oříznutí PSD při převodu do PNG pomocí Aspose.PSD pro Javu

## Zavedení
dynamickém světě vývoje v Javě je zvládnutí efektivního zpracování obrazu zásadní. Tento tutoriál vás provede procesem oříznutí souborů PSD při jejich převodu do formátu PNG pomocí výkonné knihovny Aspose.PSD for Java. Na konci tohoto podrobného průvodce budete vybaveni znalostmi pro vylepšení vašich aplikací Java o bezproblémovou manipulaci s obrázky.
## Předpoklady
Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:
- Základní znalost programování v Javě.
- Java Development Kit (JDK) nainstalovaný ve vašem systému.
- Knihovna Aspose.PSD for Java byla stažena a přidána do vašeho projektu.
- Ukázkový soubor PSD pro experimentování.
## Importujte balíčky
Ujistěte se, že ve svém projektu Java importujete potřebné balíčky pro používání funkcí Aspose.PSD:
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```
## Krok 1: Nastavte svůj projekt
Začněte vytvořením projektu Java a přidáním knihovny Aspose.PSD for Java do cesty třídy vašeho projektu.
## Krok 2: Načtěte obrázek PSD
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// Načtěte existující obrázek PSD
RasterImage image = (RasterImage)Image.load(srcPath);
```
## Krok 3: Definujte oblast oříznutí
```java
// Vytvořte instanci třídy Rectangle předáním x, y, šířky a výšky
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
## Krok 4: Ořízněte obrázek PSD
```java
// Zavolejte metodu oříznutí třídy Image a předejte instanci Rectangle
image.crop(cropRegion);
```
## Krok 5: Nastavte možnosti exportu PNG
```java
// Vytvořte instanci třídy PngOptions
PngOptions pngOptions = new PngOptions();
```
## Krok 6: Uložte oříznutý obrázek jako PNG
```java
// Poskytněte výstupní cestu a PngOptions pro převod souboru PSD na PNG a uložení výstupu
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
## Závěr
Gratuluji! Úspěšně jste se naučili, jak oříznout soubory PSD při jejich převodu na PNG pomocí Aspose.PSD for Java. Tato dovednost nepochybně zlepší vaše schopnosti zpracování obrazu v aplikacích Java.
## Často kladené otázky
### Mohu oříznout soubory PSD s nepravidelnými tvary pomocí Aspose.PSD pro Java?
Ano, Aspose.PSD for Java vám umožňuje definovat vlastní oblast oříznutí, což vám umožní oříznout obrázky do různých tvarů.
### Je Aspose.PSD for Java vhodný pro rozsáhlé úlohy zpracování obrazu?
Absolutně! Aspose.PSD je navržen tak, aby efektivně zpracovával velké obrázky, takže je ideální pro projekty s rozsáhlými požadavky na zpracování obrazu.
### Potřebuji licenci pro Aspose.PSD pro Javu?
 Ano, pro komerční použití je nutná platná licence. Můžete jej získat z[Aspose Nákup](https://purchase.aspose.com/buy).
### Jak mohu vyhledat pomoc nebo nahlásit problémy s Aspose.PSD for Java?
 Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) vyhledat pomoc, sdílet své zkušenosti a nahlásit jakékoli problémy, se kterými se setkáte.
### Mohu vyzkoušet Aspose.PSD pro Javu před nákupem?
 Jistě! Prozkoumejte funkce knihovny pomocí bezplatné zkušební verze[zde](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
