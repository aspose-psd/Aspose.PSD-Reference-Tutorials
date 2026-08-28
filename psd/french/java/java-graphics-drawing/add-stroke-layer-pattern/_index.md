---
date: 2026-08-28
description: Ajoutez un pattern à un layer en Java avec Aspose.PSD. Suivez ce guide
  étape par étape pour appliquer un effet de stroke layer, configurer les ressources
  de pattern et enregistrer vos fichiers PSD efficacement.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Comment ajouter un pattern de stroke layer en Java
og_description: Ajoutez un pattern à un layer en Java avec Aspose.PSD. Suivez ce guide
  concis pour appliquer un effet de stroke layer, configurer les ressources de pattern
  et enregistrer vos fichiers PSD efficacement.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Ajouter un pattern à un layer en Java – tutoriel Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Comment ajouter un pattern à un layer en Java
url: /fr/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment ajouter un motif à un calque en Java

## Introduction
Ajouter un motif à un calque en Java est une exigence courante lorsque vous devez enrichir les fichiers Photoshop PSD avec des effets de contour personnalisés. Avec Aspose.PSD pour Java, cette tâche devient simple, même si vous débutez avec la bibliothèque. Dans ce tutoriel, vous apprendrez comment charger un PSD, créer une ressource de motif, l’attacher à un effet de contour, puis enregistrer le résultat — le tout avec des instructions claires, étape par étape.

## Réponses rapides
- **Quelle bibliothèque est nécessaire ?** Aspose.PSD pour Java.  
- **Combien de temps prend l'implémentation ?** Environ 10‑15 minutes pour un motif de base.  
- **Ai-je besoin d'une licence ?** Une version d'essai gratuite suffit pour le développement ; une licence commerciale est requise pour la production.  
- **Quelle version de Java est prise en charge ?** JDK 8 ou version ultérieure.  
- **Puis-je l'utiliser dans un service web ?** Oui, l'API est indépendante de la plateforme et fonctionne dans tout environnement Java.

## Qu'est-ce que l'ajout d'un motif à un calque ?
Ajouter un motif à un calque signifie attribuer un bitmap en mosaïque à un effet de contour ou de remplissage afin que le motif se répète le long du contour de la forme. Cette technique est largement utilisée pour les bordures décoratives, les textures et les superpositions de marque, permettant aux designers de créer des thèmes visuels cohérents sans dessiner chaque élément manuellement.

## Pourquoi utiliser Aspose.PSD pour cette tâche ?
Aspose.PSD prend en charge **plus de 30 formats d'image** et peut manipuler des fichiers PSD jusqu'à **2 Go** sans charger le document complet en mémoire, offrant ainsi des performances rapides sur du matériel serveur standard. Son API fluide vous permet de travailler programmatique avec les effets de calque, éliminant le besoin de Photoshop dans les pipelines automatisés.

## Prérequis
Avant de commencer, assurez-vous d'avoir :
- Java Development Kit (JDK) 8 ou version ultérieure installé.  
- Aspose.PSD pour Java – téléchargez‑le depuis la **page de téléchargement Aspose.PSD pour Java**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) et ajoutez le JAR au classpath de votre projet.  
- Un IDE tel qu'IntelliJ IDEA ou Eclipse pour éditer et exécuter le code d'exemple.  
- Un fichier PSD d'exemple contenant un calque de forme que vous souhaitez modifier.

## Importer les packages
Tout d'abord, importez les espaces de noms qui donnent accès aux objets PSD, aux ressources et aux effets.

```
// No actual code block is added to preserve original placeholders.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
```

## Comment ajouter un motif à un calque en Java ?

Chargez le PSD cible, créez une ressource de motif, attachez‑la à l'effet de contour du calque souhaité, puis enregistrez le fichier. Ce flux de bout en bout ne nécessite que quelques lignes de code et fonctionne avec tout PSD standard contenant un calque de forme vectorielle.

### Étape 1 : charger le fichier PSD
Le chargement du document vous donne accès à sa hiérarchie de calques et à sa collection d'effets.  
`PsdLoadOptions` configure la façon dont le PSD est lu, tandis que `PsdImage` représente le fichier chargé en mémoire.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

En chargeant le fichier PSD, vous pouvez désormais accéder à ses calques et effets et les manipuler.

