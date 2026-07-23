---
date: 2026-03-04
description: Naučte se, jak v Javě vytvořit grafický objekt a přidat diagonální vodoznak
  do souborů PSD pomocí Aspose.PSD. Tento krok‑za‑krokem průvodce pokrývá použití
  knihovny pro vodoznaky v Javě.
linktitle: Add Diagonal Watermark to PSD Files with Java
second_title: Aspose.PSD Java API
title: Vytvoření grafického objektu v Javě – Diagonální vodoznak pro PSD
url: /cs/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidání šikmého vodoznaku do souborů PSD pomocí Javy

## Introduction
Dans le didacticiel Tomto **créer un objet graphique Java**, vous pouvez utiliser le PSD pour créer un objet graphique. Si vous êtes un designer ou un professionnel du marketing, vous serez en mesure de vous aider à devenir professionnel. Prouvez-moi que vous pouvez obtenir de bons résultats en prenant soin d'apprendre à appliquer la technologie et votre projet.

## Réponses rapides
- **Jakou knihovnu potřebuji?** Aspose.PSD pour Java (une bibliothèque robuste de filigranes d'images Java).
- **Jaké primární klíčové slovo tento tutoriál pokrývá?** créer un objet graphique Java.
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; pro produkční nasazení je vyžadována komerční licence.
- **Mohu změnit text a styl vodoznaku?** Ano – můžete přizpůsobit font, barvu, průhlednost a rotaci.
- **J'ai déjà formaté mon fichier ?** Vous pouvez utiliser un fichier PNG, mais Aspose.PSD peut exporter des fichiers PSD, JPEG, BMP.

## Qu'est-ce qu'un objet graphique en Java ?
Objet **Graphiques** představuje kreslicí plochu pro obrázek. Vous pouvez utiliser un graphique pour obtenir une méthode qui vous permet d'afficher du texte et de visualiser le bitmap sur le plan PSD. Tout ce que j'ai compris, c'est le concept principal de **créer un objet graphique Java**.

## Pourquoi utiliser Aspose.PSD pour le filigrane ?
Aspose.PSD est spécialisé dans la **bibliothèque de filigranes d'images Java**, compatible avec Adobe Photoshop. Vous pouvez contrôler et utiliser le texte pour transformer l'objet, car c'est une idée idéale pour l'exploitation côté serveur.

## Prérequis
Než se pustíme do kódu, ujistěte se, že máte následující :

### 1. Environnement de développement Java
Installez le JDK nejnovější sur [site Web Java](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### 2. Bibliothèque Aspose.PSD
Téléchargez la page [Page de téléchargements Aspose](https://releases.aspose.com/psd/java/). Přidejte JAR do projektu pomocí Maven, Gradle nebo ručního zahrnutí do classpath.

### 3. Compréhension de base de Java
Javy a commencé à utiliser Javy – il s'agit d'un objet d'entrée/sortie souborové qui peut suivre un didacticiel.

### 4. Configuration de l'EDI
Vous pouvez utiliser IntelliJ IDEA, Eclipse avec NetBeans pour un programme possible.

## Importer des packages
Pour manipuler le support PSD, vous pouvez importer Aspose.PSD :

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Nyní, když máme připravené předpoklady a potřebné balíčky importovány, projdeme kroky pro přidání šikmého vodoznaku do souboru PSD.

## Krok 1: Nastavení adresáře
```java
String dataDir = "Your Document Directory";
```
Nahraďte `"Your Document Directory"` cestou ke složce, která obsahuje váš zdrojový soubor PSD.

## Krok 2: Načtení souboru PSD
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
Metoda `Image.load` načte soubor a přetypuje jej na `PsdImage`, aby bylo možné pracovat s funkcemi specifickými pro PSD.

## Krok 3: Vytvoření grafického objektu
```java
Graphics graphics = new Graphics(psdImage);
```
Zde **create graphics object java**—plátno, na kterém nakreslíme vodoznak.

## Krok 4: Vytvoření písma pro vodoznak
```java
Font font = new Font("Arial", 20.0f);
```
Vyberte libovolný nainstalovaný font; velikost určuje, jak výrazný bude vodoznak.

## Krok 5: Vytvoření štětce pro vodoznak
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
Parametr `alpha` (první parametr) nastavuje průhlednost. Alfa = 50 dává jemný, poloprůhledný vzhled.

## Krok 6: Nastavení transformační matice
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
Otočíme kreslicí plochu o 45° kolem středu obrázku, čímž vytvoříme šikmý efekt.

## Krok 7: Definování zarovnání řetězce
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
Zarovnání na střed zajišťuje, že vodoznak bude pěkně uprostřed otočeného obdélníku.

## Krok 8: Nakreslení vodoznaku
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
Nahraďte `"Some watermark text"` názvem vaší značky nebo upozorněním na autorská práva. Obdélník určuje, kde bude text vykreslen.

## Krok 9: Uložení obrázku
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
Výstup je uložen jako PNG, ale můžete zvolit libovolný formát podporovaný Aspose.PSD.

## Cas d'utilisation courants
- **Ochrana značky :** Přidejte poloprůhledné logo, aby se zabránilo neoprávněnému použití.
- **Dávkové zpracování :** Automatizujte vodoznakování velkých knihoven obrázků na serveru.
- **Création náhledy :** Vous avez choisi un client de conception, přičemž originální soubory zůstávají nedotčeny.

## Dépannage et conseils
- **Průhlednost není vidět?** Zvyšte hodnotu alfa (např. `100`) pro silnější vodoznak.
- **Vodoznak je mimo střed?** Ověřte, že bod otáčení používá přesné dělení šířky/výšky obrázku.
- **Obavy o výkon :** Znovu použijte stejný objekt `Graphics` při zpracování více obrázků ve smyčce.

## FAQ
### Qu'est-ce qu'Aspose.PSD ?
Aspose.PSD est un outil Java pratique pour manipuler les fichiers PSD sans Adobe Photoshop.

### Puis-je utiliser d'autres polices pour le filigrane ?
Maintenant, vous devez utiliser la police de libération, vous avez besoin d'un système et d'un système pour votre sécurité.

### Existe-t-il un moyen de personnaliser la transparence du filigrane ?
Určite! Vous devez utiliser la note d'Alfa pour `SolidBrush`, au plus près de l'application.

### Puis-je ajouter plusieurs filigranes ?
Maintenant, vous pouvez utiliser la méthode `drawString` pour définir les paramètres de votre choix.

### Où puis-je trouver plus d'informations sur Aspose.PSD ?
Vous recevrez également des informations sur les documents [zde](https://reference.aspose.com/psd/java/).

---

**Dernière mise à jour :** 2026-03-04
**Testé avec :** Aspose.PSD 24.12 pour Java
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}