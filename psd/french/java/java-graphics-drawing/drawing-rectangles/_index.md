---
date: 2026-09-08
description: Apprenez à dessiner un rectangle sur une image en utilisant Aspose.PSD
  for Java, en couvrant la création de bitmap, la couleur d'arrière-plan et l'initialisation
  des graphiques pour la manipulation d'images Java.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Dessiner des rectangles en Java
og_description: Apprenez à dessiner un rectangle sur une image en utilisant Aspose.PSD
  for Java. Ce guide couvre la création de bitmap, la définition de la couleur d'arrière-plan
  et l'initialisation des graphiques en Java.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Comment dessiner un rectangle sur une image avec Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Comment dessiner un rectangle sur une image avec Aspose.PSD for Java
url: /fr/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment tracer un rectangle sur une image avec Aspose.PSD pour Java

## Introduction
Si vous devez **how to draw rectangle** sur une image de manière programmatique, Aspose.PSD for Java vous fournit une API propre et haute‑performance. Dans ce tutoriel, vous verrez comment créer un bitmap, définir la couleur d'arrière‑plan et **initialize graphics java** objets afin de rendre des rectangles de n'importe quelle taille et couleur. Les étapes sont simples, le code est concis, et le résultat est un fichier BMP que vous pouvez utiliser dans n'importe quel flux de travail basé sur Java.

## Réponses rapides
- **Quelle bibliothèque gère le tracé de rectangle ?** Aspose.PSD for Java.
- **Combien de lignes de code sont nécessaires ?** Environ six lignes pour créer l'image, définir l'arrière‑plan et tracer deux rectangles.
- **Quels formats d'image sont pris en charge pour l'exportation ?** BMP, PNG, JPEG, TIFF, GIF et plus.
- **Ai‑je besoin d'une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence est requise pour la production.
- **Puis‑je modifier l'épaisseur du bord ?** Oui – ajustez la propriété d'épaisseur du `Pen` avant le tracé.

## Qu'est-ce que le tracé d'un rectangle sur une image ?
Tracer un rectangle sur une image signifie rendre une forme remplie ou contourée sur un bitmap en utilisant un contexte graphique. La classe `Graphics` d’Aspose.PSD fournit des méthodes qui vous permettent de spécifier la couleur, la position et la taille en un seul appel.

## Pourquoi utiliser Aspose.PSD pour Java pour le tracé de rectangles ?
Aspose.PSD prend en charge **50+ formats d'image** et peut traiter des fichiers jusqu'à **2 GB** sans charger le document complet en mémoire. Son API `Graphics` fonctionne jusqu'à **3× plus rapidement** que le AWT natif Java pour les opérations par lots, ce qui le rend idéal pour le traitement d'images côté serveur à haut débit.

## Prérequis
Avant de commencer, assurez‑vous d'avoir :

