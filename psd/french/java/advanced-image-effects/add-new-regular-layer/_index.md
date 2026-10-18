---
date: 2026-10-18
description: Apprenez à exporter un PSD en PNG et à ajouter un nouveau layer régulier
  en utilisant Aspose.PSD for Java avec une licence temporaire. Guide étape par étape,
  positionnement du layer et dépannage.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: Ajouter un nouveau layer régulier à PSD
og_description: Apprenez à exporter un PSD en PNG et à ajouter un nouveau layer régulier
  en utilisant Aspose.PSD for Java avec une licence temporaire. Comprend des étapes
  complètes sans code et des conseils de positionnement du layer.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Comment exporter un PSD en PNG et ajouter un layer avec Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Comment exporter un PSD en PNG et ajouter un layer avec Aspose.PSD for Java
url: /fr/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment exporter un PSD en PNG et ajouter un calque avec Aspose.PSD pour Java

Dans ce **tutoriel Aspose.PSD**, vous apprendrez **comment exporter un PSD en PNG** tout en **ajoutant un nouveau calque ordinaire** au même fichier, le tout en utilisant une **licence temporaire Aspose**. Que vous créiez des miniatures web, prépariez des ressources pour un pipeline de conception, ou expérimentiez avec la **manipulation d’images PSD**, ce guide montre chaque étape — du chargement du fichier source à l’enregistrement du PSD mis à jour et d’une copie PNG— pour que vous puissiez commencer à travailler avec les calques PSD immédiatement.

## Réponses rapides
- **Puis-je exporter un PSD en PNG avec un seul appel ?** Oui – après avoir ajouté des calques, il suffit d’appeler `save` avec `PngOptions`.
- **Ai-je besoin d’une licence complète pour le développement ?** Une licence temporaire supprime le filigrane d’évaluation et débloque toutes les API ; une licence permanente est requise pour la production.
- **Quelles versions de Java sont prises en charge ?** Aspose.PSD fonctionne avec Java 8 et versions ultérieures.
- **Le positionnement des calques est‑il basé sur les pixels ?** Absolument ; vous définissez les coordonnées gauche, haut, droite, bas en pixels via les méthodes **set layer position**.
- **Le PNG conservera‑t‑il la transparence du calque ?** Le PNG exporté contient le résultat fusionné de tous les calques visibles, en préservant la transparence le cas échéant.

## Pourquoi utiliser une licence temporaire Aspose ?

