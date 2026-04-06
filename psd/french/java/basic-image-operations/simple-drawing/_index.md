---
date: 2025-12-27
description: Apprenez à dessiner un rectangle rouge et d’autres formes dans les fichiers
  PSD à l’aide d’Aspose.PSD pour Java. Ce guide étape par étape couvre la création
  de documents, l’ajout de calques et le dessin avec des exemples de code.
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Dessiner un rectangle rouge avec Aspose.PSD pour Java
url: /fr/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dessiner un rectangle rouge avec Aspose.PSD pour Java

## Introduction

Bienvenue dans ce guide étape par étape sur la façon de **dessiner un rectangle rouge** en utilisant Aspose.PSD pour Java ! Dans ce tutoriel, nous allons créer un nouveau document PSD, ajouter un calque et dessiner des formes avec des couleurs personnalisées. Que vous automatisiez des graphiques ou construisiez un backend d'outil de conception, ce tutoriel vous fournit les blocs de construction essentiels.

## Réponses rapides
- **Quelle est la classe principale pour créer un fichier PSD?** `PsdImage`
- **Quelle méthode effacer la couleur d'arrière‑plan d'un calque?** `Graphics.clear(Color)`
- **Comment dessiner un rectangle rouge?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Ai‑je besoin d’une licence pour le développement?** Un essai gratuit suffit pour les tests; une licence est requise pour la production.
- **Puis‑je manipuler des fichiers PSD existants avec la même API ?** Oui, Aspose.PSD prend en charge l'édition complète des PSD.

## Qu'est-ce que dessiner un rectangle rouge dans un fichier PSD ?
Dessiner un rectangle rouge signifie utiliser l'objet `Graphics` pour rendre une forme rectangulaire remplie ou bordée avec la couleur rouge sur un calque spécifique d'une image PSD. Cette opération est courante pour mettre en évidence des zones, créer des espaces réservés ou ajouter des graphiques simples de manière programmatique.

## Pourquoi utiliser Aspose.PSD pour Java pour manipuler des fichiers PSD ?
Aspose.PSD fournit une API pure Java qui vous permet de lire, modifier et écrire des fichiers Photoshop PSD sans nécessiter l'installation de Photoshop. Elle prend en charge la gestion des calques, la manipulation des couleurs et le dessin vectoriel, ce qui la rend idéale pour le traitement d'images côté serveur, les pipelines d'actifs automatisés et la génération de graphiques personnalisés.

## Prérequis

- Kit de développement Java (JDK) installé sur votre machine.
- Bibliothèque Aspose.PSD pour Java. Vous pouvez la télécharger depuis la [Documentation Aspose.PSD pour Java](https://reference.aspose.com/psd/java/).

## Importer des packages

Pour commencer, importez les classes requises dans votre projet Java :

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Étape 1 : Créer un nouveau document

Tout d'abord, créez un document PSD vierge avec la taille de canevas souhaitée. Ce document hébergera le calque sur lequel nous dessinerons.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Étape 2 : Ajouter un calque

Ensuite, ajoutez un nouveau calque vierge qui couvre toute la largeur et la hauteur de l'image. Les calques sont essentiels pour séparer les opérations de dessin.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Étape 3 : Dessiner des formes

Nous utiliserons la classe `Graphics` pour manipuler les données de pixels du calque. Voici trois exemples illustrant la suppression de l'arrière‑plan et le dessin de rectangles avec différentes couleurs.

### Effacer la couleur du calque (définir le fond en jaune)

Effacer la couleur du calque (définir l'arrière‑plan en jaune)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Dessiner un rectangle rouge (élément principal)

Dessiner un rectangle rouge (objectif principal)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Dessiner un rectangle bleu (exemple supplémentaire)

Dessiner un rectangle bleu (exemple supplémentaire)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Étape 4 : Enregistrer les modifications

Enfin, écrivez l'image PSD modifiée sur le disque. Le fichier contiendra le nouveau calque et les formes dessinées.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Problèmes courants et solutions

- **Le calque n'est pas visible après le dessin** : assurez-vous que le calque est ajouté à l'image **avant** de créer l'objet `Graphics`.
- **Les couleurs apparaissent incorrectes** : vérifiez que vous utilisez `Color.getRed()` (ou d'autres méthodes statiques) plutôt que des valeurs RGB personnalisées qui pourraient être hors limites.
- **Le fichier n'est pas enregistré** : confirmez que le chemin `outputDir` existe et que l'application possède les permissions d'écriture.

## Questions fréquemment posées

### Q1 : Puis-je utiliser Aspose.PSD pour Java pour manipuler des fichiers PSD existants ?

**Q1 : Puis‑je utiliser Aspose.PSD pour Java afin de manipuler des fichiers PSD existants ?**
Oui, Aspose.PSD pour Java fournit une fonctionnalité étendue pour éditer et manipuler des fichiers PSD existants.

### Q2 : Où puis-je trouver de l'assistance pour Aspose.PSD pour Java ?

**Q2 : Où puis‑je trouver du support pour Aspose.PSD pour Java ?**
Vous pouvez visiter le [Forum Aspose.PSD pour Java](https://forum.aspose.com/c/psd/34) pour toute question liée au support.

### Q3 : Existe-t-il un essai gratuit disponible pour Aspose.PSD pour Java ?

**Q3 : Existe‑t‑il une version d'essai gratuite pour Aspose.PSD pour Java ?**
Oui, vous pouvez accéder à la version d'essai gratuite [ici](https://releases.aspose.com/).

### Q4 : Comment puis-je acheter une licence pour Aspose.PSD pour Java ?

**Q4 : Comment puis‑je acheter une licence pour Aspose.PSD pour Java?**
Vous pouvez acheter une licence depuis la [Page d'achat Aspose.PSD](https://purchase.aspose.com/buy).

### Q5 : Des licences temporaires sont-elles disponibles pour Aspose.PSD pour Java ?

**Q5 : Des licences temporaires sont‑elles disponibles pour Aspose.PSD pour Java ?**
Oui, vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

## Questions fréquemment posées supplémentaires

**Q: Puis‑je dessiner d'autres formes que des rectangles ?**
R : Oui, la classe `Graphics` prend également en charge le dessin d'ellipses, de lignes et de chemins personnalisés.

**Q : Aspose.PSD prend‑il en charge la transparence dans les formes dessinées ?**
R : Absolument ; vous pouvez utiliser `SolidBrush` avec une couleur ARGB pour inclure la transparence alpha.

**Q : Est-il possible de modifier l'opacité d'un calque ?**
R : Oui, chaque objet `Layer` possède une méthode `setOpacity` qui accepte une valeur de 0 à 255.

**Q : Comment charger un fichier PSD existant au lieu d'en créer un nouveau ?**
R : Utilisez `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` avant de manipuler les calques.

## Conclusion

Vous avez maintenant appris comment **dessiner un rectangle rouge** et d'autres formes de base dans un fichier PSD en utilisant Aspose.PSD pour Java. En créant un document, en ajoutant un calque, en effaçant son arrière-plan et en dessinant avec l'API `Graphics`, vous pouvez automatiser de nombreuses tâches de conception graphique. Explorez davantage en expérimentant avec différents pinceaux, effets de calque et formats de fichier.

---

**Dernière mise à jour :** 2025-12-27
**Testé avec :** Aspose.PSD pour Java 24.12 (dernière version au moment de la rédaction)
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}