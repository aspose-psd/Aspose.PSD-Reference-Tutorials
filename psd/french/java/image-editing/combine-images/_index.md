---
date: 2026-06-28
description: Apprenez comment combiner des images Java en utilisant Aspose.PSD, fusionner
  deux images dans une toile PSD et générer un fichier à calques en quelques minutes.
keywords:
- combine images java
- java graphics draw image
- merge images into psd
linktitle: Combiner des images
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to combine images java using Aspose.PSD, merge two pictures
    into a PSD canvas, and generate a layered file in just minutes.
  headline: Combine Images Java – Create PSD File by Merging Pictures with Aspose.PSD
  type: TechArticle
- description: Learn how to combine images java using Aspose.PSD, merge two pictures
    into a PSD canvas, and generate a layered file in just minutes.
  name: Combine Images Java – Create PSD File by Merging Pictures with Aspose.PSD
  steps:
  - name: Create PSD Options (prepare the file)
    text: '`PsdOptions` holds the configuration for the output PSD, such as compression
      level and color depth.'
  - name: Set the FileCreateSource (define where the PSD will be saved)
    text: '`FileCreateSource` tells Aspose where to write the generated file.'
  - name: Create Image Instance (initialize canvas size)
    text: The `Image` constructor creates a blank PSD canvas with the dimensions you
      specify.
  - name: Initialize Graphics and draw the first picture
    text: '`Graphics` provides drawing capabilities on the canvas. We clear the background
      to white and render the first source image on the left half.'
  - name: Draw the second picture (complete the combine)
    text: Now we place the second image on the right half of the same canvas, creating
      a second layer automatically.
  - name: Save the resulting PSD file
    text: Persist the combined canvas to disk. The resulting `combined.psd` contains
      two editable layers. Congratulations! You have successfully **combine images
      java** and generated a layered PSD file ready for further Photoshop editing.
  type: HowTo
- questions:
  - answer: Aspose.PSD natively reads and writes **15+ formats**, including PSD, PNG,
      JPEG, BMP, TIFF, GIF, and more, making it a versatile choice for image pipelines.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Yes. Each `drawImage` call creates a separate PSD layer, which you can
      later reposition, apply filters, or mask using Aspose.PSD’s extensive layer‑editing
      API.
    question: Can I perform additional edits after combining images?
  - answer: A valid license is required for production use. You can obtain one from
      the Aspose store; a free trial is available for evaluation.
    question: Do I need a commercial license for production?
  - answer: Simply repeat `graphics.drawImage(...)` with appropriate coordinates for
      each additional image. Each call adds a new layer.
    question: How do I add more than two pictures?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support, or consult the official documentation linked in the download page.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Combiner des images Java – Créer un fichier PSD en fusionnant des images avec
  Aspose.PSD
url: /fr/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Combiner des images Java – Créer un fichier PSD en fusionnant des images avec Aspose.PSD

## Introduction

Si vous devez **combine images java** en fusionnant plusieurs images en un seul fichier compatible Photoshop, Aspose.PSD pour Java rend le processus indolore. Dans ce tutoriel, nous allons créer une toile PSD de 600 × 600 pixels, dessiner deux images sources côte à côte, puis enregistrer le résultat sous forme de fichier PSD à calques. À la fin, vous comprendrez pourquoi cette technique est précieuse pour les pipelines graphiques automatisés et comment l’étendre à n’importe quel nombre d’images.

## Réponses rapides
- **Quelle bibliothèque est la meilleure pour fusionner des images en PSD ?** Aspose.PSD for Java.
- **Combien de temps prend une fusion de base ?** Environ 10‑15 minutes pour écrire et exécuter le code.
- **Ai‑je besoin d’une licence pour le développement ?** Un essai gratuit suffit pour l’évaluation ; une licence commerciale est requise pour les déploiements en production.
- **Puis‑je ajouter plus de deux images ?** Absolument – il suffit de répéter les appels `drawImage` pour chaque calque supplémentaire.
- **Quelles versions de Java sont prises en charge ?** Java 8 et supérieures (jusqu’à Java 21).

## Qu’est‑ce que combine images java ?

*Combine images java* désigne la fusion programmatique de plusieurs images raster en un seul fichier image à l’aide des API Java. Aspose.PSD offre une méthode de haut niveau, pure Java, pour le faire sans dépendances natives à Photoshop, vous permettant d’automatiser la composition, de préserver les calques et de produire un PSD compatible Photoshop qui pourra être édité ultérieurement dans Photoshop ou d’autres outils compatibles PSD.

## Pourquoi fusionner des images avec Aspose.PSD ?

Aspose.PSD prend en charge **plus de 15 formats d’image** (y compris PSD, PNG, JPEG, BMP, TIFF, GIF, et plus) et peut traiter **des documents de plusieurs centaines de pages** sans charger le fichier complet en mémoire, grâce à son architecture de streaming. La bibliothèque est **100 % Java géré**, elle s’exécute donc sur tout système d’exploitation supportant le JDK, éliminant les problèmes de DLL natives.

## Prérequis

