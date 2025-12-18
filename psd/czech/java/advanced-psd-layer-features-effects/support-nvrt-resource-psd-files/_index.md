---
date: 2025-12-17
description: Learn how to load PSD files in Java and read PSD layers while supporting
  the Nvrt resource using Aspose.PSD.
linktitle: Support Nvrt Resource in PSD Files using Java
second_title: Aspose.PSD Java API
title: How to Load PSD Files and Support Nvrt Resource using Java
url: /cs/java/advanced-psd-layer-features-effects/support-nvrt-resource-psd-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Podpora zdroje Nvrt v souborech PSD pomocí Javy

## Jak načíst soubory PSD v Javě
Když potřebujete **jak načíst psd** soubory programově, Java nabízí robustní ekosystém – zejména s knihovnou Aspose.PSD. Ať už vytváříte grafický editor, automatizujete designové pipeline nebo extrahujete assety z dokumentů Photoshopu, zvládnutí práce se PSD je nezbytné. V tomto tutoriálu vás provedeme načtením PSD, čtením jeho vrstev a konkrétně podporou zdroje Nvrt (Invert Adjustment).

## Rychlé odpovědi
- **Jaká knihovna zpracovává soubory PSD v Javě?** Aspose.PSD for Java  
- **Mohu číst vrstvy PSD?** Yes, the API provides full access to layer structures  
- **Je licence vyžadována pro produkci?** Yes, a commercial license is needed  
- **Která verze JDK je podporována?** Java 8 and higher  
- **Kde si mohu stáhnout knihovnu?** From the official Aspose download page  

## Předpoklady
Než začnete kódovat, ujistěte se, že máte následující:

- **Java Development Kit (JDK)** nainstalovaný (doporučeno Java 8+)  
- **IDE** jako IntelliJ IDEA, Eclipse nebo VS Code  
- **Aspose.PSD for Java** knihovna – stáhněte ji z oficiální stránky: [Download Aspose.PSD for Java](https://releases.aspose.com/psd/java/)  
- **Základní znalost Javy** (třídy, objekty, zpracování výjimek)  

## Import balíčků
Jakmile je vaše prostředí připravené, importujte požadované třídy. Ty vám umožní pracovat s PSD, procházet vrstvy a pracovat se zdrojem Nvrt.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.InvertAdjustmentLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.NvrtResource;
```

## Proč číst vrstvy PSD?
Čtení vrstev PSD vám umožní:

- Extrahovat jednotlivé assety (např. ikony, masky) pro opětovné použití  
- Analyzovat vrstvy úprav (jako **Nvrt**) pro pochopení úprav obrazu  
- Automatizovat dávkové zpracování designových souborů  

## Krok 1: Určete svůj zdrojový adresář
Nastavte složku, která obsahuje PSD, se kterým chcete pracovat.

```java
String sourceDir = "Your Source Directory";
String inPsdFilePath = sourceDir + "InvertAdjustmentLayer.psd";
```

Nahraďte `"Your Source Directory"` skutečnou cestou ve vašem počítači.

## Krok 2: Načtěte soubor PSD
Nyní skutečně **jak načíst psd** soubory pomocí Aspose API.

```java
PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);
```

Metoda `Image.load()` otevře soubor a připraví jej k inspekci.

## Krok 3: Inicializujte proměnnou zdroje Nvrt
Zde uložíme nalezený zdroj Nvrt.

```java
NvrtResource nvrtResource = null;
```

## Krok 4: Vyhledejte vrstvu Invert Adjustment
Iterujte přes každou vrstvu, najděte `InvertAdjustmentLayer` a poté hledejte `NvrtResource`.

```java
try {
    for (Layer layer : psdImage.getLayers()) {
        if (layer instanceof InvertAdjustmentLayer) {
            for (LayerResource layerResource : layer.getResources()) {
                if (layerResource instanceof NvrtResource) {
                    // The NvrtResource is found
                    nvrtResource = (NvrtResource)layerResource;
                    break;
                }
            }
        }
    }
} finally {
    psdImage.dispose();
}
```

`finally` blok zajišťuje, že PSD obrázek je uvolněn, což udržuje čistotu paměti.

## Krok 5: Ověřte zdroj Nvrt
Potvrďte, že zdroj byl úspěšně nalezen.

```java
Assert.isNotNull(nvrtResource);
```

Pokud tvrzení projde, úspěšně jste přečetli vrstvy PSD a extrahovali zdroj Nvrt.

## Časté úskalí a tipy
- **Kontroly na null:** Vždy ověřte, že `psdImage` a objekty vrstev nejsou null před jejich použitím.  
- **Uvolnění zdrojů:** Zapomenutí `psdImage.dispose()` může vést k únikům paměti v dlouho běžících aplikacích.  
- **Problémy s cestou k souboru:** Používejte absolutní cesty nebo zajistěte, aby pracovní adresář byl nastaven správně, aby nedošlo k `FileNotFoundException`.  

## Závěr
Nyní už víte **jak načíst psd** soubory, číst jejich vrstvy a extrahovat zdroj úpravy Nvrt pomocí Javy a Aspose.PSD. Tento základ vám umožní vytvářet výkonné nástroje pro automatizaci grafiky, dávkově zpracovávat designové assety nebo integrovat data z Photoshopu do širších pracovních toků.

## Často kladené otázky

**Q: Co je Aspose.PSD for Java?**  
A: Aspose.PSD for Java je knihovna, která umožňuje vývojářům vytvářet, upravovat, konvertovat a renderovat PSD soubory přímo z Java kódu.

**Q: Mohu použít Aspose.PSD v komerčních produktech?**  
A: Ano, pro produkční použití je vyžadována komerční licence. Možnosti zakoupení můžete prozkoumat [zde](https://purchase.aspose.com/buy).

**Q: Kde najdu dokumentaci k Aspose.PSD?**  
A: Kompletní dokumentace je k dispozici [zde](https://reference.aspose.com/psd/java/).

**Q: Je k dispozici bezplatná zkušební verze?**  
A: Rozhodně! Bezplatnou zkušební verzi Aspose.PSD for Java získáte [zde](https://releases.aspose.com/).

**Q: Jak mohu získat podporu pro Aspose.PSD?**  
A: Otázky a podporu můžete získat na fóru Aspose: [Aspose Support](https://forum.aspose.com/c/psd/34).

---

**Poslední aktualizace:** 2025-12-17  
**Testováno s:** Aspose.PSD for Java 24.11 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}