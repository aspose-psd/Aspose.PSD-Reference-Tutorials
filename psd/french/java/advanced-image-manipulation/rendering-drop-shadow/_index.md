---
date: 2025-12-04
description: Apprenez à enregistrer un PSD au format PNG et à appliquer une ombre
  portée rendue à l’aide d’Aspose.PSD pour Java. Ce guide explique comment ajouter
  une ombre, convertir un PSD en PNG et appliquer une ombre portée en Java.
language: fr
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Enregistrez le PSD en PNG et ajoutez une ombre portée avec Aspose.PSD Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer PSD en PNG & ajouter une ombre portée avec Aspose.PSD Java

## Introduction

Si vous travaillez avec des fichiers Photoshop en Java, **enregistrer PSD en PNG** tout en ajoutant une ombre portée professionnelle est une exigence courante. Aspose.PSD rend cette tâche simple, vous permettant de **convertir PSD en PNG** et **appliquer une ombre portée Java** en quelques lignes de code seulement. Dans ce tutoriel, nous parcourrons l’ensemble du processus, du chargement d’un fichier PSD à l’exportation du PNG final avec l’effet d’ombre rendu.

## Réponses rapides
- **Que signifie « enregistrer PSD en PNG » ?** Cela convertit un fichier Photoshop à calques en une image PNG plate, en conservant la transparence.  
- **Puis‑je ajouter une ombre portée lors de la conversion ?** Oui — Aspose.PSD vous permet de modifier les effets de calque avant l’exportation.  
- **Ai‑je besoin d’une licence pour exécuter le code ?** Un essai gratuit suffit pour l’évaluation ; une licence est requise pour la production.  
- **Quelle version de Java est prise en charge ?** Java 8 ou supérieur.  
- **L’effet d’ombre portée est‑il personnalisable ?** Absolument — vous pouvez ajuster la couleur, l’opacité, la distance, la taille, l’angle, etc.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Environnement de développement Java** – JDK 8 ou plus récent installé.  
- **Bibliothèque Aspose.PSD** – Téléchargez le JAR le plus récent depuis le site officiel [ici](https://releases.aspose.com/psd/java/).  
- **Un fichier PSD** – Un fichier contenant au moins un calque que vous souhaitez améliorer avec une ombre.  

## Comment enregistrer PSD en PNG avec une ombre portée en Java ?

Voici un guide étape par étape. Chaque étape comprend une brève explication suivie du code exact à copier.

### Étape 1 : Importer les packages requis

Nous commençons par importer les classes qui offrent le chargement d’image, la gestion des effets et les capacités d’exportation PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### Étape 2 : Définir le répertoire du document

Indiquez le dossier où votre PSD source et le PNG résultant seront stockés.

```java
String dataDir = "Your Document Directory";
```

### Étape 3 : Définir les chemins des fichiers PSD et PNG

Spécifiez les chemins complets pour le PSD d’entrée et le PNG de sortie.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Étape 4 : Charger le fichier PSD avec les effets activés

Activer **loadEffectsResource** garantit que les effets de calque (comme les ombres) sont disponibles pour la manipulation.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Étape 5 : Accéder à l’effet d’ombre portée

Ici nous récupérons le premier effet appliqué au deuxième calque (indice 1). C’est ici que nous lirons ou modifierons les paramètres de l’ombre.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Étape 6 : Valider les propriétés de l’effet d’ombre (facultatif mais utile)

Vérifier les propriétés existantes vous aide à décider si vous devez les modifier. Les assertions ci‑dessous confirment les valeurs par défaut.

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

> **Astuce :** Si vous souhaitez **ajouter une ombre** avec des paramètres personnalisés, modifiez les propriétés sur `shadowEffect` avant l’enregistrement (par ex., `shadowEffect.setColor(Color.getRed());`).

### Étape 7 : Enregistrer l’image modifiée en PNG

Enfin, nous exportons le PSD (avec l’ombre rendue) vers un fichier PNG. L’option `TruecolorWithAlpha` préserve la transparence.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Et voilà — un flux complet **convertir PSD en PNG** qui **applique également une ombre portée java** en une seule passe.

## Pourquoi utiliser Aspose.PSD pour cette tâche ?

- **Pas besoin de Photoshop natif** – Fonctionne sur n’importe quelle plateforme supportant Java.  
- **Fidélité totale du PSD** – Toutes les informations de calque, masques et effets sont conservés.  
- **Contrôle granulaire** – Ajustez chaque paramètre de l’ombre portée avant l’exportation.  
- **Haute performance** – Optimisé pour les gros fichiers et le traitement par lots.

## Problèmes courants et dépannage

| Symptôme | Cause probable | Solution |
|----------|----------------|----------|
| `NullPointerException` sur `shadowEffect` | Le calque cible n’a aucun effet ou l’indice est incorrect. | Vérifiez l’indice du calque (`im.getLayers()[i]`) et assurez‑vous qu’un effet existe. |
| PNG exporté est vide | Options PNG mal configurées ou image non enregistrée. | Utilisez `PngColorType.TruecolorWithAlpha` et confirmez que le chemin de `im.save()` est accessible en écriture. |
| La couleur de l’ombre n’est pas visible | Opacité de l’ombre à 0 ou couleur identique à l’arrière‑plan. | Définissez `shadowEffect.setOpacity(255);` et choisissez une couleur contrastante. |

## Questions fréquemment posées

**Q : Puis‑je appliquer des ombres portées à plusieurs calques en même temps ?**  
R : Oui. Parcourez `im.getLayers()` et modifiez chaque `DropShadowEffect` selon vos besoins.

**Q : Que fait le paramètre « Spread » ?**  
R : Il contrôle la netteté de la transition de l’ombre entre totalement opaque et transparente. Un spread plus élevé crée un bord plus dur.

**Q : Aspose.PSD est‑il compatible avec toutes les versions de Photoshop ?**  
R : Il prend en charge une large gamme de versions PSD, des premières versions jusqu’aux fichiers Photoshop CC les plus récents.

**Q : Comment obtenir de l’aide en cas de problème ?**  
R : Visitez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le support communautaire et l’assistance officielle.

**Q : Puis‑je essayer Aspose.PSD avant d’acheter ?**  
R : Bien sûr. Téléchargez un essai gratuit depuis le [site Aspose](https://releases.aspose.com/).

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Dernière mise à jour :** 2025-12-04  
**Testé avec :** Aspose.PSD 24.12 for Java  
**Auteur :** Aspose  

---