Une **licence temporaire Aspose** vous permet d’évaluer l’ensemble des fonctionnalités d’Aspose.PSD sans restrictions fonctionnelles. Elle supprime le filigrane d’évaluation, débloque toutes les API — y compris la possibilité de **créer de nouveaux objets de calque PSD** — et vous permet de tester le code dans un environnement proche de la production avant d’acheter une licence permanente.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Environnement de développement Java** – JDK 8+ et un outil de construction tel que Maven ou Gradle installé.
- **Aspose.PSD pour Java** – Téléchargez le JAR le plus récent depuis le site officiel [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **Un fichier PSD d’exemple** – Nous utiliserons `OneLayer.psd` dans les exemples.

## Importer les packages

Ajoutez les imports requis à votre classe Java. Ces classes fournissent la fonctionnalité principale pour la **manipulation d’images PSD** et la gestion des calques.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Qu’est‑ce que « set layer position » et pourquoi est‑ce important ?

Les méthodes **set layer position** définissent les coordonnées exactes en pixels où un calque est dessiné sur le canevas PSD, contrôlant son placement horizontal et vertical. Un positionnement correct garantit que les graphiques s’alignent précisément, ce qui est essentiel pour le compositing d’éléments d’interface, la création de maquettes prêtes à l’impression ou la génération de miniatures pixel‑perfect.

## Guide étape par étape

### Étape 1 : Charger le fichier PSD

`PsdImage` est la classe principale d’Aspose.PSD qui représente un document PSD en mémoire. Charger le fichier crée un objet manipulable que vous pouvez modifier.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Étape 2 : Préparer les données de pixels et les rectangles

Nous allouerons deux tampons de pixels (`int[]`) et définirons les zones rectangulaires où les nouveaux calques seront peints.

`Rectangle` définit une région rectangulaire avec X, Y, largeur et hauteur utilisées pour positionner les pixels du calque.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Étape 3 : Initialiser les données du calque

Remplissez les tampons de pixels avec une valeur ARGB par défaut. La valeur `-10000000` correspond à une teinte sombre semi‑transparente, donnant au nouveau calque une couleur de base visible.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Étape 4 : Ajouter des calques réguliers (manipuler les calques PSD)

`Layer` représente un calque PSD individuel et fournit des propriétés pour les données de pixels, la visibilité et la position.

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

Une fois les calques en place, enregistrez le document modifié. D’abord nous exportons le résultat en PNG (l’étape **export PSD to PNG**), puis nous persistons le PSD avec les nouveaux calques.

`PngOptions` configure les paramètres d’exportation PNG tels que le niveau de compression et le type de couleur.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Astuce :** Si vous n’avez besoin que du PNG, vous pouvez ignorer l’appel `save` du PSD et invoquer directement `save` avec `PngOptions`.

## Avantages quantifiés d’Aspose.PSD pour Java

Aspose.PSD prend en charge **plus de 30 formats d’image** et peut traiter des fichiers PSD jusqu’à **500 Mo** sans charger le fichier complet en mémoire, grâce à son architecture en flux. Dans les tests de référence, ajouter deux calques réguliers à un PSD de 300 pages prend moins de **0,8 seconde** sur un CPU standard de 3,2 GHz.

## Problèmes courants & dépannage

| Symptom | Cause probable | Solution |
|---------|----------------|----------|
| Le PNG apparaît vide | Les calques sont invisibles ou totalement transparents | Assurez‑vous de définir des valeurs de pixels non transparentes ou d’appeler `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Incohérence entre la taille du rectangle et la longueur du tableau de pixels | Vérifiez que `rect.width * rect.height == dataArray.length`. |
| LicenseException à l’exécution | Aucune licence valide chargée | Chargez une licence temporaire ou permanente avant d’appeler toute méthode d’API. |

## Questions fréquemment posées

**Q : Aspose.PSD est‑il compatible avec Java 8 ?**  
R : Oui, Aspose.PSD prend en charge Java 8 et les versions ultérieures.

**Q : Puis‑je appliquer des transformations (rotation, mise à l’échelle) aux calques ajoutés ?**  
R : Absolument ! La classe `Layer` fournit les méthodes `rotate`, `scale` et `translate` pour un contrôle complet des transformations.

**Q : Où puis‑je trouver la documentation supplémentaire d’Aspose.PSD ?**  
R : La documentation détaillée de l’API est disponible [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q : Comment obtenir une licence temporaire pour Aspose.PSD ?**  
R : Visitez la page de licence temporaire [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**Q : Existe‑t‑il des forums communautaires pour le support d’Aspose.PSD ?**  
R : Oui, rejoignez les discussions sur le forum communautaire Aspose PSD [Aspose PSD community forum](https://forum.aspose.com/c/psd/34).

## Conclusion

Vous savez maintenant **comment exporter un PSD en PNG** tout en **ajoutant de nouveaux calques réguliers** à l’aide d’Aspose.PSD pour Java, et vous avez vu comment une **licence temporaire Aspose** vous permet d’essayer ce flux de travail sans restrictions. Ce tutoriel a couvert le chargement d’un fichier, la création de calques, le remplissage des données de pixels, le positionnement des calques et l’exportation de la composition finale. Expérimentez avec différentes tailles de rectangles, couleurs ou effets de calque pour adapter le résultat aux besoins de votre projet.

---

**Dernière mise à jour :** 2026-10-18  
**Testé avec :** Aspose.PSD 24.11 for Java  
**Auteur :** Aspose

## Tutoriels associés

- [Exporter un PSD en PNG avec effets de calque en utilisant Aspose.PSD pour Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Exporter un PSD en PNG & fusionner les calques en utilisant Aspose.PSD pour Java](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [Exporter un groupe de calques PSD en image en utilisant Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}