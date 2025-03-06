---
title: Přidejte efekt vrstvy vnitřního stínu v PSD s Javou
linktitle: Přidejte efekt vrstvy vnitřního stínu v PSD s Javou
second_title: Aspose.PSD Java API
description: Naučte se, jak přidat efekt vnitřního stínu do souborů PSD pomocí Aspose.PSD for Java, pomocí tohoto podrobného návodu, včetně tipů a osvědčených postupů.
weight: 12
url: /cs/java/advanced-psd-layer-features-effects/add-inner-shadow-layer-effect-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidejte efekt vrstvy vnitřního stínu v PSD s Javou

## Zavedení
Jste připraveni ponořit se do světa programování grafického designu? Pokud jste někdy chtěli programově manipulovat se soubory PSD, jste na správném místě! Dnes se podíváme na to, jak přidat efekt vnitřní stínové vrstvy do PSD (Photoshop Document) pomocí Aspose.PSD pro Javu. Tato výkonná knihovna umožňuje vývojářům v Javě efektivně pracovat se soubory PSD a umožňuje řadu manipulací s obrázky, od jednoduchých úprav až po složité efekty.
## Předpoklady
Než se pustíme do kódování, pojďme vás nastavit. Zde je to, co musíte mít na svém místě:
1.  Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK. Je nezbytný pro kompilaci a spouštění kódu Java. Pokud jej ještě nemáte, můžete si jej stáhnout z[Web společnosti Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Knihovna Aspose.PSD: Budete potřebovat přístup ke knihovně Aspose.PSD. Můžete si jej snadno stáhnout z[Aspose vydání](https://releases.aspose.com/psd/java/). Je to robustní nástroj pro práci se soubory PSD, takže si nezapomeňte vzít nejnovější verzi.
3. Integrované vývojové prostředí (IDE): I když můžete použít jakýkoli textový editor, doporučuje se použít IDE jako IntelliJ IDEA, Eclipse nebo NetBeans. Poskytují užitečné funkce, jako je zvýraznění syntaxe a nástroje pro ladění.
4. Základní znalosti jazyka Java: Znalost základů jazyka Java, jako jsou proměnné, třídy a metody, vám pomůže hladce pokračovat.
5. Ukázkový soubor PSD: Chcete-li kód otestovat, ujistěte se, že máte ukázkový soubor PSD. Můžete si jej vytvořit v aplikaci Adobe Photoshop nebo si zdarma stáhnout ukázku online.
## Importujte balíčky
Jakmile máte vše nastaveno a připraveno k použití, prvním krokem je importovat potřebné balíčky do vaší třídy Java. To je klíčové pro přístup k funkcím Aspose.PSD. 
## Importujte požadované balíčky
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layereffects.IShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```
těchto řádcích přinášíme třídy, které potřebujeme, z knihovny Aspose.
Nyní, když máme naše balíčky naimportované a naše prostředí nastaveno, pojďme se vrhnout na hrubší kód. Rozdělím to na zvládnutelné kroky.
## Krok 1: Definujte adresáře
V tomto kroku upřesníme, kde se nachází náš zdrojový soubor PSD a kam chceme upravenou verzi uložit. 
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String destName = outputDir + "sample_out.psd";
```
 Nahradit`"Your Source Directory"` a`"Your Document Directory"` se skutečnými cestami ve vašem počítači. Zde sdělíte svému programu, kde má hledat soubor PSD a kam uložit novou verzi.
## Krok 2: Načtěte soubor PSD
 Dále musíme načíst existující soubor PSD do a`PsdImage` objekt. Nakonfigurujeme také možnosti načítání tak, aby zahrnovaly efekty.
```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage image = (PsdImage) Image.load(sourceFile, loadOptions);
```
 Zde vytváříme instanci`PsdLoadOptions` , nastavením pro načtení zdrojů efektů a poté načtením našeho ukázkového souboru PSD do objektu s názvem`image`. Je to jako otevřít knihu před čtením!
## Krok 3: Otevřete vrstvu pro efekt
Nyní se dostaneme k poslední vrstvě v našem souboru PSD (za předpokladu, že to je ta, na kterou chceme aplikovat náš efekt).
```java
try {
    Layer layer = image.getLayers()[image.getLayers().length - 1];
```
Tento řádek přistupuje k poslední vrstvě našeho obrázku PSD. Ve Photoshopu jsou vrstvy jako průhledné listy naskládané na sobě a ta nejvyšší je často to, co vidíte jako první.
## Krok 4: Nakonfigurujte efekt vnitřního stínu
Tento fragment kódu použije efekt vnitřního stínu na naši vrstvu. 
```java
    IShadowEffect shadowEffect = (IShadowEffect) layer.getBlendingOptions().getEffects()[0];
    shadowEffect.setColor(Color.getGreen());
    shadowEffect.setOpacity((byte) 128);
    shadowEffect.setDistance(1);
    shadowEffect.setUseGlobalLight(false);
    shadowEffect.setSize(2);
    shadowEffect.setAngle(45);
    shadowEffect.setSpread(50);
    shadowEffect.setNoise(5);
```
Tady se děje kouzlo! Tento kód přebírá efekt stínu z možností prolnutí vrstvy a upravuje jeho vlastnosti:
- Barva: Nastaví stín na zelenou.
- Neprůhlednost: Dělá to poloprůhledné.
- Vzdálenost: Mírně posune stín od okraje vrstvy.
- Velikost: Určuje, jak velký je stín.
- Úhel: Určuje směr zdroje světla.
- Spread and Noise: Otevřete kreativní možnosti pro to, jak stín vypadá.
## Krok 5: Uložte upravené PSD
Jakmile jsou všechna nastavení použita, dalším krokem je uložení našeho upraveného souboru PSD.
```java
    image.save(destName, new PsdOptions(image));
```
Tento řádek uloží naše změny. Výstupní soubor je pojmenován`sample_out.psd`a zahrnuje všechny efekty, které byly právě aplikovány. Je to jako kliknout na „Uložit“ ve Photoshopu po provedení úprav.
## Krok 6: Vyčistěte zdroje
Nakonec se ujistíme, že jsme uvolnili veškeré zdroje, které jsme použili.
```java
} finally {
    image.dispose();
}
```
 Toto je dobrý postup, jak zabránit úniku paměti. Likvidací`image` objekt, zajišťujeme, aby naše aplikace běžela hladce a efektivně.
## Závěr
A tady to máte! V několika jednoduchých krocích jste se naučili, jak přidat efekt vnitřního stínu do vrstev v souboru PSD pomocí Aspose.PSD for Java. Tato knihovna nabízí fantastické možnosti pro každého, kdo chce automatizovat úlohy grafického designu nebo integrovat funkce pro manipulaci s obrázky do svých aplikací Java. 

## FAQ
### Co je Aspose.PSD?  
Aspose.PSD je knihovna Java pro práci se soubory PSD, která umožňuje vývojářům programově manipulovat s efekty vrstev, maskami a vlastnostmi obrázků.
### Potřebuji Photoshop, abych mohl používat Aspose.PSD?  
Ne, k použití Aspose.PSD nepotřebujete Photoshop. Knihovna funguje nezávisle pro manipulaci se soubory PSD.
### Mohu použít více efektů na stejnou vrstvu?  
Absolutně! Můžete použít více efektů přístupem ke každému typu efektu podobně, jako jsme přistupovali k efektu vnitřního stínu.
### Je Aspose.PSD zdarma?  
Aspose.PSD je komerční produkt; můžete však využít bezplatnou zkušební verzi dostupnou prostřednictvím Aspose.
### Kde najdu další dokumentaci?  
 Můžete najít komplexní dokumentaci k Aspose.PSD[zde](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
