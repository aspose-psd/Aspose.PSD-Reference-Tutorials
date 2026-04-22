---
date: 2026-02-07
description: Apprenez à enregistrer un PSD au format PNG, à exporter un PNG avec canal
  alpha et à ajouter un calque d’ombre portée en utilisant Aspose.PSD pour Java –
  un guide complet, étape par étape.
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Enregistrer le PSD au format PNG et appliquer l’ombre portée lors du rendu
  dans Aspose.PSD pour Java
url: /fr/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer le PSD en PNG et appliquer une ombre portée lors du rendu avec Aspose.PSD pour Java

## Introduction

Si vous travaillez avec des fichiers Photoshop en Java, **enregistrer le PSD en PNG** est l’une des tâches les plus courantes que vous rencontrerez. Avec Aspose.PSD, vous pouvez non seulement **convertir le PSD en PNG**, mais aussi améliorer l’image en **ajoutant un calque d’ombre portée**. Dans ce tutoriel, nous parcourrons l’ensemble du processus — chargement d’un PSD, application d’une ombre portée lors du rendu, puis **enregistrement du PSD au format PNG** — afin que vous puissiez intégrer ce flux de travail dans vos propres projets en toute confiance.

## Quick Answers
- **Quelle bibliothèque gère la conversion PSD en PNG ?** Aspose.PSD for Java.  
- **Combien de temps prend l’implémentation de l’ombre portée ?** Environ 10‑15 minutes pour un exemple de base.  
- **Ai‑je besoin d’une licence pour exécuter le code ?** Un essai gratuit suffit pour l’évaluation ; une licence est requise en production.  
- **Puis‑je appliquer l’ombre à plusieurs calques ?** Oui — il suffit de parcourir les calques souhaités.  
- **Quelle version de Java est requise ?** Java 8 ou supérieure.

## Qu’est‑ce que « enregistrer le PSD en PNG » et pourquoi est‑ce important ?

Enregistrer un PSD au format PNG crée une image sans perte largement prise en charge qui conserve la transparence. Cela est essentiel lorsque vous devez afficher des ressources Photoshop sur le web, dans des applications mobiles ou dans le cadre d’un pipeline de traitement d’image plus vaste. Ajouter une ombre portée en même temps vous permet de produire un effet visuel soigné sans ouvrir Photoshop.

## Pourquoi utiliser Aspose.PSD pour ce flux de travail ?

