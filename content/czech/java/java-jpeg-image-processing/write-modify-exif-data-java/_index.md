---
title: Zapisujte a upravujte data EXIF v Javě
linktitle: Zapisujte a upravujte data EXIF v Javě
second_title: Aspose.PSD Java API
description: Naučte se zapisovat a upravovat data EXIF v souborech PSD pomocí Aspose.PSD for Java s tímto komplexním průvodcem krok za krokem.
type: docs
weight: 22
url: /cs/java/java-jpeg-image-processing/write-modify-exif-data-java/
---
## Zavedení
Chcete manipulovat s daty EXIF v souborech PSD pomocí Javy? Pokud ano, pak jste na správném místě! Tento komplexní průvodce vás provede kroky k zápisu a úpravě dat EXIF v Javě pomocí výkonné knihovny Aspose.PSD. 
## Předpoklady
Než se ponoříte do kódu, ujistěte se, že máte vše správně nastaveno.
1. Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovaný JDK.
2.  Aspose.PSD pro Java: Stáhněte si knihovnu z[zde](https://releases.aspose.com/psd/java/).
3. IDE: Použijte IDE jako IntelliJ IDEA nebo Eclipse pro bezproblémové kódování.
4. Základní znalost Javy: Znalost programování v Javě je nutností.
5.  Aspose Temporary License: Získejte dočasnou licenci od[zde](https://purchase.aspose.com/temporary-license/) odemknout plný potenciál Aspose.PSD.
## Importujte balíčky
Nejprve je třeba importovat potřebné balíčky do vašeho projektu Java. Jak na to:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.exif.enums.ExifFlash;
import com.aspose.psd.exif.enums.ExifWhiteBalance;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
Tyto importy vám umožní pracovat se soubory PSD, manipulovat s EXIF daty a využívat výkonné funkce Aspose.PSD.
Nyní, když máte vše nastaveno, pojďme si celý proces rozdělit do jednoduchých, snadno pochopitelných kroků.
## Krok 1: Načtěte obrázek PSD
Chcete-li začít, musíte do projektu načíst soubor PSD. Můžete to udělat takto:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
Tento fragment kódu načte obrázek PSD z vašeho zadaného adresáře.
## Krok 2: Opakujte zdroje obrázků
Dále musíte iterovat zdroje obrázků, abyste našli zdroj miniatur. Zde jsou data EXIF obvykle uložena ve formátu JPEG.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Zkontrolujte zdroje miniatur
}
```
## Krok 3: Identifikujte zdroj miniatur
V tomto kroku identifikujete zdroj miniatur ze zdrojů obrázků.
```java
if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
    // Extrahujte data EXIF ze zdroje miniatur
}
```
## Krok 4: Extrahujte a vytiskněte data EXIF
Jakmile identifikujete zdroj miniatur, dalším krokem je extrahovat data EXIF a vytisknout je na konzoli.
```java
JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
if (exif != null) {
    // Tisk EXIF dat
}
```
## Krok 5: Upravte data EXIF
Nyní přichází ta zábavná část – úprava EXIF dat. Zde je návod, jak můžete nastavit informace LensMake, WhiteBalance a Flash.
```java
exif.setLensMake("Sony");
exif.setWhiteBalance(ExifWhiteBalance.Auto);
exif.setFlash(ExifFlash.Fired);
```
## Krok 6: Uložte obrázek
Po provedení nezbytných úprav uložte obrázek, abyste změny použili.
```java
image.save(dataDir + "Modified_Zebras_Serengeti.psd");
```
## Závěr
tady to máte! Úspěšně jste se naučili, jak zapisovat a upravovat EXIF data v souborech PSD pomocí Aspose.PSD for Java. Tato výkonná knihovna zjednodušuje práci se složitými obrazovými formáty, což z ní činí cenný nástroj pro vývojáře pracující s grafickými soubory. 
 Pro podrobnější informace se podívejte na[Dokumentace Aspose.PSD](https://reference.aspose.com/psd/java/) . Pokud narazíte na nějaké problémy,[Fórum podpory](https://forum.aspose.com/c/psd/34) je skvělé místo pro pomoc. Nezapomeňte prozkoumat[zkušební verze zdarma](https://releases.aspose.com/) a zvážit zakoupení licence[zde](https://purchase.aspose.com/buy) pro plné funkce.
## FAQ
### Co jsou EXIF data?
Data EXIF (Exchangeable Image File Format) jsou metadata vložená do obrazových souborů, která obsahují informace, jako je nastavení fotoaparátu, datum, čas a umístění.
### Dokáže Aspose.PSD zvládnout jiné formáty obrázků?
Ano, Aspose.PSD podporuje různé formáty obrázků včetně PNG, JPEG, BMP a GIF.
### Je Aspose.PSD for Java zdarma?
Můžete použít bezplatnou zkušební verzi, ale pro plné funkce si budete muset zakoupit licenci.
### Jak získám dočasnou licenci pro Aspose.PSD?
 Můžete získat dočasnou licenci[zde](https://purchase.aspose.com/temporary-license/).
### Mohu použít Aspose.PSD pro dávkové zpracování obrázků?
Ano, můžete zpracovat více obrázků v dávce pomocí robustních funkcí Aspose.PSD.