---
date: 2026-04-05
description: Naučte se, jak vykreslit vrstvu úpravy expozice v souborech PSD pomocí
  Aspose.PSD pro Javu. Krok za krokem průvodce s ukázkami kódu pro úpravu a přidání
  vrstev expozice.
keywords:
- render exposure adjustment layer
- exposure adjustment layer
- Aspose.PSD Java
linktitle: Vykreslit vrstvu úpravy expozice v souborech PSD – Java
second_title: Aspose.PSD Java API
title: Vykreslit vrstvu úpravy expozice v souborech PSD – Java
url: /cs/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vykreslení vrstvy úpravy expozice v souborech PSD – Java

## Úvod

Pracujete se soubory Photoshop PSD a potřebujete **vykreslit vrstvu úpravy expozice** programově? Ať už upravujete existující vrstvy nebo přidáváte nové, Aspose.PSD pro Java poskytuje výkonný a intuitivní způsob, jak tyto úkoly zvládnout. V tomto průvodci vás provedeme, jak použít Aspose.PSD pro Java k vykreslení a úpravě vrstev úpravy expozice v souborech PSD. Na konci tohoto tutoriálu budete vědět, jak upravit nastavení expozice v existujících vrstvách a přidat nové vrstvy úpravy expozice do vašich souborů PSD. Pojďme na to!

## Rychlé odpovědi
- **Jaká knihovna je potřeba?** Aspose.PSD for Java
- **Mohu upravit existující vrstvu expozice?** Ano, můžete změnit expozici, offset a korekci gama.
- **Jak přidám novou vrstvu úpravy expozice?** Použijte `addExposureAdjustmentLayer()` na instanci `PsdImage`.
- **Je podporován export do PNG?** Rozhodně – použijte `PngOptions` k uložení výsledku jako PNG.
- **Potřebuji licenci pro produkci?** Pro produkční použití je vyžadována komerční licence; je k dispozici bezplatná zkušební verze.

## Co je vykreslení vrstvy úpravy expozice?

Vrstva úpravy expozice je nedestruktivní vrstva Photoshopu, která mění jas, offset a gama podkladového obrázku. Její vykreslení znamená aplikaci těchto nastavení tak, aby vizuální výsledek odrážel úpravy, které pak můžete exportovat do formátů jako PNG.

## Proč použít Aspose.PSD pro Java k vykreslení vrstvy úpravy expozice?

- **Plná kontrola** – manipulujte s vlastnostmi vrstev bez otevření Photoshopu.
- **Dávkové zpracování** – automatizujte úpravy napříč mnoha soubory.
- **Cross‑platform** – běží na libovolném systému s JDK.
- **Zachovává strukturu PSD** – udržuje vrstvy editovatelné pro budoucí úpravy.

## Požadavky

1. **Java Development Kit (JDK)** – alespoň JDK 8.
2. **Aspose.PSD for Java** – stáhněte jej z [here](https://releases.aspose.com/psd/java/).
3. **Základní znalost Javy** – měli byste být obeznámeni se standardní syntaxí Javy.
4. **IDE nebo textový editor** – IntelliJ IDEA, Eclipse, VS Code nebo jakýkoli editor, který preferujete.

## Import balíčků

Nejprve importujte požadované třídy Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Jak vykreslit vrstvu úpravy expozice – krok za krokem

### Krok 1: Načtení souboru PSD

Nahraďte `"Your Document Directory"` složkou, která obsahuje vaše soubory PSD. Metoda `Image.load()` vrací objekt `PsdImage`, který vám poskytuje plný přístup k vrstvám dokumentu.

```java
String dataDir = "Your Document Directory";  // Define your document directory
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Source PSD file path

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Load the PSD file
```

### Krok 2: Úprava existující vrstvy úpravy expozice

Cyklus prochází každou vrstvu, najde jakoukoli `ExposureLayer` a aktualizuje její tři klíčové parametry. Toto je jádro **vykreslení vrstvy úpravy expozice** s vašimi vlastními hodnotami.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Adjust the exposure level
        expLayer.setOffset(-0.25f);  // Set the offset
        expLayer.setGammaCorrection(0.5f);  // Adjust the gamma correction
    }
}
```

### Krok 3: Uložení upraveného souboru PSD

Upravený PSD zachovává všechny původní vrstvy nedotčené, ale úprava expozice nyní odráží nová nastavení.

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Path to save the modified PSD file

im.save(psdPathAfterChange);  // Save the changes to the PSD file
```

