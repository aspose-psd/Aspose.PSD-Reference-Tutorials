---
date: 2026-11-04
description: Apprenez comment enregistrer un PSD au format PNG, exporter le PNG avec
  canal alpha et ajouter un calque d'ombre portée à l'aide d'Aspose.PSD for Java –
  un guide complet, étape par étape.
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- java image manipulation
lastmod: 2026-11-04
linktitle: Appliquer une ombre portée de rendu
og_description: Enregistrez un PSD en PNG avec Aspose.PSD for Java, exportez le PNG
  avec transparence alpha et ajoutez une ombre portée de rendu – guide étape par étape
  pour les développeurs Java.
og_image_alt: Developer guide showing how to convert PSD to PNG and apply drop shadow
  using Aspose.PSD Java
og_title: Enregistrez le PSD en PNG et appliquez une ombre portée de rendu avec Aspose.PSD
  for Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  headline: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  name: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  steps:
  - name: define document directory
    text: Define the directory path where your PSD files are stored.
  - name: set psd and png file paths
    text: Specify the full file paths for the source PSD and the target PNG.
  - name: load psd file with effects
    text: '`PsdImage` loads the PSD and gives access to its layers and effects.'
  - name: access drop shadow effect
    text: '`DropShadowEffect` represents a drop‑shadow layer effect that can be read
      or modified.'
  - name: validate shadow effect properties
    text: '`shadowEffect` holds the properties of the drop‑shadow such as opacity,
      distance, and size. > **Pro tip:** Adjust `setSpread()` or `setNoise()` to create
      softer or more textured shadows.'
  - name: save as png – the “save psd as png” step
    text: '`PngOptions` configures PNG export settings, including color type and alpha
      channel handling. At this point you have successfully **converted psd to png**,
      **exported png with alpha**, and applied a rendering drop shadow in a single
      workflow.'
  type: HowTo
- questions:
  - answer: Yes. Loop through `im.getLayers()` and add or modify a `DropShadowEffect`
      for each target layer, which also lets you perform a batch psd to png conversion.
    question: Can I apply drop shadows to multiple layers simultaneously?
  - answer: '`Spread` determines how abruptly the shadow transitions from full opacity
      to transparent. A higher value creates a harder edge.'
    question: What does the ‘Spread’ parameter control?
  - answer: Aspose.PSD supports PSD files from Photoshop 3.0 up to the latest release,
      handling most layer types and effects.
    question: Is Aspose.PSD compatible with all Photoshop versions?
  - answer: Download the free trial from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/)
      and run the sample without a license key.
    question: How can I test the code before purchasing a license?
  - answer: Post your question on the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      where the community and Aspose engineers can assist.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- save psd as png
- aspose psd java
- java image manipulation
- png transparency
- rendering drop shadow
title: Enregistrez le PSD en PNG et appliquez une ombre portée de rendu avec Aspose.PSD
  for Java
url: /fr/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer le PSD en PNG et appliquer une ombre portée lors du rendu avec Aspose.PSD pour Java

## Introduction

Si vous travaillez avec des fichiers Photoshop en Java, **saving psd as png** est l’une des tâches les plus courantes que vous rencontrerez. Dans de nombreux projets, vous devrez **save psd as png** pour livrer des ressources sur le web ou les applications mobiles, tout en préservant la transparence et les effets visuels. Avec Aspose.PSD, vous pouvez non seulement **convert psd to png** mais aussi améliorer l’image en **adding a drop shadow layer**. Dans ce tutoriel, nous parcourrons l’ensemble du processus — chargement d’un PSD, application d’une ombre portée lors du rendu, et enfin **saving the PSD as a PNG** — afin que vous puissiez intégrer ce flux de travail dans vos propres projets en toute confiance.

## Réponses rapides
- **Quelle bibliothèque gère la conversion PSD en PNG ?** Aspose.PSD for Java.  
- **Combien de temps prend l’implémentation de l’ombre portée ?** Environ 10‑15 minutes pour un exemple de base.  
- **Ai-je besoin d’une licence pour exécuter le code ?** Un essai gratuit suffit pour l’évaluation ; une licence est requise pour la production.  
- **Puis‑je appliquer l’ombre à plusieurs calques ?** Oui — il suffit de parcourir les calques souhaités, ce qui permet également d’effectuer une conversion **batch psd to png**.  
- **Quelle version de Java est requise ?** Java 8 ou supérieure.

## Qu’est‑ce que « save psd as png » et pourquoi est‑ce important ?

**Saving a PSD as PNG creates a widely‑supported, lossless image that retains transparency.** Ce format est essentiel lorsque vous devez afficher des ressources Photoshop sur le web, dans des applications mobiles, ou dans le cadre d’un pipeline de traitement d’images plus large. Ajouter une ombre portée en même temps vous permet de produire un effet visuel soigné sans ouvrir Photoshop.

## Pourquoi utiliser Aspose.PSD pour ce flux de travail ?

Le rendu des effets de calque au moment du chargement est intégré, vous n’avez donc pas besoin de Photoshop. Aspose.PSD prend en charge plus de 50 formats d’entrée et de sortie (PSD, PNG, JPEG, TIFF, BMP) et peut traiter de gros documents sans charger le fichier complet en mémoire. Il préserve les effets tels que les ombres portées et les lueurs exactement comme ils apparaissent, et exporte automatiquement le PNG avec transparence alpha.

## Prérequis

