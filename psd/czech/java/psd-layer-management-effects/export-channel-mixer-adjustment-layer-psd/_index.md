---
date: 2026-03-31
description: Naučte se, jak uložit PSD jako PNG pomocí Aspose.PSD pro Javu. Tento
  tutoriál pro mixér kanálů PSD ukazuje, jak převést PSD na PNG, upravit vrstvy RGB
  a CMYK a hromadně zpracovávat soubory PSD.
linktitle: Export Channel Mixer Adjustment Layer in PSD - Java
second_title: Aspose.PSD Java API
title: Jak uložit PSD jako PNG s vrstvou úpravy Channel Mixer v Javě
url: /cs/java/psd-layer-management-effects/export-channel-mixer-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak uložit PSD jako PNG s vrstvou úpravy Channel Mixer v Javě

## Úvod

Pokud potřebujete **save PSD as PNG** a zároveň zachovat úpravy provedené vrstvou Channel Mixer, jste na správném místě. V tomto krok‑za‑krokem **psd channel mixer tutorial** vás provedeme načtením souboru PSD, úpravou jak RGB, tak CMYK vrstev Channel Mixer Adjustment Layers a nakonec exportem výsledku do PNG. Také uvidíte, jak lze stejný přístup rozšířit na **batch process PSD files** pro rozsáhlé projekty.

## Rychlé odpovědi
- **What does “save PSD as PNG” mean?** Převádí dokument Photoshopu na bezztrátový PNG při zachování průhlednosti.  
- **Which library handles the conversion?** Aspose.PSD for Java poskytuje plnou podporu pro vrstvy úprav.  
- **Can I work with both RGB and CMYK files?** Ano – API zahrnuje třídy `RgbChannelMixerLayer` a `CmykChannelMixerLayer`.  
- **Do I need a license for production use?** Vyžaduje se licencovaná verze; dočasná licence je k dispozici pro testování.  
- **Is batch processing possible?** Rozhodně – můžete projít složku a aplikovat stejné kroky na každý PSD.

## Co je vrstva úpravy Channel Mixer?

Vrstva úpravy Channel Mixer vám umožňuje přemíchat příspěvky kanálů Červená, Zelená, Modrá (nebo Azurová, Purpurová, Žlutá, Černá) pro dosažení přesné barevné rovnováhy. Na rozdíl od běžné vrstvy je nedestruktivní, což znamená, že původní pixelová data zůstávají nedotčena.

## Proč použít Aspose.PSD pro **convert PSD to PNG**?

- **Full layer fidelity** – všechny vrstvy úprav jsou během konverze zachovány.  
- **No Photoshop required** – spusťte kód na libovolném serveru nebo v CI pipeline.  
- **Supports both RGB and CMYK** – ideální pro workflow připravené na tisk.  

## Požadavky

1. **Aspose.PSD for Java** – stáhněte jej ze [download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK) 8+** – ujistěte se, že `java` je ve vaší PATH.  
3. **IDE** – IntelliJ IDEA, Eclipse nebo jakýkoli editor, který preferujete.  
4. **Sample PSD files** – soubory, které obsahují vrstvy úpravy Channel Mixer (obě varianty RGB i CMYK).

## Importovat balíčky

Nejprve importujte třídy, které budeme potřebovat. Tím se nastaví prostředí pro práci se soubory PSD a možnostmi exportu PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CmykChannelMixerLayer;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.RgbChannelMixerLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Jak **save PSD as PNG** – RGB příklad

### Krok 1: Načtěte soubor PSD, který obsahuje RGB Channel Mixer vrstvu

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ChannelMixerAdjustmentLayerRgb.psd";

PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Ukazujeme na složku obsahující náš PSD (`dataDir`) a načteme soubor do objektu `PsdImage`, který nám poskytuje plný přístup k jeho vrstvám.

