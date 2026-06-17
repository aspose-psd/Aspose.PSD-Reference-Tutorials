---
date: 2026-04-08
description: Apprenez à exporter un PSD en PNG et à créer un nouveau calque PSD avec
  Aspose.PSD pour Java en utilisant une licence temporaire Aspose. Ce tutoriel étape
  par étape couvre la manipulation d’images PSD et la définition de la position du
  calque.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Ajouter un nouveau calque normal au PSD
second_title: Aspose.PSD Java API
title: Exporter le PSD en PNG et ajouter un nouveau calque normal avec Aspose.PSD
  pour Java – licence temporaire Aspose
url: /fr/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter PSD en PNG et ajouter un nouveau calque régulier avec Aspose.PSD pour Java

## Introduction

Dans ce **aspose psd tutorial** vous découvrirez comment **exporter PSD en PNG** tout en **créant un nouveau calque régulier** dans le même fichier, **en utilisant une licence temporaire aspose** pour le développement. Que vous ayez besoin de générer des vignettes prêtes pour le web, de préparer des ressources pour un pipeline de conception, ou simplement d'expérimenter avec la **manipulation d'images psd**, Aspose.PSD pour Java vous offre un contrôle programmatique complet. Nous parcourrons chaque étape — du chargement du fichier source à l'enregistrement à la fois du PSD mis à jour et d'une copie PNG — afin que vous puissiez commencer à manipuler les calques PSD immédiatement.

## Réponses rapides

- **Puis-je exporter PSD en PNG en un seul appel ?** Oui, après avoir ajouté des calques vous pouvez appeler `save` avec `PngOptions`.
- **Ai-je besoin d'une licence pour le développement ?** Une licence temporaire fonctionne pour les tests ; une licence complète est requise pour la production.
- **Quelle version de Java est prise en charge ?** Aspose.PSD fonctionne avec Java 8 et les versions ultérieures.
- **Le positionnement des calques est-il basé sur les pixels ?** Oui, vous définissez les coordonnées gauche, haut, droite, bas en pixels en utilisant les méthodes **set layer position**.
- **Le PNG conservera-t-il la transparence du calque ?** Le PNG contiendra le résultat fusionné de tous les calques visibles.

## Pourquoi utiliser une licence temporaire aspose ?

Une **licence temporaire aspose** vous permet d'évaluer l'ensemble complet des fonctionnalités d'Aspose.PSD sans aucune restriction fonctionnelle. Elle supprime le filigrane d'évaluation, débloque toutes les API — y compris la capacité de **créer de nouveaux calques psd** — et vous permet de tester votre code dans un environnement proche de la production avant d'acheter une licence permanente.

## Prérequis

- **Environnement de développement Java** – JDK 8+ et un outil de construction (Maven/Gradle) installé.
- **Aspose.PSD pour Java** – Téléchargez le JAR le plus récent depuis le site officiel [ici](https://releases.aspose.com/psd/java/).
- **Un fichier PSD d'exemple** – Nous utiliserons `OneLayer.psd` dans les exemples.

## Importer les packages

Ajoutez les imports requis à votre classe Java. Ces classes fournissent la fonctionnalité principale pour la **manipulation d'images psd** et la gestion des calques.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Qu’est‑ce que « set layer position » et pourquoi est‑ce important ?

Lorsque vous ajoutez un nouveau calque, vous devez définir où il apparaît sur le canevas. Les méthodes `setLeft`, `setTop`, `setRight` et `setBottom` **set layer position** en coordonnées de pixels. Un positionnement correct garantit que vos graphiques s'alignent exactement comme prévu, ce qui est crucial pour des tâches telles que le compositing d'éléments UI ou la préparation de fichiers prêts à l'impression.

## Guide étape par étape

### Étape 1 : Charger le fichier PSD

Tout d'abord, chargez le PSD existant que vous souhaitez modifier. Cela vous fournit un objet `PsdImage` avec lequel vous pouvez travailler.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Étape 2 : Préparer les données de pixels et les rectangles

Nous créerons deux tampons de pixels (`int[]`) et définirons les zones rectangulaires où les nouveaux calques seront peints. C'est la base pour **créer un nouveau calque psd**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Étape 3 : Initialiser les données du calque

Remplissez les tampons de pixels avec une valeur ARGB par défaut. La valeur `-10000000` correspond à une teinte sombre semi‑transparente.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Étape 4 : Ajouter des calques réguliers (Manipuler les calques PSD)

Nous **ajoutons maintenant des calques réguliers** à l'image PSD et **définissons la position du calque** en utilisant les propriétés left, top, right et bottom. Cela montre comment **manipuler les calques PSD** de façon programmatique.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Étape 5 : Exporter le PSD en PNG et enregistrer le PSD mis à jour

Une fois les calques en place, enregistrez le document modifié. D'abord nous exportons le résultat en PNG (l'étape **export psd to png**), puis nous persistons le PSD avec les nouveaux calques.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Astuce :** Si vous n'avez besoin que du PNG, vous pouvez ignorer l'appel `save` du PSD et invoquer directement `save` avec `PngOptions`.

## Problèmes courants et dépannage

| Symptôme | Cause probable | Solution |
|----------|----------------|----------|
| Le PNG apparaît vide | Les calques sont invisibles ou totalement transparents | Assurez‑vous de définir des valeurs de pixels non transparentes ou d'appeler `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Incohérence entre la taille du rectangle et la longueur du tableau de pixels | Vérifiez que `rect.width * rect.height == dataArray.length`. |
| LicenseException à l'exécution | Aucune licence valide chargée | Chargez une licence temporaire ou permanente avant d'appeler toute méthode API. |

## Questions fréquemment posées

**Q : Aspose.PSD est‑il compatible avec Java 8 ?**  
R : Oui, Aspose.PSD prend en charge Java 8 et les versions ultérieures.

**Q : Puis‑je appliquer des transformations (rotation, mise à l'échelle) aux calques ajoutés ?**  
R : Absolument ! La classe `Layer` fournit des méthodes telles que `rotate`, `scale` et `translate` pour un contrôle complet des transformations.

**Q : Où puis‑je trouver une documentation supplémentaire sur Aspose.PSD ?**  
R : La documentation détaillée de l'API est disponible [ici](https://reference.aspose.com/psd/java/).

**Q : Comment obtenir une licence temporaire pour Aspose.PSD ?**  
R : Visitez la page de licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

**Q : Existe‑t‑il des forums communautaires pour le support d'Aspose.PSD ?**  
R : Oui, rejoignez les discussions sur les forums Aspose [ici](https://forum.aspose.com/c/psd/34).

## Conclusion

Vous avez maintenant appris comment **exporter PSD en PNG** tout en **ajoutant de nouveaux calques réguliers** avec Aspose.PSD pour Java, et vous avez vu comment une **licence temporaire aspose** vous permet d'essayer ce flux de travail sans restrictions. Ce tutoriel met en avant les capacités essentielles de **manipulation d'images psd** : charger un fichier, créer des calques, remplir les données de pixels et exporter la composition finale. N'hésitez pas à expérimenter avec différentes tailles de rectangles, couleurs de pixels ou effets de calque pour adapter le résultat aux besoins de votre projet.

---

**Dernière mise à jour :** 2026-04-08  
**Testé avec :** Aspose.PSD 24.11 for Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}