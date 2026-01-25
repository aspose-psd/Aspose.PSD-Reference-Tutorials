---
date: 2026-01-25
description: Naučte se, jak extrahovat miniaturu z PSD souborů pomocí Aspose.PSD pro
  Javu. Postupujte podle tohoto krok‑za‑krokem průvodce a rychle načtěte, extrahujte
  a uložte miniatury.
linktitle: Extract Thumbnail from PSD in Java
second_title: Aspose.PSD Java API
title: Extrahovat miniaturu z PSD v Javě
url: /cs/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extrahovat miniaturu z PSD v Javě

## Úvod
V tomto tutoriálu se naučíte **jak extrahovat miniaturu z PSD** souborů pomocí knihovny Aspose.PSD pro Java. Miniatury jsou malé náhledové obrázky vložené uvnitř PSD dokumentů a jejich extrahování vám může pomoci rychle generovat náhledy, vytvářet galerie obrázků nebo snížit úložiště, když potřebujete jen malou reprezentaci původního díla. Provedeme vás vším od nastavení projektu až po uložení extrahované miniatury jako standardního obrázkového souboru.

## Rychlé odpovědi
- **Co tento tutoriál pokrývá?** Extrahování a uložení obrázku miniatury z PSD souboru pomocí Aspose.PSD pro Java.  
- **Která knihovna je vyžadována?** Aspose.PSD pro Java (ke stažení z oficiálního webu Aspose).  
- **Potřebuji licenci?** Pro produkční použití je vyžadována dočasná nebo plná licence; k dispozici je bezplatná zkušební verze.  
- **Jaký výstupní formát se používá?** Příklad ukládá miniaturu jako JPEG soubor, ale lze zvolit libovolný podporovaný formát.  
- **Jak dlouho trvá implementace?** Přibližně 5‑10 minut pro vývojáře, který ovládá základní koncepty Javy.

## Co znamená „extrahovat miniaturu z PSD“?
Extrahování miniatury z PSD znamená načtení malého náhledového obrázku, který Photoshop ukládá do sekce zdrojů souboru. Tento náhled je typicky nízké rozlišení verze celého plátna, což ho činí ideálním pro rychlé načítání ve správci souborů nebo webových galeriích.

## Proč extrahovat miniatury pomocí Aspose.PSD?
- **Rychlost:** Není nutné otevírat celý PSD v grafickém editoru; miniatura je již vložena.  
- **Automatizace:** Ideální pro dávkové zpracování velkých knihoven obrázků.  
- **Cross‑platform:** Funguje na jakémkoli OS, který podporuje Javu, bez potřeby Photoshopu.  
- **Flexibilita formátu:** Převod miniatury na JPEG, PNG nebo jakýkoli formát podporovaný Aspose.PSD.

## Požadavky
Před zahájením se ujistěte, že máte následující nastaveno:
- Java Development Kit (JDK) nainstalovaný ve vašem systému.  
- Knihovna Aspose.PSD pro Java. Můžete ji stáhnout [zde](https://releases.aspose.com/psd/java/).  
- Základní znalost programování v Javě.

## Import balíčků
Pro zahájení zahrňte potřebný Aspose.PSD balíček ve své Java třídě:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Jak extrahovat miniaturu z PSD pomocí Aspose.PSD pro Java
Níže je podrobný návod krok za krokem. Každý krok obsahuje stručné vysvětlení následované přesným kódem, který je potřeba zkopírovat.

### Krok 1: Načtení PSD souboru
Nejprve načtěte PSD soubor, který obsahuje miniaturu, kterou chcete extrahovat.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
Nahraďte `"Your_Document_Directory/"` cestou ke složce, kde se váš PSD soubor nachází, a `"your_file.psd"` názvem vašeho PSD souboru.

### Krok 2: Procházení obrazových zdrojů
Projděte obrazové zdroje a najděte zdroj miniatury.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```

### Krok 3: Uložení extrahované miniatury
Kód v předchozím kroku již ukládá miniaturu jako JPEG soubor pojmenovaný `extracted_thumbnail.jpg` ve stejné složce. Název souboru nebo formát můžete změnit úpravou parametrů metody `save`.

### Krok 4: Zpracování různých typů miniatur
Pokud váš PSD soubor může obsahovat více typů miniatur, například `Thumbnail4Resource`, můžete logiku rozšířit tak, aby tyto případy zpracovávala podobně. Stačí přidat kontrolu `instanceof Thumbnail4Resource` uvnitř smyčky a zprac soubory obsahují zdroj miniatury. Ověřte zdrojový soubor ve Photoshopu (Soubor → Export → Miniatura) nebo použijte jiný PSD, který obsahuje náhled.  
- **Chyba nepodporovaného formátu obrázku:** Ujistěte se, že používáte aktuální verzi Aspose.PSD, která podporuje požadovaný formát.  
- **Chyby oprávnění při ukládání:** Ověřte, že aplikace má právo zápisu do výstupní složky.

## Často kladené otázky

**Q: Co je Aspose.PSD?**  
A: Aspose.PSD je Java knihovna, která umožňuje vývojářům programově pracovat s PSD a dalšími formáty souborů obrázků.

**Q: Kde mohu najít další dokumentaci k Aspose.PSD pro Java?**  
A: Můžete se podívat na [dokumentaci](https://reference.aspose.com/psd/java/) pro podrobné reference API a příklady.

**Q: Můžu vyzkoušet Aspose.PSD zdarma před zakoupením?**  
A: Ano, můžete si stáhnout [bezplatnou zkušební verzi](https://releases.aspose.com/) pro vyzkoušení možností knihovny.

**Q: Jak mohu získat dočasné licence pro Aspose.PSD?**  
A: Dočasné licence lze získat [zde](https://purchase.aspose.com/temporary-license/).

**Q: Je Aspose.PSD vhodný pro komerční použití?**  
A: Ano, Aspose.PSD může být používán jak pro osobní, tak pro komerční projekty v souladu s licenčními podmínkami.

## Závěr
V tomto tutoriálu jsme prozkoumali, jak **extrahovat miniaturu z PSD** souborů pomocí Aspose.PSD pro Java. Dodržením výše uvedených kroků můžete efektivně získat a uložit miniatury vložené ve vašich PSD dokumentech, což umožní rychlejší náhledy a zjednodušené workflow s obrázky.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-01-25  
**Testováno s:** Aspose.PSD for Java (latest release)  
**Autor:** Aspose