---
title: Podpora Infx Resource v souborech PSD s Java
linktitle: Podpora Infx Resource v souborech PSD s Java
second_title: Aspose.PSD Java API
description: Naučte se, jak manipulovat s Infx Resource v souborech PSD pomocí Aspose.PSD for Java, pomocí tohoto komplexního, podrobného tutoriálu. Ideální pro vývojáře všech úrovní.
type: docs
weight: 13
url: /cs/java/working-with-psd-files/support-infx-resource-psd-files/
---
## Zavedení

Práce se soubory PSD (Photoshop Document) v Javě se může zdát skličující, ale nemusí. Představte si, že máte vícevrstvý soubor PSD, který obsahuje různé zdroje, a potřebujete upravit konkrétní zdroje – například InfxResource – a přitom zajistit, že integrita souboru zůstane nedotčena. To je místo, kde vstupuje Aspose.PSD for Java, který nabízí intuitivní API pro bezproblémovou správu souborů PSD. V tomto tutoriálu si projdeme, jak najít, upravit a uložit InfxResource v souboru PSD pomocí Aspose.PSD for Java. Ať už jste ostřílený vývojář nebo teprve začínáte, díky této příručce bude manipulace se zdroji PSD co nejjednodušší.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte vše, co potřebujete. Zde je rychlý kontrolní seznam:

