---
date: 2026-11-04
description: Apprenez comment utiliser Aspose.PSD for Java pour appliquer une invert
  adjustment layer, traiter par lots des images PSD et créer des fichiers PSD d’image
  négative.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Comment utiliser Aspose.PSD for Java pour ajouter une invert adjustment
  layer, traiter par lots des images PSD et créer un PSD d’image négative. Suivez
  le guide étape par étape.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Comment utiliser Aspose.PSD pour ajouter une invert adjustment layer en
  Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Comment utiliser Aspose.PSD pour ajouter une invert adjustment layer en Java
url: /fr/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment utiliser Aspose.PSD pour ajouter un calque de réglage d'inversion en Java

## Introduction

Si vous recherchez une **image processing java library** robuste, Aspose.PSD pour Java est l'une des options les plus polyvalentes du marché. Dans ce tutoriel, vous verrez **comment utiliser Aspose** pour insérer un **Invert Adjustment Layer** dans un fichier PSD, l'empiler avec d'autres réglages, et même exécuter l'opération sur des dizaines de fichiers. Que vous construisiez un outil de traitement par lots, un service d'images côté serveur, ou un éditeur d'image unique, les étapes ci‑dessous vous permettront de passer du PSD source à une image négative entièrement modifiable en quelques minutes.

## Réponses rapides
- **Que fait le Invert Adjustment Layer ?** Il inverse chaque valeur RVB dans la zone sélectionnée, transformant l'image en négatif photographique.  
- **Quelle bibliothèque fournit cette fonctionnalité ?** Aspose.PSD, une **image processing java library** leader.  
- **Puis-je l'empiler avec d'autres réglages ?** Oui – vous pouvez **apply multiple adjustment layers** tels que Brightness/Contrast, Hue/Saturation, etc.  
- **Ai-je besoin d'une licence pour le développement ?** Un essai gratuit est disponible ; une licence est requise pour une utilisation en production.  
- **Combien de temps prend l'implémentation ?** Typiquement moins de 10 minutes pour un cas d'utilisation basique.

## Qu'est-ce que le Invert Adjustment Layer ?

Le Invert Adjustment Layer est une modification non destructive qui inverse les valeurs de couleur de chaque pixel qu'il affecte. Comme il se situe au-dessus de la pile de calques, vous pouvez basculer sa visibilité ou le réorganiser sans modifier de façon permanente les données d'image originales. C'est le moyen le plus rapide de **create negative image PSD** fichiers ou d'obtenir un aspect négatif de film classique.

## Pourquoi utiliser Aspose.PSD comme votre image processing java library ?

Aspose.PSD prend en charge **200+ PSD features**, peut lire et écrire des fichiers Photoshop sans nécessiter Photoshop, et traite des documents de plusieurs centaines de pages en utilisant moins de 500 Mo de mémoire du tas. Il fonctionne sur n'importe quel runtime Java (Java 6+), ce qui le rend idéal pour **batch process psd images** sous Windows, Linux ou macOS.

## Prérequis

Avant de commencer, assurez-vous d'avoir :

