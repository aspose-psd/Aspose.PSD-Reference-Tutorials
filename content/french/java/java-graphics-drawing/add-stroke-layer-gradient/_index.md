---
title: Comment ajouter un dégradé de calque de trait en Java
linktitle: Comment ajouter un dégradé de calque de trait en Java
second_title: API Java Aspose.PSD
description: Découvrez comment ajouter et personnaliser des dégradés de calques de traits dans des fichiers PSD à l'aide d'Aspose.PSD pour Java avec ce didacticiel complet étape par étape.
type: docs
weight: 10
url: /fr/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## Introduction
Vous êtes-vous déjà demandé comment ajouter un dégradé de calque de trait à vos images à l'aide de Java ? Eh bien, vous êtes au bon endroit ! Aujourd'hui, nous plongeons dans le monde d'Aspose.PSD pour Java, une bibliothèque puissante qui vous aide à manipuler facilement les fichiers PSD. Que vous soyez un débutant ou un développeur chevronné, ce guide étape par étape vous guidera tout au long du processus d'ajout d'un dégradé de calque de trait à vos fichiers PSD. Alors, attachez votre ceinture et préparez-vous à améliorer vos compétences en édition graphique !
## Conditions préalables
Avant de commencer, vous devez mettre en place quelques éléments. Assurez-vous d'avoir les éléments suivants :
1.  Kit de développement Java (JDK) : assurez-vous que JDK est installé sur votre système. Vous pouvez le télécharger depuis[Le site d'Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD pour la bibliothèque Java : vous pouvez le télécharger à partir du[Page de téléchargement Aspose.PSD](https://releases.aspose.com/psd/java/).
3. Un environnement de développement intégré (IDE) : n'importe quel IDE comme IntelliJ IDEA, Eclipse ou NetBeans fonctionnera.
4.  Un permis valide : vous pouvez obtenir un[permis temporaire](https://purchase.aspose.com/temporary-license/) si vous n'en avez pas un complet.
## Importer des packages
Tout d’abord, importons les packages nécessaires. Ceux-ci nous permettront d'utiliser les classes et méthodes nécessaires à la manipulation du fichier PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
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
Maintenant, décomposons l'exemple en plusieurs étapes pour une meilleure compréhension.
## Étape 1 : Chargez le fichier PSD
 Tout d’abord, nous devons charger le fichier PSD que nous souhaitons modifier. Nous utiliserons le`PsdLoadOptions` pour préciser que nous voulons charger les ressources des effets.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Étape 2 : accéder à l'effet de trait
Ensuite, nous devons accéder à l'effet de trait du calque qui nous intéresse. Ici, nous supposons qu'il s'agit du troisième calque (index 2) du fichier PSD.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Étape 3 : Vérifier les propriétés de l'effet de trait
Avant d'apporter des modifications, vérifions les propriétés de l'effet de trait pour nous assurer que nous modifions les paramètres corrects.
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
## Étape 4 : modifier les paramètres de remplissage dégradé
Il est maintenant temps de modifier les paramètres de remplissage dégradé en fonction de nos besoins. Nous modifierons la couleur, l'opacité, le mode de fusion et d'autres propriétés.
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
## Étape 5 : Ajouter et modifier des points de couleur et de transparence
Ajoutons de nouveaux points de couleur et de transparence et modifions ceux existants pour obtenir l'effet de dégradé souhaité.
```java
// Ajouter un nouveau point de couleur
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Changer l'emplacement du point précédent
fillSettings.getColorPoints()[1].setLocation(1899);
// Ajouter un nouveau point de transparence
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Changer l'emplacement du point de transparence précédent
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Étape 6 : Enregistrez le fichier PSD modifié
Après avoir apporté toutes les modifications nécessaires, nous devons enregistrer le fichier PSD.
```java
im.save(exportPath);
```
## Étape 7 : Vérifiez les modifications
Enfin, chargeons le fichier PSD enregistré et vérifions que nos modifications ont été correctement appliquées.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Vérifier les points de couleur
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
// Vérifier les points de transparence
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
Et voila! Vous savez maintenant comment ajouter et manipuler des dégradés de calques de traits dans des fichiers PSD à l'aide d'Aspose.PSD pour Java. Ce didacticiel couvrait le chargement du fichier PSD, l'accès et la modification des effets de trait, ainsi que l'enregistrement des modifications. Grâce à ces compétences, vous pouvez créer des dégradés visuellement attrayants et personnaliser vos fichiers PSD en fonction de vos besoins.
## FAQ
### Qu’est-ce qu’Aspose.PSD pour Java ?
Aspose.PSD pour Java est une bibliothèque qui permet aux développeurs de travailler avec des fichiers PSD dans des applications Java, fournissant des fonctionnalités pour créer, manipuler et convertir des fichiers PSD.
### Ai-je besoin d’une licence pour utiliser Aspose.PSD pour Java ?
 Oui, vous avez besoin d'une licence valide pour utiliser Aspose.PSD pour Java. Vous pouvez obtenir un[permis temporaire](https://purchase.aspose.com/temporary-license/) à des fins d’évaluation.
### Puis-je utiliser Aspose.PSD pour Java pour créer des fichiers PSD à partir de zéro ?
Absolument! Aspose.PSD pour Java fournit des API complètes pour créer et manipuler des fichiers PSD par programme.
### Est-il possible d'appliquer d'autres effets en utilisant Aspose.PSD pour Java ?
Oui, vous pouvez appliquer divers effets comme l'ombre, la lueur, etc. à l'aide d'Aspose.PSD pour Java.
### Où puis-je trouver la documentation d’Aspose.PSD pour Java ?
 Vous pouvez trouver la documentation[ici](https://reference.aspose.com/psd/java/).