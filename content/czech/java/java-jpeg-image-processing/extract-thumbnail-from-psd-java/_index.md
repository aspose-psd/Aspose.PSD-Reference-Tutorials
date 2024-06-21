---
title: Extrahujte miniaturu z PSD v Javě
linktitle: Extrahujte miniaturu z PSD v Javě
second_title: Aspose.PSD Java API
description: Naučte se, jak extrahovat miniatury ze souborů PSD pomocí Aspose.PSD for Java. Tento podrobný průvodce pokrývá vše od nastavení až po ukládání extrahovaných obrázků.
type: docs
weight: 15
url: /cs/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## Úvod
tomto tutoriálu prozkoumáme, jak extrahovat miniatury ze souborů PSD pomocí Aspose.PSD pro Java. Miniatury mohou být užitečné pro rychlé náhledy nebo pro vytváření menších verzí obrázků vložených do dokumentů PSD. Pojďme se ponořit do kroků potřebných k dosažení tohoto pomocí Aspose.PSD.
## Předpoklady
Než začneme, ujistěte se, že máte následující nastavení:
- Java Development Kit (JDK) nainstalovaný ve vašem systému.
-  Aspose.PSD pro knihovnu Java. Můžete si jej stáhnout z[tady](https://releases.aspose.com/psd/java/).
- Základní znalost programování v Javě.
## Importujte balíčky
Chcete-li začít, zahrňte do své třídy Java potřebný balíček Aspose.PSD:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Krok 1: Načtěte soubor PSD
Nejprve načtěte soubor PSD, který obsahuje miniaturu, kterou chcete extrahovat.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Nahradit`"Your_Document_Directory/"` s cestou k adresáři, kde se nachází váš soubor PSD, a`"your_file.psd"` s názvem vašeho PSD souboru.
## Krok 2: Opakujte zdroje obrázků
Procházejte zdroje obrázků a najděte zdroj miniatur.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extrahujte data miniatur
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Vytvořte nový obrázek s extrahovanými daty miniatur
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Uložte extrahovanou miniaturu jako samostatný soubor JPEG
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Zpráva o úspěchu výstupu
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Jakmile je miniatura nalezena a zpracována, opusťte smyčku
    }
}
```
## Krok 3: Uložte extrahovanou miniaturu
Uložte extrahovanou miniaturu jako samostatný soubor obrázku (v tomto případě jako soubor JPEG).
## Krok 4: Práce s různými typy miniatur
 Pokud váš soubor PSD může obsahovat více typů miniatur, jako např`Thumbnail4Resource`, můžete rozšířit logiku, abyste tyto případy řešili podobně.

## Závěr
V tomto tutoriálu jsme prozkoumali, jak extrahovat miniatury ze souborů PSD pomocí Aspose.PSD pro Java. Podle výše uvedených kroků můžete efektivně načítat a ukládat miniatury vložené do vašich dokumentů PSD.

## FAQ
### Co je Aspose.PSD?
Aspose.PSD je knihovna Java, která umožňuje vývojářům pracovat s PSD a dalšími formáty obrazových souborů programově.
### Kde najdu další dokumentaci k Aspose.PSD pro Javu?
 Můžete odkazovat na[dokumentace](https://reference.aspose.com/psd/java/) pro podrobné odkazy a příklady API.
### Mohu si Aspose.PSD vyzkoušet zdarma před nákupem?
 Ano, můžete si stáhnout a[zkušební verze zdarma](https://releases.aspose.com/) zhodnotit možnosti knihovny.
### Jak mohu získat dočasné licence pro Aspose.PSD?
 Dočasné licence lze získat od[tady](https://purchase.aspose.com/temporary-license/).
### Je Aspose.PSD vhodný pro komerční použití?
Ano, Aspose.PSD lze v rámci licenčních podmínek používat pro osobní i komerční projekty.