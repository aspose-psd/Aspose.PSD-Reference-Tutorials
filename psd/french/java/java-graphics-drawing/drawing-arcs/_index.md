---
date: 2026-09-03
description: Apprenez comment java graphics dessiner un arc en utilisant Aspose.PSD
  for Java. Guide étape par étape avec des extraits de code pour créer des arcs dans
  des fichiers PSD.
keywords:
- java graphics draw arc
- how to draw arcs java
- Aspose.PSD arc drawing
lastmod: 2026-09-03
linktitle: Dessiner des arcs en Java
og_description: Apprenez comment java graphics dessiner un arc avec Aspose.PSD for
  Java. Ce tutoriel présente les prérequis, les étapes de code et des astuces pour
  créer des arcs dans des fichiers PSD.
og_image_alt: Screenshot of a Java program drawing an arc using Aspose.PSD
og_title: Comment java graphics dessiner un arc en Java – guide Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  headline: How to java graphics draw arc in Java
  type: TechArticle
- description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  name: How to java graphics draw arc in Java
  steps:
  - name: set up your Java project
    text: Create a new Java project in your favourite IDE and add the Aspose.PSD JAR
      to the build path. Ensure the JAR is referenced correctly so the compiler can
      locate the library classes.
  - name: import required packages
    text: 'To begin, import the necessary packages from Aspose.PSD for Java: The `Pen`
      class defines the colour, width, and style of the line used to draw the arc.
      These imports expose the `PsdImage`, `Graphics`, `Pen`, and colour classes needed
      for arc drawing.'
  - name: initialise image and graphics objects
    text: 'Create an instance of `PsdImage` and obtain a `Graphics` object to draw
      on: Replace `"Your Document Directory"` with the folder where you want the output
      files saved.'
  - name: define arc parameters
    text: 'Set the geometry and style of the arc—its bounding rectangle, start angle,
      sweep angle, colour, and thickness: Adjust the values to match the visual design
      you need; for example, a 200 px radius arc starting at 45° and sweeping 270°.'
  - name: draw the arc and save the image
    text: 'Invoke `drawArc` on the `Graphics` object and persist the PSD (or export
      to another format): The `drawArc` method of the `Graphics` class renders an
      arc defined by a bounding rectangle, start angle, and sweep angle using the
      specified `Pen`. The snippet draws the arc on the canvas and saves it as a '
  type: HowTo
- questions:
  - answer: Yes, the library can draw rectangles, ellipses, lines, polygons, and custom
      paths using the same `Graphics` API.
    question: Can Aspose.PSD for Java handle other shapes besides arcs?
  - answer: Create a `Pen` with the desired `Color` and width, then pass that `Pen`
      instance to `drawArc`.
    question: How do I change the arc colour and thickness?
  - answer: Absolutely. Aspose.PSD supports PNG, JPEG, TIFF, GIF and many more – just
      change the file extension in the `save` method.
    question: Is it possible to export the PSD to a format other than BMP?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for tutorials,
      code samples, and assistance from other developers.
    question: Where can I find more examples and community support?
  - answer: Yes, it can process files up to 2 GB and render arcs without loading the
      entire document into memory, thanks to its streaming architecture.
    question: Does the library work with large PSD files?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- arc drawing
- PSD manipulation
title: Comment dessiner un arc avec java graphics en Java
url: /fr/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment dessiner un arc avec Java graphics en Java

## Introduction
Dans ce tutoriel, vous découvrirez comment **java graphics draw arc** en utilisant la bibliothèque Aspose.PSD for Java. Dessiner des arcs de manière programmatique est une exigence courante pour les composants d'interface personnalisés, les visualisations de données et les rapports riches en graphiques. Aspose.PSD for Java vous donne un contrôle total sur les fichiers PSD (Photoshop Document), vous permettant de créer, modifier et exporter des images sans avoir Photoshop installé.

## Réponses rapides
- **Quelle bibliothèque prend en charge le dessin d'arc en Java ?** Aspose.PSD for Java.
- **Ai-je besoin d'une licence pour une utilisation en production ?** Oui, une licence commerciale est requise pour les déploiements non‑essai.
- **Quels formats de fichiers puis‑je exporter ?** BMP, PNG, JPEG, TIFF, GIF et plus.
- **Puis‑je changer l'épaisseur et la couleur de l'arc ?** Oui, via l'objet `Pen` passé à `drawArc`.
- **L'API est‑elle compatible avec Java 8 et versions ultérieures ?** Entièrement compatible avec Java 8‑21.

## Qu'est-ce que Java graphics draw arc ?
`java graphics draw arc` désigne le processus de rendu d'un segment de ligne courbe — un arc — sur une surface graphique en utilisant les API de dessin de Java. Dans le contexte d'Aspose.PSD, l'opération est effectuée sur un objet `Graphics` qui représente un calque à l'intérieur d'un fichier PSD.

## Pourquoi utiliser Aspose.PSD for Java pour dessiner des arcs ?
Aspose.PSD prend en charge **plus de 50** formats d'images et de documents, peut gérer des fichiers PSD d'**jusqu'à 2 Go** et traite des documents de plusieurs centaines de pages sans charger le fichier complet en mémoire. Cette performance quantifiée le rend idéal pour la génération de graphiques côté serveur où la vitesse et l'utilisation de la mémoire sont essentielles.

