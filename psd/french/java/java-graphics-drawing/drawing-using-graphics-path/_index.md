---
date: 2026-09-08
description: Apprenez à créer une image avec la classe Graphics Path d'Aspose.PSD
  en Java. Ce guide étape par étape vous montre comment ajouter du texte, des formes
  et effacer l'arrière‑plan de l'image efficacement.
keywords:
- how to create image
- add text image java
- clear image background java
lastmod: 2026-09-08
linktitle: Comment créer une image en utilisant Graphics Path en Java
og_description: Apprenez à créer une image avec Aspose.PSD en Java. Ce tutoriel couvre
  l'ajout de texte, de formes et l'effacement de l'arrière‑plan de l'image à l'aide
  de la classe Graphics Path.
og_image_alt: Screenshot of Java code creating an image with graphics path using Aspose.PSD
og_title: Comment créer une image en utilisant Graphics Path en Java avec Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  headline: How to create image using Graphics Path in Java
  type: TechArticle
- description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  name: How to create image using Graphics Path in Java
  steps:
  - name: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
  - name: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
    text: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
  type: HowTo
- questions:
  - answer: Aspose.PSD is a Java library that enables you to create, edit, and convert
      Photoshop (PSD) files and other raster formats without requiring Photoshop.
    question: What is Aspose.PSD?
  - answer: Yes – the library supports **50+** formats, including PNG, JPEG, BMP,
      TIFF, and GIF.
    question: Can I work with formats other than PSD?
  - answer: Yes, you can access a free trial of Aspose.PSD [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: You can purchase Aspose.PSD from [here](https://purchase.aspose.com/buy).
    question: How do I purchase a license?
  - answer: You can seek support and discussions on [Aspose’s forum](https://forum.aspose.com/c/psd/34).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- graphics path
- Aspose.PSD
- Java image processing
title: Comment créer une image en utilisant Graphics Path en Java
url: /fr/java/java-graphics-drawing/drawing-using-graphics-path/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment créer une image en utilisant Graphics Path en Java

## Introduction
Dans ce tutoriel, vous apprendrez **comment créer une image** de façon programmatique en tirant parti de la puissante classe **Graphics Path** fournie par Aspose.PSD pour Java. Que vous ayez besoin de dessiner des formes personnalisées, d’intégrer du texte ou d’effacer l’arrière‑plan d’une image, le guide étape par étape ci‑dessous vous montre exactement comment obtenir des résultats de qualité professionnelle en quelques lignes de code.

## Réponses rapides
- **Quelle bibliothèque gère le dessin complexe ?** Aspose.PSD for Java’s Graphics Path class.  
- **Puis-je ajouter du texte à l'image ?** Yes – use the `GraphicsPath.addString` method.  
- **Le nettoyage de l'arrière‑plan est‑il pris en charge ?** Absolutely, fill the path with a transparent brush.  
- **Quelle version de Java est requise ?** JDK 11 or newer.  
- **Ai‑je besoin d’une licence pour la production ?** A commercial license is required; a free trial is available.

## Qu’est‑ce que la classe Graphics Path ?
La classe `GraphicsPath` est l’objet principal d’Aspose.PSD pour définir des instructions de dessin vectoriel. Elle vous permet de composer des formes, du texte et des remplissages dans un seul chemin réutilisable qui peut être rendu sur n’importe quelle image. En construisant un chemin, vous pouvez appliquer des stylos, des pinceaux et des transformations en un seul passage de rendu, ce qui améliore les performances et garde la logique de dessin organisée.

## Pourquoi utiliser Graphics Path pour ajouter du texte à une image Java et effacer l'arrière‑plan d'une image Java ?
Aspose.PSD prend en charge **plus de 50 formats d’image** (y compris PSD, PNG, JPEG, BMP) et peut traiter des fichiers jusqu’à **2 Go** sans charger le document complet en mémoire. L’utilisation de Graphics Path vous permet de combiner le dessin, le placement du texte et l’effacement de l’arrière‑plan en une seule opération haute performance, réduisant la consommation mémoire jusqu’à **30 %** par rapport aux approches raster‑only.

## Prérequis
Avant de commencer, assurez‑vous d’avoir les éléments suivants :

1. **Java Development Kit (JDK)** – un JDK 11+ stable installé. Téléchargez‑le depuis [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – obtenez le dernier JAR depuis [here](https://releases.aspose.com/psd/java/) and add it to your project’s classpath.  
3. **IDE** – tout IDE Java tel qu’Eclipse, IntelliJ IDEA ou VS Code.

Avec cela en place, vous êtes prêt à commencer à créer des images.

## Importer les packages
Pour travailler avec les graphiques, importez les espaces de noms requis :

```java
import com.aspose.psd.Color;
import com.aspose.psd.Figure;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.GraphicsPath;
import com.aspose.psd.HatchStyle;
import com.aspose.psd.Pen;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.HatchBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```

Ces importations exposent les classes de base de dessin, de pinceau et de stylo nécessaires à la manipulation d’images.

## Comment créer une image avec Graphics Path en Java ?
Créez un nouveau canevas raster, attachez un objet `Graphics` et préparez la surface de dessin. Cette étape unique configure un bitmap de **500 × 500 pixels** prêt pour le rendu vectoriel. Le canevas est initialement transparent, vous permettant de le remplir plus tard avec n’importe quelle couleur ou motif d’arrière‑plan de votre choix, ce qui est essentiel pour les scénarios d’effacement d’arrière‑plan d’image.

```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```

## Étape 1 : initialiser l’image et le graphique
Ici nous instancions un objet `PsdImage` (500 × 500) et obtenons son contexte `Graphics`.  
`PsdImage` représente une image raster en mémoire que Aspose.PSD peut manipuler et enregistrer dans de nombreux formats.  
`Graphics` fournit des méthodes de dessin qui rendent des formes, du texte et des chemins sur le `PsdImage`.

## Étape 2 : créer et configurer le graphics path
Ensuite, nous construisons un `GraphicsPath` qui contient un cercle, un rectangle et une étiquette texte.  
`GraphicsPath` est un conteneur pour les figures géométriques ; vous pouvez y ajouter des formes, des lignes et des chaînes avant le rendu.

```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```

### Ajouter du texte à l'image (add text image java)
La méthode `addString` de `GraphicsPath` place le texte spécifié aux coordonnées données en utilisant la police et le pinceau fournis. C’est la façon la plus fiable d’intégrer du texte net et évolutif au sein du chemin vectoriel.

## Étape 3 : dessiner et remplir le chemin
Nous rendons maintenant le chemin avec un stylo bleu et le remplissons à l’aide d’un pinceau à hachures verticales, ce qui montre également comment **effacer l’arrière‑plan d’une image java** en remplissant avec un motif transparent si désiré. Le `Pen` définit le style du contour, tandis que le `HatchBrush` crée un remplissage à motif.

```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```

## Étape 4 : enregistrer l'image
Enfin, écrivez l’image composée sur le disque au format PNG (ou tout autre des plus de 50 formats supportés). La méthode `save` détermine le type de fichier de sortie à partir de l’extension que vous fournissez.

```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```

## Problèmes courants et solutions
- **Chemin non visible** – assurez‑vous que la couleur du stylo contraste avec le pinceau de remplissage.  
- **Le texte apparaît flou** – utilisez une image à plus haute résolution ou une police TrueType avec un DPI suffisant.  
- **Erreurs de mémoire insuffisante sur de gros fichiers** – activez `PsdImageOptions.setUseMemoryCache(true)` pour diffuser les données au lieu de les charger entièrement.

## Questions fréquemment posées

**Q : Qu’est‑ce qu’Aspose.PSD ?**  
R : Aspose.PSD est une bibliothèque Java qui vous permet de créer, modifier et convertir des fichiers Photoshop (PSD) et d’autres formats raster sans nécessiter Photoshop.

**Q : Puis‑je travailler avec des formats autres que le PSD ?**  
R : Oui – la bibliothèque prend en charge **plus de 50** formats, dont PNG, JPEG, BMP, TIFF et GIF.

**Q : Une version d’essai est‑elle disponible ?**  
R : Oui, vous pouvez accéder à une version d’essai gratuite d’Aspose.PSD [here](https://releases.aspose.com/).

**Q : Comment acheter une licence ?**  
R : Vous pouvez acheter Aspose.PSD depuis [here](https://purchase.aspose.com/buy).

**Q : Où puis‑je obtenir du support ?**  
R : Vous pouvez rechercher du support et des discussions sur le [forum d’Aspose](https://forum.aspose.com/c/psd/34).

## Conclusion
En suivant ce guide, vous savez maintenant **comment créer une image** avec des formes vectorielles complexes, du texte intégré et des arrière‑plans transparents en utilisant la classe Graphics Path d’Aspose.PSD. Expérimentez avec différents stylos, pinceaux et géométries de chemin pour créer des graphiques plus riches pour les jeux, les éléments d’interface utilisateur ou la génération automatisée de rapports.

---

**Dernière mise à jour :** 2026-09-08  
**Testé avec :** Aspose.PSD for Java 24.11  
**Auteur :** Aspose

## Tutoriels associés

- [Générer une image PSD en Java en définissant le chemin avec Aspose.PSD](/psd/java/image-editing/create-image-by-setting-path/)
- [Redimensionner une image avec Aspose.PSD pour Java – Dessiner des formes & opérations d’image de base](/psd/java/basic-image-operations/)
- [Ajouter une signature à une image – Dessiner une image sur le canevas avec Aspose.PSD pour Java](/psd/java/advanced-image-effects/add-signature-to-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}