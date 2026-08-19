---
date: 2026-04-05
description: Naučte se exportovat PSD do PNG a sloučit vrstvy PSD pomocí Aspose.PSD
  pro Javu. Obsahuje převod PSD na JPEG, nastavení kvality JPEG a tipy na konverzi
  PSD do TIFF.
keywords:
- export psd to png
- convert psd to jpeg
- how to merge psd
- set jpeg quality
- psd to tiff conversion
linktitle: Exportovat PSD do PNG a sloučit vrstvy pomocí Aspose.PSD pro Javu
second_title: Aspose.PSD Java API
title: Exportujte PSD do PNG a sloučte vrstvy pomocí Aspose.PSD pro Javu
url: /cs/java/psd-layer-management-effects/merge-psd-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD do PNG a sloučení vrstev pomocí Aspose.PSD pro Java

## Úvod

Už jste se někdy zamysleli, jak grafičtí designéři dosahují těch složitých, vrstvených obrázků ve Photoshopu? Tajemství často spočívá v **exporting PSD to PNG** a inteligentním sloučení vrstev. Pokud pracujete s PSD soubory v Javě, zvládnutí těchto technik vám může pomoci vytvářet kompozitní obrázky, snižovat velikost souboru a připravovat aktiva pro web nebo mobilní nasazení. V tomto tutoriálu vás provedeme **how to merge PSD** vrstvami pomocí Aspose.PSD pro Java a také vám ukážeme, jak exportovat výsledek do PNG (nebo JPEG/TIFF podle potřeby). Na konci budete schopni automatizovat správu vrstev a exportní workflow přímo z vaší Java aplikace.

## Rychlé odpovědi
- **Jaká knihovna zpracovává PSD soubory v Javě?** Aspose.PSD for Java.  
- **Mohu exportovat PSD do PNG?** Yes – just set the appropriate image options.  
- **Jak sloučit více vrstev?** Load the PSD, manipulate the `Layer` collection, then save.  
- **Co když potřebuji kontrolu kvality JPEG?** Use `JpegOptions` and set the quality (0‑100).  
- **Je Photoshop vyžadován?** No, Aspose.PSD works independently of Adobe software.

## Co je export PSD do PNG?

Exportování PSD do PNG znamená převod Photoshop dokumentu (PSD) na soubor Portable Network Graphics (PNG) s možností volitelného zploštění nebo sloučení vrstev. PNG zachovává průhlednost a je široce podporováno na webu, což z něj činí populární formát pro UI aktiva.

## Proč programově sloučit vrstvy PSD?

- **Automatizace:** Hromadně zpracovávejte stovky souborů bez ručních kliknutí.  
- **Výkon:** Sloučené vrstvy snižují čas vykreslování v následných aplikacích.  
- **Velikost souboru:** Zploštění nepotřebných vrstev může zmenšit finální obrázek.  
- **Konzistence:** Zajišťuje stejný pořadí vrstev a jejich prolnutí napříč sestaveními.

## Požadavky

1. **Aspose.PSD for Java Library** – stáhněte z [Aspose.PSD for Java download link](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – IntelliJ IDEA, Eclipse nebo jakékoli IDE, které preferujete.  
3. **Sample PSD File** – soubor s více vrstvami (např. `layers.psd`).  
4. **Basic Java Knowledge** – měli byste být obeznámeni s třídami a metodami.  
5. **Aspose Temporary License (Optional)** – pro větší soubory nebo odstranění omezení zkušební verze, získejte [temporary license](https://purchase.aspose.com/temporary-license/).

## Import balíčků

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Průvodce krok za krokem

### Krok 1: Načtení PSD souboru

```java
String dataDir = "Your Document Directory";
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```

> Tento kód načte `layers.psd` do objektu `PsdImage`, čímž získáte plný přístup k jeho vrstvám.

### Krok 2: Prohlédněte vrstvy (jak sloučit psd)

```java
Layer[] layers = psdImage.getLayers();
System.out.println("Total layers: " + layers.length);

for (Layer layer : layers) {
    System.out.println("Layer name: " + layer.getName());
}
```

> Prohlížení názvů vrstev vám pomůže rozhodnout, které z nich zploštit nebo ponechat samostatně.

### Krok 3: Nastavení možností obrázku (nastavení kvality jpeg)

```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(80); // Set the quality of the JPEG image (0-100)
```

> Pokud dáváte přednost PNG nebo TIFF, můžete nahradit `JpegOptions` za `PngOptions` nebo `TiffOptions` – zde by se konfigurovala **psd to tiff conversion**.

### Krok 4: Uložení sloučeného obrázku (export psd do png)

```java
psdImage.save(dataDir + "MergePSDlayers_output.png", jpgOptions);
```

> Metoda `save` zapíše sloučený výsledek do `MergePSDlayers_output.png`.  
> *Tip:* Pro export do PNG nahraďte `jpgOptions` instancí `PngOptions`; zbytek kódu zůstane stejný.

## Časté problémy a řešení

- **File‑not‑found exception:** Ověřte, že `dataDir` končí oddělovačem cesty (`/` nebo `\\`) a že soubor `layers.psd` existuje.  
- **Unexpected colors after merge:** Ujistěte se, že režimy prolnutí vrstev jsou kompatibilní; můžete je upravit pomocí `layer.setBlendMode(...)`.  
- **Large output file:** Snižte kvalitu JPEG nebo použijte úrovně komprese PNG ke zmenšení velikosti.

## Často kladené otázky

**Q: Je možné uložit sloučený obrázek v jiných formátech než JPEG?**  
A: Rozhodně! Aspose.PSD podporuje PNG, BMP, TIFF a další. Stačí použít odpovídající třídu možností (`PngOptions`, `BmpOptions`, `TiffOptions`).

**Q: Jak mohu upravit kvalitu obrázku pro různé výstupní formáty?**  
A: Každá třída možností poskytuje vlastní nastavení kvality/komprese. Pro JPEG použijte `setQuality(int)`. Pro PNG můžete řídit `CompressionLevel`.

**Q: Potřebuji mít nainstalovaný Photoshop pro použití Aspose.PSD pro Java?**  
A: Ne. Aspose.PSD funguje nezávisle na Adobe Photoshopu, takže jej můžete spustit na jakémkoli serveru nebo v CI prostředí.

**Q: Co se stane, pokud před uložením nenastavím možnosti obrázku?**  
A: Knihovna použije výchozí nastavení (např. JPEG kvalita 75). Specifikování možností vám dává kontrolu nad konečným výstupem.

**Q: Mohu převést PSD přímo na TIFF v jednom kroku?**  
A: Ano – vytvořte instanci `TiffOptions` a zavolejte `psdImage.save("output.tiff", tiffOptions);`.

---

**Poslední aktualizace:** 2026-04-05  
**Testováno s:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}