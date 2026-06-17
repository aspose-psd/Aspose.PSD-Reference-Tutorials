---
date: 2026-03-21
description: Naučte se, jak používat ICC profily k převodu barevných profilů, aplikovat
  nastavení ICC profilu a nastavit RGB profil při vytváření PSD obrázků pomocí Aspose.PSD
  pro Javu.
linktitle: Color Conversion using ICC Profiles
second_title: Aspose.PSD Java API
title: Jak použít ICC profily pro konverzi barev v Aspose.PSD
url: /cs/java/psd-conversion/color-conversion-icc-profiles/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak používat ICC profily pro konverzi barev v Aspose.PSD

## Úvod
Pokud hledáte **how to use icc** profily, které zaručují přesné barvy napříč zařízeními, jste na správném místě. V tomto tutoriálu vás provedeme konverzí barevného profilu, aplikací ICC profilu a nastavením RGB profilu při **creating a PSD image** pomocí Aspose.PSD pro Java. Ať už budujete dávkový zpracovatelský řetězec nebo editor jedné obrázku, níže uvedené kroky vám poskytnou pevný, připravený základ pro produkci.

## Rychlé odpovědi
- **What is the primary purpose of an ICC profile?** Definuje, jak mají být barvy interpretovány na konkrétním zařízení nebo barevném prostoru.  
- **Which class represents a PSD image in Aspose.PSD?** `PsdImage`.  
- **Can I change both RGB and CMYK profiles?** Ano – použijte `setRgbColorProfile` a `setCmykColorProfile`.  
- **Do I need a license for development?** Bezplatná zkušební verze funguje pro testování; licence je vyžadována pro produkci.  
- **What output format supports YCCK?** JPEG s `JpegCompressionColorMode.Ycck`.

## Co je ICC konverze barev?
Profily ICC (International Color Consortium) jsou standardizované datové sady, které popisují barevné charakteristiky zařízení (monitory, tiskárny, skenery). Pomocí **convert color profile** z jednoho prostoru do druhého zajistíte, že vizuální vzhled zůstane konzistentní, bez ohledu na to, kde je obrázek zobrazen.

## Proč používat ICC profily s Aspose.PSD?
- **Accurate color reproduction** – nezbytné pro branding a tiskové workflowy.  
- **Cross‑platform consistency** – stejný obrázek vypadá stejně na Windows, macOS a mobilních zařízeních.  
- **Built‑in API support** – Aspose.PSD vám umožní **apply icc profile** a **set rgb profile** pomocí několika řádků Java.

## Předpoklady
Před zahájením se ujistěte, že máte následující:

