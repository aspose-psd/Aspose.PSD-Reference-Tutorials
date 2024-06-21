---
title: Převést PSB na PSD v Javě
linktitle: Převést PSB na PSD v Javě
second_title: Aspose.PSD Java API
description: Naučte se, jak plynule převést PSB na PSD v Javě pomocí Aspose.PSD, a zlepšit tak správu grafických souborů ve vašich aplikacích.
type: docs
weight: 12
url: /cs/java/java-psb-to-image-format-conversion/convert-psb-to-psd-java/
---
## Úvod
V oblasti vývoje Java je efektivní manipulace s grafickými soubory klíčová. Tento tutoriál se zaměřuje na využití Aspose.PSD pro Java k bezproblémovému převodu souborů PSB (Photoshop Big) do formátu PSD (Photoshop Document). Pomocí následujících kroků můžete tuto schopnost bez námahy integrovat do svých aplikací Java.
## Předpoklady
Než se ponoříte do procesu převodu, ujistěte se, že máte nastaveny následující předpoklady:
- Java Development Kit (JDK): Ujistěte se, že je ve vašem systému nainstalována verze JDK 8 nebo vyšší.
-  Aspose.PSD for Java Library: Stáhněte a nakonfigurujte knihovnu Aspose.PSD for Java. Můžete jej získat z[tady](https://releases.aspose.com/psd/java/).
- Integrované vývojové prostředí (IDE): Použijte IntelliJ IDEA, Eclipse nebo jiné Java IDE dle vašeho výběru.
- Základní znalost jazyka Java: Porozumění základům programování v jazyce Java bude prospěšné.
## Importujte balíčky
Nejprve importujte potřebné třídy Aspose.PSD do svého souboru Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.FileFormatVersion;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```
## Krok 1: Inicializujte proměnné a načtěte soubor PSB
Začněte definováním proměnných a načtením souboru PSB:
```java
String dataDir = "Your_Document_Directory/";
String sourceFileName = dataDir + "2layers.psb";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```
 Zajistěte výměnu`"Your_Document_Directory/"` s cestou k vašemu skutečnému adresáři dokumentu obsahujícímu soubor PSB.
## Krok 2: Nakonfigurujte možnosti převodu PSD
Dále nakonfigurujte možnosti převodu PSD:
```java
PsdOptions options = new PsdOptions();
options.setFileFormatVersion(FileFormatVersion.Psd);
```
 Tady,`FileFormatVersion.Psd` zajišťuje, že výstupní soubor je ve formátu PSD.
## Krok 3: Uložte konvertovaný soubor PSD
Uložte převedený soubor PSD pomocí načteného obrazu PSB a možností:
```java
image.save(dataDir + "ConvertFromPsb_out.psd", options);
```
 Nahradit`"ConvertFromPsb_out.psd"` s požadovaným názvem výstupního souboru a cestou.

## Závěr
Pomocí těchto kroků jste úspěšně převedli soubor PSB do formátu PSD pomocí Aspose.PSD for Java. Tato schopnost vylepšuje vaše Java aplikace tím, že poskytuje bezproblémovou integraci s formáty souborů aplikace Photoshop.
## FAQ
### Dokáže Aspose.PSD for Java zpracovat složité soubory PSB s více vrstvami?
Ano, Aspose.PSD for Java podporuje soubory PSB s více vrstvami, přičemž během převodu zachovává jejich strukturu.
### Je Aspose.PSD for Java vhodný pro dávkové zpracování převodů PSB na PSD?
Rozhodně můžete dávkové zpracování převodů PSB na PSD efektivně pomocí Aspose.PSD pro Java.
### Zachovává Aspose.PSD for Java kvalitu obrazu během převodu?
Ano, knihovna zajišťuje vysoce věrný převod, zachování kvality obrazu a detailů.
### Mohu integrovat Aspose.PSD for Java do webové aplikace?
Ano, Aspose.PSD for Java lze bez problémů integrovat do desktopových i webových aplikací Java.
### Kde najdu další podporu nebo asistenci pro Aspose.PSD pro Javu?
 Pro další pomoc navštivte stránku[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).