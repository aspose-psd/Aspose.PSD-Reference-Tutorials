---
title: Automatická oprava orientace obrázku JPEG v Javě
linktitle: Automatická oprava orientace obrázku JPEG v Javě
second_title: Aspose.PSD Java API
description: Naučte se automaticky opravovat orientaci obrázků JPEG v Javě pomocí Aspose.PSD. Vylepšete své dovednosti zpracování obrazu bez námahy.
weight: 12
url: /cs/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Automatická oprava orientace obrázku JPEG v Javě

## Zavedení
V dnešní digitální době se programová manipulace a optimalizace obrázků stala zásadním úkolem pro vývojáře napříč různými doménami. Aspose.PSD for Java dává vývojářům k dispozici robustní nástroje pro efektivní zpracování PSD, JPEG a dalších obrazových formátů. Tento výukový program se ponoří do konkrétního úkolu: automatická korekce orientace obrázku JPEG pomocí Aspose.PSD pro Java. Ať už vytváříte aplikaci pro úpravu fotografií, spravujete zdroje obrázků v systému pro správu obsahu nebo automatizujete pracovní postupy zpracování obrázků, tato příručka vás vybaví znalostmi nezbytnými pro bezproblémovou integraci této funkce do vašich aplikací Java.
## Předpoklady
Než se pustíte do tohoto výukového programu, ujistěte se, že máte nastaveny následující předpoklady:
- Vývojové prostředí Java: Ujistěte se, že máte v systému nainstalovanou sadu Java Development Kit (JDK).
-  Aspose.PSD for Java JAR: Stáhněte si knihovnu Aspose.PSD pro Java z[zde](https://releases.aspose.com/psd/java/).
- Integrované vývojové prostředí (IDE): Pro vývoj v Javě použijte IntelliJ IDEA, Eclipse nebo jakékoli IDE dle vašeho výběru.
- Základní porozumění Javě a zpracování obrazu: Výhodou bude znalost programování v Javě a základních konceptů zpracování obrazu.

## Importujte balíčky
Než začnete s příkladem, ujistěte se, že jste importovali potřebné balíčky z Aspose.PSD pro Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## Krok 1: Načtěte obrázek PSD
Nejprve načtěte obrázek PSD, který obsahuje miniaturu JPEG, jejíž orientace vyžaduje opravu:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 Nahradit`"Your Document Directory"` se skutečnou cestou k adresáři, kde se nachází váš soubor PSD.
## Krok 2: Opakujte zdroje obrázků
Dále projděte zdroje obrázků a najděte zdroj miniatur JPEG:
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Najděte zdroj miniatur. Obvykle jsou ve formátu souboru Jpeg.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Upravte data miniatur.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // Pokud je uložena miniatura, automaticky ji otočte.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```
## Krok 3: Uložte obrázek
Nakonec po použití automatického otočení uložte opravený obrázek:
```java
image.save();
```
Tento krok zajistí, že změny provedené na obrázku zůstanou zachovány.

## Závěr
Závěrem lze říci, že použití Aspose.PSD for Java poskytuje výkonné řešení pro automatickou korekci orientace obrázků JPEG v souborech PSD. Podle kroků uvedených v tomto kurzu mohou vývojáři vylepšit své pracovní postupy zpracování obrázků a zajistit, aby se obrázky správně zobrazovaly na různých platformách a zařízeních.
## FAQ
### Co je Aspose.PSD for Java?
Aspose.PSD for Java je výkonná knihovna, která umožňuje vývojářům Java pracovat s PSD, JPEG a dalšími obrazovými formáty programově.
### Jak si mohu stáhnout Aspose.PSD pro Javu?
 Knihovnu si můžete stáhnout z[zde](https://releases.aspose.com/psd/java/).
### Podporuje Aspose.PSD for Java manipulaci s obrázky?
Ano, podporuje různé úlohy manipulace s obrázky, jako je změna velikosti, oříznutí a úprava orientace.
### Kde najdu dokumentaci k Aspose.PSD pro Javu?
 K dispozici je obsáhlá dokumentace[zde](https://reference.aspose.com/psd/java/).
### Mohu vyzkoušet Aspose.PSD pro Javu zdarma?
 Ano, můžete získat bezplatnou zkušební verzi od[zde](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
