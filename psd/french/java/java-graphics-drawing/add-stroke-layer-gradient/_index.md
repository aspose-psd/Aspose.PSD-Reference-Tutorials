---
date: 2026-01-14
description: Apprenez à créer un calque de contour dégradé et à personnaliser les
  dégradés de contour dans les fichiers PSD en utilisant Aspose.PSD pour Java grâce
  à ce tutoriel étape par étape.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: Comment créer une couche de trait dégradé en Java
url: /fr/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment créer un calque de contour dégradé en Java

## Introduction
Vous êtes-vous déjà demandé comment **créer un calque de contour dégradé** dans vos fichiers PSD en utilisant Java ? Vous êtes au bon endroit ! Aujourd’hui, nous allons explorer Aspose.PSD for Java — une bibliothèque puissante qui vous permet de manipuler les fichiers PSD sans effort. Que vous soyez novice en programmation graphique ou que vous souhaitiez peaufiner des conceptions existantes, ce guide vous accompagnera pas à pas pour ajouter et personnaliser des dégradés de contour.

## Quick Answers
- **Quel est l’objectif principal ?** Créer un calque de contour dégradé sur un fichier PSD.  
- **Quelle bibliothèque est requise ?** Aspose.PSD for Java.  
- **Ai‑je besoin d’une licence ?** Oui, une licence valide (ou temporaire) est nécessaire en production.  
- **Quelle version de Java fonctionne ?** Java 8 ou supérieure.  
- **Combien de temps prend l’implémentation ?** Environ 10‑15 minutes pour un contour dégradé de base.

## Qu’est‑ce qu’un calque de contour dégradé ?
Un calque de contour dégradé est un tracé vectoriel autour d’une forme ou d’un texte qui passe en douceur d’une couleur à une autre. Avec Aspose.PSD, vous pouvez définir programmétiquement les couleurs, l’opacité, l’angle et le type (linéaire, radial, etc.) du contour.

## Pourquoi utiliser Aspose.PSD for Java ?
- **Prise en charge complète du PSD** – lire, modifier et écrire des fichiers PSD sans Photoshop.  
- **API d’effets riche** – accéder aux effets de contour, d’ombre, de lueur et bien d’autres.  
- **Multiplateforme** – fonctionne sur tout système d’exploitation supportant Java.  
- **Aucune dépendance native** – pur Java, facile à intégrer dans les pipelines CI.

## Prérequis
1. **Java Development Kit (JDK)** – Installez le dernier JDK depuis le [site d’Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java** – Téléchargez la bibliothèque depuis la [page de téléchargement Aspose.PSD](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ou NetBeans.  
4. **Licence** – Obtenez une [licence temporaire](https://purchase.aspose.com/temporary-license/) si vous ne possédez pas de licence complète.

## Import Packages
Tout d’abord, importez les classes dont nous aurons besoin pour charger le PSD, accéder aux effets et configurer les remplissages dégradés.

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

Passons maintenant à la décomposition du processus en étapes claires.

## Step 1: Load the PSD File
Nous chargeons le PSD source et activons les ressources d’effets afin que l’effet de contour soit disponible.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Step 2: Access the Stroke Effect
En supposant que le contour que nous voulons modifier appartient à la troisième couche (index 2), nous récupérons son `StrokeEffect`.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## Step 3: Verify Stroke Effect Properties
Avant d’apporter des modifications, nous confirmons les paramètres existants afin de savoir exactement ce que nous mettons à jour.

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

## Step 4: Modify the Gradient Fill Settings
Ici, nous changeons la couleur, l’opacité, le mode de fusion et d’autres propriétés pour obtenir l’aspect souhaité.

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

## Step 5: Add and Modify Color and Transparency Points
Nous ajoutons de nouveaux points de couleur et de transparence, puis ajustons ceux existants pour façonner le dégradé.

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

## Step 6: Save the Modified PSD File
Après tous les ajustements, nous écrivons le fichier mis à jour sur le disque.

```java
im.save(exportPath);
```

## Step 7: Verify the Modifications
Chargez le fichier enregistré et vérifiez que chaque propriété reflète les changements appliqués.

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
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## Conclusion
Vous savez maintenant comment **créer des effets de calque de contour dégradé** dans les fichiers PSD en utilisant Aspose.PSD for Java. En chargeant un PSD, en accédant à l’effet de contour, en ajustant les paramètres de remplissage dégradé et en enregistrant le résultat, vous pouvez produire de façon programmatique des graphiques de qualité professionnelle sans jamais ouvrir Photoshop.

## FAQ's
### Qu’est‑ce qu’Aspose.PSD for Java ?
Aspose.PSD for Java est une bibliothèque qui permet aux développeurs de travailler avec des fichiers PSD dans des applications Java, offrant des fonctionnalités pour créer, manipuler et convertir des fichiers PSD.

### Ai‑je besoin d’une licence pour utiliser Aspose.PSD for Java ?
Oui, vous devez disposer d’une licence valide pour utiliser Aspose.PSD for Java. Vous pouvez obtenir une [licence temporaire](https://purchase.aspose.com/temporary-license/) à des fins d’évaluation.

### Puis‑je créer des fichiers PSD à partir de zéro avec Aspose.PSD for Java ?
Absolument ! Aspose.PSD for Java fournit des API complètes pour créer et manipuler des fichiers PSD de manière programmatique.

### Est‑il possible d’appliquer d’autres effets avec Aspose.PSD for Java ?
Oui, vous pouvez appliquer divers effets tels que l’ombre, la lueur et bien d’autres en utilisant Aspose.PSD for Java.

### Où puis‑je trouver la documentation d’Aspose.PSD for Java ?
Vous pouvez consulter la documentation [ici](https://reference.aspose.com/psd/java/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-01-14  
**Testé avec :** Aspose.PSD for Java 24.11  
**Auteur :** Aspose