1. **Bibliothèque Aspose.PSD** – téléchargez‑la depuis [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – Java 8+ est requis ; Java 11 ou supérieur est recommandé pour de meilleures performances.  
3. **Répertoire de travail** – un dossier sur votre machine contenant les images sources (`example1.png`, `example2.png`) et où le PSD de sortie (`combined.psd`) sera écrit.  
4. **Achat de licence** – obtenez une licence commerciale [here](https://purchase.aspose.com/buy) pour une utilisation en production.  
5. **Autres versions Aspose** – explorez les produits et mises à jour supplémentaires [here](https://releases.aspose.com/).

## Importer les packages

Les instructions `import` importent les classes essentielles d’Aspose.PSD dans le scope.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdOptions;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.PsdImageLayer;
import com.aspose.psd.imageoptions.FileCreateSource;
import com.aspose.psd.graphics.Graphics;
import com.aspose.psd.Color;
```

## Comment combiner des images java avec Aspose.PSD ?

Chargez une toile vierge, dessinez chaque image sur la toile, puis enregistrez le résultat sous forme de fichier PSD – c’est l’ensemble du flux de travail en trois étapes concises. L’API crée automatiquement un calque séparé pour chaque appel `drawImage`, vous offrant une pleine éditabilité dans Photoshop par la suite.

### Étape 1 : Créer les options PSD (préparer le fichier)

`PsdOptions` contient la configuration du PSD de sortie, comme le niveau de compression et la profondeur de couleur.

```java
PsdOptions psdOptions = new PsdOptions();
```

### Étape 2 : Définir le FileCreateSource (spécifier où le PSD sera enregistré)

`FileCreateSource` indique à Aspose où écrire le fichier généré.

```java
psdOptions.setSource(new FileCreateSource(dataDir + "combined.psd", false));
```

### Étape 3 : Créer une instance Image (initialiser la taille de la toile)

Le constructeur `Image` crée une toile PSD vierge avec les dimensions que vous spécifiez.

```java
Image image = new Image(psdOptions, 600, 600);
```

### Étape 4 : Initialiser Graphics et dessiner la première image

`Graphics` fournit des capacités de dessin sur la toile. Nous effaçons le fond en blanc et rendons la première image source sur la moitié gauche.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(dataDir + "example1.png", new Rectangle(0, 0, 300, 600));
```

### Étape 5 : Dessiner la deuxième image (terminer la fusion)

Nous plaçons maintenant la deuxième image sur la moitié droite de la même toile, créant automatiquement un deuxième calque.

```java
graphics.drawImage(dataDir + "example2.png", new Rectangle(300, 0, 300, 600));
```

### Étape 6 : Enregistrer le fichier PSD résultant

Enregistrez la toile combinée sur le disque. Le `combined.psd` résultant contient deux calques éditables.

```java
image.save();
```

Félicitations ! Vous avez réussi à **combine images java** et avez généré un fichier PSD à calques prêt pour d’autres éditions Photoshop.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| `File not found` lors du chargement des images source | Chemin `dataDir` incorrect | Vérifiez que `dataDir` pointe vers le dossier contenant `example1.png` et `example2.png`. |
| Le PSD de sortie est vide | `graphics.clear` appelé après le dessin | Appelez `graphics.clear(Color.getWhite())` **avant** toute opération `drawImage`. |
| Exception de licence à l’exécution | Licence Aspose.PSD manquante ou expirée | Appliquez une licence valide avec `License license = new License(); license.setLicense("Aspose.PSD.lic");` avant tout appel d’API. |

## Questions fréquemment posées

**Q : Aspose.PSD est‑il compatible avec tous les formats d’image ?**  
R : Aspose.PSD lit et écrit nativement **plus de 15 formats**, y compris PSD, PNG, JPEG, BMP, TIFF, GIF, et plus, ce qui en fait un choix polyvalent pour les pipelines d’image.

**Q : Puis‑je effectuer des modifications supplémentaires après la fusion des images ?**  
R : Oui. Chaque appel `drawImage` crée un calque PSD distinct, que vous pouvez repositionner, appliquer des filtres ou masquer à l’aide de l’API de modification de calques d’Aspose.PSD.

**Q : Ai‑je besoin d’une licence commerciale pour la production ?**  
R : Une licence valide est requise pour une utilisation en production. Vous pouvez en obtenir une dans la boutique Aspose ; un essai gratuit est disponible pour l’évaluation.

**Q : Comment ajouter plus de deux images ?**  
R : Répétez simplement `graphics.drawImage(...)` avec les coordonnées appropriées pour chaque image supplémentaire. Chaque appel ajoute un nouveau calque.

**Q : Où puis‑je obtenir de l’aide en cas de problème ?**  
R : Consultez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le support communautaire, ou la documentation officielle liée sur la page de téléchargement.

---

**Dernière mise à jour :** 2026-06-28  
**Testé avec :** Aspose.PSD 24.11 pour Java  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Créer une image en définissant le chemin dans Aspose.PSD pour Java](/psd/java/image-editing/create-image-by-setting-path/)
- [Créer une image en utilisant un flux dans Aspose.PSD pour Java](/psd/java/image-editing/create-image-using-stream/)
- [Redimensionner une image Java - Utiliser l’énumération Resize Type dans Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

```java
PsdOptions imageOptions = new PsdOptions();
```

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

```java
Image image = Image.create(imageOptions, 600, 600);
```

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

```java
image.save();
```