---
date: 2025-12-05
description: Apprenez à enregistrer un PSD au format PNG, à convertir un PSD en PNG
  et à appliquer une ombre portée à l'aide d'Aspose.PSD pour Java – un guide complet,
  étape par étape.
language: fr
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Enregistrer le PSD au format PNG et appliquer l’ombre portée lors du rendu
  dans Aspose.PSD pour Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer un PSD en PNG et appliquer une ombre portée lors du rendu avec Aspose.PSD pour Java

## Introduction

Si vous travaillez avec des fichiers Photoshop en Java, **enregistrer un PSD en PNG** est l’une des tâches les plus courantes que vous rencontrerez. Avec Aspose.PSD, vous pouvez non seulement **convertir un PSD en PNG**, mais aussi améliorer l’image en **ajoutant un calque d’ombre portée**. Dans ce tutoriel, nous parcourrons l’ensemble du processus – charger un PSD, appliquer une ombre portée lors du rendu, et enfin **enregistrer le PSD en tant que fichier PNG** – afin que vous puissiez intégrer ce flux de travail dans vos propres projets en toute confiance.

## Réponses rapides
- **Quelle bibliothèque gère la conversion PSD en PNG ?** Aspose.PSD for Java.  
- **Combien de temps prend la mise en œuvre de l’ombre portée ?** Environ 10‑15 minutes pour un exemple de base.  
- **Ai-je besoin d’une licence pour exécuter le code ?** Un essai gratuit suffit pour l’évaluation ; une licence est requise pour la production.  
- **Puis‑je appliquer l’ombre à plusieurs calques ?** Oui – il suffit de parcourir les calques souhaités.  
- **Quelle version de Java est requise ?** Java 8 ou supérieure.

## Qu’est‑ce que « enregistrer PSD en PNG » et pourquoi est‑ce important ?

Enregistrer un PSD en PNG crée une image sans perte, largement prise en charge, qui conserve la transparence. Cela est essentiel lorsque vous devez afficher des ressources Photoshop sur le web, dans des applications mobiles, ou dans le cadre d’une chaîne de traitement d’images plus vaste. Ajouter une ombre portée en même temps vous permet de produire un effet visuel soigné sans ouvrir Photoshop.

## Prérequis

- **Environnement de développement Java** – JDK 8 ou plus récent installé.  
- **Aspose.PSD for Java** – Téléchargez le JAR le plus récent depuis la [page de téléchargement d’Aspose.PSD](https://releases.aspose.com/psd/java/).  
- **Un fichier PSD** – Le fichier doit contenir au moins un calque que vous souhaitez améliorer avec une ombre portée (par ex., *Shadow.psd*).  

## Importer les packages

Tout d’abord, importez les classes dont nous aurons besoin. Cela nous donne accès au chargement d’images, aux effets de calque et aux options d’exportation PNG.

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

### Étape 1 : Définir le répertoire du document  
Indiquez au programme où se trouve votre PSD source.

```java
String dataDir = "Your Document Directory";
```

### Étape 2 : Définir les chemins des fichiers PSD et PNG  
Spécifiez à la fois le PSD d’entrée et le PNG de sortie qui contiendra l’ombre portée rendue.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Étape 3 : Charger le fichier PSD avec les effets  
Activez le chargement des ressources d’effets afin que nous puissions manipuler l’effet d’ombre portée.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Étape 4 : Accéder à l’effet d’ombre portée  
Récupérez le premier effet d’ombre portée du deuxième calque (index 1). C’est ici que nous vérifierons ou modifierons les paramètres.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Étape 5 : Valider les propriétés de l’effet d’ombre  
Assurez‑vous que les propriétés de l’effet correspondent à ce que vous attendez avant d’enregistrer. Vous pouvez également ajuster ces valeurs pour obtenir un rendu différent.

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

> **Conseil pro :** Ajustez `setSpread()` ou `setNoise()` pour créer des ombres plus douces ou plus texturées.

### Étape 6 : Enregistrer en PNG – l’étape « enregistrer PSD en PNG »  
Exportez l’image modifiée en PNG, en préservant le canal alpha afin que l’ombre se fonde correctement.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

À ce stade, vous avez réussi à **convertir un PSD en PNG** et à appliquer une ombre portée lors du rendu dans un seul flux de travail.

## Problèmes courants et solutions

| Problème | Cause probable | Solution |
|----------|----------------|----------|
| **Ombre non visible** | `Opacity` réglé à 0 ou calque masqué | Vérifiez que `shadowEffect.getOpacity()` > 0 et que le calque est visible. |
| **Le PNG apparaît plat (pas de transparence)** | Mauvais `PngColorType` utilisé | Utilisez `PngColorType.TruecolorWithAlpha` comme indiqué. |
| **Exception lors du chargement** | Effets non chargés | Assurez‑vous que `loadOptions.setLoadEffectsResource(true)` est appelé. |
| **Index de calque incorrect** | La structure du PSD diffère | Inspectez `im.getLayers()` et choisissez le bon index. |

## Questions fréquentes

**Q : Puis‑je appliquer des ombres portées à plusieurs calques simultanément ?**  
R : Oui. Parcourez `im.getLayers()` et ajoutez ou modifiez un `DropShadowEffect` pour chaque calque cible.

**Q : Que contrôle le paramètre ‘Spread’ ?**  
R : `Spread` détermine la rapidité avec laquelle l’ombre passe d’une opacité maximale à transparente. Une valeur plus élevée crée un bord plus dur.

**Q : Aspose.PSD est‑il compatible avec toutes les versions de Photoshop ?**  
R : Aspose.PSD prend en charge les fichiers PSD de Photoshop 3.0 jusqu’à la dernière version, en gérant la plupart des types de calques et d’effets.

**Q : Comment puis‑je tester le code avant d’acheter une licence ?**  
R : Téléchargez l’essai gratuit depuis la [page de téléchargement d’Aspose.PSD](https://releases.aspose.com/psd/java/) et exécutez l’exemple sans clé de licence.

**Q : Où puis‑je obtenir de l’aide en cas de problème ?**  
R : Publiez votre question sur le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) où la communauté et les ingénieurs d’Aspose peuvent vous aider.

## Conclusion

Vous savez maintenant comment **enregistrer un PSD en PNG**, **convertir un PSD en PNG** et **appliquer un calque d’ombre portée** à l’aide d’Aspose.PSD pour Java. Cette combinaison vous permet d’automatiser la préparation d’images de haute qualité pour le web, le mobile ou les applications de bureau—sans jamais ouvrir Photoshop.

---

**Last Updated:** 2025-12-05  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}