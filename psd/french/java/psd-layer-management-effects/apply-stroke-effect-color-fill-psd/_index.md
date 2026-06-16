---
date: 2026-04-03
description: Apprenez comment enregistrer un PSD au format PNG avec un effet de contour
  et un remplissage de couleur en utilisant Aspose.PSD pour Java. Ce guide étape par
  étape montre comment exporter rapidement un PSD en PNG.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: Enregistrer le PSD en PNG avec effet de contour – Java
second_title: Aspose.PSD Java API
title: Enregistrer le PSD en PNG avec effet de contour – Java
url: /fr/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer le PSD en PNG avec effet de contour et remplissage de couleur – Java

## Introduction

Dans ce guide, vous apprendrez comment **enregistrer le PSD en PNG** tout en appliquant un effet de contour avec un remplissage de couleur à l'aide d'Aspose.PSD pour Java. Que vous soyez un développeur chevronné ou que vous débutiez, ce tutoriel pas à pas facilitera la tâche. Nous couvrirons tout, de la configuration de votre environnement à l'exportation de l'image finale, afin que vous puissiez rapidement **exporter le PSD en PNG** dans vos propres projets.

## Réponses rapides
- **Quel est l'objectif de ce tutoriel ?** Il montre comment enregistrer un fichier PSD en PNG après avoir appliqué un effet de contour personnalisable.  
- **Quelle bibliothèque est utilisée ?** Aspose.PSD for Java.  
- **Ai-je besoin d'une licence ?** Un essai gratuit fonctionne pour les tests ; une licence est requise pour la production.  
- **Puis-je changer la couleur du contour ?** Oui – vous pouvez définir n'importe quelle couleur via le `ColorFillSettings`.  
- **Le traitement par lots est-il possible ?** Absolument – encapsulez le code dans une boucle pour traiter plusieurs fichiers PSD.

## Qu’est‑ce que « enregistrer le PSD en PNG » ?

Enregistrer un PSD en PNG signifie convertir le fichier natif à calques de Photoshop en un format d'image plat, adapté au web, tout en préservant la fidélité visuelle. Cela est utile lorsque vous devez afficher du contenu PSD sur des sites web, des applications mobiles ou toute plateforme qui ne prend pas directement en charge les fichiers PSD.

## Pourquoi appliquer un effet de contour avec remplissage de couleur ?

Un contour ajoute une bordure nette autour du contenu des calques, faisant ressortir les graphiques sur des arrière‑plans complexes. Le combiner avec une couleur de remplissage personnalisée vous permet de marquer les images, de mettre en évidence des éléments d'interface, ou de créer des vignettes accrocheuses sans quitter Photoshop.

## Prérequis

1. **Java Development Kit (JDK) 8+** – assurez‑vous que `java` est dans votre PATH.  
2. **Aspose.PSD for Java** – téléchargez depuis le [site web](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, ou tout éditeur de votre choix.  
4. **Sample PSD** – un fichier contenant déjà un effet de contour (ou ajoutez‑en un dans Photoshop).  
5. **Basic Java knowledge** – vous écrirez quelques lignes de code, mais rien de complexe.

Une fois que vous avez tout cela, nous pouvons commencer à coder.

## Importer les packages

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Ces importations incluent toutes les classes nécessaires pour charger un PSD, modifier son contour et enregistrer les sorties PSD et PNG.

## Comment enregistrer le PSD en PNG avec effet de contour

### Étape 1 : Charger le fichier PSD

Tout d'abord, indiquez le dossier contenant votre PSD source.

```java
String dataDir = "Your Document Directory";
```

Remplacez `"Your Document Directory"` par le chemin réel sur votre machine.

Chargez maintenant le fichier tout en préservant les ressources d'effets existantes :

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Étape 2 : Définir la couleur du contour (et éventuellement personnaliser la largeur)

La boucle ci‑dessous parcourt chaque calque, récupère le premier `StrokeEffect` et modifie sa couleur de remplissage. Vous pouvez également ajuster `setWidth` ou `setPosition` sur l'objet `StrokeEffect` si vous devez **personnaliser la largeur du contour**.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **Astuce :** `Color.getDeepPink()` n'est qu'un exemple. Utilisez `new Color(r, g, b)` pour des valeurs RGB personnalisées.

### Étape 3 : Enregistrer le PSD modifié (optionnel)

Si vous souhaitez conserver une version PSD avec le contour mis à jour, enregistrez‑la ainsi :

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### Étape 4 : Exporter l'image en PNG (l'étape principale « enregistrer le PSD en PNG »)

Enfin, convertissez le PSD modifié en fichier PNG prêt pour le web :

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

Le PNG conserve le contour rose vif que vous avez défini précédemment, et l'option `TruecolorWithAlpha` garantit que la transparence est préservée.

## Problèmes courants et solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| **`ArrayIndexOutOfBoundsException`** | Le calque n’a aucun effet ou le premier effet n’est pas un `StrokeEffect`. | Vérifiez que le calque contient réellement un contour ou parcourez `getEffects()` pour trouver le bon type. |
| **Couleur ne change pas** | Vous pourriez modifier une copie des paramètres au lieu de l’original. | Assurez‑vous de caster directement en `ColorFillSettings` depuis `effect.getFillSettings()`. |
| **Le PNG apparaît vide** | Le PSD a été chargé sans rasteriser le calque. | Appelez `im.save(..., new PngOptions())` après toutes les modifications ; évitez d’enregistrer le `im` original avant les changements. |

## Questions fréquemment posées

**Q : Puis‑je appliquer plusieurs effets à un même calque avec Aspose.PSD pour Java ?**  
A : Oui, vous pouvez accéder aux options de fusion du calque et ajouter autant d’effets que nécessaire, y compris les ombres, les lueurs et les contours.

**Q : Est‑il possible d’automatiser le processus pour un lot de fichiers PSD ?**  
A : Absolument. Encapsulez la logique de chargement, d’application des effets et d’enregistrement dans une boucle `for‑each` qui parcourt les fichiers d’un répertoire.

**Q : Comment puis‑je annuler les modifications apportées à un fichier PSD ?**  
A : Rechargez le fichier original avant d’enregistrer des modifications ; Aspose.PSD ne fournit pas de pile d’annulation.

**Q : Puis‑je personnaliser la largeur et la position du contour ?**  
A : Oui. Utilisez `effect.setWidth(float)` et `effect.setPosition(StrokeEffect.Position)` pour contrôler l’épaisseur et le placement (à l’intérieur, à l’extérieur ou centré).

**Q : La bibliothèque Aspose.PSD pour Java est‑elle gratuite à utiliser ?**  
A : Un essai gratuit est disponible pour l’évaluation. La pleine fonctionnalité nécessite une licence achetée. Consultez les [options d’achat](https://purchase.aspose.com/buy) pour plus de détails.

---

**Dernière mise à jour :** 2026-04-03  
**Testé avec :** Aspose.PSD 24.12 for Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}