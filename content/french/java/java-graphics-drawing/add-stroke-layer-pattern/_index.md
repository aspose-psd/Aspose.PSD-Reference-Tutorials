---
title: Comment ajouter un motif de calque de trait en Java
linktitle: Comment ajouter un motif de calque de trait en Java
second_title: API Java Aspose.PSD
description: Découvrez comment ajouter un motif de calque de trait aux fichiers PSD à l'aide d'Aspose.PSD pour Java. Suivez ce guide étape par étape pour améliorer facilement vos images.
type: docs
weight: 11
url: /fr/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## Introduction
Ajouter un motif de calque de trait à une image en Java peut sembler une tâche ardue, mais avec Aspose.PSD pour Java, c'est plus facile que vous ne le pensez. Que vous conceviez des graphiques ou travailliez sur des applications de retouche photo, ce guide vous guidera pas à pas tout au long du processus. Prêt à commencer? Allons-y !
## Conditions préalables
Avant de commencer, vous aurez besoin de quelques éléments :
- Kit de développement Java (JDK) : assurez-vous que JDK est installé sur votre système.
-  Aspose.PSD pour Java : téléchargez la bibliothèque depuis[ici](https://releases.aspose.com/psd/java/) et incluez-le dans votre projet.
- Un IDE : utilisez votre environnement de développement intégré (IDE) préféré comme IntelliJ IDEA ou Eclipse.
## Importer des packages
Tout d’abord, vous devez importer les packages nécessaires dans votre projet Java. Ces packages sont essentiels pour travailler avec Aspose.PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## Étape 1 : Chargez le fichier PSD
La première étape pour ajouter un motif de calque de trait consiste à charger le fichier PSD que vous souhaitez modifier.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
En chargeant le fichier PSD, vous pouvez désormais accéder et manipuler ses calques et effets.
## Étape 2 : préparer de nouvelles données de modèle
Ensuite, vous devez préparer les nouvelles données de motif que vous appliquerez au calque de trait.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
Ces données de motif seront utilisées pour créer le nouvel effet de trait.
## Étape 3 : accéder à l'effet de trait
Pour modifier l'effet de trait, vous devez accéder au calque spécifique et à ses options de fusion.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Cela garantit que vous travaillez avec le bon calque et le bon effet.
## Étape 4 : modifier l'effet de trait
Modifions maintenant l'effet de trait avec les nouvelles données du motif.
### Mettre à jour les propriétés de l'effet de trait
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Mettre à jour la ressource de modèle
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
Cet extrait de code met à jour la ressource de modèle avec les nouvelles données de modèle.
## Étape 5 : Appliquer le nouveau modèle
Enfin, appliquez le nouveau motif à l'effet de trait et enregistrez les modifications.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Cela garantit que le nouveau modèle est appliqué correctement et que le fichier est enregistré avec les modifications.
## Étape 6 : Vérifiez les modifications
Pour vous assurer que tout a fonctionné correctement, chargez à nouveau le fichier et vérifiez les modifications.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
Cette étape vérifie que les données du motif ont été correctement appliquées à l'effet de trait.
## Conclusion
Et voila! Vous avez ajouté avec succès un motif de calque de trait à un fichier PSD à l'aide d'Aspose.PSD pour Java. En suivant ces étapes, vous pouvez facilement personnaliser et améliorer vos images. Bon codage !
## FAQ
### Qu’est-ce qu’Aspose.PSD pour Java ?
Aspose.PSD pour Java est une bibliothèque qui permet aux développeurs de créer, modifier et convertir des fichiers PSD (Photoshop Document) par programme.
### Puis-je utiliser Aspose.PSD pour Java dans un projet commercial ?
 Oui, vous pouvez l'utiliser dans des projets commerciaux. Vous pouvez acheter une licence auprès de[ici](https://purchase.aspose.com/buy).
### Existe-t-il un essai gratuit disponible pour Aspose.PSD pour Java ?
 Oui, vous pouvez télécharger une version d'essai gratuite à partir de[ici](https://releases.aspose.com/).
### Comment puis-je obtenir de l'assistance pour Aspose.PSD pour Java ?
 Vous pouvez obtenir de l'aide sur les forums de la communauté Aspose[ici](https://forum.aspose.com/c/psd/34).
### Quelle est la configuration système requise pour Aspose.PSD pour Java ?
Vous avez besoin d'installer JDK et d'un IDE pour le développement. La bibliothèque prend en charge plusieurs systèmes d'exploitation, notamment Windows, Linux et macOS.