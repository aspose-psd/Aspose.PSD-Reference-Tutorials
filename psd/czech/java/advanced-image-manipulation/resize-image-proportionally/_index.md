---
title: Změňte velikost obrázku proporcionálně pomocí Aspose.PSD pro Javu
linktitle: Změňte velikost obrázku proporcionálně
second_title: Aspose.PSD Java API
description: Vylepšete své Java aplikace pomocí Aspose.PSD. Postupujte podle našeho průvodce a změňte velikost obrázků proporcionálně bez námahy. Zvyšte své možnosti zpracování obrazu ještě dnes.
weight: 17
url: /cs/java/advanced-image-manipulation/resize-image-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Změňte velikost obrázku proporcionálně pomocí Aspose.PSD pro Javu

## Zavedení

Vítejte v našem podrobném průvodci proporcionální změnou velikosti obrázků pomocí Aspose.PSD pro Java. Pokud chcete vylepšit své Java aplikace o efektivní možnosti změny velikosti obrázků, jste na správném místě. V tomto tutoriálu vás provedeme procesem pomocí jasných a stručných kroků.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

1. Prostředí Java: Ujistěte se, že máte v systému nainstalovanou Javu.
2.  Knihovna Aspose.PSD: Stáhněte a nainstalujte knihovnu Aspose.PSD. Můžete najít potřebné zdroje[zde](https://releases.aspose.com/psd/java/).

## Importujte balíčky

Jakmile budete mít své požadavky seřazené, importujte požadované balíčky do svého projektu Java. Ujistěte se, že knihovna Aspose.PSD je ve vašem projektu správně odkazována.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Načtěte obrázek

Začněte načtením obrázku, jehož velikost chcete změnit, do aplikace Java.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Krok 2: Zadejte šířku a výšku

Určete novou šířku a výšku obrázku se změněnou velikostí. V tomto příkladu změníme velikost obrázku na polovinu původních rozměrů.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Krok 3: Uložte obrázek se změněnou velikostí

Uložte obrázek se změněnou velikostí do požadovaného umístění a zadejte možnosti formátu (v tomto případě PNG).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

A tady to máte! Úspěšně jste proporcionálně změnili velikost obrázku pomocí Aspose.PSD pro Java.

## Závěr

V tomto tutoriálu jsme probrali základní kroky k proporcionální změně velikosti obrázků pomocí knihovny Aspose.PSD pro Javu. Nyní můžete tuto funkci bez námahy integrovat do svých aplikací Java pro lepší práci s obrázky.

## FAQ

### Q1: Je Aspose.PSD kompatibilní se všemi formáty obrázků?

 Odpověď 1: Aspose.PSD podporuje různé formáty obrázků, včetně PSD, PNG, JPEG a dalších. Zkontrolujte[dokumentace](https://reference.aspose.com/psd/java/) pro úplný seznam.

### Q2: Mohu použít Aspose.PSD pro komerční projekty?

 A2: Ano, můžete. Navštivte[nákupní stránku](https://purchase.aspose.com/buy) pro podrobnosti o licencích.

### Q3: Jsou k dispozici dočasné licence pro testovací účely?

 A3: Ano, můžete získat dočasnou licenci[zde](https://purchase.aspose.com/temporary-license/) pro hodnocení.

### Q4: Kde najdu podporu pro Aspose.PSD?

 A4: Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) za podporu a pomoc komunity.

### Q5: Jak mohu získat přístup k dokumentaci Aspose.PSD?

 A5: Viz podrobná dokumentace[zde](https://reference.aspose.com/psd/java/).
`
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
