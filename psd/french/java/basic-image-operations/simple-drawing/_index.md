---
date: 2026-06-13
description: Apprenez à dessiner un rectangle dans des fichiers PSD en utilisant Aspose.PSD
  for Java. Ce guide montre du code étape par étape, l'ajout de calques, le traitement
  d'images côté serveur et le dessin de formes.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: Effectuer un dessin simple
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Comment dessiner un rectangle dans un PSD avec Aspose.PSD for Java
url: /fr/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment dessiner un rectangle dans un PSD avec Aspose.PSD pour Java

## Introduction

Dans ce tutoriel, vous découvrirez **comment dessiner un rectangle** à l’intérieur d’un fichier Photoshop PSD en utilisant la bibliothèque pure‑Java Aspose.PSD. Que vous construisiez une chaîne d’outils côté serveur, automatisiez la création de vignettes ou ajoutiez des graphiques dynamiques à des conceptions existantes, les étapes ci‑dessous vous offrent une solution complète, prête pour la production. Nous couvrirons la création d’un nouveau document PSD, l’ajout d’un calque, l’effacement de l’arrière‑plan, puis le dessin de rectangles rouge et bleu — le tout sans jamais lancer Photoshop.

## Réponses rapides
- **Quelle est la classe principale pour créer un fichier PSD ?** `PsdImage`
- **Quelle méthode efface la couleur d'arrière‑plan d'un calque ?** `Graphics.clear(Color)`
- **Comment dessiner un rectangle rouge ?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Ai‑je besoin d’une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence est requise pour la production.
- **Puis‑je manipuler des fichiers PSD existants avec la même API ?** Oui, Aspose.PSD prend en charge la modification complète des PSD.

## Dessiner un rectangle rouge dans un fichier PSD

Dessiner un rectangle rouge consiste à utiliser l’objet `Graphics` pour rendre une forme rectangulaire remplie ou contournée avec la couleur rouge sur un calque spécifique d’une image PSD. Cette opération est courante pour mettre en évidence des zones, créer des espaces réservés ou ajouter des graphiques simples de manière programmatique.

## Pourquoi utiliser Aspose.PSD pour Java afin de manipuler des fichiers PSD ?

Aspose.PSD pour Java prend en charge **plus de 50 formats d’entrée et de sortie**, peut traiter des fichiers PSD de plusieurs centaines de pages sans charger le fichier complet en mémoire, et fonctionne sur toute plateforme compatible Java 8 ou supérieure. Son moteur de traitement d’images côté serveur élimine le besoin de Photoshop, réduit les coûts de licence et permet des flux de travail automatisés capables de gérer jusqu’à **10 Go** de données d’image par heure sur une VM modeste.

## Prérequis