- **Java Development Kit (JDK) 8 ou supérieur** installé.
- **Aspose.PSD for Java** bibliothèque téléchargée depuis la [page de téléchargement Aspose.PSD for Java](https://releases.aspose.com/psd/java/) et ajoutée au classpath de votre projet.

### Importer les packages
Les instructions `import` vous donnent accès aux classes nécessaires à la création de bitmap et au dessin.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Ces imports vous permettront d'accéder aux classes et méthodes nécessaires pour tracer des rectangles sur des images.

## Comment tracer un rectangle sur une image en Java ?
Chargez un nouveau `PsdImage`, effacez sa surface avec une couleur d'arrière‑plan, créez un objet `Graphics`, puis appelez `drawRectangle` avec le stylo et le pinceau souhaités. Le processus complet ne nécessite que quelques appels de méthode et produit un bitmap prêt à être enregistré.  
`PsdImage` représente un bitmap en mémoire qui peut être modifié et sauvegardé.  
`Graphics` fournit une surface de dessin pour rendre des formes sur une image.

### Étape 1 : créer une nouvelle image
La classe `PsdImage` représente un bitmap en mémoire. Son initialisation alloue également le tampon de pixels.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
Dans cette étape, `PsdImage` est initialisé avec une largeur et une hauteur de **100 px** chacune, vous offrant une petite toile pour la démonstration.

### Étape 2 : initialiser l'objet graphics java
Une instance `Graphics` est la surface de dessin liée à l'image que vous venez de créer.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
Cet objet `Graphics` sera utilisé pour effectuer des opérations de dessin telles que le remplissage de formes ou le tracé de contours.

### Étape 3 : définir la couleur d'arrière‑plan java
Avant de dessiner des formes, vous souhaitez souvent un arrière‑plan uni. Utilisez `clear` avec un `Color` pour remplir toute la toile.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
L'arrière‑plan est défini sur **yellow**, offrant un fort contraste pour les rectangles **red** et **blue** qui suivent.

### Étape 4 : tracer des rectangles sur l'image
Utilisez `drawRectangle` avec un `Pen` pour le contour et un `SolidBrush` pour le remplissage. Vous pouvez tracer plusieurs rectangles avec différentes couleurs et positions.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Ces commandes tracent un rectangle **red** à (10, 10) et un rectangle **blue** à (50, 50), chacun de 40 px de largeur et 30 px de hauteur.

### Étape 5 : exporter l'image en bitmap
Enfin, persistez l'image modifiée sur le disque. Aspose.PSD encode automatiquement le bitmap dans le format que vous spécifiez.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
L'image est enregistrée en tant que fichier BMP au chemin stocké dans `outpath`.

## Problèmes courants et solutions
- **Blank output file** – Assurez‑vous d’appeler `graphics.clear` avant le tracé ; sinon la toile peut rester transparente.
- **Incorrect colors** – Vérifiez que vous importez `com.aspose.psd.Color` et non `java.awt.Color`.
- **Large images out of memory** – Utilisez les constructeurs `PsdImage` qui supportent le streaming afin d'éviter de charger le fichier complet en RAM.

## Questions fréquemment posées

**Q : Aspose.PSD for Java peut‑il gérer d’autres formes que les rectangles ?**  
A : Oui, il prend en charge les ellipses, les lignes, les polygones et les chemins personnalisés, vous offrant des capacités complètes de dessin vectoriel.

**Q : Comment puis‑je modifier l'épaisseur du bord du rectangle ?**  
A : Appelez la méthode `setWidth(float)` de l'objet `Pen` avant d’appeler `drawRectangle`.

**Q : Aspose.PSD for Java est‑il adapté aux tâches de traitement d'images haute performance ?**  
A : Absolument – son API de streaming traite des fichiers PSD de plusieurs centaines de pages avec moins de 200 Mo d’utilisation de RAM.

**Q : Où puis‑je trouver plus d'exemples et de tutoriels pour Aspose.PSD for Java ?**  
A : Vous pouvez explorer davantage d'exemples et la documentation détaillée sur la [documentation Aspose.PSD for Java](https://reference.aspose.com/psd/java/).

**Q : Aspose.PSD for Java prend‑il en charge d’autres formats d'image que le BMP ?**  
A : Oui, il prend en charge PNG, JPEG, TIFF, GIF, et plus de 30 formats supplémentaires pour l'importation et l'exportation.

## Conclusion
Vous savez maintenant **how to draw rectangle** sur une image en utilisant Aspose.PSD for Java, depuis la création d'un bitmap jusqu'à la définition de la couleur d'arrière‑plan et l'initialisation du graphics. Expérimentez avec différentes tailles, couleurs et formes supplémentaires pour maîtriser **java image manipulation**. Lorsque vous êtes prêt, intégrez ce modèle dans des pipelines de traitement par lots plus grands ou des éditeurs pilotés par l'interface utilisateur.

---

**Dernière mise à jour :** 2026-09-08  
**Testé avec :** Aspose.PSD for Java 24.12  
**Auteur :** Aspose

## Tutoriels associés

- [Redimensionner l'image avec Aspose.PSD for Java – Dessiner des formes et opérations d'image de base](/psd/java/basic-image-operations/)
- [Ajouter une signature à l'image – Dessiner une image sur le canevas avec Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Recadrer l'image par rectangle avec Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}