### Krok 4: Export výsledku jako PNG

Použití `PngOptions` s `TruecolorWithAlpha` zajišťuje, že exportovaný PNG zachová plnou barevnou hloubku a jakoukoli průhlednost z PSD.

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Path to save the PNG file

PngOptions saveOptions = new PngOptions();  // Create PNG options
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

im.save(pngExportPath, saveOptions);  // Save as PNG
```

### Krok 5: Přidání nové vrstvy úpravy expozice

Pokud potřebujete **přidat novou vrstvu úpravy expozice** do existujícího dokumentu, použijte následující kód:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Source PSD file path

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Load the PSD file

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Add new exposure adjustment layer

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Path to save the modified PSD file
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Path to save the PNG file

img.save(psdPathAfterChange);  // Save the changes to the PSD file

PngOptions options = new PngOptions();  // Create PNG options
options.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

img.save(pngExportPath, options);  // Save as PNG
```

## Časté problémy a tipy

- **Vrstva nenalezena** – Ujistěte se, že PSD skutečně obsahuje `ExposureLayer`. Použijte `instanceof ExposureLayer` jak je ukázáno, abyste se vyhnuli `ClassCastException`.
- **Chyby cesty k souboru** – Používejte absolutní cesty nebo ověřte, že `dataDir` končí oddělovačem souborů (`/` nebo `\`).
- **Výjimka licence** – Spuštění bez platné licence přidá vodoznak do výstupu. Zaregistrujte licenci brzy v kódu (`License license = new License(); license.setLicense("Aspose.PSD.lic");`).

## Často kladené otázky

### Co je Aspose.PSD pro Java?

Aspose.PSD pro Java je knihovna, která vám umožňuje programově vytvářet, upravovat a konvertovat soubory PSD pomocí Javy. Poskytuje komplexní funkčnost pro práci s dokumenty Photoshopu.

### Mohu použít Aspose.PSD pro Java k manipulaci s jinými typy vrstev?

Ano, Aspose.PSD pro Java podporuje různé typy vrstev, včetně textových vrstev, vrstev úprav a obrazových vrstev, což umožňuje rozsáhlou manipulaci se soubory PSD.

### Jak začít s Aspose.PSD pro Java?

Můžete začít stažením knihovny z [webové stránky](https://releases.aspose.com/psd/java/) a nahlédnutím do [dokumentace](https://reference.aspose.com/psd/java/) pro podrobné návody a příklady.

### Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro Java?

Ano, je k dispozici bezplatná zkušební verze. Můžete si ji stáhnout [zde](https://releases.aspose.com/).

### Jak mohu získat podporu pro Aspose.PSD pro Java?

Pro podporu můžete navštívit [fórum podpory Aspose](https://forum.aspose.com/c/psd/34), kde můžete klást otázky a získat pomoc od komunity.

**Další otázky**

**Q: Mohu dávkově zpracovávat více souborů PSD?**  
A: Rozhodně. Zabalte logiku načítání, úprav a ukládání do smyčky, která iteruje přes seznam cest k souborům.

**Q: Zachovává knihovna hierarchii vrstev, když přidám novou vrstvu expozice?**  
A: Ano. Nová vrstva je přidána nad existující vrstvy, čímž zachovává původní hierarchii.

**Q: Do jakých obrazových formátů mohu exportovat kromě PNG?**  
A: Aspose.PSD podporuje JPEG, BMP, TIFF a několik dalších formátů prostřednictvím odpovídajících tříd `*Options`.

---

**Poslední aktualizace:** 2026-04-05  
**Testováno s:** Aspose.PSD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}