- **Environnement de développement Java** – JDK 8 ou plus récent installé.  
- **Aspose.PSD for Java** – Téléchargez le JAR le plus récent depuis la [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
- **Un fichier PSD** – Le fichier doit contenir au moins un calque que vous souhaitez améliorer avec une ombre portée (par ex., *Shadow.psd*).  

## Importer les packages

L’espace de noms `com.aspose.psd` fournit les classes principales pour charger des images, manipuler des calques et exporter des fichiers PNG. `PsdImage` est la classe principale utilisée pour charger et manipuler les fichiers PSD.  

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## Guide étape par étape

### Étape 1 : définir le répertoire des documents
Définissez le chemin du répertoire où vos fichiers PSD sont stockés.  

```java
String dataDir = "Your Document Directory";
```

### Étape 2 : définir les chemins des fichiers PSD et PNG
Spécifiez les chemins complets des fichiers source PSD et cible PNG.  

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Étape 3 : charger le fichier PSD avec les effets
`PsdImage` charge le PSD et donne accès à ses calques et effets.  

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Étape 4 : accéder à l’effet d’ombre portée
`DropShadowEffect` représente un effet de calque d’ombre portée qui peut être lu ou modifié.  

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Étape 5 : valider les propriétés de l’effet d’ombre
`shadowEffect` contient les propriétés de l’ombre portée telles que l’opacité, la distance et la taille.  

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **Astuce :** Ajustez `setSpread()` ou `setNoise()` pour créer des ombres plus douces ou plus texturées.

### Étape 6 : enregistrer en PNG – l’étape « save psd as png »
`PngOptions` configure les paramètres d’exportation PNG, y compris le type de couleur et la gestion du canal alpha.  

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

À ce stade, vous avez réussi à **convert psd to png**, **exported png with alpha**, et appliqué une ombre portée lors du rendu dans un seul flux de travail.

## Exporter le PNG avec transparence alpha

Lorsque vous avez besoin que la sortie PNG conserve son arrière‑plan transparent — notamment pour les superpositions d’interface ou les graphiques web — assurez‑vous d’utiliser `PngColorType.TruecolorWithAlpha` comme indiqué à l’étape d’enregistrement ci‑dessus. Cela garantit que l’ombre portée repose sur un canevas transparent plutôt que sur un fond uni, vous aidant à **preserve png transparency**.

## Ajouter une couche d’ombre portée avec Java

Si votre PSD contient plusieurs calques nécessitant des ombres, répétez simplement **Step 4** et **Step 5** à l’intérieur d’une boucle qui itère sur `im.getLayers()`. Chaque itération peut créer ou modifier une instance `DropShadowEffect`, vous offrant un contrôle granulaire sur l’opacité, la distance, la taille et l’angle de chaque calque. Cette approche permet également une conversion **batch psd to png** où chaque fichier reçoit le même traitement d’ombre.

## Cas d’utilisation courants pour l’enregistrement du PSD en PNG

* **Web asset pipelines** – Convertir les PSD fournis par les designers en PNG prêts pour le web avec des ombres intégrées.  
* **Mobile app resources** – Générer des icônes PNG transparentes à la volée, évitant l’exportation manuelle.  
* **Batch processing** – Automatiser la conversion de centaines de fichiers PSD dans un job côté serveur, en veillant à ce que chaque PNG conserve son canal alpha et ses effets visuels.  

## Problèmes courants et solutions

| Problème | Cause probable | Solution |
|----------|----------------|----------|
| **Ombre non visible** | `Opacity` réglée à 0 ou le calque est masqué | Vérifiez que `shadowEffect.getOpacity()` > 0 et la visibilité du calque. |
| **Le PNG apparaît plat (pas de transparence)** | `PngColorType` incorrect utilisé | Utilisez `PngColorType.TruecolorWithAlpha` comme indiqué. |
| **Exception lors du chargement** | Effets non chargés | Assurez‑vous que `loadOptions.setLoadEffectsResource(true)` est appelé. |
| **Index de calque incorrect** | La structure du PSD diffère | Inspectez `im.getLayers()` et choisissez le bon indice. |

## Questions fréquentes

**Q : Puis‑je appliquer des ombres portées à plusieurs calques simultanément ?**  
R : Oui. Parcourez `im.getLayers()` et ajoutez ou modifiez un `DropShadowEffect` pour chaque calque cible, ce qui vous permet également d’effectuer une conversion **batch psd to png**.

**Q : Que contrôle le paramètre ‘Spread’ ?**  
R : `Spread` détermine la rapidité avec laquelle l’ombre passe d’une opacité totale à la transparence. Une valeur plus élevée crée un bord plus dur.

**Q : Aspose.PSD est‑il compatible avec toutes les versions de Photoshop ?**  
R : Aspose.PSD prend en charge les fichiers PSD de Photoshop 3.0 jusqu’à la dernière version, en gérant la plupart des types de calques et des effets.

**Q : Comment puis‑je tester le code avant d’acheter une licence ?**  
R : Téléchargez l’essai gratuit depuis la [Aspose.PSD download page](https://releases.aspose.com/psd/java/) et exécutez l’exemple sans clé de licence.

**Q : Où puis‑je obtenir de l’aide en cas de problème ?**  
R : Publiez votre question sur le [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) où la communauté et les ingénieurs Aspose peuvent vous aider.

## Conclusion

Vous savez maintenant comment **save psd as png**, **export png with alpha**, **convert psd to png**, et **apply a drop shadow layer** avec Aspose.PSD for Java. Cette combinaison vous permet d’automatiser la préparation d’images de haute qualité pour le web, le mobile ou les applications de bureau — sans jamais ouvrir Photoshop.

---

**Last Updated:** 2026-11-04  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose

## Tutoriels associés

- [Convertir le PSD en PNG avec superposition de couleur – Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)
- [Comment ajouter une ombre dans PSD avec Java – Effets de calque avancés](/psd/java/advanced-psd-layer-features-effects/)
- [Comment convertir le PSD en formats d’image raster avec Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}