---
date: 2026-10-03
description: Naučte se, jak v Javě číst metadata obrázku a upravovat JPEG EXIF značky
  pomocí Aspose.PSD for Java v tomto krok‑za‑krokem průvodci, ideální pro vývojáře,
  kteří efektivně pracují s metadaty obrázků.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: Čtení a úprava JPEG EXIF značek v Javě
og_description: Naučte se, jak v Javě číst metadata obrázku a upravovat JPEG EXIF
  značky pomocí Aspose.PSD for Java. Tento průvodce ukazuje krok‑za‑krokem kód pro
  extrakci a aktualizaci informací EXIF.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: Jak v Javě číst metadata obrázku a upravovat JPEG EXIF značky
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: Jak v Javě číst metadata obrázku a upravovat JPEG EXIF značky
url: /cs/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Čtení a úprava JPEG EXIF značek v Javě

## Úvod
Pokud potřebujete **java read image metadata** z JPEG souborů a změnit je programově, jste na správném místě. V tomto tutoriálu si projdeme extrakci a aktualizaci EXIF značek pomocí Aspose.PSD pro Java. Na konci budete schopni získat podrobnosti o fotoaparátu, orientaci a vlastní pole a zapsat je zpět do souboru – vše bez grafického editoru.

## Rychlé odpovědi
- **Která knihovna zpracovává JPEG EXIF v Javě?** Aspose.PSD for Java.
- **Kolik řádků kódu je potřeba k načtení EXIF?** Přibližně tři řádky po načtení obrázku.
- **Můžete upravovat EXIF značky?** Ano, můžete změnit jakoukoli standardní nebo vlastní značku a výsledek uložit.
- **Podporované formáty obrázků?** Více než 150 formátů, včetně PSD, JPEG, PNG, TIFF a BMP.
- **Minimální verze Javy?** Java 7 nebo vyšší.

## Proč používat Aspose.PSD pro Java?
Aspose.PSD podporuje **150+ formátů obrázků** a může zpracovávat soubory až do **2 GB** bez načtení celého dokumentu do paměti, což vám poskytuje rychlé operace s metadaty s nízkou spotřebou paměti u velkých kolekcí fotografií. Také poskytuje jednoduché API pro čtení a zápis EXIF, IPTC a XMP dat, což umožňuje efektivní a spolehlivé hromadné zpracování tisíců obrázků.