- Java Development Kit (JDK) 8 ou ultérieur installé sur votre machine.  
- Bibliothèque Aspose.PSD pour Java. Vous pouvez la télécharger depuis la [Documentation Aspose.PSD pour Java](https://reference.aspose.com/psd/java/).

## Importer les packages

Les instructions `import` font entrer les classes requises dans le scope afin que vous puissiez travailler avec les images PSD, les calques, les couleurs et les graphiques.

La classe `PsdImage` est l’objet de haut niveau d’Aspose.PSD qui représente un fichier PSD unique en mémoire.  
`Graphics` fournit des primitives de dessin telles que lignes, rectangles et ellipses.  
`Color` et `Pen` vous permettent de spécifier les couleurs de trait et l’épaisseur.  
La classe `Layer` représente un calque d’image individuel au sein d’un document PSD.  
La classe `Rectangle` définit la position et la taille d’une zone rectangulaire utilisée pour les opérations de dessin.  
La classe `SolidBrush` remplit les formes avec une couleur unie.

## Quelle est la première étape pour créer un document PSD ?

Vous instanciez `PsdImage` en fournissant la largeur et la hauteur du canevas en pixels, ce qui crée une structure de fichier PSD vide. Après avoir configuré les calques ou l’arrière‑plan initiaux, invoquez la méthode `save` avec un chemin de fichier pour écrire le document sur le disque. Cela prépare l’image pour les opérations d’édition ultérieures.

## Étape 1 : Créer un nouveau document

Tout d’abord, créez un nouveau document PSD avec la taille de canevas souhaitée. Ce document hébergera le calque sur lequel nous dessinerons.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Comment ajouter un nouveau calque vierge à une image PSD ?

Commencez par créer une nouvelle instance `Layer` avec la même largeur et hauteur que le `PsdImage` parent. Ajoutez ensuite ce calque à la collection `Layers` de l’image à l’aide de la méthode `add`. Une fois le calque intégré à l’image, récupérez son objet `Graphics` pour effectuer les opérations de dessin ; sans cette étape, les dessins n’apparaîtront pas.

## Étape 2 : Ajouter un calque

Ensuite, ajoutez un nouveau calque vierge qui couvre toute la largeur et la hauteur de l’image. Les calques sont essentiels pour séparer les opérations de dessin.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Quel est le but d’effacer la couleur d’arrière‑plan d’un calque ?

Appeler `Graphics.clear` avec une `Color` spécifique remplit l’ensemble du calque avec cette couleur, réinitialisant ainsi toutes les données de pixels. Cela garantit que tout contenu antérieur est supprimé et que le calque démarre à partir d’un arrière‑plan connu, évitant ainsi les transparences ou mélanges de couleurs inattendus lorsque le PSD est ouvert ou édité plus tard dans Photoshop.

## Étape 3 : Dessiner des formes

Nous utiliserons la classe `Graphics` pour manipuler les données de pixels du calque. Voici trois exemples illustrant l’effacement de l’arrière‑plan et le dessin de rectangles avec différentes couleurs.

### Effacer la couleur du calque (définir l’arrière‑plan en jaune)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### Dessiner un rectangle rouge (objectif principal)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Dessiner un rectangle bleu (exemple supplémentaire)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## Comment enregistrer le fichier PSD modifié sur le disque ?

Utilisez la méthode `save` sur l’objet `PsdImage`, en passant le chemin complet du fichier et, éventuellement, en spécifiant le format d’image souhaité (PSD par défaut). Cette opération écrit tous les calques, masques et commandes de dessin dans un seul fichier PSD conforme aux spécifications Photoshop, permettant son ouverture sans avertissements.

## Étape 4 : Enregistrer les modifications

Enfin, écrivez l’image PSD modifiée sur le disque. Le fichier contiendra le nouveau calque ainsi que les formes dessinées.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Problèmes courants et solutions

- **Calque non visible après le dessin :** Assurez‑vous que le calque est ajouté à l’image **avant** de créer l’objet `Graphics`. La surface de dessin doit être attachée à un calque valide.
- **Les couleurs apparaissent incorrectes :** Vérifiez que vous utilisez `Color.getRed()` (ou `Color.getBlue()`) plutôt que de construire une valeur RGB personnalisée dépassant la plage 0‑255.
- **Fichier non enregistré :** Confirmez que le chemin `outputDir` existe et que l’application possède les permissions d’écriture. Sous Linux, il peut être nécessaire d’ajuster la propriété du dossier ou d’utiliser `Files.createDirectories`.
- **Ralentissement des performances sur les gros fichiers :** Utilisez `setLoadOptions` de `PsdImage` pour charger uniquement les canaux requis, réduisant la consommation mémoire pour les PSD de plus de 200 Mo.

## Questions fréquemment posées

**Q1 : Puis‑je utiliser Aspose.PSD pour Java afin de manipuler des fichiers PSD existants ?**  
**R1 :** Oui, Aspose.PSD pour Java offre une fonctionnalité étendue pour éditer et manipuler des fichiers PSD existants, y compris le réordonnancement des calques, les ajustements de masques et le dessin vectoriel.

**Q2 : Où puis‑je trouver du support pour Aspose.PSD pour Java ?**  
**R2 :** Vous pouvez consulter le [Forum Aspose.PSD pour Java](https://forum.aspose.com/c/psd/34) pour obtenir de l’aide communautaire et les réponses officielles d’Aspose.

**Q3 : Existe‑t‑il une version d’essai gratuite d’Aspose.PSD pour Java ?**  
**R3 :** Oui, vous pouvez accéder à la version d’essai gratuite [ici](https://releases.aspose.com/). L’essai comprend toutes les fonctionnalités mais ajoute un filigrane aux fichiers enregistrés.

**Q4 : Comment puis‑je acheter une licence pour Aspose.PSD pour Java ?**  
**R4 :** Vous pouvez acheter une licence sur la [Page d’achat Aspose.PSD](https://purchase.aspose.com/buy). Les options de licence comprennent les licences perpétuelles, d’abonnement et site.

**Q5 : Des licences temporaires sont‑elles disponibles pour Aspose.PSD pour Java ?**  
**R5 :** Oui, vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

## Questions fréquemment posées supplémentaires

**Q : Puis‑je dessiner d’autres formes que des rectangles ?**  
**R :** Oui, la classe `Graphics` prend également en charge le dessin d’ellipses, de lignes et de chemins personnalisés via la méthode `drawPath`.

**Q : Aspose.PSD prend‑il en charge la transparence dans les formes dessinées ?**  
**R :** Absolument ; vous pouvez utiliser `SolidBrush` avec une couleur ARGB pour inclure la transparence alpha, permettant des superpositions semi‑transparentes.

**Q : Est‑il possible de modifier l’opacité d’un calque ?**  
**R :** Oui, chaque objet `Layer` possède une méthode `setOpacity` qui accepte une valeur de 0 à 255, offrant un contrôle fin de la transparence du calque.

**Q : Comment charger un fichier PSD existant au lieu d’en créer un nouveau ?**  
**R :** Utilisez `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` avant de manipuler les calques. L’image chargée conserve tous les calques et masques d’origine.

## Conclusion

Vous avez maintenant maîtrisé **comment dessiner un rectangle** et manipuler les calques à l’intérieur d’un fichier PSD en utilisant Aspose.PSD pour Java. En créant un document, en ajoutant un calque, en effaçant son arrière‑plan et en dessinant avec l’API `Graphics`, vous pouvez automatiser d’innombrables tâches de conception graphique côté serveur. Expérimentez avec différents stylos, pinceaux et effets de calque pour étendre cette base à des pipelines de génération d’images entièrement fonctionnels.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Comment dessiner des formes Java – Opérations d’image de base](/psd/java/basic-image-operations/)
- [Redimensionnement simple avec Aspose.PSD – Bibliothèque de manipulation d’images Java](/psd/java/basic-image-operations/simple-resizing/)
- [Recadrer une image par rectangle avec Aspose.PSD pour Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**Last Updated:** 2026-06-13  
**Testé avec:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Auteur:** Aspose