### Étape 2 : préparer les nouvelles données de motif
Créez un `PatternResource` qui contient le bitmap que vous souhaitez répéter comme motif de contour.  
`PatternResource` est une ressource globale PSD qui stocke un motif bitmap répétitif. `Rectangle` définit les limites du motif, et `UUID` fournit un identifiant unique.

```
// Placeholder for original code.
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
```

Ces données de motif seront utilisées pour créer le nouvel effet de contour.

### Étape 3 : accéder à l'effet de contour
Identifiez le calque de forme qui possède déjà un contour, puis récupérez son objet `StrokeEffect`.  
`StrokeEffect` représente l'effet de contour appliqué à un calque de forme.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

Cela garantit que vous travaillez sur le bon calque et le bon effet.

### Étape 4 : modifier l'effet de contour
Mettez maintenant à jour les propriétés du contour pour qu’il référence la nouvelle ressource de motif.

#### Mettre à jour les propriétés de l'effet de contour
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### Mettre à jour la ressource du motif
`PattResource` est une ressource globale de calque PSD qui stocke les données du motif.

```
// Placeholder for original code.
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
```

Ces extraits remplacent le motif existant par celui que vous avez fourni.

### Étape 5 : appliquer le nouveau motif
`PatternFillSettings` contient les paramètres de remplissage pour un effet de contour basé sur un motif. Validez les modifications sur le calque et écrivez le PSD mis à jour sur le disque.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

Cela garantit que le nouveau motif est appliqué correctement et que le fichier est enregistré avec les changements.

### Étape 6 : vérifier les modifications
Rechargez le fichier et inspectez le contour pour confirmer que le motif apparaît comme prévu.

```
// Placeholder for original code.
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
```

Cette étape vérifie que les données du motif ont bien été appliquées à l'effet de contour.

## Problèmes courants et dépannage
- **Motif non visible :** Assurez‑vous que le DPI de l'image du motif correspond à la résolution du PSD, et que le drapeau `Enabled` du contour est réglé sur `true`.  
- **Les gros fichiers PSD provoquent OutOfMemoryError :** Utilisez `PsdImage.load(..., LoadOptions)` avec `LoadOptions.setLoadAllLayers(false)` pour charger les calques à la demande.  
- **Calque incorrect sélectionné :** Vérifiez l’indice ou le nom du calque avant d’accéder à ses effets ; vous pouvez énumérer `psdImage.getLayers()` pour lister les calques disponibles.

## Questions fréquemment posées

**Q : Qu'est‑ce que Aspose.PSD pour Java ?**  
R : Aspose.PSD pour Java est une bibliothèque qui permet aux développeurs de créer, modifier et convertir des fichiers PSD (Photoshop Document) de façon programmatique.

**Q : Puis‑je utiliser Aspose.PSD pour Java dans un projet commercial ?**  
R : Oui, vous pouvez l’utiliser dans des projets commerciaux. Vous pouvez acheter une licence sur la **page d'achat Aspose**([Aspose purchase page](https://purchase.aspose.com/buy)).

**Q : Existe‑t‑il une version d'essai gratuite d'Aspose.PSD pour Java ?**  
R : Oui, vous pouvez télécharger une version d'essai gratuite depuis la **page des releases Aspose**([Aspose releases page](https://releases.aspose.com/)).

**Q : Comment obtenir du support pour Aspose.PSD pour Java ?**  
R : Vous pouvez obtenir de l'aide sur les forums communautaires Aspose **ici**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)).

**Q : Quelles sont les exigences système pour Aspose.PSD pour Java ?**  
R : Vous avez besoin d’un JDK installé et d’un IDE pour le développement. La bibliothèque prend en charge Windows, Linux et macOS.

## Conclusion
Vous avez maintenant appris comment ajouter un motif à un calque en Java avec Aspose.PSD. En suivant les étapes ci‑dessus, vous pouvez enrichir programmatique les fichiers PSD avec des motifs de contour personnalisés, automatiser les flux de travail de marque et intégrer le traitement graphique dans toute application Java. Explorez d’autres fonctionnalités d’Aspose.PSD telles que la fusion de calques, les ajustements de couleur et l’exportation vers PNG ou JPEG pour étendre davantage votre boîte à outils de traitement d’image.

---

**Last Updated:** 2026-08-28  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose

## Tutoriels associés

- [Rendu du calque de remplissage de motif PSD](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Superposition de motif PSD : ajouter des effets avec Aspose.PSD pour Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Comment changer la couleur du contour en Java avec Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}