1. **Aspose.PSD for Java** – téléchargez le dernier JAR depuis le site officiel [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 ou ultérieur installé et configuré dans votre `PATH`.  

Vous êtes maintenant prêt à écrire le code.

## Importer les packages

La classe `PsdImage` représente un document Photoshop complet en mémoire, tandis que les classes de calques de réglage résident dans le package `com.aspose.psd.layers.adjustments`.

La classe `PsdImage` est l'objet de niveau supérieur d'Aspose.PSD qui encapsule la structure et les données de pixels d'un fichier PSD. Importez les espaces de noms, puis vous pourrez charger, modifier et enregistrer des fichiers PSD.

## Étape 1 : configurer le répertoire du document

Définissez le dossier qui contient votre fichier PSD source et où la sortie sera enregistrée. L'utilisation de chemins absolus évite les `NullPointerException` lorsque le répertoire de travail change.

## Étape 2 : charger le fichier PSD

Chargez le fichier source dans un objet `PsdImage`. Cet objet conserve la hiérarchie complète des calques en mémoire, permettant des modifications non destructives.

La classe `PsdImage` fournit une méthode statique `load` qui lit l'en-tête du fichier, valide le format et construit une représentation en mémoire prête à être manipulée.

## Étape 3 : ajouter un calque de réglage d'inversion

Appelez la méthode intégrée pour insérer un Invert Adjustment Layer au sommet de la pile de calques actuelle. Vous pouvez ensuite ajouter d'autres calques (p. ex., Brightness, Hue) pour **apply multiple adjustment layers** dans un seul flux de travail.

`addInvertAdjustmentLayer()` ajoute un Invert Adjustment Layer à la collection de calques du PSD.

## Étape 4 : enregistrer la sortie

Enregistrez le PSD modifié sur le disque.  

`save()` écrit le fichier PSD, incluant tous les calques et métadonnées, vers le chemin spécifié.

L'enregistrement utilise la même méthode `save` qui écrit le document complet, incluant tous les calques de réglage, masques et métadonnées, dans le format spécifié.

### Que s'est-il passé ?

Le fichier PSD a été chargé dans un objet `PsdImage`, un `InvertAdjustmentLayer` a été créé et ajouté comme calque le plus haut, et le document a été enregistré. Cette séquence préserve les données d'image originales tout en ajoutant un effet d'inversion non destructif qui peut être basculé ou réordonné plus tard.

Vous avez maintenant utilisé avec succès Aspose.PSD, une **image processing java library**, pour manipuler un fichier PSD.

## Comment traiter par lots des images PSD avec un réglage d'inversion ?

Chargez chaque fichier dans une boucle `for`, appliquez les mêmes étapes, et appelez `save` à chaque itération. Comme Aspose.PSD traite les fichiers de manière flux, vous pouvez gérer **hundreds of PSDs** tout en maintenant l'utilisation de la mémoire sous 300 Mo en réutilisant la même instance `PsdImage`.

## Comment convertir un PSD en image négative ?

Ajoutez le Invert Adjustment Layer comme élément le plus haut et enregistrez le document – cette opération équivaut à **convert PSD to negative**. Vous pouvez ensuite désactiver ou supprimer le calque pour revenir à l'apparence originale sans recharger le fichier source.

## Problèmes courants et astuces

| Problème | Cause | Solution |
|----------|-------|----------|
| **NullPointerException sur `Image.load`** | Chemin de fichier incorrect ou fichier manquant | Vérifiez `dataDir` et le nom du fichier ; utilisez des chemins absolus pour les tests |
| **Ordre des calques inattendu** | L'ajout de calques après ceux existants modifie l'empilement | Insérez le calque d'inversion avant les autres réglages, ou réordonnez via `psdImage.getLayers().move()` |
| **Ralentissement des performances sur de grands PSD** | Chargement de fichiers très volumineux en mémoire | Augmentez le tas JVM (`-Xmx2g`) ou traitez les fichiers par morceaux en utilisant `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` |

## Questions fréquemment posées

**Q : Aspose.PSD est‑il compatible avec toutes les versions de Java ?**  
A : Oui, il prend en charge Java 6.0 et ultérieur, y compris Java 8, 11 et 17.

**Q : Puis‑je appliquer plusieurs calques de réglage en une seule opération ?**  
A : Absolument. Après avoir ajouté le calque d'inversion, vous pouvez appeler `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()`, etc., pour empiler les effets.

**Q : Où puis‑je trouver la référence complète de l'API ?**  
A : La documentation complète est disponible [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q : Existe‑t‑il un essai gratuit pour Aspose.PSD ?**  
A : Oui, vous pouvez télécharger une version d'essai [Aspose.PSD trial download](https://releases.aspose.com/).

**Q : Comment obtenir une licence temporaire pour les tests ?**  
A : Demandez une licence temporaire [temporary license request page](https://purchase.aspose.com/temporary-license/).

---

**Dernière mise à jour :** 2026-11-04  
**Testé avec :** Aspose.PSD 24.12 for Java  
**Auteur :** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## Tutoriels associés

- [Ajouter un calque de réglage de niveau aux fichiers PSD avec Aspose.PSD pour Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [Comment ajouter un calque de réglage – Mélangeur de canaux dans PSD (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [Comment modifier un PSD - Ajouter un calque de réglage de courbes avec Java](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}