### Krok 2: Upravit RGB Channel Mixer vrstvu

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof RgbChannelMixerLayer) {
        RgbChannelMixerLayer rgbLayer = (RgbChannelMixerLayer) im.getLayers()[i];
        rgbLayer.getRedChannel().setBlue((short) 100);
        rgbLayer.getBlueChannel().setGreen((short) -100);
        rgbLayer.getGreenChannel().setConstant((short) 50);
    }
}
```

Procházíme všechny vrstvy, najdeme `RgbChannelMixerLayer` a upravíme hodnoty jejích kanálů. Tento příklad zvyšuje podíl modré v červeném kanálu, snižuje zelenou v modrém kanálu a přidává konstantní posun do zeleného kanálu.

### Krok 3: Uložit upravený PSD (stále PSD)

```java
String psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.psd";
im.save(psdPathAfterChange);
```

Uložení souboru zachová vrstvu úpravy, takže ji můžete později v Photoshopu znovu otevřít, pokud bude potřeba.

### Krok 4: Exportovat obrázek do PNG (krok **save PSD as PNG**)

```java
String pngExportPath = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.png";
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Vytvoříme instanci `PngOptions`, nastavíme typ barvy na `TruecolorWithAlpha`, aby se zachovala průhlednost, a poté exportujeme obrázek.

## Jak **save PSD as PNG** – CMYK příklad

### Krok 5: Načtěte soubor PSD, který obsahuje CMYK Channel Mixer vrstvu

```java
sourceFileName = dataDir + "ChannelMixerAdjustmentLayerCmyk.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

Proces načítání je stejný; pracujeme jen s jiným souborem, který používá barevný model CMYK.

### Krok 6: Upravit CMYK Channel Mixer vrstvu

```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof CmykChannelMixerLayer) {
        CmykChannelMixerLayer cmykLayer = (CmykChannelMixerLayer) img.getLayers()[i];
        cmykLayer.getCyanChannel().setBlack((short) 20);
        cmykLayer.getMagentaChannel().setYellow((short) 50);
        cmykLayer.getYellowChannel().setCyan((short) -25);
        cmykLayer.getBlackChannel().setYellow((short) 25);
    }
}
```

Zde upravujeme kanály CMYK: přidáváme černou do azurové, ladíme žlutou složku purpurové atd. To ukazuje flexibilitu API pro soubory určené k tisku.

### Krok 7: Uložit upravený CMYK PSD

```java
psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.psd";
img.save(psdPathAfterChange);
```

Opět zachováme verzi PSD s novými úpravami.

### Krok 8: Exportovat CMYK obrázek do PNG

```java
pngExportPath = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
img.save(pngExportPath, options);
```

I když je zdroj CMYK, export do PNG automaticky převede obrázek na PNG založený na RGB, přičemž zachová průhlednost.

## Časté problémy a řešení

| Problém | Proč se to děje | Řešení |
|---------|----------------|--------|
| PNG se zobrazuje se špatnými barvami | Konverze CMYK → RGB bez správného profilu | Ujistěte se, že zdrojový PSD má vložený ICC profil; Aspose.PSD jej během exportu respektuje. |
| Vrstva úpravy nebyla nalezena | Neshoda typu vrstvy (např. místo toho vrstva „Color Balance“) | Ověřte třídu vrstvy (`RgbChannelMixerLayer` nebo `CmykChannelMixerLayer`) před přetypováním. |
| Výjimka licence za běhu | Používání knihovny bez platné licence | Použijte dočasnou licenci ze stránky [temporary license](https://purchase.aspose.com/temporary-license/) během vývoje. |

## Často kladené otázky

**Q: Mohu použít Aspose.PSD pro Java s jinými formáty obrázků?**  
A: Ano, knihovna podporuje PNG, JPEG, BMP, TIFF a mnoho dalších kromě PSD.

**Q: Jak zacházet s dalšími vrstvami úprav, jako jsou Curves nebo Levels?**  
A: Každý typ úpravy má vlastní třídu (např. `CurvesAdjustmentLayer`). Můžete s nimi manipulovat podobně jako s příkladem Channel Mixer.

**Q: Existuje způsob, jak **batch process PSD files** do PNG?**  
A: Rozhodně. Zabalte výše uvedené kroky do smyčky `for‑each`, která prochází soubory ve složce a aplikuje stejné úpravy a logiku exportu.

**Q: Jaká je nejlepší praxe pro zachování maximální kvality obrazu při konverzi?**  
A: Použijte `PngOptions` s `TruecolorWithAlpha` a vyhněte se down‑samplingu. Také si ponechte originální PSD, pokud budete později potřebovat bezztrátové úpravy.

**Q: Potřebuji placenou licenci pro produkční použití?**  
A: Ano. Dočasná licence stačí pro hodnocení, ale plná licence je vyžadována pro komerční nasazení.

---

**Poslední aktualizace:** 2026-03-31  
**Testováno s:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}