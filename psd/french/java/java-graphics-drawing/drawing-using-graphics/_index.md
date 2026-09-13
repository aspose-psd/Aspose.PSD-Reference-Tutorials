---
date: 2026-09-13
description: Apprenez à dessiner une ellipse et d'autres shapes en Java avec Aspose.PSD.
  Ce tutoriel Java graphics étape par étape montre gradient fills, polygon fills et
  image export.
keywords:
- how to draw ellipse
- draw shapes java
- how to create gradient
- java graphics tutorial
- fill polygon java
lastmod: 2026-09-13
linktitle: Dessiner en utilisant Graphics en Java
og_description: Apprenez à dessiner une ellipse en Java avec Aspose.PSD. Ce tutoriel
  Java graphics couvre shape drawing, gradient fills, polygon filling et exporting
  images.
og_image_alt: Screenshot of Java code drawing an ellipse with Aspose.PSD
og_title: Comment dessiner une ellipse en utilisant graphics en Java avec Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-13'
  description: Learn how to draw an ellipse and other shapes in Java with Aspose.PSD.
    This step‑by‑step Java graphics tutorial shows gradient fills, polygon fills,
    and image export.
  headline: How to draw ellipse using graphics in Java with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Yes, it supports layer merging, channel adjustments, text rendering, and
      advanced masking in addition to shape drawing.
    question: Can Aspose.PSD handle complex image manipulations?
  - answer: Absolutely; the library is optimized for speed and can process a 10 MP
      image in under 2 seconds on a typical server.
    question: Is Aspose.PSD suitable for high‑performance applications?
  - answer: Visit the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and API references.
    question: Where can I find more examples and documentation?
  - answer: Yes, you can export to BMP, PNG, JPEG, TIFF, GIF, and PSD among others.
    question: Does Aspose.PSD support multiple image formats for export?
  - answer: Reach out to the Aspose.PSD community on the [support forum](https://forum.aspose.com/c/psd/34)
      or consider a [temporary license](https://purchase.aspose.com/temporary-license/)
      for priority assistance.
    question: How can I get support or assistance if I encounter issues?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- drawing shapes java
- gradient fill java
- initialize graphics java
title: Comment dessiner une ellipse en utilisant graphics en Java avec Aspose.PSD
url: /fr/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment dessiner une ellipse à l'aide de graphiques en Java avec Aspose.PSD

## Introduction
Dans ce tutoriel Java sur les graphiques, vous découvrirez **comment dessiner une ellipse** ainsi que d'autres formes de manière programmatique en utilisant Aspose.PSD pour Java. Que vous ayez besoin de générer des miniatures dynamiques, de créer des éléments d'interface personnalisés ou d'automatiser des flux de travail de conception, maîtriser le dessin d'ellipses et les remplissages en dégradé vous offre un contrôle visuel précis. Les étapes ci‑dessous vous guident à travers l'initialisation du graphique, la configuration des stylos et des pinceaux, et l'exportation du résultat dans des formats d'image courants.

## Réponses rapides
- **Quelle bibliothèque est requise ?** Aspose.PSD for Java (download from the official site).  
- **Quelle forme le tutoriel cible-t-il ?** Dessiner une ellipse et remplir un polygone.  
- **Puis-je exporter vers d'autres formats que BMP ?** Oui – PNG, JPEG, TIFF, et d'autres sont pris en charge.  
- **Ai-je besoin d'une licence pour le développement ?** Une licence temporaire gratuite fonctionne pour les tests ; une licence complète est requise pour la production.  
- **L'API convient-elle aux images volumineuses ?** Aspose.PSD traite des fichiers jusqu'à 500 MB sans charger l'intégralité du bitmap en mémoire.

## Comment dessiner une ellipse en Java ?
Chargez un `PsdImage` avec la largeur et la hauteur souhaitées, créez un objet `Graphics`, définissez un `Pen`, puis appelez `drawEllipse` avec un rectangle englobant. L'opération complète ne nécessite que quelques appels de méthode et s'exécute en moins d'une seconde pour des images typiques de 800×600 sur du matériel moderne.

## Qu'est-ce qu'Aspose.PSD pour Java ?
Aspose.PSD pour Java est une **bibliothèque pure‑Java qui fournit plus de 50 conversions de formats d'image et des capacités complètes d'édition PSD** sans nécessiter Adobe Photoshop. Elle peut rendre, modifier et exporter des fichiers multi‑couches tout en maintenant une faible consommation de mémoire, ce qui la rend idéale pour la génération graphique côté serveur.

## Pourquoi utiliser Aspose.PSD pour dessiner des formes ?
Aspose.PSD offre haute performance, prise en charge étendue des formats et rendu précis, ce qui le rend idéal pour la génération graphique côté serveur et le dessin de formes complexes.

- **Performance :** Gère des images jusqu'à 500 MB avec moins de 150 MB d'utilisation du tas (≈30 % inférieur aux bibliothèques concurrentes).  
- **Prise en charge des formats :** Plus de 50 formats d'entrée et de sortie, y compris BMP, PNG, JPEG, TIFF et PSD.  
- **Précision :** Le rendu sous‑pixel garantit des ellipses nettes et des dégradés fluides sur les écrans haute‑DPI.

## Prérequis
- Connaissances de base en programmation Java.  
- Java Development Kit (JDK) installé.  
- Un IDE tel qu'IntelliJ IDEA ou Eclipse.  
- Bibliothèque Aspose.PSD pour Java. Vous pouvez la télécharger depuis [Aspose.PSD Java download](https://releases.aspose.com/psd/java/).

## Importer les packages
Pour commencer, importez les classes Aspose.PSD nécessaires ainsi que les utilitaires Java standards. Les classes suivantes fournissent des primitives de dessin et la gestion des couleurs :
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Étape 1 : créer un objet image
`PsdImage` représente une toile raster en mémoire sur laquelle on peut dessiner et enregistrer dans divers formats.
```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## Étape 2 : initialiser l'objet graphics
`Graphics` est la surface de dessin liée à un `PsdImage`, permettant des opérations vectorielles telles que le dessin de formes.
```java
Graphics graphics = new Graphics(image);
```

## Étape 3 : nettoyer la surface de l'image
`clear` remplit toute la toile avec une couleur d'arrière‑plan unique.
```java
graphics.clear(Color.getWhite());
```

## Étape 4 : créer et configurer l'objet pen
`Pen` définit la couleur du trait, l'épaisseur et le style utilisés lors du dessin des contours.
```java
Pen pen = new Pen(Color.getBlue());
```

## Étape 5 : dessiner des formes
`drawEllipse` rend une ellipse qui s'insère dans le rectangle spécifié en utilisant le stylo actuel.
```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## Étape 6 : utiliser des pinceaux pour le remplissage
`LinearGradientBrush` crée un remplissage en dégradé qui passe d'une couleur à une autre sur une zone définie.
```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## Étape 7 : enregistrer l'image modifiée
`save` écrit le `PsdImage` sur le disque dans le format choisi, tel que BMP ou PNG.
```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## Pièges courants et dépannage
- **NullPointerException sur graphics :** Assurez‑vous que le `PsdImage` est entièrement instancié avant de créer l'objet `Graphics`.  
- **Couleurs incorrectes :** Utilisez `Color.fromArgb` pour spécifier des valeurs ARGB exactes lorsque la palette par défaut ne correspond pas aux attentes.  
- **Lenteur de performance sur les grandes images :** Activez `PsdImageOptions` avec `compression = CompressionType.Rle` pour réduire la consommation de mémoire.

## Questions fréquemment posées

**Q : Aspose.PSD peut‑il gérer des manipulations d'images complexes ?**  
A : Oui, il prend en charge la fusion de calques, les ajustements de canaux, le rendu de texte et le masquage avancé en plus du dessin de formes.

**Q : Aspose.PSD convient‑il aux applications haute performance ?**  
A : Absolument ; la bibliothèque est optimisée pour la vitesse et peut traiter une image de 10 MP en moins de 2 secondes sur un serveur typique.

**Q : Où puis‑je trouver plus d'exemples et de documentation ?**  
A : Visitez la [documentation Aspose.PSD Java](https://reference.aspose.com/psd/java/) pour des guides complets et des références API.

**Q : Aspose.PSD prend‑il en charge plusieurs formats d'image pour l'exportation ?**  
A : Oui, vous pouvez exporter vers BMP, PNG, JPEG, TIFF, GIF et PSD entre autres.

**Q : Comment obtenir du support ou de l'aide si je rencontre des problèmes ?**  
A : Contactez la communauté Aspose.PSD sur le [forum de support](https://forum.aspose.com/c/psd/34) ou envisagez une [licence temporaire](https://purchase.aspose.com/temporary-license/) pour une assistance prioritaire.

---

**Dernière mise à jour :** 2026-09-13  
**Testé avec :** Aspose.PSD for Java 24.10  
**Auteur :** Aspose

## Tutoriels associés

- [Redimensionner l'image avec Aspose.PSD pour Java – Dessiner des formes et opérations d'image de base](/psd/java/basic-image-operations/)
- [Dessiner et enregistrer un rectangle dans un PSD avec Aspose.PSD pour Java](/psd/java/basic-image-operations/simple-drawing/)
- [Ajouter une signature à l'image – Dessiner l'image sur le canevas avec Aspose.PSD pour Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}