## Požadavky
1. **Java Development Kit (JDK)** – ujistěte se, že máte JDK 11 nebo novější. Můžete jej stáhnout z [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – získejte nejnovější JAR ze [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse nebo jakýkoli editor, který preferujete.  
4. **Basic Java knowledge** – měli byste být zdatní v vytváření projektů a přidávání externích JAR souborů.

## Co je Java read image metadata?
Java read image metadata označuje proces programového přístupu k vloženým informacím, jako jsou EXIF, IPTC a XMP, uloženým uvnitř souborů obrázků pomocí Java kódu. Tato metadata mohou zahrnovat nastavení fotoaparátu, časová razítka, GPS souřadnice, upozornění na autorská práva a uživatelské komentáře, což umožňuje aplikacím organizovat, vyhledávat a manipulovat s obrázky na základě jejich popisných dat.

## Import balíčků
Nejprve přidejte Aspose.PSD JAR do classpath vašeho projektu a importujte požadované třídy.

Balíček `com.aspose.psd` poskytuje hlavní API pro načítání obrázků a přístup k jejich zdrojům.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Jak číst metadata obrázku z JPEG souborů v Javě?
Načtěte JPEG pomocí `PsdImage.load("image.jpg")`, najděte zdroj miniatury, který obsahuje EXIF data, a poté zavolejte `ExifData.read()`, abyste získali naplněný objekt `ExifData`. Tento jednoprostý přístup vám poskytuje plný přístup ke všem standardním EXIF polím a jakýmkoli vlastním značkám, které jste mohli přidat.

## Krok 1: Načíst PSD obrázek
PsdImage je třída Aspose.PSD představující soubor PSD a poskytuje metody pro přístup k jeho zdrojům a metadatům.  
V tomto kroku načteme PSD obrázek, ze kterého chceme číst EXIF data. Ujistěte se, že váš obrázek je ve správném adresáři.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Krok 2: Procházet zdroje obrázku
ThumbnailResource představuje miniaturu uloženou v souboru PSD, často obsahující vložená EXIF data.  
Jakmile je obrázek načten, dalším krokem je procházet jeho zdroje a najít zdroj miniatury, který typicky obsahuje EXIF data.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Krok 3: Extrahovat EXIF data
JpegExifData je třída, která obsahuje EXIF informace extrahované z JPEG obrázku, umožňující číst a upravovat jednotlivé značky.  
Nyní, když máme zdroj miniatury, můžeme z něj extrahovat EXIF data. EXIF data zahrnují cenné informace jako jméno vlastníka fotoaparátu, hodnotu clony, orientaci a další.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## Krok 4: Upravit EXIF data
Po načtení EXIF dat můžete chtít upravit některá jejich pole. Zde je návod, jak to provést:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## Krok 5: Uložit změny
Nakonec, po úpravě EXIF dat, uložte změny do nového PSD souboru.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Časté problémy a řešení
- **Chybějící zdroj miniatury** – Některé JPEG soubory ukládají EXIF přímo v hlavní hlavičce obrázku. Pokud zdroj miniatury chybí, použijte místo toho `image.getExifData()`.  
- **Velké soubory způsobují OutOfMemoryError** – Ujistěte se, že JVM běží s dostatečnou haldou (`-Xmx2g`) nebo zpracovávejte obrázek ve streamovacím režimu pomocí `PsdImage.load(inputStream, loadOptions)`.  
- **Nepodporované typy značek** – Aspose.PSD podporuje všechny standardní EXIF značky; vlastní značky mohou vyžadovat ruční zpracování na úrovni bajtů.

## Často kladené otázky

**Q: Co jsou EXIF data?**  
A: EXIF (Exchangeable Image File Format) metadata ukládají nastavení fotoaparátu, časová razítka, GPS souřadnice a další informace vložené do JPEG a dalších souborů obrázků.

**Q: Mohu používat Aspose.PSD pro Java zdarma?**  
A: Můžete získat bezplatnou zkušební verzi na [Aspose releases page](https://releases.aspose.com/).

**Q: Je Aspose.PSD pro Java kompatibilní se všemi verzemi Javy?**  
A: Aspose.PSD pro Java podporuje Java SE 7 a vyšší.

**Q: Kde mohu najít další dokumentaci k Aspose.PSD pro Java?**  
A: Podívejte se na [documentation](https://reference.aspose.com/psd/java/) pro více detailů.

**Q: Jak získám podporu pro Aspose.PSD pro Java?**  
A: Podporu můžete získat na [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).

## Závěr
Podle těchto kroků můžete **java read image metadata** z libovolného JPEG, upravit potřebná EXIF pole a zapsat aktualizovaná data zpět do souboru – vše pomocí několika řádků čistého Java kódu. Bohaté API Aspose.PSD zajišťuje spolehlivé a výkonné zpracování metadat, takže jej můžete integrovat do hromadných zpracovatelských pipeline, nástrojů pro správu fotografií nebo jakékoli aplikace, která potřebuje pracovat s informacemi o obrázcích.

---

**Poslední aktualizace:** 2026-10-03  
**Testováno s:** Aspose.PSD for Java 24.5  
**Autor:** Aspose

## Související tutoriály

- [Číst konkrétní informace o EXIF značkách v Javě s Aspose (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [Vytvořit XMP metadata v PSD souborech pomocí Aspose.PSD pro Java](/psd/java/image-editing/create-xmp-metadata/)
- [Změnit velikost obrázku s Aspose.PSD pro Java – kreslení tvarů a základní operace s obrázky](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}