1. **Aspose.PSD for Java** – stáhněte nejnovější knihovnu ze stránky [releases](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – JDK 8+ a vaše oblíbené IDE.  
3. **ICC Profiles** – pro tento příklad použijeme `eciRGB_v2.icc` (RGB) a `ISOcoated_v2_FullGamut4.icc` (CMYK). Můžete je získat z důvěryhodných zdrojů pro správu barev.

## Import balíčků
Přidejte požadované Aspose.PSD jmenné prostory do svého projektu. Tyto importy vám poskytují přístup k manipulaci s obrázky, možnostem JPEG a zdrojům streamu.

```java
import com.aspose.psd.Color;
import com.aspose.psd.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
import com.aspose.psd.sources.StreamSource;
import java.io.File;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
```

## Jak používat ICC profily pro konverzi barev
Níže je krok‑za‑krokem průvodce, který ukazuje **how to convert color** pomocí ICC profilů při **creating a PSD image**.

### Krok 1: Vytvořit nový obrázek (Create PSD Image)
Nejprve vytvořte prázdný `PsdImage`. To vám poskytne plátno, které můžete naplnit pixelovými daty.

```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

### Krok 2: Naplnit data obrázku
Naplněte obrázek surovými ARGB pixelovými hodnotami. V reálném scénáři můžete načíst pixelová data z jiného zdroje, ale zde pouze ilustrujeme proces.

```java
int count = image.getWidth() * image.getHeight();
int[] pixels = new int[count];
int r = 0, g = 0, b = 0, channel = 0;
for (int i = 0; i < count; i++) {
    // Fill pixels with color values.
    // ...
}
// Save the newly created pixels.
image.saveArgb32Pixels(image.getBounds(), pixels);
```

### Krok 3: Uložit obrázek s výchozími ICC profily
Uložení v tomto okamžiku zapíše obrázek s výchozími barevnými profily knihovny. Tento krok vám pomůže vidět rozdíl po aplikaci vlastních profilů později.

```java
image.save(dataDir + "Default_profiles.jpg");
```

### Krok 4: Aktualizovat barevné profily (Apply ICC Profile & Set RGB Profile)
Načtěte externí ICC soubory a přiřaďte je k obrázku. Zde **apply icc profile** a **set rgb profile**.

```java
File rgbFile = new File(dataDir + "eciRGB_v2.icc");
FileInputStream rgbInputStream = new FileInputStream(rgbFile);
StreamSource rgbprofile = new StreamSource(rgbInputStream);
File cmykFile = new File(dataDir + "ISOcoated_v2_FullGamut4.icc");
FileInputStream cmykInputStream = new FileInputStream(cmykFile);
StreamSource cmykprofile = new StreamSource(cmykInputStream);
image.setRgbColorProfile(rgbprofile);
image.setCmykColorProfile(cmykprofile);
```

### Krok 5: Uložit obrázek s novými YCCK profily
Nakonec exportujte obrázek jako JPEG pomocí YCCK barevného režimu, který respektuje CMYK profil, který jsme právě nastavili.

```java
JpegOptions options = new JpegOptions();
options.setColorType(JpegCompressionColorMode.Ycck);
image.save(dataDir + "Ycck_profiles.jpg", options);
```

Po provedení těchto kroků jste **converted the color profile** PSD obrázku, **applied ICC profiles** a **set the RGB profile** pro přesné vykreslení.

## Časté problémy a řešení
| Problém | Důvod | Řešení |
|-------|--------|-----|
| Barvy vypadají po konverzi vybledlé | Špatně přiřazený profil nebo chybějící data profilu | Ověřte, že ICC soubory odpovídají barevnému prostoru zdrojového obrázku. |
| `FileNotFoundException` when loading ICC files | Nesprávná cesta `dataDir` | Použijte absolutní cestu nebo zajistěte, aby soubory byly umístěny ve specifikovaném adresáři. |
| JPEG uložen bez YCCK barev | `JpegOptions` není nastaven na `Ycck` | Zavolejte `options.setColorType(JpegCompressionColorMode.Ycck)` před uložením. |

## Často kladené otázky
**Q: Mohu použít vlastní ICC profily s Aspose.PSD pro Java?**  
A: Ano, jednoduše nahraďte poskytnuté ICC soubory svými vlastními a nasměrujte `StreamSource` na nové soubory.

**Q: Jak mohu řešit barevné rozdíly ve výsledných obrázcích?**  
A: Jemně dolaďte ICC profily nebo použijte color‑adjustment API Aspose.PSD k úpravě jasu, kontrastu nebo gammy po konverzi.

**Q: Je Aspose.PSD vhodný pro dávkové zpracování obrázků?**  
A: Rozhodně. Můžete projít složku s PSD soubory, aplikovat stejnou logiku profilů a efektivně uložit výsledky.

**Q: Kde mohu najít více ICC profilů pro správu barev?**  
A: Podívejte se na web ICC, stránku Adobe s barevnými zdroji nebo knihovny od výrobců, které poskytují zařízení‑specifické profily.

**Q: Jaké jsou výhody používání ICC profilů při konverzi barev?**  
A: Zaručují konzistentní barvy napříč různými zařízeními, zjednodušují automatizaci workflow a snižují manuální úsilí při ladění barev.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Poslední aktualizace:** 2026-03-21  
**Testováno s:** Aspose.PSD for Java (latest)  
**Autor:** Aspose