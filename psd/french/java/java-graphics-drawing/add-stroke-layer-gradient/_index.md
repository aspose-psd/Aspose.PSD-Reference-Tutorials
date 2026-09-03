---
date: 2026-09-03
description: Apprenez à créer gradient stroke java et à personnaliser les dégradés
  de traits dans les fichiers PSD en utilisant Aspose.PSD for Java. Guide étape par
  étape pour les développeurs.
keywords:
- create gradient stroke java
- add gradient stroke psd
- Aspose.PSD Java
- PSD gradient stroke
lastmod: 2026-09-03
linktitle: Comment créer une couche Gradient Stroke en Java
og_description: Créez gradient stroke java avec Aspose.PSD for Java en quelques minutes.
  Ce tutoriel vous montre comment ajouter et personnaliser les gradient strokes dans
  les fichiers PSD, avec des extraits de code et les meilleures pratiques.
og_image_alt: Screenshot of a PSD file showing a gradient stroke applied via Aspose.PSD
  Java API
og_title: Créer gradient stroke java – Guide de tutoriel Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  headline: Create gradient stroke java – Aspose.PSD tutorial guide
  type: TechArticle
- description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  name: Create gradient stroke java – Aspose.PSD tutorial guide
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
    text: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a pure‑Java library that lets developers create,
      edit, convert, and render Photoshop PSD files without requiring Adobe Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Yes, a valid license is required for production use. You can obtain a
      [temporary license](https://purchase.aspose.com/temporary-license/) for evaluation.
    question: Do I need a license to use Aspose.PSD for Java?
  - answer: Absolutely. Aspose.PSD provides APIs to build a new PSD document, add
      layers, apply effects, and save the file entirely programmatically.
    question: Can I create PSD files from scratch with this library?
  - answer: Yes, you can apply shadows, glows, bevels, and many other layer effects
      using the same effect‑based API.
    question: Is it possible to apply other effects besides gradient strokes?
  - answer: The official documentation is available in the [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full reference documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- gradient stroke
- Aspose.PSD
- Java graphics
title: Créer gradient stroke java – Guide de tutoriel Aspose.PSD
url: /fr/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment créer un contour dégradé java avec Aspose.PSD

## Introduction
Si vous avez besoin de **create gradient stroke java** effets sans ouvrir Photoshop, vous êtes au bon endroit. Dans ce tutoriel, vous apprendrez à utiliser Aspose.PSD for Java — une bibliothèque pure‑Java qui vous donne un contrôle programmatique complet sur les fichiers PSD. Nous parcourrons le chargement d’un PSD, l’accès à l’effet de contour d’un calque, la configuration d’un remplissage dégradé, puis l’enregistrement du résultat. À la fin, vous pourrez ajouter des contours dégradés de qualité professionnelle aux formes ou au texte en quelques lignes de code.

## Réponses rapides
- **Quel est l'objectif principal ?** Créer un calque de contour dégradé sur un fichier PSD en utilisant Java.  
- **Quelle bibliothèque fournit l'API ?** Aspose.PSD for Java (prend en charge Java 8 +).  
- **Ai‑je besoin d’une licence pour la production ?** Oui – une licence valide ou temporaire est requise.  
- **Combien de temps prend une implémentation de base ?** Environ 10‑15 minutes pour un simple contour.  
- **Puis‑je personnaliser le type de dégradé ?** Absolument – les dégradés linéaires, radiaux et basés sur l'angle sont tous pris en charge.

## Qu'est‑ce qu'un calque de contour dégradé ?
Un calque de contour dégradé est un contour vectoriel dont la couleur passe en douceur d’une teinte à une autre, voire plusieurs. Il peut être appliqué aux formes, au texte ou à tout masque vectoriel à l’intérieur d’un fichier PSD, offrant aux concepteurs un effet visuel dynamique sans rasteriser le dessin.

## Pourquoi utiliser Aspose.PSD pour Java ?
Aspose.PSD for Java offre **une prise en charge complète du PSD** pour plus de 100 fonctionnalités — y compris les calques, masques, calques de réglage et effets de calque — et peut traiter des fichiers jusqu’à 2 Go sans charger l’ensemble du document en mémoire. La bibliothèque fonctionne sur tout système d’exploitation supportant Java, ne possède aucune dépendance native, et est mise à jour chaque mois pour rester compatible avec les dernières spécifications des fichiers Photoshop.

## Prérequis
1. **Java Development Kit (JDK)** – Installez le dernier JDK depuis le [site d'Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java** – Téléchargez la bibliothèque depuis la [page de téléchargement d'Aspose.PSD](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ou NetBeans.  
4. **Licence** – Obtenez une [licence temporaire](https://purchase.aspose.com/temporary-license/) si vous ne possédez pas de licence commerciale complète.

## Importer les packages
Les instructions `import` importent les classes nécessaires dans le scope.  

```text
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
```

Maintenant, décomposons le processus en étapes claires.

## Étape 1 : Charger le fichier PSD
Charger le fichier source est la première étape ; vous devez activer les ressources d’effets afin que les informations de contour soient disponibles pour la modification. **PsdLoadOptions** configure la façon dont un fichier PSD est chargé, vous permettant d’activer ou de désactiver des ressources spécifiques.  

```text
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
```

## Étape 2 : Accéder à l'effet de contour
**StrokeEffect** représente le style de contour appliqué à un calque, incluant la largeur, la couleur et le remplissage dégradé.  

```text
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
```

## Étape 3 : Vérifier les propriétés de l'effet de contour
Avant de modifier quoi que ce soit, il est recommandé de lire les propriétés existantes. Cela vous aide à comprendre la configuration actuelle et à éviter d’écraser involontairement des paramètres importants. **GradientFillSettings** contient la configuration du remplissage dégradé pour un effet de contour.  

```text
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
```

## Étape 4 : Modifier les paramètres du remplissage dégradé
`GradientFill` définit comment les couleurs transitent le long du contour. Vous pouvez changer son type (linéaire, radial), son angle et son mode de fusion, puis attribuer de nouveaux points de couleur et de transparence.  

```text
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
```

## Étape 5 : Ajouter et modifier les points de couleur et de transparence
Un dégradé est construit à partir d’une série de points d’arrêt de couleur et d’opacité. **GradientColorPoint** définit un point d’arrêt de couleur dans un dégradé, en spécifiant sa couleur et sa position. **GradientTransparencyPoint** définit un point d’arrêt d’opacité dans un dégradé, en spécifiant son opacité et sa position. Ajouter ou ajuster ces points vous permet de façonner le flux visuel du contour.  

```text
```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
```

## Étape 6 : Enregistrer le fichier PSD modifié
Après tous les ajustements, écrivez le document mis à jour sur le disque. Aspose.PSD préserve automatiquement toutes les autres calques et ressources.  

```text
```java
im.save(exportPath);
```
```

## Étape 7 : Vérifier les modifications
Rechargez le fichier enregistré et vérifiez que les propriétés du dégradé du contour correspondent aux valeurs que vous avez définies. Cette étape de vérification est essentielle pour les pipelines automatisés. **Assert** fournit des assertions de test simples pour vérifier les conditions pendant l’exécution.  

```text
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(2411, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint1.getOpacity());
Assert.areEqual(4096, transparencyPoint1.getLocation());
```
```

## Pièges courants et conseils de dépannage
- **Erreur de licence manquante** – Si vous voyez une exception de licence, vérifiez que le fichier de licence temporaire est correctement chargé avant tout appel d’API.  
- **Dégradé non visible** – Assurez‑vous que le drapeau `strokeEnabled` du calque cible est réglé sur `true` ; sinon l’effet est ignoré lors du rendu.  
- **Performance sur les gros fichiers** – Pour les PSD de plus de 500 Mo, envisagez d’utiliser `PsdImage.load(..., LoadOptions)` avec `loadResources = false` et activez uniquement les ressources dont vous avez besoin.

## Questions fréquemment posées

**Q : Qu’est‑ce qu’Aspose.PSD pour Java ?**  
R : Aspose.PSD for Java est une bibliothèque pure‑Java qui permet aux développeurs de créer, modifier, convertir et rendre des fichiers Photoshop PSD sans nécessiter Adobe Photoshop.

**Q : Ai‑je besoin d’une licence pour utiliser Aspose.PSD pour Java ?**  
R : Oui, une licence valide est requise pour une utilisation en production. Vous pouvez obtenir une [licence temporaire](https://purchase.aspose.com/temporary-license/) pour l’évaluation.

**Q : Puis‑je créer des fichiers PSD à partir de zéro avec cette bibliothèque ?**  
R : Absolument. Aspose.PSD fournit des API pour construire un nouveau document PSD, ajouter des calques, appliquer des effets et enregistrer le fichier entièrement par programme.

**Q : Est‑il possible d’appliquer d’autres effets en plus des contours dégradés ?**  
R : Oui, vous pouvez appliquer des ombres, des lueurs, des biseaux et de nombreux autres effets de calque en utilisant la même API basée sur les effets.

**Q : Où puis‑je trouver la documentation de référence complète ?**  
R : La documentation officielle est disponible dans la [référence API Aspose.PSD Java](https://reference.aspose.com/psd/java/).

## Conclusion
Vous disposez maintenant d’une solution complète, de bout en bout, pour **create gradient stroke java** des effets dans les fichiers PSD en utilisant Aspose.PSD. En chargeant un PSD, en accédant à l’effet de contour, en configurant un remplissage dégradé et en enregistrant le fichier, vous pouvez automatiser des flux de travail graphiques sophistiqués qui nécessiteraient autrement un travail manuel dans Photoshop. Expérimentez différents types de dégradés, modes de fusion et points d’opacité pour obtenir exactement le rendu souhaité pour votre application.

---

**Last Updated:** 2026-09-03  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## Tutoriels associés

- [Create Gradient Fill PSD with Java using Aspose.PSD – Add Gradient Fill Layer](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [How to Create Radial Gradient Effects in Aspose.PSD for Java](/psd/java/advanced-image-effects/add-gradient-effects/)
- [How to Change Stroke Color Java Using Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}