---
title: Číst a upravovat JPEG EXIF tagy v Javě
linktitle: Číst a upravovat JPEG EXIF tagy v Javě
second_title: Aspose.PSD Java API
description: V tomto podrobném průvodci se dozvíte, jak číst a upravovat JPEG EXIF tagy pomocí Aspose.PSD for Java. Ideální pro vývojáře, kteří chtějí bez námahy zpracovávat metadata obrázků.
weight: 18
url: /cs/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Číst a upravovat JPEG EXIF tagy v Javě

## Zavedení
Ahoj! Přemýšleli jste někdy, jak můžete číst a upravovat JPEG EXIF tagy pomocí Javy? Pokud ano, jste na správném místě! Tento tutoriál vás provede procesem krok za krokem pomocí Aspose.PSD pro Java. Ať už jste zkušený vývojář nebo nováček, na konci této příručky budete s JPEG EXIF tagy pracovat jako profesionál. Takže, pojďme se ponořit!
## Předpoklady
Než začneme, ujistěte se, že máte následující:
1.  Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK. Můžete si jej stáhnout z[Web společnosti Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD for Java Library: Musíte si stáhnout knihovnu Aspose.PSD for Java. Získejte to z[Aspose stránku vydání](https://releases.aspose.com/psd/java/).
3. Integrované vývojové prostředí (IDE): IDE jako IntelliJ IDEA nebo Eclipse vám usnadní práci s kódováním.
4. Základní znalosti jazyka Java: Pro absolvování tohoto tutoriálu je vyžadována základní znalost jazyka Java.
## Importujte balíčky
Nejprve naimportujme potřebné balíčky. Otevřete své Java IDE a vytvořte nový Java projekt. Poté do závislostí projektu zahrňte knihovnu Aspose.PSD for Java.
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## Krok 1: Načtěte obrázek PSD
tomto kroku načteme PSD obrázek, ze kterého chceme číst EXIF data. Ujistěte se, že je váš obrázek ve správném adresáři.
```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```
## Krok 2: Opakujte zdroje obrázků
Jakmile je obrázek načten, dalším krokem je iterovat jeho prostředky a najít zdroj miniatur, který obvykle obsahuje data EXIF.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Pokračujte dalším krokem
    }
}
```
## Krok 3: Extrahujte data EXIF
Nyní, když máme zdroj miniatur, můžeme z něj extrahovat data EXIF. Data EXIF obsahují cenné informace, jako je jméno vlastníka fotoaparátu, hodnota clony, orientace a další.
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
## Krok 4: Upravte data EXIF
Po přečtení EXIF dat možná budete chtít upravit některá jeho pole. Můžete to udělat takto:
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
## Krok 5: Uložte změny
Nakonec po úpravě EXIF dat uložte změny do nového souboru PSD.
```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Závěr
tady to máte! Pomocí následujících kroků můžete snadno číst a upravovat JPEG EXIF tagy pomocí Aspose.PSD pro Java. Díky této výkonné knihovně je manipulace s metadaty obrázků hračkou. Takže pokračujte a vyzkoušejte to na svých vlastních projektech. Šťastné kódování!
## FAQ
### Co jsou EXIF data?
Data EXIF (Exchangeable Image File Format) obsahují metadata o snímku, jako je nastavení fotoaparátu a orientace.
### Mohu používat Aspose.PSD pro Javu zdarma?
 Můžete získat bezplatnou zkušební verzi od[Aspose stránku vydání](https://releases.aspose.com/).
### Je Aspose.PSD for Java kompatibilní se všemi verzemi Java?
Aspose.PSD for Java podporuje Java SE 7 a vyšší.
### Kde najdu další dokumentaci k Aspose.PSD pro Javu?
 Podívejte se na[dokumentace](https://reference.aspose.com/psd/java/) pro více podrobností.
### Jak získám podporu pro Aspose.PSD pro Javu?
 Můžete získat podporu od[Aspose fórum podpory PSD](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