* **Contrôle complet depuis le code** – Aucun besoin de lancer Photoshop ou de dépendre d’outils externes.  
* **Conserve les effets de calque** – Les ombres portées, les lueurs et autres effets sont rendus exactement comme ils apparaissent dans le fichier original.  
* **Exportation PNG avec alpha** – La sortie PNG garde le fond transparent, prête à être utilisée sur le web ou dans une interface utilisateur.  
* **Multi‑plateforme** – Fonctionne sur tout OS supportant Java 8+.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Environnement de développement Java** – JDK 8 ou plus récent installé.  
- **Aspose.PSD for Java** – Téléchargez le JAR le plus récent depuis la [page de téléchargement d’Aspose.PSD](https://releases.aspose.com/psd/java/).  
- **Un fichier PSD** – Le fichier doit contenir au moins un calque que vous souhaitez enrichir d’une ombre portée (par ex., *Shadow.psd*).  

## Import Packages

Tout d’abord, importez les classes dont nous aurons besoin. Cela nous donne accès au chargement d’image, aux effets de calque et aux options d’exportation PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step‑by‑Step Guide

### Step 1: Define Document Directory  
Indiquez au programme où se trouve votre PSD source.

```java
String dataDir = "Your Document Directory";
```

### Step 2: Set PSD and PNG File Paths  
Définissez à la fois le PSD d’entrée et le PNG de sortie qui contiendra l’ombre portée rendue.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Step 3: Load PSD File with Effects  
Activez le chargement des ressources d’effets afin que nous puissions manipuler l’effet d’ombre portée.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Step 4: Access Drop Shadow Effect  
Récupérez le premier effet d’ombre portée du deuxième calque (index 1). C’est ici que nous vérifierons ou modifierons les paramètres.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Step 5: Validate Shadow Effect Properties  
Assurez‑vous que les propriétés de l’effet correspondent à vos attentes avant d’enregistrer. Vous pouvez également ajuster ces valeurs pour obtenir un rendu différent.

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

> **Pro tip:** Ajustez `setSpread()` ou `setNoise()` pour créer des ombres plus douces ou plus texturées.

### Step 6: Save as PNG – the “save PSD as PNG” step  
Exportez l’image modifiée au format PNG, en conservant le canal alpha afin que l’ombre se fonde correctement.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

À ce stade, vous avez **converti le PSD en PNG**, **exporté le PNG avec alpha**, et appliqué une ombre portée lors du rendu dans un seul flux de travail.

## Export PNG with Alpha Transparency

Lorsque vous avez besoin que la sortie PNG conserve son arrière‑plan transparent—en particulier pour des superpositions UI ou des graphiques web—assurez‑vous d’utiliser `PngColorType.TruecolorWithAlpha` comme indiqué dans l’étape d’enregistrement ci‑dessus. Cela garantit que l’ombre portée repose sur un canevas transparent plutôt que sur un fond uni.

## Add Drop Shadow Layer Using Java

Si votre PSD contient plusieurs calques nécessitant des ombres, répétez simplement **l’Étape 4** et **l’Étape 5** à l’intérieur d’une boucle qui itère sur `im.getLayers()`. Chaque itération peut créer ou modifier une instance `DropShadowEffect`, vous offrant un contrôle granulaire sur l’opacité, la distance, la taille et l’angle pour chaque calque.

## Java Convert Photoshop PNG – Common Use Cases

* **Pipelines d’actifs web** – Convertir les PSD fournis par les designers en PNG prêts pour le web avec des ombres intégrées.  
* **Ressources d’applications mobiles** – Générer des icônes PNG transparentes à la volée, évitant une exportation manuelle.  
* **Traitement par lots** – Automatiser la conversion de centaines de fichiers PSD dans un job côté serveur.

## Common Issues and Solutions

| Problème | Cause probable | Solution |
|----------|----------------|----------|
| **Ombre non visible** | `Opacity` à 0 ou calque masqué | Vérifiez que `shadowEffect.getOpacity()` > 0 et que le calque est visible. |
| **Le PNG apparaît plat (pas de transparence)** | Mauvais `PngColorType` utilisé | Utilisez `PngColorType.TruecolorWithAlpha` comme indiqué. |
| **Exception lors du chargement** | Effets non chargés | Assurez‑vous que `loadOptions.setLoadEffectsResource(true)` est appelé. |
| **Index de calque incorrect** | La structure du PSD diffère | Inspectez `im.getLayers()` et choisissez le bon index. |

## Frequently Asked Questions

**Q : Puis‑je appliquer des ombres portées à plusieurs calques simultanément ?**  
R : Oui. Parcourez `im.getLayers()` et ajoutez ou modifiez un `DropShadowEffect` pour chaque calque cible.

**Q : Que contrôle le paramètre ‘Spread’ ?**  
R : `Spread` détermine la rapidité avec laquelle l’ombre passe d’une opacité maximale à transparente. Une valeur plus élevée crée un bord plus dur.

**Q : Aspose.PSD est‑il compatible avec toutes les versions de Photoshop ?**  
R : Aspose.PSD prend en charge les fichiers PSD de Photoshop 3.0 jusqu’à la version la plus récente, en gérant la plupart des types de calques et d’effets.

**Q : Comment tester le code avant d’acheter une licence ?**  
R : Téléchargez l’essai gratuit depuis la [page de téléchargement d’Aspose.PSD](https://releases.aspose.com/psd/java/) et exécutez l’exemple sans clé de licence.

**Q : Où puis‑je obtenir de l’aide si je rencontre des problèmes ?**  
R : Posez votre question sur le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) où la communauté et les ingénieurs d’Aspose peuvent vous assister.

## Conclusion

Vous savez maintenant comment **enregistrer le PSD en PNG**, **exporter le PNG avec alpha**, **convertir les PNG Photoshop** et **appliquer un calque d’ombre portée** en utilisant Aspose.PSD pour Java. Cette combinaison vous permet d’automatiser la préparation d’images de haute qualité pour le web, le mobile ou les applications de bureau—sans jamais ouvrir Photoshop.

---

**Dernière mise à jour :** 2026-02-07  
**Testé avec :** Aspose.PSD 24.11 for Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}