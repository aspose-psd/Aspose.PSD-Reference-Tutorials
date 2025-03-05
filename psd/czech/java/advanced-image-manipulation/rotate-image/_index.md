---
title: Otočte obrázek v Aspose.PSD pro Java
linktitle: Otočit obrázek
second_title: Aspose.PSD Java API
description: Prozkoumejte rotaci obrazu v Javě bez námahy s Aspose.PSD. Snadno otáčejte, překlápějte a ukládejte soubory PSD.
type: docs
weight: 19
url: /cs/java/advanced-image-manipulation/rotate-image/
---
## Zavedení

Aspose.PSD for Java poskytuje výkonnou sadu funkcí pro práci s obrázky a umožňuje vývojářům efektivně manipulovat a zpracovávat soubory PSD. V tomto tutoriálu se zaměříme na jeden konkrétní úkol: otáčení obrázku. Ať už vytváříte aplikaci pro úpravu fotografií nebo jednoduše potřebujete upravit orientaci obrázku, Aspose.PSD tento proces zjednoduší.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.PSD for Java Library: Ujistěte se, že jste si stáhli a nainstalovali knihovnu Aspose.PSD for Java. Najdete zde knihovnu a podrobnou dokumentaci[zde](https://reference.aspose.com/psd/java/).

- Vývojové prostředí Java: Ujistěte se, že máte na svém počítači nastavené vývojové prostředí Java.

-  Ukázkový soubor PSD: Připravte si ukázkový soubor PSD, který chcete otočit. Upravte`sourceFile` proměnná v ukázkovém kódu s cestou k vašemu souboru PSD.

## Importujte balíčky

Začněte importem potřebných balíčků, abyste mohli využít možnosti Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Krok 1: Načtěte obrázek

 Načtěte existující obrázek do instance souboru`Image` třída:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Krok 2: Otočte obrázek

 Otočte obrázek pomocí`rotateFlip` metoda. V tomto příkladu otočíme obrázek o 270 stupňů:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Krok 3: Uložte otočený obrázek

 Uložte otočený obrázek pomocí`save` metoda a určení výstupního formátu (v tomto případě JPEG):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Závěr

Gratuluji! Úspěšně jste otočili obrázek pomocí Aspose.PSD pro Java. Tato jednoduchá, ale výkonná knihovna otevírá svět možností pro manipulaci s obrázky ve vašich aplikacích Java.

## FAQ

### Q1: Je Aspose.PSD kompatibilní s různými formáty obrázků?

Odpověď 1: Ano, Aspose.PSD podporuje různé formáty obrázků, včetně PSD, JPEG, PNG a dalších.

### Q2: Mohu použít vlastní otočení, nejen předdefinované převrácení?

A2: Rozhodně! Aspose.PSD poskytuje flexibilitu pro použití vlastních rotací podle vašich specifických požadavků.

### Q3: Kde najdu další podporu nebo pomoc?

 A3: V případě jakýchkoli dotazů nebo problémů navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) za podporu komunity.

### Q4: Je k dispozici bezplatná zkušební verze?

 A4: Ano, můžete prozkoumat Aspose.PSD pomocí a[zkušební verze zdarma](https://releases.aspose.com/).

### Q5: Jak získám dočasnou licenci?

 A5: Pokud potřebujete dočasnou licenci, můžete ji získat[zde](https://purchase.aspose.com/temporary-license/).