## Prérequis
1. **Environnement de développement Java** – Installez Java depuis le [site d'Oracle](https://www.oracle.com/java/).  
2. **Bibliothèque Aspose.PSD for Java** – Téléchargez le dernier JAR depuis la [page de téléchargement](https://releases.aspose.com/psd/java/). Suivez les instructions fournies pour ajouter le JAR au classpath de votre projet.

## Comment Java graphics draw arc en Java ?
Chargez un nouveau `PsdImage`, obtenez sa surface `Graphics`, configurez un `Pen` avec la couleur et l'épaisseur souhaitées, puis appelez `drawArc`. Cette séquence concise crée l'arc et enregistre le résultat dans une chaîne de méthodes unique. En ajustant le rectangle englobant et les paramètres d'angle, vous pouvez contrôler la taille, la position et l'étendue de l'arc pour répondre aux exigences de votre conception.

### Étape 1 : configurez votre projet Java
Créez un nouveau projet Java dans votre IDE préféré et ajoutez le JAR Aspose.PSD au chemin de construction. Assurez‑vous que le JAR est correctement référencé afin que le compilateur puisse localiser les classes de la bibliothèque.

### Étape 2 : importez les packages requis
Pour commencer, importez les packages nécessaires d'Aspose.PSD for Java :
La classe `Pen` définit la couleur, la largeur et le style de la ligne utilisée pour dessiner l'arc.
```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```  
Ces importations exposent les classes `PsdImage`, `Graphics`, `Pen` et les classes de couleur nécessaires au dessin d'arc.

### Étape 3 : initialisez les objets image et graphics
Créez une instance de `PsdImage` et obtenez un objet `Graphics` sur lequel dessiner :
```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```  
Remplacez `"Your Document Directory"` par le dossier où vous souhaitez enregistrer les fichiers de sortie.

### Étape 4 : définissez les paramètres de l'arc
Définissez la géométrie et le style de l'arc — son rectangle englobant, l'angle de départ, l'angle de balayage, la couleur et l'épaisseur :
```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```  
Ajustez les valeurs pour correspondre au design visuel souhaité ; par exemple, un arc de rayon 200 px commençant à 45° et balayant 270°.

### Étape 5 : dessinez l'arc et enregistrez l'image
Appelez `drawArc` sur l'objet `Graphics` et persistez le PSD (ou exportez-le dans un autre format) :
La méthode `drawArc` de la classe `Graphics` rend un arc défini par un rectangle englobant, un angle de départ et un angle de balayage en utilisant le `Pen` spécifié.
```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```  
L'extrait dessine l'arc sur le canevas et l'enregistre sous forme de fichier BMP. Modifiez l'extension du fichier dans `outputPath` pour exporter en PNG, JPEG ou TIFF.

## Pièges courants et dépannage
- **Unités d'angle incorrectes** – Aspose.PSD attend des angles en degrés, pas en radians. Fournir des radians produira des résultats inattendus.
- **Épaisseur du Pen trop grande** – Des stylos très épais peuvent faire dépasser l'arc des limites de l'image ; réduisez l'épaisseur ou agrandissez le canevas.
- **Problèmes de chemin de fichier** – Utilisez des chemins absolus ou assurez‑vous que le répertoire de travail a les permissions d'écriture pour éviter `IOException`.

## Questions fréquemment posées

**Q : Aspose.PSD for Java peut‑il gérer d'autres formes que les arcs ?**  
R : Oui, la bibliothèque peut dessiner des rectangles, des ellipses, des lignes, des polygones et des chemins personnalisés en utilisant la même API `Graphics`.

**Q : Comment changer la couleur et l'épaisseur de l'arc ?**  
R : Créez un `Pen` avec le `Color` et la largeur souhaités, puis passez cette instance de `Pen` à `drawArc`.

**Q : Est‑il possible d'exporter le PSD dans un format autre que BMP ?**  
R : Absolument. Aspose.PSD prend en charge PNG, JPEG, TIFF, GIF et bien d'autres – il suffit de changer l'extension du fichier dans la méthode `save`.

**Q : Où puis‑je trouver plus d'exemples et de support communautaire ?**  
R : Consultez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour des tutoriels, des exemples de code et de l'aide d'autres développeurs.

**Q : La bibliothèque fonctionne‑t‑elle avec de gros fichiers PSD ?**  
R : Oui, elle peut traiter des fichiers jusqu'à 2 Go et rendre des arcs sans charger le document complet en mémoire, grâce à son architecture de streaming.

---

**Dernière mise à jour :** 2026-09-03  
**Testé avec :** Aspose.PSD for Java 24.11  
**Auteur :** Aspose

## Tutoriels associés

- [Dessiner et enregistrer un rectangle dans un PSD avec Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [Redimensionner une image avec Aspose.PSD for Java – Dessiner des formes & opérations d'image de base](/psd/java/basic-image-operations/)
- [Comment changer la couleur du trait Java en utilisant Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}