1.  Java Development Kit (JDK): Ujistěte se, že je na vašem počítači nainstalována nejnovější verze JDK. Můžete si jej stáhnout z[Web společnosti Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
  
2.  Aspose.PSD for Java Library: Stáhněte si nejnovější verzi Aspose.PSD pro Java z[odkaz ke stažení](https://releases.aspose.com/psd/java/) Pokud jste to ještě neudělali, můžete získat bezplatnou zkušební verzi nebo zakoupit licenci od[zde](https://purchase.aspose.com/).

3. Integrované vývojové prostředí (IDE): Jakékoli Java IDE jako IntelliJ IDEA, Eclipse nebo NetBeans tuto práci zvládne.

4. Základní znalost jazyka Java: Znalost programování v jazyce Java je nezbytná. Pokud s Javou začínáte, zvažte, zda si oprášit základy Java, než budete pokračovat.

5. Ukázkový soubor PSD: Spolu s výukovým programem je nutné následovat ukázkový soubor PSD s InfxResource. Můžete použít svůj vlastní soubor nebo si stáhnout ukázkový soubor.

## Importujte balíčky

Chcete-li začít s Aspose.PSD for Java, prvním krokem je importovat potřebné balíčky do vašeho projektu Java. Tento krok je kritický, protože umožňuje vaší Java aplikaci používat funkce knihovny Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layerresources.InfxResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.LayerResource;
import com.aspose.psd.systemexceptions.ArgumentNullException;
```

Nyní si kód rozdělíme do snadno pochopitelných kroků.

## Krok 1: Nastavte zdrojové a cílové cesty

Nejprve musíte určit zdrojový adresář, kde se nachází váš soubor PSD, a cílový adresář, do kterého bude upravený soubor uložen.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFileName = sourceDir + "SampleForInfxResource.psd";
String destinationFileName = outputDir + "SampleForInfxResource_out.psd";
```

 Zde,`sourceDir` je cesta k adresáři, kde se nachází váš původní soubor PSD, a`outputDir` je místo, kam se uloží upravený soubor PSD. Nastavením těchto cest zajistíte, že vaše aplikace bude vědět, kde má najít a uložit soubory, se kterými potřebuje pracovat.

## Krok 2: Načtěte obrázek PSD

 Dále načtěte soubor PSD do a`PsdImage` objekt. Tento objekt vám umožní manipulovat s vrstvami a prostředky v souboru PSD.

```java
PsdImage im = null;
try {
    im = (PsdImage) Image.load(sourceFileName);
} catch (ArgumentNullException e) {
    System.out.println("File not found: " + e.getMessage());
}
```

 The`Image.load` metoda se zde používá k načtení souboru PSD. Pokud soubor není nalezen nebo je cesta nesprávná, an`ArgumentNullException` bude zachycen a zobrazí se příslušná zpráva.

## Krok 3: Iterujte přes vrstvy a prostředky

 Jakmile je soubor PSD načten, dalším krokem je procházet jeho vrstvami a najít konkrétní`InfxResource` hledáte.

```java
boolean isRequiredResourceFound = false;

for (Layer layer : im.getLayers()) {
    for (LayerResource layerResource : layer.getResources()) {
        if (layerResource instanceof InfxResource) {
            InfxResource resource = (InfxResource) layerResource;
            isRequiredResourceFound = true;
            
            // Ověřte a upravte zdroj
            if (!resource.getBlendInteriorElements()) {
                resource.setBlendInteriorElements(true);
                im.save(destinationFileName);
            }
            break;
        }
    }
}
```

 Zde procházíme každou vrstvu a její přidružené zdroje. Pokud`InfxResource`je nalezen, provádíme kontroly nebo úpravy. Konkrétně kontrolujeme, zda`BlendInteriorElements` je nepravda, a pokud ano, nastavte ji na hodnotu true a uložte upravený soubor.

## Krok 4: Uložte a zlikvidujte obrázek

Po úpravě prostředku je nezbytné uložit změny a zlikvidovat objekt obrázku, aby se uvolnila paměť.

```java
finally {
    if (im != null) im.dispose();
}
```

 The`finally` blok zajišťuje, že`PsdImage` objekt je správně zlikvidován, čímž se zabrání únikům paměti a zajistí, že vaše aplikace zůstane efektivní.

## Krok 5: Načtěte a ověřte upravený soubor PSD

Nyní, když jste uložili upravený soubor PSD, je posledním krokem jeho opětovné načtení a ověření, že změny byly použity správně.

```java
PsdImage im2 = null;
try {
    im2 = (PsdImage) Image.load(destinationFileName);
    for (Layer layer : im2.getLayers()) {
        for (LayerResource layerResource : layer.getResources()) {
            if (layerResource instanceof InfxResource) {
                InfxResource resource = (InfxResource) layerResource;
                Assert.isTrue(resource.getBlendInteriorElements(), "The InfxResource.BlendInteriorElements should change to true");
                break;
            }
        }
    }
} finally {
    if (im2 != null) im2.dispose();
}
```

 Tento krok je zásadní pro zajištění toho, že úprava byla aplikována podle očekávání. Načtete upravený soubor a zkontrolujete`BlendInteriorElements` vlastnost, aby bylo zajištěno, že je nastavena na`true`.

## Závěr

 Gratuluji! Úspěšně jste se naučili, jak s ním manipulovat`InfxResource` souboru PSD pomocí Aspose.PSD for Java. Ať už pracujete na malém projektu nebo integrujete tuto funkci do větší aplikace, kroky popsané v tomto tutoriálu vám poslouží jako pevný základ. Síla Aspose.PSD for Java spočívá v jeho flexibilitě a snadném použití, což z něj činí nepostradatelný nástroj pro vývojáře pracující se soubory PSD. Takže pokračujte, prozkoumejte další funkce a uvidíte, čeho dalšího můžete dosáhnout s Aspose.PSD pro Javu!

## FAQ

### Mohu použít Aspose.PSD for Java k manipulaci s jinými prostředky v souboru PSD?

 Ano, Aspose.PSD for Java vám umožňuje manipulovat s různými prostředky a vlastnostmi v rámci souboru PSD, nejenom`InfxResource`.

###  Co se stane, když`InfxResource` is not found in the PSD file?

 Pokud`InfxResource` není nalezen, bude kód pokračovat ve vykonávání, ale zadané akce nebudou provedeny a lze zaprotokolovat zprávu pro účely ladění.

### Jak zpracuji velké soubory PSD s více vrstvami?

Manipulace s velkými soubory PSD s více vrstvami může vyžadovat více paměti a výpočetního výkonu. Ujistěte se, že je vaše prostředí optimalizováno, a zvažte vyřazení objektů, když již nejsou potřeba, abyste uvolnili prostředky.

### Je možné vrátit změny provedené v souboru PSD?

Jakmile jsou změny uloženy, jsou trvalé, pokud neuchováte zálohu původního souboru. Vždy pracujte na kopii souboru, pokud potřebujete zachovat originál beze změny.

### Mohu automatizovat úpravy více souborů PSD pomocí Aspose.PSD pro Java?

Ano, můžete vytvářet skripty pro dávkové zpracování více souborů PSD a aplikovat stejné úpravy na každý soubor.