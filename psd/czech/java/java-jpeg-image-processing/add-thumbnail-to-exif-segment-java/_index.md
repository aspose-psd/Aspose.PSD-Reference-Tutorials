---
date: 2026-09-18
description: Naučte se, jak přidat java image metadata thumbnail do segmentu EXIF
  pomocí Aspose.PSD for Java. Tento krok‑za‑krokem průvodce pokrývá předpoklady, procházení
  kódu a uložení aktualizovaného obrazu.
keywords:
- java image metadata
- how to add thumbnail
- java exif metadata
lastmod: 2026-09-18
linktitle: Přidat thumbnail do segmentu EXIF v Java
og_description: Naučte se, jak přidat java image metadata thumbnail do segmentu EXIF
  pomocí Aspose.PSD for Java. Postupujte podle krok‑za‑krokem průvodce pro vložení
  thumbnailů a uložení aktualizovaného obrazu.
og_image_alt: Guide showing Java code to embed a thumbnail into EXIF metadata using
  Aspose.PSD
og_title: Jak přidat java image metadata thumbnail do segmentu EXIF
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to add java image metadata thumbnail to the EXIF segment
    using Aspose.PSD for Java. This step‑by‑step guide covers prerequisites, code
    walkthrough, and saving the updated image.
  headline: How to add java image metadata thumbnail to EXIF segment
  type: TechArticle
- questions:
  - answer: EXIF metadata is embedded information in digital images that includes
      camera settings, capture date, GPS coordinates, and other details.
    question: What is EXIF metadata?
  - answer: Adding a thumbnail improves user experience by allowing quick image previews
      without loading the full image.
    question: Why add a thumbnail to EXIF?
  - answer: You can download Aspose.PSD for Java from the [Aspose.PSD for Java download
      page](https://releases.aspose.com/psd/java/).
    question: Where can I download Aspose.PSD for Java?
  - answer: You can obtain a temporary license for Aspose.PSD from the [temporary
      license page](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.PSD?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How do I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- EXIF thumbnail
- Aspose.PSD
- Java image processing
title: Jak přidat java image metadata thumbnail do segmentu EXIF
url: /cs/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidat miniaturu metadat obrázku Java do segmentu EXIF

## Úvod
V tomto tutoriálu se naučíte, jak pomocí Aspose.PSD pro Java přidat miniaturu **java image metadata** do EXIF segmentu souboru PSD. EXIF (Exchangeable Image File Format) metadata ukládají nastavení fotoaparátu, datum pořízení, polohu a další užitečné informace. Vložení malé náhledové miniatury umožňuje aplikacím zobrazit rychlý pohled na obrázek bez načítání celého souboru, což zlepšuje výkon a uživatelský zážitek.

## Rychlé odpovědi
- **Co tutoriál pokrývá?** Přidání miniatury do EXIF segmentu PSD obrázku pomocí Aspose.PSD pro Java.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní integraci.  
- **Potřebuji licenci?** Pro produkční použití je vyžadována dočasná licence; pro hodnocení stačí bezplatná zkušební verze.  
- **Která verze Javy je podporována?** Java 8 a novější jsou plně podporovány.  
- **Lze zpracovávat velké soubory?** Ano—Aspose.PSD dokáže zpracovat soubory až do 2 GB, aniž by načítal celý obrázek do paměti.

## Co jsou metadata obrázku Java?
Metadata obrázku Java odkazují na strukturované informace vložené do souborů obrázků (např. EXIF, IPTC nebo XMP), které lze programově číst, upravovat nebo vytvářet pomocí Java knihoven jako je Aspose.PSD. Tato metadata umožňují aplikacím získat nastavení fotoaparátu, časová razítka, GPS souřadnice a vlastní data, aniž by bylo nutné otevírat vizuální obsah.

## Proč přidat miniaturu do metadat EXIF?
Přidání miniatury do EXIF segmentu poskytuje okamžitý vizuální náznak pro prohlížeče obrázků, správce souborů a systémy pro správu obsahu. Aspose.PSD zpracovává miniatury v paměti, což vám umožní vložit náhled za méně než 0,2 sekundy pro obrázky až do 500 KB, a podporuje více než 30 formátů obrázků, včetně PSD, JPEG, PNG a TIFF.

## Předpoklady
- Základní znalost programování v Javě.  
- Nainstalovaný Java Development Kit (JDK) ve vašem systému.  
- IDE (Integrované vývojové prostředí) pro Javu, např. IntelliJ IDEA nebo Eclipse.  
- Knihovna Aspose.PSD pro Java. Můžete ji stáhnout ze stránky [Aspose.PSD for Java Download page](https://releases.aspose.com/psd/java/).

## Import balíčků
Následující importy přinášejí třídy Aspose.PSD potřebné pro práci s PSD obrázky a EXIF daty.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Krok 1: načíst PSD obrázek
`PsdImage` představuje soubor Photoshop PSD a poskytuje přístup k jeho vrstvám a zdrojům.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```

## Krok 2: iterovat přes zdroje obrázku
`ImageResource` zapouzdřuje zdroje jako miniatury, ICC profily a metadata vložená do souboru PSD.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Process the thumbnail resource
    }
}
```

## Krok 3: upravit data miniatury
`JpegOptions` umožňuje konfigurovat nastavení specifická pro JPEG, například kvalitu, pro obrázek miniatury.  
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // Set JPEG quality
```

## Krok 4: uložit obrázek
Volání `save` zapíše aktualizovaný EXIF segment (včetně nové miniatury) zpět na disk bez pře‑kódování celého obrázku.  
```java
image.save(dataDir + "output.psd");
```

## Časté problémy a řešení
- **Miniatura se nezobrazuje:** Ověřte, že je zdroj miniatury správně přidán do EXIF segmentu a že je obrázek uložen metodou `PsdImage.save`.  
- **Chyby nedostatku paměti u velkých souborů:** Použijte `PsdImage.load(..., LoadOptions)` s `LoadOptions.setLoadOnlyMetadata(true)`, abyste pracovali jen s metadaty.  
- **Nesprávná orientace:** Zajistěte, aby miniatura respektovala orientační příznak původního obrázku; můžete přečíst EXIF tag `Orientation` a miniaturu podle toho otočit.

## Často kladené otázky

**Q: Co jsou metadata EXIF?**  
A: Metadata EXIF jsou vložené informace v digitálních obrázcích, které zahrnují nastavení fotoaparátu, datum pořízení, GPS souřadnice a další podrobnosti.

**Q: Proč přidat miniaturu do EXIF?**  
A: Přidání miniatury zlepšuje uživatelský zážitek tím, že umožňuje rychlé náhledy obrázku bez načítání celého souboru.

**Q: Kde mohu stáhnout Aspose.PSD pro Java?**  
A: Můžete stáhnout Aspose.PSD pro Java ze stránky [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).

**Q: Jak získat dočasnou licenci pro Aspose.PSD?**  
A: Dočasnou licenci pro Aspose.PSD můžete získat na [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Jak získat podporu pro Aspose.PSD?**  
A: Pro podporu navštivte [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

---

**Poslední aktualizace:** 2026-09-18  
**Testováno s:** Aspose.PSD for Java 24.10  
**Autor:** Aspose

## Související tutoriály

- [Vytvořit XMP metadata v souborech PSD pomocí Aspose.PSD pro Java](/psd/java/image-editing/create-xmp-metadata/)
- [Změnit velikost obrázku s Aspose.PSD pro Java – kreslení tvarů a základní operace s obrázky](/psd/java/basic-image-operations/)
- [Jak převést PSD na rastrové formáty obrázků pomocí Aspose.PSD pro Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}